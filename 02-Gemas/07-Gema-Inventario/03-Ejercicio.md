# Ejercicio: Alertas Automáticas de Mantenimiento Preventivo

## El Caso: Sistema de Alertas para Flota Municipal

**Contexto:**
Eres el responsable de mantenimiento de la flota municipal. El Ayuntamiento tiene 12 vehículos que usas diariamente. Hace poco tuviste un problema: el seguro de un camión venció sin que lo supieras, y durante 3 días la flota estuvo parcialmente inmobilizada.

Tu jefe te pide crear un sistema automático de alertas para evitar que vuelva a pasar.

## Parte 1: Datos de la Flota

Revisa esta información sobre los vehículos:

```
📋 FLOTA MUNICIPAL - ESTADO ACTUAL
Fecha hoy: 15 de marzo de 2024

VEHÍCULOS TURISMOS (4 unidades):
1. Turismo V-001 (Renault Clio)
   - Placa: 1234ABC
   - Año: 2018 (6 años)
   - Seguro: Vence 30 de marzo (¡15 días!)
   - ITV: Vence 15 de abril (¡31 días!)
   - Último mantenimiento: 2024-02-28
   - Km: 128.000
   - Responsable: Juan García (Policía Local)
   - Estado: Operativo

2. Turismo V-002 (Seat Ibiza)
   - Placa: 5678DEF
   - Año: 2019 (5 años)
   - Seguro: Vence 10 de mayo (¡56 días!)
   - ITV: Vence 20 de mayo (¡66 días!)
   - Último mantenimiento: 2024-01-15
   - Km: 95.000
   - Responsable: María López (Servicios Sociales)
   - Estado: Operativo

3. Turismo V-003 (Ford Focus)
   - Placa: 9876XYZ
   - Año: 2020 (4 años)
   - Seguro: Vence 5 de febrero (¡VENCIDO HACE 38 DÍAS!)
   - ITV: Vence 15 de febrero (¡VENCIDA HACE 28 DÍAS!)
   - Último mantenimiento: 2023-12-10
   - Km: 82.000
   - Responsable: Carlos Rodríguez (Juzgado)
   - Estado: NO DEBE USARSE - VENCIDO
   - ALERTA CRÍTICA: Vehículo en riesgo legal

4. Turismo V-004 (Peugeot 208)
   - Placa: 4567GHI
   - Año: 2021 (3 años)
   - Seguro: Vence 25 de junio (¡102 días!)
   - ITV: Vence 3 de julio (¡110 días!)
   - Último mantenimiento: 2024-03-05
   - Km: 45.000
   - Responsable: Ana Martínez (Biblioteca)
   - Estado: Operativo

CAMIONES (4 unidades):
5. Camión C-001 (Iveco)
   - Placa: 2345JKL
   - Año: 2016 (8 años)
   - Seguro: Vence 20 de marzo (¡5 DÍAS - CRÍTICO!)
   - ITV: Vence 25 de marzo (¡10 DÍAS - CRÍTICO!)
   - Último mantenimiento: 2024-02-15
   - Km: 189.000
   - Responsable: Servicios de Limpieza
   - Estado: Operativo - ALERTA MÁXIMA

6. Camión C-002 (Man)
   - Placa: 6789MNO
   - Año: 2017 (7 años)
   - Seguro: Vence 8 de abril (¡24 días!)
   - ITV: Vence 15 de abril (¡31 días!)
   - Último mantenimiento: 2024-01-20
   - Km: 156.000
   - Responsable: Servicios de Limpieza
   - Estado: Operativo

7. Camión C-003 (Mercedes)
   - Placa: 0123PQR
   - Año: 2018 (6 años)
   - Seguro: Vence 12 de mayo (¡58 días!)
   - ITV: Vence 20 de mayo (¡66 días!)
   - Último mantenimiento: 2024-02-28
   - Km: 145.000
   - Responsable: Servicios de Mantenimiento
   - Estado: Operativo

8. Camión C-004 (Scania)
   - Placa: 4567STU
   - Año: 2014 (10 años)
   - Seguro: Vence 3 de junio (¡80 días!)
   - ITV: Vence 10 de junio (¡87 días!)
   - Último mantenimiento: 2024-01-10 (¡2 meses sin revisión!)
   - Km: 210.000
   - Responsable: Servicios de Obras
   - Estado: Operativo - PERO MANTENIMIENTO ATRASADO

VEHÍCULOS ESPECIALES (2 unidades):
9. Grúa G-001 (Palfinger)
   - Placa: 8901VWX
   - Año: 2015 (9 años)
   - Seguro: Vence 28 de marzo (¡13 DÍAS!)
   - ITV: Vence 5 de abril (¡21 DÍAS!)
   - Certificado de grúa: Vence 30 de junio (válido, 107 días)
   - Último mantenimiento: 2024-02-10
   - Km: 98.000
   - Responsable: Servicios de Obras
   - Estado: Operativo - ALERTA

10. Volquete V-001 (Scania)
    - Placa: 2345YZA
    - Año: 2017 (7 años)
    - Seguro: Vence 15 de septiembre (¡184 DÍAS - TRANQUILO!)
    - ITV: Vence 22 de octubre (¡221 DÍAS - TRANQUILO!)
    - Último mantenimiento: 2024-03-10
    - Km: 167.000
    - Responsable: Servicios de Obras
    - Estado: Operativo

MOTOCICLETAS (2 unidades):
11. Moto M-001 (Honda CB500)
    - Placa: 5678BCD
    - Año: 2019 (5 años)
    - Seguro: Vence 31 de marzo (¡16 DÍAS!)
    - ITV: Vence 8 de abril (¡24 DÍAS!)
    - Último mantenimiento: 2024-02-05
    - Km: 34.000
    - Responsable: Policía Local
    - Estado: Operativo

12. Moto M-002 (Yamaha MT-07)
    - Placa: 9012EFG
    - Año: 2020 (4 años)
    - Seguro: Vence 2 de mayo (¡48 DÍAS!)
    - ITV: Vence 10 de mayo (¡56 DÍAS!)
    - Último mantenimiento: 2024-01-25
    - Km: 28.000
    - Responsable: Policía Local
    - Estado: Operativo
```

