# 📊 Caso Práctico: Excel Avanzado - Fórmulas Complejas con IA

**Aprende a construir fórmulas profesionales usando IA como guía, no como solución directa**

---

## 📌 Objetivo

En este ejercicio crearás un **sistema de calificación profesional** completo para una asignatura, utilizando la IA para **entender y construir** fórmulas, no para copiarlas directamente.

Aprenderás a:
✅ Pedir a la IA que EXPLIQUE fórmulas en lugar de darlas  
✅ Construir fórmulas paso a paso  
✅ Validar tu trabajo contra una solución  
✅ Aplicar estas técnicas en tu administración  

**Resultado:** Un archivo Excel completamente funcional que califica automáticamente.

---

## 📋 El Archivo: Sistema de Evaluación

### Descarga el archivo

El archivo `evaluacion.xlsx` está en la carpeta `datos/`:

```
📁 01-IA-Generativa/datos/evaluacion.xlsx
```

**Descárgalo antes de empezar.**

---

## 🧠 Entendiendo el Sistema

### Las Columnas Existentes

El archivo tiene estas columnas CON DATOS:

| Columna | Nombre | Descripción | Ejemplo |
|---------|--------|-------------|---------|
| A | Alumno | Identificador anonimizado | A01, A02, A03 |
| B | P1 | Nota práctica 1 (0-10) | 8.5 |
| C | PP1 | Nota prueba práctica 1 (0-10) | 7.0 |
| E | P2 | Nota práctica 2 (0-10) | 9.0 |
| F | PP2 | Nota prueba práctica 2 (0-10) | 8.5 |
| H | P3 | Nota práctica 3 (0-10) | 7.5 |
| I | PP3 | Nota prueba práctica 3 (0-10) | 8.0 |
| K | Ex | Nota examen final (0-10) | 7.0 |

### Las Columnas a Calcular

Tu trabajo es llenar estas columnas VACÍAS:

| Columna | Nombre | Cálculo | Dificultad |
|---------|--------|---------|-----------|
| D | PF1 | Media geométrica de B y C | ⭐ Fácil |
| G | PF2 | Media geométrica de E y F | ⭐ Fácil |
| J | PF3 | Media geométrica de H e I | ⭐ Fácil |
| L | Nota_Final | Promedio ponderado con validaciones | ⭐⭐⭐ Difícil |
| M | Nota_Acta | Nota con restricciones legales | ⭐⭐⭐ Difícil |
| N | Retro | Retroalimentación automática | ⭐⭐⭐⭐ Muy Difícil |

---

## 💡 ¿Qué es la Media Geométrica?

La media geométrica es más "justa" que la media aritmética cuando tienes componentes de diferente peso.

```
Media Aritmética: (8 + 4) / 2 = 6
Media Geométrica: √(8 × 4) = √32 ≈ 5.66

Nota: La geométrica castiga más si una nota es muy baja.
```

**En Excel:**
```
Fórmula: =POTENCIA(B2*C2; 0.5)
O más moderna: =MEDIA.GEOM(B2:C2)
```

---

## 🎯 Ejercicio Paso a Paso

### **PASO 1: Entender el Archivo**

Abre el archivo `evaluacion.xlsx` y:

1. Mira los datos existentes (columnas A-I, K)
2. Identifica qué datos FALTAN
3. Cuenta cuántos alumnos hay
4. Nota que algunos datos pueden estar vacíos (0 o en blanco)

<details>
    <summary>💡 Consejo</summary>
<br>

En Excel/Sheets, presiona **Ctrl+End** para ir al última celda con datos. Así ves el rango completo.

</details>

---

### **PASO 2: Fórmula Fácil - Media Geométrica (PF1)**

Necesitas llenar la **columna D (PF1)** con la media geométrica de B y C.

**Prompt para la IA:**

