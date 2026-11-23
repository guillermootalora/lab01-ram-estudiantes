# Laboratorio 01 · Memoria RAM — Versión para el estudiante

Autor: Ing. Guillermo Otálora Luna · Digital Forensics (203028123) · UNAD

Esta versión del tutorial no trae las salidas de Volatility3 ni las respuestas. El estudiante ejecuta cada comando, interpreta su salida con las tablas y responde las preguntas guía en su informe. La versión completa (`sitio_publicable`) se comparte después de la entrega.

## Diferencias con la versión completa

| Se quitó | Se dejó o se cambió |
|---|---|
| Salidas reales de windows.info, pslist, cmdline, netscan, netstat y del resumen de URLs | Un recuadro naranja «✎ Su salida» en cada paso |
| Recuadros «Respuesta a la pregunta N» | Recuadros «Para su informe · pregunta N» con preguntas guía |
| Columna «Valor en esta imagen» y valores concretos (PID, horas, build, CPU) | Explicación de cada campo y tablas de referencia (builds de Windows, códigos de arquitectura, UTC−5) |
| Línea de tiempo con horas | Línea de tiempo con `hh:mm:ss` para completar |
| Gráfico de apariciones de URLs y `resultados-volatility-lab01.zip` | — |
| Filtros `findstr "msedge"` (delataban el navegador) | Filtros con varios navegadores y herramientas |
| Sección «Cómo reemplazar las imágenes» (es para el docente) | — |

Se conservaron las salidas de verificación de hash, de instalación y de la Parte 2 (adquisición), porque no responden las preguntas del caso.

Descargas: `Tutorial-Lab01-Estudiante.pdf` y `.docx`, la plantilla del informe, `buscar_urls.py`, los hashes y la cadena de custodia.

## Publicar en Google Sites

Google Sites no aloja archivos HTML propios: solo muestra páginas que ya estén publicadas en otro lugar. Por eso son dos pasos: publicar esta carpeta en GitHub Pages y luego insertarla en Google Sites.

### 1. Publicar esta carpeta en GitHub Pages (repositorio nuevo)

El tutorial descarga `buscar_urls.py` desde `https://guillermootalora.github.io/lab01-ram-estudiantes/`. Por eso el repositorio debe llamarse exactamente **lab01-ram-estudiantes**.

1. En GitHub, cree un repositorio público llamado `lab01-ram-estudiantes`, sin README.
2. En PowerShell, ejecute:

   ```powershell
   cd D:\com.gaol.unad\laboratorio_01\sitio_estudiantes
   git init -b main
   git add -A
   git commit -m "Lab01 versión estudiante"
   git remote add origin https://github.com/guillermootalora/lab01-ram-estudiantes.git
   git push -u origin main
   ```

3. En el repositorio, vaya a **Settings → Pages → Source: Deploy from a branch → main / (root) → Save**.
4. En uno o dos minutos la página queda en `https://guillermootalora.github.io/lab01-ram-estudiantes/`.

### 2. Insertarla en Google Sites

1. Entre a <https://sites.google.com> y cree un sitio con **+ En blanco**.
2. En el panel derecho, vaya a **Insertar → Insertar**, pestaña **Por URL**, y pegue `https://guillermootalora.github.io/lab01-ram-estudiantes/`.
3. Elija **Página completa** y haga clic en **Insertar**.
4. Estire el recuadro al ancho y alto de la página.
5. Opcional: agregue botones (**Insertar → Botón**) que lleven a la carpeta **Artefacto_RAW** de Drive y a la plantilla del informe.
6. Haga clic en **Publicar**. En **Quién puede ver mi sitio** puede limitarlo a usuarios de `@unad.edu.co`.

## Regenerar esta versión

Esta carpeta la genera `build_est.py` a partir del mismo contenido de la versión completa. Si se corrige el tutorial completo, hay que volver a generarla para que los cambios lleguen aquí.
