# Diseñar una Gema para Análisis de Contratos

## Objetivo
Crear un asistente especializado que revise contratos del sector público español, detecte riesgos legales y financieros, y proporcione orientación sin necesidad de abogado para análisis iniciales.

## Qué vamos a aprender
- Qué debe incluir un "cerebro" especializado en contratos públicos
- Cómo estructurar restricciones para evitar recomendaciones legales peligrosas
- Qué normativa es crítica en análisis de contratos
- Cómo diseñar una Gema que genere confianza

## Ejemplo guiado

Elena trabaja en Contratación de un ayuntamiento de 40.000 habitantes. Recibe un contrato de servicios de limpieza de la empresa que ya trabaja con ellos. El contrato tiene 45 páginas. Elena tiene 3 horas para revisar antes de la Junta de Gobierno. No puede esperar al asesor legal (que tarda 2 semanas).

**Sin Gema:** Elena lee los 45 puntos, muchos incomprensibles, termina preguntando al abogado igual.

**Con Gema bien diseñada:** Elena pega el contrato y pregunta "¿Cuáles son los 5 riesgos principales?" En 5 minutos tiene una lista clara, sabe qué preguntar al asesor.

## Prompt explicado

Un prompt del sistema para una Gema de Contratos públicos debe:

1. **Definir rol** - Quién eres
2. **Especializar en contexto público** - Qué tipo de contratos
3. **Incluir normativa crítica** - Qué leyes aplican
4. **Establecer restricciones claras** - Qué NO recomendarás
5. **Definir tipos de análisis** - Qué puedes hacer

```text
Eres especialista en análisis de contratos de la administración pública española. Tu objetivo es revisar contratos, detectar riesgos, resumir términos y ayudar a personal administrativo a comprender qué están firmando antes de que lo revise un abogado.

TIPO DE CONTRATOS QUE ANALIZAS:
- Contratos de servicios (limpieza, seguridad, mantenimiento)
- Contratos de suministros (materiales, equipos)
- Contratos de consultorías y asesoramiento
- Contratos de obras (aunque estos requieren especial cuidado)
- Contratos de concesión y colaboración público-privada

NORMATIVA APLICABLE:
- Ley 9/2017 de Contratos del Sector Público (LCSP)
- Real Decreto 1098/2001 (Reglamentación técnica)
- Ley 40/2015 (Régimen Jurídico del Sector Público)
- RGPD (si el contrato maneja datos personales)
- Ley de Responsabilidad Civil de la Administración

TU MANERA DE ANALIZAR:
1. Resumes: Qué es, a quién se le paga, cuánto, cuánto tiempo dura
2. Detectas riesgos: Cláusulas no estándar, costes ocultos, plazos confusos
3. Comparas: Con lo que es normal en el sector público
4. Recomendaciones: Qué preguntar, qué cambiar, cuándo consultar abogado
5. Escala de riesgo: Bajo/Medio/Alto (con explicación)

RESTRICCIONES (IMPORTANTE):
- NUNCA recomendarás rescindir un contrato sin consultar a asesor legal
- NUNCA dirás "esto es ilegal" sin base muy clara
- Siempre señalas: "Consulta a tu asesor legal para decisión final"
- No eres abogado, eres asistente administrativo
- Si hay conflicto legal real, lo escalas

FORMATO DE RESPUESTA:
Para cada análisis incluye:
1. Resumen en 3 párrafos: qué es este contrato
2. Puntos clave: elementos principales
3. Riesgos identificados: por nivel (bajo/medio/alto)
4. Comparación: cómo se compara con estándares
5. Próximos pasos: qué preguntar, a quién, cuándo escalar
6. Confianza de análisis: (alta/media/baja) - según lo claro que esté el contrato
```

## Variantes según tu contexto

Personaliza tu Gema según tu administración:

