# Restricciones: Guardrails de Seguridad y Límites Claros

## Objetivo

Aprender a establecer restricciones explícitas en tus prompts para proteger datos sensibles, garantizar cumplimiento normativo y evitar que la IA asuma responsabilidades que no le corresponden.

### Qué vamos a aprender

- Qué son restricciones y por qué son críticas en administración
- Tipos de restricciones: datos, comportamiento, alcance
- Cómo especificar límites explícitamente
- Diferencia entre restricción y censura
- Aplicaciones prácticas con RGPD, información confidencial y responsabilidad

---

## Concepto Clave: Restricción vs Censura

### Restricción (CORRECTA)
"No devuelves datos personales de empleados sin justificación de acceso autorizado."
- **Propósito:** Proteger
- **Efecto:** Define qué sí puedo pedir dentro de límites legales
- **Resultado:** Cumplimiento normativo

### Censura (INAPROPIADA)
"No puedes decir nada crítico sobre la administración."
- **Propósito:** Ocultar
- **Efecto:** Limita análisis legítimo
- **Resultado:** Falta de valor

**Nuestra aproximación:** Restricciones robustas que protegen sin limitar análisis legítimo.

---

## Ejemplo Guiado: Protegiendo Datos de Empleados

### Situación
Necesitas análisis de datos de nómina para decisiones presupuestarias, pero los datos incluyen información sensible de empleados.

### Prompt SIN restricciones (PELIGROSO)
```text
Analiza estos datos de nómina y dame un informe de costes.
[Datos completos con nombres, DNI, domicilio, salarios individuales]
```

**Problemas:**
- IA podría revelar datos personales en análisis
- Falta de consentimiento explícito
- Violación RGPD
- No hay auditoría de quién accede a qué

### Prompt CON restricciones (CORRECTO)
```text
Analiza estos datos de nómina para decisiones presupuestarias.

RESTRICCIONES CRÍTICAS:
1. DATOS SENSIBLES: 
   - NO incluyas nombres, DNI o domicilios en ninguna respuesta
   - Usa solo categorías (grupos salariales: A, B, C, D)
   
2. ANONIMIZACIÓN:
   - Todos los análisis en términos agregados
   - Nunca identificable a nivel individual
   
3. LÍMITE DE INFORMACIÓN:
   - Solo proporciona: costes totales, medias, desviaciones
   - NO devuelvas listados de personas
   
4. JUSTIFICACIÓN DE DECISIONES:
   - Si necesitas más detalle, justifica por qué
   - Ejemplificar la decisión presupuestaria afectada

[Datos anonimizados: Nómina agregada por categorías]
```

**Ventajas:**
- Datos protegidos
- Cumplimiento RGPD
- Análisis válido mantenido
- Trazabilidad clara

---

## Tipos de Restricciones

### 1. Restricciones de Datos
```text
RESTRICCIONES DE DATOS:
- No revelar correos electrónicos personales
- No exponer datos de géolocalización
- No mencionar números de teléfono específicos
- No incluir referencias a expedientes individuales identificables
```

**Uso:** Cuando manejas datos personales o identificables.

### 2. Restricciones de Comportamiento
```text
RESTRICCIONES DE COMPORTAMIENTO:
- No asumir responsabilidades legales
- No actuar como asesor legal (esto requiere colegiado)
- No tomar decisiones finales en recursos humanos
- No hacer promesas sobre plazos administrativos
```

**Uso:** Cuando la IA podría exceder su alcance apropiado.

### 3. Restricciones de Alcance
```text
RESTRICCIONES DE ALCANCE:
- Analiza solo documentos internos, no públicos
- No extrapolés a otros organismos o contextos
- No generalizas desde un caso a normativa general
- Circunscribe análisis a contrato número X
```

**Uso:** Para evitar generalizaciones inapropiadas.

### 4. Restricciones de Verificabilidad
```text
RESTRICCIONES DE VERIFICABILIDAD:
- No inventes fuentes que no existen
- Si citas normativa, incluye artículo exacto y año
- Si hace 5 años no sabías de algo, dice "requiere verificación"
- Diferencia entre "hecho comprobado" y "posible"
```

