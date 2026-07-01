# Plantilla: Estructura Completa de tu Gema

## Cómo usar esta plantilla

Esta plantilla te guía paso a paso en la construcción de tu Gema. Llénala completamente. Será tu guía durante el desarrollo.

---

## SECCIÓN 1: OBJETIVO Y PROPÓSITO

### 1.1 Nombre de la Gema
```
Nombre: ___________________________________
(Debe ser memorable y describir qué hace)
```

### 1.2 Propósito (1 frase clara)
```
Propósito: ___________________________________

Mi Gema es un asistente especializado en: _____
```

### 1.3 Problema específico que resuelve
```
Antes (sin Gema):
- Tarea: _____________________________
- Tiempo: _______ horas/semana
- Errores comunes: ____________________

Después (con Gema):
- Tiempo esperado: _______ horas/semana
- Reducción de errores: ______%
- Beneficio principal: __________________
```

### 1.4 Usuarios y contexto
```
Usuarios: _____________________________
Frecuencia de uso: [ ] Diaria [ ] Semanal [ ] Mensual
Contexto: (¿Cuándo se usa?)
_____________________________
```

---

## SECCIÓN 2: CONTEXTO ESPECIALIZADO

### 2.1 Normas y procedimientos aplicables
```
Norma 1: ____________________________
Norma 2: ____________________________
Norma 3: ____________________________

Procedimiento base: ____________________
```

### 2.2 Conceptos clave que la Gema debe conocer
```
Concepto 1: ___________________________
Concepto 2: ___________________________
Concepto 3: ___________________________

Definiciones:
- Concepto 1: _______________________
- Concepto 2: _______________________
```

### 2.3 Datos, clasificaciones o tablas importantes
```
Categoría A: ________________________
Categoría B: ________________________
Categoría C: ________________________

Tabla 1: [Qué datos clave debe tener]
┌────┬────┬────┐
│    │    │    │
└────┴────┴────┘
```

### 2.4 Plazos, límites o restricciones normativas
```
Plazo 1: __________ (Máximo: _____ días)
Plazo 2: __________ (Máximo: _____ días)
Límite 1: __________ (Valor: ________)
Límite 2: __________ (Valor: ________)
```

### 2.5 Excepciones o variantes importantes
```
Excepción 1: ________________________
Cómo manejarla: ______________________

Excepción 2: ________________________
Cómo manejarla: ______________________

Variante local: _______________________
```

---

## SECCIÓN 3: FUNCIONALIDADES CLAVE

### 3.1 Qué puede hacer tu Gema (máximo 5-6)

```
1. [FUNCIONALIDAD]
   Caso de uso: ________________________
   Input típico: ________________________
   Output esperado: ______________________

2. [FUNCIONALIDAD]
   Caso de uso: ________________________
   Input típico: ________________________
   Output esperado: ______________________

3. [FUNCIONALIDAD]
   Caso de uso: ________________________
   Input típico: ________________________
   Output esperado: ______________________

(Máximo 6, sé específico)
```

### 3.2 Qué NO puede hacer (restricciones críticas)

```
❌ NO puede: _________________________
❌ NO puede: _________________________
❌ NO puede: _________________________
❌ NO puede: _________________________

Razón: Estos requieren decisión humana / contexto externo / autorización
```

---

## SECCIÓN 4: RESTRICCIONES Y RESPONSABILIDADES

### 4.1 Decisiones que solo pueden tomar humanos
```
Decisión 1: _________________________
Por qué: ____________________________

Decisión 2: _________________________
Por qué: ____________________________
```

### 4.2 Información que NO puede generar
```
- _________________________________
- _________________________________
- _________________________________
```

### 4.3 Responsabilidades claras
```
La Gema: Orientar, validar, alertar
Humano: Decidir, autorizar, actuar
```

---

## SECCIÓN 5: EJEMPLOS DE PROMPTS

### 5.1 Prompt principal (el más usado)

```text
[COPIAR AQUÍ EL PROMPT DEL SISTEMA - ver 03-Desarrollo.md]
```

### 5.2 Otros prompts prácticos (3-5 ejemplos)

```
PROMPT 1: [Situación típica]
Entrada: ____________________________
Respuesta esperada: ____________________

PROMPT 2: [Situación típica]
Entrada: ____________________________
Respuesta esperada: ____________________

PROMPT 3: [Caso límite]
Entrada: ____________________________
Respuesta esperada: ____________________
```

---

## SECCIÓN 6: CASOS DE USO

### 6.1 Casos de uso principales (mínimo 3)

