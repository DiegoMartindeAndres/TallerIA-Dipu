# 📊 Caso Práctico: Resúmenes y Síntesis de Normativa

## Objetivo de este caso

Aprenderás a **usar IA para sintetizar leyes complejas en resúmenes ejecutivos** que los políticos y técnicos puedan entender en 5 minutos. Descubrirás cómo mantener precisión jurídica mientras simplificas un RGPD de 99 artículos a los puntos esenciales.

---

## Qué vamos a aprender

✅ Cómo estructurar un prompt de síntesis sin perder exactitud  
✅ Técnicas para "traducir" lenguaje legal a lenguaje comprensible  
✅ Ejemplos reales: RGPD, LOPA, LBRL en 2-3 páginas  
✅ Cómo verificar que el resumen no distorsiona la norma  
✅ Prompts probados en administración pública  
✅ Ejercicios de síntesis progresivos  

---

## Introducción: El problema de la normativa compleja

La administración pública **ahoga en regulación**. Cada año:
- 📌 El RGPD tiene 99 artículos → 700+ páginas de guías
- 📌 La LOPA tiene 80 artículos → documentos interpretativas interminables
- 📌 La LBRL tiene 241 artículos → imposible que los concejales los conozcan todos

**El dilema:**
- Si pedimos "leer la normativa completa" → Nadie la lee
- Si pedimos un resumen manual → Toma semanas y es inconsistente

**La solución: IA instrumento → En 10 minutos tenemos un resumen precisoFielmente resumido** que todos pueden leer.

---

## Diferencia: Un resumen manual vs con IA

### ❌ Síntesis manual (5-7 días)
- Leemos la normativa entera
- Hacemos notas a mano
- Escribimos resumen
- Lo revisamos 2-3 veces
- Resultado: Bueno pero tardío, y solo está en la cabeza de 1 persona

### ✅ Síntesis con IA (45 minutos)
- Proporcionamos el PDF/texto de la norma
- Escribimos prompt de síntesis
- Generamos resumen en 2 minutos
- Revisamos exactitud (20 min)
- Resultado: Disponible para todos, consistente, verificable

---

## La estructura del prompt de síntesis

Para que la IA resuma sin perder precisión, necesitamos:

### 1️⃣ OBJETIVO CLARO
"Extrae los 5-7 puntos esenciales que TODO técnico de administración debe conocer"

### 2️⃣ PÚBLICO OBJETIVO
"Para alcaldes y concejales sin formación jurídica específica"

### 3️⃣ RESTRICCIONES DE EXACTITUD
"No simplifiques conceptos jurídicos: si el original dice 'legitimación activa' NO lo cambies a 'quien puede quejarse'"

### 4️⃣ FORMATO DE SALIDA
"Usa estructura: Punto clave → Definición simple → Artículos → Implicación práctica"

### 5️⃣ VERIFICACIÓN
"Para cada punto, cita el artículo exacto donde aparece"

---

## Ejemplo guiado: Resumir el RGPD en 3 páginas

El **Reglamento General de Protección de Datos (RGPD)** tiene:
- 99 artículos
- 7 capítulos temáticos
- ~700 páginas de guías oficiales
- Multitud de definiciones (tratamiento, responsable, interesado, etc)

**Nuestro objetivo:** Extraer los 5 conceptos que DEBEN conocer los gestores públicos.

### El prompt de síntesis para RGPD

```text
CONTEXTO: Eres un experto en Protección de Datos con 10 años de experiencia 
formando a administraciones públicas.

TAREA: Crea un RESUMEN EJECUTIVO del RGPD para alcaldes y personal administrativo 
sin formación jurídica.

NORMATIVA A RESUMIR:
[Aquí iría el texto completo del RGPD o los artículos clave]

ESTRUCTURA REQUERIDA:
Para cada punto clave:
1. Título simple (no jerga legal)
2. ¿Qué es? (explicación en 2-3 líneas)
3. Artículos del RGPD que lo regulan
4. ¿Por qué nos importa en administración? (implicación práctica)
5. ¿Qué pasa si no lo cumplimos? (consecuencias reales)

PUNTOS A INCLUIR:
- Consentimiento y legitimación
- Derechos de los interesados
- Obligaciones del responsable del tratamiento
- Incidentes de seguridad
- DPD (Delegado de Protección de Datos)

RESTRICCIONES:
- Cada punto máximo 200 palabras
- Cita artículos específicos (ej: Art. 6, apartado 1, letra a)
- No simplifiques conceptos jurídicos: mantén precisión técnica
- Cuando hagas analogía, aclara que es una analogía
- Extensión total: 1500-2000 palabras
- Usa ejemplos españoles (AEPD, administración local)

TONO: Accesible pero preciso. Un alcalde sin asesor legal pueda entenderlo.
```

---