**Uso:** Cuando necesitas confiabilidad en información crítica.

### 5. Restricciones de Conflictos
```text
RESTRICCIONES DE CONFLICTOS:
- Si hay conflicto de intereses, decláralo explícitamente
- No tomes partido en conflictividades laborales
- Mantén neutralidad en controversias entre áreas
- Señala cuando una recomendación beneficia más a un grupo
```

**Uso:** En situaciones con múltiples actores.

---

## Prompt Explicado: Estructura de Restricciones

```text
[CONTEXTO Y OBJETIVO]

RESTRICCIONES OBLIGATORIAS:
1. [TIPO DE DATO]: [QUÉ NO HACER]
2. [TIPO DE COMPORTAMIENTO]: [QUÉ NO ASUMIR]
3. [VERIFICABILIDAD]: [QUÉ ASEGURAR]

Si necesitas información que viole estas restricciones:
- Detente y explica por qué la necesitarías
- Proporciona alternativa que la cumpla

[TAREA ESPECÍFICA]
```

**Componentes clave:**
- **Contexto:** Por qué existen estas restricciones
- **Explicitación:** Cada restricción es clara y concisa
- **Salida de emergencia:** Qué hacer si algo no encaja
- **Tarea:** El trabajo real a realizar respetando límites

---

## Ejemplos de Restricciones Prácticas

### Ejemplo 1: Análisis de Expediente con RGPD
```text
Analiza este expediente administrativo.

RESTRICCIONES:
- No menciones el nombre del ciudadano, úsalo como "Solicitante"
- No incluyas domicilio completo, solo municipio
- Los datos de teléfono no aparecerán en tu análisis
- Anonimiza identificadores (DNI→DNI, etc.)
- Enfoca en el proceso administrativo, no en datos personales

ANÁLISIS ESPERADO: Conformidad legal, tramitación, plazos.
```

### Ejemplo 2: Evaluación de Personal con Confidencialidad
```text
Actúa como Responsable de Recursos Humanos.
Analiza esta propuesta de promoción.

RESTRICCIONES:
- No compartes resultados con terceros no autorizados
- No menciones comparativas con otros empleados
- No haces evaluación de desempeño individual pública
- Solo orientación confidencial a decisión management

ANÁLISIS ESPERADO: Conformidad con criterios, recomendación confidencial.
```

### Ejemplo 3: Contrato de Proveedor con Límites
```text
Revisa este contrato de suministro.

RESTRICCIONES:
- No contactes directamente al proveedor
- No negoces términos (solo analiza)
- No hagas promesas de cambios contractuales
- Tus recomendaciones son asesoramiento, no decisión vinculante
- Requiere aprobación del responsable de contratación

ANÁLISIS ESPERADO: Riesgos legales, recomendaciones de mejora.
```

### Ejemplo 4: Comunicación Pública Sensible
```text
Redacta respuesta a ciudadano sobre investigación interna.

RESTRICCIONES:
- No reveles detalles de investigación en curso
- No menciones nombres de investigados
- No anticipes conclusiones preliminares
- Mantén tono profesional y empático
- Reitera derecho de acceso a información cuando proceda

RESPUESTA ESPERADA: Comunicación profesional, dentro de límites legales.
```

---

## Ejercicio

**Situación:**
Tu área ha recibido una solicitud de análisis sobre problemas de clima laboral en un departamento. Necesitas analizar sin vulnerar privacidad de empleados ni revelar información que pudiera perjudicar investigaciones.

**Datos disponibles (sensibles):**
```
- Quejas anónimas de 5 empleados
- Entrevistas privadas realizadas por RRHH
- Resultados de test de satisfacción
- Información de bajas médicas relacionadas
- Correos internos entre management
```

**Tu tarea:**
Diseña un prompt que:
1. Analice la situación real
2. Establezca restricciones claras sobre datos sensibles
3. Especifique qué información SÍ se puede usar
4. Proporcione recomendaciones sin revelar identidades

**Restricciones que debes especificar:**
- Datos anónimos
- No revelar causas personales de bajas
- No mencionar correos específicos
- Mantener confidencialidad de denunciantes

