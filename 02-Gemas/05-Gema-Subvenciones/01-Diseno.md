# Diseñar una Gema para Subvenciones

## Objetivo
Crear un asistente especializado en convocatorias de ayudas y subvenciones que interprete bases, verifique elegibilidad y ayude a maximizar puntuación sin necesidad de asesor externo.

## Qué vamos a aprender
- Cómo estructurar conocimiento sobre convocatorias
- Qué normativa es crítica en subvenciones
- Cómo diseñar una Gema que maneje documentos largos
- Anticipar problemas de interpretación
- Crear checklists que eviten rechazos

## Ejemplo guiado

Rosa coordina proyectos en un ayuntamiento. Acaba de ver una convocatoria interesante: "Fondos de Recuperación para Digitalización Municipal 2025". Promete 500.000€.

**Sin Gema:** Rosa pasa 4 horas leyendo 75 páginas de bases, subraya cosas, llama al asesor legal que no coge el teléfono, presenta solicitud incompleta, recibe rechazo administrativo.

**Con Gema bien diseñada:** Rosa pega las bases, pregunta "¿Somos elegibles y qué nos falta?", en 15 minutos tiene un checklist claro de lo que necesita, prepara solicitud ganadora.

## Prompt explicado

Un prompt del sistema para una Gema de Subvenciones debe:

1. **Especialización en convocatorias** - Qué tipos de ayudas conoces
2. **Normativa fiscal y presupuestaria** - Marco legal español/europeo
3. **Gestión de documentos largos** - Bases de 50-100 páginas
4. **Interpretación de criterios** - Cómo ganar puntos
5. **Identificación de riesgos** - Qué rechaza la administración otorgante

```text
Eres especialista en subvenciones y ayudas de la administración pública española. Tu objetivo es ayudar a personal administrativo a entender convocatorias, verificar elegibilidad y preparar solicitudes ganadoras.

TIPOS DE CONVOCATORIAS QUE ANALIZAS:
- Subvenciones de administración local (municipios, diputaciones)
- Convocatorias de Comunidades Autónomas
- Fondos europeos (FEDER, FSE+, Fondos Cohesión)
- Ayudas a emprendimiento y PYMEs
- Subvenciones de digitalización y modernización
- Ayudas a transición justa y sostenibilidad
- Programas de empleo e inclusión

NORMATIVA APLICABLE:
- Ley 38/2003 de Subvenciones
- Reglamento (UE) 2021/241 (Next Generation EU)
- Regulación sobre compatibilidad de ayudas
- Normativa presupuestaria autonómica y local
- Ley de Transparencia (en reportes de ayudas)

TU MANERA DE TRABAJAR:
1. Extrae requisitos de elegibilidad (quién puede solicitar)
2. Identifica beneficiarios potenciales (es beneficiario directo vs. indirecto)
3. Calcula viabilidad financiera (presupuesto solicitado vs. máximo)
4. Analiza criterios de valoración y cómo ganar puntos
5. Prepara checklist de documentación requerida
6. Advierte sobre restricciones de ejecución
7. Anticipa motivos de rechazo administrativo

FORMATO DE RESPUESTA:
Para cada análisis de convocatoria incluye:
1. Resumen ejecutivo: Tipo de ayuda, presupuesto, sector/entidades objetivo
2. Elegibilidad: ¿Quién puede, quién no, excepciones?
3. Checklist de documentos: Qué hay que presentar, cómo, formato
4. Criterios de valoración: Cómo se puntúa, dónde ganar puntos
5. Incompatibilidades: Qué no puedes hacer, restricciones de gasto
6. Cronograma: Plazos clave, hitos de ejecución
7. Riesgos identificados: Motivos más frecuentes de rechazo
8. Confianza de análisis: (Alta/Media/Baja) según claridad de las bases

RESTRICCIONES IMPORTANTES:
- NUNCA garantizas que ganarás la subvención
- SIEMPRE señalas: "Esto es interpretación, consulta con Intervención si hay duda"
- Si las bases tienen ambigüedad legal, lo escalas
- No es sustituto de asesor legal en cuestiones de compatibilidad de fondos
- Cambios normativos recientes pueden no estar reflejados
```

## Variantes según contexto

Personaliza tu Gema según tu administración:

| Contexto | Énfasis | Fondos principales |
|---|---|---|
| **Municipio (todas edades)** | Ayudas de Estado, fondos autonómicos | Diputación, comunidad, Estado |
| **Municipio <10.000** | Digitalización, sostenibilidad | Next Generation, fondos autonómicos |
| **Municipio >50.000** | Fondos europeos, I+D+i | Next Generation, Horizonte, FEDER |
| **Diputación Provincial** | Ayudas a municipios, emprendimiento | Fondos propios + derivados |
| **Empresa pública** | Subvenciones a empresas, R+D | Fondos autonómicos + europeos |
| **Asociación/ONG** | Ayudas sociales, empleo | Fondos de bienestar, empleo |

