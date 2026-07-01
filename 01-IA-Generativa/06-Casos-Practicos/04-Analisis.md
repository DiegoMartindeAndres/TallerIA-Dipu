# 🔍 Caso Práctico: Análisis de Datos y Textos

## Objetivo de este caso

Aprenderás a **usar IA para extraer información de documentos complejos, identificar patrones y automatizar búsqueda**. Descubrirás cómo analizar expedientes de 200 páginas en minutos.

---

## Qué vamos a aprender

✅ Extracción de datos de documentos complejos  
✅ Identificación de patrones en textos normtivos  
✅ Análisis de expedientes para decisiones administrativas  
✅ Prompts de búsqueda precisa y filtrado  
✅ Validación de resultados de análisis  
✅ Ejercicios progresivos con documentos reales  

---

## Introducción: El análisis manual es lento

La administración pública recibe constantemente:
- 📌 Expedientes de 100+ páginas
- 📌 Solicitudes de acceso a información
- 📌 Alertas de normativa nueva
- 📌 Documentos de terceros para evaluación

**El problema manual:**
- ❌ Analista lee 8 horas para 1 expediente
- ❌ Fácil perder información
- ❌ Inconsistencia entre analistas
- ❌ Costo de tiempo enorme

**Con IA:**
- ✅ Análisis inicial en 2 minutos
- ✅ Resultados consistentes
- ✅ Humano valida no analiza
- ✅ Ahorro 80% del tiempo

---

## Estructura del prompt de análisis

Para análisis preciso, necesitamos:

### 1️⃣ DOCUMENTO CLARO
"Adjunto expediente completo sobre..."

### 2️⃣ OBJETIVO DE ANÁLISIS
"Extrae: 1) Ingresos, 2) Gastos, 3) Irregularidades"

### 3️⃣ FORMATO DE SALIDA
"Tabla con columnas: Concepto | Cantidad | Referencia en documento"

### 4️⃣ RESTRICCIÓN DE EXACTITUD
"Solo extrae información textualmente presente. No interpoles."

### 5️⃣ PRIORIZACIÓN
"Si hay conflicto de datos, señálalo como INCONSISTENCIA"

---

## Ejemplo guiado: Análisis de expediente de facturación

Necesitas **revisar 50 facturas de un proveedor** para verificar si cumple términos de contrato.

**Datos brutos:**
- Contrato establece: "Máximo 2 facturas mensuales, plazo 30 días"
- Tienes 50 facturas de 2024
- Necesitas saber: ¿Cuántas son irregulares?

### El prompt de análisis

```text
CONTEXTO: Eres analista de cumplimiento de contratos en administración pública 
con 8 años de experiencia.

TAREA: Analiza las facturas adjuntas del Proveedor "ABC Servicios" contra el 
Contrato 2024/001.

TÉRMINOS DEL CONTRATO:
- Máximo 2 facturas por mes (si >2 = incumplimiento)
- Plazo de pago: 30 días máximo desde recepción
- Importes máximos por factura: €5.000 (si >€5.000 = incumplimiento)

INSTRUCCIONES:
1. Revisa TODAS las 50 facturas
2. Para cada mes de 2024: cuenta facturas
3. Identifica:
   - Meses con >2 facturas (INCUMPLIMIENTO CANTIDAD)
   - Facturas >€5.000 (INCUMPLIMIENTO IMPORTE)
   - Pagos fuera del plazo de 30 días (INCUMPLIMIENTO PLAZO)

FORMATO DE SALIDA:
[Tabla con columnas:]
Mes | Num Facturas | Importe Total | Facturas >€5k | Facturas Fuera Plazo | Estado

RESUMEN FINAL:
- Total incumplimientos
- Acción recomendada

RESTRICCIONES:
- Solo datos presentes en facturas
- Si información está incompleta, anótalo como [SIN DATOS]
- No estimes o interpoles fechas
```

---

## Ejemplo de resultado esperado

<details>
<summary>👇 Resultado del análisis (tabla)</summary>

| Mes | Num Facturas | Importe Total | Facturas >€5k | Fuera de Plazo | Estado |
|-----|--------|--------|---------|---------|------|
| Enero | 2 | €8.900 | Factura #F001 (€5.200) | 0 | ✅ CUMPLE CANTIDAD, ❌ INCUMPLE IMPORTE |
| Febrero | 3 | €12.400 | Facturas #F005 (€6.000), #F006 (€5.100) | 1 | ❌ INCUMPLE CANTIDAD, IMPORTE, PLAZO |
| Marzo | 2 | €9.500 | Factura #F010 (€5.300) | 0 | ✅ CUMPLE CANTIDAD, ❌ INCUMPLE IMPORTE |
| Abril | 4 | €18.200 | Facturas #F014-F017 (todas >€5k) | 2 | ❌ INCUMPLE CANTIDAD, IMPORTE, PLAZO |
| Mayo | 2 | €8.000 | 0 | 0 | ✅ CUMPLE |
| Junio | 2 | €9.100 | Factura #F025 (€5.050) | 1 | ❌ INCUMPLE IMPORTE, PLAZO |

### RESUMEN DE INCUMPLIMIENTOS
- **Mes Abril:** 4 facturas vs límite 2 (200% incumplimiento)
- **Importes:** 8 de 50 facturas exceden €5.000
- **Plazos:** 4 de 50 facturas pagadas fuera de 30 días
- **Acción recomendada:** Notificar incumplimiento al proveedor, retener próximo pago hasta regularización

### OBSERVACIONES
- Patrón: Febrero-Abril son meses con mayor incumplimiento
- Junio muestra mejora (2 facturas, cumple cantidad)
- [SIN DATOS] Necesita confirmación de fechas de recepción vs pago en facturas #014, #017

