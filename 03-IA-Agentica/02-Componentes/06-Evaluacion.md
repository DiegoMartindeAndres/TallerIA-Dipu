# Medir Si Tu Agente Funciona

## 🎯 Objetivo

Entender cómo evaluar si un agente está realmente mejorando tu proceso.

## 📖 Qué vamos a aprender

"Implementamos un agente" ≠ "El agente funciona"

Necesitas números. Datos. Pruebas de que realmente está ayudando.

## 📊 Métricas Clave

### Métrica 1: Tiempo

**Antes (Sin agente)**
- Procesar 1 solicitud: 45 minutos (administrativo)
- Procesar 100 solicitudes: 4.500 minutos (75 horas)

**Después (Con agente)**
- Procesar 1 solicitud: 3 minutos (automático)
- Procesar 100 solicitudes: 50 horas (validaciones humanas)

**Mejora**: 33 horas ahorradas/mes

```
MÉTRICA: TIEMPO ECONOMIZADO
Fórmula: (Tiempo_manual - Tiempo_agente) / Tiempo_manual × 100
Ejemplo: (4500 - 300) / 4500 × 100 = 93% más rápido
```

### Métrica 2: Precisión

**Antes**
- Errores detectados: 18 de cada 100 (18% error)
- Errores no detectados: ~5% (no se descubren)
- Error real: ~23%

**Después**
- Errores del agente: 1 de cada 1000 (0.1%)
- Por qué tan bajo: Chequeos automáticos, validaciones múltiples
- Error real: 0.1%

```
MÉTRICA: PRECISIÓN
Fórmula: (Aciertos_correctos / Total) × 100
Ejemplo: 997 correctas de 1000 = 99.7% precisión
```

### Métrica 3: Consistencia

**Antes**
```
Administrativo A: Aplica criterio X de forma laxa
Administrativo B: Aplica criterio X de forma estricta
Resultado: Misma solicitud → Diferente resultado (incoherencia)
```

**Después**
```
Agente: Aplica SIEMPRE la misma regla
Resultado: 100% consistencia
```

```
MÉTRICA: CONSISTENCIA
Medida: Revisión de casos similares
Resultado esperado: Misma decisión en casos idénticos
```

### Métrica 4: Satisfacción del Ciudadano

**Encuesta a ciudadanos**:

```
Antes (Proceso manual):
┌─────────────────────┐
│ ¿Satisfecho?        │
│ SÍ: 60%             │
│ NO: 40%             │
│                     │
│ Quejas principales: │
│ - Demasiado lento   │
│ - Información vaga  │
│ - Inconsistente     │
└─────────────────────┘

Después (Con agente):
┌─────────────────────┐
│ ¿Satisfecho?        │
│ SÍ: 87%             │
│ NO: 13%             │
│                     │
│ Quejas principales: │
│ - Ninguna relevante │
│ - Algunos: "Muy     │
│   automático"       │
└─────────────────────┘
```

```
MÉTRICA: NPS (Net Promoter Score)
Fórmula: (% Promotores - % Detractores)
Ejemplo: (87% - 13%) = +74 NPS (Excelente)
```

### Métrica 5: Costo

```
ANTES:
- 2 administrativos: €40.000/año cada uno = €80.000
- Software: €3.000
- Infraestructura: €2.000
TOTAL: €85.000/año

DESPUÉS:
- 0,5 administrativo (el otro hace cosas más valiosas)
- Software de agente: €5.000
- Infraestructura mejorada: €4.000
TOTAL: €24.000/año

AHORRO: €61.000/año
```

```
MÉTRICA: ROI (Retorno de Inversión)
Fórmula: (Ahorros - Inversión) / Inversión × 100
Ejemplo: (61.000 - 15.000) / 15.000 × 100 = 307% ROI
Significado: Por cada €1 invertido, ganas €3,07
```

## 🎯 Auditoría de Decisiones

No confíes ciegamente. AUDITA.

### Cómo Auditar

```
CADA MES, REVISA:

1. Decisiones automáticas (muestreo al azar 1%)
   - 1 de cada 100 decisiones automáticas
   - Revisar si fue correcta
   - Si falló: ¿Por qué? ¿Fallo del agente o caso especial?

2. Decisiones que escalaron
   - 100% de escaladas (son pocas)
   - ¿Fueron correctas? ¿El agente escaló cuando debía?

3. Casos límite
   - Decisiones donde el agente estuvo "en la línea"
   - ¿Fue correcto el lado que eligió?

4. Errores reportados
   - Ciudadanos que se quejaron
   - Revisar si el agente cometió error o el ciudadano mal entendió
```

### Ejemplo de Auditoría Mensual

