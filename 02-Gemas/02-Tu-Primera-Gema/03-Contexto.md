# Contexto: La Base de tu Gema Especializada

## ¿Qué es el contexto en una Gema?

El contexto es el conjunto de información que le das a tu Gema para que sea experta en su área. Es como un bibliotecario que te da acceso a los libros correctos antes de responderte una pregunta. Sin contexto, tu Gema es un generador de texto genérico. Con contexto, se convierte en un especialista.

El contexto puede incluir:
- **Documentos**: manuales, guías, procedimientos, normativas
- **Datos estructurados**: tablas, clasificaciones, categorías
- **Normas y regulaciones**: leyes, decretos, instrucciones técnicas
- **Ejemplos**: casos previos, decisiones tomadas, mejores prácticas
- **Restricciones**: qué no debe hacer, límites, responsabilidades

### Ejemplo práctico
Sin contexto, si le pides a una Gema "¿Cuál es el siguiente paso en un procedimiento de contratación?", te dará un paso genérico. Con contexto sobre la LOPA, el Manual de Procedimientos de tu organización y los plazos específicos, te dirá exactamente qué debe ocurrir a continuación en tu administración.

## Por qué el contexto importa

Una Gema sin contexto es imprecisa y general. Puede ser peligrosa si da consejos genéricos que no aplican a tu situación específica.

Un contexto bien diseñado:

1. **Especializa la Gema**: transforma un modelo general en un experto
2. **Reduce errores**: disminuye alucinaciones sobre normas inexistentes
3. **Acelera respuestas**: no necesita explicar el marco general
4. **Aumenta confianza**: el usuario confía en la precisión
5. **Mejora consistencia**: la Gema siempre responde con los mismos criterios

## Ejemplos de contexto útil

### Para una Gema de Expedientes
```text
CONTEXTO: Procedimiento de contratación según la LOPA (Ley de Obra Pública)
Documentos necesarios:
- Acta de inicio
- Presupuesto detallado
- Licitación o solicitud de ofertas
- Evaluación de ofertas
- Resolución de adjudicación
- Certificado de desempeño

Plazos clave:
- Publicación de licitación: mínimo 15 días hábiles
- Plazo de presentación de ofertas: mínimo 10 días desde publicación
- Evaluación: máximo 20 días
- Resolución: máximo 30 días desde cierre

Responsables:
- Gerencia: control general
- Secretaría: documentación
- Administración: validación de cumplimiento
```

### Para una Gema de Inventario
```text
CONTEXTO: Gestión de inventario municipal
Categorías de bienes:
- Inmuebles
- Vehículos (matriculación, seguros, ITV anual)
- Equipos informáticos (vida útil: 4 años)
- Mobiliario
- Herramientas

Ciclo de vida:
1. Alta: registro con número único
2. Revisión periódica: anual (inventario físico)
3. Mantenimiento: según cronograma
4. Baja: justificación y autorización

Documentación requerida:
- Ficha de bien (descripción, ubicación, responsable)
- Registro de mantenimiento
- Certificado de disposición (al darlo de baja)
```

## Cómo incluir contexto en el prompt del sistema

El contexto va en el **prompt del sistema** (system prompt). Este es el mensaje que le das a la Gema antes de que empiece a interactuar contigo.

### Estructura recomendada

```text
Eres un asistente especializado en [ÁREA].

Tu objetivo es [OBJETIVO ESPECÍFICO].

INFORMACIÓN DE REFERENCIA:
[Contexto sobre normas, procedimientos, documentos]

FUNCIONALIDADES:
1. [Qué puede hacer]
2. [Qué puede hacer]
3. [Qué NO puede hacer]

FORMATO DE RESPUESTA:
[Especifica cómo debe presentar la información]

RESTRICCIONES:
- No puedes [X]
- Debes siempre [Y]
- Si [situación], entonces [acción]
```

### Ejemplo completo para Gema de Procedimientos

```text
Eres un asistente experto en procedimientos administrativos de la administración local.

Tu objetivo es orientar al personal administrativo sobre los pasos exactos, plazos y 
responsables en cada procedimiento.

INFORMACIÓN DE REFERENCIA:
Procedimientos regidos por LOPA, Ley de Contratación Pública y Normativa Local.
Todos los procedimientos tienen fases definidas con plazos específicos.

FUNCIONALIDADES:
1. Identificar en qué fase se encuentra un procedimiento
2. Indicar el siguiente paso obligatorio
3. Alertar sobre plazos próximos a vencer
4. Identificar documentación faltante
5. NO emitir decisiones finales, solo orientación

FORMATO DE RESPUESTA:
- Fase actual: [Nombre de la fase]
- Próximo paso: [Acción específica]
- Plazo: [Días hábiles disponibles]
- Documentación: [Qué falta]
- Notas: [Alertas importantes]

RESTRICCIONES:
- Siempre cita la norma aplicable
- No hagas interpretaciones legales (derivar a servicios jurídicos si es necesario)
- Usa datos de nuestro Manual de Procedimientos como referencia principal
```

## Limitaciones del contexto

### 1. Tamaño y tokens

Cada modelo tiene un límite de tokens (palabras + números). Si tu contexto es demasiado grande, no entra en la ventana de contexto.

