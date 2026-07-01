# Prompts Efectivos para Análisis de Subvenciones

## Objetivo
Dominar técnicas para extraer información crítica de convocatorias de subvenciones, verificar elegibilidad y diseñar estrategias de solicitud ganadoras.

## Qué vamos a aprender
- Estructura de prompts para análisis de convocatorias
- Cómo extraer requisitos de bases complejas
- Técnicas para identificar criterios de valoración ocultos
- Cómo calcular viabilidad de una solicitud
- Cuándo escalar a asesores externos

## Ejemplo guiado

Javier recibe una convocatoria de la Diputación: "Programa de Digitalización Local 2025". 42 páginas de bases. Presupuesto disponible: 1 millón. Su pregunta inicial es: "¿Podemos presentar?"

**Pregunta vaga:** "¿Vale la pena esta subvención?"  
**Respuesta:** Información muy general, no activa​ble

**Pregunta efectiva:** "¿Qué tiene que tener mi solicitud para no ser rechazada administrativamente? Dame checklist."  
**Respuesta:** Lista clara, sabe exactamente qué preparar

## Prompts explicados con ejemplos

### Prompt 1: Elegibilidad Rápida

Cuando necesitas saber en 5 minutos si tu administración puede solicitar.

```text
Analiza estas bases de convocatoria:

[PEGA LAS BASES AQUÍ]

Dime SOLO:
1. ¿Quién puede solicitar? (tipo de entidad, territorio, tamaño)
2. ¿Nosotros podemos? SÍ / NO / DEPENDE DE...
3. Si hay requisitos previos (acreditaciones, registros) que necesitamos
4. El plazo en el que estamos (si queda tiempo)
5. Si hay exclusiones automáticas para nosotros

Formato: Sí/No/Depende para cada punto, máximo una línea de explicación.
```

**Ejemplo real:**
```text
Analiza estas bases de "Ayudas para Modernización de Servicios Administrativos":

[PEGAMOS 30 PÁGS DE BASES]

Dime SOLO:
1. ¿Qué tipo de administración local puede solicitar?
2. ¿Un ayuntamiento de 15.000 habitantes puede?
3. ¿Necesitamos estar en algún registro especial?
4. ¿Cuánto tiempo queda para presentar?
5. ¿Hay algo que NO podamos hacer por ley?

Responde directo, sin rodeos.
```

### Prompt 2: Checklist de Documentación

Para asegurarte de que no te falta nada en la solicitud.

```text
¿Qué documentos necesitamos presentar?

[PEGA LAS BASES]

Dame una tabla con:
- Documento requerido
- Obligatorio sí/no
- Dónde se especifica en las bases (número de apartado)
- Modelo disponible (sí/no)
- Dónde conseguirlo
- Plazo de validez (si aplica)

Si falta documentación de terceros (asesor, notario), avísame.
```

**Ejemplo real:**
```text
¿Qué documentos necesitamos para esta solicitud de digitalización?

[PEGAMOS CONVOCATORIA COMPLETA]

Dame una tabla con:
- Documento
- Obligatorio
- Apartado en bases donde aparece
- Modelo disponible
- Plazo de validez

Extra: ¿Necesitamos certificado de no deuda?
```

### Prompt 3: Criterios de Valoración

El prompt donde la Gema más te ayuda: entender cómo ganar puntos.

```text
¿Cómo se puntúa esta solicitud?

[PEGA BASES, ESPECIALMENTE APARTADO DE CRITERIOS]

Para cada criterio de valoración:
1. Qué se valorar exactamente
2. Puntuación máxima
3. Cómo se interpreta (ej: "innovador" ¿significa qué?)
4. Dónde he visto que ganan puntos otros
5. ¿Hay ejemplos de proyectos ganadores anteriores?
6. ¿Debilidad nuestra en este criterio?

Luego: ¿En cuál debemos enfocarnos para ganar?
```

**Ejemplo real:**
```text
¿Cómo se puntúa el Programa de Inclusión Digital?

[PEGAMOS CONVOCATORIA]

Para cada criterio de valoración (supongamos que hay sostenibilidad, impacto social, innovación):
1. Qué significa exactamente
2. Puntos máximos
3. Ejemplos de proyectos que ganaron alto en esto
4. Dónde flojea nuestro ayuntamiento

Contexto: Somos un municipio rural de 8.000 habitantes, no somos digitales pero sí comprometidos.
```

### Prompt 4: Incompatibilidades y Restricciones

El prompt que evita disgustos después.

```text
¿Hay restricciones que no vea?

[PEGA BASES]

Busca y explícame:
1. Restricciones territoriales (qué zonas sí/no)
2. Incompatibilidades con otras ayudas
3. Restricciones de personal (¿qué tipo de recurso humano?)
4. Restricciones de gasto (qué no se puede gastar)
5. Restricciones de subcontratación
6. Restricciones temporales (ejecución máxima/mínima)
7. Cambios de objeto permitidos (¿podemos cambiar el proyecto después?)

Si veo riesgo: avísame "NIVEL ALTO" o similar.
```

