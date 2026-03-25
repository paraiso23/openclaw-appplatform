# Umbrales de Desviación — Strategy

## Tabla de señales

Strategy monitoriza la base de datos periódicamente y detecta desviaciones según estos umbrales:

| Señal | Condición | Severidad | Acción |
|-------|-----------|-----------|--------|
| `deal_cold` | Deal sin update > 14 días | ⚠️ media | Nudge al owner |
| `deal_critical` | Deal sin update > 28 días | 🔴 alta | Escalado al CEO |
| `okr_stalled` | Score sin cambio > 14 días | ⚠️ media | Alerta en canal de pulso |
| `okr_behind` | Score < 40% a mitad de quarter | 🔴 alta | Plan de recuperación |
| `okr_at_risk` | Score < 70% a 2 semanas del cierre | 🔴 alta | Escalado CEO + agenda forzada |
| `bloqueo_aging` | Bloqueo sin resolución > 7 días | ⚠️ media | Nudge + bump en canal |
| `bloqueo_critical` | Bloqueo sin resolución > 14 días | 🔴 alta | Escalado CEO |
| `tarea_overdue` | Tarea pasada de deadline > 3 días | ⚠️ media | Nudge al owner |
| `acta_missing` | Reunión sin acta > 24h | ⚠️ media | Reminder al responsable |
| `pipeline_thin` | < 3 deals activos | 🔴 alta | Señal a responsable comercial |
| `reunion_low_score` | Scorecard reunión < 5/10 | ⚠️ media | Sugerencia de mejora |

## Configuración

Estos umbrales son **defaults**. Se pueden ajustar por organización editando este archivo.

## Niveles de acción

- **Nudge** (⚠️): Mensaje privado vía Personal del owner
- **Alerta** (⚠️→🔴): Publicación en canal del equipo
- **Escalado** (🔴): Notificación directa al CEO + punto forzado en próximo pulso
