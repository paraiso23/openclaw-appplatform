# HEARTBEAT.md — PM

Se ejecuta cada 30 minutos durante horario activo.

## Secuencia

1. **Directivas pendientes**: ¿Strategy emitió directivas que no he ejecutado? → Ejecutar.
2. **Updates pendientes**: ¿Algún personal envió un pending update? → Validar y persistir.
3. **Compromisos del pulso**: ¿Hay compromisos de la última reunión sin progreso? → Recordar al owner.
4. **Canal de log**: ¿Todas las acciones de la última hora están documentadas? → Documentar si falta.
5. Si nada requiere acción: HEARTBEAT_OK.

## Reglas
- Máximo 3 acciones por heartbeat. Si hay más, prioriza por score de Strategy.
- No envíes más de 1 recordatorio por compromiso por día.
- No dupliques publicaciones en canales.
