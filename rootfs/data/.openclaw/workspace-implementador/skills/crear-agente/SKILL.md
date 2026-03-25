---
name: crear-agente
description: Genera y activa agentes del sistema (Strategy, PM, Personales) a partir de templates
---

# Skill: Crear Agente

## Cuándo se activa

Después del OrganiAma. El CEO ha confirmado su equipo y quiere proceder con la creación de agentes.

## Qué hace

Copia templates desde `templates/`, rellena variables con los datos del `data/`, y añade los agentes al `openclaw.json`.

## Orden de creación

1. **Strategy** — primero, porque debe escanear datos antes de que el PM opere
2. **PM** — segundo, porque coordina los personales
3. **Personales** — uno por cada miembro del equipo, empezando por el CEO

## Proceso por agente

### Strategy

1. Copiar `templates/workspace-strategy/` → `workspace-strategy/`
2. Leer `data/horizonte.md` → inyectar en `workspace-strategy/HORIZONTE.md`
3. Añadir config al `openclaw.json` usando `templates/openclaw-fragments/agent-strategy.jsonc`
4. Confirmar al CEO: "🧠 Strategy creado. Empezará a analizar tus datos."

### PM

1. Copiar `templates/workspace-pm/` → `workspace-pm/`
2. Configurar sub-agentes: strategy + todos los personales del equipo
3. Añadir config al `openclaw.json` usando `templates/openclaw-fragments/agent-pm.jsonc`
4. Confirmar: "🎯 PM creado. Será tu coordinador en los canales de equipo."

### Personal (repetir por cada miembro del equipo)

1. Leer `data/equipo/[nombre].json`
2. Copiar `templates/workspace-personal/` → `workspace-personal-[nombre]/`
3. Rellenar variables en SOUL.template.md:
   - `{{NOMBRE}}` → nombre
   - `{{ROL}}` → rol
   - `{{FOCO_PRINCIPAL}}` → responsabilidades[0]
   - `{{DESCRIPCION_TONO}}` → inferir del rol (CEO=ejecutivo, CTO=técnico, CFO=preciso, Ventas=acción)
   - `{{HORARIO_INICIO}}` / `{{HORARIO_FIN}}` → defaults por timezone
4. Rellenar USER.template.md con datos del perfil
5. Preguntar al usuario por preferencias de tono y horarios (breve, 3 preguntas):
   - "¿Cómo prefiere [nombre] que le hable su asistente?"
   - "¿Horarios de deep work?"
   - "¿Bot de Telegram listo? (token)"
6. Añadir config al `openclaw.json` usando `templates/openclaw-fragments/agent-personal.jsonc`
7. Añadir binding Telegram usando `templates/openclaw-fragments/binding-telegram.jsonc`
8. Confirmar: "👤 Asistente de [nombre] creado."

## Persistencia

- Actualizar `MEMORY.md` → marcar cada agente como creado
- Actualizar `data/equipo/[nombre].json` → `"onboarded": true`

## Transición

Cuando todos los agentes estén creados:
> "✅ Todos los agentes están configurados:
> - 🧠 Strategy — analizando tus datos
> - 🎯 PM — coordinando en [canal]
> - 👤 [N] asistentes personales activos
>
> Vamos a hacer una prueba rápida para verificar que todo funciona.
> 1. Envía un mensaje a tu personal por Telegram
> 2. Verifica que el PM aparece en tu canal de equipo
>
> Cuando confirmes, arrancamos el Ciclo 1 del método AIOS."

Pasar al skill `ciclo`.
