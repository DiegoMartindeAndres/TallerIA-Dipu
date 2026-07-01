# Chain of Thought: Pensamiento en Cadena para Razonamientos Complejos

## Objetivo

Dominar la técnica de "Pensamiento en Cadena" para que la IA explique su razonamiento paso a paso, mejorando significativamente la calidad y confiabilidad de respuestas en tareas complejas.

### Qué vamos a aprender

- Qué es Chain of Thought (CoT) y por qué funciona
- Cómo estructurar prompts para forzar razonamiento explícito
- Diferencia de calidad: con y sin CoT
- Aplicaciones prácticas en administración pública
- Cómo combinar CoT con roles y formatos

---

## Qué es Chain of Thought

**Chain of Thought** es una técnica que pide a la IA que **explique su proceso de pensamiento paso a paso** antes de dar la respuesta final.

### Por qué funciona
- **Reduce errores:** Al razonar explícitamente, detecta inconsistencias
- **Mejora calidad:** Fuerza análisis más profundo
- **Genera confianza:** Ves cómo llegó a la conclusión
- **Permite verificación:** Puedes revisar cada paso
- **Es especialmente efectivo en:** Decisiones complejas, análisis legales, evaluaciones de riesgos

---

## Ejemplo Simple: Sin vs Con Chain of Thought

### Pregunta base
"¿Podemos denegar una solicitud de acceso a información porque 'nos parece prudente'?"

### Respuesta SIN Chain of Thought
```text
No, no es motivo válido.
```

**Problema:** Muy corta, sin justificación, el usuario no entiende por qué.

### Respuesta CON Chain of Thought
```text
Empecemos por el razonamiento:

1. NORMATIVA APLICABLE
   - La Ley de Transparencia 19/2013 establece derecho de acceso a información pública
   - Permite denegación solo por motivos tasados (excepciones legales)
   - La discrección no es causa de denegación en legislación española

2. ANÁLISIS DEL TÉRMINO "PRUDENCIA"
   - "Prudencia" es criterio subjetivo y discrecional
   - No coincide con ninguna excepción legal (seguridad, datos personales, etc.)

3. CONCLUSIÓN
   No. La "prudencia" no es motivo legal válido para denegar acceso a información.

4. RIESGO LEGAL
   - Denegar sin causa tasada expone a recurso administrativo
   - Tribunal anularía decisión como arbitraria

RESPUESTA: Requiere motivo legal específico de la LTAI.
```

**Ventaja:** Ves la lógica completa, puedes verificarla, es defensible.

---

## Ejemplo Complejo: Análisis de Contrato con CoT

### Situación
Recibiste contrato de suministro que "parece correcto" pero necesitas estar seguro antes de contratación.

### Prompt SIN Chain of Thought
```text
¿Es seguro firmar este contrato de suministro?
[contrato]
```

**Problema:** Análisis superficial, riesgos no identificados.

### Prompt CON Chain of Thought
```text
Actúa como Abogado Administrativo especializado en contratación pública.

Necesito analizar este contrato de suministro antes de firmar.
Por favor, razona paso a paso:

1. VERIFICACIÓN LEGAL: ¿Cumple con requisitos de LCSP?
2. ANÁLISIS DE CLÁUSULAS: ¿Qué cláusulas son problemáticas?
3. EVALUACIÓN DE RIESGOS: ¿Qué riesgos potenciales hay?
4. COMPARACIÓN: ¿Es estándar o tiene desviaciones?
5. RECOMENDACIÓN: ¿Qué cambios son críticos antes de firmar?

Explica tu razonamiento en cada paso.

[contrato]
```

**Resultado:** Análisis profundo, estructurado, identificas riesgos reales.

---

## Prompt Explicado: Estructura de Chain of Thought

```text
[CONTEXTO/ROL]

Necesito que analices [PROBLEMA] paso a paso:

PASO 1: [PRIMER ASPECTO]
- ¿Qué se debe verificar?
- ¿Cuál es el análisis?

PASO 2: [SEGUNDO ASPECTO]
- ¿Qué se debe verificar?
- ¿Cuál es el análisis?

PASO 3: [TERCER ASPECTO]
- ¿Qué se debe verificar?
- ¿Cuál es el análisis?

CONCLUSIÓN:
- Síntesis de pasos anteriores
- Recomendación clara

[CONTENIDO A ANALIZAR]
```

