# Prompts Efectivos para la Gema de Normativa

## Objetivo
Aprender a formular preguntas potentes a tu Gema de Normativa para obtener respuestas claras, precisas y aplicables a tu trabajo diario.

## Qué vamos a aprender
- Cómo pasar de preguntas vagas a preguntas específicas
- Estructura de prompts efectivos para normativa
- Técnicas para simplificar leyes complejas
- Cómo comparar normativas diferentes
- Cuándo y cómo pedir orientación especializada

## Ejemplo guiado

Carlos trabaja en la Oficina de Transparencia de un ayuntamiento. Recibe una solicitud de información de un ciudadano sobre empleados públicos. Carlos sabe que está regulado por la **Ley 19/2013 de Transparencia** y el **RGPD**, pero no sabe exactamente cuál es el equilibrio.

**Pregunta vaga:** "¿Qué dice la ley sobre esto?"  
**Resultado:** respuesta muy larga, general, con demasiada información

**Pregunta efectiva:** "Según la Ley 19/2013, ¿puedo publicar el nombre y departamento de un empleado? ¿Qué dice el RGPD?"  
**Resultado:** respuesta clara, con los dos marcos legales, aplicable inmediatamente

## Prompts explicados y ejemplos

### Prompt 1: Explicación Simple

Este prompt busca que tu Gema simplifique una norma compleja en términos que cualquiera entienda.

```text
Soy personal administrativo sin formación jurídica. Explícame qué dice este artículo en 4 párrafos máximo:

[PEGA AQUÍ EL ARTÍCULO O DESCRIBE LA LEY]

Por favor:
1. Párrafo 1: Qué es (en términos simples)
2. Párrafo 2: Qué afecta (a mi trabajo específicamente)
3. Párrafo 3: Qué debo hacer (acciones concretas)
4. Párrafo 4: Qué puede pasar si no lo hago (consecuencias)
```

**Ejemplo real:**
```text
Soy personal administrativo sin formación jurídica. Explícame qué dice este artículo en 4 párrafos máximo:

Artículo 6 RGPD - "Licitud del tratamiento"

Por favor:
1. Párrafo 1: Qué es
2. Párrafo 2: Qué afecta a mi trabajo específicamente en registros civiles
3. Párrafo 3: Qué debo hacer
4. Párrafo 4: Qué puede pasar si no lo hago
```

### Prompt 2: Interpretación Contextualizada

Cuando necesitas saber cómo aplica una ley a tu situación específica.

```text
Contexto: [describe tu situación]

Normativa: [ley o artículo]

Mi pregunta: [qué necesitas saber]

Por favor, explica:
1. ¿Se aplica esta norma a mi caso?
2. ¿Cuál es la interpretación correcta?
3. ¿Hay excepciones que deba conocer?
4. ¿Quién puede darte orientación legal final?
```

**Ejemplo real:**
```text
Contexto: Trabajo en una biblioteca pública municipal. Un usuario solicita acceso a la lista de registros de préstamos de otro usuario.

Normativa: Ley 19/2013 de Transparencia y RGPD

Mi pregunta: ¿Debo dar esa información?

Por favor, explica:
1. ¿Se aplica esta norma a mi caso?
2. ¿Cuál es la interpretación correcta?
3. ¿Hay excepciones que deba conocer?
4. ¿Quién puede darte orientación legal final?
```

### Prompt 3: Cumplimiento Verificable

Para comprobar si tu procedimiento cumple con la ley.

```text
He creado este procedimiento:

[DESCRIBE LOS PASOS QUE SIGUES]

Normativa aplicable: [LEY/DECRETO]

¿Estoy cumpliendo con la normativa? Analiza:
1. Cada paso que doy
2. Si cada paso cumple con la ley
3. Dónde puede haber riesgos
4. Qué cambios harías
```

**Ejemplo real:**
```text
He creado este procedimiento para guardar datos de usuarios:

1. Recopilo nombre, DNI y correo en formulario
2. Los guardo en Excel en una carpeta compartida
3. Los borro después de 6 meses
4. No informo al usuario sobre qué haremos con sus datos

Normativa aplicable: RGPD y LOPDGDD

¿Estoy cumpliendo? Analiza:
1. Cada paso que doy
2. Si cada paso cumple con la ley
3. Dónde puede haber riesgos
4. Qué cambios harías
```

