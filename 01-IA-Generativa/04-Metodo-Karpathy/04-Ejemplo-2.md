# Ejemplo 2: Analiza Normativa Compleja

## Objetivo
Ver cómo el método Karpathy se aplica a tareas de mayor complejidad: interpretación de normativa y extracción de obligaciones.

## Qué Aprenderemos
- Cómo estructurar análisis normativo con precisión
- Diferencia entre interpretación vaga vs estructurada
- Cómo verificar que IA cumple toda normativa sin omisiones
- Template para interpretación de cualquier regulación

---

## Contexto: La Tarea Real

**Escenario:** Has recibido normativa nueva: "Decreto 3/2024 sobre Contratación Pública Sostenible". Es compleja, con 45 artículos. Necesitas:

1. ¿Qué cambios aplican a tu municipio?
2. ¿Qué nuevas obligaciones tenemos?
3. ¿Cuáles son plazos y procedimientos?
4. ¿Qué impacto tiene en contrataciones actuales?

**Desafío:** La normativa es técnica, tiene muchas referencias cruzadas, y errores de interpretación pueden ser costosos.

---

## VERSIÓN 1: Método Tradicional

### Tu Solicitud
```text
Resume el Decreto 3/2024 sobre contratación sostenible
```

### Respuesta Típica

```
RESUMEN DECRETO 3/2024

El decreto aborda contratación pública sostenible.

Puntos principales:
- Empresas contratistas deben cumplir criterios sostenibles
- Se incluyen consideraciones medioambientales
- Procedimientos deben incorporar sostenibilidad

Aplicación:
- Aplicable a contratos públicos
- Requiere cumplimiento normativo

Más información:
- Consulte documentos originales
```

### Problemas Identificados ❌

| Problema | Riesgo |
|----------|--------|
| NO especifica qué = "sostenible" | Ambigüedad legal, riesgo de recurso |
| NO detalla procedimiento nuevo | Incumplimiento sin saberlo |
| NO lista plazos | Pérdida de plazo = ilegalidad |
| NO identifica excepciones | Aplicación errónea |
| NO menciona documentación requerida | Expedientes incompletos |
| NO explica impacto presupuestario | Sorpresas en costos |

**Calificación:** 25/100 (Potencialmente peligroso)
**Riesgo legal:** CRÍTICO

---

## VERSIÓN 2: Método Karpathy

### Paso 1: Define Los 3 Pilares

#### CONTEXTO:
```text
Eres abogado especializado en contratación pública municipal.
Tu audiencia es directora de contratación de municipio de 50.000 
habitantes con:
- Experiencia: 10+ años en contratación pública
- Objetivo: Cumplir normativa SIN sorpresas legales
- Contexto: Municipio ha tenido 2 recursos ganados por 
  contratistas en últimos 3 años

Necesitas documentación que sea:
- Defensible ante auditoría
- Clara para explicar a contratistas
- Operacional (qué hacer paso a paso)
```

#### TAREA:
```text
Analiza Decreto 3/2024 sobre Contratación Sostenible.
Extrae:
1. OBLIGACIONES NUEVAS: Qué cambia vs procedimiento anterior
2. DEFINICIONES: Qué significa "sostenible" en este contexto
3. PROCEDIMIENTO: Paso a paso de contratación bajo este decreto
4. PLAZOS: Todas las fechas, períodos, límites aplicables
5. DOCUMENTACIÓN: Qué expediente debe incluir
6. EXCEPCIONES: Contratos donde NO aplica
7. PENALIDADES: Qué ocurre si no cumplimos
8. TRANSICIÓN: Qué aplica a contratos en curso

Considera:
- Decreto completo (adjunto)
- Normativa anterior (Ley 9/2017)
- Jurisprudencia si existe
```

#### FORMATO:
```text
Estructura:
- Tabla 1: Obligaciones nuevas (Artículo | Obligación | Plazos | Responsable)
- Tabla 2: Definiciones clave (Término | Significado | Excepciones)
- Sección: Procedimiento paso a paso (5-7 pasos numerados)
- Tabla 3: Plazos críticos (Evento | Plazo | Consecuencia incumplimiento)
- Checklist: Documentación a incluir en expediente
- Sección: Contratos en curso (¿se aplica o no?)

Tono:
- Técnico pero accesible
- Sin ambigüedad legal
- Orientado a cumplimiento, no interpretación

Extensión: Máx 5 páginas
```

