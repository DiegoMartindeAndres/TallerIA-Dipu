# 🌍 Caso Práctico: Traducción y Localización de Documentos

## Objetivo de este caso

Aprenderás a **usar IA para traducir documentos administrativos manteniendo contexto técnico y corrección formal**. Descubrirás cuándo la IA es suficiente, cuándo revisar, y cuándo un humano es obligatorio.

---

## Qué vamos a aprender

✅ Qué pierden/ganan los documentos en traducción IA  
✅ Cuándo usar IA (documentos informales) vs traductor humano (contratos legales)  
✅ Ejemplos: Convenios internacionales, cartas EU, normas técnicas  
✅ Prompts para traducción de documentos administrativos  
✅ Mantener referencias normativas, numeraciones, formato  
✅ Ejercicios de traducción con verificación  

---

## Introducción: El dilema de traducir en administración

Las administraciones públicas necesitan traducir:
- 📌 Convenios de cooperación internacional
- 📌 Cartas oficiales a ciudadanos franceses/portugueses
- 📌 Documentos de Bruselas (reuniones EU)
- 📌 Manuales técnicos de equipamiento
- 📌 Correspondencia con organismos internacionales

**El problema:**
- ❌ Un traductor profesional cuesta 200-400€/página
- ❌ Tarda 1-2 semanas
- ❌ Pero la urgencia es ahora

**La oportunidad:**
- ✅ IA traduce en 1 minuto
- ✅ Coste: Casi gratis
- ✅ Pero: Necesita revisión de exactitud

---

## Diferencia: Tipos de traducciones según riesgo

### 🟢 TRADUCCIÓN BAJA RIESGO (IA solo)
- 📄 Email informativo a ciudadano extranjero
- 📄 Foleto informativo sobre servicios
- 📄 Resumen de noticia para web
- ⏱️ Tiempo IA: 2 minutos

### 🟡 TRADUCCIÓN MEDIO RIESGO (IA + revisión técnica)
- 📄 Acuerdo de colaboración no vinculante
- 📄 Documento de orientación política
- 📄 Manual técnico de procedimiento
- ⏱️ Tiempo total: 30 minutos (15 IA + 15 revisión)

### 🔴 TRADUCCIÓN ALTO RIESGO (Traductor profesional)
- 📄 Contrato legal (convenio, concesión)
- 📄 Instrumento vinculante (resolución oficial)
- 📄 Documento de responsabilidad (sentencia)
- ⏱️ Tiempo: 1-2 semanas + €500+

---

## Estructura del prompt de traducción

Para que la IA traduzca bien documentos administrativos:

### 1️⃣ IDIOMAS PRECISOS
"Traduce del español al francés" (no "al francés europeo" → genera confusión)

### 2️⃣ CONTEXTO ADMINISTRATIVO
"Documento oficial de administración municipal española"

### 3️⃣ RESTRICCIONES DE FORMATO
"Mantén numeraciones, referencias, viñetas exactamente igual"

### 4️⃣ PRESERVACIÓN DE TÉRMINOS TÉCNICOS
"Términos como 'RGPD', 'AEPD', 'padrón municipal' NO traducir"

### 5️⃣ TONO OBJETIVO
"Traduce formal, oficial. No suavices lenguaje ni cambies significado"

---

## Ejemplo guiado: Traducir una resolución administrativa

Necesitas traducir al inglés una **resolución de otorgamiento de subvención** para que entiendan ciudadanos/autoridades UK.

### El documento original (español)

```
RESOLUCIÓN DE OTORGAMIENTO DE SUBVENCIÓN

Visto el expediente 2024/3456, tramitado en virtud de la Convocatoria de 
Subvenciones para Proyectos de Accesibilidad, convocada por Orden de esta 
Consejería de 15 de marzo de 2024.

CONSIDERANDOS

Primero.- Que la solicitante ha cumplido los requisitos formales establecidos 
en las bases de la convocatoria.

Segundo.- Que el proyecto presentado tiene especial relevancia para la comunidad 
local.

DISPOSITIVO

Artículo Único.- Se otorga subvención por importe de €15.000 (quince mil euros) 
al Proyecto "Digitalización de Servicios", con código de proyecto DIG-2024-001.

La subvención se abonará conforme a lo previsto en el artículo 4 de la Orden 
de Convocatoria.

Segovia, 25 de octubre de 2024
```

