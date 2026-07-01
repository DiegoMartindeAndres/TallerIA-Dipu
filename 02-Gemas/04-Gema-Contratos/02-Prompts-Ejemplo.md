# Prompts Efectivos para Análisis de Contratos

## Objetivo
Dominar técnicas para hacer preguntas que generen análisis claros, estructurados y accionables de contratos públicos.

## Qué vamos a aprender
- Estructura de prompts para análisis de contratos
- Cómo solicitar diferentes tipos de análisis
- Técnicas para detectar riesgos ocultos
- Cómo comparar contratos
- Cuándo y cómo escalar a abogado

## Ejemplo guiado

David acaba de recibir un contrato de asesoramiento jurídico externo. Son 25 páginas. Su pregunta inicial es: "¿Está bien?"

**Pregunta vaga:** "¿Es este un buen contrato?"  
**Respuesta:** Demasiado general, información que no puede usar

**Pregunta efectiva:** "¿Cuáles son los 5 riesgos principales? Para cada uno, dime nivel (bajo/medio/alto) y qué hacer."  
**Respuesta:** Lista clara, puede tomar decisiones

## Prompts explicados con ejemplos

### Prompt 1: Resumen Ejecutivo

Cuando necesitas entender rápidamente qué es un contrato.

```text
Analiza este contrato y dame un resumen de 5 minutos:

[PEGA CONTRATO AQUÍ]

Incluye:
1. Qué es (una frase)
2. Quién lo firma (nosotros y ellos)
3. Cuánto cuesta y cuánto tiempo dura
4. Cuál es el servicio/producto
5. Cuándo hay que renovarlo

Solo hechos, sin análisis legal.
```

**Ejemplo real:**
```text
Analiza este contrato y dame un resumen de 5 minutos:

[PEGAMOS CONTRATO DE LIMPIEZA DE 45 PÁGS]

Incluye:
1. Qué es (una frase)
2. Quién lo firma (nosotros y ellos)
3. Cuánto cuesta y cuánto tiempo dura
4. Cuál es el servicio/producto
5. Cuándo hay que renovarlo
```

### Prompt 2: Detección de Riesgos

El prompt más importante: encontrar qué puede salir mal.

```text
Revisa este contrato y detecta riesgos:

[PEGA CONTRATO]

Para cada riesgo:
- Nivel: BAJO / MEDIO / ALTO
- Descripción: qué puede pasar
- Dónde en el contrato: número de cláusula
- Qué hacer: cambiar, preguntar, aceptar, consultar abogado

Sé específico, no general.
```

**Ejemplo real:**
```text
Revisa este contrato de servicios de limpieza y detecta riesgos:

[PEGAMOS CONTRATO]

Para cada riesgo:
- Nivel: BAJO / MEDIO / ALTO
- Descripción: qué puede pasar
- Dónde en el contrato: número de cláusula
- Qué hacer: cambiar, preguntar, aceptar, consultar abogado

Enfoque especial en: precios, cláusula de revisión, penalizaciones, responsabilidad
```

### Prompt 3: Comparación de Contratos

Para ver qué ha cambiado respecto al anterior.

```text
Compara estos dos contratos:

CONTRATO A (antiguo):
[PEGA CONTRATO ANTERIOR]

CONTRATO B (nuevo):
[PEGA CONTRATO NUEVO]

Dime:
1. ¿Cuáles son los cambios principales?
2. ¿Quién se beneficia más en cada cambio (nosotros o ellos)?
3. ¿Hay cambios preocupantes?
4. ¿Qué debería renegociar?

Cita cláusulas específicas.
```

**Ejemplo real:**
```text
Compara estos dos contratos de seguridad:

CONTRATO A (2022 - actual):
[PEGAMOS CONTRATO VIGENTE]

CONTRATO B (2025 - propuesto):
[PEGAMOS CONTRATO NUEVO]

Dime:
1. ¿Cuáles son los cambios principales?
2. ¿Nos afecta positiva o negativamente cada cambio?
3. ¿Hay cambios preocupantes?
4. ¿Qué debería renegociar antes de firmar?
```

### Prompt 4: Análisis de Cláusula Específica

Cuando una cláusula te parece rara y quieres entenderla.

```text
Explícame esta cláusula del contrato:

[PEGA LA CLÁUSULA COMPLETA]

Dime:
1. Qué significa en términos simples
2. Por qué la incluyen (quién se beneficia)
3. ¿Es esto estándar en contratos públicos?
4. Riesgos para nosotros
5. ¿Debería cambiar esto?
```

