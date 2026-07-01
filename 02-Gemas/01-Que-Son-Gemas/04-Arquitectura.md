# 🏗️ Arquitectura: Cómo se estructura una Gema

## Objetivo

Entender **cómo está construida una Gema internamente**. Descubrirás que no es 
magia, sino componentes bien organizados que trabajan juntos.

### Qué vamos a aprender

✅ Componentes principales de una Gema  
✅ Diferencia entre Sistema y Usuario  
✅ Cómo funciona cada parte  
✅ Ejemplo completo de arquitectura  
✅ Cómo se construye de cero  

---

## Ejemplo guiado: Desmantelando una Gema

Vamos a analizar una Gema de **Análisis de Contratos** públicos 
y ver qué tiene en su interior.

### La Gema por dentro

Una Gema tiene 3 capas principales:

```
┌─────────────────────────────────────────┐
│ CAPA 1: SISTEMA (Instrucciones Base)    │
│ "Quién eres" - Rol y comportamiento     │
└─────────────────────────────────────────┘
                    ↓
┌─────────────────────────────────────────┐
│ CAPA 2: CONTEXTO (Base de Conocimiento) │
│ "Qué sabes" - Normativas, ejemplos      │
└─────────────────────────────────────────┘
                    ↓
┌─────────────────────────────────────────┐
│ CAPA 3: USUARIO (Interacción)           │
│ "Qué necesito" - La pregunta del usuario │
└─────────────────────────────────────────┘
                    ↓
             RESPUESTA ESPECIALIZADA
```

---

## Componentes principales

### 1️⃣ CAPA SISTEMA: Las Instrucciones Base

**¿Qué es?**  
El "ADN" de la Gema. Defines quién es, qué puede hacer, cómo se comporta.

**Ejemplo (Gema de Contratos):**

```text
ROL:
Eres un experto en análisis de contratos del sector público español.

COMPETENCIAS:
- Analizar cláusulas de contratos públicos
- Identificar riesgos legales
- Verificar cumplimiento de LCSP
- Extraer información clave

RESTRICCIONES:
- No eres abogado, eres analista
- No haces asesoría legal vinculante
- Si hay duda, recomienda consulta legal

FORMATO DE RESPUESTA:
- Resumen ejecutivo (3 líneas)
- Hallazgos clave (máximo 5)
- Riesgos identificados
- Recomendaciones
```

**¿Por qué importa?**  
Define el comportamiento. Sin esto, la Gema sería como ChatGPT normal.

---

### 2️⃣ CAPA CONTEXTO: La Base de Conocimiento

**¿Qué es?**  
Ejemplos, normativas, procedimientos específicos que la Gema debe "recordar".

**Ejemplo (Contexto de Contratos):**

```text
NORMATIVAS CLAVE:
- LCSP (Ley de Contratos del Sector Público): Arts. 1-340
- Real Decreto 203/2022: procedimientos de contratación
- Instrucciones de la JUNTA [municipio]: 2024

TIPOS DE CONTRATOS:
- Suministro: < 50k (contratación simplificada), > 50k (abierto)
- Servicios: < 80k (simplificada), > 80k (abierto)
- Obras: < 100k (simplificada), > 100k (abierto)

EJEMPLOS DE CLÁUSULAS PROBLEMÁTICAS:
1. "Sin período de garantía" → Riesgo: Incumplimiento LCSP
2. "Adjudicación a criterio único" → Riesgo: Reclamaciones
3. "Penalización por retraso: 0%" → Riesgo: No hay incentivo

CRITERIOS DE ADJUDICACIÓN RECOMENDADOS:
- Precio: 30-40%
- Experiencia: 20-30%
- Calidad: 20-30%
- Sostenibilidad: 10-20%
```

**¿Por qué importa?**  
Es lo que diferencia una Gema genérica de una especializada. Sin contexto, 
es solo ChatGPT.

---

### 3️⃣ CAPA USUARIO: La Pregunta

