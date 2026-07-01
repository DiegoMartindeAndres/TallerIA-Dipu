# Detalle Técnico: Los 3 Pilares

## Objetivo
Entender profundamente POR QUÉ cada pilar funciona y CÓMO aplicarlo con precisión.

## Qué Aprenderemos
- Anatomía de un prompt Karpathy
- Por qué el contexto "resetea" el pensamiento de la IA
- La ciencia detrás de restricciones que mejoran creatividad
- Cómo integrar los 3 pilares en 60 segundos

---

## Pilar 1: CONTEXTO (The Foundation)

### Qué Es
Establecer el "universo" en el que la IA trabaja.

### Por Qué Funciona

La IA moderna (como GPT-4) procesa el contexto como **instrucciones implícitas**. Sin contexto, asume suposiciones. Con contexto, se "calibra" automáticamente.

**Ejemplo mental:**

```
Pides: "Redacta un memo"
IA piensa: "¿Memo de qué? ¿Para quién? ¿Formal? ¿Casual? 
           Voy a asumir algo genérico..."

Pides: "Redacta un memo administrativo interno, para director
        municipio, sobre atraso de presupuesto, tono profesional"
IA piensa: "Contexto claro. Público: ejecutivo municipal.
           Tono: formal pero urgente. Tema: financiero = precise..."
```

### Componentes Clave del CONTEXTO

#### 1. Rol/Expertise
```text
Eres experto en:
- Administración pública municipal
- Procesos de contratación
- Normativa estatal y autonómica
```

**Por qué:** Define la "lente" con que interpreta la información.

#### 2. Audiencia Específica
```text
Tu lector es:
- Director/a de un ayuntamiento de 50.000 habitantes
- 10+ años experiencia en gestión pública
- Interesado en eficiencia y cumplimiento legal
- Sin paciencia para explicaciones obvias
```

**Por qué:** Calibra nivel de detalle, jerga, tone.

#### 3. Objetivo Comercial/Administrativo
```text
El objetivo es:
- Mejorar eficiencia sin aumentar presupuesto
- Cumplir normativa reciente (Orden XXX/2024)
- Generar documentación defensible legalmente
```

**Por qué:** Prioriza qué importa, qué es secundario.

#### 4. Restricciones del Contexto
```text
Consideraciones:
- Este municipio tiene presupuesto TIC limitado (< 50.000€/año)
- Plantilla actual: 87 personas, sin área de IA
- Sistema actual: Compartidas municipales, sin SGAD moderno
```

**Por qué:** Fuerza soluciones realistas, no idealistas.

### Formato Mínimo de CONTEXTO

```text
CONTEXTO:
Eres consultor administrativo especializado en [ESPECIALIDAD].
Tu cliente es [PERFIL CLIENTE].
El objetivo es [OBJETIVO ESPECÍFICO].
Restricciones: [LÍMITES REALES].
```

**Tiempo:** 30-60 segundos para escribir.
**Impacto:** +30-40 puntos de calidad.

---

## Pilar 2: TAREA (The Precision)

### Qué Es
La definición exacta de QUÉ necesitas que la IA produzca.

### Por Qué Funciona

La ambigüedad es el enemigo de la calidad. Cuanta más precisión, menos "adivinanza" necesita hacer la IA.

**Niveles de claridad:**

#### Nivel 1: Vago (✗ Evita)
```text
"Analiza nuestros presupuestos"
```
**Problema:** ¿Cuántos años? ¿Qué busca? ¿Qué compara?

#### Nivel 2: Mejor
```text
"Compara presupuesto 2023 vs 2024"
```
**Problema:** ¿En qué aspecto? ¿Qué departamentos? ¿Variación importante = qué %?

#### Nivel 3: Karpathy (✓ Ideal)
```text
TAREA:
Compara presupuesto 2024 vs 2023 específicamente en:
- Gastos de personal: variación > 5%
- Servicios externos: nuevas contrataciones vs cancelaciones
- Capítulo 4 (transferencias): cambios en política municipal

Para CADA variación importante:
- Explica por qué cambió
- Cuantifica impacto (euros/porcentaje)
- Sugiere implicaciones de presupuesto 2025

Datos a usar:
- archivo: presupuesto_2024.xlsx (adjunto)
- normativa: Decreto Presupuestario 2024 (adjunto)
```