### Prompt 4: Comparación de Normas

Cuando dos leyes parecen contradictirse.

```text
Tengo dos normas que parecen en conflicto:

NORMA A: [artículo de una ley]

NORMA B: [artículo de otra ley]

Mi pregunta: ¿Cuál prevalece en mi situación?

Contexto: [qué intento hacer]

Por favor:
1. Explica qué dice cada una
2. ¿Hay realmente conflicto?
3. Cuál aplica en mi caso y por qué
4. Qué hago si aún no estoy seguro
```

## Variantes

Según tu necesidad, adapta los prompts:

| Necesidad | Ajusta el prompt |
|---|---|
| **Es urgente** | Añade "Responde en máximo 2 párrafos" |
| **Necesitas crear un proceso** | Añade "Dame 5 pasos claros que debo seguir" |
| **Hay riesgo legal** | Añade "¿Qué riesgos tiene?" y "¿Cuándo consultar abogado?" |
| **Es muy técnico** | Añade "Usa solo términos administrativos simples" |
| **Afecta a múltiples leyes** | Añade "¿Qué otra normativa afecta a esto?" |

## Ejercicio

**Tu misión: Crea 3 prompts para tu trabajo**

1. Identifica una norma que consultas frecuentemente
2. Identifica un caso donde dos normas parecen conflictuar
3. Identifica un procedimiento que quieras verificar

Para cada uno, escribe un prompt siguiendo los modelos anteriores.

**Pistas:**
- Sé lo más específico posible
- Incluye el contexto real de tu trabajo
- Pide análisis paso a paso

## Solución orientativa

<details>
  <summary>¿Quieres ver ejemplos completos?</summary>

**Ejemplo 1 - Normativa que consulto frecuentemente:**

```text
Trabajo en la Dirección de Personal. Necesito saber cuándo puedo consultar el expediente de un empleado público.

Contexto: Ley 40/2015 (Régimen Jurídico del Sector Público) y RD 5/2015 (Función Pública)

Mi pregunta: ¿Un empleado puede acceder a su expediente completo? ¿Hay restricciones?

Necesito: 3 respuestas cortas (sí/no/depende) y para cada una una razón legal.
```

**Ejemplo 2 - Conflicto entre normas:**

```text
Recibimos una solicitud bajo la Ley 19/2013 (Transparencia) pidiendo información sobre procesos de selección de personal. El empleado que ganó prefiere que no se haga pública.

Norma A: "Transparencia activa de procedimientos públicos"
Norma B: "Protección de datos personales en procesos de selección"

¿Qué publicamos?

Contexto: Municipio de 50.000 habitantes, proceso de oposición.
```

**Ejemplo 3 - Procedimiento a verificar:**

```text
Nuestro procedimiento para notificaciones:

1. Correo electrónico al interesado
2. Seguimiento si no abre en 5 días
3. Si no responde, lo consideramos notificado
4. Guardamos prueba de envío en papel

Normativa: Ley 39/2015 (Procedimiento Administrativo Común)

¿Es válido este proceso?
```

</details>

## Reto avanzado

Nivel 1: Crea un prompt para una ley que te afecta, úsalo con tu Gema y ajusta la respuesta

Nivel 2: Crea dos prompts que se contradicen (para entender mejor cómo formula la Gema)

Nivel 3: Crea un prompt que combine 3 normativas diferentes (RGPD + Transparencia + Procedimiento Administrativo) aplicadas a un caso real

## Qué hemos aprendido

✓ Una pregunta específica da una respuesta específica  
✓ Los prompts efectivos incluyen contexto y necesidad clara  
✓ Los mejores prompts piden análisis paso a paso  
✓ Comparar normas requiere estructura, no solo preguntar "¿cuál gana?"  
✓ Los ejemplos reales ahorran confusión  

**Próximo paso:** En el siguiente módulo aplicaremos todo esto a un caso práctico completo.
