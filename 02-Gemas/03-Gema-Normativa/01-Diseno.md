# Diseñar una Gema para Analizar Normativa

## Objetivo
Crear un asistente especializado en normativas españolas que explique, interprete y compare leyes, decretos y circulares de forma clara y accesible para personal administrativo sin conocimiento jurídico previo.

## Qué vamos a aprender
En esta lección descubrirás cómo:
- Definir el contexto especializado para normativa
- Estructurar un prompt del sistema que evite errores legales
- Diseñar una Gema que simplifique leyes complejas
- Anticipar preguntas frecuentes sobre normativas

## Ejemplo guiado

Imaginemos que María trabaja en el Registro Civil de un municipio. Cada día recibe consultas sobre la **Ley de Modernización de la Justicia del Siglo XXI** (LMRSP). Las leyes son densas, con muchos artículos y disposiciones finales. María necesita un asistente que le ayude a encontrar rápidamente qué dice la ley sobre un tema específico.

Una Gema bien diseñada para normativa haría que María pudiera preguntar cosas como:
- "¿Qué dice la LMRSP sobre autenticación electrónica?"
- "¿Puedo aplicar esto en mi oficina?"
- "¿Cómo afecta el RGPD a este procedimiento?"

## Prompt explicado

Un prompt del sistema para una Gema Normativa debe incluir:

1. **Rol especializado** - Quién eres y qué sabes
2. **Contexto legal** - Qué normativas conoces
3. **Restricciones** - Qué NO debes hacer
4. **Formato de respuesta** - Cómo estructurar explicaciones
5. **Referencias** - Cómo citar correctamente

```text
Eres un especialista en normativa de la administración pública española. Tu misión es explicar leyes, decretos y circulares de forma clara para personas sin formación jurídica.

NORMATIVAS PRINCIPALES QUE CONOCES:
- Ley 1/2000 (Ley de Enjuiciamiento Civil)
- Ley 39/2015 (Procedimiento Administrativo Común)
- Ley 40/2015 (Régimen Jurídico del Sector Público)
- Reglamento General de Protección de Datos (RGPD)
- Ley 19/2013 (Régimen Jurídico de las Bases de Datos)
- Ley 19/2013 (Transparencia, Acceso a la Información Pública)

TU MANERA DE TRABAJAR:
1. Explica siempre en lenguaje administrativo simple
2. Cita el artículo exacto de la ley (Ej: "Art. 22, apartado 3")
3. Incluye un ejemplo práctico si es posible
4. Señala si hay cambios recientes o cómo se interpreta
5. NUNCA des asesoramiento legal definitivo (di "consulta con tu asesor legal")

FORMATO DE RESPUESTA:
- Párrafo introductorio: qué dice la norma
- Desglose: los puntos clave
- Ejemplo: caso real de administración pública
- Implicaciones: qué significa para tu trabajo
- Fuente: referencia exacta de la ley
```

## Variantes

Según tu contexto administrativo, puedes especializar más la Gema:

| Especialización | Ejemplo | Focus |
|---|---|---|
| **Protección de Datos** | RGPD + LOPDGDD | Privacidad, consentimiento, derechos |
| **Transparencia** | Ley 19/2013 | Acceso a información, publicidad activa |
| **Contratación Pública** | LCSP | Procedimientos, anuncios, criterios |
| **Procedimiento Administrativo** | Ley 39/2015 | Plazos, recursos, notificaciones |
| **Personal Público** | RD 5/2015, Función Pública | Derechos, deberes, incompatibilidades |

## Ejercicio

**Tu misión: Diseña tu propia Gema Normativa**

1. Identifica 3 leyes que consultas regularmente en tu puesto
2. Escribe cuál es el rol más útil para tu Gema
3. Define 5 restricciones importantes (qué no debe hacer)
4. Propón 4 tipos de preguntas que tu Gema responderá

**Pistas:**
- ¿Qué normativas consultas más de una vez al mes?
- ¿Cuál es la razón más común de confusión en tu equipo?
- ¿Hay algún cambio legal reciente que todos necesitan entender?

## Solución orientativa

<details>
  <summary>¿Quieres ver un ejemplo de respuesta?</summary>

**Mi Gema Normativa: Personal Administrativo del Ayuntamiento**

1. **Leyes principales:**
   - Ley 39/2015 (Procedimiento Administrativo Común)
   - Ley 40/2015 (Régimen Jurídico)
   - RGPD + LOPDGDD

2. **Rol:** "Eres un especialista en procedimientos administrativos locales. Explicas cómo tramitar solicitudes, denuncias y recursos ante la administración municipal según la normativa española actual."

3. **Restricciones:**
   - No soy un abogado, no puedo asumir responsabilidad legal
   - No conozco cambios legales posteriores a 2025
   - No puedo interpretar sentencias judiciales
   - Consulta siempre con tu asesor legal en casos complejos

4. **Preguntas que responderé:**
   - "¿Cuál es el plazo para presentar un recurso administrativo?"
   - "¿Qué información debo pedir cuando me lo solicitan?"
   - "¿Cómo notificar una resolución correctamente?"
   - "¿Qué datos puedo guardar según RGPD?"

</details>

## Reto avanzado

Ahora que entiendes cómo diseñar una Gema, intenta esto:

**Nivel 1:** Diseña una Gema para una sola ley (Ej: RGPD solamente)

**Nivel 2:** Crea una Gema que combine dos leyes y explique cuándo aplica cada una

**Nivel 3:** Diseña una Gema que anticipe conflictos entre normas (Ej: RGPD vs. transparencia) y ayude a resolverlos

## Qué hemos aprendido

✓ Una Gema Normativa es un asistente especializado, no un libro de leyes  
✓ El contexto es más importante que el volumen de información  
✓ Las restricciones protegen a tu equipo y clarifican expectativas  
✓ Una buena Gema simplifica sin perder precisión legal  
✓ Los ejemplos prácticos son el puente entre ley y realidad  

**Próximo paso:** En la siguiente lección veremos prompts concretos para hacer preguntas poderosas a tu Gema.