**Componentes clave:**
- **Contexto claro:** Rol, situación, objetivo
- **Pasos explícitos:** Estructura el análisis en fases
- **Preguntas guía:** Indican qué se espera en cada paso
- **Conclusión solicitada:** Cierra el análisis con recomendación

---

## Variantes de Chain of Thought

### Variante 1: CoT Estructurado (Paso a paso)
```text
Resuelve este problema en 5 pasos exactos:

Paso 1: Identifica los hechos clave
Paso 2: Determina la normativa aplicable
Paso 3: Analiza conformidad con cada requisito
Paso 4: Identifica desviaciones o riesgos
Paso 5: Proporciona recomendación

[Contenido]
```

### Variante 2: CoT con Verificación
```text
Antes de responder, razona:
1. ¿Qué información es relevante?
2. ¿Qué información falta?
3. ¿Hay contradicciones?
4. ¿Qué supuestos estoy haciendo?
5. Ahora, responde.
```

### Variante 3: CoT Argumentativo
```text
Defiende tu posición. Para cada recomendación:
- ARGUMENTO: ¿Por qué lo digo?
- EVIDENCIA: ¿Dónde está basado?
- OBJECIÓN: ¿Qué contraargumento podría haber?
- RESPUESTA: ¿Cómo rebaten esa objeción?
```

### Variante 4: CoT Comparativo
```text
Compara dos opciones paso a paso:
1. Opción A: Ventajas
2. Opción A: Desventajas
3. Opción B: Ventajas
4. Opción B: Desventajas
5. Análisis de riesgos de cada una
6. Recomendación justificada
```

---

## Comparación Real: Misma Pregunta, Con y Sin CoT

### Caso: Evaluación de solicitud de exención de tasa

**Pregunta:**
"Solicitan exención de tasa para tramitar un permiso. ¿Debo concederla?"

### Respuesta SIN CoT
```
No, normalmente se requiere tasa según la normativa local.
```

---

### Respuesta CON CoT
```
Razonemos paso a paso:

PASO 1: NORMATIVA APLICABLE
- Ordenanza fiscal local: establece tasa obligatoria para tramitación
- Excepciones legales: menores de edad, discapacidad, vulnerabilidad
- Decreto estatal: situaciones de emergencia

PASO 2: ANÁLISIS DEL SOLICITANTE
- ¿Se ajusta a alguna excepción legal?
- ¿Hay documento que lo acredite?
- ¿Es justificable administrativamente?

PASO 3: EVALUACIÓN DE RIESGOS LEGALES
- Conceder sin motivo: puede recurrirse como arbitrario
- Negar sin analizar: podría ser discriminatorio

PASO 4: DECISIÓN
- Si cumple excepciones legales: SÍ conceder
- Si no cumple: NO, pero ofrecer facilidades de pago

RESPUESTA: Verifica si solicitante cumple con alguna excepción legal tasada.
Si no, la tasa es obligatoria, pero ofrece fraccionamiento si es necesario.
```

---

## Ejercicio

**Situación:**
Tu gerencia ha reducido el presupuesto en un 15% para el próximo año. Debe reasignarse presupuesto entre 5 áreas: Personal (40%), Inversión (25%), Funcionamiento (20%), Subvenciones (10%), Formación (5%).

Necesitas recomendar dónde reducir.

**Tu tarea:**
Diseña un prompt con **Chain of Thought** que analice esta decisión presupuestaria paso a paso.

**Estructura esperada:**
1. Analiza impacto de reducción en cada área
2. Evalúa riesgos legales/operacionales
3. Considera dependencias entre áreas
4. Proporciona recomendación

**Tiempo:** 25 minutos

**Pista:** No pidas simplemente "¿dónde reducir?" sino fuerza un razonamiento estructurado que te permita entender la lógica.

---

## Solución Orientativa

<details>
  <summary>¿Quieres ver cómo estructurar el prompt con CoT?</summary>

