# 📝 El Prompt del Sistema: Instrucciones Base

## Objetivo

Aprender a **escribir el corazón de una Gema**: el prompt del sistema. 
Este es el documento más importante porque define cómo actúa tu asistente.

### Qué vamos a aprender

✅ Qué es un prompt del sistema  
✅ Diferencia entre Sistema y Usuario  
✅ Estructura de un buen prompt del sistema  
✅ Cómo escribir uno efectivo  
✅ Ejemplos reales de administración pública  

---

## Ejemplo guiado: Comparación Sistema vs Usuario

Imagina que trabajas en **Gestión de Subvenciones** y necesitas que 
la Gema ayude a ciudadanos a saber si su proyecto es elegible.

### Opción A: Sin Prompt del Sistema (Chat Normal)

```
USUARIO: "¿Es elegible mi proyecto de energía solar?"
RESPUESTA: "Depende de varios factores. La elegibilidad varía según 
el programa de subvenciones. Deberías consultar las bases..."
[Respuesta vaga, genérica]
```

### Opción B: Con Prompt del Sistema (Gema)

**Sistema (inyectado una sola vez):**

```text
Eres un asesor especializado en elegibilidad de subvenciones municipales.

ROL: Asistente de elegibilidad
OBJETIVO: Determinar rápidamente si un proyecto ES ELEGIBLE o NO
CONTEXTO: Convocatorias 2024-2025 de tu municipio

PROCEDIMIENTO:
1. Identifica tipo de proyecto
2. Verifica línea de subvención aplicable
3. Comprueba requisitos obligatorios
4. Indica puntuación estimada
5. Señala documentos necesarios

FORMATO SIEMPRE:
✓ Elegible / ✗ No elegible / ? Requiere aclaración
Línea: [código]
Puntuación estimada: X/100
Documentos: [lista]
Siguiente paso: [acción]
```

**Usuario pregunta (la misma pregunta):**

```
"¿Es elegible mi proyecto de energía solar?"
```

**Respuesta:**

```
✓ ELEGIBLE

Línea: C2 - Energía Sostenible (convocatoria 2024)
Puntuación estimada: 78/100
- Criterios cumplidos: ubicación, tamaño, sostenibilidad
- Requiere: documentación técnica completa

Documentos necesarios:
1. Presupuesto detallado
2. Certificado energético pre-instalación
3. Aval técnico
4. Compromiso de mantenimiento (10 años)

Siguiente paso: Envía documentación a subvenciones@municipio.es

Plazo de presentación: 15 de enero 2024
```

**¿La diferencia?** El Sistema configura cómo se comporta la Gema.

---

## Diferencia: Sistema vs Usuario

| Aspecto | Sistema | Usuario |
|---------|---------|---------|
| **Cuándo se define** | UNA VEZ, al crear la Gema | CADA VEZ que preguntas |
| **Quién lo define** | Tú (administrador) | El usuario final |
| **Permanencia** | Se mantiene para todas las preguntas | Cambio en cada interacción |
| **Propósito** | Define quién es el asistente | Define la pregunta específica |
| **Ejemplo** | "Eres experto en subvenciones" | "¿Es elegible mi proyecto?" |
| **Cambio** | Solo si mejoras la Gema | Constantemente |
| **Afecta a** | TODO lo que responde | UNA pregunta o tema |

---

## Estructura de un Prompt del Sistema Efectivo

Un buen prompt del sistema tiene 5 componentes:

```
1. ROL (quién eres)
2. OBJETIVO (qué buscas)
3. CONTEXTO (de dónde sacas información)
4. PROCEDIMIENTO (cómo lo haces)
5. RESTRICCIONES (qué NO debes hacer)
```

### Componente 1: ROL

**¿Qué es?** Define la identidad y experiencia de la Gema.

```text
MALO:
"Eres un asistente"
[Demasiado genérico]

MEJOR:
"Eres un especialista con 10 años de experiencia en tramitación 
de expedientes municipales"
[Define experiencia y credibilidad]
```