```
CASO 1: [Situación real]
Contexto: _____________________________
Pregunta: ______________________________
Qué debe hacer: ________________________
Resultado exitoso: ______________________

CASO 2: [Situación real]
Contexto: _____________________________
Pregunta: ______________________________
Qué debe hacer: ________________________
Resultado exitoso: ______________________

CASO 3: [Situación límite o excepcional]
Contexto: _____________________________
Pregunta: ______________________________
Qué debe hacer: ________________________
Resultado exitoso: ______________________
```

### 6.2 Casos de error o rechazo

```
CASO ERROR 1: [Situación donde debe rechazar]
Entrada: _____________________________
Respuesta correcta: "NO porque..." ______
Por qué es importante: ___________________

CASO ERROR 2: [Situación donde debe alertar]
Entrada: _____________________________
Respuesta correcta: "ALERTA: ..." ________
Por qué es importante: ___________________
```

---

## SECCIÓN 7: MÉTRICAS DE ÉXITO

### 7.1 ¿Cómo sabes que funciona?

```
Métrica 1 (Precisión):
- Objetivo: ___% de aciertos
- Cómo medir: ____________________

Métrica 2 (Velocidad):
- Objetivo: < ___ minutos por consulta
- Cómo medir: ____________________

Métrica 3 (Adopción):
- Objetivo: ___ usuarios/semana la usan
- Cómo medir: ____________________

Métrica 4 (Confiabilidad):
- Objetivo: 0 errores críticos en 1 mes
- Cómo medir: ____________________
```

### 7.2 Criterio de "lista para producción"
```
✅ Funcionalidad 1 testada: ___% aciertos
✅ Funcionalidad 2 testada: ___% aciertos
✅ Funcionalidad 3 testada: ___% aciertos
✅ Casos límite probados: Sí/No
✅ Restricciones respetadas: Sí/No
✅ Documentación completa: Sí/No
✅ Equipo la validó: Sí/No
```

---

## SECCIÓN 8: PLAN DE IMPLEMENTACIÓN

### 8.1 Fases de desarrollo

```
FASE 1: Construcción básica (Estimado: 1-2 horas)
├─ Escribir prompt del sistema
├─ Incorporar contexto
└─ Crear primeros ejemplos

FASE 2: Testing (Estimado: 1-2 horas)
├─ Probar con 10+ casos reales
├─ Identificar fallos
└─ Refinar

FASE 3: Validación (Estimado: 1 hora)
├─ Validar con equipo
├─ Recoger feedback
└─ Ajustes finales

FASE 4: Presentación (Estimado: 1 hora)
├─ Preparar demo
├─ Explicar beneficios
└─ Plan de uso
```

### 8.2 Responsables

```
Desarrollo: Tú
Testing: Tú + 1-2 compañeros
Validación: Tu jefe/responsable
Presentación: Tú al equipo
```

### 8.3 Cronograma

```
Inicio: [Fecha]
Fase 1 completada: [Fecha prevista]
Fase 2 completada: [Fecha prevista]
Fase 3 completada: [Fecha prevista]
Fase 4 (Presentación): [Fecha prevista]
Lanzamiento: [Fecha prevista]
```

---

## EJERCICIO: Completar tu plantilla

**Tiempo:** 1-1.5 horas

1. **Llena cada sección** basándote en tu idea (de 01-Ideacion.md)
2. **Sé específico:** Números, fechas, ejemplos concretos (no genéricos)
3. **Revisa la coherencia:** ¿Las funcionalidades resuelven el problema?
4. **Busca feedback:** Comparte con 1-2 compañeros
5. **Refina:** Ajusta basado en feedback

<details>
<summary>💡 Ejemplo completado: Plantilla para Validador de Expedientes de Subvención</summary>

### SECCIÓN 1: OBJETIVO Y PROPÓSITO

**Nombre:** Validador Rápido de Expedientes de Subvención

**Propósito:** Asistente que valida automáticamente si solicitudes de subvención cumplen requisitos de admisibilidad

**Problema:** Revisión manual de expedientes toma 2-3 horas cada uno. Propenso a errores. Queremos: precisión, rapidez, consistencia.

**Antes vs. Después:**
- Antes: 2-3 horas/expediente, 2-3 errores por 20 expedientes
- Después: 15-20 minutos/expediente, 0 errores esperados
- Reducción: 87% de tiempo, 100% de errores evitados

**Usuarios:** Personal Servicios Subvenciones (2 personas) + Jefa de Servicios
**Frecuencia:** Diaria (durante periodos de convocatoria)

### SECCIÓN 2: CONTEXTO

