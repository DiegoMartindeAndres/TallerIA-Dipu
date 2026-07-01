# Las 5 Características Clave de un Agente

## 🎯 Objetivo

Entender profundamente los 5 pilares que hacen funcionar un agente, para que después puedas diseñar tu propio.

## 📖 Qué vamos a aprender

Un agente es un sistema complejo, pero se estructura alrededor de 5 características fundamentales. Si entiendes estas 5, entiendes cómo funcionan todos los agentes del mundo.

## 1️⃣ Autonomía: "Decide Qué Hacer"

### Qué es
La capacidad del agente de **tomar decisiones** sin que le digas cada paso. Le das un objetivo ("procesa estas solicitudes") y el agente decide automáticamente cómo hacerlo.

### Cómo funciona
En lugar de esperar órdenes tuyas:
```
Tú: "Procesa esta solicitud"
Agente: "OK, voy a validar datos... OK, voy a consultar normativa... 
         OK, voy a calcular puntuación... OK, voy a generar resolución..."
```

### Ejemplo Real
**En un ayuntamiento**: Agente que recibe solicitudes. Sin que nadie le diga, automáticamente:
- Lee el tipo de solicitud (subvención, licencia, padrón)
- Recupera normativa aplicable
- Valida documentación requerida
- Sigue el proceso correcto para ese tipo

**Sin autonomía**: Alguien tendría que decir "Este es tipo A, sigue proceso X". Para cada solicitud.
**Con autonomía**: El agente lo descubre solo.

### Beneficio
Tu equipo se enfoca en excepciones y decisiones complejas. El agente maneja lo rutinario.

---

## 2️⃣ Planificación: "Desglosa el Objetivo"

### Qué es
La capacidad de dividir un objetivo complejo en tareas ordenadas, entendiendo dependencias.

### Cómo funciona
Objetivo: "Genera informe mensual de subvenciones"

Sin planificación:
```
Agente: "Hago un informe de subvenciones"
Resultado: Incompleto, datos incorrectos, mucho tiempo
```

Con planificación:
```
Agente piensa automáticamente:
  1. Debo acceder a BD (tengo permisos?)
  2. Extraer datos de enero a febrero (necesito fechas exactas)
  3. Validar datos (alguno corrupto?)
  4. Agrupar por tipo de subvención (tengo categorías?)
  5. Calcular totales por categoría (fórmula?)
  6. Crear gráficos (qué tipo?)
  7. Generar documento PDF (formato?)
  8. Enviar por email a Director (a quién?)

Agente: "Necesito estos pasos en este orden. Empiezo..."
```

### Ejemplo Real
**Procesamiento de expedientes**: El agente sabe que no puede validar firma de solicitante ANTES de verificar que existe en el sistema. Ordena automáticamente: primero identidad, luego datos, luego validaciones.

### Beneficio
Procesos complejos se completan sin errores. No hay "olvidos" de pasos.

---

## 3️⃣ Herramientas: "Accede a Tus Sistemas"

### Qué es
Las herramientas son las conexiones del agente a sistemas reales: bases de datos, APIs, email, documentos.

### Cómo funciona
Un agente sin herramientas es solo un chatbot. Un agente CON herramientas hace cosas reales:

```
Herramientas disponibles:
  - Lectura de base de datos ciudadanos
  - Escritura en base de datos de solicitudes
  - Envío de email
  - Generación de PDFs
  - Lectura de normativa (documentos)
  - Consulta catastro externo (API)
  - Integración tesorería (API)
```

Cuando el agente necesita una acción:
```
Agente: "Necesito enviar email de confirmación"
Agente: Usa herramienta "Envío de email"
Resultado: Email realmente enviado
```

### Ejemplo Real
**Banca municipal**: Agente con herramientas:
- Lee cuenta actual (herramienta BD)
- Consulta transacciones (herramienta historial)
- Valida documentación (herramienta OCR)
- Ejecuta transferencia (herramienta movimiento dinero)

Un agente sin estas herramientas solo podría "contar" qué hacer. Con ellas, LO HACE.

