# Estructura de Prompts: La Fórmula Mágica 🎯

📌 **Objetivo**: Aprender la estructura universal que hace que tus prompts funcionen. Una vez domines esto, podrás lograr casi cualquier cosa con la IA.

## 📚 Qué vamos a aprender

- Los 3 componentes clave de un buen prompt
- Por qué el orden importa
- Cómo aplicar la fórmula en casos reales
- Errores comunes y cómo evitarlos

---

## 🧠 Ejemplo guiado

**Comparemos dos enfoques:**

### ❌ Prompt sin estructura (malo):
```text
Analiza esta solicitud de licencia.
```

**Resultado**: Respuesta genérica, poco útil.

---

### ✅ Prompt con estructura (excelente):
```text
ROL: Eres un asistente especializado en análisis de solicitudes 
de licencia urbanística para administraciones públicas.

CONTEXTO: He recibido esta solicitud incompleta. Necesito saber 
exactamente qué falta antes de devolvérsela al ciudadano.

ENTRADA: "Solicito licencia para construcción de vivienda unifamiliar 
en parcela 123. Adjunto proyecto técnico."

TAREA: Identifica cada documento faltante según normativa estándar.

FORMATO: Lista con viñetas. Para cada documento faltante, explica 
brevemente por qué es obligatorio.
```

**Resultado**: Respuesta específica, estructurada, verificable.

---

## 💬 La Fórmula: Rol + Contexto + Entrada + Tarea + Formato

Esto es el **corazón del prompting efectivo**:

### 1. **ROL** (¿Quién eres?)
Define el expertise esperado de la IA.

**Ejemplos**:
```text
Eres un abogado administrativo especializado en derecho municipal.
Eres un redactor oficial de documentos administrativos.
Eres un analista de expedientes con 10 años de experiencia.
```

### 2. **CONTEXTO** (¿Por qué?)
Explica la situación, restricciones, objetivo final.

**Ejemplos**:
```text
Necesito una resolución para denegar una solicitud ilegal.
Estoy redactando una convocatoria para que sea clara para ciudadanos sin asesoría.
Debo resumir un expediente de 50 páginas manteniendo detalles críticos.
```

### 3. **ENTRADA** (¿Qué datos?)
Los datos concretos sobre los que trabajar.

**Ejemplos**:
```text
Texto de la ley: [pegar aquí]
Datos de la solicitud: [pegar aquí]
Expediente anterior: [pegar aquí]
```

### 4. **TAREA** (¿Qué hacer?)
La acción específica requerida.

**Ejemplos**:
```text
Identifica 3 posibles sesgos en esta decisión.
Resume los puntos principales de desacuerdo.
Propón 2 argumentos legales alternativos.
```

### 5. **FORMATO** (¿Cómo?)
Define cómo quieres la respuesta.

**Ejemplos**:
```text
Responde en tabla con columnas: Riesgo | Evidencia | Recomendación
Redacta como si fueras un memo oficial.
Lista con viñetas. Cada punto máximo 2 líneas.
```

---

## 🔄 Variantes según contexto administrativo

### Variante 1: Análisis de documentos
```text
ROL: Eres un clasificador de documentos administrativos.

CONTEXTO: Recibimos 200 solicitudes diarias. Necesito clasificarlas 
por urgencia para priorizar revisión.

ENTRADA: [Lista de 5 solicitudes de ejemplo]

TAREA: Clasifica cada solicitud por urgencia (CRÍTICA / ALTA / NORMAL / BAJA)
y explica brevemente por qué.

FORMATO: Tabla con columnas: Solicitud | Urgencia | Justificación
```

### Variante 2: Redacción oficial
```text
ROL: Eres redactor de comunicaciones municipales clara y legalmente correcta.

CONTEXTO: Debo comunicar a un ciudadano que su solicitud fue rechazada, 
pero de forma que entienda por qué sin necesidad de asesoría legal.

ENTRADA: Motivo del rechazo: "No cumple requisitos de acceso por 
situación económica establecida en normativa."

TAREA: Redacta el párrafo de comunicación del rechazo.

FORMATO: Máximo 3 párrafos. Lenguaje accesible pero formal.
```

