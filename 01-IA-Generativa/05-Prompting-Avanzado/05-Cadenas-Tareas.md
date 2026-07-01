# Cadenas de Tareas: Orquestación de Múltiples Prompts

## Objetivo

Aprender a descomponer tareas complejas en múltiples prompts secuenciales, manteniendo contexto entre pasos y mejorando control y calidad del resultado final.

### Qué vamos a aprender

- Qué es una cadena de tareas y cuándo es necesaria
- Diferencia entre "un prompt complejo" y "múltiples prompts encadenados"
- Cómo diseñar el flujo: qué información pasa de paso a paso
- Gestión de contexto entre prompts
- Manejo de errores en cadenas
- Casos prácticos de administración pública

---

## Concepto: ¿Por Qué Encadenar?

### Problema: Un Prompt Gigante
```text
Lee este formulario de solicitud. Extrae campos. Clasifica riesgo. 
Verifica conformidad. Genera informe. Proporciona recomendación. 
Redacta comunicación al solicitante.
```

**Problemas:**
- Prompt muy largo, confuso, desordenado
- Difícil de depurar si algo falla
- Sin intermedios, no verificas cada paso
- Si falla en mitad, pierdes todo
- No puedes reutilizar pasos

### Solución: Cadena Estructurada
```
PASO 1: Extracción (lectura formulario)
    ↓ (salida: datos estructurados)
PASO 2: Clasificación (análisis riesgo)
    ↓ (salida: nivel riesgo + justificación)
PASO 3: Verificación (conformidad legal)
    ↓ (salida: conformidad sí/no + observaciones)
PASO 4: Análisis (síntesis de pasos anteriores)
    ↓ (salida: informe técnico)
PASO 5: Recomendación (decisión final)
    ↓ (salida: recomendación + fundamentos)
PASO 6: Comunicación (redacción para solicitante)
    ↓ (salida: borrador comunicación)
```

**Ventajas:**
- Cada paso es claro, auditable
- Puedes verificar intermedios
- Si falla paso 3, sabes exactamente dónde
- Reutilizas pasos en otros procesos
- Control explícito

---

## Ejemplo 1: Procesamiento de Solicitud de Acceso a Información (6 pasos)

### Contexto de la Cadena
Ciudadano solicita acceso a información sobre contrataciones públicas. Necesitas: lectura → clasificación → conformidad legal → riesgos → decisión → comunicación.

### Paso 1: Extracción
```text
Extrae de esta solicitud de acceso a información:
- Solicitante (anonimizado como "Ciudadano X")
- Información solicitada (tema específico)
- Formato solicitado
- Fecha solicitud
- Email contacto

Estructura: JSON con estos campos.

[Solicitud]
```
**Salida esperada:** Datos estructurados en JSON

---

### Paso 2: Clasificación de Información Solicitada
```text
Actúa como especialista en Transparencia y Acceso a Información.

Tenemos estas categorías de información:
- PÚBLICA: Sin restricciones
- PARCIALMENTE LIMITADA: Contiene datos que requieren redacción
- RESTRINGIDA: Excepciones legales aplicables
- NO DISPONIBLE: No existe en nuestros archivos

Información solicitada (del paso anterior):
[Información extraída del paso 1]

Clasifica y justifica cada clasificación.

Salida: JSON con { categoría, justificación, excepciones_aplicables }
```
**Salida esperada:** Clasificación con justificación legal

---

### Paso 3: Verificación de Conformidad Legal
```text
Actúa como Abogado Administrativo especializado en Ley de Transparencia.

Tenemos la siguiente solicitación y clasificación:
[Resultado paso 2]

VERIFICA:
- ¿Es derecho legítimo del solicitante?
- ¿Se aplican excepciones legales correctamente?
- ¿Hay normativa sectorial que limite?
- ¿Hay datos personales que proteger (RGPD)?

Proporciona análisis detallado y dictamen (Conforme/No conforme/Condicionado)

Formato: 
- Resumen ejecutivo
- Análisis detallado
- Dictamen final
- Próximos pasos si procede
```
**Salida esperada:** Dictamen legal estructurado

---