**Límites típicos:**
- GPT-4: hasta 8,000 o 128,000 tokens (según versión)
- Claude: hasta 200,000 tokens
- Modelos locales: 4,000-16,000 tokens

**Calcular:** aproximadamente 1 token ≈ 4 caracteres.

### 2. Relevancia del contexto

Más contexto no siempre es mejor. Un contexto que incluye información irrelevante puede confundir a la Gema.

**Buena práctica:** incluye solo el contexto que la Gema necesitará para responder al 90% de las preguntas que le harás.

### 3. Actualización del contexto

El contexto debe mantenerse actualizado. Si una norma cambia o tu procedimiento se modifica, la Gema seguirá dando respuestas basadas en información antigua.

**Estrategia:** revisa el contexto mensualmente y actualiza la Gema.

### 4. Conflictos de contexto

Si el contexto contiene información contradictoria, la Gema puede quedar confundida.

**Solución:** valida el contexto antes de incluirlo. Si hay dos versiones de una norma, incluye solo la vigente.

## Tipos de contexto por nivel

### Nivel 1: Contexto Mínimo (200-500 palabras)
- Definiciones básicas
- 2-3 puntos clave
- Caso de uso principal

**Uso:** Gemas simples, respuestas rápidas

### Nivel 2: Contexto Estándar (500-1500 palabras)
- Procedimiento completo
- Normas aplicables
- Ejemplos de entrada/salida
- Restricciones clave

**Uso:** Gemas operacionales, la mayoría de casos

### Nivel 3: Contexto Completo (1500-5000 palabras)
- Manual completo del procedimiento
- Todas las normas y excepciones
- Casos especiales
- Histórico de decisiones

**Uso:** Gemas críticas, decisiones complejas, auditoría

## Ejercicio: Crear contexto para tu Gema

Elige un procedimiento o tarea que realizas frecuentemente (p.ej., "validar un expediente", "elaborar un informe", "tramitar una solicitud").

### Paso 1: Define el objetivo
```
Mi Gema debe: _________________________________
```

### Paso 2: Identifica el contexto necesario
Responde estas preguntas:
- ¿Qué normas aplican?
- ¿Cuáles son los pasos principales?
- ¿Cuál es el resultado esperado?
- ¿Qué errores comunes hay que evitar?

### Paso 3: Recopila información
- Busca el manual relevante
- Extrae los puntos clave
- Crea ejemplos de tu trabajo

### Paso 4: Escribe el contexto
Siguiendo la estructura recomendada, escribe entre 300-800 palabras que describan el contexto de tu Gema.

<details>
<summary>💡 Ejemplo completado: Contexto para Gema de Validación de Expedientes</summary>

```text
CONTEXTO: Validación de expedientes de contratación menor

Objetivo: Verificar que un expediente de contratación cumpla con la normativa local 
antes de ejecutar el gasto.

NORMATIVA APLICABLE:
- LOPA (Ley de Obra Pública)
- Ley de Contratación Pública (si aplica)
- Manual de Procedimientos de Contratación Menor
- Instrucción de Contratación Menor (última revisión: 2024)

DOCUMENTACIÓN REQUERIDA:
1. Solicitud inicial: justificación del gasto
2. Presupuesto detallado: desglose por partidas
3. Comprobante de disponibilidad presupuestaria (informe de tesorería)
4. Justificación de necesidad
5. Resolución de aprobación (firma de ordenanza)
6. Ofertas recibidas (mínimo 3, o justificación de por qué menos)
7. Acta de evaluación
8. Resolución de adjudicación
9. Contrato o orden de ejecución

PLAZOS CLAVE:
- Publicación de necesidad: mínimo 5 días hábiles
- Respuesta de proveedores: mínimo 3 días desde publicación
- Evaluación: máximo 5 días hábiles
- Adjudicación: máximo 3 días hábiles tras evaluación

CONTROLES OBLIGATORIOS:
1. ¿Está todo firmado por autoridad competente?
2. ¿Hay disponibilidad presupuestaria?
3. ¿Se cumplió el plazo de publicación mínimo?
4. ¿Hay al menos 3 ofertas o justificación de por qué no?
5. ¿El importe adjudicado no supera la oferta más baja?

ALERTAS COMUNES:
- Falta firma del ordenanza
- No hay comprobante de disponibilidad presupuestaria
- Menos de 3 ofertas sin justificación
- Plazo entre publicación y cierre insuficiente
- Adjudicación a oferta que no es la más favorable

FORMATO DE RESPUESTA:
- Estado: [Completo / Incompleto]
- Documentación: [Lista con ✓ o ✗]
- Alertas: [Problemas encontrados]
- Acción siguiente: [Qué hacer]
```

</details>

---

## Resumen clave

✅ **El contexto es lo que diferencia una Gema de un modelo genérico**
✅ **Incluye: normas, procedimientos, ejemplos, restricciones**
✅ **Tamaño recomendado: 500-1500 palabras**
✅ **Revísalo regularmente para mantenerlo actualizado**
✅ **Menos contexto irrelevante es mejor que más contexto confuso**

En el próximo capítulo aprenderás a **refinar tu Gema iterativamente** para que funcione cada vez mejor.