## Variantes de síntesis por tipo de norma

### 📋 Variante 1: SÍNTESIS DE LEYES PROCESUALES

```text
Para leyes sobre procedimiento (Ley 39/2015, etc):
ESTRUCTURA: Paso 1 → Paso 2 → Paso 3 + EXCEPCIONES + RECURSOS
ENFOQUE: Cronología (qué pasa primero, qué después)
EJEMPLO: "Ciudadano presenta solicitud → Administración tiene 3 meses → 
Si no responde = silencio administrativo negativo"
```

### 📋 Variante 2: SÍNTESIS DE REGLAMENTOS TÉCNICOS

```text
Para reglamentos (accesibilidad, seguridad, etc):
ESTRUCTURA: Objetivo → Qué se permite/prohíbe → Sanciones
ENFOQUE: Qué tengo que hacer/qué NO puedo hacer
EJEMPLO: "Real Decreto accesibilidad: Rampas máximo 8% pendiente, 
ascensores obligatorios en >2 plantas"
```

### 📋 Variante 3: SÍNTESIS DE DERECHOS DE CIUDADANOS

```text
Para leyes de derechos (transparencia, acceso, etc):
ESTRUCTURA: Qué derecho tengo → Cómo lo ejercito → Excepciones
ENFOQUE: Desde el punto de vista del ciudadano
EJEMPLO: "Tengo derecho a acceder a documentos públicos en 15 días, 
excepto datos personales de terceros"
```

---

## Ejemplo real: RGPD resumido en puntos clave

<details>
<summary>👇 Haz clic para ver un resumen RGPD real (simplificado)</summary>

### RESUMEN EJECUTIVO: RGPD PARA ADMINISTRACIONES PÚBLICAS

#### PUNTO 1: ¿QUIÉN ES RESPONSABLE DE PROTEGER DATOS?

**¿Qué es?** La administración es "responsable del tratamiento" de datos. Eso significa: tú controlas cómo se usan, y tú eres responsable si algo va mal.

**Artículos:** Art. 4(7), Art. 24

**Implicación práctica:** 
- Tu ayuntamiento es responsable de que los datos del padrón sean seguros
- Si se piratean datos de ciudadanos → La administración responde
- Necesitas procedimientos de seguridad, registros, políticas claras

**¿Qué pasa si no cumples?**
- Multas hasta €20 millones o 4% de ingresos anuales
- El ciudadano puede demandarte por daños

---

#### PUNTO 2: ¿CUÁNDO PUEDO RECOPILAR DATOS?

**¿Qué es?** No puedes recopilar datos "porque sí". Necesitas una razón legal.

**Artículos:** Art. 6(1) - Las 6 bases legales

**Las 6 razones permitidas:**
1. **Consentimiento:** Ciudadano te lo permite (raramente usado en admin)
2. **Contrato:** Necesitas datos para cumplir un servicio
3. **Obligación legal:** Una ley te ordena recopilar (ej: padrón)
4. **Interés vital:** Proteger vida (emergencias médicas)
5. **Función pública:** Administración cumpliendo su misión
6. **Interés legítimo:** Tú o terceros tenemos interés legítimo

**Implicación práctica:**
- Padrón municipal = Base legal "obligación legal"
- Datos de empleados = Base legal "contrato de trabajo"
- Email de candidatos a empleo = Necesita consentimiento

**¿Qué pasa si no tienes base legal?**
- Multa de hasta €10 millones
- Los datos se deben eliminar

---

#### PUNTO 3: ¿QUÉ DERECHOS TIENEN LOS CIUDADANOS?

**¿Qué es?** Los ciudadanos pueden pedirte cosas sobre sus datos.

**Artículos:** Art. 15-22

**Los 6 derechos principales:**
1. **Acceso:** "¿Qué datos tienes de mí?" → Respuesta en 30 días
2. **Rectificación:** "Ese dato es incorrecto, corrígelo"
3. **Supresión:** "Borra mis datos" (si ya no hay razón legal)
4. **Limitación:** "No uses mis datos, solo guárdalos"
5. **Portabilidad:** "Dame mis datos en formato portátil"
6. **Oposición:** "No analices mis datos para X fin"

**Implicación práctica:**
- Ciudadano puede pedirte: "¿Qué datos tienes de mí?"
- Tienes 30 días para responder por escrito
- No puedes cobrar por esto

**¿Qué pasa si no cumples?**
- Multa hasta €10 millones
- El ciudadano puede quejarse a la Autoridad de Protección (AEPD)

---

#### PUNTO 4: ¿CUÁNTO TIEMPO GUARDO LOS DATOS?

**¿Qué es?** No puedes guardar datos indefinidamente. Existe un plazo máximo.

**Artículos:** Art. 5(1)(e), Art. 17

**Regla simple:** "Guarda datos mientras los necesites, bórralos después"