**Ejemplo real:**
```text
¿Hay restricciones o trampa que me pierda?

[PEGAMOS BASES COMPLETAS]

Busca especialmente:
1. ¿Hay zonas territoriales excluidas?
2. ¿Si recibimos otra ayuda europea, esto se anula?
3. ¿El personal tiene que ser nuevo o puede ser el actual?
4. ¿Qué tipo de gastos son "NO elegibles"?
5. ¿Cuál es el plazo máximo para ejecutar?
6. Si cambia la política del gobierno, ¿se puede cancelar?

Marca como CRÍTICO si es importante para nosotros.
```

### Prompt 5: Presupuesto Realista

Para saber cuánto pedir sin arriesgar.

```text
¿Cuál es el presupuesto realista?

[PEGA BASES + DESCRIBE TU PROYECTO]

Dime:
1. Presupuesto mínimo y máximo permitido
2. Mi presupuesto estimado (con margen de seguridad +10%)
3. ¿Hay cofinanciación requerida? ¿Cuánta?
4. ¿Hay gastos que todos subestiman?
5. ¿Hay gastos extras por auditoría, control, intermediarios?
6. Presupuesto recomendado (que tenga probabilidad de ser aprobado)

Contexto: Proyecto de modernización de oficina municipal.
```

## Variantes según necesidad

| Necesidad | Añade al prompt |
|---|---|
| **Es muy urgente** | "Responde en máximo 3 párrafos" |
| **Primera vez que presentas** | "¿Cuál es el error más común que ve?" |
| **Hay dinero europeo** | "¿Hay normativa europea que afecte?" |
| **Plazo muy corto** | "¿Mínimo que necesito para tener oportunidad?" |
| **Tu sector es nuevo** | "¿Hay ejemplos previos similares?" |
| **Hay muchas restricciones** | "Resalta solo lo CRÍTICO para nosotros" |

## Ejercicio

**Tu misión: Crea 3 prompts para tu trabajo**

1. **Prompt de elegibilidad rápida:** Para cualquier convocatoria que recibas
2. **Prompt de documentación:** Adaptado a tu administración
3. **Prompt de criterios:** Enfocado en dónde usualmente pierdes puntos

Escribe los 3 prompts ahora. Si tienes una convocatoria disponible, pruébalos.

**Pistas:**
- Sé tan específico como puedas sobre tu contexto
- Include el tipo de administración
- Señala lo que más te preocupa (presupuesto, documentación, ejecución)

## Solución orientativa

<details>
  <summary>¿Quieres ver ejemplos completos?</summary>

**Ejemplo 1 - Elegibilidad rápida para ayuntamiento:**

```text
Analiza estas bases de "Municipios Inteligentes 2025":

[PEGAMOS CONVOCATORIA]

Dime SOLO (responde sí/no/depende):
1. ¿Qué tipo de municipios pueden solicitar?
2. ¿Un ayuntamiento de 12.000 hab​itantes puede?
3. ¿Necesitamos certificación ISO o algo?
4. ¿Todavía hay plazo o pasó?
5. ¿Hay algo que legalmente NO podamos hacer?
6. ¿Es nuestro sector el objetivo de esta ayuda?

Contexto: Municipio rural, sin experiencia previa en estas ayudas.
```

**Ejemplo 2 - Documentación para Diputación:**

```text
¿Qué necesitamos presentar exactamente?

[PEGAMOS BASES DE DIPUTACIÓN]

Dame una tabla:
| Documento | Obligatorio | Dónde aparece | Modelo | Dónde conseguirlo |
|-----------|-----------|---|---|---|

Extra importante:
- ¿Necesitamos acta de Pleno aprobando?
- ¿Certificado de no deuda con la Diputación?
- ¿Aval bancario? ¿De cuánto mínimo?
- ¿Todo en PDF o hay formulario online?
```

**Ejemplo 3 - Criterios para ganar:**

```text
¿Cómo ganamos en esta convocatoria?

[PEGAMOS "PLAN DE EMPLEO LOCAL"]

Para cada criterio de valoración:
1. Qué se valora
2. Puntos máximos
3. Ejemplos previos ganadores
4. Dónde somos fuertes (nuestro ayuntamiento)
5. Dónde somos débiles

Contexto: Ayuntamiento de 25.000 hab, con desempleo juvenil alto, pero sector industrial pequeño.

Conclusión: ¿En qué criterio debería enfocarme para maximizar puntos?
```

</details>

## Reto avanzado

**Nivel 1:** Toma una convocatoria real, crea 3 prompts y prúebalos con tu Gema

**Nivel 2:** Crea un "prompt maestro" que combina elegibilidad + documentación + criterios en una sola pregunta

**Nivel 3:** Diseña un prompt que compara 2 convocatorias similares y recomienda cuál tiene más probabilidad ganancia

## Qué hemos aprendido

✓ Cada tipo de pregunta extrae información diferente de bases complejas  
✓ Elegibilidad no es todo: documentación y presupuesto importan más  
✓ Criterios de valoración son donde se gana o pierde  
✓ Incompatibilidades son una trampa oculta  
✓ Un presupuesto realista tiene más probabilidad que uno optimista  
✓ Prompts específicos a tu contexto dan resultados mejores  

**Próximo paso:** Aplicaremos todo esto a un caso práctico real.
