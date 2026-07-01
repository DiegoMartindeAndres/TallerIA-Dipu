# Las Alucinaciones de la IA 👻

📌 **Objetivo**: Comprender qué son las alucinaciones, cuándo ocurren y cómo evitarlas. Es la trampa más común y necesitas estar preparado.

## 📚 Qué vamos a aprender

- Qué son realmente las alucinaciones
- Por qué ocurren (su causa raíz)
- Señales de alerta
- Estrategias para evitarlas
- Cómo verificar respuestas

---

## 🧠 Ejemplo guiado

**Caso real**: Un administrativo pregunta a la IA:

> "¿Cuál es el artículo de la Ley de Administración Pública que regula el plazo máximo para resolver expedientes?"

La IA responde con confianza absoluta:

> "Artículo 42: Los expedientes administrativos deben resolverse en un plazo máximo de 3 meses."

El administrativo lo cita en una resolución. **Resultado**: El artículo no existe tal como fue descrito. La IA "alucinó".

**¿Qué pasó?**

La IA no "inventó a propósito". Simplemente siguió su patrón:
1. "Pregunta sobre leyes" → "Respuesta con número de artículo"
2. Generó un número plausible (42)
3. Generó texto que suena oficial
4. **Pero NO verificó si era real**

---

## 💬 Prompt explicado

**Peor caso - ALUCINA:**
```text
¿Cuál es el artículo exacto de la normativa sobre licencias urbanísticas?
```

**Mejor caso - REDUCE alucinaciones:**
```text
En la Ley de Ordenación Territorial de España, busca el artículo 
que regula plazos de licencia urbanística.

Si no lo encuentra en tu conocimiento, responde: "No tengo información verificada."

Importante: Mejor decir "no sé" que inventar.
```

**Mejor aún - ELIMINA alucinaciones:**
```text
Adjunto la Ley de Ordenación Territorial actualizada (abajo).

Analiza este texto y encuentra el artículo sobre plazos de licencia urbanística.
Responde solo con información del documento proporcionado.

[Insertar aquí el texto de la ley]
```

---

## 🔄 Tipos de alucinaciones

### 1. **Alucinaciones factales**
> "La capital de Portugal es Lisboa. La capital de Andorra es Barcelona."
*(Andorra no tiene capital; su co-príncep es... la IA inventó)*

**En tu trabajo**: Inventa artículos, normas, plazos, procedimientos que no existen.

### 2. **Alucinaciones de conexión**
> "Como mencionaste en tu email anterior de febrero..."
*(Nunca mencionaste nada, la IA lo inventó)*

**En tu trabajo**: "Según tu expediente anterior..." cuando no hay conexión real.

### 3. **Alucinaciones de cita**
> "Como dice Pérez et al. (2023) en el estudio 'Análisis de Tramitación...'"
*(El estudio no existe)*

**En tu trabajo**: Cita normas, sentencias, estudios que no existen.

---

## 🎯 Ejercicio de detección

**Propósito**: Aprender a detectar alucinaciones.

**Lee estas respuestas** (de verdad son casos reales alterados) y marca ⚠️ dónde sospechas una alucinación:

1. ⚠️ _____ "La Resolución 2024-45 del Ministerio del Interior especifica que los expedientes de vivienda se tramitan en máximo 15 días hábiles."

2. ⚠️ _____ "En el procedimiento administrativo común, el ciudadano tiene derecho de audiencia antes de la resolución denegatoria."

3. ⚠️ _____ "El Decreto-Ley 7/2023 sobre digitalización administrativa establece que todos los trámites deben realizarse sin papel."

4. ⚠️ _____ "Según tu expediente anterior 2023-001, la normativa ha cambiado."

5. ⚠️ _____ "El RGPD requiere consentimiento para tratar datos personales, con excepciones en funciones públicas."

---

<details>
<summary>💡 Análisis de riesgo</summary>

1. ⚠️ **ALTO RIESGO**: Resoluciones específicas (números, años) son muy peligrosas. Verificar en BOE.
2. ✅ **BAJO RIESGO**: Es un principio general de derecho administrativo (LRJSP). Probable corrección.
3. ⚠️ **RIESGO ALTO**: Decreto-Ley específico con número. Verificar existencia.
4. ⚠️ **CLARAMENTE ALUCINADA**: La IA no sabe de tu expediente específico. Imposible referenciar.
5. ✅ **BAJO RIESGO**: Es información verificable sobre RGPD, probable corrección.

**Patrón**: Cuanto más específico (números, fechas, referencias exactas), mayor riesgo de alucinación.

</details>

---

## 🚀 Reto avanzado

**Pregunta incómoda**: ¿Por qué la IA es especialmente peligrosa con la ley?

Piensa en:
1. **Confianza**: Suena como un abogado, pero no lo es
2. **Estabilidad**: La ley cambia, la IA tiene fecha de corte
3. **Responsabilidad**: Tú eres responsable si usas información incorrecta, no la IA
4. **Verificabilidad**: Otros pueden ver que usaste IA y dudarán de ti

**Propuesta**: Diseña un protocolo para tu equipo que proteja contra alucinaciones legales.

---

## ✅ Qué hemos aprendido

✓ Las alucinaciones **NO son errores**, son características del diseño  
✓ Ocurren porque la IA **predice lo probable, no verifica**  
✓ Son especialmente peligrosas en **contextos legales y numéricos**  
✓ La única defensa es **verifica siempre información crítica**

---

## 🛡️ Protocolo anti-alucinaciones

### Para información crítica (decisiones legales):

1. **Proporciona contexto** (adjunta documentos, leyes)
2. **Pide verificación** ("¿Estás seguro de esta información?")
3. **Verifica independientemente** (consulta BOE, normativa oficial)
4. **Desconfía de números específicos** (años, artículos, plazos)
5. **Busca fuentes** ("¿De dónde sacaste esto?")
6. **Usa con humildad** (es una asistente, no experta legal)

### Ejemplos seguros

✅ Pedir síntesis de un documento que adjuntas  
✅ Pedir redacción de un memo (que luego revisas)  
✅ Pedir ideas de argumentos (que investigas después)  
✅ Pedir clasificación de datos (que verificas)

### Ejemplos peligrosos

❌ Pedir leyes sin adjuntar el texto  
❌ Pedir datos históricos precisos  
❌ Aceptar citas sin verificar  
❌ Usar como única fuente de información legal

---

## 📝 Nota importante

**No es incompetencia de la IA, es su naturaleza.** Las alucinaciones son inherentes a cómo funcionan estos modelos. No es "bug", es "feature" que puede ser peligrosa si no la entiendes.

**Siguiente tema**: Ahora que entiendes cómo funciona y sus límites, preparémonos para hacerla útil. → 05-Estructura-Prompts.md

---

## 🔍 Checklist antes de usar información de IA

- [ ] ¿Es información crítica para una decisión legal/administrativa?
- [ ] ¿Cité fuentes específicas (artículos, leyes)?
- [ ] ¿Verificué esa información en fuente oficial?
- [ ] ¿Podría una alucinación aquí causar daño?
- [ ] ¿Tengo tiempo para verificar o mejor evito?

Si respondes sí a preguntas 1-3 o 4, **verifica siempre antes de usar**.