### Paso 4: Evaluación de Riesgos y Factibilidad
```text
Actúa como Responsable de Cumplimiento.

Tenemos: 
- Solicitud clasificada (paso 2)
- Dictamen legal (paso 3)

EVALÚA:
1. Riesgo de reputación (positivo/negativo/neutral)
2. Riesgo operacional (complejidad de recopilación)
3. Riesgo legal (probabilidad de recurso)
4. Viabilidad (¿podemos proporcionar en plazo legal?)

Proporciona puntuación 1-5 en cada factor.
Si algún riesgo es >3, destácalo.

Salida: Matriz de riesgos con recomendaciones de mitigación.
```
**Salida esperada:** Matriz de riesgos y recomendaciones

---

### Paso 5: Decisión y Recomendación Final
```text
Eres comisión evaluadora de acceso a información.

Tenemos:
- Clasificación legal (paso 2)
- Dictamen legal (paso 3)
- Matriz de riesgos (paso 4)

DECIDE:
- CONCEDER (acceso total)
- CONCEDER PARCIALMENTE (con redacciones)
- DENEGAR (con justificación de excepciones)

Justifica la decisión en máximo 3 puntos clave.

Salida: Decisión + fundamento + observaciones.
```
**Salida esperada:** Decisión administrativa motivada

---

### Paso 6: Redacción de Comunicación
```text
Redacta comunicación oficial al solicitante.

Información:
- Decisión (paso 5): [decisión]
- Fundamento (paso 5): [fundamento]
- Plazo: 10 días hábiles desde recepción
- Derecho a recurso: Explicar brevemente

RESTRICCIONES:
- Tono profesional, no técnico
- Accesible para ciudadano promedio
- Incluir datos de contacto para recurso
- Anonimizar datos sensibles internos

Formato: Borrador de carta oficial.

[Todos los datos anteriores]
```
**Salida esperada:** Borrador de comunicación profesional

---

## Ejemplo 2: Análisis de Contrato de Proveedor (4 pasos)

### Paso 1: Extracción Estructurada
```text
Extrae de este contrato de suministro:
- Partes contratantes
- Objeto del contrato
- Duración y plazos
- Precio y forma de pago
- Cláusulas clave (responsabilidad, terminación, resolución)

Formato: JSON con estructura clara.
```

### Paso 2: Identificación de Riesgos Legales
```text
Actúa como Abogado Administrativo.

Contrato extraído:
[Del paso 1]

Identifica problemas en:
- Compatibilidad con LCSP
- Cláusulas abusivas
- Ausencia de cláusulas necesarias
- Riesgos de responsabilidad

Formato: Lista de riesgos con severidad (crítico/alto/medio/bajo).
```

### Paso 3: Recomendaciones de Enmienda
```text
Actúa como Especialista en Negociación Contractual.

Riesgos identificados:
[Del paso 2]

Para cada riesgo crítico o alto:
- ¿Qué cambio se necesita?
- ¿Cómo redactar la enmienda?
- ¿Qué argumento usar con el proveedor?

Formato: Tabla con columnas [Riesgo | Enmienda propuesta | Argumento].
```

### Paso 4: Decisión Final
```text
¿Recomendación final?
- FIRMAR TAL CUAL (solo si no hay riesgos críticos)
- FIRMAR CON ENMIENDAS (si acepta cambios)
- RENEGOCIAR (si hay conflictos
- NO FIRMAR (si riesgos son inaceptables)

Justifica brevemente y proporciona próximos pasos.
```

---

## Gestión de Contexto Entre Pasos

### Patrón 1: Resumen Propagable
```text
[Después del paso anterior]

RESUMEN PARA SIGUIENTE PASO:
- Punto clave 1
- Punto clave 2
- Punto clave 3

[Ahora el siguiente paso inicia con este resumen]
```

### Patrón 2: Entrega Explícita de Contexto
```text
INFORMACIÓN DEL PASO ANTERIOR:
[Resultado paso N, resumido en máximo 3 puntos]

CONTINUAMOS CON:
[Nuevo paso, que aprovecha contexto]
```

### Patrón 3: Verificación Entre Pasos
```text
ANTES DE CONTINUAR:
¿Estamos de acuerdo en esto?
- Interpretación del paso anterior
- Supuestos que hacemos
- Decisiones ya tomadas

[Si no concuerdan, solicita aclaración]
```

---

## Manejo de Errores en Cadenas

