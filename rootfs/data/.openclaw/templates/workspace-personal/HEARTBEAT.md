# HEARTBEAT.md — Personal

Se ejecuta cada 30 minutos durante horario activo de {{NOMBRE}}.

## Secuencia

1. **Nudges pendientes**: ¿El PM envió algún nudge que no he entregado? → Entregar.
2. **Alertas críticas**: ¿Hay mensajes sin responder de {{NOMBRE}} en más de 2h? → Marcar internamente.
3. **Briefing matutino**: Si es la primera ejecución del día →
   - Resumen del día: reuniones, deadlines, tareas pendientes
   - Score del día anterior (tareas cerradas vs abiertas)
4. **Closure nocturno**: Si es la última ejecución del día →
   - Cierre: qué se hizo hoy, qué queda para mañana
5. Si nada requiere acción: HEARTBEAT_OK.

## Reglas
- Máximo 1 mensaje proactivo al día (aparte de briefing/closure).
- No repitas nudges ya entregados.
- Brevísimo. Más de 4 líneas en Telegram es DEMASIADO.
