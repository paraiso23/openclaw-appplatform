---
name: organiama
description: Mapea el equipo directivo, responsabilidades y bloqueos departamentales
---

# Skill: OrganiAma — Mapa de Responsabilidades

## Cuándo se activa

Después de completar el Setup (Horizonte listo). El CEO ya confía en el sistema.

## Qué hace

Extrae la estructura organizacional: quiénes son los directivos, qué hacen, qué bloquea su trabajo. Con esta información se crean los agentes personales.

## Secuencia

### Paso 1: Tamaño del equipo

> "¿Cuántas personas forman tu equipo directivo? Las que toman decisiones o la gente con la que necesitas coordinarte cada semana."

### Paso 2: Perfil de cada persona (repetir por cada una)

> "Cuéntame sobre [persona N]:
> - ¿Nombre?
> - ¿Qué rol tiene?
> - ¿De qué es responsable?
> - ¿Cuáles son sus bloqueos más frecuentes?
> - ¿Usa Telegram?"

Extraer para cada persona:
- nombre
- rol
- departamento
- responsabilidades (lista)
- bloqueos típicos (lista)
- canal preferido (telegram/slack/otro)
- telegram_id (si disponible, si no, se configura después)

### Paso 3: Dependencias

> "¿Hay dependencias fuertes entre departamentos? Por ejemplo: ¿ventas depende de que finanzas apruebe presupuestos? ¿Tecnología bloquea a operaciones?"

### Paso 4: Confirmación

Presentar el mapa al CEO para validación:

> "Este es tu OrganIAma — el mapa de tu equipo:
>
> 👤 [Nombre] — [Rol]
>    Responsable de: [lista]
>    Bloqueos: [lista]
>
> 👤 [Nombre] — [Rol]
>    ...
>
> ¿Es correcto? ¿Falta alguien?"

## Persistencia

Crear `data/organiama.md` con el mapa visual.
Crear `data/equipo/[nombre].json` por cada persona:

```json
{
  "nombre": "...",
  "rol": "...",
  "departamento": "...",
  "responsabilidades": ["..."],
  "bloqueos": ["..."],
  "canal_dm": "telegram",
  "telegram_id": null,
  "bot_token": null,
  "onboarded": false
}
```

Actualizar `MEMORY.md` → Equipo mapeado.

## Transición

> "Excelente. Ahora voy a crear los agentes del sistema. Primero Strategy (el cerebro estratégico) y el PM (el coordinador). Después, un asistente personal para cada miembro del equipo. ¿Procedo?"

Pasar al skill `crear-agente`.