### Variante 3: Mejora de procesos
```text
ROL: Eres consultor de eficiencia administrativa.

CONTEXTO: Nuestro proceso de tramitación de licencias toma 90 días. 
Queremos reducirlo manteniendo calidad.

ENTRADA: Descripción del proceso actual:
1. Recepción y clasificación (5 días)
2. Análisis técnico (30 días)
3. Solicitud de información adicional (20 días)
4. Resolución (15 días)
5. Notificación (20 días)

TAREA: Identifica 3 cuellos de botella reales y propón optimizaciones.

FORMATO: Tabla con: Fase | Tiempo actual | Problema | Solución | 
Tiempo estimado nuevo
```

---

## 🎯 Ejercicio: Construye tu propio prompt

**Propósito**: Practicar la estructura con un caso real.

**Situación**: Necesitas que la IA redacte un email recordatorio a los ciudadanos sobre un cambio en la convocatoria de ayudas.

**Tu tarea**: Completa estos 5 elementos:

1. **ROL**: Eres un ___________________
2. **CONTEXTO**: Necesito ___________________
3. **ENTRADA**: El cambio es ___________________
4. **TAREA**: Redacta ___________________
5. **FORMATO**: El email debe ___________________

---

<details>
<summary>💡 Ejemplo completado</summary>

1. **ROL**: Eres un redactor de comunicaciones claras para ciudadanía.

2. **CONTEXTO**: Hubo un cambio en la convocatoria de ayudas por error administrativo. 
Los ciudadanos ya presentaron solicitudes bajo las bases anteriores. Necesito un email 
que explique el cambio, disculpe la confusión, y explique qué deben hacer.

3. **ENTRADA**: Cambio: Se amplía el plazo de solicitud de 30 a 45 días y se reduce 
la documentación obligatoria (ya no es obligatorio adjuntar cotización previa).

4. **TAREA**: Redacta un email que:
   - Se disculpe por la confusión
   - Explique claramente qué cambió
   - Indique qué deben hacer quienes ya presentaron
   - Aclare que pueden presentar solicitudes nuevas o enmiendas

5. **FORMATO**: 
   - 1 párrafo de disculpa
   - 2 párrafos de cambios (uno para cada cambio)
   - 1 párrafo de acciones a tomar
   - Tono amable pero profesional
   - Máximo 300 palabras

</details>

---

## 🚀 Reto avanzado

**Desafío 1**: Reescribe un prompt mal estructurado.

Tengo esto: "Necesito una resolución de concesión de licencia."

Mejóralo usando la estructura completa. Piensa: ¿Qué falta?

---

**Desafío 2**: La estructura con conversación.

¿Qué pasaría si después de usar la estructura una vez, preguntas:

> "¿Podrías hacer la versión para ciudadanos sin asesoría?"

¿Cambiarías el ROL? ¿El FORMATO? Piensa cómo ajustarías cada elemento.

---

## ✅ Qué hemos aprendido

✓ La estructura **ROL + CONTEXTO + ENTRADA + TAREA + FORMATO** es universal  
✓ Cuanto más **específico**, mejor es el resultado  
✓ El **orden importa**: contexto primero, entrada después  
✓ Esta fórmula funciona para casi cualquier tarea  

---

## 📋 Checklist para tu próximo prompt

- [ ] Definí un ROL claro
- [ ] Expliqué el CONTEXTO (el "por qué")
- [ ] Proporcioné ENTRADA concreta (no genérica)
- [ ] Especifiqué TAREA sin ambigüedad
- [ ] Definí FORMATO esperado
- [ ] El prompt tiene ~200-300 palabras (estructurado pero no excesivo)
- [ ] Evité lenguaje vago ("haz algo bueno", "analiza bien")

**Siguiente paso**: Profundizamos en la claridad y especificidad. → 06-Claridad.md
