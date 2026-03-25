---
name: ciclo
description: Gestiona los ciclos del método AIOS (Onboarding → Alineación → Optimización → Consolidación → Automatización)
---

# Skill: Ciclo — Gestión de Ciclos AIOS

## Cuándo se activa

Después de crear todos los agentes y que el CEO confirme que funcionan. Este skill gestiona la evolución del sistema a largo plazo.

## Los 5 ciclos

Leer `metodo-aios/CICLOS.md` para la definición completa. Resumen:

| Ciclo | Nombre | Meta |
|-------|--------|------|
| 1 | Onboarding | OKRs definidos, 4 pulsos completados, equipo usando el sistema |
| 2 | Alineación | Bloqueos visibles, comunicación mejorada, marco de responsabilidad |
| 3 | Optimización | Coordinación activa, reuniones 7/10, agenda interiorizada |
| 4 | Consolidación | IA teniendo impacto medible, implementador imprescindible |
| 5 | Automatización | Mejoras evidentes, automatizaciones activas, IA como activo |

## Acciones del Implementador por ciclo

### Ciclo 1 (activo post-setup)

El Implementador guía activamente:

1. **Pre-pulso** (24h antes del jueves):
   - Generar agenda con Strategy
   - Enviar recordatorio al CEO: "Mañana tenemos pulso. Agenda preparada."
2. **Post-pulso** (viernes):
   - Verificar que el acta fue subida
   - Enviar valoración del pulso al CEO
   - Sugerir mejoras

Repetir 4 veces (4 pulsos semanales).

3. **Mensual** (fin de ciclo):
   - Preparar informe del ciclo
   - Revisar OKRs con Strategy
   - Proponer ajustes al CEO

### Ciclos 2–3

El Implementador reduce intervención:
- Solo actúa si Strategy detecta anomalías
- Envía resumen quincenal de salud del sistema
- Propone transiciones de ciclo cuando se cumplen criterios

### Ciclos 4–5

El Implementador es passive:
- Monitoriza pero no interviene
- Strategy y PM gestionan autónomamente
- El Implementador actúa solo si el CEO lo solicita

## Criterios de transición

Para avanzar de ciclo, Strategy debe confirmar que se cumplen los indicadores definidos en `metodo-aios/CICLOS.md`.

El Implementador propone la transición al CEO:
> "Tu equipo ha alcanzado los indicadores del Ciclo [N]. Recomiendo avanzar al Ciclo [N+1]: [nombre]. ¿Procedo?"

## Persistencia

Actualizar `MEMORY.md`:
- Ciclo actual
- Pulsos completados
- Scorecard promedio
- Fecha de inicio del ciclo
