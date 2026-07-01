# Formatos de Salida: Controlar Exactamente Cómo Presenta la IA

## Objetivo

Aprender a especificar el formato exacto en el que deseas la respuesta (JSON, CSV, tabla, lista, HTML) para procesarla fácilmente o presentarla profesionalmente.

### Qué vamos a aprender

- Qué es un formato de salida y por qué importa
- Formatos útiles en administración: JSON, CSV, Markdown, HTML, listas
- Cómo especificar el formato en tu prompt
- Cuándo usar cada formato
- Combinar formato con roles y contexto para máxima efectividad

---

## Ejemplo Guiado: Extrayendo Información de una Normativa

Necesitas extraer requisitos clave de una circular administrativa sobre subvenciones. El mismo contenido puede presentarse de formas completamente distintas según tu necesidad.

### Contenido base (mismo para todos los ejemplos)
"La subvención está dirigida a pymes en sector servicios. Requisitos: estar constituida hace 3+ años, facturación 2023 entre 100K y 2M, máximo 5 trabajadores. Documentos: balance, nóminas, declaración responsable. Plazo de solicitud: 15 días desde publicación en BOE. Dotación máxima 15.000€."

### Formato 1: Estructura de lectura fácil (Lista)
**Prompt:** "Extrae los requisitos principales en formato de lista numerada."

**Resultado:**
1. Pymes del sector servicios
2. Constituida hace 3+ años
3. Facturación 2023: 100K-2M€
4. Máximo 5 trabajadores
5. Plazo: 15 días desde BOE
6. Dotación máxima: 15.000€

**Uso ideal:** Compartir rápidamente con compañeros, checklist interno.

### Formato 2: Estructura importable en hoja de cálculo (CSV)
**Prompt:** "Extrae en formato CSV el requisito y su descripción."

**Resultado:**
```
Requisito,Descripción
Sector,Servicios
Antigüedad mínima,3 años
Facturación mínima,100000
Facturación máxima,2000000
Trabajadores máximos,5
Plazo solicitud,15 días
Dotación máxima,15000
```

**Uso ideal:** Importar a Excel, base de datos, procesar automáticamente.

### Formato 3: Estructura legible en tabla (Markdown)
**Prompt:** "Extrae en formato tabla Markdown."

**Resultado:**
| Requisito | Valor |
|-----------|-------|
| Sector | Servicios |
| Antigüedad | 3+ años |
| Facturación mínima | 100.000€ |
| Facturación máxima | 2.000.000€ |
| Trabajadores máximos | 5 |
| Plazo | 15 días |
| Dotación máxima | 15.000€ |

**Uso ideal:** Incrustar en informes, documentos, webs.

### Formato 4: Estructura procesable (JSON)
**Prompt:** "Extrae en formato JSON con estructura: { requisitos: { nombre: string, valor: string, tipo: string } }"

**Resultado:**
```json
{
  "subvención": {
    "sector": "Servicios",
    "requisitos": [
      {
        "nombre": "Antigüedad mínima",
        "valor": "3 años",
        "tipo": "temporal"
      },
      {
        "nombre": "Facturación 2023",
        "valor": "100.000€ - 2.000.000€",
        "tipo": "rango_numérico"
      }
    ],
    "plazo_solicitud": "15 días desde publicación BOE",
    "dotación_máxima": 15000
  }
}
```

**Uso ideal:** Alimentar bases de datos, integración con sistemas, procesamiento automático.

---

## Prompt Explicado

```text
Extrae [QUÉ EXTRAER] en formato [FORMATO ESPECÍFICO]:

[ESPECIFICACIÓN DEL FORMATO]

Contenido a procesar:
[CONTENIDO]
```

**Componentes clave:**
- **[QUÉ EXTRAER]:** Requisitos, plazos, contactos, criterios
- **[FORMATO ESPECÍFICO]:** JSON, CSV, Markdown tabla, HTML, lista numerada
- **[ESPECIFICACIÓN]:** Cómo debe estructurarse exactamente el formato
- **[CONTENIDO]:** El texto, documento o información a extraer

---

## Formatos Principales y Cuándo Usarlos

### 1. **Lista (Numerada o con viñetas)**
```text
Estructura los resultados como lista numerada.
Cada elemento debe ser claro y conciso.
```
**Cuándo:** Comunicación rápida, compartir con no técnicos, presentaciones.