#### RESTRICCIONES:
```text
CRÍTICO - Verificar:
- Citas exactas del decreto (número artículo)
- Si hay jurisprudencia contradictoria, mencionarla
- NO asumir; si no está en decreto, decirlo explícitamente
- Marcar "DUDA LEGAL" si algo admite interpretación

NO incluir:
- Opinión sin fundamentar en decreto
- Recomendaciones no basadas en texto

SÍ incluir:
- Cada artículo aplicable citado
- Si normativa anterior prevalece en algún punto
- Recomendaciones de consulta legal si hay ambigüedad
```

### Paso 2: Solicitud Completa Karpathy

```text
CONTEXTO:
Eres abogado especializado en contratación pública municipal.
Tu audiencia es directora de contratación de municipio 50k 
habitantes, con 10+ años experiencia. Necesita cumplir normativa 
SIN sorpresas legales (municipio ha tenido 2 recursos en 3 años).
Documentación debe ser defensible ante auditoría y operacional.

TAREA:
Analiza Decreto 3/2024 sobre Contratación Sostenible.
Extrae con precisión:
1. OBLIGACIONES NUEVAS: Qué cambia vs procedimiento anterior
2. DEFINICIONES: Qué = "sostenible" en contexto decreto
3. PROCEDIMIENTO: Paso a paso de contratación bajo decreto
4. PLAZOS: Todas fechas, períodos, límites
5. DOCUMENTACIÓN: Qué expediente debe incluir
6. EXCEPCIONES: Contratos donde NO aplica
7. PENALIDADES: Consecuencias incumplimiento
8. TRANSICIÓN: Aplica a contratos en curso?

Considera: Decreto 3/2024 (adjunto), Ley 9/2017, jurisprudencia.

FORMATO:
- Tabla: Obligaciones nuevas (Artículo | Obligación | Plazo | Responsable)
- Tabla: Definiciones (Término | Significado | Excepciones)
- Sección: Procedimiento 5-7 pasos numerados
- Tabla: Plazos críticos (Evento | Plazo | Si incumples)
- Checklist: Documentación expediente
- Sección: Contratos en curso (¿aplica?)
- Tono: Técnico pero accesible, sin ambigüedad
- Máx: 5 páginas

RESTRICCIONES:
- CRÍTICO: Citas exactas (art., párrafo)
- Si hay jurisprudencia contradictoria, mencionarla
- NO asumir; si no está, decirlo
- Marcar "DUDA LEGAL" si hay interpretación múltiple
- CADA recomendación fundamentada en decreto
```

### Respuesta Karpathy (Extracto)