### Prompt para traducir al inglés

```text
TAREA: Traduce al inglés británico el siguiente documento administrativo español.

CONTEXTO:
- Documento: Resolución administrativa de otorgamiento de subvención
- Origen: Administración municipal española
- Público: Ciudadanos y autoridades UK que necesitan comprender la decisión oficial

RESTRICCIONES CRÍTICAS:
1. Formato exacto: Mantén estructura, numeraciones (Artículo Único, Considerandos)
2. Términos NO traducir:
   - Orden de Convocatoria (mantén en español)
   - Expediente 2024/3456 (número exacto)
   - €15.000 (símbolo euro, cantidad exacta)
3. Tono: Formal máximo, oficial, imperativo
4. Lenguaje legal: Usa términos legales en inglés ("hereby grants", "pursuant to")
5. Fechas: Mantén formato español (25 de octubre de 2024 = 25 October 2024)

VALIDACIÓN:
- Verifica que importes en €, referencias y números son idénticos
- Asegúrate que "Considerandos" se traduce a estructura legal inglesa equivalente
- La fecha debe estar en formato internacional correcto

SALIDA:
Documento completo traducido, formato idéntico al original.
```

---

## Traducción esperada (resultado con IA)

```
RESOLUTION GRANTING SUBSIDY

Having reviewed the case file 2024/3456, processed under the Convocation for 
Grants for Accessibility Projects, convened by Order of this Department of 
15 March 2024.

RECITALS

First.- That the applicant has fulfilled all formal requirements established 
in the convocation bases.

Second.- That the project presented has special relevance for the local community.

OPERATIVE PART

Single Article.- A subsidy of €15,000 (fifteen thousand euros) is hereby granted 
to the "Digitalization of Services" Project, with project code DIG-2024-001.

The subsidy shall be paid in accordance with the provisions of Article 4 of the 
Convocation Order.

Segovia, 25 October 2024
```

**Nota:** IA preservó:
- ✅ Estructura exacta (Recitals, Operative Part)
- ✅ Importes y referencias numéricas idénticas
- ✅ Formato de fechas internacional
- ✅ Código de proyecto exacto
- ✅ Tono formal y oficial

---

## Variantes de traducción por tipo de documento

### 📝 Variante 1: TRADUCCIÓN CON REFERENCIAS LEGALES

```text
Para documentos que citan leyes/normas:
- Las normas españolas (ej: "Ley 30/1992") mantienen número, NO traducir nombre
- Si existe equivalente legal en país destino, añade nota al pie
- Ejemplo: "Pursuant to Law 30/1992 (equivalent to the UK Administrative 
  Procedure Act)"
- SIEMPRE verifica referencias legales existen en país destino
```

### 📝 Variante 2: TRADUCCIÓN DE TÉRMINOS ADMINISTRATIVOS ESPAÑOLES

```text
Para documentos de administración local/autonómica:
- "Consejería" → "Department" (UK) o "Ministry" (contexto)
- "Diputación" → "Provincial Council"
- "Padrón municipal" → "Municipal Register" (explicación en nota al pie)
- "Orden de Consejería" → "Departmental Order"
- NUNCA inventes: si término no tiene equivalente exacto, explica en nota
```

### 📝 Variante 3: TRADUCCIÓN DE DOCUMENTOS EU

```text
Para documentos que circulan en Europa:
- Usa inglés europeo (no solo británico)
- Mantén estructura de documentos EU (ej: "Considerando A, B, C" → "Recital A, B, C")
- Cita referencias EU exactamente (ej: "Reg. (UE) 2018/1807")
- Traduce títulos de directivas si existen versiones oficiales en inglés
```

---

## Ejercicio práctico: Traduce un documento oficial

📋 **Tu tarea:** Traduce un **comunicado oficial** de tu administración al portugués.

**Documento de ejemplo (que debes adaptar con tus datos):**

```
COMUNICADO OFICIAL

La Diputación de Segovia informa que, a partir del 1 de noviembre de 2024, 
los trámites administrativos se tramitarán mediante el sistema de expediente 
electrónico conforme a lo previsto en la Ley 39/2015.

Los ciudadanos podrán presentar solicitudes a través del portal www.diputacion-segovia.es.

Se prevé reducción de plazos administrativos del 20%.

Segovia, 28 de octubre de 2024
Área de Administración Electrónica
```

