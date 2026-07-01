# Roles Especializados: La Magia de Cambiar de Perspectiva

## Objetivo

Aprender a asignar roles específicos a la IA para obtener respuestas especializadas adaptadas a tu necesidad concreta, mejorando calidad y relevancia.

### Qué vamos a aprender

- Qué es un rol y cómo cambia la perspectiva de análisis
- Por qué "Actúa como X" produce resultados completamente diferentes
- Roles profesionales útiles para administración pública
- Cómo combinar roles para contextos más ricos
- Cuándo es más efectivo usar roles especializados

---

## Ejemplo Guiado: Análisis de una Denuncia Administrativa

Imagina que necesitas analizar una denuncia sobre presunta corrupción en adjudicación de contratos. El mismo contenido puede analizarse desde perspectivas completamente distintas:

### Sin rol especificado
"Analiza esta denuncia: El proceso de licitación para obras de infraestructura no fue transparente, falta documentación de justificación de criterios de puntuación."

**Problema:** Respuesta genérica, podría abordar aspectos superfluos.

### Con rol especializado (versión 1)
"Actúa como un Auditor de Organismos Públicos con 15 años de experiencia. Analiza esta denuncia: El proceso de licitación para obras de infraestructura no fue transparente, falta documentación de justificación de criterios de puntuación."

**Resultado:** Enfoque en irregularidades, control interno, documentación probatoria.

### Con rol especializado (versión 2)
"Actúa como Abogada Especialista en Derecho Administrativo. Analiza esta denuncia: El proceso de licitación para obras de infraestructura no fue transparente, falta documentación de justificación de criterios de puntuación."

**Resultado:** Enfoque en disposiciones legales aplicables, vulneración de principios (publicidad, igualdad).

### Con rol especializado (versión 3)
"Actúa como Responsable de Compliance y Gestión de Riesgos. Analiza esta denuncia: El proceso de licitación para obras de infraestructura no fue transparente, falta documentación de justificación de criterios de puntuación."

**Resultado:** Enfoque en riesgos reputacionales, medidas correctivas, prevención futura.

¿Ves la diferencia? **Tres perspectivas, tres análisis valiosos.**

---

## Prompt Explicado

```text
Actúa como [ESPECIALISTA CON EXPERIENCIA]. 
Tienes [CONTEXTO ESPECÍFICO Y BACKGROUND].

Tu objetivo: [QUÉ NECESITAS EXACTAMENTE]

Analiza: [CONTENIDO A ANALIZAR]

Proporciona tu análisis desde tu perspectiva profesional.
```

**Componentes clave:**
- **[ESPECIALISTA CON EXPERIENCIA]:** Abogado, Auditor, Inspector, Gestor de Calidad, etc.
- **[CONTEXTO ESPECÍFICO]:** "15 años en administración", "especialista en RGPD", "experta en fraude"
- **[QUÉ NECESITAS]:** Señala claramente qué tipo de análisis esperas
- **[CONTENIDO]:** El material específico sobre el que trabajar

---

## Roles Útiles para Administración Pública

### 1. **Abogado Administrativo**
Especialista en legislación administrativa, procedimientos, derechos y obligaciones.
```text
Actúa como un Abogado Administrativo especializado en normativa de administración electrónica. 
¿Qué vulneraciones legales pueden identificarse en este proceso?
```

### 2. **Auditor de Organismos Públicos**
Experto en control interno, cumplimiento, irregularidades, documentación.
```text
Actúa como un Auditor de la Administración Pública con 12 años de experiencia.
Desde una perspectiva de control interno, ¿qué debería verificarse en este procedimiento?
```

### 3. **Inspector de Hacienda Pública**
Especialista en cumplimiento fiscal, fraude, gasto público.
```text
Actúa como Inspector de Hacienda Pública especializado en gasto público.
¿Qué indicadores de alerta detectas en esta situación?
```

### 4. **Responsable de Cumplimiento Normativo (Compliance)**
Experto en riesgos, prevención, medidas correctivas.
```text
Actúa como Responsable de Compliance de un organismo público.
¿Cuál sería tu plan de acción correctiva y preventiva?
```

### 5. **Gestor de Recursos Humanos**
Especialista en normas laborales, conflictividad, resolución de problemas.
```text
Actúa como Responsable de Recursos Humanos de administración local.
¿Cómo abordarías esta situación desde perspectiva laboral?
```

### 6. **Responsable de Transparencia y RGPD**
Experto en protección de datos, acceso a información, privacidad.
```text
Actúa como Responsable de Tratamiento de Datos (RGPD) y Transparencia.
¿Qué implicaciones tiene esto en términos de protección de datos?
```

---

## Variantes y Combinaciones

### Rol con experiencia temporal
```text
Actúa como un Inspector de Trabajo con 20 años de experiencia en conflictividad laboral.
```

### Rol con especialización sectorial
```text
Actúa como Abogado Administrativo especializado en contratación pública y fraude.
```

### Combinación de roles (para análisis multidimensional)
```text
Soy una junta de expertos compuesta por:
1. Un Auditor de Organismos Públicos
2. Un Abogado Administrativo
3. Un Responsable de Cumplimiento

Analicemos juntos esta situación desde vuestras tres perspectivas.
```

