# Ejemplos: Few-Shot Learning 🎓

📌 **Objetivo**: Entender cómo los ejemplos reentrenan la IA en tiempo real. Un buen ejemplo vale más que mil palabras.

## 📚 Qué vamos a aprender

- Por qué los ejemplos son tan poderosos
- Cómo dar buenos ejemplos (few-shot learning)
- Cuántos ejemplos necesitas
- Cómo aplicar esto en casos administrativos

---

## 🧠 Ejemplo guiado

**Caso**: Necesitas clasificar solicitudes por urgencia.

### ❌ Sin ejemplos (resultado genérico):
```text
Clasifica esta solicitud por urgencia: CRÍTICA, ALTA, NORMAL, BAJA.

Solicitud: "Necesito una licencia para abrir un café."
```

**IA responde**: 
> "NORMAL (es una solicitud estándar)"

---

### ✅ Con ejemplos (resultado preciso):
```text
Clasifica solicitudes por urgencia: CRÍTICA, ALTA, NORMAL, BAJA.

EJEMPLOS PARA CALIBRAR:

Ejemplo 1:
Solicitud: "Llevo 3 meses esperando resolución de licencia ambiental. 
He paralizado toda producción."
Contexto: Expediente abierto hace 6 meses, media legal es 3 meses.
Clasificación correcta: CRÍTICA (Retraso grave + impacto económico)

Ejemplo 2:
Solicitud: "Solicito licencia de cambio de uso de local residencial a oficinas."
Contexto: Completamente documentado, barrio sin conflictividad.
Clasificación correcta: NORMAL (Trámite estándar)

Ejemplo 3:
Solicitud: "Necesito ampliación de licencia por 2 meses más. 
Ya completé obras pero trámites burocráticos retrasaron firma."
Contexto: Solicitante tiene buen historial, ampliación es común.
Clasificación correcta: ALTA (Requiere rapidez pero no es crítico)

AHORA clasifica:
Solicitud: "Necesito una licencia para abrir un café."
```

**IA responde**:
> "NORMAL (Solicitud estándar de cambio de uso sin urgencia aparente. 
> Si hubiera retrasos previos o complicaciones, podría ser ALTA)"

**Diferencia**: La IA comprendió qué significa "urgencia" observando ejemplos reales.

---

## 💬 Few-Shot Learning explicado

**Few-Shot** = "aprender de pocos ejemplos"

Funciona así:

1. **Sin ejemplos** → IA predice por probabilidad general
2. **Con 1 ejemplo** → IA comienza a entender patrón
3. **Con 2-3 ejemplos** → IA calibra bien (punto óptimo)
4. **Con 5+ ejemplos** → Mejora se estabiliza (punto de rendimientos decrecientes)

---

## 🔄 Tipos de ejemplos y cómo darlos

### Tipo 1: Ejemplo de FORMATO

**Caso**: Redactar memorándums en estilo consistente.

```text
Redacta este memorándum con el formato de los anteriores:

FORMATO ESPERADO (basado en ejemplos previos):

EJEMPLO 1 - Comunicación interna:
"MEMORÁNDUM
Para: Jefes de Sección
De: Dirección General
Asunto: Nueva normativa digital
Fecha: 5 de octubre de 2024

Introducción (por qué).
Cuerpo (qué cambia, paso-a-paso).
Requerimientos (qué debe hacer cada departamento).
Contacto para preguntas: [email]"

EJEMPLO 2 - Urgente:
"MEMORÁNDUM - ASUNTO URGENTE
Para: [específico]
De: [específico]
Asunto: [muy concreto]
Fecha: [hoy]

Párrafo 1: Situación crítica.
Párrafo 2: Acción inmediata requerida.
Párrafo 3: Plazo y responsable.
Contacto: [teléfono directo]"

AHORA redacta:
Asunto: Implementación nuevo sistema de expedientes digitales
Públicos: Todos los administrativos
Urgencia: Sí, a partir del 15 de octubre
```

---

### Tipo 2: Ejemplo de DECISIÓN

**Caso**: Clasificar documentos como "Aprobable" o "Requiere enmienda".

```text
Clasifica esta solicitud como APROBABLE o REQUIERE ENMIENDA.

EJEMPLOS DE APROBACIÓN:

EJEMPLO 1:
Solicitud: Licencia de obra menor
- Documentación: Completa (proyecto, presupuesto, firma)
- Normativa: Cumple zonas permitidas
- Pagos: Tasas abonadas
Clasificación: APROBABLE ✅

EJEMPLO 2:
Solicitud: Cambio de uso de local
- Documentación: Proyecto técnico, estudio acústico, antecedentes
- Normativa: Zona permite usos mixtos
- Afecciones: Sin problemas de vecindario (estudio consultó 3 vecinos)
Clasificación: APROBABLE ✅

EJEMPLOS DE ENMIENDA REQUERIDA:

EJEMPLO 1:
Solicitud: Licencia de obra mayor
- Documentación: Falta estudio de impacto ambiental
- Normativa: Zona protegida requiere análisis ambiental
- Tasas: Pagadas
Clasificación: REQUIERE ENMIENDA ⚠️
(Solicitante tiene 10 días para adjuntar estudio)

EJEMPLO 2:
Solicitud: Ampliación comercio
- Documentación: Incompleta (falta certificado de limpieza)
- Normativa: Cumple
- Afecciones: No evaluadas
Clasificación: REQUIERE ENMIENDA ⚠️

AHORA clasifica:
Solicitud: Remodelación de fachada en edificio histórico
- Documentación: Proyecto completo, firma, tasas
- Normativa: Zona centro histórico requiere informe patrimonio
- Status: Sin informe patrimonio adjunto
```

