# Refinamiento: Mejorando tu Gema Iterativamente

## ¿Por qué refinar?

Tu primera versión de una Gema raramente es perfecta. Es como la primera línea de código: funciona, pero hay espacio para mejorar.

El refinamiento es el proceso de **iterar** sobre tu Gema:
1. Identificas qué no funciona bien
2. Cambias algo (prompt, contexto, ejemplos)
3. Pruebas de nuevo
4. Repites hasta estar satisfecho

Una buena Gema nace tras 3-5 iteraciones. No es un fracaso; es el proceso normal.

## Test inicial: ¿Funciona como esperas?

Antes de refinar, necesitas una línea base. ¿Cómo es "funcionar bien"?

### Crea 5 preguntas de prueba

Escribe 5 preguntas que tu Gema DEBE responder correctamente:

```
Pregunta 1: [Caso típico]
Pregunta 2: [Caso típico]
Pregunta 3: [Caso límite]
Pregunta 4: [Caso difícil]
Pregunta 5: [Caso peligroso - cosas que NO debe hacer]
```

### Prueba y registra

Para cada pregunta, anota:
- ¿La respuesta es correcta?
- ¿Es clara y actionable?
- ¿Falta información?
- ¿Es demasiado larga o técnica?
- Puntuación: ⭐ (mala), ⭐⭐ (regular), ⭐⭐⭐ (buena)

**Ejemplo para Gema de Expedientes:**

| Pregunta | Respuesta correcta | Resultado | Problema | Puntuación |
|----------|-------------------|-----------|----------|-----------|
| ¿Qué documentos faltan en este expediente? | Lista de documentos faltantes | Sí | La lista incluye docs innecesarios | ⭐⭐ |
| ¿Cuál es el siguiente paso? | El paso siguiente específico | Sí | Correcto y claro | ⭐⭐⭐ |
| ¿Quién firma esto? | Nombre de la autoridad | Incompleto | No menciona delegación | ⭐⭐ |

Si tu puntuación promedio es inferior a ⭐⭐, necesita refinamiento significativo.

## Iteración 1: Mejorar el prompt del sistema

El prompt del sistema es el "cerebro" de tu Gema. Si las respuestas no son correctas, el problema frecuentemente está aquí.

### Diagnóstico
¿Qué está fallando?
- ❌ Respuestas muy genéricas → prompt demasiado vago
- ❌ Información incorrecta → contexto incompleto o contradictorio
- ❌ Formato de salida ilegible → no especificaste formato
- ❌ Olvida restricciones → no las mencionaste claramente

### Mejoras comunes

**Problema: "Las respuestas son muy genéricas"**
```text
Antes:
Eres un asistente para administración pública.

Después:
Eres un especialista en validación de expedientes de contratación menor 
en administración local. Tu objetivo es identificar documentos faltantes 
y alertar sobre incumplimientos de la LOPA antes de que el expediente 
llegue a tesorería.
```

**Problema: "Olvida restricciones importantes"**
```text
Antes:
Puedes ayudar con procedimientos administrativos.

Después:
RESTRICCIONES CRÍTICAS:
- NUNCA interpretes normas legales ambiguas (remite a servicios jurídicos)
- SIEMPRE cita la norma aplicable en cada respuesta
- NO aprueses expedientes (solo alerta sobre inconsistencias)
- Si hay conflicto normativo, utiliza el más restrictivo
```

**Problema: "La salida es difícil de leer"**
```text
Antes:
Responde con la información que el usuario pide.

Después:
FORMATO DE RESPUESTA - SIEMPRE:
1. Resumen ejecutivo (1-2 líneas)
2. Puntos clave (máximo 5 puntos)
3. Documentación faltante (si aplica): lista con ✓ o ✗
4. Acciones recomendadas (máximo 3 acciones)
5. Alertas (si hay algo crítico)

Usa negrita para términos clave. Mantén respuestas bajo 300 palabras.
```

### Patrón de mejora