### Error en Paso Intermedio: ¿Qué hacer?
```text
Si el resultado del paso X no es satisfactorio:

1. DIAGNOSTICA: ¿Qué salió mal?
   - ¿Prompt poco claro?
   - ¿Entrada deficiente?
   - ¿Restricción o interpretación?

2. SOLUCIONA: Vuelve a ejecutar ese paso con correcciones
   - Ajusta instrucciones si fue confusión
   - Proporciona entrada más clara si fue datos
   - Simplifica si fue sobrecarga

3. CONTINÚA: Una vez solucionado, avanza a siguiente paso
```

### Punto de Control: Verificación Explícita
```text
Después de cada paso importante:
"¿Estás de acuerdo con este resultado? Sí / No

Si no, explica qué debería ser diferente."
```

---

## Ejercicio

**Situación:**
Necesitas procesar una denuncia de incumplimiento administrativo. Requiere múltiples análisis antes de decisión.

**Tu tarea:**
Diseña una **cadena de 4-5 pasos** para procesar esta denuncia:

```
Denuncia: "Junta de contratación no evaluó criterios segundo adjudicatario. 
Licitación parecía favorable a empresa A. No hay documentación de razonamiento."
```

**Pasos que debes especificar:**
1. Extracción de hechos denunciados
2. Identificación de normativa relevante
3. Análisis de cumplimiento
4. Evaluación de riesgos de investigación
5. Recomendación (investigar sí/no)

**Instrucciones:**
- Para cada paso, escribe el prompt explícitamente
- Define exactamente qué información pasa de paso a paso
- Especifica formato de salida en cada paso
- Añade un paso 6 (opcional): redacción de respuesta a denunciante

**Tiempo:** 30 minutos

---

## Solución Orientativa

<details>
  <summary>¿Quieres ver cómo estructurar la cadena de denuncia?</summary>

### Cadena de 5 Pasos: Procesamiento de Denuncia

#### PASO 1: Extracción de Hechos
```text
Extrae de esta denuncia administrativa:
- Hechos específicos (qué pasó, no interpretaciones)
- Fechas y actores implicados (anonimizados)
- Documentos mencionados (ausentes o presentes)
- Régimen de contratación mencionado

Estructura: JSON con campos claros.
Ej: { hechos: [], fechas: [], actores: [], documentación: [] }

[Denuncia]
```

**Salida esperada:** Datos estructurados, anonimizados

---

#### PASO 2: Identificación de Normativa
```text
Actúa como Abogado Administrativo especializado en contratación pública.

Hechos extraídos:
[Del paso 1]

Identifica:
- Régimen de contratación aplicable (¿LCSP? ¿Privado?)
- Normativa sobre evaluación de criterios
- Documentación obligatoria
- Plazos de recursión

Formato: Lista de normativa aplicable con referencias exactas.
```

**Salida esperada:** Marco legal identificado

---

#### PASO 3: Análisis de Cumplimiento
```text
Actúa como Auditor de Organismos Públicos.

Normativa identificada:
[Del paso 2]

Hechos denunciados:
[Del paso 1]

ANALIZA:
- ¿Qué debería haber sucedido según normativa?
- ¿Qué sucedió según hechos denunciados?
- ¿Hay desviación clara?
- ¿Hay documentación que justifique lo sucedido?

Formato: Análisis comparativo, claro.
```

**Salida esperada:** Identificación de posibles incumplimientos

---

#### PASO 4: Evaluación de Riesgos de Investigación
```text
Actúa como Responsable de Compliance.

Posibles incumplimientos:
[Del paso 3]

EVALÚA:
- Probabilidad de hallazgo si investigamos (1-5)
- Riesgo reputacional de investigación (positivo/neutro/negativo)
- Riesgo legal para organización (probabilidad de demanda)
- Recursos necesarios (esfuerzo investigación)

Formato: Matriz de riesgos
```

**Salida esperada:** Evaluación de conveniencia de investigación

---

#### PASO 5: Recomendación
```text
COMISIÓN EVALUADORA: Decides sobre la denuncia.

Análisis completo:
- Hechos: [Del paso 1]
- Normativa: [Del paso 2]
- Incumplimientos potenciales: [Del paso 3]
- Riesgos: [Del paso 4]

DECIDE:
1. ¿INVESTIGAR (sí/no)?
   Fundamento en máximo 3 puntos

2. Si SÍ, ¿Qué investigar prioritariamente?

3. ¿Notificar al denunciante? ¿Cómo?

Formato: Decisión administrativa motivada
```

