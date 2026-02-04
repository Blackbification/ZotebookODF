# Post de LinkedIn - ZotebookODF

---

## VERSIÓN PARA PUBLICAR

---

🚀 **Acabo de publicar ZotebookODF. Gratis. Open source.**

Y no, no sé programar.

La hice con Claude en una tarde (bueno, varias tardes de debugging intenso).

---

**El problema:**

NotebookLM de Google es BRUTAL para analizar papers científicos. Le subes 10 PDFs y te hace síntesis, comparaciones, encuentra conexiones...

Pero tiene un problema gordo: las citas son números genéricos.

"El ejercicio mejora la AR 1, 2, 3..."

¿1, 2, 3 de qué? No sirve para un documento académico.

---

**La solución: ZotebookODF**

Una extensión de Chrome que:

→ Captura qué paper es cada número  
→ Cruza con tu biblioteca de Zotero  
→ Genera bibliografía automática (Vancouver, APA, Harvard)  
→ Exporta listo para pegar  

---

**De esto:**

"El ejercicio mejora la salud 1, 2, confirmando que es seguro 3, 4, 5."

**A esto:**

"El ejercicio mejora la salud [1], [2], confirmando que es seguro [3].

Referencias  
[1] Jahanbin et al. The Effect of Conditioning Exercise... 2014.  
[2] Lange et al. Effects of Aerobic and Resistance Exercise... 2019.  
[3] Li & Wang. Clinical effect and biological mechanism... 2023."

---

**¿Lo mejor?**

También exporta con marcadores para Zotero ODF Scan.

Resultado: citas ACTIVAS en Word que puedes gestionar desde Zotero.

---

**El proceso fue una locura.**

9 versiones.  
Más de 50 iteraciones.  
Debugging de regex, formatos de archivo, APIs de Chrome...  

Algunos problemas que tuvimos que resolver:

❌ Los números de NotebookLM no corresponden a nada fijo  
❌ El mismo paper puede tener 3 números diferentes  
❌ Las citas aparecían repetidas: [2], [2], [2]  
❌ Los formatos de exportación no funcionaban  

Todo resuelto. Todo documentado en el repo.

---

**5 cosas que aprendí:**

1. **El prototipo es fácil. Los edge cases son el 80% del trabajo.**

2. **La IA no reemplaza el pensamiento.** Claude escribió el código, pero yo tuve que definir el problema, testear, y decidir qué priorizar.

3. **El debugging es un diálogo.** Le describía el síntoma, él proponía hipótesis, yo testeaba. Así hasta encontrar la causa.

4. **Simplificar es más difícil que complicar.** Las primeras versiones tenían 6 botones. La final tiene 2.

5. **Publicar algo útil es más satisfactorio que publicar algo perfecto.**

---

🔗 **GitHub:** [enlace en comentarios]

Licencia AGPL-3.0 (la misma que Zotero).  
Gratis. Open source. Para siempre.

Si te dedicas a investigación y usas NotebookLM + Zotero, esto te va a ahorrar HORAS.

---

¿Preguntas? Dispara en comentarios 👇

¿Ideas para mejorarlo? Abre un issue en GitHub.

¿Quieres contribuir? Los PRs son bienvenidos.

---

#IA #Investigación #NotebookLM #Zotero #OpenSource #Chrome #Medicina #Academia

---

## VERSIÓN EXTENDIDA (para artículo o newsletter)

---

# Cómo construí ZotebookODF sin saber programar

## El problema que me volvía loco

Si usas NotebookLM para investigación, sabes lo potente que es. Subes papers, haces preguntas, y te genera síntesis brillantes con citas a las fuentes.

Pero hay un problema: las citas son números genéricos.

"El ejercicio físico mejora la funcionalidad en pacientes con artritis reumatoide 1, 2, confirmando que la intensidad moderada es segura 3, 4, 5."

¿Qué es 1? ¿Qué es 2? No hay forma de saberlo sin hacer clic en cada número.

Y lo peor: si quieres usar ese texto en un documento académico, tienes que:

1. Identificar manualmente cada cita
2. Buscar la referencia completa
3. Formatear la bibliografía
4. Rezar para no equivocarte

Horas de trabajo tedioso.

## La solución: ZotebookODF

Decidí crear una herramienta que automatizara todo el proceso:

1. **Captura las citas** → Haces clic en cada número y la extensión registra qué paper es
2. **Cruza con Zotero** → Cargas tu biblioteca en CSL JSON y obtiene metadatos completos
3. **Genera bibliografía** → Automáticamente, en Vancouver, APA o Harvard
4. **Exporta listo** → Copias y pegas, o descargas para Zotero ODF Scan

