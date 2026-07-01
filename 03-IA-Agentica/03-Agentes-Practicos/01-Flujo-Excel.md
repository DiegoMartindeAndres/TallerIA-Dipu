# Agente Procesando Flujos Excel: El Capstone del Taller

## 🎯 Objetivo

Ver cómo un agente automatiza el workflow que aprendiste en el Bloque 1: calificaciones → cálculos → reportes.

## 📖 Qué vamos a aprender

Recuerda: En el Bloque 1 aprendiste sobre datos, Excel, y fórmulas. Un humano hace esto manualmente.

Ahora: Un agente lo hace automáticamente. 24/7. Sin errores.

## 📚 El Caso: Calificaciones de Solicitudes de Subvención

### El Proceso Antes (Manual)

```
LUNES 09:00
├─ Administrativo descarga Excel de solicitudes recibidas
├─ Abre cada PDF: 50 solicitudes
├─ Extrae manualmente: nombre, monto, criterios
├─ Copia a Excel
├─ Aplica fórmulas: =SUMA, =SI, =BUSCARV
├─ Genera gráficos
├─ Crea informe Word
├─ Envía por email

TIEMPO: 8 horas
ERRORES: ~10% (copiar mal, fórmulas olvidadas)
FRECUENCIA: Semanal
```

### El Proceso Después (Con Agente)

```
CADA DÍA A LAS 18:00
├─ Agente: ¿Hay solicitudes nuevas?
├─ SÍ → Descarga listado
├─ Lee cada PDF (OCR automático)
├─ Extrae: nombre, monto, criterios
├─ Consulta BD normativa (¿aplica? ¿No aplica?)
├─ Calcula: =SUMA fórmulas
├─ Genera puntuación
├─ Crea gráficos
├─ Redacta informe
├─ Envía por email a director

TIEMPO: 5 minutos
ERRORES: 0,1%
FRECUENCIA: Diaria (ahora tienes datos frescos)
```

## 🔄 Flujo Detallado: De Solicitudes a Reportes

### Paso 1: Descarga y Lectura
```
Agente: "¿Hay solicitudes nuevas hoy?"
[Consulta carpeta compartida / email / sistema]
Encuentra: 7 PDFs nuevos

Agente: "Voy a leerlos todos"
[OCR automático en cada PDF]
Resultado: 
  Solicitud 1: Ana García, €1.500, rural
  Solicitud 2: Juan Pérez, €2.000, urbano
  ... (7 total)
```

### Paso 2: Validación y Extracción
```
Para CADA solicitud:
├─ ¿Documentación completa? SÍ/NO
├─ ¿Solicitante existe? SÍ/NO
├─ ¿Hay conflictos? SÍ/NO
└─ Extrae: Datos clave en tabla

Resultado: Tabla con 7 filas
```

### Paso 3: Cálculo de Puntuación
```
Para CADA solicitud, agente calcula:

Criterio 1: Situación económica
  → Ingresos: €15.000/año
  → Tope: €20.000
  → Puntos: 20 (dentro de tope)

Criterio 2: Ubicación
  → Zona rural: +15 puntos
  → Zona desfavorecida: +10 puntos

Criterio 3: Prioridad especial
  → Joven: +5
  → Mujer: +5

TOTAL: 20 + 15 + 5 + 5 = 45 puntos

ESTO SE REPITE PARA LAS 7 SOLICITUDES
```

### Paso 4: Generación de Excel
```
Agente: "Crearé Excel con resultados"

COLUMNAS:
├─ Nombre
├─ Monto solicitado
├─ Puntuación
├─ Categoría (Buena/Media/Baja)
├─ Recomendación (Aprobar/Evaluar/Rechazar)
└─ Estado

FILAS (ejemplo):
Ana García      €1.500    45    Buena    Aprobar     OK
Juan Pérez      €2.000    32    Media    Evaluar     OK
Rosa López      €800      52    Excelente Aprobar    OK
...

TOTAL: 7 solicitudes clasificadas
```

### Paso 5: Gráficos Automáticos
```
Agente genera:

GRÁFICO 1: Distribución por categoría
  Excelentes: 2
  Buenas: 3
  Medias: 2
  [Gráfico circular]

GRÁFICO 2: Montos solicitados vs puntuación
  [Gráfico dispersión]

GRÁFICO 3: Tendencia (si es semanal/mensual)
  Semana 1: 45 promedio
  Semana 2: 48 promedio
  Semana 3: 50 promedio
  [Gráfico línea: tendencia creciente]
```