**¿Qué es?**  
Lo que pregunta el usuario. La Gema combina Sistema + Contexto + Pregunta 
del usuario para responder.

**Ejemplo:**

```text
USUARIO: "Analiza este contrato de suministro por 75.000€. 
¿Cumple LCSP?"

[Aquí viene el contrato]
```

**¿Por qué importa?**  
Es el disparador. La Gema recibe esto y activa todo su conocimiento para 
responder específicamente a TU pregunta.

---

## Prompt explicado: Sistema vs Usuario

```text
=== SISTEMA (inyectado una sola vez) ===
"Eres experto en contratos municipales. 
Siempre citas LCSP. Identificas riesgos legales. 
Formato: Resumen | Hallazgos | Riesgos | Recomendaciones"

=== CONTEXTO (información cargada) ===
"Normativa LCSP completa, tipos de contratos, cuantías, 
procedimientos, ejemplos de cláusulas problemáticas"

=== USUARIO (cada interacción) ===
"¿Cumple este contrato la LCSP?"
[Texto del contrato]

=== RESULTADO ===
Respuesta especializada que combina:
- Las instrucciones del Sistema
- El conocimiento del Contexto
- La pregunta específica del Usuario
```

---

## Arquitectura completa: Paso a paso

### Paso 1: Rol y Comportamiento (Sistema)

```text
✓ Quién eres
✓ Cuáles son tus competencias
✓ Cómo debes comportarte
✓ Cuáles son tus limitaciones
✓ Qué debes hacer si no sabes algo
```

### Paso 2: Información y Ejemplos (Contexto)

```text
✓ Normativas aplicables
✓ Procedimientos de tu organización
✓ Ejemplos reales (casos buenos y malos)
✓ Terminología específica
✓ Contactos o referencias
```

### Paso 3: Instrucciones de Formato (Sistema)

```text
✓ Cómo estructurar las respuestas
✓ Qué información incluir siempre
✓ Cuándo alertar de riesgos
✓ Cómo citar fuentes
```

---

## Ejercicio: Analiza una Gema Real

**Objetivo:** Identificar Sistema, Contexto y Usuario en una Gema existente.

Te proporciono una Gema de Expedientes. Separa los componentes:

### La Gema Completa

```text
Eres un asistente especializado en gestión de expedientes administrativos 
en ayuntamientos españoles.

PROCEDIMIENTOS:
- Expedientes simples: 10 días
- Expedientes complejos: 30 días (extensible a 10 más)
- Expedientes especiales: según normativa específica

TIPOS DE DOCUMENTOS OBLIGATORIOS:
1. Acta de inicio
2. Documentación de prueba
3. Informes técnicos (si procede)
4. Resolución

NORMATIVA:
- LPAC arts. 20-30 (plazos)
- LOFAGE (competencias)
- Ordenanzas municipales [tu municipio]

CUANDO RESPONDAS:
- Identifica tipo de expediente
- Cita plazo máximo
- Lista documentos necesarios
- Incluye excepciones
- Cita artículos exactos

USUARIO PREGUNTA:
"Tengo un expediente de solicitud de ayuda social. ¿Cuáles son los pasos 
y plazos?"
```

### Tu tarea:

1. **Extrae el SISTEMA:**  
   _________________________________

2. **Extrae el CONTEXTO:**  
   _________________________________

3. **Extrae la PREGUNTA DEL USUARIO:**  
   _________________________________

4. **Predice la RESPUESTA:**  
   _________________________________

---

## Solución orientativa

<details>
  <summary>¿Quieres ver la solución?</summary>

### SISTEMA (Instrucciones Base)
```
Eres un asistente especializado en gestión de expedientes administrativos 
en ayuntamientos españoles.

CUANDO RESPONDAS:
- Identifica tipo de expediente
- Cita plazo máximo
- Lista documentos necesarios
- Incluye excepciones
- Cita artículos exactos
```

