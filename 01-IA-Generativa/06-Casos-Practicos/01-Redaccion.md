# 📝 Caso Práctico: Redacción de Documentos Administrativos

## Objetivo de este caso

En este caso aprenderás a **usar IA para redactar informes, resoluciones y oficios administrativos** manteniendo el tono oficial, la precisión jurídica y el cumplimiento normativo. Descubrirás técnicas para que ChatGPT o Claude generen documentos listos para firmar, sin sacrificar la calidad formal.

---

## Qué vamos a aprender

✅ Cómo estructurar un prompt para documentos formales  
✅ Técnicas para mantener tono oficial y vocabulario administrativo  
✅ Cómo evitar errores legales usando IA  
✅ Ejemplos reales: informes de inspección, resoluciones, oficios  
✅ Prompts probados en la administración pública  
✅ Ejercicios prácticos paso a paso  

---

## Introducción: Por qué la IA mejora la redacción administrativa

La redacción administrativa es una habilidad crítica pero **enormemente lenta**. Un informe de inspección puede tomar 2-3 horas. Una resolución requiere revisar normativa, citar artículos, usar referencias correctas.

**Con IA bien instruida:**
- 📌 Reducimos redacción a **20 minutos** (con revisión)
- 📌 Evitamos errores formales y referencias incorrectas
- 📌 Mejoramos consistencia (todos los documentos tienen la misma estructura)
- 📌 Liberamos tiempo para análisis y decisiones reales

**El reto:** La IA por defecto produce texto "natural" pero poco formal. Necesitamos instruirla correctamente.

---

## Diferencia: Un documento sin IA vs con IA

### ❌ Redacción manual (2,5 horas)
- Abrimos plantilla antiguo
- Copiamos párrafos de documentos anteriores
- Buscamos referencias normativas
- Corregimos 3 veces
- Resultado: Bueno pero inconsistente

### ✅ Redacción con IA (30 minutos)
- Estructuramos el prompt (5 min)
- Generamos versión inicial (2 min)
- Revisamos y ajustamos fondo (10 min)
- Resultado: Profesional, consistente, citando normativa correcta

---

## Las partes clave de un buen prompt para documentos

Para que la IA genere documentos administrativos de calidad, necesitamos:

### 1️⃣ ROL CLARO
Definimos quién es la IA: "Eres un experto redactor de documentos administrativos con 15 años de experiencia en la administración pública"

### 2️⃣ CONTEXTO NORMATIVO
Indicamos leyes y procedimientos: "Basándote en la LOPA (Ley Orgánica de Protección de Datos), el artículo 6 de la Ley 30/1992..."

### 3️⃣ RESTRICCIONES FORMALES
Indicamos límites: "Usa segunda persona formal, referencias legales precisas, no inventes excepciones"

### 4️⃣ EJEMPLOS DE ESTRUCTURA
Mostramos cómo queremos que se estructure: "Encabezado → Antecedentes → Hechos → Fundamentos de derecho → Dispositivo"

### 5️⃣ DATOS CONCRETOS
Proporcionamos info específica: Nombres, fechas, artículos, expedientes

---

## Ejemplo guiado: Redactar un informe de inspección

Imagina que necesitas redactar un **informe de inspección de accesibilidad en un edificio público**. Tienes los datos brutos:
- Edificio: Centro Cultural "La Paz", Segovia
- Fecha inspección: 15 de octubre 2024
- Inspector: María García López (colegiado 2845)
- Problemas encontrados: Rampas insuficientes, ascensor sin botones braille, señalética sin contraste
- Normativa: REAL DECRETO 1627/1997 sobre disposiciones mínimas de seguridad

### Paso 1: Estructura básica del prompt

```text
Eres un inspector de accesibilidad con 10 años de experiencia en la administración pública.
Redacta un INFORME TÉCNICO DE INSPECCIÓN siguiendo esta estructura:
- Encabezado con datos del centro
- Antecedentes (motivo de la inspección)
- Hechos observados (problemas encontrados)
- Fundamentos de derecho (normativa aplicable)
- Conclusiones y recomendaciones
- Dispositivo (decisión final)

Usa lenguaje formal, referencias normativas precisas, segunda persona formal.
No inventes datos, usa solo los proporcionados.
```

### Paso 2: Añadimos datos concretos

```text
DATOS:
- Centro: Centro Cultural "La Paz", Segovia, C/ Velarde 23
- Fecha inspección: 15 de octubre 2024
- Inspector: María García López, Colegiada 2845
- Problemas: 
  * Rampa de acceso con pendiente 12% (máximo permitido 8%)
  * Ascensor sin botones en braille
  * Señalética sin suficiente contraste de color
  
NORMATIVA APLICABLE:
- Real Decreto 1627/1997 sobre disposiciones mínimas de seguridad en construcción
- Orden VIV/561/2010 sobre documentación accesible
```

### Paso 3: Indicamos restricciones de calidad