**Salida esperada:** Decisión clara y fundamentada

---

#### PASO 6 (OPCIONAL): Respuesta a Denunciante
```text
Redacta respuesta oficial al denunciante.

Información:
- Hechos reconocidos: [relevantes del paso 1]
- Decisión: [Del paso 5]
- Justificación: [Del paso 5, simplificada]

RESTRICCIONES:
- Tono profesional, respetuoso
- No accedes a proporcionar información sobre investigación en curso
- Informas de derechos de recurso
- Plazo de respuesta explicado

Formato: Borrador de comunicación oficial
```

**Salida esperada:** Comunicación profesional

---

### Cómo usar esta cadena

1. **Fase de entrada:** Copia denuncia íntegra
2. **Paso 1:** Ejecutas, obtienes datos estructurados
3. **Paso 2:** Copias resultado paso 1, ejecutas, obtienes marco legal
4. **Paso 3:** Copias resultados 1+2, ejecutas, obtienes análisis
5. **Paso 4:** Copias resultado 3, ejecutas, obtienes riesgos
6. **Paso 5:** Copias 1+3+4, ejecutas, obtienes recomendación
7. **(Opt) Paso 6:** Copias 1+5, ejecutas, obtienes comunicación

**Control de calidad:** Después de cada paso, verifica que resultado tenga sentido antes de continuar.

</details>

---

## Reto Avanzado

**Nivel: Experto**

Diseña una cadena de tareas que combine:
1. **Múltiples pasos** (5-7)
2. **Diferentes roles** (Abogado, Auditor, Compliance en pasos distintos)
3. **Diferentes formatos** (JSON en extracción, tabla en análisis, texto en recomendación)
4. **Gestión de contexto** (cada paso usa outputs anteriores)

Desafío extra: Añade **puntos de control** donde pidas verificación antes de continuar.

---

## Qué Hemos Aprendido

✅ **Cadenas > Prompts monolíticos:** Descomponer en pasos mejora calidad y control.

✅ **Cada paso es auditable:** Puedes revisar exactamente dónde ocurrió cada decisión.

✅ **Reutilización:** Un paso diseñado bien se reutiliza en múltiples procesos.

✅ **Manejo de errores:** Si falla un paso, sabes exactamente cuál y puedes rehacerlo.

✅ **Contexto es clave:** Pasar información correcta entre pasos es crítico.

✅ **Complejidad manejable:** Lo que parece imposible en un prompt es factible en cadena.

✅ **Documentación natural:** La cadena misma documenta el proceso de decisión.

---

## Síntesis: De Técnicas Aisladas a Orquestación Completa

Hemos aprendido cinco técnicas avanzadas:

1. **Roles Especializados:** Perspectivas diferentes
2. **Formatos de Salida:** Estructura exacta
3. **Chain of Thought:** Razonamientos explícitos
4. **Restricciones:** Límites de seguridad
5. **Cadenas de Tareas:** Orquestación de múltiples prompts

**La magia ocurre cuando las combinas:**

```
PROMPT POTENTÍSIMO = 
  Rol específico 
  + Razonamiento paso a paso (CoT)
  + Restricciones claras
  + Formato exacto de salida
  + Parte de una cadena de tareas
  + Con contexto de pasos anteriores
```

**Ejemplo final completo:**

```text
Paso 3 de 5: Análisis de Conformidad

Actúa como Abogado Administrativo especializado en LCSP. [ROL]

Información de pasos anteriores:
- Hechos: [del paso 1]
- Normativa: [del paso 2]

Analiza paso a paso: [CHAIN OF THOUGHT]
1. ¿Qué dice la normativa exactamente?
2. ¿Qué sucedió en el caso?
3. ¿Hay desvío?
4. ¿Es grave?
5. ¿Defensible?

Restricciones: [RESTRICCIONES]
- No revelaré identidades específicas
- Basaré análisis en normativa publicada
- Señalaré si hay ambigüedad normativa

Proporciona resultado en tabla Markdown: [FORMATO]
| Aspecto | Normativa | Hecho | Cumple | Riesgo |

[CONTENIDO: Datos del caso]
```

Esto es la cúspide del prompting profesional. 🎯

**¿Siguiente nivel?** Las "Gemas" en el Bloque 2 llevan esto a casos reales e integrados. Ya tienes las herramientas; ahora aprenderás dónde aplicarlas con máximo impacto.