### CONTEXTO (Base de Conocimiento)
```
PROCEDIMIENTOS:
- Expedientes simples: 10 días
- Expedientes complejos: 30 días (extensible a 10 más)

TIPOS DE DOCUMENTOS OBLIGATORIOS:
1. Acta de inicio
2. Documentación de prueba
3. Informes técnicos
4. Resolución

NORMATIVA:
- LPAC arts. 20-30 (plazos)
- LOFAGE (competencias)
- Ordenanzas municipales [tu municipio]
```

### USUARIO (Pregunta)
```
"Tengo un expediente de solicitud de ayuda social. 
¿Cuáles son los pasos y plazos?"
```

### RESPUESTA ESPERADA
```
Expediente: SIMPLE (ayuda social)
Plazo: 10 días hábiles (LPAC art. 21)

PASOS OBLIGATORIOS:
1. Acta de inicio (< 3 días desde solicitud)
2. Solicitud documentación (5 días disponibles)
3. Informe técnico (si es necesario)
4. Resolución (máximo 7 días tras cierre)

DOCUMENTOS NECESARIOS:
- DNI solicitante
- Datos económicos
- Justificación de necesidad
- Empadronamiento [tu municipio]

EXCEPCIONES:
Si falta documentación, se suspende plazo hasta 10 días más
```

</details>

---

## Variantes: Arquitecturas diferentes

### Arquitectura 1: Gema Analista
```
Sistema: "Analiza y reporta"
Contexto: Normas, criterios de análisis
Usuario: "¿Es legal esto?"
Resultado: Análisis con riesgos
```

### Arquitectura 2: Gema Asistente
```
Sistema: "Ayuda y guía paso a paso"
Contexto: Procedimientos, checklists
Usuario: "¿Cómo hago X?"
Resultado: Pasos detallados
```

### Arquitectura 3: Gema Asesor
```
Sistema: "Recomienda decisiones"
Contexto: Casos precedentes, mejores prácticas
Usuario: "¿Qué opción es mejor?"
Resultado: Recomendación con justificación
```

---

## Reto avanzado: Diseña la Arquitectura

**Objetivo:** Diseña la arquitectura completa de una Gema para tu puesto.

### Paso 1: Elige un proceso
(Ejemplo: Gestión de quejas, Análisis de solicitudes)

**Proceso elegido:** _____________________________

### Paso 2: Define el SISTEMA

Completa:
```
Eres un asistente especializado en [tu proceso].

COMPETENCIAS:
- [Competencia 1]
- [Competencia 2]
- [Competencia 3]

RESTRICCIONES:
- [Limitación 1]
- [Limitación 2]

FORMATO DE RESPUESTA:
- [Estructura 1]
- [Estructura 2]
- [Estructura 3]
```

### Paso 3: Define el CONTEXTO

Necesitarás:
- Normativas clave: ________________
- Procedimientos: ________________
- Ejemplos: ________________
- Excepciones: ________________

### Paso 4: Escribe una PREGUNTA DE PRUEBA

¿Qué preguntaría un usuario?

________________

### Paso 5: Predice la RESPUESTA

¿Qué debería contestar tu Gema?

________________

---

## Qué hemos aprendido

🏗️ **Una Gema tiene 3 capas arquitectónicas:**

1. **Sistema** 📋  
   Las instrucciones base que definen quién es y cómo actúa

2. **Contexto** 📚  
   La base de conocimiento que la hace especializada

3. **Usuario** 💬  
   La pregunta específica que la activa

💡 **La fórmula:**

```
Gema = Sistema (quién eres) 
      + Contexto (qué sabes)
      + Pregunta de Usuario (qué necesito)
      = Respuesta especializada
```

🎯 **Por qué importa:**
- Entender la arquitectura te permite CREAR tus propias Gemas
- Sabes qué falta si una Gema funciona mal
- Puedes optimizar cada componente

🚀 **Siguiente paso:** Aprenderás a **crear el Sistema** 
(el corazón de cualquier Gema).

---

**Consejo:** Las mejores Gemas tienen Sistema claro + Contexto rico + 
Usuario específico. Si faltan componentes, la respuesta será vaga. 🔍

