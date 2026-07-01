# Desarrollo: Construyendo tu Gema Paso a Paso

## Paso 1: Escribe el prompt del sistema

Este es el corazón de tu Gema. Es donde le cuentas TODO lo que necesita saber.

### Estructura recomendada

```text
PATRÓN DE PROMPT PARA TU GEMA:

Eres un asistente especializado en [TU ÁREA].

OBJETIVO:
[Qué exactamente debe hacer]

CONTEXTO NORMATIVO/PROCEDURAL:
[Normas, procedimientos, conceptos clave]
[Clasificaciones, definiciones]

CAPACIDADES:
1. [Qué puede hacer]
2. [Qué puede hacer]
3. [Qué puede hacer]
4. [Qué puede hacer]
5. [Qué puede hacer]

RESTRICCIONES CRÍTICAS:
- NUNCA [cosa que no debe hacer]
- SIEMPRE [cosa que debe cumplir]
- SI [situación] ENTONCES [acción]

FORMATO DE RESPUESTA:
[Especifica exactamente cómo presentar info]

EJEMPLOS:
[Muestra 2-3 ejemplos de entrada/salida correcta]
```

### Ejercicio: Escribe tu prompt

Usa tu plantilla (de 02-Plantilla.md) para llenar:

```text
Eres un asistente especializado en [DE SECCIÓN 1]:
_______________________________________________

OBJETIVO:
[DE SECCIÓN 1 - Propósito]
_______________________________________________

CONTEXTO NORMATIVO:
[DE SECCIÓN 2 - Normas, conceptos, tablas, plazos]
_______________________________________________
_______________________________________________

CAPACIDADES:
1. [DE SECCIÓN 3 - Función 1]
2. [DE SECCIÓN 3 - Función 2]
3. [DE SECCIÓN 3 - Función 3]
4. [DE SECCIÓN 3 - Función 4]
5. [DE SECCIÓN 3 - Función 5]

RESTRICCIONES CRÍTICAS:
[DE SECCIÓN 4 - Lo que NO puede hacer]
_______________________________________________

FORMATO DE RESPUESTA:
[Especifica cómo presentar cada respuesta]
_______________________________________________

EJEMPLOS:
Entrada: [DE SECCIÓN 6 - Caso 1]
Salida esperada: [Resultado correcto]

Entrada: [DE SECCIÓN 6 - Caso 2]
Salida esperada: [Resultado correcto]
```

**Resultado:** Tienes tu prompt del sistema. Guárdalo en archivo o documento.

---

## Paso 2: Incorpora contexto específico

Tu Gema necesita conocimiento que le des explícitamente.

### Qué incluir como contexto

```
INFORMACIÓN ESPECÍFICA DE TU ADMINISTRACIÓN:

Plazos locales:
- Plazo X: ______ días (en tu municipio)
- Plazo Y: ______ días (en tu municipio)

Procedimiento específico:
- Fase 1: _________________
- Fase 2: _________________
- Responsable: ____________

Documentación que REQUIERES:
1. _________________
2. _________________
3. _________________

Excepciones autorizadas localmente:
- _________________
- _________________

Clasificaciones/categorías:
- Categoría A: _________________
- Categoría B: _________________

Responsables en tu administración:
- Quién aprueba: _________________
- Quién revisa: _________________
- Quién decide: _________________
```

### Cómo incluirlo en el prompt

Agrega una nueva sección: "INFORMACIÓN DE [TU MUNICIPIO]":

```text
[Tu prompt anterior...]

INFORMACIÓN DE [MUNICIPIO]:
- Plazos máximos: [Tus plazos]
- Responsables: [Tus roles]
- Documentación requerida: [Tu lista]
- Excepciones locales: [Tus excepciones]

[Resto del prompt...]
```

---

## Paso 3: Prueba con casos reales

Ahora testa tu Gema con datos reales.

### Ejercicio: Testing

**Crea dataset de 10 casos:**

```
CASO 1: [Situación típica, esperado: ✓]
CASO 2: [Situación típica, esperado: ✓]
CASO 3: [Situación típica, esperado: ✓]
CASO 4: [Situación límite, esperado: ✓]
CASO 5: [Error común, esperado: ✗ Debe detectar]
CASO 6: [Excepción autorizada, esperado: ✓]
CASO 7: [Incumplimiento subsanable, esperado: ⚠]
CASO 8: [Incumplimiento crítico, esperado: ✗]
CASO 9: [Ambigüedad, esperado: Remitir a humano]
CASO 10: [Tu caso más frecuente, esperado: ✓]
```

### Cómo testear

1. **Copia el prompt** completo en tu herramienta IA (ChatGPT, Claude, etc.)
2. **Lanza cada caso** como pregunta separada
3. **Registra resultado**: ✓ Correcto / ✗ Incorrecto / ⚠ Parcial
4. **Calcula aciertos**: X de 10 = X% de precisión

### Tabla de resultados

| Caso | Entrada | Respuesta | ✓/✗/⚠ | Problema |
|------|---------|-----------|-------|----------|
| 1 | [breve] | [breve] | ✓ | - |
| 2 | [breve] | [breve] | ✓ | - |
| 3 | [breve] | [breve] | ✓ | - |
| 4 | [breve] | [breve] | ✓ | - |
| 5 | [breve] | [breve] | ✓ | - |
| ... | ... | ... | ... | ... |
| **TOTAL** | | | | **X/10 aciertos** |

**Objetivo mínimo:** 8/10 = 80% aciertos

Si tienes < 80%:
- Identifica qué falló
- Refina el prompt
- Repite testing

---

## Paso 4: Itera y mejora

### Si las respuestas no son correctas

