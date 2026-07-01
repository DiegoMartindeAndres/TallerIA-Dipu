# ¿Cómo funciona una IA? 🔧

📌 **Objetivo**: Entender el mecanismo interno de una IA (tokens, probabilidades, predicción). No necesitas ser matemático: usaremos analogías del mundo real.

## 📚 Qué vamos a aprender

- Qué son los tokens (las "palabras" de la IA)
- Cómo funciona la predicción de probabilidades
- Por qué a veces da respuestas extrañas
- Cómo ajustar el "nivel de creatividad"

---

## 🧠 Ejemplo guiado

Imagina que eres un operador de centralita que ha atendido miles de llamadas administrativas. Alguien te dice las primeras palabras de una llamada:

"Buenos días, llamo porque..."

**Tu cerebro automáticamente activa patrones**: ¿Cuáles son las continuaciones más probables?
- "...tengo una duda sobre un trámite" (60%)
- "...he perdido un documento" (25%)
- "...me han cobrado mal" (15%)

Eso es exactamente lo que hace una IA:

1. **Lee tokens** (fragmentos de texto)
2. **Calcula probabilidades** de qué viene después
3. **Elige la opción más probable** (o a veces una menos probable)
4. **Repite** hasta completar la respuesta

---

## 💬 Prompt explicado

```text
Contexto: Eres un asistente de redacción oficial para la Administración Pública.

Usuario: "Redacta el inicio de un memorándum administrativo 
sobre retrasos en tramitación"

Respuesta esperada: "Asunto: Comunicación sobre retrasos 
en tramitación de expedientes..."
```

**¿Cómo funciona internamente?**

1. **Tokenización**: El texto se divide en pequeños fragmentos:
   - "Redacta" → token 1
   - "el inicio" → tokens 2-3
   - "de un memorándum" → tokens 4-6

2. **Predicción progresiva**:
   - Token siguiente más probable: "Asunto:"
   - Token siguiente: (probable) "Comunicación"
   - Token siguiente: (probable) "sobre"

3. **Refinamiento**: Ajusta según el contexto acumulado (cómo está siendo el memorándum hasta ahora)

---

## 🔄 Variantes

**Variante 1 - Controlar la "temperatura" (creatividad):**
```text
Redacta una solicitud de licencia de obra.
Tono: Formal y conciso.

Importante: Usa frases estándar, no inventes expresiones nuevas.
```

**Variante 2 - Forzar mayor variedad:**
```text
Redacta una solicitud de licencia de obra.
Requiero 3 versiones diferentes, cada una con un enfoque distinto.
```

**Variante 3 - Limitar opciones (contexto específico):**
```text
Eres un sistema de clasificación de trámites administrativos.
Solo puedes usar estas categorías:
- Licencia urbanística
- Autorización ambiental
- Permiso de actividad
- Otro (especificar)

Clasifica: "Solicitud para reformar fachada de edificio histórico"
```

---

## 🎯 Ejercicio

**Propósito**: Entender cómo predice la IA.

**Tarea**: Completa estas frases como si fueras el cerebro de una IA:

1. "El ciudadano solicitó una licencia urbanística, por lo tanto..."
   - Opción más probable (70%): ________________
   - Opción menos probable (30%): ________________

2. "El trámite se retrasó porque..."
   - Opción más probable: ________________
   - Opción menos probable: ________________

3. "Para que la solicitud sea válida..."
   - Opción más probable: ________________
   - Opción menos probable: ________________

---

<details>
<summary>💡 Ejemplo de respuesta</summary>

**1. El ciudadano solicitó una licencia urbanística, por lo tanto...**
- Opción más probable (70%): "debe acompañar documentación técnica"
- Opción menos probable (30%): "podría recibir asesoría jurídica personalizada"

**2. El trámite se retrasó porque...**
- Opción más probable: "faltaba documentación incompleta"
- Opción menos probable: "la Administración decidió hacer un análisis ambiental exhaustivo"

**3. Para que la solicitud sea válida...**
- Opción más probable: "debe estar firmada por el solicitante"
- Opción menos probable: "necesita ser revisada por la junta directiva en pleno"

**¿Por qué esto importa?** Cada vez que das ejemplos a la IA, estás **reentrenando sus probabilidades** en esa conversación específica.

</details>

---

## 🚀 Reto avanzado

**Pregunta provocadora**: ¿Qué sucedería si la IA aprende que "siempre que aparece Javier López, el expediente se rechaza"?

- ¿Es sesgo de datos?
- ¿Debería el sistema revelarlo?
- ¿Cómo detectarías este problema?

**Segundo reto**: Investiga qué es la "temperatura" en modelos de lenguaje. ¿Cuándo querrías una temperatura alta vs baja en tu trabajo administrativo?

---

## ✅ Qué hemos aprendido

✓ Una IA es un **predictor de probabilidades**  
✓ Procesa texto en fragmentos llamados **tokens**  
✓ Su respuesta es tan buena como **la suma de sus predicciones previas**  
✓ Puedes influir en su "creatividad" mediante **contexto y ejemplos**

**Avance importante**: Esto significa que el cómo **formulas** tu pregunta es crítico. Lo veremos en el siguiente módulo.

---

## 📝 Nota técnica

*Para los curiosos: Los modelos modernos como GPT-4 usan transformers, que procesan texto en paralelo usando atención (attention). Pero el concepto de "predicción de tokens con probabilidades" sigue siendo el corazón del funcionamiento.*

**Siguiente paso**: Limitaciones reales → 03-Limitaciones.md