**IA responde**:
> "REQUIERE ENMIENDA (Falta informe de patrimonio, obligatorio en zona histórica. 
> De otro modo, documentación completa)"

---

### Tipo 3: Ejemplo de RAZONAMIENTO

**Caso**: Analizar por qué se retrasan trámites.

```text
Analiza POR QUÉ se retrasa este trámite (proporciona motivo específico).

EJEMPLOS DE ANÁLISIS:

EJEMPLO 1:
Caso: Licencia ambiental se retrasa 45 días
Análisis: "Retraso por falta de coordinación. 
Área técnica espera informe de especialista (15 días). 
Especialista no fue contactado hasta día 30 del trámite."
Causa raíz: Comunicación interna deficiente

EJEMPLO 2:
Caso: Cambio de uso se aprueba en 20 días (bien)
Análisis: "Se tramitó rápido porque área técnica checó completitud 
en recepción. No hubo devoluciones. Abogada revisó en paralelo 
mientras técnico trabajaba."
Causa raíz: Procesos paralelos + screening inicial

EJEMPLO 3:
Caso: Obra menor se retrasa por datos incompletos
Análisis: "Ciudadano no sabía documentación exacta requerida. 
Sistema envió notificación genérica. Ciudadano devolvió datos 
incorrectos. Ciclo requirió 3 devoluciones."
Causa raíz: Mala comunicación inicial al ciudadano

AHORA analiza:
Caso: Este expediente de vivienda tarda 60 días en recibir resolución.
Cronología:
- Día 1-5: En recepción
- Día 6-20: En análisis técnico (nada pasa)
- Día 21-35: En análisis técnico (nada pasa)
- Día 36-50: En análisis legal
- Día 51-60: Esperando firma

¿Cuál es la causa raíz del retraso?
```

---

## 🎯 Ejercicio: Crear ejemplos

**Propósito**: Practicar la creación de ejemplos efectivos.

**Situación**: Necesitas que la IA corrija emails a ciudadanos.
Los emails deben ser profesionales pero accesibles.

**Tu tarea**: Proporciona 2 ejemplos BUENOS y 1 ejemplo MALO, 
para que la IA aprenda qué esperas.

EMAIL MALO (inclúyelo como ejemplo de lo que NO quieres):
- Demasiado técnico
- Falta de empatía
- Confuso

EMAIL BUENO (inclúyelo como ejemplo de lo que SÍ quieres):
- Profesional pero claro
- Empático pero directo
- Con próximos pasos

---

<details>
<summary>💡 Ejemplo completado</summary>

```text
CORRECCIÓN DE EMAILS A CIUDADANOS

EJEMPLO MALO (NO HAGAS ESTO):
"Estimado Sr./Sra.,

Comunicáronse denegatoria respecto solicitación de licencia ambiental, 
conforme artículos 42-48 LRJSP y plan ordenación territorial. 
Afecciones medioambientales incompatibles con zonificación actual. 
Recurso administrativo ordinario disponible conforme LRJAP.

Cordiales saludos,
Administración"

Problema: Incomprensible, sin contexto, sin empatía.

EJEMPLO BUENO (HAZ ESTO):
"Estimado Sr./Sra.,

Hemos evaluado su solicitud de licencia ambiental para la ubicación 
que indicó. Desafortunadamente, no podemos aprobarla.

¿Por qué? La zona está clasificada como protegida, y la actividad 
que propone no es compatible con esa clasificación según la normativa.

¿Qué puede hacer?
1. Puede presentar un recurso (tiene 30 días desde hoy)
2. Puede considerar otra ubicación fuera de zona protegida
3. Puede contactarnos para una reunión sin compromiso

Estamos aquí para ayudar. Llame al [teléfono] o visite [URL].

Cordiales saludos,
Licencias Urbanísticas"

Lo positivo: Claro, empatético, próximos pasos, contacto fácil.

AHORA corrige este email:
"Se informa que expediente 2024-456 NO PROCEDE. 
Deficiencias administrativas. Devolución solicitante. 
Replazo 10 días. Consulte normativa vigente."
```

</details>

---

## 🚀 Reto avanzado

**Reto 1**: Crea un set de ejemplos que enseñe a la IA "qué es un riesgo legal" 
en contexto administrativo.

- Ejemplo de riesgo legal ALTO
- Ejemplo de riesgo MEDIO
- Ejemplo de BAJO riesgo / sin riesgo

**Reto 2**: ¿Qué pasa si tus ejemplos son incorrectos?

Si proporcionas ejemplos con sesgos o errores, ¿qué hace la IA?
¿Cómo detectarías que tu "entrenamiento" fue incorrecto?

---

## ✅ Qué hemos aprendido

✓ Los ejemplos **retrenean la IA en tiempo real** (few-shot learning)  
✓ **2-3 ejemplos bien elegidos** = óptimo (más = rendimientos decrecientes)  
✓ Tipos: formato, decisión, razonamiento  
✓ Los ejemplos son **tu mejor herramienta** para consistencia  

---

## 📋 Checklist de ejemplos

- [ ] ¿Proporcioné 2-3 ejemplos representativos?
- [ ] ¿Cada ejemplo está claramente etiquetado (bueno/malo, correcto/incorrecto)?
- [ ] ¿Los ejemplos cubren la variedad de casos reales?
- [ ] ¿Un colega vería que esos ejemplos "entrenan bien" la IA?
- [ ] ¿Los ejemplos son propios (reales) o genéricos?
- [ ] ¿Expliqué brevemente por qué cada ejemplo es bueno/malo?

**Siguiente paso**: Cómo refinar respuestas iterativamente. → 09-Iteracion.md
