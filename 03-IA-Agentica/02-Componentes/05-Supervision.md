# El Papel Crucial de la Supervisión Humana

## 🎯 Objetivo

Comprender cómo mantienes el control sobre el agente mediante supervisión.

## 📖 Qué vamos a aprender

Esto es importante: **Un agente es autónomo, pero NUNCA sin supervisión humana.**

La pregunta no es "¿Es el agente autónomo?" → SÍ
La pregunta es "¿Es seguro sin vigilancia?" → NO

La supervisión es lo que hace que un agente sea útil en administración pública.

## 🎯 La Realidad de la Autonomía

```
Autonomía ≠ "Hace lo que quiere"

Autonomía = "Toma decisiones dentro de guardrails claros"

COMPARACIÓN:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Empleado humano (Juana):
- Autonomía: Juana decide cómo procesar solicitudes
- Control: Pero solo hasta €5.000. Para >€5.000, pregunta al jefe
- Límite: No puede cambiar normativa, solo aplicarla

Agente:
- Autonomía: Agente decide cómo procesar solicitudes
- Control: Pero solo hasta €5.000. Para >€5.000, pide aprobación
- Límite: No puede cambiar normativa, solo aplicarla
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

La diferencia: Juana necesita pausa para pensar. El agente es instantáneo. Pero la lógica es idéntica.

## 🛡️ Qué Debe Revisar Siempre un Humano

### Decisiones sobre Dinero (Alto Valor Financiero)
```
POLÍTICA DE SUPERVISIÓN:
- Subvención < €1.000 → Agente APRUEBA automático
- Subvención €1.000-€5.000 → Agente PROPONE, jefe APRUEBA (5 min)
- Subvención > €5.000 → Humano REVISA completamente (15 min)
- Ayuda excepcional > €10.000 → Director AUTORIZA personalmente
```

### Decisiones sobre Derechos del Ciudadano
```
Ejemplos:
- ¿Puede denegarle acceso a un documento? → Humano revisa
- ¿Puede aprobar/rechazar una solicitud? → Humano verifica criterios
- ¿Puede cambiar plazos? → Humano autoriza

Razonamiento:
Si el agente comete error, el ciudadano puede estar meses sin su derecho.
Por eso, revisión humana es obligatoria.
```

### Decisiones con Datos Sensibles
```
Datos que requieren supervisión especial:
- Salud (si se menciona accidentalmente)
- Situación económica crítica
- Información familiar
- Casos de vulnerabilidad

PROTOCOLO:
Si agente detecta dato sensible inesperado:
  → No lo guarda
  → Alerta a humano
  → Humano decide si es necesario
```

### Decisiones que Afectan a Terceros
```
Ejemplo: Licencia de obra
- Decisión del agente afecta a vecinos
- ¿Y si el agente se equivoca?

PROTOCOLO:
- Agente procesa normalmente
- Pero notificación a vecinos: SIEMPRE supervisada por humano
- Jefe verifica antes de enviar "Tu licencia fue denegada"
```

## ⚠️ Límites de Gasto, Criticidad, Datos Sensibles

### Configuración de Límites

```
PLANTILLA DE GUARDRAILS:

┌─────────────────────────────────────┐
│ LÍMITES DEL AGENTE - Municipio XYZ  │
├─────────────────────────────────────┤
│                                     │
│ AUTORIDAD FINANCIERA:               │
│ ✓ Puede gastar: < €1.000            │
│ ✗ NO puede gastar: > €1.000         │
│                                     │
│ CRITICIDAD:                         │
│ ✓ Decisiones rutinarias: Automático │
│ ✗ Decisiones importantes: Revisión  │
│ ✗ Decisiones críticas: Autorización │
│                                     │
│ DATOS SENSIBLES:                    │
│ ✓ Puede procesar: Datos generales   │
│ ✗ NO puede procesar: Datos salud    │
│                                     │
│ HORARIO:                            │
│ ✓ Activo: 08:00-20:00               │
│ ✗ Pausa: 20:00-08:00 (revisar x día)│
│                                     │
│ EXCEPCIONES:                        │
│ • Si detecta patrón anómalo: ALERTA │
│ • Si combinación rara: ESCALADA     │
│                                     │
└─────────────────────────────────────┘
```

## 🔔 Alertas y Aprobaciones

### Tipos de Alertas

**ALERTA NORMAL** (Informativo)
```
Usuario recibe: Email
Contenido: "He procesado 15 solicitudes hoy. 
           Todas aprobadas. Aquí está el resumen."
Acción: El usuario revisa cuando quiera (no urgente)
```

**ALERTA IMPORTANTE** (Requiere Revisión)
```
Usuario recibe: Email + Notificación en sistema
Contenido: "Solicitud de €5.000 lista para tu aprobación. 
           [REVISAR]"
Acción: Usuario debe revisar en 24 horas
```

**ALERTA CRÍTICA** (Requiere Autorización Inmediata)
```
Usuario recibe: Email URGENTE + Teléfono (SMS)
Contenido: "Solicitud de €50.000 con dudas legales. 
           Necesito Director. URGENTE"