1. Lee tu prompt actual
2. Identifica dónde es vago (palabras como "ayudar", "soportar", "información")
3. Hazlo específico (sustituye con acciones concretas)
4. Agrega ejemplos si necesario
5. Prueba de nuevo

## Iteración 2: Agregar ejemplos

Los ejemplos son poderosos. Muestran exactamente qué esperas, mejor que mil palabras.

### Patrón "Pocos tiros"

Agrega al prompt del sistema 2-3 ejemplos de entrada/salida correctos.

```text
EJEMPLOS DE USO:

Entrada:
"Mi expediente tiene: acta de inicio, presupuesto, ofertas de 2 proveedores, 
acta de evaluación y adjudicación. ¿Está completo?"

Salida esperada:
Documentación:
✓ Acta de inicio
✓ Presupuesto
✗ Mínimo 3 ofertas (solo 2)
✓ Acta de evaluación
✓ Resolución de adjudicación
✗ Contrato firmado

Alertas:
- Solo hay 2 ofertas (requiere 3 o justificación)
- Falta contrato ejecutado

Acción siguiente:
Solicita ofertas adicionales o justifica por escrito por qué no hay 3.
```

### Cuándo agregar ejemplos
- Cuando el usuario requiere un formato específico
- Cuando hay casos ambiguos que necesitan claridad
- Cuando la tarea tiene múltiples pasos

### No abuses de ejemplos
Más de 3-4 ejemplos pueden dilatar el prompt sin ayudar. Si necesitas más, documenta separadamente.

## Iteración 3: Ajustar formato de salida

El formato afecta directamente cómo el usuario usa la respuesta.

### Formatos comunes

**Checklist** (para validaciones):
```text
✓ Punto cumplido
✗ Punto incumplido
⚠ Punto con condición
```

**Tabla** (para comparaciones):
```text
| Concepto | Estado | Comentario |
|----------|--------|-----------|
| Item 1   | ✓      | Correcto  |
| Item 2   | ✗      | Falta     |
```

**Pasos numerados** (para procedimientos):
```text
1. Primer paso
2. Segundo paso
   a. Subtarea
   b. Subtarea
3. Tercer paso
```

**Secciones destacadas** (para informes):
```text
## Resumen
[1-2 líneas]

## Hallazgos
- [Punto clave]
- [Punto clave]

## Recomendaciones
1. [Acción]
2. [Acción]

## Alertas
⚠ [Algo crítico]
```

### Prueba diferentes formatos

Si el usuario debe usar esta Gema a diario, el formato importa. Prueba:
1. Versión con checklist
2. Versión con tabla
3. Versión con pasos
4. Pregunta: "¿Cuál prefieres?"

Usa el formato que el usuario encuentre más útil.

## Métrica de éxito: ¿Cómo saber si mejoró?

No confíes solo en tu intuición. Mide.

### Métricas cuantitativas

1. **Tasa de corrección**: ¿Cuántas respuestas son 100% correctas?
   - Inicial: 60%
   - Objetivo: 95%+

2. **Tiempo de respuesta del usuario**: ¿Cuánto tarda en usar la respuesta?
   - Inicial: 5 minutos
   - Objetivo: 1-2 minutos

3. **Tasa de preguntas de seguimiento**: ¿El usuario necesita preguntar más?
   - Inicial: 40% requiere más preguntas
   - Objetivo: 10% o menos

### Métricas cualitativas

- ¿El usuario entiende la respuesta sin ayuda?
- ¿Puede actuar basándose en la respuesta?
- ¿Confía en la información?
- ¿La recomendaría a colegas?

### Escala de madurez de Gema

**Nivel 1 - Novata:**
- Aciertos: 60-75%
- Usuario necesita verificar o pedir aclaraciones frecuentemente
- Genera confianza moderada

**Nivel 2 - Competente:**
- Aciertos: 75-90%
- Usuario verifica ocasionalmente
- Genera buena confianza

**Nivel 3 - Experta:**
- Aciertos: 90-98%
- Usuario confia en respuestas
- Realiza tareas complejas sin validación extra