**Tiempo:** 20 minutos

---

## Solución Orientativa

<details>
  <summary>¿Quieres ver cómo estructurar el prompt con restricciones?</summary>

### Prompt con Restricciones Explícitas
```text
Actúa como Responsable de Mejora Organizacional en administración pública.

CONTEXTO: Análisis de situación de clima laboral en Departamento de X 
basado en información sensible. Objetivo: diagnóstico con recomendaciones.

RESTRICCIONES OBLIGATORIAS:

1. PRIVACIDAD DE EMPLEADOS:
   - Nunca menciones nombres ni identificadores
   - Usa referencias como "Grupo de 5 empleados" o "Equipo técnico"
   - Anonimiza completamente las quejas

2. INFORMACIÓN SENSIBLE:
   - Razones de bajas médicas: Solo categoría (ausencia prolongada)
   - No especules sobre causas personales
   - Si hay información médica, respeta confidencialidad

3. CORREOS Y COMUNICACIONES:
   - No transcribo diálogos específicos entre personas
   - Usa resumen temático: "Comunicación sobre...", no detalles personales

4. INVESTIGACIONES:
   - Si hay investigación en curso: No anticipes conclusiones
   - Señala que hay investigación pero no comentes detalles
   - Enfócate en situación general

5. RECOMENDACIONES:
   - Deben ser implementables sin revelar fuentes
   - No acuses individuos, propone mejoras estructurales
   - Enfoque colectivo, no individual

INFORMACIÓN USABLE:
- Patrón agregado de quejas (frecuencia temas)
- Resultados de test de satisfacción (puntuaciones, no respuestas)
- Tendencias de ausentismo (no casos individuales)
- Temas comunes identificados

ANÁLISIS ESPERADO:
- Diagnóstico de clima laboral (general)
- Problemas identificados (agrupados)
- Recomendaciones de mejora organizacional
- Plan de acción confidencial para management

[Datos presentados respetando anonimización]
```

### Estructura esperada de respuesta

```
## DIAGNÓSTICO (Respetuoso de privacidad)
- Grupo de 5 empleados reporta preocupaciones
- Test de satisfacción muestra puntuación 3.2/5 (baja)
- Ausentismo en el grupo: aumento del 40%

## TEMAS COMUNES IDENTIFICADOS
- Comunicación poco clara
- Falta de reconocimiento
- Sobrecarga de tareas

## RECOMENDACIONES ESTRUCTURALES
[Mejoras organizacionales que no revelan fuentes ni personas]

## ADVERTENCIAS SOBRE LÍMITES
- Esta es orientación; decisiones últimas requieren management
- Si hay investigación formal en curso, coordina con ella
- Implementación requiere aprobación de RRHH
```

**Ventaja:** Análisis útil manteniendo privacidad y confidencialidad.

</details>

---

## Reto Avanzado

**Nivel: Experto**

Crea un prompt que combine:
1. **Restricciones** (protección de datos)
2. **Chain of Thought** (razonamiento paso a paso)
3. **Rol Especializado** (Abogado o Auditor)

El prompt debe permitir análisis profundo respetando todos los límites de seguridad.

Desafío extra: Diseña restricciones para un caso donde hay tensión entre "análisis útil" y "protección de privacidad". ¿Cómo las balancearías?

---

## Qué Hemos Aprendido

✅ **Restricciones son protección, no limitación:** Bien diseñadas, permiten análisis mejor.

✅ **RGPD no es obstáculo:** Es estructura para trabajar responsablemente.

✅ **Explicitación es clave:** Si no lo dices, IA podría asumir mal.

✅ **Diferentes contextos, diferentes restricciones:** Contratos, RRHH, datos ciudadanos... cada uno requiere límites específicos.

✅ **Declaración de límites mejora confianza:** Si declares qué no harás, clientes confían más en qué sí haces.

✅ **Responsabilidad clara:** Restricciones bien definidas evitan que IA se vea como responsable de decisiones que no le corresponden.

**Próximo paso:** Aprende a Encadenar Tareas (documento final) para orquestar múltiples prompts en flujos complejos.
