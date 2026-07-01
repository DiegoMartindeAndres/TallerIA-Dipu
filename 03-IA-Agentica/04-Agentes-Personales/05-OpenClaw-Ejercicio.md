# Tu Primer Agente OpenClaw (Ejercicio Paso a Paso)

## 🎯 Objetivo

Guiarte para crear tu primer agente OpenClaw de forma práctica.

## 📖 Qué vamos a hacer

Crearemos un agente simple pero funcional: **Resume emails de ciudadanos automáticamente**.

Cuando tu ciudad recibe 50 emails/día, tener un resumen de cada uno ahorra tiempo.

## 🔧 Paso 1: Preparación (10 minutos)

### Crea una cuenta en OpenClaw
```
1. Ve a: openclaw.io (o plataforma actual)
2. Regístrate (email, contraseña)
3. Confirma email
4. Listo: Acceso a dashboard
```

### Conecta tu email
```
CONFIGURACIÓN:
┌─ Tipo: Email
├─ Protocolo: IMAP o API Gmail
├─ Email: tu.email@ayuntamiento.es
├─ Contraseña: [aplicación contraseña, no personal]
└─ Cartera: Todos los emails
```

## 📝 Paso 2: Define el Agente (5 minutos)

### Nombre y Descripción
```
NOMBRE: "Resumidor de Emails Ciudadanos"

DESCRIPCIÓN: 
"Este agente lee emails de ciudadanos, 
 extrae información clave, 
 y genera un resumen ejecutivo 
 para respuesta rápida."

OBJETIVO PRINCIPAL:
"Procesar 30 emails/día"
"Generar resumen de máximo 5 líneas por email"
```

### Personalidad y Tono
```
SELECCIONA:
├─ Formalidad: Profesional
├─ Tono: Empático pero eficiente
├─ Idioma: Español de España
└─ Estilo: Resumen ejecutivo
```

## 🎛️ Paso 3: Configura Capacidades (15 minutos)

### Capacidad 1: Lectura de Emails
```
CONEXIÓN:
┌─ Fuente: Tu bandeja de entrada
├─ Carpeta: [Inbox]
├─ Filtro: Remitente = ciudadano@*.es
├─ Frecuencia: Cada hora
└─ Acción: Procesar nuevos
```

### Capacidad 4: Lógica de Procesamiento
```
REGLA 1: Clasificar tipo de email
├─ SI contiene "denuncia" → Tipo: DENUNCIA
├─ SI contiene "solicitud" → Tipo: SOLICITUD
├─ SI contiene "reclamación" → Tipo: RECLAMACIÓN
├─ ELSE → Tipo: CONSULTA

REGLA 2: Extraer información clave
├─ Nombre del ciudadano
├─ Teléfono (si existe)
├─ Asunto principal
├─ Urgencia (clasificar)
└─ Acciones sugeridas

REGLA 3: Generar resumen
├─ Máximo 5 líneas
├─ Puntos clave resaltados
├─ Acción recomendada
└─ Prioridad (ALTA/MEDIA/BAJA)
```

## 📄 Paso 4: Crea el Prompt del Sistema (10 minutos)

El "prompt del sistema" es cómo le dices al agente CÓMO actuar:

```
PROMPT EJEMPLO:

"Eres un asistente administrativo especializado.

Tu tarea: Procesar emails de ciudadanos.

FORMATO DE SALIDA:
┌──────────────────────────────
│ RESUMEN DE EMAIL
├──────────────────────────────
│ Tipo: [DENUNCIA/SOLICITUD/RECLAMACIÓN/CONSULTA]
│ Prioridad: [ALTA/MEDIA/BAJA]
│ Ciudadano: [Nombre]
│ Contacto: [Email/Teléfono]
│ Asunto: [En una línea]
│ Problema: [Explicación breve]
│ Acción sugerida: [Qué hacer]
│ Escalada: [¿Necesita supervisor?]
└──────────────────────────────

REGLAS:
- Sé empático: El ciudadano está frustrado
- Sé conciso: Máximo 100 palabras
- Sé práctico: Sugiere acción clara
- Sé neutral: No juzgues, solo resume
"
```

## 🧪 Paso 5: Prueba con Email Real (10 minutos)

### Email de Prueba
```
FROM: juan@mail.com
SUBJECT: Mi licencia sigue sin resolver

Cuerpo:
"Hola, 
Hace 3 meses solicité licencia para reforma de casa.
Me dijeron 10 días hábiles.
Hoy me dijeron que falta documentación.
Nadie me explicó qué documentación falta.
Estoy muy frustrado.
¿Cuándo la tendré?
Gracias,
Juan García"
```

