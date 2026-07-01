# Contexto: El Superpoder 💪

📌 **Objetivo**: Entender que el contexto es el factor más poderoso para mejorar respuestas de IA. Proporcionar contexto es el 80% del trabajo.

## 📚 Qué vamos a aprender

- Por qué el contexto es crucial
- Técnicas para "inyectar" contexto efectivamente
- Cuánto contexto es suficiente
- Cómo usarlo en administración pública

---

## 🧠 Ejemplo guiado

**Problema**: Necesitas que la IA redacte una resolución de denegación de licencia.

### ❌ Sin contexto (resultado genérico):
```text
Redacta una resolución denegando una solicitud de licencia de obra.
```

**IA produce**:
> "Se deniega la solicitud de licencia de obra por incumplimiento de normativa. 
> El solicitante tiene derecho de recurso."

**Problema**: Genérica, sin fundamento legal específico, no servible.

---

### ✅ Con contexto (resultado preciso):
```text
CONTEXTO NORMATIVO:
- Ley de Ordenación Territorial 2/2006
- Plan General de Ordenación Urbana vigente (2015)
- Zona clasificada: Área protegida de patrimonio
- Usos permitidos en zona: Residencial, equipamientos públicos
- Usos prohibidos: Industrial, comercial, hostelería

CONTEXTO DE LA SOLICITUD:
- Solicitante: Empresa X, CIF 12345678A
- Ubicación: Calle Principal 50
- Solicitud: Licencia para local comercial/hostelería
- Documentación adjunta: Proyecto técnico (24 sept 2024)
- Fecha entrada: 1 octubre 2024

CONTEXTO ADMINISTRATIVO:
- Área técnica ha evaluado: DICTAMEN NEGATIVO (17 octubre 2024)
- Razón técnica: No cumple usos permitidos en zona protegida
- Este tipo de solicitud tiene precedente: 3 rechazos anteriores por mismo motivo
- Apelaciones anteriores: Siempre confirmadas por Tribunal Administrativo

TAREA:
Redacta la resolución de denegación que:
1. Cite la norma aplicable (ley, plan, clasificación)
2. Haga referencia al dictamen técnico
3. Explique específicamente por qué se deniega (no genérico)
4. Indique derechos de recurso administrativo
5. Mantenga ton profesional y claro

FORMATO:
- Estructura estándar de resolución administrativa
- Considerandos, fundamentos legales, parte dispositiva
- Máximo 1 página
```

**IA produce**:
> "RESOLUCIÓN
> 
> CONSIDERANDO:
> Que la solicitud de licencia de actividad comercial/hostelería presentada 
> por Empresa X con CIF 12345678A para la Calle Principal 50 entra en contradicción 
> con la clasificación urbanística del Plan General de Ordenación Urbana de 2015.
> 
> FUNDAMENTOS DE DERECHO:
> Art. 15 de la Ley de Ordenación Territorial 2/2006: Los usos permitidos 
> en áreas protegidas de patrimonio se limitan a residencial y equipamientos públicos.
> La actividad solicitada (hostelería) está expresamente prohibida.
> 
> FALLO:
> Se DENIEGA la licencia..."

**Diferencia**: Precisa, legal, referenciada, profundamente superior.

---

## 💬 Técnicas de inyección de contexto

### Técnica 1: Proporcionando TEXTOS LEGALES

**Peor**:
```text
¿Es legal que rechacemos esta solicitud?
```

**Mejor**:
```text
Adjunto: Artículos 42-48 de la Ley de Procedimiento Administrativo.

Pregunta: Basándote SOLO en estos artículos, 
¿podemos rechazar una solicitud por documentación incompleta?

Caso concreto: El solicitante no adjuntó el certificado de empadronamiento.
```

---

### Técnica 2: Descripción PASO A PASO del proceso

**Peor**:
```text
Optimiza nuestro proceso de tramitación.
```

**Mejor**:
```text
Nuestro proceso actual:

1. ENTRADA (1-2 días)
   - Recepción de solicitud
   - Registro en BRIM
   - Escaneo de documentos
   - Asignación a técnico

2. ANÁLISIS INICIAL (3-5 días)
   - Técnico revisa completitud
   - Si incompleto: notificación al ciudadano
   - Ciudadano tiene 10 días para completar

3. ANÁLISIS TÉCNICO (20-30 días)
   - Evaluación proyecto
   - Consulta especialistas si necesario
   - Solicitud info adicional si falta

4. APROBACIÓN LEGAL (5-10 días)
   - Abogada revisa resolución
   - Correcciones legales
   - Redacción final

5. RESOLUCIÓN (1-2 días)
   - Firma de la resolución
   - Notificación ciudadano

Problema: Los trámites toman 90-120 días, objetivo es 60.
Propón optimizaciones concretas.
```

---

### Técnica 3: Proporcionando EJEMPLOS PREVIOS

**Peor**:
```text
¿Cuáles deberían ser los requisitos mínimos para una convocatoria?
```