```
ANÁLISIS OPERACIONAL DECRETO 3/2024
Contratación Pública Sostenible
[Municipio], Fecha: [Hoy]

TABLA 1: OBLIGACIONES NUEVAS

| Artículo | Obligación Nueva | Plazo Aplicación | Responsable |
|----------|------------------|------------------|------------|
| Art. 5 | Incluir cláusulas sostenibilidad en todas convocatorias | 90 días (entrada vigor) | Dirección Contratación |
| Art. 8 | Verificar cumplimiento normativa ambiental contratista | ANTES firma contrato | Técnico responsable |
| Art. 12 | Reportar trimestralmente % contratos sostenibles | Cada trimestre | RRHH + Contratación |
| Art. 15 | Establecer criterios de selección por sostenibilidad | ANTES próxima convocatoria | Comisión evaluación |
| Art. 22 | Incluir clausuras de penalización por incumplimiento | En cláusulas contrato | Secretaría |

TABLA 2: DEFINICIONES CLAVE

| Término | Significado según Decreto | Excepciones |
|---------|---------------------------|-----------|
| "Contratación Sostenible" | Art. 2: "Contratación pública que integra criterios medioambientales, sociales y de gobernanza en proceso de selección" | Contratos menores < 5.000€ (Art. 4.2) |
| "Criterios Sostenibilidad" | Art. 3: Mínimo 3 de: eficiencia energética, residuos, responsabilidad social, cadena suministro ética | Contratos servicios básicos urgentes |
| "Verificación Cumplimiento" | Art. 8: Auditoría documental previa + 2 inspecciones durante ejecución | Contratos < 10.000€ (auditoría solo documental) |

PROCEDIMIENTO PASO A PASO

Nuevo proceso bajo Decreto 3/2024:

1. PREPARACIÓN (T-30 días antes convocatoria)
   - Dirección Contratación: Diseña cláusulas sostenibilidad
   - Técnico responsable: Define criterios específicos del servicio
   - Comisión evaluación: Establece puntuación sostenibilidad (mín 20% de puntuación)
   
2. CONVOCATORIA (T-0)
   - Publicar con cláusulas sostenibilidad incluidas
   - Explícitamente indicar % puntuación asignado a sostenibilidad
   - Requisito: Contratista debe adjuntar "Plan Sostenibilidad" (plantilla municipal)
   
3. EVALUACIÓN (T+15 días)
   - Técnico: Evalúa Plan Sostenibilidad (máx 20 puntos)
   - Comisión: Puntuación estándar (60 puntos) + sostenibilidad (20 puntos) + precio (20 puntos)
   - Acta: Documentar porqué cada contratista merece puntuación sostenibilidad
   
4. VERIFICACIÓN PRE-FIRMA (T+5 días post-resolución)
   - Dirección Legal: Verifica contratista cumple normativa ambiental
   - Técnico: Revisa Plan Sostenibilidad en detalle
   - Si "rojo": NO firmar hasta subsanación
   
5. FIRMA CONTRATO (T+10 días post-resolución)
   - Incluir: Cláusula 22 (penalización incumplimiento sostenibilidad)
   - Especificar: Qué indicadores se monitorizan (ej: residuos, eficiencia)
   - Firmar
   
6. EJECUCIÓN (Durante contrato)
   - Inspección 1: Mes 1 (verificar cumplimiento)
   - Inspección 2: Mes 50% contrato (control intermedio)
   - Reporte: Si incumplimiento, activar cláusula 22
   
7. CIERRE (Final contrato)
   - Tecnico: Evalúa desempeño sostenibilidad
   - Dirección: Recopila datos para reportaje trimestral

TABLA 3: PLAZOS CRÍTICOS

| Evento | Plazo Límite | Si Incumples | Nota |
|--------|--------------|-------------|------|
| Cláusulas sostenibilidad en convocatorias | 90 días entrada vigor (Art. 5.1) | Recurso contratista + anulación convocatoria | CRÍTICO |
| Verificación contratista pre-firma | ANTES firma (Art. 8.3) | Contrato potencialmente nulo | CRÍTICO |
| Inspección 1 durante ejecución | Mes 1 (Art. 14.1) | Penalización 5% contrato | Importante |
| Reporte trimestral | Último día cada trimestre (Art. 12.2) | Posible sanción autonómica | Importante |

CHECKLIST: DOCUMENTACIÓN EXPEDIENTE

Cada expediente de contratación DEBE incluir:

Fase Pre-Convocatoria:
- [ ] Cláusulas de sostenibilidad diseñadas (Dirección Contratación)
- [ ] Criterios sostenibilidad definidos (Técnico)
- [ ] Plantilla "Plan Sostenibilidad" para contratistas (adjunta en convocatoria)

Fase Convocatoria:
- [ ] Convocatoria publicada CON cláusulas sostenibilidad (extracto en acta)
- [ ] Clarificación % puntuación sostenibilidad (mín 20%, en acta)

Fase Evaluación:
- [ ] Acta evaluación: Puntuación sostenibilidad justificada por contratista
- [ ] Plan Sostenibilidad recibido de cada contratista (archivado)

Fase Pre-Firma:
- [ ] Verificación legal: Contratista cumple normativa ambiental (informe Dirección Legal)
- [ ] Inspección técnica Plan Sostenibilidad (informe Técnico)
- [ ] Aprobación para proceder a firma (autorización Dirección)

Fase Ejecución:
- [ ] Cláusula 22 (penalización) en contrato FIRMADO
- [ ] Indicadores sostenibilidad especificados en contrato (anexo técnico)
- [ ] Inspección 1 (mes 1): Informe cumplimiento
- [ ] Inspección 2 (mes 50%): Informe cumplimiento
- [ ] Reportes de incidencias si las hay (correos/actas)

¿APLICA A CONTRATOS EN CURSO?

Sí, PARCIALMENTE (Art. 20 "Disposición Transitoria"):
- Contratos <90 días: NO se aplica (pueden terminarse sin cambios)
- Contratos 90-365 días: Aplica SOLO cláusula 22 (penalización) si se renueva
- Contratos >365 días: Aplica criterios sostenibilidad a próxima renovación

ACCIONES INMEDIATAS PARA TU MUNICIPIO:

1. Semana 1: Comunicar cambio a todas áreas contratantes
2. Semana 2: Dirección diseña cláusulas + criterios
3. Semana 3: Capacita Comisión Evaluación
4. Semana 4: Primera convocatoria bajo Decreto 3/2024
5. Seguimiento trimestral: Reporte sostenibilidad

DUDAS LEGALES IDENTIFICADAS:

- Art. 8.3: "Verificación ANTES firma" - Si es auditoría física, 
  plazo podría extenderse (RECOMENDACIÓN: Consultar Asesoría)
  
- Art. 22: Penalización "máximo 5%" - Qué pasa si contrato ya 
  finalizó? (RECOMENDACIÓN: Incluir en nuevo contrato)

```