### Resultado del Agente
```
RESUMEN DE EMAIL
──────────────────────────────
Tipo: RECLAMACIÓN
Prioridad: MEDIA
Ciudadano: Juan García
Contacto: juan@mail.com
Asunto: Licencia pendiente 3 meses, solicita información
Problema: Licencia solicitada hace 3 meses sin resolución. 
          Se le informó de documentación faltante pero sin detalles.
Acción: Consultar BD, identificar qué falta, contactar con Juan.
Escalada: SÍ (fue prometida 10 días, transcurrieron 90)
──────────────────────────────
```

## ⚙️ Paso 6: Configura Salida (5 minutos)

### Dónde guardar los resúmenes

**OPCIÓN A: Email diario**
```
├─ Enviar a: tu@ayuntamiento.es
├─ Asunto: "Resumen diario de ciudadanos - [fecha]"
├─ Frecuencia: 17:00 cada día
└─ Formato: HTML formateado
```

**OPCIÓN B: Carpeta compartida Excel**
```
├─ Guardar en: /shared/ciudadanos/resúmenes.xlsx
├─ Formato: Una fila per email
├─ Actualizar: Automáticamente cada hora
└─ Columnas: Tipo, Prioridad, Nombre, Problema, Acción
```

**OPCIÓN C: Dashboard web**
```
├─ URL: https://agentes.ayuntamiento.es/ciudadanos
├─ Acceso: Restringido (solo tu equipo)
├─ Visualización: Tabla + filtros + búsqueda
└─ Actualizar: Tiempo real
```

## ✅ Paso 7: Activa y Monitorea (5 minutos)

### Activación
```
1. Botón: [ACTIVAR AGENTE]
2. Confirmación: "¿Crear agente en producción?"
3. Respuesta: "SÍ"
4. Estado: "ACTIVO" (color verde)
```

### Monitoreo
```
DASHBOARD MUESTRA:
├─ Emails procesados hoy: 27
├─ Resúmenes generados: 27
├─ Errores: 0
├─ Tiempo promedio: 1,2 segundos por email
├─ Última ejecución: Hace 15 minutos
└─ Próxima: En 45 minutos
```

## 🎯 Ejercicio: Crea TU Primer Agente

Sigue los pasos 1-7 con TU idea:

**Tipo de agente**: ____________________________

1. **Paso 1**: ¿Cuenta creada? SÍ / NO
2. **Paso 2**: ¿Nombre y descripción?
3. **Paso 3**: ¿Capacidades configuradas?
4. **Paso 4**: ¿Prompt creado?
5. **Paso 5**: ¿Prueba realizada?
6. **Paso 6**: ¿Salida configurada?
7. **Paso 7**: ¿Agente activo?

<details>
  <summary>💡 Checklist para Resumidor de Emails (haz clic para ver)</summary>

- [ ] Cuenta OpenClaw creada
- [ ] Email conectado
- [ ] Nombre: "Resumidor de Emails"
- [ ] Conectar bandeja de entrada
- [ ] Prompt creado (resumen format)
- [ ] Probado con 3 emails reales
- [ ] Salida: Excel compartido
- [ ] Agente activado
- [ ] Verificar que procesa nuevos

**Cuando TODO esté checkmarkado: ¡Tu agente funciona!**

</details>

## 🚀 Reto Avanzado

Una vez funciona el básico, amplía:

```
MEJORA 1: Escaladas automáticas
├─ Si Prioridad = ALTA y Tipo = RECLAMACIÓN
├─ Enviar email a: Supervisor
├─ No esperar reporte diario

MEJORA 2: Integración con BD
├─ Agente consulta BD de solicitudes
├─ "Juan tiene licencia desde hace 90 días"
├─ Agente actualiza estado a URGENTE

MEJORA 3: Generación automática de respuestas
├─ Para preguntas simples
├─ Agente genera respuesta de ejemplo
├─ Tú la revisas 10 segundos y envías

MEJORA 4: Aprendizaje
├─ Agente recuerda qué respuestas funcionaron
├─ Próximo email similar: Sugiere respuesta comprobada
```

## ✅ Qué hemos aprendido

1. **OpenClaw es accesible**: 7 pasos, ~1 hora
2. **No requiere código**: Todo interfaz visual
3. **Funciona con datos reales**: Tus emails, tus datos
4. **Es iterable**: Cambios en minutos
5. **Ahorra tiempo real**: Resultado inmediato

---

**Próximo paso**: Ahora que dominaste OpenClaw, ¿qué pasa cuando necesitas más poder? Hermes.