| Problema | Causa probable | Solución |
|----------|---------------|----|
| Respuestas genéricas | Prompt muy vago | Sé más específico |
| Olvida restricciones | No las mencionaste claramente | Agrega restricción explícita |
| Salida confusa | No especificaste formato | Define formato exacto |
| Errores de cálculo | Falta contexto | Agrega datos/ejemplos |

### Ciclo de mejora

```
Testing (10 casos) → Identifica 2-3 problemas
  ↓
Refina prompt (ataca 1 problema)
  ↓
Testing (5 casos nuevos)
  ↓
¿Mejoró? Sí → Próximo problema / No → Intenta solución diferente
  ↓
Repite hasta 90%+ aciertos
```

---

## Paso 5: Documenta y compartibiliza

### Crea documento final

Guarda tu Gema en un formato que otros puedan usar:

**Opción A: Documento Word/Google Docs**
```
NOMBRE: Mi Gema [Nombre]
PROPÓSITO: [1 frase]

CÓMO USARLA:
1. Copia este prompt completo
2. Pégalo en ChatGPT/Claude
3. Haz tu pregunta
4. Obtén respuesta especializada

PROMPT DEL SISTEMA:
[Tu prompt completo aquí]

EJEMPLOS DE USO:
Pregunta 1: ...
Pregunta 2: ...

LIMITACIONES:
- NO puede: ...
- REQUIERE: ...

CONTACTO: [Tu nombre para preguntas]
```

**Opción B: Archivo Markdown (.md)**
- Más profesional
- Fácil de versionar
- Puedes compartir en repositorio

**Opción C: Video/Tutorial corto**
- Muestra la Gema en acción
- Enseña a otros cómo usarla
- Duración: 5-10 minutos

### Checklist de validación

Antes de considerar tu Gema "lista", verifica:

```
FUNCIONALIDAD:
[ ] Funciona con casos típicos
[ ] Detecta errores/excepciones
[ ] Respeta restricciones
[ ] Formato de salida es claro

PRECISIÓN:
[ ] 80%+ aciertos en testing
[ ] 0 errores críticos
[ ] Resultados reproducibles

DOCUMENTACIÓN:
[ ] Prompt está documentado
[ ] Ejemplos de uso incluidos
[ ] Limitaciones claras
[ ] Instrucciones para otros

USABILIDAD:
[ ] Un compañero puede usarla sin ayuda
[ ] Respuestas son actionables
[ ] Tiempo de respuesta aceptable

CALIDAD:
[ ] Revisada por compañero
[ ] Aprobada por jefe
[ ] Listo para "producción"
```

---

## Ejercicio completo: Construir tu Gema

**Tiempo total: 3-4 horas**

### Bloque 1: Construcción (1-2 horas)

```
[ ] Escribir prompt del sistema (30 min)
[ ] Incorporar contexto específico (30 min)
[ ] Crear dataset de 10 casos (30 min)
[ ] Testear en herramienta IA (30 min)
```

### Bloque 2: Mejora (1-2 horas)

```
[ ] Analizar resultados (15 min)
[ ] Identificar 2-3 problemas (15 min)
[ ] Iterar Prompt (30 min)
[ ] Re-testear (30 min)
[ ] Si < 80%, repetir (30 min)
```

### Bloque 3: Documentación (30-45 min)

```
[ ] Crear documento final (15 min)
[ ] Revisar con compañero (15 min)
[ ] Ajustes finales (15 min)
```

---

## Resultado esperado

Al completar estos pasos, tienes:

✅ **Prompt del sistema funcional**
✅ **Contexto incorporado**
✅ **Testing con 80%+ aciertos**
✅ **Documentación completa**
✅ **Listo para que otros lo usen**

<details>
<summary>💡 Ejemplo: Gema construida y validada</summary>

**GEMA VALIDADOR DE ADMISIBILIDAD DE SUBVENCIONES**

**Resultado testing:**
- Caso 1-3: ✓ Validación correcta (típicos)
- Caso 4: ✓ Identificó límite correctamente
- Caso 5: ✓ Detectó incumplimiento
- Caso 6: ✓ Aceptó excepción autorizada
- Caso 7: ✓ Clasificó como subsanable
- Caso 8: ✓ Rechazó incumplimiento crítico
- Caso 9: ✓ Remitió a jurídica
- Caso 10: ✓ Manejó caso frecuente
- Caso 11 (nuevo): ✓ 
- Caso 12 (nuevo): ✓

**Resultado: 12/12 = 100% aciertos**

**Iteraciones necesarias:**
- Iteración 1: 6/10 aciertos (60%) → Agregué restricciones explícitas
- Iteración 2: 9/10 aciertos (90%) → Mejoré formato de salida
- Iteración 3: 12/12 aciertos (100%) → Agregué ejemplos específicos

**Tiempo total:** 2.5 horas

**Impacto:**
- Tiempo por validación: 2.5 horas → 15 minutos (84% reducción)
- Errores: 2-3 por 20 expedientes → 0 esperados
- Adopción: Personal la usa en cada convocatoria

</details>

---

## Próximo paso

✅ **Construiste tu Gema**
✅ **La testeaste y validaste**
✅ **La documentaste**

**Próximo:** Ve a **04-Presentacion.md** para presentarla a tu equipo y obtener feedback.

---

## Resumen del desarrollo

✅ Escribiste prompt del sistema
✅ Incorporaste contexto específico
✅ Testeaste con casos reales
✅ Iteraste hasta 80%+ aciertos
✅ Documentaste completamente
✅ Tienes checklist de validación

**¡Tu Gema está lista!** 🚀

Próxima fase: Presentarla al equipo y ver el impacto real.