## Parte 2: Tu Análisis

Antes de ver la solución, responde:

### Pregunta 1: Alertas inmediatas
¿Qué vehículos necesitan acción ESTA SEMANA (próximos 7 días)?

**Tu respuesta:**
```
[Lista vehículos con acción urgente]
```

### Pregunta 2: Alertas de atención (próximas 2 semanas)
¿Cuáles vencerán en los próximos 14 días?

**Tu respuesta:**
```
[Lista con fechas]
```

### Pregunta 3: Proyección trimestral
¿Cuántos vehículos necesitarán renovación en Q2 (abril-junio)?

**Tu respuesta:**
```
[Resumen trimestral]
```

### Pregunta 4: Problemas operacionales
¿Hay vehículos que NO DEBEN USARSE hoy?

**Tu respuesta:**
```
[Vehículos no operativos + razón]
```

---

## Solución Guiada

<details>
<summary>📋 Ver análisis completo</summary>

### RESPUESTA 1: Alertas inmediatas (próximos 7 días)

🚨 **CRÍTICO - ACCIÓN HOY:**

1. **Turismo V-003 (placa 9876XYZ)**
   - Seguro: VENCIDO hace 38 días
   - ITV: VENCIDA hace 28 días
   - **INMEDIATAMENTE:** Comunicar a Carlos Rodríguez que NO PUEDE usar este vehículo
   - **ACCIÓN:** Contactar a compañía seguros para renovación URGENTE
   - **RIESGO:** Circulación sin seguro = multa + responsabilidad civil + inmobilización

2. **Camión C-001 (placa 2345JKL)**
   - Seguro vence: 20 de marzo (5 DÍAS)
   - ITV vence: 25 de marzo (10 DÍAS)
   - **ACCIÓN:** Contactar compañía seguros HOY para renovación
   - **ACCIÓN:** Solicitar cita para ITV ESTA SEMANA
   - **RIESGO:** Vehículo operativo en limpieza, no puede detenerse

⚠ **ALTO - ESTA SEMANA:**

3. **Grúa G-001 (placa 8901VWX)**
   - Seguro vence: 28 de marzo (13 días)
   - ITV vence: 5 de abril (21 días)
   - Certificado de grúa: Válido hasta 30 de junio
   - **ACCIÓN:** Contactar seguros para renovación próxima semana

4. **Moto M-001 (placa 5678BCD)**
   - Seguro vence: 31 de marzo (16 días)
   - ITV vence: 8 de abril (24 días)
   - **ACCIÓN:** Planificar renovación para próxima semana

### RESPUESTA 2: Alertas próximas 14 días

**Semana 2 (18-24 marzo):**
- Turismo V-001: Seguro 30 marzo (15 días)
- Moto M-001: Seguro 31 marzo (16 días)

**Semana 3 (25-31 marzo):**
- Camión C-001: Seguro 20 marzo ✓ YA PASÓ (pero aún está en la lista de críticos)
- Camión C-001: ITV 25 marzo (10 días) ✓ CRÍTICO

### RESPUESTA 3: Proyección trimestral (Q2: Abril-Junio)