### 2. **CSV (Comma Separated Values)**
```text
Formato CSV con campos: [nombre campo 1], [nombre campo 2], [nombre campo 3]
Usa ";" como separador.
Incluye encabezado.
```
**Cuándo:** Importar a Excel, base de datos, procesamiento automático.

### 3. **Tabla Markdown**
```text
Formato tabla Markdown:
| Encabezado 1 | Encabezado 2 | Encabezado 3 |
|---|---|---|
| dato | dato | dato |
```
**Cuándo:** Informes técnicos, documentación, webs, wikis.

### 4. **JSON (JavaScript Object Notation)**
```text
Formato JSON con esta estructura:
{
  "campo1": "valor",
  "campo2": [
    { "subelemento1": "valor", "subelemento2": "valor" }
  ]
}
```
**Cuándo:** Integración sistemas, APIs, procesamiento programático.

### 5. **HTML**
```text
Formato HTML, incluyendo estructura básica.
Usa clases CSS: .requisito, .obligatorio, .opcional
```
**Cuándo:** Publicar en web, integración en portales.

### 6. **Estructura jerárquica (anidada)**
```text
Formato jerárquico con indentación:
- Sección A
  - Subsección A1
    - Detalle
  - Subsección A2
- Sección B
```
**Cuándo:** Información con múltiples niveles, procesos secuenciales.

---

## Variantes y Combinaciones Poderosas

### Variante 1: Formato + Rol + Contenido
```text
Actúa como Auditor Administrativo. 
Analiza esta solicitud de subvención y devuelve en formato JSON 
con campos: riesgo_nivel, descripción, recomendación, documentación_necesaria.
```

### Variante 2: Formato con especificación strict
```text
Devuelve en CSV con exactamente 5 columnas:
1. Requisito
2. Descripción
3. Obligatorio (Sí/No)
4. Documento probatorio
5. Validable
```

### Variante 3: Formato con filtros
```text
De la normativa, extrae solo requisitos "Obligatorio=Sí" 
y devuelve en lista numerada, priorizados por importancia.
```

---

## Ejercicio

**Situación:**
Tu organización ha recibido un informe de auditoría con 23 hallazgos. Necesitas presentar esta información a diferentes públicos con diferentes formatos.

**Hallazgos crudos (muestra):**
```
H1: No existe registro formal de asistencia. Riesgo: medio. 
Causa: Falta protocolo. Recomendación: Implementar sistema.

H2: Desviación presupuestaria 8%. Riesgo: alto. 
Causa: Falta de estimación. Recomendación: Mejorar planificación.

H3: No hay segregación de funciones en pagos. Riesgo: alto. 
Causa: Personal reducido. Recomendación: Revisar arquitectura proceso.
```

**Tu tarea:**
1. Extrae los 3 hallazgos en **Formato 1: Lista numerada** (para presentación verbal a directiva)
2. Extrae los 3 hallazgos en **Formato 2: CSV** (para importar a Excel y análisis)
3. Extrae los 3 hallazgos en **Formato 3: JSON** (si fuera para un sistema de seguimiento)

**Instrucciones:**
- Mantén solo información esencial
- Normaliza términos (Alto→3, Medio→2, Bajo→1)
- En JSON, añade campo "id" y "estado" (pendiente/en_progreso/cerrado)

**Tiempo:** 20 minutos

---

## Solución Orientativa

<details>
  <summary>¿Quieres ver cómo estructurar cada formato?</summary>

### Formato 1: Lista para presentación verbal
```text
Extrae los hallazgos del informe en formato de lista numerada simple y clara.
Cada hallazgo debe incluir: descripción, nivel de riesgo, causa, y recomendación.

Hallazgos a extraer:
[los 3 hallazgos]
```

**Resultado esperado:**
```
1. Falta de registro formal de asistencia
   - Riesgo: Medio
   - Causa: Ausencia de protocolo
   - Recomendación: Implementar sistema de registro

2. Desviación presupuestaria del 8%
   - Riesgo: Alto
   - Causa: Falta de estimación presupuestaria adecuada
   - Recomendación: Mejorar proceso de planificación financiera

3. Inexistencia de segregación de funciones en pagos
   - Riesgo: Alto
   - Causa: Recursos humanos limitados
   - Recomendación: Revisar y rediseñar arquitectura del proceso
```