**Normas:** Ley Subvenciones Andalucía, Bases Convocatoria 2024, Procedimiento Local

**Conceptos clave:**
- Admisibilidad vs. Elegibilidad (admisibilidad = requisitos formales; elegibilidad = criterios de beneficiario)
- Incompatibilidad (no puede recibir si ya recibió en últimos 2 años)
- Subsanabilidad (requisito puede suplirse en plazo)

**Tabla de documentación requerida:**
1. Solicitud oficial firmada
2. Presupuesto detallado
3. Certificado de constitución (si asociación)
4. CIF/DNI de responsable
5. Justificativo de domicilio

**Plazos:**
- Presentación solicitud: máximo 20 días desde convocatoria
- Validación admisibilidad: máximo 20 días desde cierre
- Notificación rechazados: antes evaluación méritos

**Excepciones:**
- Si < 3 meses actividad: puede presentar certificado en trámite
- Si es nueva: bases especiales para constitución

### SECCIÓN 3: FUNCIONALIDADES

1. **Validar completitud de documentación**
   - Caso: Revisar que tiene todos 5 documentos requeridos
   - Input: Listado de documentos presentados
   - Output: ✓ Completo O ✗ Incompleto - Falta: [listado]

2. **Revisar ineligibilidad por incompatibilidad**
   - Caso: Verificar que no recibió misma subvención hace <2 años
   - Input: Nombre solicitante
   - Output: ✓ Elegible O ✗ Incompatible - Recibió hace X años

3. **Validar coherencia de importes**
   - Caso: Comparar gasto declarado vs. presupuesto presentado
   - Input: Gasto solicitado + presupuesto
   - Output: ✓ Coherente O ⚠ Inconsistencia - Diferencia: X%

4. **Clasificar incumplimientos por criticidad**
   - Caso: Determinar si falta es subsanable o crítica
   - Input: Descripción del incumplimiento
   - Output: CRÍTICO (no admisible) O SUBSANABLE (3 días) O INFORMACIÓN (verifica)

5. **Generar acta de admisibilidad**
   - Caso: Crear documento conclusivo de validación
   - Input: Todos los datos anteriores
   - Output: Acta que puede firmar Jefa de Servicios

**NO puede hacer:**
- ❌ Evaluar méritos (eso es para comisión)
- ❌ Acceder a sistemas externo de subsidios anteriores (requiere búsqueda manual)
- ❌ Decidir excepciones no previstas (requiere decisión humana)
- ❌ Generar listados de compatibilidades complejas (solo alerta de incumplimiento claro)

### SECCIÓN 4: RESTRICCIONES

**Solo humanos pueden:**
- Interpretar si una circunstancia ajena es causa justificada de retraso
- Autorizar excepciones no previstas en bases
- Decidir sobre recursos/impugnaciones

**La Gema solo puede:**
- Verificar hechos objetivos (tienes/no tienes documento)
- Alertar sobre incumplimientos normativos
- Clasificar por criticidad

### SECCIÓN 5: EJEMPLOS DE PROMPTS

**Prompt principal (ver 03-Desarrollo.md)**

**Prompts prácticos:**

PROMPT 1: "¿Esta solicitud cumple requisitos?"
Input: [Listado de documentos que tiene]
Expected: Lista de completitud + alertas de incumplimientos

PROMPT 2: "¿Puedo admitir esta solicitud?"
Input: [Documentación + fecha de último subsidio similar]
Expected: Sí/No + justificación de admisibilidad

PROMPT 3: "¿Qué le falta para que sea admisible?"
Input: [Documentación presentada]
Expected: Listado de qué falta con plazo de subsanación

### SECCIÓN 7: MÉTRICAS

- Precisión: 98% aciertos (testear con 50 expedientes reales)
- Velocidad: <5 minutos por expediente
- Adopción: 100% del personal la usa en periodo de convocatoria
- Errores: 0 errores en primer mes

**Criterio lanzamiento:** Testear con 10 expedientes reales, 100% de aciertos

</details>

---

## Próximo paso

✅ **Completaste la plantilla**

Tienes ahora:
- Estructura clara ✓
- Contexto documentado ✓
- Funcionalidades especificadas ✓
- Casos de uso definidos ✓

**Próximo:** Ve a **03-Desarrollo.md** para escribir el prompt del sistema y construir tu Gema.

---

## Resumen de la plantilla

✅ Documentaste tu Gema completamente
✅ Definiste comportamiento esperado
✅ Especificaste límites claros
✅ Tienes casos de uso listos
✅ Sabes cómo medir éxito

**Estás listo para construir.** ¡Adelante! 🚀
