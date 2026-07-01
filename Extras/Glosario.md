# 📚 Glosario: Términos y Conceptos Clave

**Definiciones accesibles de los términos más importantes del taller**

---

## 📖 Índice Alfabético

### A

**Alucinación**
Cuando la IA genera información falsa creyendo que es verdadera. No es un error del modelo, es su naturaleza: predice tokens probables, a veces incorrectamente.

*Ejemplo:* "¿Quién fue el presidente de España en 2050?" → IA inventa un nombre porque no tiene datos de futuro.

---

**Agente**
Sistema de IA que puede:
- Planificar pasos para resolver un objetivo
- Usar herramientas
- Mantener memoria
- Tomar decisiones de forma autónoma
- Iterar hasta completar la tarea

*Diferencia con chatbot:* El chatbot responde preguntas. El agente ejecuta tareas.

---

**API (Interfaz de Programación de Aplicaciones)**
Forma en que programas diferentes hablan entre sí. En IA, es cómo conectas herramientas con modelos.

*Ejemplo:* ChatGPT tiene una API que permite que otras aplicaciones usen su tecnología.

---

### C

**Chatbot**
Sistema de IA que:
- Responde preguntas
- Mantiene conversación
- No toma decisiones autónomas
- Espera input humano para cada paso

*Ejemplo:* ChatGPT en su versión base es un chatbot.

---

**Chain-of-Thought (Cadena de Pensamiento)**
Técnica donde pides a la IA que razone paso a paso en lugar de dar la respuesta directa.

```text
❌ Mal: ¿Cuál es el resultado?
✅ Bien: Razona paso a paso: primero..., segundo..., finalmente...
```

---

**Contexto**
Información adicional que proporcionas sobre el dominio o la tarea específica.

```text
Prompt sin contexto: Resume este documento
Prompt con contexto: Eres analista de normativa municipal. Resume este documento enfocándote en plazos y responsables.
```

---

**Contexto de Ventana (Window Context)**
La cantidad máxima de tokens que un modelo puede procesar a la vez.

*ChatGPT 4o:* 128K tokens ≈ 100,000 palabras  
*Claude 3 Opus:* 200K tokens ≈ 150,000 palabras

---

### E

**Embedding**
Representación matemática de un concepto. La IA convierte palabras en números multidimensionales.

*Concepto simple:* Imagina que cada palabra tiene coordenadas en el espacio. "Gato" y "Perro" estarían cerca. "Gato" y "Galaxia" lejos.

---

### F

**Fine-tuning (Ajuste Fino)**
Entrenar un modelo preexistente con tus datos específicos para mejorar su comportamiento.

*Caso real:* Entrenar ChatGPT con 500 ejemplos de tu estilo administrativo.

---

**Few-Shot Learning**
Técnica donde proporcionas algunos ejemplos para enseñar a la IA el patrón deseado.

```text
Ejemplo 1:
Entrada: "Hola"
Salida: "Buenos días"

Ejemplo 2:
Entrada: "¿Qué hora es?"
Salida: "Son las 14:30"

Ahora tú:
Entrada: "Gracias"
```

---

### G

**Gema**
Asistente especializado de IA con:
- Instrucciones del sistema específicas
- Contexto de dominio inyectado
- Ejemplos personalizados
- Capacidad de memoria conversacional

*Diferencia:* Una Gema sabe de administración municipal. Un prompt genérico no.

---

### H

**Hallucination**
Ver **Alucinación**

---

**Herramienta (Tool)**
Función que puede ejecutar un agente. Ejemplos:
- Búsqueda en internet
- Cálculos matemáticos
- Lectura de archivos
- Envío de emails
- Acceso a bases de datos

---

### I

**IA Generativa**
Sistema que **crea contenido nuevo** (texto, código, imágenes) basado en lo que aprendió.

*Vs Predictiva:* Predice números. Generativa produce contenido creativo.

---

**Input / Output**
- **Input:** Lo que tú das (el prompt)
- **Output:** Lo que la IA devuelve (la respuesta)