**Ejemplos:**
- Datos de empleado → Mientras trabaja + 6 años (por impuestos)
- Solicitud de subvención rechazada → 4 años (plazo contable)
- Email de ciudadano con consulta → 3 meses después de responder

**Implicación práctica:**
- Necesitas calendario de destrucción de datos
- Automatizar borrado: scripts que eliminen datos a fecha X
- Documentar cuánto tiempo guardas cada tipo de dato

**¿Qué pasa si no cumples?**
- Datos innecesarios = Violación del RGPD
- Multa hasta €10 millones

---

#### PUNTO 5: ¿QUÉ HAGO SI HAY VIOLACIÓN DE DATOS?

**¿Qué es?** Si se piratean/pierden/filtran datos → Hay que avisar a AEPD y ciudadanos.

**Artículos:** Art. 33, Art. 34

**Procedimiento:**
1. **Detectas brecha** → Comunicas a AEPD en 72 horas
2. **Valoras riesgo:**
   - Bajo riesgo → Avisas a AEPD, fin
   - Alto riesgo → Avisas también a ciudadanos afectados
3. **Ciudadanos reciben:** Notificación clara + qué hacer

**Implicación práctica:**
- Necesitas procedimiento de notificación rápida
- AEPD evaluará si fue negligencia tuya
- Más riesgo = Más multa

**¿Qué pasa si no cumples?**
- Multa hasta €20 millones
- Investigación por negligencia
- Responsabilidad civil

</details>

---

## Ejercicio práctico: Resume LOPA en 5 puntos

📋 **Tu tarea:** Crea un RESUMEN EJECUTIVO de la LOPA (Ley Orgánica de Protección de Datos Animales... o si prefieres, de una norma que tengas a mano).

**Tu proceso:**
1. Obtén el texto de la norma (PDF, web oficial, etc)
2. Usa el prompt anterior adaptado
3. Genera resumen de 5 puntos clave
4. Verifica cada punto citando artículos exactos
5. Simplifica lenguaje jurídico a "alcalde lo entienda"

**Tiempo:** 20-30 minutos

**Verificación:**
- ¿Cada punto tiene artículo exacto?
- ¿Un alcalde sin asesor lo entiende?
- ¿Perdiste precisión jurídica al simplificar?

---

## Solución: Cómo verificar que tu resumen es correcto

<details>
<summary>🔓 Checklist de validación de síntesis</summary>

✅ **Artículos citados:** Para cada punto, ¿cita artículo exacto? Verifica en original.

✅ **Precisión jurídica:** ¿La IA simplificó demasiado? Ejemplo:
   - ❌ Incorrecto: "Puedes borrar datos cuando quieras"
   - ✅ Correcto: "Puedes pedir supresión si no existe base legal"

✅ **No inventado:** ¿Todos los conceptos están en la norma original?

✅ **Implicaciones reales:** ¿Las consecuencias son reales? (multas, procedimientos)

✅ **Comprensibilidad:** Lee el resumen a alguien sin formación → ¿Lo entiende?

✅ **Utilidad práctica:** ¿Los responsables pueden tomar decisiones con esto?

</details>

---

## Reto avanzado: Síntesis multi-idioma

🚀 **Desafío:** Crea un resumen de una norma EU (ej: Directiva 2022/2561) en:
1. Español (para gobierno local)
2. Inglés simple (para ciudadanos europeos)
3. Gráfico (infografía mental de conceptos)

Usa el mismo prompt, solo cambia "idioma" y "público objetivo".

---

## Errores comunes en síntesis

❌ **Error 1:** "Simplifica todo, aunque pierda sentido legal"  
✅ **Corrección:** "Simplifica lenguaje, mantén precisión jurídica"

❌ **Error 2:** "No cites artículos, es muy técnico"  
✅ **Corrección:** Citar artículos = verificabilidad (lo opuesto a no verificable)

❌ **Error 3:** "El IA resume solo, sin validación"  
✅ **Corrección:** Siempre verifica síntesis contra original (especialmente números)

---

## Qué hemos aprendido

✅ IA acelera síntesis, pero revisión humana es imprescindible  
✅ Especificar público objetivo mejora mucho la comprensibilidad  
✅ Restricción "no simplifiques jurídica" protege exactitud  
✅ Un buen resumen es reutilizable por años  
✅ Síntesis bien hechas democratizan el conocimiento normativo  

---

## Próximos pasos

→ **Caso Práctico 3:** [Traducción de documentos](./03-Traduccion.md)  
→ **Caso Práctico 4:** [Análisis de datos](./04-Analisis.md)  
→ **Volver a:** [Índice de Casos Prácticos](./README.md)

---

**💡 Tip final:** Guarda tus síntesis → Son documentos reutilizables. Una síntesis del RGPD hoy sirve para capacitación el próximo año.