```
MES: Junio 2024
Agente procesó: 250 solicitudes

MUESTRA AUDITORÍA (1%):
┌──────────────────────────────────┐
│ Decisión #127 - Juan García      │
│ Solicitud: Subvención €800       │
│ Agente decidió: APROBADA         │
│                                  │
│ Auditor (TÚ) revisa:             │
│ ✓ Documentación completa? SÍ     │
│ ✓ Criterios cumplidos? SÍ        │
│ ✓ Monto apropiado? SÍ            │
│ ✓ Decisión correcta? SÍ          │
│                                  │
│ VEREDICTO: OK ✓                  │
└──────────────────────────────────┘

┌──────────────────────────────────┐
│ Decisión #203 - Rosa López       │
│ Solicitud: Subvención €1.200     │
│ Agente decidió: PENDIENTE (falta │
│                 documento X)      │
│                                  │
│ Auditor revisa:                  │
│ ✓ Documento realmente requerido? │
│   (Consulto normativa)           │
│   SÍ, normativa lo requiere      │
│ ✓ Decisión correcta? SÍ          │
│                                  │
│ VEREDICTO: OK ✓                  │
└──────────────────────────────────┘

RESULTADO MENSUAL:
- Auditadas: 3 decisiones
- Correctas: 3
- Precisión auditada: 100%
```

## 📈 Dashboard de Seguimiento

Un buen agente tiene un "dashboard" visible:

```
╔════════════════════════════════════════════════════╗
║         DASHBOARD AGENTE SUBVENCIONES              ║
║                   Junio 2024                       ║
╠════════════════════════════════════════════════════╣
║                                                    ║
║ VELOCIDAD                                          ║
║ Solicitudes procesadas: 250  |  Target: 200   ✓ OK║
║ Tiempo promedio: 3.2 min     |  Target: 5     ✓ OK║
║                                                    ║
║ CALIDAD                                            ║
║ Precisión: 99.6%             |  Target: 98%   ✓ OK║
║ Errores: 1 de 250            |  Target: 2      ✓ OK║
║                                                    ║
║ SATISFACCIÓN                                       ║
║ Ciudadanos satisfechos: 94%  |  Target: 90%   ✓ OK║
║ NPS Score: +78               |  Target: +60   ✓ OK║
║                                                    ║
║ COSTO                                              ║
║ Ahorro mensual: €5.100       |  Target: €5k   ✓ OK║
║ ROI acumulado: +315%         |  Target: +300% ✓ OK║
║                                                    ║
║ TENDENCIA                                          ║
║ vs Mes anterior: ↑ 8% velocidad, ↑ 2% calidad   ✓ ║
║                                                    ║
╚════════════════════════════════════════════════════╝
```

## 🎯 Ejercicio: Define KPIs Para Tu Agente

**Proceso**: ___________________________

Define 5 KPIs (Key Performance Indicators):

1. **KPI 1 - Velocidad**
   - Métrica: 
   - Valor actual (sin agente):
   - Valor objetivo (con agente):

2. **KPI 2 - Calidad**
   - Métrica:
   - Valor actual:
   - Valor objetivo:

3. **KPI 3 - Satisfacción**
   - Métrica:
   - Valor actual:
   - Valor objetivo:

4. **KPI 4 - Eficiencia**
   - Métrica:
   - Valor actual:
   - Valor objetivo:

5. **KPI 5 - Costo/ROI**
   - Métrica:
   - Valor actual:
   - Valor objetivo:

<details>
  <summary>💡 Ejemplo: Procesamiento de Licencias (haz clic para ver)</summary>

1. **Velocidad**
   - Métrica: Días promedio resolución
   - Actual: 14 días
   - Objetivo: 3 días

2. **Calidad**
   - Métrica: % de licencias sin errores legales
   - Actual: 85%
   - Objetivo: 98%

3. **Satisfacción**
   - Métrica: NPS score
   - Actual: +35
   - Objetivo: +70

4. **Eficiencia**
   - Métrica: Horas administrativo por licencia
   - Actual: 2 horas
   - Objetivo: 0,2 horas

5. **ROI**
   - Métrica: Ahorro anual
   - Actual: €0 (no existe agente)
   - Objetivo: €45.000/año

</details>

## 🚀 Reto Avanzado

**Falsos Positivos en Métricas**:

Cuidado: A veces las métricas mentir.

```
EJEMPLO:
Métrica: "El agente procesa 95% solicitudes automáticas"
Interpretación naïve: "¡Excelente! Funciona casi solo!"

REALIDAD:
El 95% es porque el agente ESCALA TODO que es complejo.
Está evitando trabajo duro, no resolviéndolo.

MEJOR MÉTRICA:
"% de solicitudes resueltas CORRECTAMENTE automáticas"
→ 75% automático sin escaladas = Bueno
→ 95% automático pero 30% mal = Malo
```

¿Qué otras métricas podrían ser engañosas en tu caso?

## ✅ Qué hemos aprendido

1. **La velocidad es importante, pero no todo**: Precisión importa igual
2. **La satisfacción del ciudadano es el test real**: Las métricas internas son secundarias
3. **Audita regularmente**: No confíes ciegamente
4. **ROI es el lenguaje de la administración**: Muestra ahorro = Más presupuesto futuro
5. **Las métricas pueden engañar**: Interpreta con cuidado

---

**Próximo paso**: Ahora que conoces los componentes, veamos casos prácticos. Agentes en acción.