---

## Impacto del Método Karpathy en Este Análisis

### Beneficio 1: Completitud
**Sin Karpathy:** Resumen genérico, pierdes obligaciones
**Con Karpathy:** Cada artículo extraído, documentado

### Beneficio 2: Operacionalidad
**Sin Karpathy:** "Aplica sostenibilidad" ← ¿Cómo?
**Con Karpathy:** Paso a paso, quién, cuándo, qué documentar

### Beneficio 3: Defensibilidad Legal
**Sin Karpathy:** Expediente incompleto, riesgo de recurso
**Con Karpathy:** Expediente verificable, defensible

### Beneficio 4: Cumplimiento
**Sin Karpathy:** Riesgo de incumplimiento por desconocimiento
**Con Karpathy:** Checklist asegura cumplimiento

---

## Solución Oculta: Template para Análisis Normativo

<details>
<summary>Haz clic para copiar template</summary>

```text
CONTEXTO:
Eres [ESPECIALISTA: abogado, consultor, etc].
Tu audiencia es [PERFIL: experiencia, objetivo].
Necesitas documentación que sea: [REQUISITOS: defensible, operacional, etc].

TAREA:
Analiza [NORMATIVA: decreto, ley, etc].
Extrae:
1. OBLIGACIONES NUEVAS: Qué cambia
2. DEFINICIONES: Clave términos
3. PROCEDIMIENTO: Paso a paso
4. PLAZOS: Fechas, períodos
5. DOCUMENTACIÓN: Qué expediente incluye
6. EXCEPCIONES: No aplica a...
7. PENALIDADES: Si incumples...
8. TRANSICIÓN: Contracts en curso?

Considera: [Normativa completa], [Normativa anterior], [Jurisprudencia].

FORMATO:
- Tabla: Obligaciones (Artículo | Obligación | Plazo | Responsable)
- Tabla: Definiciones (Término | Significado | Excepciones)
- Sección: Procedimiento numerado
- Tabla: Plazos críticos
- Checklist: Documentación
- Sección: Contratos en curso
- Tono: Técnico, sin ambigüedad
- Máx páginas: [NÚMERO]

RESTRICCIONES:
- Citas exactas (artículo, párrafo)
- Si hay interpretación múltiple, marcar "DUDA LEGAL"
- CADA recomendación fundamentada
- Si NO está en texto, decirlo
- Jurisprudencia si existe
```

</details>

---

## Reto: Aplica a Normativa Real

¿Hay normativa reciente en tu municipio que necesites analizar?
- Regulación nueva
- Cambio en procedimiento administrativo
- Normativa autonómica o estatal

**Tu reto:**
1. Obtén el documento (completo)
2. Reformúlalo usando template Karpathy
3. Solicítalo a IA
4. Documentalo: ¿Qué hizo diferencia?

---

## Qué Aprendimos

✅ **Karpathy se aplica a análisis complejos (no solo tareas simples)**

✅ **Diferencia en completitud: 25/100 → 90/100**

✅ **Diferencia en riesgo legal: CRÍTICO → CONTROLADO**

✅ **Documentación defensible requiere estructura + precisión**

✅ **Template reutilizable para cualquier normativa**

---

## Siguiente Paso

En el próximo documento, TÚ practicarás con caso real guiado: Redacción de convocatoria de subvención.

**⏱️ Tiempo de lectura: 14 minutos**
**💡 Dificultad: Avanzado (análisis normativo)**
**🎯 Impacto: 90% mejora en calidad + defensibilidad legal**