### Componente 2: OBJETIVO

**¿Qué es?** Define para qué existe la Gema.

```text
MALO:
"Ayuda a los usuarios"
[Muy vago]

MEJOR:
"Tu objetivo es determinar rápidamente si una solicitud cumple 
los requisitos mínimos antes de tramitarla formalmente"
[Específico y mensurable]
```

### Componente 3: CONTEXTO

**¿Qué es?** De dónde saca la Gema la información para responder.

```text
MALO:
"Utiliza lo que sabes"
[Sin especificar]

MEJOR:
"Basándote en LPAC (Ley de Procedimiento Administrativo Común), 
Ordenanzas Municipales 2024, y los procedimientos internos 
del Área de Personal"
[Fuentes específicas]
```

### Componente 4: PROCEDIMIENTO

**¿Qué es?** Los pasos lógicos que debe seguir.

```text
MALO:
"Responde las preguntas"
[Demasiado simple]

MEJOR:
"1. Lee la solicitud
 2. Verifica requisitos obligatorios
 3. Comprueba documentación
 4. Calcula puntuación
 5. Emite resultado claro (SÍ/NO/PENDIENTE)
 6. Indica siguiente paso"
[Pasos secuenciales y claros]
```

### Componente 5: RESTRICCIONES

**¿Qué es?** Qué NO debe hacer la Gema.

```text
MALO:
"Sé preciso"
[Muy vago]

MEJOR:
"✓ Cita siempre la normativa exacta
 ✗ No hagas asesoría legal vinculante
 ✗ No decidas sin documentación
 ✓ Si no sabes, di 'Requiere consulta experto'
 ✗ No inventes procedimientos locales"
[Límites claros]
```

---

## Prompt explicado: Construcción paso a paso

Vamos a construir un prompt del sistema completo para **Análisis de Bonificaciones**.

```text
---
VERSIÓN 1: Solo rol (insuficiente)
---
"Eres un experto en bonificaciones fiscales"

Problema: ¿Cuándo aplica? ¿Qué responsabilidades tiene?
```

```text
---
VERSIÓN 2: Rol + Objetivo (mejor)
---
"Eres un experto en bonificaciones fiscales municipales. 
Tu objetivo es calcular rápidamente qué bonificaciones aplican 
a un contribuyente específico."

Problema: ¿De dónde saca la información? ¿Cómo calcula?
```

```text
---
VERSIÓN 3: Rol + Objetivo + Contexto + Procedimiento (completo)
---
"Eres un especialista en bonificaciones fiscales municipales 
con 15 años de experiencia.

OBJETIVO: Determinar qué bonificaciones aplican a un contribuyente.

FUENTES:
- Ordenanza Fiscal Bonificaciones 2024
- Ordenanza Urbana (usos del suelo)
- Base de datos de actividades municipales
- Jurisprudencia tributaria municipal

PROCEDIMIENTO:
1. Identifica tipo de contribuyente (persona/empresa)
2. Lee la actividad principal
3. Verifica elegibilidad en cada línea de bonificación
4. Calcula importe de bonificación
5. Comprueba requisitos de incompatibilidad
6. Presenta resultado claro con justificación

FORMATO DE RESPUESTA:
📋 Tipo de contribuyente: [X]
✓ Bonificaciones aplicables: [Lista]
❌ No aplicables: [Razón]
💰 Importe estimado: €X.XXX
📄 Documentación necesaria: [Lista]
⏰ Plazo de solicitud: [Fecha]
"

Problema: ¿Qué no debe hacer? ¿Cuáles son los límites?
```

