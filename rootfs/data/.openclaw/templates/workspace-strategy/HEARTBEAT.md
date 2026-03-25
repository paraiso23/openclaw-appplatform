# HEARTBEAT.md — Strategy

Este archivo se ejecuta cada 2 horas durante horario activo.

## Secuencia

1. **Scan de datos**: Leer pipeline, OKRs, bloqueos, y tareas desde aios-bridge
2. **Evaluar umbrales**: Comparar datos con `metodo-aios/UMBRALES.md`
3. **Detectar señales**: Cualquier desviación que cruce un umbral
4. **Priorizar**: Calcular score según `metodo-aios/PRIORIDADES.md`
5. **Emitir directivas**: Enviar al PM las señales que requieran acción

## Comportamiento

- Si no hay señales: HEARTBEAT_OK (no generes output)
- Si hay señales nuevas: emite directiva por cada una
- Si hay señales repetidas del heartbeat anterior: NO las repitas. Solo emite señales nuevas o que hayan empeorado
- Nunca envíes más de 5 señales por heartbeat. Si hay más, prioriza las top 5

## Horizonte

Lee `HORIZONTE.md` para contextualizar las señales con la visión y valores de la empresa.
