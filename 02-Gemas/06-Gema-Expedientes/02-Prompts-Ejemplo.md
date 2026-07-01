# Prompts Prácticos para Expedientes

## Antes de empezar

Cada prompt está diseñado para un uso específico. Puedes:
- Copiar y usar directamente
- Adaptar a tu contexto
- Combinar varios prompts
- Crear variantes propias

**Importante:** Para mejores resultados, incluye el contexto de tu administración (tipo de expediente, plazos locales, documentación específica).

## Prompt 1: ¿Qué documentos faltan en este expediente?

**Caso de uso:** Validación básica de documentación
**Tiempo de respuesta:** <30 segundos
**Precisión:** Alta

```text
Tengo un expediente de contratación de servicios de consultoría. 

Documentos que tengo:
- Acta de inicio (2024-01-15)
- Presupuesto detallado: 45.000€
- Informe de disponibilidad presupuestaria (Tesorería, 2024-01-16)
- Resolución de aprobación (firma Alcalde, 2024-01-17)
- Publicación en web municipal (10 días hábiles, hasta 2024-01-31)
- Ofertas recibidas: 4 empresas
- Acta de evaluación técnica y económica

¿Qué documentos me faltan antes de adjudicar?
```

**Cómo adaptarlo:**
1. Sustituye tipo de expediente
2. Cambia importes reales
3. Actualiza fechas
4. Incluye documentación que tienes

**Prompt mejorado (agregando contexto):**

```text
Eres validador de expedientes administrativos en mi administración.
Sé estricto: aplicamos LOPA y Ley de Contratación Pública.

Tengo un expediente de [TIPO]: [DESCRIPCIÓN]
Importe: [CANTIDAD]€
Fase actual: [FASE]

Documentación presente:
- [Doc 1]
- [Doc 2]
- [Doc 3]

¿Qué documentos faltan? Sé específico sobre criticidad y por qué cada uno es obligatorio.
```

## Prompt 2: ¿Está en riesgo algún plazo?

**Caso de uso:** Alertas de vencimientos
**Tiempo de respuesta:** <30 segundos
**Precisión:** Alta

```text
Expediente de contratación de servicios de auditoría.

Fechas clave:
- Publicación: 10 de enero (plazo mínimo: 10 días hábiles)
- Cierre de ofertas: 25 de enero
- Inicio de evaluación: 26 de enero (hoy es 3 de febrero)
- Evaluación en curso: 8 días transcurridos
- Próxima audiencia con Comisión: 10 de febrero

¿Qué plazos están en riesgo? ¿Cuántos días me quedan?
```

**Cómo adaptarlo:**
1. Sustituye fechas reales
2. Incluye todos los hitos importantes
3. Especifica la fecha "hoy"
4. Menciona próximos eventos

**Variante para urgencias:**

```text
Expediente de [TIPO], importe [CANTIDAD]€.

Plazo de evaluación: máximo 20 días desde cierre de ofertas.
Cierre de ofertas: [FECHA]
Hoy: [HOY]

¿Cuántos días me quedan? ¿Es riesgo crítico?
¿Puedo pedir prórroga?
```

## Prompt 3: ¿Cuál es el siguiente paso obligatorio?

**Caso de uso:** Orientación operacional
**Tiempo de respuesta:** <30 segundos
**Precisión:** Crítica

```text
Expediente de compra de licencias de software.

Estado actual:
- Acta de inicio: ✓ (2024-01-15)
- Solicitud de ofertas: ✓ (publicado 10 días, hasta 2024-01-31)
- Ofertas recibidas: ✓ (3 empresas, 1 de ellas ineligible)
- Evaluación: ✓ completada
- Resolución de adjudicación: ✓ (firmada 2024-02-05)
- Plazo de impugnación: transcurrido (10 días)

¿Qué debo hacer ahora?
```

**Cómo adaptarlo:**
1. Lista cada fase con su estado (✓/✗)
2. Incluye fechas de completitud
3. Menciona cualquier incidencia
4. Pregunta qué viene

**Variante estructurada:**

```text
Mi expediente está en [FASE ACTUAL].

Acción: [Lo que acabo de hacer]
Fecha: [Cuándo]

Según LOPA, ¿cuál es el siguiente paso?
¿Cuáles son los requisitos?
¿Cuál es el plazo?
```

## Prompt 4: ¿Es válida esta excepción?

**Caso de uso:** Validación de incumplimientos justificados
**Tiempo de respuesta:** 1-2 minutos
**Precisión:** Media (requiere verificación jurídica)

```text
Expediente de servicios de reformas.

Normativa: LOPA requiere mínimo 3 ofertas válidas.

Situación:
- Publicación: web municipal, portal de contratación, LinkedIn
- Plazo: 10 días hábiles
- Respuestas: 2 ofertas válidas, 1 ineligible por falta de requisitos técnicos

Justificación: "Publicamos en 3 canales como se requiere. 
Esperamos 15 días (más de lo mínimo). Solo llegaron 2 ofertas válidas."

¿Es válida esta excepción? ¿Puedo adjudicar con 2 ofertas?
```