**Tu proceso:**
1. Selecciona un documento actual de tu administración
2. Especifica idioma destino (francés, alemán, inglés, portugués)
3. Escribe prompt usando estructura anterior
4. Genera traducción
5. Verifica:
   - ¿Números y fechas son exactos?
   - ¿URLs sin cambios?
   - ¿Tono formal mantenido?
6. Revisa con hablante nativo si es posible

**Tiempo:** 20 minutos

---

## Verificación de calidad de traducción

<details>
<summary>🔓 Checklist: ¿Es buena la traducción IA?</summary>

### Verificación OBLIGATORIA

✅ **Números exactos:** €, expedientes, artículos → ¿Idénticos?
✅ **Fechas:** Formato correcto en idioma destino
✅ **Referencias normativas:** Mantienen código original
✅ **URLs:** No traducidas, exactamente como original
✅ **Nombres propios:** Iguales (Segovia, España, etc)
✅ **Acrónimos:** AEPD, RGPD, LOPA → Sin traducir

### Verificación DE CALIDAD

✅ **Estructura:** ¿Es idéntica a original?
✅ **Tono:** ¿Mantiene formalidad?
✅ **Términos legales:** ¿Usa vocabulario legal correcto en idioma destino?
✅ **Ambigüedad:** ¿Hay párrafos que se pueden malinterpretar?
✅ **Claridad:** Lee a hablante nativo → ¿Entiende claramente?

### Verificación DE SEGURIDAD

✅ **Responsabilidad legal:** ¿Cambia significado alguna frase?
✅ **Interpretación:** ¿Una mala traducción podría cambiar decisión legal?
✅ **Contexto perdido:** ¿Hay notas al pie necesarias?

**Si algo falla:** = Revisar por humano. No publicar.

</details>

---

## Reto avanzado: Localización multi-país

🚀 **Desafío:** El mismo documento para 3 países = 3 traducciones DIFERENTES

**Mismo documento en:**
1. **Inglés UK** (British English, referencias legales UK)
2. **Inglés USA** (American English, términos americanos)
3. **Francés** (referencias legales francesas)

Cada traducción incluye:
- Nota al pie explicando diferencias legales de cada país
- Términos administrativos adaptados localmente

---

## Errores comunes en traducción

❌ **Error 1:** Usar IA sin mencionar contexto administrativo  
✅ **Corrección:** Incluir siempre "es documento oficial administrativo"

❌ **Error 2:** Traducir referencias normativas (perderás rastreabilidad)  
✅ **Corrección:** Referencias originales + nota al pie con equivalente

❌ **Error 3:** "La IA traduce solo, confiamos ciegamente"  
✅ **Corrección:** SIEMPRE revisar números, fechas, términos legales

❌ **Error 4:** Publicar traducciones sin revisar por nativo  
✅ **Corrección:** Para oficial → revisar por traductor profesional

---

## Cuándo SÍ y cuándo NO usar IA para traducción

### ✅ USAR IA
- Documentos informativos
- Borradores internos
- Comunicados de bajo riesgo
- Documentos con plazo urgente
- Orientación/guías

### ❌ NO USAR IA
- Contratos legales
- Sentencias/resoluciones vinculantes
- Documentos de responsabilidad civil
- Que requieran certificación oficial
- Donde error = daño legal

**Regla:** Si el error en traducción puede causar daño legal → Traductor profesional.

---

## Qué hemos aprendido

✅ IA es herramienta rápida para traducciones de bajo riesgo  
✅ Contexto administrativo mejora calidad significativamente  
✅ Mantener referencias y números es crítico  
✅ Revisión humana no es opcional para documentos serios  
✅ Cada idioma/país puede requerir adaptaciones locales  

---

## Próximos pasos

→ **Caso Práctico 4:** [Análisis de datos](./04-Analisis.md)  
→ **Caso Práctico 5:** [Brainstorming](./05-Brainstorming.md)  
→ **Volver a:** [Índice de Casos Prácticos](./README.md)

---

**🌐 Consejo final:** Para administración pública, crea un "diccionario de términos" de tu administración (Consejería → Department) y úsalo en todos los prompts. Garantiza consistencia.