### Beneficio
Tu agente no solo habla, actúa en tus sistemas. Es productivo, no solo informativo.

### Limitaciones Importantes
Las herramientas definen lo que el agente PUEDE hacer. Si no conectas BD, el agente no puede acceder datos. Esto es seguridad: el agente solo hace lo que explícitamente le autorizas.

---

## 4️⃣ Memoria: "Recuerda y Aprende"

### Qué es
La capacidad del agente de **recordar** información entre sesiones y de **aprender** de interacciones anteriores.

### Tipos de Memoria

**Memoria Corto Plazo (Contexto)**
```
Usuario: "Procesa solicitud de Juan Pérez"
Agente: [Lee solicitud de Juan]
Agente: "Listo, procesada"
Usuario: "¿Quién es solicitante?"
Agente: "Juan Pérez" [Lo recuerda de hace 10 segundos]
```

**Memoria Largo Plazo (Persistente)**
```
Mes 1: El agente procesa 100 solicitudes, comete error con categoría "Vivienda"
Agente: Aprende: "Si es vivienda, aplicar normativa X, no Y"

Mes 2: Nueva solicitud de vivienda llega
Agente: [Consulta memoria] "Ah, vivienda... uso normativa X"
Resultado: Correcto. Aprendió del error.
```

### Ejemplo Real
**Atención a ciudadanos**: Ciudadana María ha llamado 5 veces sobre su solicitud. Sin memoria:
```
Llamada 5: "Hola, ¿estado de mi solicitud?"
Chatbot: "¿Cual es tu nombre?"
María: [Frustrada] "¡MARÍA! Como te he dicho 4 veces"
```

Con memoria:
```
Llamada 5: "Hola, ¿estado de mi solicitud?"
Agente: [Consulta memoria] "María! Veo que has llamado 4 veces. 
                             Tu solicitud está en revisión final. 
                             Te notificaremos mañana."
María: "Excelente, gracias"
```

### Beneficio
Experiencia consistente. El usuario no se repite. El agente mejora con el tiempo.

### Privacidad
La memoria debe protegerse (RGPD). El agente recuerda información del usuario, que es dato personal. Necesita encriptación y control de acceso.

---

## 5️⃣ Supervisión: "Humano en Control"

### Qué es
La característica que hace que el agente sea útil en administración pública: **el humano siempre está en control**.

El agente es autónomo PERO dentro de límites. Es como un empleado de confianza que toma decisiones del día a día, pero escalas decisiones críticas a tu supervisor.

### Cómo funciona
```
Decisión rutinaria (< 500€):
  Agente: Decide automáticamente
  
Decisión importante (500€ - 10.000€):
  Agente: "Esto necesita aprobación"
  Humano: Revisa y aprueba/rechaza
  
Decisión crítica (> 10.000€):
  Agente: "Esto necesita autorización de Director"
  Director: Decide
```

### Ejemplo Real
**Gestión de subvenciones**:
- Solicitud de 800€: Agente apruebaautomáticamente (si cumple criterios)
- Solicitud de 5.000€: Sistema alerta a Jefe de Servicio ("¿Apruebo?")
- Solicitud de 50.000€ o dudosa: Director debe revisar personalmente

### Configuración de Supervisión

El agente necesita límites claros:

```
LIMITES DEL AGENTE:
✓ Puede: Validar documentación
✓ Puede: Consultar normativa
✓ Puede: Calcular puntuaciones
✗ NO puede: Denegar sin revisión
✓ Puede: Aprobar hasta 10.000€
✗ NO puede: Aprobar > 50.000€
✓ Puede: Contactar a solicitante
✗ NO puede: Pedir información no contemplada en normativa
```

### Beneficio
Seguridad jurídica. Responsabilidad clara. Confianza en el sistema.

---

## 📚 Ejemplo: Cómo Funcionan las 5 Juntas

Imaginemos un agente en tu ayuntamiento que procesa solicitudes de licencia de obra.