---

## Ejercicio

**Situación:**
Tu ayuntamiento ha recibido varias solicitudes de información sobre un proceso de selección de personal que parece opaco. Necesitas analizar el caso desde múltiples ángulos.

**Tu tarea:**
1. Pide análisis del mismo contenido con 3 roles diferentes
2. Usa este contenido como base:

"Se convocó una plaza de coordinador de proyectos comunitarios con requisitos: Máster universitario, 5 años experiencia, inglés C1. Se presentaron 8 candidatos. La comisión evaluó por currículum sin entrevistas. Ganador fue el único máster. Terceros cuestionan el proceso."

**Instrucciones específicas:**
- Primer prompt: Abogado Administrativo (enfoque legal)
- Segundo prompt: Auditor Público (enfoque control interno)
- Tercero: Responsable de Cumplimiento (enfoque riesgos)

**Tiempo:** 15 minutos

---

## Solución Orientativa

<details>
  <summary>¿Quieres ver cómo estructurar los prompts?</summary>

### Prompt 1: Perspectiva Legal
```text
Actúa como un Abogado Administrativo especializado en procedimientos selectivos 
y contratación pública en administración local.

Situación: Se convocó una plaza de coordinador de proyectos comunitarios con requisitos: 
Máster universitario, 5 años experiencia, inglés C1. Se presentaron 8 candidatos. 
La comisión evaluó por currículum sin entrevistas. Ganador fue el único máster. 
Terceros cuestionan el proceso.

¿Qué vulneraciones legales potenciales pueden identificarse en este procedimiento selectivo?
¿Qué normativa se incumple? ¿Qué derechos podrían estar en riesgo?
```

**Tipo de respuesta esperada:** Referencias a ley de procedimiento administrativo común, principios de publicidad, igualdad, mérito y capacidad. Análisis de criterios discriminatorios.

### Prompt 2: Perspectiva de Auditoría
```text
Actúa como un Auditor de Organismos Públicos con experiencia en procesos selectivos.

Situación: Se convocó una plaza de coordinador de proyectos comunitarios con requisitos: 
Máster universitario, 5 años experiencia, inglés C1. Se presentaron 8 candidatos. 
La comisión evaluó por currículum sin entrevistas. Ganador fue el único máster. 
Terceros cuestionan el proceso.

Desde una perspectiva de control interno y cumplimiento, ¿qué debería haberse verificado? 
¿Qué documentación falta? ¿Qué irregularidades detectas?
```

**Tipo de respuesta esperada:** Análisis de documentación, protocolos faltantes, trazabilidad de decisiones, separación de funciones.

### Prompt 3: Perspectiva de Compliance
```text
Actúa como Responsable de Cumplimiento y Gestión de Riesgos de un organismo público.

Situación: Se convocó una plaza de coordinador de proyectos comunitarios con requisitos: 
Máster universitario, 5 años experiencia, inglés C1. Se presentaron 8 candidatos. 
La comisión evaluó por currículum sin entrevistas. Ganador fue el único máster. 
Terceros cuestionan el proceso.

¿Cuáles son los principales riesgos? ¿Qué medidas correctivas recomendarías? 
¿Qué hacer para prevenir situaciones similares?
```

**Tipo de respuesta esperada:** Gestión de riesgos reputacionales, medidas preventivas, protocolos de futuro.

**Lo que observarás:** Aunque el contenido es idéntico, las respuestas tendrán ángulos distintos, cada una valiosa para tu análisis completo.

</details>

---

## Reto Avanzado

**Nivel: Experto**

Diseña un prompt que combine 3 roles en una "junta de expertos". La IA debe analizar un caso concreto desde tres perspectivas simultáneamente, con formato que diferencie claramente cada análisis.

Ejemplo de estructura esperada:
```
## Análisis desde perspectiva legal
[Respuesta]

## Análisis desde perspectiva de auditoría
[Respuesta]

## Análisis desde perspectiva de cumplimiento
[Respuesta]

## Síntesis final: Recomendación conjunta
[Respuesta]
```

¿Puedes construir un prompt que logre esto? Pista: Indica claramente que necesitas respuestas estructuradas en secciones.

---

## Qué Hemos Aprendido

✅ **Los roles transforman respuestas:** No es lo mismo preguntar genéricamente que establecer una perspectiva específica.

✅ **La experiencia importa:** Incluir años de experiencia y contexto enriquece las respuestas.

✅ **Combinaciones potentes:** Una junta de expertos da análisis multidimensional y más robusto.

✅ **Ahorro de tiempo:** En lugar de 3 consultas diferentes, puedes obtener 3 perspectivas en 1 prompt bien diseñado.

✅ **Aplicabilidad inmediata:** Abogados, Auditores, Inspectores, Gestores de Cumplimiento... estos roles existen en tu organización; la IA puede "replicar" su perspectiva.

**Próximo paso:** Combina Roles Especializados con Formatos de Salida (documento siguiente) para obtener análisis perspectivado Y estructurado exactamente como lo necesitas.