```text
RESTRICCIONES CRÍTICAS:
- Todas las referencias normativas deben citarse textualmente (no inventes artículos)
- Sé específico en medidas: "pendiente 12%" no "demasiada pendiente"
- Usa "se observó" en pasiva formal, nunca "vimos"
- Cada conclusión debe estar fundamentada en derecho, no en opinión
- Proporciona 3 opciones de remediación para cada problema
```

---

## El prompt completo para nuestro informe

Aquí está el **prompt profesional listo para usar**:

```text
CONTEXTO: Eres un inspector técnico de accesibilidad con 12 años de experiencia en administración local. Redactas informes que servirán como base para decisiones administrativas.

TAREA: Redacta un INFORME TÉCNICO DE INSPECCIÓN DE ACCESIBILIDAD siguiendo estructura oficial.

ESTRUCTURA REQUERIDA:
1. Encabezado (Número de expediente, fecha, inspector)
2. Antecedentes (Por qué se hace la inspección)
3. Descripción del centro inspeccionado
4. Hechos observados (Problemas encontrados, medidas específicas)
5. Fundamentos de derecho (Artículos aplicables del RD 1627/1997)
6. Conclusiones (Cumplimiento sí/no fundamentado)
7. Recomendaciones (Acciones concretas para remediar)
8. Dispositivo (Decisión)

DATOS A INCLUIR:
- Centro: Centro Cultural "La Paz", Segovia, C/ Velarde 23, Segovia 40001
- Fecha inspección: 15 de octubre 2024
- Inspector: María García López, Ingeniero Técnico, Colegiado 2845
- Hallazgos técnicos:
  * Rampa entrada principal: pendiente 12% (límite 8% según RD)
  * Ascensor 2ª planta sin botones en braille
  * Señalética emergencia con bajo contraste color (ratio 2:1, mínimo 3:1)
  * Pasillos accesibles: correctos (1,50m de ancho)
  * Puertas de emergencia: Sin botones de apertura accesible

NORMAS DE REDACCIÓN:
- Lenguaje formal, segunda persona impersonal ("se observó", no "encontramos")
- Referencias normativas precisas (cita artículos específicos)
- Números y medidas exactas, no aproximaciones
- Cada conclusión fundamentada en derecho, no en opinión
- Proporciona soluciones concretas para cada deficiencia
- Extensión: 800-1000 palabras
- No inventes datos, normativa o artículos

TONO: Profesional, objetivo, técnico, sin sesgo.
```

---

## Variantes del prompt: Adaptándo a otros documentos

### 📄 Variante 1: RESOLUCIÓN ADMINISTRATIVA

```text
Redacta una RESOLUCIÓN ADMINISTRATIVA consecuencia de una inspección deficiente.
Estructura: Visto el informe + Considerandos legales + Artículos normativos + Parte dispositiva
Requisito: Cita artículo de la ley que sustenta la decisión
Tono: Formal máximo, impersonal
```

### 📄 Variante 2: OFICIO DE NOTIFICACIÓN

```text
Redacta un OFICIO de notificación de una resolución a un ciudadano.
Estructura: Encabezado + Destinatario + Cuerpo (explicación clara) + Recursos + Firma
Requisito: Lenguaje comprensible, explica qué hacer a continuación
Tono: Formal pero accesible
```

### 📄 Variante 3: DICTAMEN JURÍDICO

```text
Redacta un DICTAMEN sobre compatibilidad de una decisión con normativa.
Estructura: Antecedentes + Normativa aplicable + Análisis jurídico + Conclusión
Requisito: Analiza pros/contras, cita jurisprudencia si es relevante
Tono: Analítico, imparcial
```

---

## Ejercicio práctico: Tu turno

📋 **Tu tarea:** Redacta un **informe de inspección de protocolo COVID** en una residencia de mayores.

**Datos brutos que tienes:**
- Centro: Residencia "San José", Ávila, Ctra. de Segovia km 5
- Fecha: 12 de noviembre 2024
- Inspector: Luis Martínez (colegiado 1340)
- Problemas detectados:
  * Dispensadores de desinfectante: Falta en 3 de 5 plantas
  * Carteles informativos: Desactualizados (diciembre 2023)
  * Aislamiento de positivos: Insuficiente (habitaciones compartidas)
  * Protecciones individuales: Stock adecuado en almacén

**Instrucción:** 
1. Copia el prompt anterior
2. Modifica DATOS y contexto específico
3. Genera el informe
4. Revisa: ¿Las referencias normativas son reales? ¿El tono es formal?

**Tiempo:** 15-20 minutos (5 min prompt + 5 min generación + 10 min revisión)

---

## Solución: Informe de ejemplo (oculta)

<details>
<summary>🔓 Haz clic para ver el informe completamente redactado</summary>