```text
Necesito una fórmula Excel que calcule la media geométrica 
de dos números en las celdas B2 y C2.

Antes de darme la fórmula, explícame:
1. Qué es la media geométrica
2. Por qué es mejor que la media aritmética en este contexto
3. Cuál es la función Excel que la calcula
4. Qué pasa si uno de los valores es 0

Solo después de eso, dame la fórmula exacta.
```

**Lo importante:** Pides EXPLICACIÓN antes de la fórmula. Así entiendas qué hace.

<details>
    <summary>✅ Respuesta esperada (resumen)</summary>
<br>

La IA debería explicarte que:

- Media geométrica = raíz cuadrada del producto
- En administración educativa = penaliza más si una nota es muy baja
- Función: `=MEDIA.GEOM(B2:C2)` o `=POTENCIA(B2*C2; 0.5)`
- Si uno es 0 = el resultado es 0 (fórmula da error)

Luego:
```excel
=IFERROR(MEDIA.GEOM(B2:C2); 0)
```

Esto devuelve 0 si hay error (dato faltante).

</details>

**Tu turno:**
1. Abre un chat con ChatGPT o Claude
2. Copia el prompt anterior
3. Lee la explicación
4. Escribe la fórmula en D2
5. Copia la fórmula a D3:D20

---

### **PASO 3: Generalizar a PF2 y PF3**

Ahora que dominas media geométrica, necesitas:
- Columna G (PF2): Media geométrica de E y F
- Columna J (PF3): Media geométrica de H e I

**Pregunta a la IA:**

```text
Tengo fórmulas para calcular media geométrica en Excel.
Necesito aplicarlas a columnas diferentes:
- Columna D: media de B y C (ya hecha)
- Columna G: media de E y F (nueva)
- Columna J: media de H e I (nueva)

¿Cómo copio la estructura de la fórmula a columnas diferentes?
¿Hay algún patrón que deba seguir?
```

**Resultado esperado:** Las 3 columnas llenas con media geométrica.

---

### **PASO 4: Nota Final - La Fórmula Compleja**

Ahora llega la difícil. La **columna L (Nota_Final)** tiene lógica compleja:

```
Reglas:
1. Si alguna práctica final < 4 → Nota final = 0
2. Si promedio prácticas < 5 → Nota final = 0
3. Si examen < 4 → Nota final = 0
4. Si todas las condiciones pasan → Promedio ponderado:
   - Prácticas: 40%
   - Examen: 60%
5. Redondea a 2 decimales
```

**Prompt a la IA:**

```text
Necesito crear una fórmula EXCEL que calcule la nota final con estas reglas:

CONDICIONES PARA SUSPENDER (nota 0):
- Si D2 < 4 (práctica 1 insuficiente)
- Si G2 < 4 (práctica 2 insuficiente)  
- Si J2 < 4 (práctica 3 insuficiente)
- Si promedio de D, G, J < 5
- Si K2 < 4 (examen insuficiente)

SI TODAS PASAN:
- Calcula: (promedio de D, G, J) * 0.4 + K2 * 0.6
- Redondea a 2 decimales

Explícame paso a paso cómo construiría esto con IF anidados.
NO me des la fórmula aún, solo la estructura.
```

**Objetivo:** Que la IA te enseñe la LÓGICA, no solo el código.

<details>
    <summary>🚀 Pista (sin solución)</summary>
<br>

La estructura es aproximadamente:

```
SI(alguna_condición_falla)
  ENTONCES: 0
SINO:
  redondea(promedio * 0.4 + examen * 0.6; 2)
```

En Excel eso se hace con IF anidados o con una combinación de SI, O, Y.

La función O() verifica si CUALQUIER condición es verdadera.

</details>

---

### **PASO 5: Nota de Acta - Más Reglas**

La **columna M (Nota_Acta)** es parecida a Nota_Final, pero:

```
Reglas especiales de acta:
- Si falta algún dato → 0
- Si Nota_Final = 0 BUT promedio >= 4.5 → 4.5
- Si Nota_Final = 0 BUT promedio >= 4 < 4.5 → 4
- Si Nota_Final > 0 → Nota_Final (tal cual)
```