Acción: Director debe autorizar en 1 hora
```

### Flujo de Aprobación

```
SOLICITUD LLEGA AL AGENTE
    ↓
AGENTE ANALIZA
    ↓
┌─────────────────────────────────┐
├─ ¿Es automático? ────────────────┤
│      SÍ → APRUEBA directamente   │
│      NO → Sigue...              │
└─────────────────────────────────┘
    ↓
┌─────────────────────────────────┐
├─ ¿Es importante pero normal?────┤
│      SÍ → Envía a JEFE          │
│          Jefe recibe: "¿Apruebo?"│
│          Jefe decide en 5 min    │
│      NO → Sigue...              │
└─────────────────────────────────┘
    ↓
┌─────────────────────────────────┐
├─ ¿Es crítico o dudoso?──────────┤
│      SÍ → Escala a DIRECTOR     │
│          Director: "Revisar"     │
│          Director decide en 24h  │
│      NO → Sigue...              │
└─────────────────────────────────┘
    ↓
┌─────────────────────────────────┐
├─ ¿Es excepcional/desconocido?──┤
│      SÍ → Pide AUTORIZACIÓN     │
│          Cuerpo colegiado        │
│          Decisión: 48-72h        │
│      NO → Sigue...              │
└─────────────────────────────────┘
    ↓
ACCIÓN EJECUTADA O RECHAZADA
```

## 📚 Ejemplo: Agente que Necesita Autorización

```
SOLICITUD: Juan pide subvención de €3.500 para herramientas

ANÁLISIS DEL AGENTE:
├─ ¿Existe Juan? SÍ ✓
├─ ¿Documentación completa? SÍ ✓
├─ ¿Elegible? SÍ ✓
├─ ¿Puntuación? 45 puntos (buena)
├─ ¿Monto apropiado? €3.500 propuesto por norma
└─ ¿Hay riesgo? NO ✗

PERO:
El agente está configurado:
- AUTOMÁTICO hasta €1.000
- JEFE hasta €5.000

ACCIÓN:
┌──────────────────────────────┐
│ PROPUESTA DE APROBACIÓN      │
│                              │
│ Solicitante: Juan García     │
│ Monto: €3.500                │
│ Puntuación: 45/100           │
│ Estado: PROPUESTO            │
│                              │
│ [BOTÓN: APROBAR]             │
│ [BOTÓN: REVISAR]             │
│ [BOTÓN: RECHAZAR]            │
└──────────────────────────────┘

JEFE RECIBE:
- Email con enlace a decisión
- Tarda 3 minutos en revisar
- Haz clic en "APROBAR"
- Agente recibe autorización
- Automáticamente genera resolución y notifica

RESULTADO: €3.500 aprobados en < 1 hora (vs 3 días manual)
```

## 🎯 Ejercicio: Define Supervisión para Tu Agente

**Proceso**: ___________________________

Completa:

1. **¿Qué se aprueba automáticamente (sin humano)?**
   - 

2. **¿Qué necesita aprobación de Jefe (en 24h)?**
   - 

3. **¿Qué necesita aprobación de Director (en 48h)?**
   - 

4. **¿Qué necesita Cuerpo colegiado (decisión comunitaria)?**
   - 

5. **¿Qué datos NO PUEDE tocar el agente?**
   - 

<details>
  <summary>💡 Ejemplo: Gestión de Subvenciones (haz clic para ver)</summary>

1. **¿Qué se aprueba automáticamente?**
   - Subvenciones < €500, documentación completa, solicitante sin antecedentes

2. **¿Qué necesita Jefe (24h)?**
   - Subvenciones €500-€2.000

3. **¿Qué necesita Director (48h)?**
   - Subvenciones €2.000-€10.000, O dudas normativas

4. **¿Qué necesita cuerpo colegiado?**
   - Subvenciones > €10.000, O casos excepcionales

5. **¿Qué datos NO PUEDE tocar?**
   - Información de salud, datos de menores, información bancaria completa

</details>

## 🚀 Reto Avanzado

**Escenario de Riesgo**:

Imagina que el agente detecta un patrón:
- Juan ha solicitado 10 subvenciones este mes
- Todas de €999 (justo bajo el límite automático)
- Todas aprobadas sin revisión

¿Qué hace?

```
OPCIÓN A: Continuar (es legal)
OPCIÓN B: Alertar (puede ser fraude coordinado)
OPCIÓN C: Escalar automáticamente

RESPUESTA CORRECTA: C
"Patrón detectado: Múltiples solicitudes de mismo solicitante 
 justo bajo límite. Esto REQUIERE revisión manual"

El agente no juzga, pero alerta. El humano decide.
```

## ✅ Qué hemos aprendido

1. **Autonomía ≠ Sin Supervisión**: El agente es autónomo dentro de límites
2. **Hay 4 niveles de decisión**: Automático, Jefe, Director, Cuerpo
3. **Los límites se configuran claramente**: Dinero, criticidad, datos sensibles
4. **Las alertas son cruciales**: El agente avisa, el humano decide
5. **La confianza se gana**: No empiezas con agente con todo acceso

---

**Próximo paso**: ¿Cómo sabemos si el agente está funcionando bien? Evaluación.
