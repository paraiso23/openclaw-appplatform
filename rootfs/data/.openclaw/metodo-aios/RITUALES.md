# Rituales — Método AIOS

## Rituales automáticos (cron)

| Ritual | Frecuencia | Hora | Agente |
|--------|-----------|------|--------|
| Briefing matutino | L–V | 30 min antes del inicio | Personal → cada usuario |
| Closure nocturno | L–V | Hora de cierre del usuario | Personal → cada usuario |
| Context Sentinel | Cada 2h | Active hours | Strategy → scan de datos |
| Scorecard semanal | Viernes | 18:00 | Strategy → genera, PM publica |

## Rituales facilitados (humano + IA)

### Reunión de Pulso (semanal, 40 min)

1. **Pre-pulso** (lunes): Strategy genera agenda basada en datos
2. **Envío** (24h antes): PM envía agenda a todos los asistentes
3. **Reunión**: Equipo directivo + Strategy (observa y captura)
4. **Post-reunión**: PM envía resumen, valoración, estado del ciclo
5. **Persistencia**: Acta + compromisos se suben a la base de datos
6. **Seguimiento**: Strategy monitoriza compromisos en siguientes heartbeats

### Reunión Mensual (fin de ciclo, 2h)

1. Pitch de estado trimestral del CEO
2. Revisión OKRs: conclusiones y aprendizajes
3. Definición de nuevos OKRs
4. Informe Q&A del estado de la IA
5. Impacto de la IA en empleados
6. Valoración ética
7. Q&A y actualizaciones
8. Propuesta para siguiente trimestre con IA

## Notas sobre rituales

- Los rituales **no se saltan**. Son la base del contrato cerrado.
- El implementador verifica que se cumplan durante los primeros 2 ciclos.
- OKRs mal nombrados, no concretos o sobredimensionados crean frustración. Strategy puede proponer ajustes.