**Mes de Abril:**
- 6 renovaciones de seguro
- 6 renovaciones de ITV
- Costo estimado: ~6.000€ (100€/renovación aprox)

**Mes de Mayo:**
- 4 renovaciones de seguro
- 4 renovaciones de ITV
- Costo estimado: ~4.000€

**Mes de Junio:**
- 2 renovaciones de seguro
- 2 renovaciones de ITV
- 1 renovación de Certificado de Grúa: 300€
- Costo estimado: ~2.300€

**TOTAL Q2:** ~12.300€ (sin incluir mantenimiento mecánico)

### RESPUESTA 4: Vehículos NO operativos

❌ **INMOVILIZADO INMEDIATAMENTE:**

1. **Turismo V-003 (placa 9876XYZ)**
   - Razón: Seguro vencido (38 días)
   - Razón: ITV vencida (28 días)
   - **NO PUEDE CIRCULAR** hasta ambos sean renovados
   - **Impacto:** Carlos Rodríguez (Juzgado) necesita transporte alternativo
   - **Acción:** Comunicar al responsable. Alternativa: usar V-001 (si está libre)

⚠ **EN RIESGO - REVISAR:**

2. **Camión C-004 (placa 4567STU)**
   - Razón: Mantenimiento mecánico ATRASADO (2 meses sin revisión)
   - Km: 210.000 (alta utilización)
   - Edad: 10 años (antigüedad)
   - **RECOMENDACIÓN:** Revisar antes de seguir usando
   - **Acción:** Agendar revisión mecánica urgente

### CALENDARIO DE ACCIONES

**HOY (15 de marzo):**
- [ ] Comunicar a Carlos Rodríguez (Juzgado): V-003 FUERA DE SERVICIO
- [ ] Contactar compañía seguros: V-003 renovación urgente
- [ ] Contactar compañía seguros: C-001 renovación para 20 marzo
- [ ] Solicitar cita ITV: C-001 para semana próxima

**Semana del 18 marzo:**
- [ ] Solicitar cita ITV: G-001, M-001
- [ ] Contactar seguros: Renovaciones semana siguiente (V-001, M-001)
- [ ] Revisar C-004 mecánicamente

**Semana del 25 marzo:**
- [ ] Confirmar renovaciones C-001
- [ ] Agendar revisiones próximas

### PROYECCIÓN: Próximos cambios de vehículos

Vehículos cercanos a fin de vida útil (>8 años):
- C-004 (Scania 2014): Evaluar condición en junio
- G-001 (Grúa 2015): Evaluar condición en septiembre

**Presupuesto estimado 2024-2025:**
- Renovaciones (seguros + ITV): ~30.000€
- Mantenimiento preventivo: ~15.000€
- Cambio de vehículos antiguos: ~60.000€ (1-2 vehículos)

### SISTEMA AUTOMÁTICO PROPUESTO

Para evitar que vuelva a ocurrir:

1. **Revisión semanal:** Cada lunes, verificar alertas de próximos 30 días
2. **Notificación automática:** 2 semanas antes de cada vencimiento
3. **Alerta crítica:** 1 semana antes (EMAIL A JEFE)
4. **Bloqueo operacional:** Vehículos vencidos quedan fuera de servicio en sistema
5. **Reporte mensual:** Estado de flota para Gerencia

</details>

---

## Reflexión: Lecciones aprendidas

✅ **El Turismo V-003 venció sin que lo supieran** - necesitas alertas automáticas
✅ **Hay patrones:** Vencimientos escalonados, presión presupuestaria en trimestres
✅ **Proyección es clave:** Saber qué viene te permite presupuestar
✅ **Responsables deben saberlo:** Comunicación clara con quién usa cada vehículo
✅ **Mantenimiento preventivo > mantenimiento de emergencia**

## Reto Avanzado: Tu propia flota

Ahora que entiendes, crea un análisis para TU flota:

1. Recopila datos de todos tus vehículos/equipos
2. Identifica vencimientos próximos
3. Calcula impacto presupuestario
4. Propón sistema de alertas automáticas
5. Presenta a tu jefe

---

## Resumen de Competencias

**Después de este ejercicio, sabes:**

✅ Identificar alertas inmediatas vs. proyección
✅ Calcular impacto presupuestario trimestral
✅ Comunicar riesgos operacionales
✅ Diseñar sistema de alertas preventivo
✅ Usar Gema Inventario de forma crítica

**Conclusión:** La Gema Inventario es tu aliada contra sorpresas operacionales. Úsala para prevenir, no para reaccionar.

¡Tu flota funcionará mejor, más tiempo, con menos problemas!
