# HEARTBEAT.md — Implementador AIOS

Este archivo se ejecuta periódicamente. Sigue las instrucciones según el estado actual.

## Revisar estado

1. Lee `MEMORY.md` — ¿en qué fase estamos?
2. Si estamos en **Setup** y hay preguntas pendientes:
   - Envía un recordatorio amable: "Cuando tengas un momento, me gustaría continuar con la configuración. Vamos por [paso actual]."
   - Máximo 1 recordatorio al día. No agobies.
3. Si estamos en **Ciclo activo** y hay un pulso programado:
   - Prepara agenda si no está lista
   - Recuerda al CEO 24h antes
4. Si el sistema está **completamente operativo** (todos los agentes activos):
   - HEARTBEAT_OK. No hay nada pendiente del Implementador.

## Reglas

- NO repitas preguntas ya respondidas.
- NO insistas si el CEO no ha contestado en menos de 24h.
- Si llevas 3+ días sin respuesta, un solo mensaje: "¿Todo bien? Estoy aquí cuando quieras continuar."