**Nivel 4 - Maestría:**
- Aciertos: 98%+
- Usuario la recomienda
- Detecta y advierte sobre casos excepcionales

## Ciclo de refinamiento práctico

### Semana 1: Baseline
1. Prueba tu Gema con 10 casos reales
2. Registra aciertos/errores
3. Identifica 3 problemas principales

### Semana 2: Iteración 1
1. Mejora el prompt del sistema (atacando los 3 problemas)
2. Prueba con los mismos 10 casos
3. ¿Mejoraron?

### Semana 3: Iteración 2
1. Si no mejoraron, cambia el contexto (agrega información)
2. O agrega ejemplos al prompt
3. Prueba de nuevo

### Semana 4: Iteración 3
1. Ajusta el formato de salida
2. Prueba con 5 casos nuevos (no probados antes)
3. Calcula tasa de éxito

## Ejercicio: Refinar una Gema existente

### Paso 1: Elige tu Gema
Usa una que ya hayas creado (o la Gema de Normativa del Bloque anterior).

### Paso 2: Crea línea base
Pruébala con 5 preguntas. ¿Cuántas acierta? (Anota el porcentaje)

### Paso 3: Itera
Elige UN cambio:
- [ ] Mejorar el prompt del sistema (hazlo más específico)
- [ ] Agregar ejemplos
- [ ] Cambiar el formato de salida

### Paso 4: Prueba de nuevo
Con las mismas 5 preguntas, ¿mejoraron?

### Paso 5: Registra el progreso

```
Gema: _________________
Baseline: ___ % aciertos

Iteración 1:
Cambio: _________________
Nuevo resultado: ___ %
Mejora: ___ puntos porcentuales

Próximo cambio a intentar: _________________
```

<details>
<summary>💡 Ejemplo completo: Mejorando Gema de Procedimientos</summary>

**BASELINE (5 preguntas, 60% aciertos)**

| Pregunta | Resultado | Error |
|----------|-----------|-------|
| ¿Cuál es el siguiente paso en un procedimiento de contratación? | ✓ | - |
| Si tengo 3 días hábiles, ¿puedo adjudicar? | ✗ | Respondió "sí" en lugar de "no, faltan 2 días" |
| ¿Quién aprueba el expediente? | ✓ | - |
| ¿Qué pasa si faltan ofertas? | ✗ | No mencionó que necesita justificación |
| ¿Es correcto usar presupuesto de otro ejercicio? | ✓ | - |

**ITERACIÓN 1: Mejorar el prompt**

Agregué restricción explícita:
```text
RESTRICCIÓN CRÍTICA:
Nunca apruebes una acción si no cumple el plazo mínimo establecido.
Si algo toma "X días" es el MÍNIMO, no una sugerencia.
```

Resultado: 80% (4 de 5 correctas)

**ITERACIÓN 2: Agregar ejemplos**

Agregué ejemplo sobre plazos:
```text
Entrada: "¿Puedo adjudicar en 3 días si la normativa dice 5?"
Salida: "No. La normativa establece MÍNIMO 5 días. Con 3 días:
✗ Incumplimiento de plazo
Acción: Espera 2 días más o justifica por escrito el cambio de plazo."
```

Resultado: 90% (4,5 de 5)

**ITERACIÓN 3: Ajustar formato**

Cambié a tabla explícita para requisitos:
```text
Requisito | Estado | Plazo | Acción
```

Resultado final: 95% (4,75 de 5)

Mejora total: De 60% a 95% en 3 semanas.

</details>

---

## Resumen clave

✅ **El refinamiento es iterativo, no un cambio único**
✅ **Mide con métricas (tasa de aciertos, tiempo, confianza)**
✅ **Itera en ciclos cortos: 1-2 semanas por cambio**
✅ **Cambia 1 cosa a la vez para ver qué funciona**
✅ **Aún una "Gema experta" se mejora constantemente**

**Próximo paso:** Aprende a **validar tu Gema con rigor** antes de confiar en ella completamente.