**Ejemplo real:**
```text
Explícame esta cláusula del contrato de asesoramiento:

"La Administración se reserva el derecho de dar por terminado el contrato, 
sin necesidad de justa causa, en cualquier momento, con una antelación 
mínima de 30 días."

Dime:
1. Qué significa en términos simples
2. Por qué la incluyen (quién se beneficia)
3. ¿Es esto estándar en contratos públicos?
4. Riesgos para nosotros (especialmente económicos)
5. ¿Debería cambiar esto?
```

### Prompt 5: Checklist de Conformidad

Para verificar que el contrato cumple normativa.

```text
¿Este contrato cumple con la LCSP y normativa aplicable?

[PEGA CONTRATO]

Revisa:
1. ¿Tiene todas las cláusulas obligatorias?
2. ¿Especifica criterios de selección?
3. ¿Hay cláusulas prohibidas por ley?
4. ¿Los plazos son legales?
5. ¿Falta algo importante?

Para cada punto: CUMPLE / FALTA / INCUMPLE
```

## Variantes según necesidad

| Necesidad | Añade al prompt |
|---|---|
| **Es muy urgente** | "Responde en máximo 3 párrafos y 5 puntos" |
| **Hay dinero en juego** | "¿Cuáles son los riesgos financieros?" |
| **Datos personales** | "¿Se cumple RGPD? ¿Falta algo?" |
| **Contratista nuevo** | "¿Hay señales de alarma en el contrato?" |
| **Contratista de siempre** | "¿Qué ha mejorado o empeorado vs. el anterior?" |
| **Obras o infraestructura** | "¿Hay cláusulas de responsabilidad de civil?" |

## Ejercicio

**Tu misión: Crea 3 prompts para tu trabajo**

1. **Prompt de resumen:** Para el próximo contrato que recibas (sin analizar, solo entender)
2. **Prompt de riesgos:** Enfocado en lo que más te preocupa en tu contexto
3. **Prompt de comparación:** Usando un contrato anterior que tengas

Escribe los 3 prompts ahora. Si tienes un contrato disponible, pruébalos.

**Pistas:**
- Sé tan específico como puedas
- Incluye el tipo de contrato
- Señala lo que más te importa

## Solución orientativa

<details>
  <summary>¿Quieres ver ejemplos completos?</summary>

**Ejemplo 1 - Resumen de contrato nuevo:**

```text
Analiza este contrato de servicios de mantenimiento de parques y dame un resumen de 5 minutos:

[PEGAMOS CONTRATO]

Incluye:
1. Qué es (una frase)
2. Empresa contratada y duración
3. Presupuesto anual y cómo se paga
4. Qué mantenimiento se cubre (podas, riego, plagas, etc.)
5. Cuándo termina y si es renovable
6. Quién supervisa el trabajo

Solo hechos, nada de análisis legal. Imagina que lo cuentas a un concejal que no sabe.
```

**Ejemplo 2 - Riesgos en contrato de consultoría:**

```text
Revisa este contrato de auditoría externa y detecta riesgos:

[PEGAMOS CONTRATO]

Para cada riesgo:
- Nivel: BAJO / MEDIO / ALTO
- Descripción: qué puede pasar
- Dónde: número de cláusula
- Acción: qué hacer

Enfoque especial:
- Confidencialidad de información (vamos a compartir datos sensibles)
- Responsabilidad por errores en la auditoría
- Salida de datos hacia terceros
- Cómo pagar si hay discrepancias
```

**Ejemplo 3 - Comparación con contrato anterior:**

```text
Compara este contrato de servicios de limpieza 2025 con el de 2022:

ANTIGUO (2022):
[PEGAMOS CONTRATO 2022]

NUEVO (2025):
[PEGAMOS CONTRATO 2025]

Dime:
1. Cambios principales (especialmente en precio)
2. Quién gana en cada cambio
3. Cambios que nos preocupan
4. Qué renegociaría

Contexto: La empresa es la misma, el ayuntamiento es igual, pero ha habido inflación y cambios de ley.
```

</details>

## Reto avanzado

**Nivel 1:** Toma un contrato real, úsalo con los 5 prompts y compara resultados

**Nivel 2:** Crea un "prompt de auditoría" que te permita revisar en 15 minutos si un contrato está listo para firmar

**Nivel 3:** Crea un prompt que detecte cambios peligrosos solo comparando cláusulas clave (sin analizar el contrato completo)

## Qué hemos aprendido

✓ Cada tipo de pregunta genera un tipo diferente de análisis  
✓ Un resumen es el punto de partida, no el destino  
✓ Los riesgos se encuentran en las cláusulas específicas, no en párrafos generales  
✓ Comparar contratos antiguos vs. nuevos revela lo que cambió  
✓ Antes de escalar a abogado, necesitas entender el contrato tú mismo  

**Próximo paso:** Aplicaremos todo esto a un caso práctico real.
