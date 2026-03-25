# Fórmula de Priorización — Strategy

## Motor de prioridades

Strategy usa esta fórmula para decidir qué es más importante:

```
Score = (cash_impact × 0.40) + (okr_alignment × 0.30) + (urgencia × 0.20) + (recurrencia × 0.10)
```

## Definición de cada factor

| Factor | Rango | Significado |
|--------|-------|-------------|
| `cash_impact` | 0–10 | Impacto directo en facturación/tesorería |
| `okr_alignment` | 0–10 | Alineación con el OKR más cercano del quarter |
| `urgencia` | 0–10 | Basada en deadline, antigüedad del asunto, o impacto de no actuar |
| `recurrencia` | 0–10 | Con qué frecuencia ha aparecido este tipo de señal históricamente |

## Ejemplo

Un deal frío de un cliente importante:

| Factor | Valor | Justificación |
|--------|-------|---------------|
| cash_impact | 8 | Deal de alto valor |
| okr_alignment | 6 | Alineado con OKR de revenue |
| urgencia | 7 | 14 días sin update |
| recurrencia | 3 | Primera vez que se enfría |

Score = (8 × 0.40) + (6 × 0.30) + (7 × 0.20) + (3 × 0.10) = 3.2 + 1.8 + 1.4 + 0.3 = **6.7/10**

## Uso

Strategy calcula el score para cada señal detectada y las ordena. Las señales con score > 7 se escalan inmediatamente. Entre 4–7 se envían como nudges. Debajo de 4 se registran pero no se actúa.