```
SOLICITUD ENTRA AL SISTEMA

[AUTONOMÍA] Agente decide automáticamente:
  "Esto es licencia de obra. Activar protocolo de licencias."

[PLANIFICACIÓN] Agente ordena tasos:
  "Paso 1: Validar solicitante
   Paso 2: Verificar documentación obligatoria
   Paso 3: Consultar normativa urbanística vigente
   Paso 4: Revisar conflictos de interés
   Paso 5: Calcular tasas
   Paso 6: Generar resolución"

[HERRAMIENTAS] Agente ejecuta cada paso:
  - Lee DNI del solicitante (herramienta: BD ciudadanos)
  - Valida documentos (herramienta: OCR, validación de formatos)
  - Consulta PGOU (herramienta: acceso a normativa digitalizada)
  - Revisa BOP (herramienta: API Boletín Oficial)
  - Calcula tarifa (herramienta: tabla de tasas en BD)

[MEMORIA] Agente recuerda de casos pasados:
  "Este solicitante tuvo un problema similar hace 6 meses.
   Asegúrate de solicitar documentación adicional."

[SUPERVISIÓN] Agente toma decisión con límites:
  SI trámite simple (< 1000€ y sin complejidad):
    → Agente APRUEBA automáticamente
  SI mediocomplejo (1000-5000€):
    → Agente propone: "APROBAR" y envía a Jefe
    → Jefe decide en 5 minutos
  SI complejo o duda normativa:
    → Agente escalada: "REVISAR COMPLETO"
    → Abogado municipal revisa

RESULTADO: 
Solicitudes simples: procesadas en 2 horas (automático)
Solicitudes medianas: aprobadas en 1 día (con jefe)
Solicitudes complejas: revisadas por experto (se usan recursos en lo importante)
```

## 🎯 Ejercicio: Diseña Tu Agente

Elige un proceso de tu puesto. Cómo tendría que ser tu agente:

**Proceso elegido**: ___________________________

1. **Autonomía**: ¿Qué decisiones toma solo? ¿Cuáles necesitan confirmación?
2. **Planificación**: ¿Qué pasos son necesarios? ¿En qué orden?
3. **Herramientas**: ¿Qué sistemas necesita acceder?
4. **Memoria**: ¿Qué debe recordar? ¿De qué puede aprender?
5. **Supervisión**: ¿Cuándo necesita tu permiso? ¿Cuándo decide solo?

<details>
  <summary>💡 Ejemplo completo (haz clic para ver)</summary>

**Proceso: Procesar Expedientes de Padrón**

1. **Autonomía**: Agente decide si es cambio de domicilio, alta o baja. Decide qué validaciones aplicar según tipo.

2. **Planificación**: 
   - Paso 1: Leer solicitud
   - Paso 2: Validar DNI/NIE
   - Paso 3: Verificar padrón anterior
   - Paso 4: Validar documentación
   - Paso 5: Comprobar incompatibilidades
   - Paso 6: Generar resolución

3. **Herramientas**: BD padrón, BD documentos, API validación DNI, generador de resoluciones, correo electrónico

4. **Memoria**: Recuerda casos similares de solicitante. Aprende qué documentos frecuentemente faltan por tipo de expediente.

5. **Supervisión**: 
   - Automático: cambios de domicilio simples
   - Supervisión: cambios con discrepancias menores
   - Revisión manual: nuevas altas que puedan generar conflictos

</details>

## 🚀 Reto Avanzado

Ahora que entiendes las 5 características, piensa:
- ¿Cuál es la característica más importante para TU caso de uso? ¿Por qué?
- ¿Cuál sería la más difícil de implementar? ¿Por qué?
- Si solo pudieras elegir 3 de las 5, ¿cuáles elegirías? ¿Qué sacrificarías?

## ✅ Qué hemos aprendido

1. **Autonomía**: El agente decide, no solo sugiere
2. **Planificación**: El agente desglosa problemas complejos
3. **Herramientas**: El agente conecta con tus sistemas reales
4. **Memoria**: El agente aprende y mejora con el tiempo
5. **Supervisión**: El humano siempre está en control

Estas 5 características son lo que diferencia un agente de cualquier otra cosa.

---

**Próximo paso**: Veamos casos de uso prácticos en administración pública. ¿Dónde puedes aplicar esto?