**Ventaja:** La IA sabe EXACTAMENTE qué buscar, dónde, y por qué.

### Componentes Clave de TAREA

#### 1. Qué Producir (Sustantivo)
```text
Produce:
- Análisis de...
- Propuesta de...
- Evaluación de...
- Redacción de...
```

#### 2. Especificidad de Scope
```text
Específicamente enfocado en:
- Período: 2024 vs 2023 (últimos 12 meses)
- Departamentos: Administrativo + RRHH + Tesorería
- Métrica: Variación > 5% es "significativa"
```

#### 3. Datos de Entrada
```text
Considera:
- Documento X (adjunto)
- Normativa Y (requiere cumplimiento)
- Contexto Z (información previa)
```

#### 4. Acciones Esperadas
```text
Para cada hallazgo, incluye:
- Análisis de causa raíz
- Impacto en próximos meses
- Recomendación concreta
```

### Formato Mínimo de TAREA

```text
TAREA:
Produce [QUÉ: sustantivo] sobre [SCOPE: específico]
Considera [DATOS: fuentes] 
Para cada elemento, incluye [ACCIÓN: qué hacer].
```

**Tiempo:** 1-2 minutos para escribir.
**Impacto:** +25-35 puntos de calidad.

---

## Pilar 3: FORMATO & RESTRICCIONES (The Boundaries)

### Qué Es
Define CÓMO se presenta el resultado y QUÉ no puede hacer.

### Por Qué Funciona

**Psicología:** Las restricciones fuerzan creatividad DENTRO de límites. Un poeta con métrica (soneto) es más creativo que sin límites.

**Técnicamente:** Restricciones reducen "espacio de búsqueda" de la IA, permitiendo mayor profundidad en lo que SÍ puede hacer.

### Componentes de FORMATO

#### 1. Estructura Visual
```text
Formato:
- Título + Resumen ejecutivo (1 párrafo)
- Tabla: [Columna A] | [Columna B] | [Columna C]
- 3-5 puntos clave (bullets)
- Recomendaciones en orden de prioridad
```

**Por qué:** La IA sabe exactamente qué "Shape" tiene el resultado.

#### 2. Extensión
```text
Extensión:
- Total: máx 2 páginas
- Sección de análisis: 1 página
- Recomendaciones: 1 página
```

**Por qué:** Fuerza síntesis, no divagación.

#### 3. Lenguaje
```text
Lenguaje:
- Tono: Profesional pero accesible
- Evita: Jerga técnica innecesaria, referencias externas
- Incluye: Explicación de términos = auditor entienda
```

**Por qué:** Calibra accesibilidad, asegura que se entienda.

#### 4. Ejemplos de Salida
```text
Ejemplo de tabla esperada:
| Departamento | 2023 | 2024 | Variación | Causa |
|---|---|---|---|---|
| RRHH | 45k | 52k | +15% | 2 nuevos puestos |
```

**Por qué:** La IA entiende formato esperado copiando ejemplo.

### Componentes de RESTRICCIONES

#### 1. Qué NO Hacer
```text
Restricciones:
- NO incluir información sensible (números de cuenta)
- NO hacer recomendaciones que impliquen cambio normativo
- NO comparar con municipios privados (diferencia legal)
```

**Por qué:** Evita que la IA genere respuestas "inútiles" o problemáticas.

#### 2. Límites de Scope
```text
Límites:
- Enfoque SOLO en eficiencia operacional
- NO analizar política municipal
- Asumir presupuesto TIC actual (no aumenta)
```

**Por qué:** Mantiene análisis dentro de dominio relevante.

#### 3. Normativa a Respetar
```text
Consideraciones legales:
- Cumplir Ley de Transparencia
- Respetar RGPD en menciones de personal
- Citar normativa presupuestaria si aplica
```

**Por qué:** Asegura que output es defendible legalmente.

### Formato Mínimo de RESTRICCIONES

```text
RESTRICCIONES:
- Extensión máx: [PÁGINAS]
- Lenguaje: [TONO]
- NO incluir: [COSAS PROHIBIDAS]
- Normativa a respetar: [LEYES]
```

**Tiempo:** 1-2 minutos para escribir.
**Impacto:** +15-25 puntos de calidad.

---

## Integración de los 3 Pilares (Template Completo)