| Contexto | Énfasis | Normativa extra |
|---|---|---|
| **Municipio pequeño (<20.000)** | Contratos de servicios básicos | Ley Básica Régimen Local (LBRL) |
| **Municipio medio (20-100.000)** | Mezcla de servicios y consultorías | Normativa ambiental (contratación sostenible) |
| **Municipio grande (>100.000)** | Contratos complejos, concesiones | Ley de Responsabilidad Civil, Contratación Verde |
| **Diputación Provincial** | Contratos de transferencia, obras | Ley de Haciendas Locales |
| **Entidad pública (hospital, universidad)** | Servicios especializados | Normativa específica del sector |

## Ejercicio

**Tu misión: Diseña tu Gema de Contratos**

Responde estas preguntas:

1. ¿Qué tipos de contratos revisas más frecuentemente?
2. ¿Cuál es el riesgo más grande que has visto (pérdida de dinero, problemas legales)?
3. ¿Hay contratistas que trabajen regularmente contigo?
4. ¿Qué normativa es crítica en tu contexto?
5. ¿Qué 3 preguntas harías más frecuentemente a una Gema de Contratos?

Con esas respuestas, escribe tu propio prompt del sistema.

**Pistas:**
- ¿Qué contrato causa más dolor de cabeza en tu área?
- ¿Quién es tu "cliente" para esta Gema (tú, tu equipo, tu jefe)?
- ¿Hay cambios legales recientes que debería conocer tu Gema?

## Solución orientativa

<details>
  <summary>¿Quieres ver un ejemplo de Gema personalizada?</summary>

**Mi Gema de Contratos: Ayuntamiento de 35.000 habitantes**

**Tipos de contratos que reviso:**
1. Servicios de limpieza (anual)
2. Servicios de seguridad (anual)
3. Mantenimiento de infraestructuras (variable)
4. Consultorías puntuales
5. Gestión de servicios (basuras, agua)

**Riesgo más grande:**
Contratos de larga duración donde la cláusula de revisión de precios es confusa, y nos queda un contrato 5 años sin poder ajustar por inflación.

**Contratistas regularmente:**
- 3 empresas de servicios locales
- 2-3 empresas de consultorías que varían
- 1 empresa de mantenimiento

**Normativa crítica:**
- LCSP (obviamente)
- Responsabilidad civil (porque si algo falla, nos demandan)
- Sostenibilidad (nuevos requisitos de contratación verde)
- RGPD (muchos servicios manejan datos de ciudadanos)

**Mi prompt del sistema:**

```text
Eres especialista en análisis de contratos para un ayuntamiento español de 35.000 habitantes. Revisas contratos de servicios (limpieza, seguridad, mantenimiento) y asesorías.

Tu objetivo: En 10 minutos, decirle a un administrativo qué es el contrato, cuáles son los riesgos, y qué preguntas hacer antes de firmarlo.

ENFOQUE ESPECIAL:
- Cláusulas de revisión de precios (muchas son confusas)
- Responsabilidad civil (¿quién se queda sin cobertura?)
- Datos personales (RGPD)
- Plazo de vigencia (¿es renovable? ¿a quién le favorece?)
- Multas y penalizaciones (¿son proporcionales?)

SIEMPRE señala si necesita revisión de abogado (especialmente contratos >100.000€ o con cláusulas inusuales).
```

</details>

## Reto avanzado

**Nivel 1:** Toma tu Gema de Contratos y úsala con un contrato real de tu área

**Nivel 2:** Crea dos versiones de tu Gema (una para el jefe/a, otra para tu equipo administrativo) y nota las diferencias

**Nivel 3:** Diseña una Gema que compare tres contratos iguales de diferentes periodos y detecte cambios normales vs. peligrosos

## Qué hemos aprendido

✓ Una Gema de Contratos es diferente a una de Normativa (específica vs. general)  
✓ El contexto (tamaño de administración) cambia lo que necesitas  
✓ Las restricciones son tan importantes como las funciones  
✓ Un buen análisis de contrato empieza por entender el resumen, no los detalles  
✓ La escala de riesgos (bajo/medio/alto) es más útil que listas largas  

**Próximo paso:** Veremos prompts específicos para hacer preguntas poderosas a esta Gema.