---

### K

**Karpathy, Andrej**
Investigador clave en IA. Su método revoluciona prompting profundo explicando cómo realmente funcionan los modelos de lenguaje.

---

### M

**Modelo de Lenguaje**
Sistema entrenado con miles de millones de palabras que predice la siguiente palabra más probable.

*Simplificado:* Es como un autocomplete avanzadísimo.

---

**Memoria (en Agentes)**
Información que el agente recuerda:
- **Memoria a corto plazo:** La conversación actual
- **Memoria a largo plazo:** Contexto inyectado
- **Memoria de trabajo:** Cálculos internos

---

### O

**Objetivo**
Lo que quieres que la IA logre. Debe ser:
- Específico
- Medible
- Realista

```text
❌ "Ayúdame con Excel"
✅ "Crea una fórmula que calcule la media geométrica de dos valores en las columnas B y C"
```

---

### P

**Prompt**
Instrucción que das a la IA. Puede incluir:
- Instrucción principal
- Contexto
- Ejemplos
- Restricciones

---

**Prompting**
El arte y ciencia de escribir prompts efectivos.

---

### R

**RAG (Retrieval-Augmented Generation)**
Técnica donde el agente busca información relevante ANTES de generar la respuesta.

*Resultado:* Respuestas más precisas basadas en datos reales.

---

### S

**Sistema (System Prompt)**
Instrucciones globales que definen el comportamiento de la IA.

```text
Sistema: Eres abogado administrativo especializado en normativa municipal.
         Siempre citas artículos cuando es posible.
         
Usuario: ¿Puedo hacer X?
```

---

### T

**Temperatura**
Parámetro que controla la "creatividad" de la respuesta:
- **Baja (0.1):** Respuestas consistentes, predecibles, factuales
- **Alta (0.9):** Respuestas creativas, variadas, aventuradas

*Uso:* Temperatura baja para análisis legal. Alta para brainstorming.

---

**Token**
La unidad básica de texto que procesa un modelo.

```text
Aproximación:
- 1 token ≈ 4 caracteres
- 1 token ≈ 0.75 palabras
- 1 página A4 ≈ 400 tokens
```

---

### V

**Ventana de Contexto**
Ver **Contexto de Ventana**

---

### Z

**Zero-Shot Learning**
Técnica donde la IA resuelve algo sin ningún ejemplo previo.

```text
"Traduce esto al latín" → Zero-shot (sin ejemplos de traducción)
```

---

## 🔗 Términos Relacionados

### Bloques del Taller

- **Bloque 1:** Prompting, iteración, claridad, contexto
- **Bloque 2:** Gemas, sistema, especialización, memoria
- **Bloque 3:** Agente, herramientas, autonomía, supervisión

---

### Herramientas Mencionadas

- **ChatGPT:** Chatbot de OpenAI
- **Claude:** Modelo de Anthropic
- **Gemini:** Modelo de Google
- **OpenClaw:** Agente personal de código abierto
- **Hermes:** Agente personal de Anthropic

---

## 📝 Notas Importantes

### Diferencias Críticas

| Término | Significa | No Significa |
|---------|-----------|------------|
| **IA** | Inteligencia Artificial | Consciencia o sentimientos |
| **Generativa** | Crea contenido | Es original |
| **Agente** | Autónomo limitado | Toma decisiones sin validar |
| **Alucinación** | Error predecible | Que está "soñando" |
| **Modelo** | Sistema estadístico | Que entiende como humano |

---

### La Regla de Oro del Glosario

**Si no entiendes un término, NO avances.**

Vuelve aquí, búscalo, entiéndelo. Estos términos aparecerán constantemente.

---

## 🎯 Próximo Paso

¿Necesitas entender otro término? Regresa aquí.

¿Listo para continuar? Vuelve a tu documento anterior.

---

## ✨ Última Nota

Este glosario crece con el taller. Nuevos términos aparecerán en cada bloque.

**Familiarízate con estos conceptos. Son tu lenguaje común con la IA.** 🚀