```
INFORME TÉCNICO DE INSPECCIÓN

Expediente: INSP/2024/COVID-001
Fecha: 12 de noviembre de 2024
Inspector: Luis Martínez García, Técnico Superior en Prevención
Colegiado: 1340

I. ANTECEDENTES

Por iniciativa del Departamento de Salud Pública, se ha programado una inspección 
de verificación de cumplimiento del protocolo COVID-19 en la Residencia "San José".

II. CENTRO INSPECCIONADO

Denominación: Residencia de Mayores "San José"
Ubicación: Carretera de Segovia km 5, Ávila 05002
Capacidad: 80 residentes
Última inspección: 15 de septiembre 2024

III. HECHOS OBSERVADOS

Durante la visita realizada el 12 de noviembre de 2024, se observaron los siguientes 
aspectos:

A) Medidas de higiene y desinfección:
   - Se verificó la existencia de dispensadores de desinfectante en puntos clave
   - Se detectó DEFICIENCIA: Ausencia de dispensadores en plantas 2, 3 y 4
   - Plantas 1 y 5 disponen de dispensadores funcionales
   - Nivel de stock de gel desinfectante: Adecuado en almacén

B) Información y señalización:
   - Carteles informativos sobre COVID-19: DEFICIENCIA detectada
   - Fecha de actualización de carteles: Diciembre 2023 (caducados hace 11 meses)
   - Contenido: Información sobre síntomas de variantes ya no circulantes

C) Aislamiento y control de positivos:
   - Espacios de aislamiento: 4 habitaciones
   - DEFICIENCIA: Habitaciones de aislamiento compartidas entre 2 residentes positivos
   - Protocolo normativo requiere habitación individual

D) Protecciones individuales:
   - Stock de mascarillas quirúrgicas: 3.000 unidades (suficiente)
   - EPIs para personal: Cantidades adecuadas
   - Esta área CUMPLE requisitos

IV. FUNDAMENTOS DE DERECHO

- Orden SND/398/2020, de 9 de mayo, por la que se establecen medidas de higiene e 
  higiene alimentaria en la industria de alimentación
- Real Decreto-ley 6/2020, de 10 de marzo, por el que se adoptan determinadas medidas 
  urgentes en el ámbito económico
- Protocolo Técnico de Residencias de Mayores ante COVID-19 (Ministerio de Sanidad, 
  2024)

V. CONCLUSIONES

Se DETECTAN DEFICIENCIAS EN:
1. Dispensadores de desinfectante en plantas 2-4
2. Carteles informativos desactualizados
3. Aislamiento de casos positivos en habitaciones compartidas

CUMPLIMIENTO GENERAL: NO FAVORABLE

Se requieren acciones correctoras en 15 días hábiles.

VI. RECOMENDACIONES

1. Instalar dispensadores en todas las plantas (3 equipos adicionales necesarios)
2. Actualizar carteles informativos con información de 2024
3. Habilitar 4 habitaciones de aislamiento individual
4. Revisar protocolo de admisión de positivos

VII. DISPOSITIVO

Se requiere al centro la implementación de medidas correctoras dentro de 15 días 
hábiles. Próxima inspección: 15 de diciembre 2024.

Segovia, 12 de noviembre de 2024
Luis Martínez García
Inspector de Salud Pública - Colegiado 1340
```

</details>

---

## Reto avanzado: Mejora el protocolo

🚀 **Desafío extra:** Usando el mismo prompt, genera versiones para:

1. **ACTA DE INFRACCIÓN** (Si no cumple → parte de sanción)
2. **EMAIL DE NOTIFICACIÓN** (Informal, pero que cite el informe oficial)
3. **RESUMEN EJECUTIVO** (1 página para el consejero)

**Tip:** Modifica solo la sección "ESTRUCTURA REQUERIDA" del prompt. El resto permanece igual.

---

## Errores comunes (y cómo evitarlos)

❌ **Error 1:** "No menciones normalización, solo escribe"  
✅ **Corrección:** Incluye siempre "Fundamentos de derecho" aunque sea simple

❌ **Error 2:** "Genera un documento administrativo"  
✅ **Corrección:** Especifica: "INFORME TÉCNICO", estructura exacta

❌ **Error 3:** Usar ChatGPT sin restricciones  
✅ **Corrección:** Siempre agrega: "No inventes artículos, normativa o datos"

---

## Qué hemos aprendido

✅ La estructura del prompt es 90% del éxito en documentos formales  
✅ Las restricciones ("No inventes") previenen errores críticos  
✅ Ejemplos concretos y datos específicos generan resultados profesionales  
✅ IA acelera redacción pero SIEMPRE requiere revisión de referencias legales  
✅ Un prompt bien hecho es reutilizable en docenas de casos similares  

---

## Próximos pasos

→ **Caso Práctico 2:** [Resúmenes de normativa compleja](./02-Resumen.md)  
→ **Caso Práctico 3:** [Traducción de documentos](./03-Traduccion.md)  
→ **Volver a:** [Índice de Casos Prácticos](./README.md)

---

**📧 Feedback:** ¿Te resultó útil este caso? ¿Quieres ejemplos de qué tipo de documento?  
**💡 Tip:** Guarda el prompt en un documento — lo necesitarás toda la carrera.