**Mejor**:
```text
Adjunto ejemplos de convocatorias exitosas que hemos usado:

[CONVOCATORIA 2022 - Subsidio vivienda: Requisitos]
[CONVOCATORIA 2023 - Ayudas a emprendimiento: Requisitos]

Ahora redacta UNA NUEVA convocatoria para subsidio de energías renovables.
Mantén el nivel de claridad de las anteriores.
Incluye los mismos tipos de requisitos (documentación, económicos, temporales).
```

---

### Técnica 4: Estableciendo RESTRICCIONES y SUPOSICIONES

**Peor**:
```text
¿Qué datos deberíamos recoger en una solicitud?
```

**Mejor**:
```text
RESTRICCIONES:
- Solo datos NECESARIOS para evaluar elegibilidad
- Sin preguntas redundantes con expedientes anteriores
- Máximo 15 campos en el formulario
- Apto para ciudadanos sin asesoría

DATOS QUE YA TENEMOS:
- Padrón de habitantes (acceso via API)
- Historial de anteriores solicitudes
- Datos de ingresos (AEAT via convenio)

DATOS QUE NECESITAMOS:
- Justificación específica de solicitud
- Documentación acreditativa (si requiere)
- [Otros 2-3 datos específicos]

¿Qué formulario minimal conseguiría nuestro objetivo?
```

---

## 🔄 Cantidad óptima de contexto

| Situación | Contexto recomendado | Por qué |
|-----------|-------------------|--------|
| **Redacción genérica** | 1-2 párrafos | Orientación general |
| **Análisis específico** | 3-5 párrafos | Detalles para precisión |
| **Decisión legal** | Completo (ley, precedentes) | Responsabilidad legal |
| **Cambio de proceso** | Describir actual + objetivo | Mejora basada en hechos |
| **Redacción oficial** | Plantilla + ejemplo + restricciones | Consistency + exactitud |

**Regla**: Si tiendes a recibir respuestas genéricas, **más contexto**.

---

## 🎯 Ejercicio: Construir contexto

**Propósito**: Práctica de inyección contextual.

**Situación real**: Necesitas que la IA analice por qué vuestros trámites de licencia 
se atrasan más en verano que en invierno.

**Tu tarea**: Proporciona TODO el contexto que la IA necesitaría:

1. **Contexto operativo** (cómo funciona actualmente)
2. **Datos históricos** (lo que sabes de retrasos)
3. **Restricciones** (qué no puedes cambiar)
4. **Objetivo claro** (qué quieres entender)

---

<details>
<summary>💡 Ejemplo completo</summary>

```text
CONTEXTO OPERATIVO:
Nuestro equipo de licencias está compuesto por:
- 1 jefa de sección
- 4 técnicos administrativos
- 1 abogada (compartida con otras secciones)

Proceso:
1. Recepción (2 días)
2. Análisis técnico (15-20 días)
3. Revisión legal (3-5 días)
4. Resolución (2 días)

DATOS HISTÓRICOS (últimos 3 años):
- Enero-junio: Plazo promedio 28 días
- Julio-septiembre: Plazo promedio 42 días
- Octubre-diciembre: Plazo promedio 26 días
- Julio especialmente malo (52 días promedio)

RESTRICCIONES:
- Presupuesto: Sin aumento (no puedo contratar temporales)
- Personal: La abogada es compartida, no hay forma de aumentar % dedicación
- Normativa: Los trámites toman el tiempo que toman (no se pueden acelerar legalmente)

DATOS ADICIONALES:
- Verano: Personal de vacaciones (30% ausencia en julio-agosto)
- Verano: Volumen de solicitudes AUMENTA 40% (¿por qué?)
- Las denegaciones tardan lo mismo que las aprobaciones

PREGUNTA:
¿Por qué aumentan los retrasos en verano? 
¿Hay soluciones operativas sin presupuesto adicional?
```

</details>

---

## 🚀 Reto avanzado

**Reto 1**: Piensa en una decisión administrativa compleja que tuviste que tomar. 
¿Cuánto contexto deberías proporcionar a la IA para que entienda tu situación realmente?

**Reto 2**: ¿Qué sucede si proporcionas contexto SESGADO?

Ejemplo: "Todos los ciudadanos de barrio X presentan solicitudes malhechas"
- ¿Detectaría la IA tu sesgo?
- ¿Cómo afectaría a sus recomendaciones?
- ¿Cómo equilibrarías la información?

---

## ✅ Qué hemos aprendido

✓ Contexto = **precisión exponencial**  
✓ Es mejor **demasiado contexto que poco**  
✓ Técnicas: textos legales, procesos paso-a-paso, ejemplos, restricciones  
✓ El contexto **equilibra automatización con humanidad**

---

## 📋 Checklist de contexto

- [ ] ¿Incluí la normativa/referencias legales aplicables?
- [ ] ¿Describí el proceso o situación actual paso-a-paso?
- [ ] ¿Proporcioné ejemplos previos similares?
- [ ] ¿Establecí restricciones claras?
- [ ] ¿Expliqué por qué necesito esto?
- [ ] ¿Un colega podría reproducir mis resultados con este contexto?

**Siguiente paso**: Ejemplos amplían aún más la precisión. → 08-Ejemplos.md
