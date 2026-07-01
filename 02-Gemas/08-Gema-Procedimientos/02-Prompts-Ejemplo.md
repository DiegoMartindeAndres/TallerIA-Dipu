# Prompts Prácticos para Procedimientos

## Prompt 1: ¿Dónde estamos en este procedimiento?

**Caso de uso:** Orientación general
**Tiempo:** <1 minuto
**Urgencia:** Moderada

```text
Tenemos un procedimiento de contratación de servicios en marcha.

Estado actual:
- Acta de inicio: Completa (10/01/2024)
- Aprobación: Completa (11/01/2024)
- Publicación: Completa (20/01 - 3/02, 10 días hábiles)
- Recepción ofertas: Completa (3/02/2024, recibidas 4 ofertas)
- Evaluación: EN CURSO (comenzó 4/02, comisión evaluando)

Hoy: 18 de febrero

¿En qué fase estamos? ¿Vamos retrasados? ¿Cuál es el siguiente paso?
```

## Prompt 2: ¿Cuál es exactamente el próximo paso?

**Caso de uso:** Orientación operacional
**Tiempo:** <30 segundos
**Urgencia:** Alta

```text
Acabamos de recibir y registrar las ofertas en un procedimiento de contratación.

¿Cuál es el próximo paso OBLIGATORIO que debemos hacer?
¿Quién es responsable?
¿Cuánto tiempo tenemos?
¿Qué documentación se genera en este paso?
```

**Variante más específica:**

```text
Hemos completado la evaluación técnica y económica.
Tenemos el acta de evaluación lista para que la firme la comisión.

¿Qué paso obligatorio viene EXACTAMENTE después?
¿Quién debe hacerlo?
¿Es resolver la adjudicación o hay algo más primero?
```

## Prompt 3: ¿Quién firma esto? ¿Con qué autorización?

**Caso de uso:** Claridad de responsabilidades
**Tiempo:** <30 segundos
**Urgencia:** Crítica

```text
Tenemos una resolución de adjudicación lista.

¿Quién debe firmarla?
  a) ¿El Alcalde?
  b) ¿Un delegado del Alcalde?
  c) ¿El Gerente?
  d) ¿Otra persona?

¿Requiere visado de Jurídica antes?
¿Requiere aprobación de algún órgano?
¿Hay constancia documentada de la autorización?
```

## Prompt 4: ¿Cuánto tiempo tenemos para completar esta fase?

**Caso de uso:** Gestión de plazos
**Tiempo:** <1 minuto
**Urgencia:** Alta

```text
Estamos en fase de evaluación de un procedimiento de contratación.

Datos:
- Cierre de ofertas: 5 de marzo
- Hoy: 10 de marzo
- Plazo máximo legal: 20 días hábiles desde cierre

¿Cuántos días hábiles tenemos disponibles?
¿Cuándo es el vencimiento exacto (incluyendo festivos)?
¿Hay riesgo de incumplimiento?
```

## Prompt 5: ¿Hemos omitido algún paso?

**Caso de uso:** Validación de secuencia
**Tiempo:** 1-2 minutos
**Urgencia:** Alta

```text
Quiero verificar que nuestro procedimiento de contratación cumple con LOPA.

Pasos que hemos completado:
1. ✓ Acta de inicio
2. ✓ Presupuesto
3. ✓ Aprobación (firma Alcalde)
4. ✓ Publicación (10 días)
5. ✓ Recepción ofertas
6. ✓ Evaluación técnica
7. ✗ Evaluación económica (¿la haremos después?)
8. ? Acta de evaluación conjunta
9. ✓ Propuesta de adjudicación
10. ✓ Resolución de adjudicación
11. (No empezado) Contrato

¿Cumplimos todos los requisitos? ¿Falta algo? ¿El orden es correcto?
```

## Prompt 6: ¿Esto es diferente porque es urgencia?

**Caso de uso:** Procedimientos excepcionales
**Tiempo:** 1-2 minutos
**Urgencia:** Crítica

```text
Tenemos una necesidad URGENTE de contratar servicios de limpieza.

Situación:
- La empresa actual canceló contrato sin aviso
- Necesitamos cobertura ASAP
- Servicios de Limpieza pide que hagamos contratación de emergencia

¿Cuál es el procedimiento si es urgencia?
¿Cuáles son los plazos reducidos permitidos?
¿Quién debe autorizar esto?
¿Qué documentación necesitamos?
¿Es legal reducir plazos de publicación?
```

## Combinando prompts para auditoría completa

```
AUDITORÍA COMPLETA DE PROCEDIMIENTO:

Paso 1 (Prompt 1): ¿Dónde estamos?
  ↓
Paso 2 (Prompt 5): ¿Hemos omitido pasos?
  ↓
Paso 3 (Prompt 2): ¿Cuál es el próximo paso?
  ↓
Paso 4 (Prompt 3): ¿Quién firma?
  ↓
Paso 5 (Prompt 4): ¿Cuánto tiempo tenemos?
  ↓
Resultado: Procedimiento validado y orientado
```

## Ejercicio: Crear tus prompts

### Paso 1: Identifica 3 procedimientos complejos
```
1. ¿_________________________________?
2. ¿_________________________________?
3. ¿_________________________________?
```

### Paso 2: Para cada uno, crea un prompt
Usa estructura:
```text
[CONTEXTO del procedimiento]
[ESTADO ACTUAL: qué fases completadas, cuál en curso]
[PREGUNTA clara: dónde, qué sigue, plazos, responsables]
```

### Paso 3: Prueba con un procedimiento real
- ¿La respuesta es precisa?
- ¿Te falta información en el prompt?
- ¿Necesita ajustes?

### Paso 4: Refina y documenta
Crea tu propio "playbook" de procedimientos.

<details>
<summary>💡 Ejemplo: Prompts personalizados para mi administración</summary>

**Pregunta frecuente 1: "¿Podemos adjudicar ya?"**

```text
Procedimiento de contratación de servicios.

Estado:
- Ofertas cerradas: 5 de marzo (hace 10 días)
- Comisión evaluadora: Reunida 2 veces
- Acta técnica: COMPLETA (5/03)
- Acta económica: PENDIENTE (prevista para hoy)

¿Podemos firmar resolución de adjudicación sin que esté lista el acta económica?
¿Cuál es el requisito mínimo?
```

**Pregunta frecuente 2: "¿Quién autoriza esto?"**

```text
Tenemos una solicitud de prórroga en un procedimiento de contratación.

¿Quién autoriza ampliación de plazo?
  - ¿El Alcalde?
  - ¿La Comisión evaluadora?
  - ¿Gerencia?

¿Requiere documentación especial?
¿Cuál es el máximo de prórroga permitida?
```

**Pregunta frecuente 3: "¿Estamos retrasados?"**

```text
Procedimiento iniciado: 1 de febrero 2024.

Fases completadas:
- Aprobación: 3 de febrero
- Publicación: 20 enero - 3 febrero
- Cierre ofertas: 5 de marzo
- Hoy: 20 de marzo
- Siguiente (Resolución adjudicación): previsto para 25 de marzo

Plazo legal: 50-60 días típico desde inicio a formalización.

¿Vamos dentro de plazos?
¿Vamos al ritmo esperado?
¿Hay riesgo de incumplimiento?
```

</details>

---

## Resumen

✅ 6 prompts prácticos y listos para usar
✅ Cada uno resuelve una pregunta común
✅ Puedes combinarlos para auditoría completa
✅ Personaliza según tus procedimientos
✅ Documentación clara = menos errores

**Próximo paso:** Ve a **03-Ejercicio.md** para resolver un caso completo paso a paso.
