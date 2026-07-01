# Limitaciones de la IA 🚧

📌 **Objetivo**: Conocer qué puede y qué NO puede hacer una IA. Entender estos límites es crucial para usarla correctamente en tu trabajo administrativo.

## 📚 Qué vamos a aprender

- Qué PUEDE hacer una IA bien (y mal)
- Qué NO puede hacer bajo ninguna circunstancia
- Casos de uso incorrectos peligrosos
- Cuándo NO debes confiar en ella

---

## 🧠 Ejemplo guiado

**Escenario real**: Trabajas en gestión de expedientes. Tu jefe te pide:

> "Usa la IA para decidir cuáles de estos 100 expedientes de licencia rechazamos este mes. Tenemos presupuesto limitado."

❌ **PELIGRO**: La IA podría:
- Aprender sesgos históricos ("siempre rechazamos expedientes de zona X")
- Tomar decisiones discriminatorias sin que lo notes
- Mezclar criterios técnicos con datos personales

✅ **Lo correcto**: Usarla para:
- Analizar expedientes y destacar riesgos potenciales
- Clasificar por complejidad
- Hacer un primer filtro
- **Pero TÚ tomas la decisión final**, basándote en legalidad, equidad y contexto

---

## 💬 Prompt explicado

**Lo que NO debes hacer:**
```text
Decide automáticamente cuáles de estos 100 expedientes rechazamos.
```

**Lo que SÍ debes hacer:**
```text
Analiza estos 100 expedientes de licencia y:
1. Destaca aquellos que no cumplen requisitos técnicos mínimos
2. Agrupa por tipo de deficiencia
3. Sugiere qué requiere más análisis profundo

Yo tomaré la decisión final.
```

**¿Cuál es la diferencia?**
- Primer caso: Delegas responsabilidad a la IA (ILEGAL en decisiones administrativas)
- Segundo caso: La IA es una HERRAMIENTA de análisis (lo legal y ético)

---

## 🔄 Limitaciones concretas

### ❌ Lo que NO puede hacer

| Limitación | Por qué | Ejemplo |
|-----------|--------|---------|
| **Datos reales actualizados** | Su conocimiento tiene fecha de corte | "¿Qué cambios normativos hay en 2025?" |
| **Acceso a internet/sistemas** | No navega ni consulta bases de datos | "Consulta el expediente 2024-45678" |
| **Decisiones legales vinculantes** | Requiere responsabilidad legal | "¿Rechazamos esta solicitud?" |
| **Datos privados de ciudadanos** | No tiene identidad ni privacidad | Compartir nombres/NIFs sin protección |
| **Contextualidad legal 100% exacta** | Ley cambia, IA no actualiza sola | "¿Es legal esto ahora?" |
| **Garantías de exactitud** | Puede alucinar (veremos esto) | Datos estadísticos precisos |

### ✅ Lo que SÍ puede hacer bien

| Capacidad | Por qué | Ejemplo |
|-----------|--------|---------|
| **Análisis y síntesis** | Procesa texto excelentemente | Resumir un expediente largo |
| **Clasificación** | Detecta patrones en datos | Categorizar solicitudes |
| **Redacción profesional** | Genera texto coherente | Borradores de memorandos |
| **Brainstorming** | Genera alternativas | Ideas para comunicación |
| **Aprendizaje contextual** | Adapta respuestas en la charla | Ajusta tono según ejemplo |
| **Búsqueda de palabras clave** | Encuentra términos en texto | Localizar cláusulas en normas |

---

## 🎯 Ejercicio

**Propósito**: Identificar usos seguros vs peligrosos.

**Tarea**: Para cada caso, marca ✅ (uso seguro) o ❌ (uso peligroso):

1. _____ Usar IA para sugerir cuáles de 50 solicitudes están incompletas
2. _____ Usar IA para rechazar automáticamente expedientes sin revisión
3. _____ Usar IA para redactar un borrador de resolución de denegación
4. _____ Usar IA para tomar la decisión final de una licencia ambiental
5. _____ Usar IA para sumarizar la normativa aplicable en un caso
6. _____ Compartir expedientes completos con ciudadanos en la IA
7. _____ Usar IA para identificar patrones de retrasos en tramitación
8. _____ Usar IA como único criterio para rechazar una solicitud

---

<details>
<summary>💡 Solución comentada</summary>

1. ✅ **Sugerir incompletos**: Es un análisis, TÚ revisas y decides
2. ❌ **Rechazar automáticamente**: Decisión legal debe ser humana
3. ✅ **Redactar borrador**: Es ayuda a la redacción, TÚ lo revisas
4. ❌ **Decisión final ambiental**: Tiene implicaciones legales graves
5. ✅ **Sumarizar normativa**: Es síntesis de información existente
6. ❌ **Compartir expedientes completos**: Violación de privacidad de datos
7. ✅ **Identificar patrones de retrasos**: Es análisis de proceso, útil para mejora
8. ❌ **Único criterio de rechazo**: La decisión debe estar justificada legalmente

**La regla de oro**: Si la decisión tiene **implicaciones legales** o afecta a **derechos de ciudadanos**, el humano decide.

</details>

---

## 🚀 Reto avanzado

**Caso real**: Una alcaldía usa IA para clasificar expedientes de vivienda. Descubre que sistemáticamente rechaza más solicitudes de un barrio específico.

**Preguntas**:
1. ¿Qué fue lo que salió mal?
2. ¿Quién es responsable legalmente?
3. ¿Cómo se habría evitado?
4. ¿Qué haríais vosotros en esa situación?

**Segundo reto**: ¿Cuál es la diferencia entre "no puede hacer" y "hace mal"? ¿Y si algo es tecnológicamente posible pero éticamente inaceptable?

---

## ✅ Qué hemos aprendido

✓ La IA es una **herramienta, no un reemplazo** de tu criterio profesional  
✓ Decisiones con implicaciones legales **siempre requieren revisión humana**  
✓ Datos sensibles **nunca se comparten** sin cuidado  
✓ Los sesgos pueden entrar sutilmente si no eres **cuidadoso en supervisión**

**Próxima trampa común**: ¿Qué sucede cuando la IA "inventa" información? → 04-Alucinaciones.md

---

## 📋 Checklist de seguridad

Antes de usar IA en un proceso administrativo, pregúntate:

- [ ] ¿La decisión final la tomo yo (o mi equipo)?
- [ ] ¿He comprobado los datos que la IA propone?
- [ ] ¿Protejo la privacidad de los datos compartidos?
- [ ] ¿Podría este uso crear sesgos injustos?
- [ ] ¿Estoy usando la IA para amplificar mi capacidad, no reemplazarme?