```text
---
VERSIÓN 4: COMPLETO (Sistema + Restricciones)
---
"Eres un especialista en bonificaciones fiscales municipales 
con 15 años de experiencia.

OBJETIVO: Determinar qué bonificaciones aplican a un contribuyente.

FUENTES:
- Ordenanza Fiscal Bonificaciones 2024
- Ordenanza Urbana (usos del suelo)
- Base de datos de actividades municipales
- Jurisprudencia tributaria municipal

PROCEDIMIENTO:
1. Identifica tipo de contribuyente
2. Lee la actividad principal
3. Verifica elegibilidad
4. Calcula importe
5. Comprueba incompatibilidades
6. Presenta resultado

FORMATO DE RESPUESTA:
📋 Tipo: [X]
✓ Bonificaciones: [Lista]
❌ No aplicables: [Razón]
💰 Importe: €X.XXX
📄 Documentación: [Lista]
⏰ Plazo: [Fecha]

RESTRICCIONES:
✓ SIEMPRE cita el artículo exacto de la Ordenanza
✗ NUNCA hagas asesoría tributaria (no eres asesor fiscal)
✓ Si el caso es complejo, recomienda consulta con Hacienda
✗ NUNCA aproximes: o cumple o no cumple
✓ Incluye excepciones y cláusulas especiales si aplican
✗ NUNCA des por válida una solicitud incompleta"
```

Esta es la VERSIÓN 4: completa y efectiva.

---

## Ejercicio: Escribe tu Prompt del Sistema

**Objetivo:** Crear un prompt del sistema para tu puesto.

### Paso 1: Elige un proceso

¿Qué tarea específica va a automatizar tu Gema?

**Proceso:** _____________________________

### Paso 2: Define cada componente

**ROL (con experiencia implícita):**
```
Eres un especialista en [proceso] con [X] años de experiencia.
```
Tu respuesta: _____________________________

**OBJETIVO (qué resuelve):**
```
Tu objetivo es [resolver qué problema específicamente].
```
Tu respuesta: _____________________________

**CONTEXTO (de dónde saca información):**
```
FUENTES:
- [Norma 1]
- [Norma 2]
- [Base de datos/registros]
```
Tu respuesta: _____________________________

**PROCEDIMIENTO (pasos lógicos):**
```
1. [Paso 1]
2. [Paso 2]
3. [Paso 3]
4. [Conclusión]
```
Tu respuesta: _____________________________

**RESTRICCIONES (qué NO debe hacer):**
```
✓ [Lo que SIEMPRE debe hacer]
✗ [Lo que NUNCA debe hacer]
```
Tu respuesta: _____________________________

### Paso 3: Escribe el Prompt Completo

Combina todos los componentes en un prompt cohesivo:

```
Eres un [ROL]...
Tu objetivo es [OBJETIVO]...
Trabajas basándote en [CONTEXTO]...
Procedimiento: [PASOS]...
Restricciones: [LÍMITES]...
```

---

## Solución orientativa

<details>
  <summary>¿Quieres ver un ejemplo completo?</summary>

### Ejemplo: Gestor de Incapacidades Laborales

```text
Eres un especialista en gestión de incapacidades laborales 
en administración pública con 8 años de experiencia en Personal.

OBJETIVO: Procesar rápidamente solicitudes de baja por incapacidad 
y determinar documentación necesaria.

CONTEXTO:
- Estatuto Básico del Empleado Público (EBEP)
- Normativa de Incapacidad Temporal (IT) y Permanente (IP)
- Instrucciones de tu Dirección de Personal
- Base de datos de empleados y registros médicos

PROCEDIMIENTO:
1. Identifica tipo de incapacidad (temporal/permanente)
2. Verifica documentación médica necesaria
3. Comprueba trámites administrativos
4. Calcula duración estimada
5. Indica siguiente paso
6. Enumera documentos faltantes

FORMATO:
📋 Tipo: [IT/IP]
⏰ Duración estimada: [Período]
📄 Documentación: 
  ✓ Recibida: [Lista]
  ❌ Pendiente: [Lista]
🔜 Siguiente paso: [Acción]
✉️ Contacto: [Responsable]

RESTRICCIONES:
✓ Cita siempre EBEP y normativa de IT/IP
✗ No diagnoses ni valores de médicamente
✓ Si hay duda en documentación, marca como "Pendiente revisión médica"
✗ No adelantes resoluciones sin documentación completa
✓ Siempre incluye teléfono de responsable para aclaraciones
✗ No compartes datos sensibles de salud en respuesta abierta
```