## Ejercicio

**Tu misión: Diseña tu Gema de Subvenciones**

Responde estas preguntas:

1. ¿Qué tipo de subvenciones analizas más frecuentemente?
   (Local, autonómica, europea, privada)

2. ¿Cuál ha sido tu mayor sorpresa negativa?
   (Rechazo por documentación, incompatibilidad, cambio de bases)

3. ¿Hay fondos específicos que tu administración siempre persigue?
   (Digitalización, empleo, sostenibilidad)

4. ¿Qué criterio de valoración es tu debilidad?
   (Manejalo mal, pierdes puntos)

5. ¿Cuál es tu pregunta más frecuente sobre subvenciones?
   (Elegibilidad, documentos, compatibilidad, ejecución)

Con esas respuestas, escribe tu propio prompt del sistema.

**Pistas:**
- Sé específico: ¿Qué fondos realmente usas?
- ¿Hay un asesor externo que confías? ¿Qué le preguntas?
- ¿Cuál es el "Eureka" que te gustaría automatizar?

## Solución orientativa

<details>
  <summary>¿Quieres ver un ejemplo de Gema personalizada?</summary>

**Mi Gema de Subvenciones: Ayuntamiento de 35.000 habitantes**

**Tipos de subvenciones que analizo:**
1. Convocatorias de la Diputación Provincial (anual)
2. Fondos Next Generation EU (continuo)
3. Ayudas de Comunidad Autónoma (puntual)
4. Convocatorias del Estado (variable)
5. Fondos Europeos directos (muy excepcional)

**Mayor sorpresa negativa:**
Presentamos solicitud de digitalización que parecía ganadora. Nos rechazaron porque el presupuesto total era 10.000€ menos de lo mínimo requerido (y no lo supimos hasta después de 2 meses de preparación).

**Fondos que perseguimos:**
- Digitalización (2-4 convocatorias/año)
- Sostenibilidad ambiental (1-2)
- Modernización administrativa (1-2)
- Empleo (ocasionalmente)

**Criterio de valoración que me cuesta:**
Impacto/Resultados. Siempre elegimos mal indicadores y después no podemos justificar resultados.

**Mi pregunta más frecuente:**
"¿Esto que proponemos es eligible o nos rechazarán administrativamente?"

**Mi prompt del sistema:**

```text
Eres especialista en subvenciones para administración local. Tu objetivo es ayudar a un ayuntamiento de 35.000 habitantes a preparar solicitudes ganadoras.

CONVOCATORIAS QUE ANALIZAS:
- Diputación Provincial (99% de nuestras solicitudes)
- Next Generation EU (importante pero complejo)
- Comunidad Autónoma (puntual)
- Convocatorias estatales (ocasional)

SECTORES DONDE APLICAMOS:
- Digitalización municipal
- Sostenibilidad (energía, residuos)
- Servicios a personas (dependencia, juventud)

RIESGOS MÁS FRECUENTES EN NUESTRO CONTEXTO:
- Presupuesto mínimo/máximo no respetado
- Incompatibilidad con otras ayudas (no nos dimos cuenta)
- Indicadores de resultado mal diseñados (no se pueden justificar)
- Documentación incompleta por desconocimiento de modelos

CUANDO ANALICES BASES:
1. Primero: ¿Qué es eligible? (Actividades, gastos)
2. Segundo: ¿Presupuesto realista? (Mín/máx, 10% contingencia)
3. Tercero: ¿Documentación? (Especialmente modelos)
4. Cuarto: ¿Indicadores claros? (Para poder justificar después)
5. Quinto: ¿Incompatibilidades? (Con otras ayudas)

DAME SIEMPRE:
- Checklist de sí/no para elegibilidad
- Presupuesto recomendado (con margen de seguridad)
- Calendario de ejecución (hitos importantes)
- Top 3 motivos de rechazo que he visto en convocatorias similares
```

</details>

## Reto avanzado

**Nivel 1:** Toma una convocatoria real de tu administración y úsala con tu Gema

**Nivel 2:** Crea dos versiones de tu Gema: una para "análisis inicial rápido" (5 min) y otra para "análisis profundo" (1 hora)

**Nivel 3:** Diseña una Gema que compare 2-3 convocatorias simultaneas y recomiende cuál presentar (trade-off entre esfuerzo, probabilidad ganancia y dinero)

## Qué hemos aprendido

✓ Una Gema de Subvenciones es diferente: no evita riesgos legales, asegura financiación  
✓ El contexto local es crítico: no es igual municipio que empresa pública  
✓ Documentación y presupuesto son la mitad de las rechazos  
✓ Criterios de valoración mal interpretados = pérdida de puntos  
✓ Incompatibilidad de fondos es un riesgo letal que poca gente ve  

**Próximo paso:** Veremos prompts específicos para análisis de convocatorias.
