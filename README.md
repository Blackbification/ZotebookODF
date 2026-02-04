# 📚 ZotebookODF

**Exporta respuestas de NotebookLM con citas académicas formales**

[![Chrome Extension](https://img.shields.io/badge/Chrome-Extension-4285F4?logo=googlechrome&logoColor=white)](https://github.com/tu-usuario/ZotebookODF)
[![License: AGPL v3](https://img.shields.io/badge/License-AGPL%20v3-blue.svg)](https://www.gnu.org/licenses/agpl-3.0)
[![Version](https://img.shields.io/badge/Version-1.0.0-green)]()

---

## 🎯 ¿Qué problema resuelve?

**NotebookLM** de Google es genial para analizar papers. Pero las citas son números genéricos (1, 2, 3...) que no sirven para documentos académicos.

**ZotebookODF** convierte esto:
```
El ejercicio mejora la salud 1, 2, confirmando que es seguro 3, 4, 5.
```

En esto:
```
El ejercicio mejora la salud [1], [2], confirmando que es seguro [3].

Referencias
[1] Jahanbin et al. The Effect of Conditioning Exercise... 2014.
[2] Lange et al. Effects of Aerobic and Resistance Exercise... 2019.
[3] Li & Wang. Clinical effect and biological mechanism... 2023.
```

---

## ✨ Funcionalidades

- ✅ Captura citas haciendo clic en los números
- ✅ Cruza con tu biblioteca de Zotero
- ✅ Genera bibliografía automática (Vancouver, APA, Harvard)
- ✅ Colapsa citas duplicadas: `[2], [2], [2]` → `[2]`
- ✅ Exporta para Zotero ODF Scan (citas activas)

---

# 🚀 GUÍA DE INSTALACIÓN (paso a paso)

## Paso 1: Descarga la extensión

1. Ve a la página del proyecto en GitHub
2. Haz clic en el botón verde **"Code"**
3. Selecciona **"Download ZIP"**
4. Se descargará un archivo llamado `ZotebookODF-main.zip`

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
2. Escribe en la barra de direcciones: `chrome://extensions`
3. Pulsa **Enter**
4. Activa el **"Modo de desarrollador"** (interruptor en la esquina superior derecha)
5. Haz clic en **"Cargar descomprimida"**
6. Busca y selecciona la carpeta `ZotebookODF-main` que descomprimiste
7. Haz clic en **"Seleccionar carpeta"**

✅ **¡Listo!** Verás el icono 📚 en tu barra de extensiones de Chrome.

---

# 📖 GUÍA DE USO

## Preparación: Exporta tu biblioteca de Zotero

Antes de usar ZotebookODF, necesitas exportar los papers que vas a usar:

1. Abre **Zotero** en tu ordenador
2. Haz clic derecho sobre la carpeta/colección con tus papers
3. Selecciona **"Exportar colección..."**
4. En "Formato", selecciona **"CSL JSON"**
5. Haz clic en **"OK"**
6. Guarda el archivo (por ejemplo: `mis-papers.json`)

## Uso de ZotebookODF

### 1️⃣ Carga tu biblioteca

1. Abre **NotebookLM** en Chrome (notebooklm.google.com)
2. Haz clic en el icono 📚 de ZotebookODF
3. En la sección "Biblioteca Zotero", haz clic en **"📁 Cargar JSON"**
4. Selecciona el archivo que exportaste de Zotero
5. Verás "✓ X referencias" cuando se cargue correctamente

### 2️⃣ Captura las citas

1. En NotebookLM, haz una pregunta sobre tus papers
2. Cuando aparezca la respuesta con números (1, 2, 3...)
3. **Haz clic en cada número** para que ZotebookODF capture qué paper es
4. El contador de "Referencias capturadas" irá aumentando

### 3️⃣ Exporta

Tienes dos opciones:

**📋 Copiar todo** (la más fácil):
- Haz clic en "📋 Copiar todo"
- Pega directamente en Word, Google Docs, o donde quieras
- Incluye el texto con citas `[1], [2]` y la bibliografía

**📥 TXT para Zotero ODF Scan** (para citas activas):
- Haz clic en "📥 TXT para Zotero ODF Scan"
- Se descarga un archivo `.txt`
- Sigue las instrucciones de ODF Scan (ver abajo)

---

## 🔄 Cómo usar ODF Scan (citas activas en Word)

ODF Scan convierte los marcadores `[@citekey]` en citas activas de Zotero que puedes gestionar y actualizar.

### Requisito previo: Instala el plugin ODF Scan

**ODF Scan NO viene instalado por defecto en Zotero.** Tienes que descargarlo:

1. Ve a la página oficial: https://zotero-odf-scan.github.io/zotero-odf-scan/
2. Descarga el archivo `.xpi` correspondiente a tu versión de Zotero
3. En Zotero: **Herramientas** → **Extensiones** (o **Add-ons**)
4. Clic en el icono de engranaje ⚙️ → **"Install Add-on From File..."**
5. Selecciona el archivo `.xpi` que descargaste
6. Reinicia Zotero

✅ Ahora verás la opción **"ODF/RTF Scan..."** en el menú Herramientas.

### Paso 1: Prepara el documento

1. Haz clic en **"📥 TXT para Zotero ODF Scan"** en ZotebookODF
2. Se descarga un archivo `notebooklm-para-zotero.txt`
3. Abre el archivo `.txt` con el Bloc de notas o cualquier editor
4. Copia todo el contenido (**Ctrl+A**, luego **Ctrl+C**)
5. Abre **Microsoft Word**
6. Pega el contenido (**Ctrl+V**)
7. **Guarda como documento de Word (.docx)** - Esto es importante, NO guardes como .txt

### Paso 2: Escanea con ODF Scan

1. Abre **Zotero**
2. Ve a **Herramientas** → **ODF/RTF Scan...**
3. En **"Input file"**: selecciona el `.docx` que acabas de guardar
4. En **"Output file"**: elige dónde guardar el resultado (puede ser el mismo archivo u otro nuevo)
5. Haz clic en **"Next"**
6. Zotero escaneará el documento y detectará los marcadores `[@citekey]`
7. Te mostrará las citas encontradas - verifica que coincidan
8. Haz clic en **"Next"** y luego **"Finish"**

### Paso 3: Configura el estilo de citación

Ahora tienes un documento con citas de Zotero, pero necesitas elegir el formato:

1. Abre el documento resultante en **Word**
2. Ve a la pestaña **Zotero** en Word (si tienes el plugin de Word instalado)
3. Haz clic en **"Document Preferences"**
4. Selecciona el **estilo de citación** que quieras (Vancouver, APA, etc.)
5. Haz clic en **"OK"**
6. Las citas se transformarán automáticamente al formato elegido

### Paso 4: Añade la bibliografía

1. Coloca el cursor donde quieras la bibliografía (normalmente al final)
2. En la pestaña Zotero de Word, haz clic en **"Add/Edit Bibliography"**
3. ¡Zotero genera la bibliografía automáticamente!

✅ **¡Listo!** Ahora tienes un documento con:
- Citas activas vinculadas a Zotero
- Posibilidad de cambiar el estilo con un clic
- Bibliografía que se actualiza automáticamente

---

### 💡 Consejo: Si no tienes el plugin de Word para Zotero

Si no ves la pestaña "Zotero" en Word:

1. Abre **Zotero**
2. Ve a **Editar** → **Preferencias** → **Citar**
3. Haz clic en **"Instalar complemento de Microsoft Word"**
4. Reinicia Word

---

## 🎨 Estilos de citación

| Estilo | Formato | Ideal para |
|--------|---------|------------|
| **Vancouver** | `[1], [2], [3]` | Medicina, biomedicina |
| **APA** | `(Lange et al., 2019)` | Psicología, educación |
| **Harvard** | `(Lange et al. 2019)` | General |

---

## ❓ Problemas frecuentes

### "No se capturan las citas"
- Asegúrate de hacer clic directamente sobre el número en NotebookLM
- Espera a que aparezca el popup con el título del paper
- Si no aparece, haz clic de nuevo

### "No aparece la bibliografía"
- Verifica que cargaste el archivo JSON de Zotero
- Comprueba que el JSON incluye los papers que estás citando

### "Los números no coinciden"
- Esto es normal. NotebookLM usa números arbitrarios
- ZotebookODF los reorganiza automáticamente

---

## 📜 Licencia

AGPL-3.0 License - Igual que Zotero.

Puedes usarlo, modificarlo y distribuirlo. Si lo modificas y lo distribuyes, tienes que compartir tu código.

---

## 👤 Autor

**Juan**  
- Médico Internista | Hospital Universitario de Jerez
- Profesor Asociado | Universidad de Cádiz
- Antiexperto en IA y Salud

---

## 🙏 Agradecimientos

- [NotebookLM](https://notebooklm.google.com) de Google
- [Zotero](https://www.zotero.org/) - Gestor de referencias
- Claude (Anthropic) - Asistencia en desarrollo

---

<p align="center">
  <b>⭐ Si te resulta útil, ¡dale una estrella al repo!</b>
</p>

<p align="center">
  <i>Hecho con ❤️ para la comunidad de investigadores</i>
</p>