</details>

---

## Variantes de análisis por tipo de documento

### 📊 Variante 1: ANÁLISIS DE EXPEDIENTE ADMINISTRATIVO

```text
Para expedientes de solicitudes (subvenciones, licencias):
EXTRAE: 1) Datos solicitante 2) Documentos adjuntos 3) Requisitos cumplidos 
4) Irregularidades
FORMATO: Lista de verificación (Sí/No/Falta)
RESULTADO: Recomendación (Admitir/Denegar/Subsanar)
```

### 📊 Variante 2: ANÁLISIS DE NORMATIVA PARA CAMBIOS

```text
Para detectar qué cambió en una nueva ley vs anterior:
EXTRAE: 1) Artículos modificados 2) Texto anterior vs nuevo 
3) Implicaciones prácticas
FORMATO: Tabla comparativa
RESULTADO: Documento de "Cambios principales"
```

### 📊 Variante 3: ANÁLISIS DE DATOS FINANCIEROS

```text
Para presupuestos, gastos, ingresos:
EXTRAE: 1) Ingresos por categoría 2) Gastos por concepto 3) Saldo 
4) Tendencias
FORMATO: Tabla + análisis de variaciones
RESULTADO: Reporte ejecutivo con alertas
```

---

## Ejercicio práctico: Analiza un expediente de subvención

📋 **Tu tarea:** Analiza un **expediente de solicitud de subvención** incompleto.

**Lo que tienes:**
1. Formulario solicitud (datos solicitante)
2. Presupuesto desglosado
3. Documentos de justificación (algunos faltan)
4. Bases de la convocatoria (requisitos)

**Lo que necesitas:**
1. Crear checklist de requisitos
2. Verificar cuáles se cumplen
3. Listar documentos faltantes
4. Identificar irregularidades
5. Recomendar: Admitir / Denegar / Solicitar subsanación

**Tu proceso:**
1. Define requisitos de la convocatoria en prompt
2. Describe documentos presentes
3. Genera análisis
4. Valida con persona que presentó solicitud

**Tiempo:** 20-30 minutos

---

## Validación de análisis: ¿Es correcto?

<details>
<summary>🔓 Checklist: Validar que análisis es fiable</summary>

### VALIDACIÓN DE EXACTITUD

✅ **Números coinciden:** ¿Las cifras extraídas están textualmente en documento?
   - Verifica 3-5 al azar
   - Si IA dice "€15.000" → Busca en documento exactamente "15.000" o "15000"

✅ **Referencias cruzadas:** ¿IA cita página/sección dónde encontró dato?
   - Debe decir: "Página 5, tabla 3"
   - No confiar en análisis sin referencias

✅ **Completud:** ¿Analizó TODAS las páginas?
   - Cuenta páginas documento
   - Verifica que IA las procesó todas

✅ **Inconsistencias detectadas:** ¿IA señaló conflictos de datos?
   - Buen síntoma: IA dice "Factura #1 dice €1000, Factura #2 dice €900 pero referencia misma transacción"

### VALIDACIÓN DE LÓGICA

✅ **Razonamiento transparente:** ¿Explica POR QUÉ algo es incumplimiento?
   - ❌ Malo: "Abril incumple"
   - ✅ Bueno: "Abril incumple porque contrato dice máx 2 facturas/mes y hay 4"

✅ **Alternativas consideradas:** ¿Menciona interpretaciones posibles?
   - Buen síntoma: "Podría interpretarse como..."

### VALIDACIÓN DE SEGURIDAD

✅ **No alucinó:** ¿Todos los datos están en documento original?
   - Si dice algo que NO existe → RECHAZO total del análisis

✅ **Recomendaciones fundamentadas:** ¿Las recomendaciones tiene base legal?
   - Debe citar artículos, términos de contrato, etc

**Si algo falla:** Rechaza análisis, solicita revisión humana.

</details>

---

## Reto avanzado: Análisis de múltiples documentos

🚀 **Desafío:** Analiza 3 expedientes de diferentes solicitantes, compara y ranking.

**Tarea:**
1. Analiza cada expediente individualmente
2. Extrae puntuación de cumplimiento (0-100%)
3. Ranking de mejores/peores
4. Patrones comunes entre solicitantes

**Resultado:** Matriz de decisión para validar rápidamente 100 solicitudes

---

## Errores comunes en análisis

❌ **Error 1:** "IA analiza sin verificar"  
✅ **Corrección:** Humano verifica 10% de análisis como muestreo

❌ **Error 2:** "No especifico qué extraer"  
✅ **Corrección:** Lista explícita de datos que necesitas

❌ **Error 3:** "IA inventa datos si no los encuentra"  
✅ **Corrección:** Incluir restricción "Solo datos presentes en documento"

❌ **Error 4:** "Confío ciegamente en IA"  
✅ **Corrección:** Muestreo de 10-20% para validar + siempre revisar decisiones críticas

---

## Qué hemos aprendido

✅ IA es herramienta de análisis inicial muy potente  
✅ Especificar formato de salida mejora usabilidad  
✅ Restricción de exactitud previene "alucinaciones"  
✅ Muestreo de validación es imprescindible  
✅ Análisis IA mejora consistencia entre analistas  

---

## Próximos pasos

→ **Caso Práctico 5:** [Brainstorming](./05-Brainstorming.md)  
→ **Bloque 2:** [Introducción a Gemas](../02-Gemas/01-Que-Son-Gemas/01-Concepto.md)  
→ **Volver a:** [Índice de Casos Prácticos](./README.md)

---

**💡 Tip de oro:** Para análisis repetitivos (ej: revisar 100 solicitudes mensuales) → Crea una Gema especializada. Reutilízala todo el año.
