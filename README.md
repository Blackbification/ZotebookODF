# 📚 ZotebookODF

**Exporta respuestas de NotebookLM con citas académicas formales y bibliografía automática**

[![Chrome Extension](https://img.shields.io/badge/Chrome-Extension-4285F4?logo=googlechrome&logoColor=white)](https://github.com/tu-usuario/ZotebookODF)
[![License: AGPL v3](https://img.shields.io/badge/License-AGPL%20v3-blue.svg)](https://www.gnu.org/licenses/agpl-3.0)
[![Version](https://img.shields.io/badge/Version-1.0.0-green)]()

---

## 🎯 ¿Qué problema resuelve?

**NotebookLM** de Google es genial para analizar papers científicos. Pero tiene un problema: las citas son números genéricos (1, 2, 3...) que **no sirven para documentos académicos**.

### Antes (NotebookLM):
```
El ejercicio mejora la salud en pacientes con AR 1, 2, confirmando 
que la intensidad moderada es segura 3, 4, 5.
```

### Después (con ZotebookODF):
```
El ejercicio mejora la salud en pacientes con AR [1], [2], confirmando 
que la intensidad moderada es segura [3].

──────────────────────────────────────────

Referencias

[1] Jahanbin I, Hoseini Moghadam M, Nazarinia M, Ghodsbin F, Bagheri Z, 
    Ashraf A. The Effect of Conditioning Exercise on the Health Status 
    and Pain in Patients with Rheumatoid Arthritis. Int J Community 
    Based Nurs Midwifery. 2014;2(3):169-76.

[2] Lange E, Kucharski D, Svedlund S, et al. Effects of Aerobic and 
    Resistance Exercise in Older Adults With Rheumatoid Arthritis. 
    Arthritis Care Res. 2019;71(1):61-70. doi:10.1002/acr.23589

[3] Li Z, Wang XQ. Clinical effect and biological mechanism of exercise 
    for rheumatoid arthritis: A mini review. Front Immunol. 2023;13:1089621.
```

---

## ✨ ¿Qué hace ZotebookODF?

- ✅ **Captura citas** haciendo clic en los números de NotebookLM
- ✅ **Cruza con tu biblioteca de Zotero** para obtener metadatos completos
- ✅ **Genera bibliografía automática** (Vancouver, APA, Harvard)
- ✅ **Colapsa citas duplicadas**: `[2], [2], [2]` → `[2]`
- ✅ **Exporta para Zotero ODF Scan** → citas activas en Word

---

# 📋 REQUISITOS PREVIOS

Antes de instalar ZotebookODF, necesitas tener:

### 1. Google Chrome
- Descarga: https://www.google.com/chrome/

### 2. Zotero (versión escritorio)
- Descarga: https://www.zotero.org/download/
- Instálalo y crea tu biblioteca de referencias

### 3. Better BibTeX para Zotero (RECOMENDADO)
Este plugin genera automáticamente los "citation keys" que ZotebookODF necesita.

**Instalación:**
1. Descarga el archivo `.xpi` desde: https://retorque.re/zotero-better-bibtex/installation/
2. En Zotero: **Herramientas** → **Complementos**
3. Clic en el engranaje ⚙️ → **"Instalar complemento desde archivo..."**
4. Selecciona el archivo `.xpi` descargado
5. Reinicia Zotero

### 4. Plugin ODF Scan para Zotero (si quieres citas activas)
**Solo necesario si quieres convertir las citas en citas activas de Zotero en Word.**

**Instalación:**
1. Ve a: https://zotero-odf-scan.github.io/zotero-odf-scan/
2. Descarga el archivo `.xpi`
3. En Zotero: **Herramientas** → **Complementos**
4. Clic en el engranaje ⚙️ → **"Instalar complemento desde archivo..."**
5. Selecciona el archivo `.xpi` descargado
6. Reinicia Zotero
7. Verifica: debe aparecer **"ODF Scan"** en el menú **Herramientas**

### 5. Plugin de Zotero para Word (si quieres citas activas)
**Para que las citas activas funcionen en Word.**

**Instalación:**
1. En Zotero: **Editar** → **Preferencias** → **Citar**
2. Pestaña **"Procesadores de texto"**
3. Clic en **"Instalar complemento de Microsoft Word"**
4. Reinicia Word
5. Verifica: debe aparecer una pestaña **"Zotero"** en Word

---

# 🚀 INSTALACIÓN DE ZOTEBOOKODF

## Paso 1: Descarga la extensión

1. Ve a la página del proyecto en GitHub
2. Haz clic en el botón verde **"< > Code"**
3. Selecciona **"Download ZIP"**
4. Se descargará un archivo `ZotebookODF-main.zip`

## Paso 2: Descomprime el archivo

### En Windows:
1. Ve a tu carpeta de **Descargas**
2. Haz clic derecho sobre `ZotebookODF-main.zip`
3. Selecciona **"Extraer todo..."**
4. Haz clic en **"Extraer"**
5. Se creará una carpeta llamada `ZotebookODF-main`

### En Mac:
1. Ve a tu carpeta de **Descargas**
2. Haz doble clic sobre `ZotebookODF-main.zip`
3. Se creará automáticamente una carpeta `ZotebookODF-main`

## Paso 3: Instala la extensión en Chrome

1. Abre **Google Chrome**
2. En la barra de direcciones, escribe: `chrome://extensions`
3. Pulsa **Enter**
4. En la esquina superior derecha, activa el **"Modo de desarrollador"** (el interruptor)
5. Aparecerán nuevos botones. Haz clic en **"Cargar descomprimida"**
6. Navega hasta la carpeta `ZotebookODF-main` que descomprimiste
7. Selecciona la carpeta y haz clic en **"Seleccionar carpeta"**

✅ **¡Listo!** Verás el icono 📚 en tu barra de extensiones de Chrome.

**Tip:** Si no ves el icono, haz clic en el icono de puzzle 🧩 en Chrome y fija ZotebookODF.

---

# 📖 GUÍA DE USO COMPLETA

## PARTE 1: Preparación (solo la primera vez)

### 1.1 Exporta tu biblioteca de Zotero

1. Abre **Zotero** en tu ordenador
2. En el panel izquierdo, haz clic derecho sobre la **carpeta/colección** que contiene los papers que vas a usar en NotebookLM
3. Selecciona **"Exportar colección..."**
4. En el menú desplegable "Formato", selecciona **"CSL JSON"**
5. Haz clic en **"OK"**
6. Elige dónde guardar el archivo (por ejemplo: `mis-papers.json`)
7. Haz clic en **"Guardar"**

**⚠️ IMPORTANTE:** 
- Exporta SOLO la colección que contiene los papers que subiste a NotebookLM
- Si añades más papers a NotebookLM, vuelve a exportar el JSON

### 1.2 Carga el JSON en ZotebookODF

1. Abre **NotebookLM** en Chrome: https://notebooklm.google.com
2. Haz clic en el icono 📚 de **ZotebookODF** en la barra de extensiones
3. En la sección **"1. Biblioteca Zotero"**, haz clic en **"📁 Cargar JSON"**
4. Selecciona el archivo `.json` que exportaste de Zotero
5. Verás el mensaje **"✓ X referencias"** confirmando que se cargó

---

## PARTE 2: Captura de citas en NotebookLM

### 2.1 Genera una respuesta con citas

1. En NotebookLM, abre tu cuaderno con los papers
2. Escribe una pregunta en el chat
3. NotebookLM generará una respuesta con números de cita: `1`, `2`, `3`...

### 2.2 Captura cada cita

**Este paso es FUNDAMENTAL:**

1. En la respuesta de NotebookLM, **haz clic en cada número** de cita (1, 2, 3...)
2. Aparecerá un popup mostrando el título del paper
3. ZotebookODF captura automáticamente esa información
4. Repite para TODOS los números de cita que quieras incluir

**Verifica:** En el popup de ZotebookODF, la sección **"2. Referencias capturadas"** mostrará cuántas has capturado.

**⚠️ IMPORTANTE:**
- Debes hacer clic en CADA número que quieras citar
- Si no haces clic en un número, ZotebookODF no sabrá a qué paper corresponde
- Puedes hacer clic en **🔄** para actualizar si algo no aparece

---

## PARTE 3: Exportación

### Opción A: Copiar texto formateado (la más fácil)

**Usa esta opción si solo quieres el texto con citas y bibliografía para pegarlo.**

1. En ZotebookODF, selecciona el **estilo de citación**:
   - **Vancouver**: [1], [2], [3] — ideal para medicina
   - **APA**: (Autor et al., 2019) — ideal para psicología
   - **Harvard**: (Autor et al. 2019) — uso general

2. Haz clic en **"📋 Copiar todo"**

3. El texto con citas + bibliografía está en tu portapapeles

4. Pégalo donde quieras (**Ctrl+V** o **Cmd+V**):
   - Microsoft Word
   - Google Docs
   - Cualquier editor de texto

✅ **Resultado:** Texto con citas formateadas y bibliografía lista.

---

### Opción B: Exportar para Zotero ODF Scan (citas activas)

**Usa esta opción si quieres citas ACTIVAS que puedas gestionar desde Zotero.**

#### Paso B.1: Exporta desde ZotebookODF

1. En ZotebookODF, haz clic en **"📥 TXT para Zotero ODF Scan"**
2. Se descargará un archivo `notebooklm-para-zotero.txt`

#### Paso B.2: Prepara el documento en Word

1. Abre el archivo `notebooklm-para-zotero.txt` con el **Bloc de notas**
2. Selecciona todo el texto: **Ctrl+A**
3. Copia: **Ctrl+C**
4. Abre **Microsoft Word**
5. Pega el texto: **Ctrl+V**
6. Guarda el documento como **Word (.docx)**:
   - **Archivo** → **Guardar como**
   - Elige ubicación
   - Asegúrate de que el formato sea **"Documento de Word (*.docx)"**
   - Haz clic en **Guardar**

#### Paso B.3: Ejecuta ODF Scan en Zotero

1. Abre **Zotero**
2. Ve a **Herramientas** → **ODF Scan...**
3. En el diálogo que aparece:
   - **File type:** selecciona **"Pandoc -> Zotero citations"**
   - **Input file:** haz clic en "Browse" y selecciona el `.docx` que guardaste
   - **Output file:** elige dónde guardar el resultado (puede ser el mismo nombre con "-cited" al final)
4. Haz clic en **"Next"**
5. ODF Scan escaneará el documento y detectará los marcadores `[@citekey]`
6. Haz clic en **"Next"** y luego **"Done"**

#### Paso B.4: Configura el estilo de citación en Word

1. Abre el documento resultante en **Word**
2. Verás que las citas ahora son campos de Zotero (se resaltan en gris al hacer clic)
3. En la pestaña **Zotero** de Word:
   - Haz clic en **"Document Preferences"**
   - Selecciona el **estilo de citación** que quieras (Vancouver, APA, etc.)
   - Haz clic en **OK**
4. Las citas se transformarán al formato elegido

#### Paso B.5: Añade la bibliografía

1. Coloca el cursor donde quieras la bibliografía (normalmente al final)
2. En la pestaña **Zotero** de Word, haz clic en **"Add/Edit Bibliography"**
3. Zotero generará automáticamente la bibliografía

✅ **Resultado:** Documento con citas activas vinculadas a Zotero. Puedes cambiar el estilo con un clic y la bibliografía se actualiza automáticamente.

---

## 🎨 Estilos de citación disponibles

| Estilo | Formato en texto | Ideal para |
|--------|------------------|------------|
| **Vancouver** | [1], [2], [3] | Medicina, biomedicina, enfermería |
| **APA** | (Lange et al., 2019) | Psicología, educación, ciencias sociales |
| **Harvard** | (Lange et al. 2019) | Uso general, negocios |

---

## ❓ Solución de problemas

### "No se capturan las citas"
- **Causa:** No hiciste clic en los números de cita en NotebookLM
- **Solución:** Haz clic directamente sobre cada número (1, 2, 3...) en la respuesta de NotebookLM

### "La bibliografía no muestra todos los datos"
- **Causa:** El JSON de Zotero no tiene los metadatos completos
- **Solución:** Asegúrate de que los items en Zotero tienen título, autores, año y revista

### "ODF Scan no reconoce las citas"
- **Causa:** El formato del marcador no es correcto
- **Solución:** Asegúrate de seleccionar **"Pandoc -> Zotero citations"** en ODF Scan

### "No veo la pestaña Zotero en Word"
- **Causa:** El plugin de Word no está instalado
- **Solución:** En Zotero: Editar → Preferencias → Citar → "Instalar complemento de Microsoft Word"

### "Los citation keys no coinciden"
- **Causa:** Better BibTeX no está instalado o los keys son diferentes
- **Solución:** Instala Better BibTeX y vuelve a exportar el JSON

---

## 📁 Estructura del proyecto

```
ZotebookODF/
├── manifest.json       # Configuración de la extensión
├── popup.html          # Interfaz del popup
├── src/
│   ├── content.js      # Script inyectado en NotebookLM
│   ├── popup.js        # Lógica del popup
│   └── background.js   # Service worker
├── styles/
│   ├── popup.css       # Estilos del popup
│   └── content.css     # Estilos inyectados
└── icons/              # Iconos de la extensión
```

---

## 📜 Licencia

**AGPL-3.0** - La misma licencia que Zotero.

Puedes usar, modificar y distribuir este software. Si lo modificas y lo distribuyes, debes compartir tu código bajo la misma licencia.

---

## 👤 Autor

**Juan**  
- Médico Internista | Hospital Universitario de Jerez
- Profesor Asociado | Universidad de Cádiz
- Antiexperto en IA y Salud

---

## 🙏 Agradecimientos

- [NotebookLM](https://notebooklm.google.com) de Google
- [Zotero](https://www.zotero.org/) - Gestor de referencias open source
- [Better BibTeX](https://retorque.re/zotero-better-bibtex/) - Plugin esencial para citation keys
- [ODF Scan](https://zotero-odf-scan.github.io/zotero-odf-scan/) - Conversión a citas activas
- Claude (Anthropic) - Asistencia en desarrollo

---

<p align="center">
  <b>⭐ Si te resulta útil, ¡dale una estrella al repo!</b>
</p>

<p align="center">
  <i>Hecho con ❤️ para la comunidad de investigadores</i>
</p>