**Pregunta:**

```text
La nota de acta es DIFERENTE a la nota final.
Tiene reglas especiales para "presentados suspensos".

Explícame estas reglas y cómo las implementaría con SI().
¿Qué diferencia hay entre usar SI anidados vs usar LET()?
```

---

### **PASO 6: Retroalimentación Automática - El Reto Final**

La **columna N (Retro)** genera un mensaje personalizado:

```
"La nota final de la práctica 1 no supera el 4. 
No se puede hacer media con las prácticas 2 y 3.

No tienes aprobadas las prácticas. 
Necesitas al menos un 5 de media..."
```

Este es un ejercicio **muy avanzado** de concatenación condicional.

**Pregunta:**

```text
Necesito crear un mensaje de retroalimentación automático 
que SOLO muestre las razones por las que suspendió.

Las razones posibles son:
1. Práctica 1 final < 4
2. Práctica 2 final < 4
3. Práctica 3 final < 4
4. Promedio prácticas < 5
5. Examen < 4

¿Cómo construyo una fórmula que:
- Compruebe cada condición
- SOLO incluya los mensajes que apliquen
- Los concatene en un texto

¿Existe una función que haga esto automáticamente?
```

**Respuesta esperada:** UNIRCADENAS() o TEXTJOIN()

---

## 🔄 Variantes y Mejoras

### Variante 1: Otros Pesos
```
¿Qué pasaría si el ponderado fuera:
- Prácticas 50%
- Examen 50%
```

**Cambio:** Solo modifica los 0.4 y 0.6 en la fórmula.

### Variante 2: Mínimo en Examen
```
¿Qué si el mínimo en examen fuera 5 en lugar de 4?
```

**Cambio:** Modifica la condición K2 < 4 a K2 < 5

### Variante 3: Validaciones Adicionales
```
¿Y si quisieras que NO HAYA nota final 
si falta algún dato?
```

**Nuevo requisito:** Agrega validaciones con ESERROR()

---

## 🎯 Validación Final

Cuando termines:

1. **Descarga** la solución: `evaluacion_SOL.xlsx`
2. **Compara** tu archivo con la solución
3. **Verifica:** ¿Producen el mismo resultado?
4. **Revisa:** ¿Tus fórmulas son diferentes pero válidas?

> El 80% de fórmulas diferentes pueden ser correctas si producen el mismo resultado.

---

## 🚀 Reto Avanzado

**Para los que quieren más:**

1. **Auditoría automática**: Crea una columna O que valide que todas las fórmulas funcionan correctamente
2. **Gráfico dinámico**: Un gráfico que muestre distribución de notas
3. **Estadísticas**: Calcula media, mediana, moda de notas finales
4. **Exportación**: Crea un script que exporte solo los suspensos a un archivo nuevo

---

## ✅ Qué Hemos Aprendido

🎯 **Media geométrica** y por qué es importante  
🎯 **IF anidados** para lógica compleja  
🎯 **Funciones de error** como IFERROR  
🎯 **Concatenación** de textos condicionales  
🎯 **Uso de IA** para ENTENDER, no copiar  
🎯 **Validación** de fórmulas  

---

## 💡 Aplicación en Tu Trabajo

Este sistema se puede adaptar a:

- **Evaluación de proveedores**
- **Calificación de solicitudes**
- **Ranking de candidatos**
- **Puntuación de expedientes**
- **Evaluación de proyectos**

La técnica es universal.

---

## 📝 Siguiente Paso

Una vez domines esto:

1. Mira cómo un **Agente** (Bloque 3) podría hacer esto automáticamente
2. Imagina aplicarlo a datos reales de tu administración
3. Piensa en procesos repetitivos en tu puesto que podrían automatizarse

**El verdadero poder viene cuando combinas Excel + IA + Automatización.** 🚀
