# Prompts Prácticos para Inventario
## Prompt 1: ¿Qué vence esta semana?
**Caso de uso:** Alertas diarias rápidas
**Tiempo:** <30 segundos
**Tipo:** Urgencia operacional
```text
Hoy es [HOY - ejemplo: 15 de marzo de 2024].
Activos municipales con vencimientos próximos (próximos 7 días):
Vehículos:
- Camión C-001 (placa 1234ABC): Seguro vence 18/03
- Furgoneta C-002 (placa 5678DEF): ITV vence 20/03
Equipos IT:
- Servidor central (SRV-001): Certificado SSL vence 17/03
- Portátil dirección (PORT-042): Revisión técnica pendiente
¿Qué necesito hacer esta semana?
```
**Variante con más contexto:**
```text
Mi municipio tiene [CANTIDAD] vehículos y [CANTIDAD] equipos IT.
Hoy: [HOY]
Próximos 7 días: Alertarme de CUALQUIER vencimiento.
Tengo estos activos con fechas próximas:
[LISTA DE ACTIVOS CON FECHAS DE VENCIMIENTO]
¿Qué requiere acción URGENTE esta semana?
```
## Prompt 2: ¿Cuándo cambiar equipos IT?
**Caso de uso:** Planificación de cambios
**Tiempo:** 1-2 minutos
**Tipo:** Proyección presupuestaria
```text
Nuestro equipamiento informático:
- 30 ordenadores de escritorio (adquiridos 2020)
- 15 portátiles (adquiridos 2021-2022)
- 5 servidores (adquiridos 2018-2019)
Vida útil según normas:
- Escritorios: 4 años
- Portátiles: 3 años
- Servidores: 5 años
¿Cuándo debo reemplazar cada categoría?
¿Cuál es la proyección para 2024-2025?
¿Presupuesto estimado?
```
**Respuesta esperada:**
```
CAMBIOS PROYECTADOS:
2024:
✓ Escritorios (2020): Cumplirán 4 años en [MES 2024] - REEMPLAZO URGENTE
✓ Portátiles (2021): Cumplirán 3 años en [MES 2024] - COMIENZAN BAJA
2025:
✓ Servidores (2018-2019): Evaluación de estado
```
## Prompt 3: ¿Este vehículo está al día?
**Caso de uso:** Validación rápida antes de usar
**Tiempo:** <30 segundos
**Tipo:** Verificación operacional
```text
Necesito usar el vehículo C-045 (Camión blanco, placa 9876XYZ).
Datos del vehículo:
- Adquirido: 2018
- Último servicio: 15 de enero
- Seguro: Vence 30 de marzo
- ITV: Vence 30 de marzo
- Km: 125.000
¿Está al día? ¿Puedo usarlo hoy?
¿Qué revisar antes de usarlo?
```
## Prompt 4: ¿Puedo dar de baja este activo?
**Caso de uso:** Validación de procedimiento de baja
**Tiempo:** 1-2 minutos
**Tipo:** Cumplimiento normativo
```text
Quiero dar de baja un ordenador.
Datos:
- Número inventario: COMP-2018-045
- Modelo: Lenovo ThinkCentre
- Adquirido: 2018
- Razón de baja: Obsoleto, no arranca tras actualización Windows
Documentación que tengo:
✓ Acta de recepción (2018)
✓ Solicitud de baja (firmada por responsable área)
❌ Certificado de disposición (no existe)
❌ Resolución de Alcalde autorizando baja
¿Cuál es el procedimiento correcto?
¿Qué me falta?
¿Quién debe autorizar?
```
## Prompt 5: Reporte de estado de inventario
**Caso de uso:** Reportes para jefatura/auditoría
**Tiempo:** 2-3 minutos
**Tipo:** Resumen ejecutivo
```text
Necesito un reporte del estado del inventario de vehículos 
para presentar al Alcalde.
Datos de la flota:
[LISTA COMPLETA CON VEHÍCULOS, AÑOS, VENCIMIENTOS]
Genera un resumen que incluya:
1. Total de vehículos
2. Estado de seguro/ITV (al día vs. vencido)
3. Alertas de próximos vencimientos (próximos 3 meses)
4. Proyección de cambios (próximos 2 años)
5. Acciones recomendadas
Formato: Ejecutivo, máximo 1 página, lenguaje profesional.
```
## Prompt 6: ¿Qué activos no están asignados?
**Caso de uso:** Auditoría de control
**Tiempo:** 1 minuto
**Tipo:** Verificación de custodia
```text
Necesito auditar qué activos no tienen responsable asignado.
Equipos informáticos en nuestro inventario:
- COMP-2023-001 a COMP-2023-025: 25 equipos (asignados)
- COMP-2022-001 a COMP-2022-010: 10 equipos (2 sin asignar: 005, 008)
- COMP-2021-001 a COMP-2021-015: 15 equipos (asignados)
- PORT-2023-001 a PORT-2023-008: 8 equipos (1 sin asignar: 003)
¿Cuáles son los equipos sin responsable?
¿Es normal? ¿Qué debo hacer?
```
## Combinando prompts para análisis completo
```
Semana 1:
 Prompt 1: ¿Qué vence esta semana?
 Prompt 3: ¿Este vehículo está al día?
 Prompt 6: ¿Qué activos faltan asignar?
Mes:
 Prompt 2: ¿Cuándo cambiar equipos?
 Prompt 5: Reporte de estado
 Prompt 4: ¿Puedo dar de baja?
Trimestre:
 Reporte general + auditoría completa
```
## Ejercicio: Crear tus prompts
### Paso 1: Identifica 3 preguntas frecuentes
```
1. ¿_________________________________?
2. ¿_________________________________?
3. ¿_________________________________?
```
### Paso 2: Para cada una, crea un prompt
Usa estructura:
```text
[CONTEXTO de tu administración]
[INFORMACIÓN sobre activo/s específico/s]
[PREGUNTA clara]
[FORMATO deseado de respuesta]
```
### Paso 3: Prueba con datos reales
- ¿La respuesta es precisa?
- ¿Te falta información en el prompt?
- ¿Cómo mejorar?
### Paso 4: Automatiza
Una vez que funcione bien, úsalo regularmente como checklist.
<details>
<summary>💡 Ejemplo: Prompts personalizados para mi administración</summary>
**Pregunta frecuente 1: "¿Hay algún seguro o ITV a punto de vencer?"**
```text
Hoy es [HOY].
Mi flota municipal:
- 5 vehículos turismos
- 3 camiones
- 2 vehículos especiales
Vencimientos próximos:
- Camión C-001: Seguro 20 de abril, ITV 25 de abril
- Furgoneta C-002: Seguro 10 de mayo, ITV 15 de mayo
- Turismo V-001: Seguro 30 de marzo
¿Cuál vence primero?
¿Cuántos días tengo antes de que venza?
¿Cómo prevengo sorpresas?
```
**Pregunta frecuente 2: "¿Cuándo tengo que cambiar mis portátiles?"**
```text
Tengo 12 portátiles en la administración:
- 5 adquiridos en 2021 (3 años ahora)
- 4 adquiridos en 2022 (2 años ahora)
- 3 adquiridos en 2023 (1 año ahora)
Vida útil normal: 3-4 años
¿Cuál es el cronograma de cambios para 2024-2025?
¿Presupuesto estimado si cambio los del 2021?
¿Es mejor cambiar todo o escalonado?
```
**Pregunta frecuente 3: "¿Este activo está listo para baja?"**
```text
Tengo una impresora multifunción (INV-2015-088).
Estado:
- Adquirida: 2015 (9 años)
- Condición: No imprime a color (cabezal dañado)
- Coste de reparación: 800€ (60% del valor de compra)
- Alternativa: Impresora nueva por 1.200€
¿Está justificada la baja?
¿Cuál es el procedimiento?
¿Qué documento necesito del Alcalde?
```
</details>
---
## Resumen
✅ 6 prompts prácticos listos para usar
✅ Cada uno con variantes personalizables
✅ Enfoque en: alertas, planificación, validación
✅ Puedes combinarlos para auditoría completa
✅ Automatiza tu gestión de inventario
**Próximo paso:** Ve a **03-Ejercicio.md** para resolver un caso práctico completo de alertas de mantenimiento.
