---
name: setup
description: Extrae el Horizonte de la empresa del CEO — visión, propósito, valores, bloqueos
---

# Skill: Setup — Extracción del Horizonte

## Cuándo se activa

Al inicio del onboarding, cuando `MEMORY.md` tiene `Fase: sin_iniciar` o cuando el Setup no está completo.

## Qué hace

Guía al CEO a través de una serie de preguntas para extraer la información fundacional de su empresa. Esto crea el ADN que alimenta a Strategy.

## Secuencia de preguntas

Haz las preguntas **de una en una**. Espera la respuesta antes de la siguiente. Si el CEO da información parcial, confirma lo que entendiste y pide lo que falta.

### Bloque 1: La empresa

> "Para empezar, cuéntame sobre tu empresa. ¿Cómo se llama y a qué se dedica?"

Extraer: nombre, sector, tamaño aproximado, antigüedad.

### Bloque 2: Propósito

> "¿Por qué existe esta empresa? ¿Cuál es la razón de ser más allá de facturar?"

### Bloque 3: High Goal

> "Si pudieras lograr UNA cosa con tu empresa, sin límites, ¿cuál sería?"

### Bloque 4: Visión a 3 años

> "Imagina tu empresa en 3 años. ¿Cómo se ve? Personas, productos, clientes, impacto."

### Bloque 5: Visión a 1 año

> "¿Qué debería haber pasado de aquí a 1 año para que consideres el año un éxito?"

### Bloque 6: Valores

> "¿Cuáles son los 3 a 5 valores reales que guían las decisiones de tu equipo? No los del manual corporativo — los que usáis de verdad."

### Bloque 7: Bloqueos

> "¿Cuáles son los 3 obstáculos principales que impiden que tu empresa crezca al ritmo que debería?"

### Bloque 8: Cierre

> "¿Hay algo más que quieras que el sistema sepa? Algo que no sale en las reuniones pero que es importante para entender la realidad del negocio."

## Persistencia

Al completar cada respuesta, actualizar `MEMORY.md` marcando el checkbox correspondiente.

Al completar el bloque completo, crear `data/horizonte.md` con toda la información estructurada y `data/empresa.json` con los datos básicos:

```json
{
  "nombre": "...",
  "sector": "...",
  "ceo": { "nombre": "...", "canal": "..." },
  "timezone": "...",
  "fecha_setup": "..."
}
```

## Transición

Cuando el Horizonte esté completo, informar al CEO:
> "Perfecto. Tengo una imagen clara de tu empresa. Ahora vamos a mapear tu equipo directivo para crear sus asistentes personales."

Pasar al skill `organiama`.