### Formato 2: CSV para Excel
```text
Extrae en formato CSV con separador ";" 
Campos: ID, Hallazgo, Descripción, RiesgoNivel, Causa, Recomendación, Estado

Usa esta codificación:
- RiesgoNivel: 1=Bajo, 2=Medio, 3=Alto
- Estado: pendiente/en_progreso/cerrado
```

**Resultado esperado:**
```
ID;Hallazgo;Descripción;RiesgoNivel;Causa;Recomendación;Estado
H1;Falta registro asistencia;No existe registro formal de asistencia;2;Ausencia de protocolo;Implementar sistema de registro;pendiente
H2;Desviación presupuestaria;Desviación 8% del presupuesto;3;Falta de estimación;Mejorar planificación presupuestaria;pendiente
H3;Sin segregación funciones;No hay segregación en proceso de pagos;3;Personal reducido;Revisar arquitectura proceso;en_progreso
```

### Formato 3: JSON para sistema
```text
Extrae en formato JSON. 
Estructura:
{
  "hallazgos": [
    {
      "id": "string",
      "título": "string",
      "descripción": "string",
      "riesgo": { "nivel": número 1-3, "etiqueta": "string" },
      "causa": "string",
      "recomendación": "string",
      "estado": "string"
    }
  ]
}
```

**Resultado esperado:**
```json
{
  "hallazgos": [
    {
      "id": "H1",
      "título": "Falta de registro formal de asistencia",
      "descripción": "No existe registro formal de asistencia del personal",
      "riesgo": {
        "nivel": 2,
        "etiqueta": "Medio"
      },
      "causa": "Ausencia de protocolo establecido",
      "recomendación": "Implementar sistema de registro de asistencia",
      "estado": "pendiente"
    },
    {
      "id": "H2",
      "título": "Desviación presupuestaria",
      "descripción": "Desviación del 8% respecto al presupuesto aprobado",
      "riesgo": {
        "nivel": 3,
        "etiqueta": "Alto"
      },
      "causa": "Falta de estimación presupuestaria adecuada",
      "recomendación": "Mejorar el proceso de planificación presupuestaria",
      "estado": "pendiente"
    },
    {
      "id": "H3",
      "título": "Inexistencia de segregación de funciones en pagos",
      "descripción": "No hay segregación de funciones en el proceso de pagos",
      "riesgo": {
        "nivel": 3,
        "etiqueta": "Alto"
      },
      "causa": "Recursos humanos limitados en la organización",
      "recomendación": "Revisar y rediseñar la arquitectura del proceso",
      "estado": "en_progreso"
    }
  ]
}
```

**Ventaja de JSON:** Puedes alimentar una base de datos o dashboard que actualice automáticamente el estado de cada hallazgo.

</details>

---

## Reto Avanzado

**Nivel: Experto**

Crea un prompt que:
1. Extrae información de un documento normativo
2. La estructura en **3 formatos simultáneamente**: Lista, CSV y JSON
3. El prompt debe ser único (no 3 prompts separados)

Pista: Usa delimitadores claros como "---FORMATO: LISTA---", "---FORMATO: CSV---", etc.

Ejemplo esperado: Una única respuesta que contenga la misma información en 3 formatos distinguibles.

---

## Qué Hemos Aprendido

✅ **El formato importa tanto como el contenido:** La información correcta en formato incorrecto es inútil.

✅ **Diferentes públicos, diferentes formatos:** Tu jefe prefiere listas, Excel prefiere CSV, sistemas prefieren JSON.

✅ **Automatización mediante formato:** CSV y JSON permiten integración automática con otros sistemas.

✅ **Especificidad en prompts:** Indicar exactamente qué formato evita malinterpretaciones.

✅ **Combinación de técnicas:** Roles + Formatos = análisis perspectivado Y estructurado perfectamente.

✅ **Ahorro de tiempo:** Una vez extraído en formato correcto, se procesa automáticamente sin reescrituras.

**Próximo paso:** Combina Roles + Formatos con Chain of Thought (documento siguiente) para razonamientos complejos estructurados exactamente como los necesitas.