### Prompt con Chain of Thought
```text
Actúa como Responsable de Gestión Presupuestaria de administración pública.

Situación: Reducción presupuestaria del 15%. Distribución actual:
- Personal (40%): 600.000€ → afectado: -90.000€
- Inversión (25%): 375.000€ → afectado: -56.250€
- Funcionamiento (20%): 300.000€ → afectado: -45.000€
- Subvenciones (10%): 150.000€ → afectado: -22.500€
- Formación (5%): 75.000€ → afectado: -11.250€

Analiza paso a paso:

PASO 1: RIGIDEZ DE CADA PARTIDA
- ¿Qué partidas son legalmente inamovibles?
- ¿Qué margen de flexibilidad tiene cada una?
- ¿Hay restricciones contractuales?

PASO 2: ANÁLISIS DE IMPACTO OPERACIONAL
- Si reducimos Personal 15%: ¿cuántos puestos se pierden?
- Si reducimos Inversión 15%: ¿qué proyectos se detienen?
- Si reducimos Funcionamiento 15%: ¿se paraliza operación?
- Si reducimos Subvenciones 15%: ¿qué beneficiarios se ven afectados?
- Si reducimos Formación 15%: ¿se cumple con requisitos de capacitación?

PASO 3: EVALUACIÓN DE RIESGOS LEGALES/SOCIALES
- ¿Hay compromisos que no pueden no cumplirse?
- ¿Hay riesgos de demandas o conflictividad?
- ¿Hay impacto reputacional?
- ¿Hay vulneración de derechos?

PASO 4: ANÁLISIS DE INTERDEPENDENCIAS
- ¿Reducir una partida afecta a otras?
- ¿Hay efectos en cascada?
- ¿Qué combinaciones son más resilientes?

PASO 5: ESCENARIOS COMPARATIVOS
- Escenario 1: Reduce solo lo flexible
- Escenario 2: Distribuye proporcionalmente
- Escenario 3: Protege áreas críticas y reduce otras más

PASO 6: RECOMENDACIÓN JUSTIFICADA
- ¿Cuál es la opción menos dañina?
- ¿Qué medidas complementarias se necesitan?
- ¿Cuál es tu propuesta final?

Razona cada paso explícitamente.
```

### Resultado esperado

**Estructura de respuesta:**

```
PASO 1: RIGIDEZ
- Personal: Muy rígida (convenios, obligaciones legales)
- Inversión: Flexible (proyectos aplazables)
- Funcionamiento: Parcialmente rígida (servicios mínimos)
- Subvenciones: Rígida legalmente (compromisos previos)
- Formación: Flexible (puede reducirse)

[La IA continúa analizando cada paso...]

RECOMENDACIÓN FINAL:
Reducir de forma proporcional Inversión (donde más espacio hay)
y Formación (donde hay flexibilidad). Mantener Personal y Subvenciones
por rigidez legal. Negociar Funcionamiento.
```

**Ventaja:** Ves exactamente por qué se recomienda X en lugar de Y.

</details>

---

## Reto Avanzado

**Nivel: Experto**

Diseña un prompt que combine:
1. **Chain of Thought** (razonamiento paso a paso)
2. **Rol Especializado** (Abogado o Auditor)
3. **Formato de Salida** (tabla Markdown con análisis)

Ejemplo esperado: Un único prompt que produzca razonamiento explícito en formato estructurado de tabla.

---

## Qué Hemos Aprendido

✅ **Chain of Thought fuerza calidad:** No es lo mismo pensar que explicar qué se piensa.

✅ **Reduce errores significativamente:** El razonamiento explícito detecta inconsistencias.

✅ **Genera confianza y defensibilidad:** Puedes mostrar tu lógica a superiores o auditores.

✅ **Esencial en decisiones complejas:** Personal, presupuesto, evaluaciones legales.

✅ **Mejora el análisis cíclico:** Si no estás de acuerdo, sabes exactamente dónde rebatir.

✅ **Se combina bien con otras técnicas:** CoT + Roles + Formatos = herramienta potentísima.

**Próximo paso:** Aprende a establecer Restricciones (documento siguiente) para que la IA respete límites de seguridad y datos sensibles.