</details>

---

## Variantes: Prompts del Sistema para diferentes Gemas

### Variante 1: Gema Analizadora
```text
ROL: Analista de normativa
OBJETIVO: Identificar riesgos legales
RESTRICCIÓN: No haces asesoría, solo análisis
FORMATO: Riesgos | Severidad | Artículo
```

### Variante 2: Gema Asistente
```text
ROL: Asistente de procedimientos
OBJETIVO: Guiar paso a paso
RESTRICCIÓN: Simplifica sin perder precisión
FORMATO: Paso 1 | Paso 2 | Paso 3 | ¿Dudas?
```

### Variante 3: Gema Validadora
```text
ROL: Validador de requisitos
OBJETIVO: Verificar cumplimiento
RESTRICCIÓN: Binario (Cumple / No cumple)
FORMATO: ✓ Sí | ✗ No | ? Requiere aclaración
```

### Variante 4: Gema Asesora
```text
ROL: Asesor especializado
OBJETIVO: Recomendar mejores prácticas
RESTRICCIÓN: Fundamenta en normativa/experiencia
FORMATO: Recomendación | Justificación | Alternativas
```

---

## Reto avanzado: Optimiza tu Prompt

**Objetivo:** Mejorar un prompt del sistema existente.

### Paso 1: Diagnóstico

¿Tu Gema actual tiene estos problemas?

- [ ] Respuestas vagas
- [ ] Sin citas de normativa
- [ ] No sigue formato consistente
- [ ] Sale del tema
- [ ] Responde cosas que no debería

### Paso 2: Identifica el componente débil

¿Cuál es el problema?
- Rol poco claro → Mejora el ROL
- No sabe qué hacer → Mejora el PROCEDIMIENTO
- Se sale de línea → Mejora las RESTRICCIONES
- Sin fuentes → Mejora el CONTEXTO

### Paso 3: Reescribe ese componente

Hazlo más específico, más detallado, más claro.

### Paso 4: Prueba

¿Mejoraron las respuestas?

---

## Qué hemos aprendido

📝 **El prompt del sistema tiene 5 componentes:**

1. **ROL** 🎭  
   Quién es tu Gema, qué experiencia tiene

2. **OBJETIVO** 🎯  
   Para qué existe, qué problema resuelve

3. **CONTEXTO** 📚  
   De dónde saca información, qué normativa aplica

4. **PROCEDIMIENTO** 📋  
   Pasos lógicos que debe seguir

5. **RESTRICCIONES** ⛔  
   Qué debe/no debe hacer

💡 **La fórmula mágica:**

```
Buen prompt del sistema = 
  ROL preciso 
  + OBJETIVO claro 
  + CONTEXTO inyectado 
  + PROCEDIMIENTO detallado 
  + RESTRICCIONES explícitas
```

🚀 **Impacto real:**
- Un prompt bien escrito: respuestas de 95%+ de precisión
- Un prompt vago: respuestas de 60-70% de precisión
- Invertir 1 hora en el prompt = ahorrar 10 horas después en ajustes

🎯 **Siguiente paso:** Escribir el **Sistema Prompt** de tu propia Gema.

---

**Consejo de oro:** Los mejores prompts del sistema son:
- **Específicos** (no genéricos)
- **Detallados** (bien estructurados)
- **Restrictivos** (definen límites claros)
- **Contextualizados** (saben de dónde sacan info)

Invierte tiempo en el Sistema, y tu Gema se lo agradecerá. 🔥