### Paso 6: Informe Automático
```
Agente genera: Informe PDF

CONTENIDO:
═════════════════════════════════════════
Resumen de Solicitudes Procesadas
Período: [fecha]
═════════════════════════════════════════

TOTAL PROCESADAS: 7
- Completas: 7 ✓
- Incompletas: 0

DISTRIBUCIÓN:
- Ubicación rural: 5 (71%)
- Ubicación urbana: 2 (29%)

PUNTUACIÓN PROMEDIO: 44,4/100
RANGO: 32-52 puntos

RECOMENDACIONES:
✓ 4 solicitudes: APROBAR (puntuación > 40)
? 2 solicitudes: EVALUAR (puntuación 30-40)
✗ 1 solicitud: REVISAR (dudas normativas)

IMPACTO PRESUPUESTARIO:
Monto total solicitado: €10.300
Monto recomendado a aprobar: €8.500
Gasto estimado: 82% del presupuesto disponible

PRÓXIMOS PASOS:
1. Jefe revisa recomendaciones
2. Decisiones finales
3. Notificación a solicitantes
```

### Paso 7: Envío y Notificación
```
Agente:
├─ Adjunta Excel con detalles
├─ Adjunta PDF con informe
├─ Adjunta gráficos
├─ Envía a: Director
├─ CC: Jefe de Servicio
├─ Actualiza BD: "Reportes generados el [fecha]"

DESTINATARIOS RECIBEN:
Email: "Tu informe semanal de solicitudes"
Archivos: 3 (Excel, PDF, gráficos)
Tiempo para leer y decidir: ~15 minutos
```

## 📊 Comparación: Tú vs Agente

| Aspecto | Tú (Manual) | Agente |
|---------|---------|--------|
| Tiempo | 8 horas | 5 minutos |
| Errores | ~10% | 0,1% |
| Frecuencia | Semanal (si hay tiempo) | Diaria (siempre) |
| Información fresca | 1 semana de retraso | Hoy |
| Formato | Excel + Word (inconsistente) | Estándar (consistente) |
| Escalabilidad | Máx 50 solicitudes | 1.000+ sin problema |
| De noche/festivos | No | SÍ |

## 🎯 Ejercicio: Tu Flujo Excel

Piensa en un proceso tuyo que usa Excel frecuentemente:

**Proceso**: ___________________________

1. **¿Qué datos necesitas?**
   - 

2. **¿Qué cálculos haces?**
   - 

3. **¿Qué gráficos generas?**
   - 

4. **¿A quién le envías?**
   - 

5. **¿Cuánto tiempo tardas?**
   - 

<details>
  <summary>💡 Ejemplo: Control de Asistencia (haz clic para ver)</summary>

1. **¿Qué datos necesitas?**
   - Registro de entrada/salida de empleados

2. **¿Qué cálculos haces?**
   - Horas trabajadas = Salida - Entrada
   - Horas extra = (Horas trabájadas - 8) si > 8h
   - Total mes = SUMA horas día

3. **¿Qué gráficos generas?**
   - Horas por empleado
   - Horas extra por mes
   - Absencias

4. **¿A quién le envías?**
   - RRHH, Nómina

5. **¿Cuánto tiempo tardas?**
   - 3 horas/mes

Un agente lo haría en 5 minutos, todos los días.

</details>

## 🚀 Reto Avanzado

Aquí está lo potente:

**Con el agente, tu trabajo cambia:**

Antes: Eres "quien genera el Excel"
Después: Eres "quien interpreta datos y toma decisiones"

**Nueva pregunta**:

"Los datos muestran que solicitudes rurales tienen 5 puntos más promedio. ¿Debemos ajustar criterios? ¿Es jusicia o sesgo?"

Eso es lo que hará tu jefe con los datos del agente.

## ✅ Qué hemos aprendido

1. **Excel + OCR + Fórmulas = Automatización**: El agente es tu asistente de datos
2. **La velocidad es libertad**: Datos diarios = Decisiones mejor informadas
3. **Menos tiempo en "generar", más en "analizar"**: El valor está en la interpretación
4. **Un flujo que tardaba 8 horas → 5 minutos**: Esa es la realidad de los agentes

---

**Próximo paso**: Documentos en lugar de Excel. Agentes que leen y clasifican.