**Cómo adaptarlo:**
1. Especifica la excepción que solicitas
2. Incluye justificación completa
3. Menciona lo que SÍ cumpliste
4. Pregunta explícitamente

**Variante para excepciones de plazo:**

```text
¿Puedo reducir el plazo de [PLAZO ORIGINAL] a [PLAZO SOLICITADO]?

Justificación: [Razón de urgencia]
Resolución de urgencia: [Sí/No - si existe, incluye fecha]

¿Es legal? ¿Qué requisitos necesito?
```

## Prompt 5: Resumen ejecutivo del expediente

**Caso de uso:** Reportes rápidos para jefatura
**Tiempo de respuesta:** 1-2 minutos
**Precisión:** Alta

```text
Quiero un resumen ejecutivo de este expediente para presentar a Gerencia.

Expediente: Contratación de servicios de asesoría jurídica
Importe: 12.500€
Fases completadas: Iniciación, Licitación, Evaluación, Adjudicación
Fase actual: Formalización (contrato en fase de firma)

Genera un resumen que responda:
1. ¿En qué fase está?
2. ¿Está dentro de plazos?
3. ¿Hay problemas?
4. ¿Cuándo estará listo para ejecución?

Formato: máximo 5 líneas, lenguaje profesional.
```

**Cómo adaptarlo:**
1. Cambia tipo y importe
2. Menciona fases completadas
3. Especifica qué información necesita jefatura
4. Define formato deseado

## Prompt 6: Validación completa (checklist)

**Caso de uso:** Validación integral antes de enviar a tesorería
**Tiempo de respuesta:** 2-3 minutos
**Precisión:** Crítica

```text
Necesito validación COMPLETA de este expediente antes de enviarlo a Tesorería.

Expediente: Servicios de limpieza para edificios municipales
Importe: 28.500€

✓ Documentación presente:
- Acta de inicio
- Presupuesto
- Disponibilidad presupuestaria
- Resolución de aprobación
- Publicación (10 días)
- Ofertas (3 empresas)
- Evaluación
- Adjudicación
- Contrato firmado

Revísalo y dame:
1. Checklist de completitud (✓/✗)
2. Problemas encontrados (si los hay)
3. Alertas de cumplimiento normativo
4. ¿Es seguro enviar a Tesorería?

Sé estricto. No apruebas nada ambiguo.
```

**Cómo adaptarlo:**
1. Lista TU documentación real
2. Especifica si hay algo cuestionable
3. Pide formato explícito
4. Define criterio de "aprobado"

## Combinando prompts

Puedes encadenar prompts para análisis completo:

```text
1. Primero: Prompt 1 (¿Faltan documentos?)
   ↓
2. Luego: Prompt 2 (¿Plazos en riesgo?)
   ↓
3. Después: Prompt 3 (¿Siguiente paso?)
   ↓
4. Finalmente: Prompt 5 (¿Resumen ejecutivo?)
```

## Ejercicio: Crear tus propios prompts

### Paso 1: Identifica 3 preguntas que haces frecuentemente

```
1. ¿_________________________________?
2. ¿_________________________________?
3. ¿_________________________________?
```

### Paso 2: Para cada pregunta, crea un prompt

Usa esta estructura:

```text
[CONTEXTO de situación]
[INFORMACIÓN específica de TU caso]
[PREGUNTA clara]
[FORMATO deseado de respuesta opcional]
```

### Paso 3: Prueba tus prompts

- Copia en tu herramienta IA
- ¿Te da respuesta útil?
- ¿Necesita ajustes?

### Paso 4: Refina

Si la respuesta no es perfecta:
- Agrega más contexto
- Sé más específico
- Define mejor el formato
- Repite

<details>
<summary>💡 Ejemplo: Prompts personalizados para mi administración</summary>

**Pregunta frecuente 1:** "¿Tenemos que hacer audiencia pública en esto?"

```text
Expediente de [TIPO], importe [CANTIDAD]€.

¿Requiere audiencia pública según LOPA?
¿Cuál es el plazo para realizarla?
¿Quién puede participar?
¿Cómo documentamos que se realizó?
```

**Pregunta frecuente 2:** "¿Este proveedor puede participar?"

```text
Proveedor: [NOMBRE], CIF [CIF]

Criterios de elegibilidad:
- Debe estar dado de alta en Hacienda
- No puede tener deudas con administración
- Debe cumplir requisitos técnicos específicos

¿Cumple este proveedor? ¿Por qué sí o por qué no?
```

**Pregunta frecuente 3:** "¿Puedo cambiar esto a mitad de proceso?"

```text
Expediente en fase de [FASE ACTUAL].

Cambio solicitado: [QUÉ CAMBIO]

¿Es legal hacer este cambio ahora?
¿Qué tramitación necesito?
¿Qué riesgos tiene?
```

</details>

---

## Resumen

✅ 6 prompts prácticos listos para usar
✅ Cada uno con variantes adaptables
✅ Enfoque en: validación, plazos, orientación, excepciones
✅ Encadena prompts para análisis completo
✅ Personaliza según tu contexto local

**Próximo paso:** Ve a **03-Ejercicio.md** para resolver un caso práctico completo.