```text
CONTEXTO:
Eres [EXPERTICIA]. Tu cliente es [PERFIL]. 
Objetivo: [QUÉ QUEREMOS LOGRAR].
Restricciones: [LÍMITES REALES].

TAREA:
Produce [QUÉ] sobre [SCOPE].
Considera [DATOS].
Para cada elemento, [ACCIÓN].

FORMATO:
- Estructura: [CÓMO SE VE]
- Extensión: [LÍMITE]
- Lenguaje: [TONO]

RESTRICCIONES:
- NO: [PROHIBIDO]
- Normativa: [LEYES]
```

**Tiempo total para escribir:** 3-4 minutos.
**Tiempo que ahorra:** 30-60 minutos de iteraciones.

---

## Cómo Funciona Internamente

### Cerebro de IA Sin Pilares
```
"Redacta un informe"
    ↓
¿Sobre qué? → Asumo "financiero"
¿Para quién? → Asumo "ejecutivos"
¿Cómo? → Asumo "formal"
    ↓
Resultado: Genérico, posiblemente mal
```

### Cerebro de IA Con Pilares
```
"Contexto: Director de 50k-municipio buscando eficiencia"
"Tarea: Analiza presupuesto 2024 vs 2023, enfocado en RRHH"
"Formato: Tabla + 3 recomendaciones, máx 2 páginas"
    ↓
Contexto calibra: Tono ejecutivo, audiencia experimentada
Tarea especifica: Enfoque RRHH, comparativa histórica
Formato restringe: Concisión, presentación tabla
    ↓
Resultado: Preciso, accionable, efectivo
```

---

## Solución Oculta: Checklist de Validación de Pilares

<details>
<summary>Haz clic para ver checklist</summary>

**CONTEXTO - ¿Incluye estos elementos?**
- [ ] Rol/Experticia clara
- [ ] Perfil de lector específico
- [ ] Objetivo comercial/administrativo
- [ ] Restricciones del contexto real

**TAREA - ¿Especifica estos elementos?**
- [ ] Qué producir (verbo + sustantivo)
- [ ] Scope específico (período, departamentos, métricas)
- [ ] Datos de entrada (fuentes, documentos)
- [ ] Acciones esperadas (qué hacer con hallazgos)

**FORMATO & RESTRICCIONES - ¿Define estos elementos?**
- [ ] Estructura visual (tabla, bullets, etc)
- [ ] Extensión máxima clara
- [ ] Tono/lenguaje
- [ ] Prohibiciones explícitas
- [ ] Normativa a respetar

**Si respondiste SÍ a 10-12 elementos:** Prompt Karpathy perfecto
**Si respondiste SÍ a 7-9 elementos:** Buen prompt, marginal de mejora
**Si respondiste SÍ a < 7 elementos:** Necesita trabajo

</details>

---

## Reto: Mejora Tu Prompt Actual

Elige una solicitud que hiciste recientemente a IA (o usa de ejemplo):

**Versión actual (probablemente débil):**
```text
[Tu solicitud típica]
```

**Ahora reformúlala** usando los 3 pilares:
```text
CONTEXTO: [...]
TAREA: [...]
FORMATO: [...]
RESTRICCIONES: [...]
```

**Compara:** ¿Cuántos elementos agregaste? ¿Cuál sientes que mejoró más?

---

## Por Qué Esto Revoluciona Administración

### Antes (Prompting Tradicional)
- Solicitud vaga
- Respuesta genérica
- 5 ajustes para hacerla útil
- Frustración

### Después (Método Karpathy)
- Solicitud precisa (3-4 min setup)
- Respuesta específica
- 0-1 ajuste máximo
- Satisfacción

**Conversión de costo:** 30 min de iteración = 3-4 min de setup.

---

## Qué Aprendimos

✅ **Contexto = calibración de la IA**

✅ **Tarea = especificidad radical**

✅ **Formato & Restricciones = creatividad dentro de límites**

✅ **Los 3 pilares = multiplicador de calidad**

✅ **Costo de setup: 3-4 minutos = Retorno: 30-60 minutos ahorrados**

---

## Siguiente Paso

En el próximo documento, veremos ejemplo simple paso a paso: redacción de memo administrativo.

**⏱️ Tiempo de lectura: 10 minutos**
**💡 Dificultad: Intermedio (conceptual + técnico)**
**🎯 Transformación: Cimiento para aplicaciones reales**
