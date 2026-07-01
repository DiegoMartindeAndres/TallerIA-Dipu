# 📐 Anatomía de Prompts para Imágenes

📌 **Objetivo**: Entender cómo funcionan los prompts para generadores de imágenes y por qué algunos funcionan mejor que otros.

## 📚 Qué vamos a aprender

- Las 7 dimensiones de un buen prompt de imagen
- Por qué "haz una imagen bonita" no funciona
- Cómo escribir prompts reproducibles
- Errores comunes

---

## 🧠 Ejemplo guiado: De malo a excelente

### ❌ Prompt vago (resultado impredecible):
```text
Un cartel para un curso de IA
```

**Resultado esperado**: Probablemente feo. La IA adivina.

---

### ✅ Prompt estructurado (resultado profesional):
```text
A professional training poster with:
- Subject: AI course for public administration
- Style: Modern flat design with geometric shapes
- Colors: Gradient from deep blue (#003366) to light cyan (#00CCFF)
- Layout: Top half for eye-catching graphics, bottom half for text
- Text: "Artificial Intelligence for Public Administration" in bold sans-serif
- Mood: Professional, accessible, innovative
- Target audience: Administrative staff
- Composition: Centered, balanced
- Aspect ratio: Vertical (1024x1024)
- Quality: High-definition, print-ready
```

**Resultado esperado**: Profesional, coherente, utilizable.

---

## 💬 Las 7 Dimensiones de un Buen Prompt de Imagen

### 1️⃣ TIPO DE TRABAJO (What)
Qué tipo de imagen quieres generar.

**Ejemplos:**
```text
A poster for...
A book cover featuring...
An infographic showing...
A promotional banner with...
A website hero image...
```

### 2️⃣ CONTEXTO (Why)
Para qué sirve. Ayuda a la IA a entender el propósito.

**Ejemplos:**
```text
For a tech company website
For a training course
For social media marketing
For a printed brochure
For an internal presentation
```

### 3️⃣ ESTILO VISUAL (How it looks)
Qué movimiento artístico, técnica o referencia.

**Ejemplos:**
```text
Modern minimalist design
Watercolor illustration
3D render
Photorealistic
Vector art
Infographic style
```

### 4️⃣ PALETA DE COLORES (Color palette)
Colores dominantes. Sé específico: nombres o códigos hex.

**Ejemplos:**
```text
Blue and white
Warm earth tones: beige, terracotta, ochre
Gradient from purple to pink
Monochromatic grayscale
High contrast black and neon green
```

### 5️⃣ COMPOSICIÓN (Layout)
Cómo está organizado visualmente.

**Ejemplos:**
```text
Centered composition with symmetry
Diagonal layout with movement
Grid-based design
Z-pattern flow
Left-aligned with breathing room on right
```

### 6️⃣ ELEMENTOS ESPECÍFICOS (Details)
Qué elementos incluir o excluir.

**Ejemplos:**
```text
Include: icons, graphs, human figures
Exclude: text, people, complex backgrounds
Features: bold typography, subtle shadows, geometric shapes
```

### 7️⃣ TONO EMOCIONAL (Mood)
Qué siente la persona que lo ve.

**Ejemplos:**
```text
Professional and trustworthy
Fun and playful
Serious and authoritative
Innovative and cutting-edge
Warm and welcoming
```

---

## 🔄 Comparación: Antes y Después

### CASO 1: Cartel de un curso

#### ❌ Vago:
```text
Un cartel para un curso de inteligencia artificial
```

#### ✅ Optimizado:
```text
A professional course poster featuring:
- Title: "Master Artificial Intelligence"
- Style: Modern flat design with geometric elements
- Colors: Deep blue (#0052CC), lime green (#00DC82), white background
- Layout: Centered title at top, three feature icons in middle, 
  call-to-action button at bottom
- Mood: Inspiring, accessible, cutting-edge
- Target: Adults in tech and business
- Format: Vertical poster (1024x1024), print-ready
```

---

## 🎯 Ejercicio

**Tu turno**: Toma este prompt vago y conviértelo en uno estructurado.

```text
Vago: "Un cartel sobre IA para empleados públicos"
```

Piensa en:
1. ¿Qué tipo de trabajo es?
2. ¿Para qué sirve?
3. ¿Qué estilo visual?
4. ¿Qué colores?
5. ¿Qué composición?
6. ¿Qué elementos?
7. ¿Qué tono?

<details>
    <summary>¿Quieres una solución orientativa?</summary>

```text
A professional awareness poster for public administration staff:
- Headline: "Artificial Intelligence: A Tool for Better Service"
- Style: Clean corporate design with modern typography
- Colors: Government blue (#003D7A), warm orange (#FF8C00) accents, white
- Layout: Left 40% for image/icon, right 60% for text
- Key visual: AI symbol (circuit board pattern or neural network)
- Mood: Trustworthy, professional, not intimidating
- Target: Administrative staff with varying tech comfort
- Format: A4 landscape (1024x576), suitable for printing and digital display
- Typography: Sans-serif, high contrast for readability
```

</details>

---

## 🚀 Reto avanzado

Elige **uno de estos escenarios** y escribe un prompt estructurado de 7 dimensiones:

1. **Cartel**: "Seguridad cibernética en el trabajo"
2. **Portada de guía**: Manual de uso de herramientas de IA
3. **Bannerpara web**: "Transformación digital de la administración"
4. **Infografía**: Pasos para usar ChatGPT correctamente

---

## ✅ Qué hemos aprendido

✓ Los prompts de imagen tienen **7 dimensiones clave**
✓ La especificidad genera mejores resultados
✓ El contexto y el propósito importan
✓ La emoción es tan importante como la estética

**Siguiente**: 03-Estilos-y-Efectos.md para dominar estilos visuales