## El proceso de desarrollo

No soy programador. Soy médico. Mi código más complejo hasta ahora era un Excel con macros.

Pero tenía a Claude.

### Versión 1.0 - El prototipo

Le expliqué el problema y en 30 minutos tenía algo funcionando:
- Detectaba los números de cita
- Los reemplazaba por formato [1], [2]
- Generaba una bibliografía básica

**Problema:** Los números de NotebookLM no corresponden a nada fijo. El "1" de una respuesta puede ser diferente al "1" de otra.

### Versiones 2.0-5.0 - Captura y matching

Añadimos captura de títulos al hacer clic, y matching con la biblioteca de Zotero.

**Problemas:** El popup tardaba, los títulos a veces estaban truncados, el matching fallaba con diferencias menores.

### Versión 6.0 - Matching fuzzy

Algoritmo más inteligente que tolera diferencias menores en los títulos.

**Nuevo problema:** El mismo paper podía tener múltiples números diferentes.

### Versión 7.0 - Mapeo múltiple y ODF Scan

La extensión entiende que los números 3, 7 y 12 pueden ser el mismo paper. También añadimos exportación con marcadores [@citekey] para ODF Scan.

**Nuevo problema:** Aparecía [2], [2], [2] cuando NotebookLM citaba el mismo paper varias veces seguidas.

### Versión 8.0 - Colapso de duplicados

[2], [2], [2] → [2]

**Nuevo problema:** Demasiados botones y opciones confusas.

### Versión 9.0 - Simplificación radical

Dos botones:
- "📋 Copiar todo"
- "📥 TXT para Zotero ODF Scan"

Simple. Efectivo. Funciona.

## Lo que aprendí

### 1. La iteración es clave
No intentes hacer todo perfecto a la primera.

### 2. Los edge cases son el 80% del trabajo
El prototipo tomó 30 minutos. Los casos especiales tomaron días.

### 3. La IA no reemplaza el pensamiento
Claude escribió el código. Yo definí el problema, identifiqué casos de uso, testeé exhaustivamente, y decidí qué priorizar.

### 4. El debugging es un diálogo
Síntoma → Hipótesis → Test → Repetir.

### 5. Simplificar es más difícil que complicar
Las primeras versiones tenían 6 botones. La final tiene 2.

## El resultado final

Una extensión que:

✅ Captura citas de NotebookLM  
✅ Mapea múltiples números al mismo paper  
✅ Genera bibliografía automática  
✅ Colapsa citas duplicadas  
✅ Exporta para Zotero ODF Scan  
✅ Soporta Vancouver, APA, Harvard  

**Gratis. Open source. AGPL-3.0 (igual que Zotero).**

---

**Link al repositorio:** GitHub [enlace]

Si te resulta útil, dale una ⭐ al repo.

---

## VERSIÓN THREAD (para X/Twitter)

---

🧵 Acabo de publicar ZotebookODF.

Una extensión de Chrome que soluciona un problema GORDO de NotebookLM.

Sin saber programar. Con Claude.

Hilo 👇

---

1/ NotebookLM es BRUTAL para analizar papers.

Pero las citas son números genéricos: 1, 2, 3...

No sirven para documentos académicos.

---

2/ ZotebookODF:
- Captura qué paper es cada número
- Cruza con tu Zotero
- Genera bibliografía automática
- Exporta listo para usar

---

3/ De esto:
"mejora la salud 1, 2, 3..."

A esto:
"mejora la salud [1], [2].

Referencias
[1] Lange et al. 2019.
[2] Jahanbin et al. 2014."

---

4/ El proceso:
- 9 versiones
- 50+ iteraciones
- Regex, APIs, formatos...

Todo con Claude.

---

5/ Lo más difícil:

❌ No fue escribir código
✅ Fue identificar los edge cases

Prototipo: 30 min
Edge cases: días

---

6/ Funcionalidades:

✅ Captura citas
✅ Mapea múltiples números al mismo paper
✅ Colapsa duplicados [2],[2],[2] → [2]
✅ Bibliografía automática
✅ Exporta para Zotero ODF Scan
✅ Vancouver, APA, Harvard

---

7/ 

🔗 GitHub: [link]

Gratis.
Open source.
AGPL-3.0 (como Zotero).

---

8/ Aprendizajes:

1. Itera rápido
2. Los edge cases son el 80%
3. La IA no reemplaza el pensamiento
4. Simplificar > Complicar

---

9/ Si te mola:
⭐ Estrella al repo
🔄 RT para investigadores
💬 Ideas en comentarios

---

/fin

#IA #Investigación #OpenSource
