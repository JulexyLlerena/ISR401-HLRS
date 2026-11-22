# Proyecto Fin de Curso (PFC) - Entrega 1: Ingeniería de Requerimientos (ISR-401)

**Institución:** Universidad Técnica Estatal de Quevedo (UTEQ)  
**Facultad:** Facultad de Ciencias de la Computación  
**Carrera:** Ingeniería de Software  
**Nivel:** Cuarto  
**Paralelo:** A  
**Docente:** Gleiston Cicerón Guerrero Ulloa, PhD  
**Grupo:** HLRS

### Integrantes

- Herrera Moran Gilmar Javier
- Llerena Abril Angelina Julexy
- Rivera Rodriguez Joseph Jeremy
- Saltos Tello Joseph Orlando

---

## 1. Descripción del repositorio

Este repositorio contiene los archivos correspondientes a la primera entrega (`TA-PFC-E1`) del Proyecto Fin de Curso de la asignatura Ingeniería de Requerimientos (ISR-401).

El proyecto consiste en el análisis y la planificación inicial de una propuesta de aplicación web para apoyar la gestión de **un local de manualidades**, un emprendimiento dedicado a la elaboración y comercialización de productos de manualidades, ubicado en Quevedo, Ecuador.

Esta primera entrega establece la visión y el alcance del sistema, la identificación de las partes interesadas, el contexto de la solución y el plan de elicitación. Su documentación toma como referencia la norma **ISO/IEC/IEEE 29148:2018**, junto con los lineamientos académicos de la asignatura.

El documento principal se encuentra desarrollado en LaTeX y permite generar una versión PDF mediante los compiladores correspondientes.

## 2. Estructura del proyecto

La organización de los archivos es la siguiente:

```text
PFC/
└── E1/
    ├── etica/
    │   ├── cnInformado_cliente.pdf
    │   ├── cnInformado_cliente.tex
    │   ├── cnInformado_propietario.pdf
    │   └── cnInformado_propietario.tex
    │
    ├── evidencias/
    │   ├── Carta_Aceptación_Anonimizad...
    │   ├── ChatGPT_02_Propuesta_Estruct...
    │   ├── ChatGPT_03_Correccion_Redac...
    │   ├── ChatGPT_04_Resultado_Correccion_PFC...
    │   ├── Consentimiento_Informado_A...
    │   ├── IA_01_Generacion_Estructura_I...
    │   ├── MANIFIESTO.md
    │   └── Registro_Primer_Contacto.pdf
    │
    ├── figuras/
    │   ├── diagrama_contexto.png
    │   └── matriz_poder_interes.png
    │
    ├── instrumentos/
    │   ├── Cuestionario.pdf
    │   ├── Guia_observacion.pdf
    │   └── Guion_Entrevista.pdf
    │
    ├── modelos/
    │   ├── diagrama-contexto.drawio
    │   └── matriz_poder_interes.drawio
    │
    ├── main.pdf
    ├── main.tex
    ├── referencias.bib
    └── README.md
```

**Descripción de los archivos y directorios:**

| Archivo o directorio | Descripción |
|---|---|
| `main.tex` | Archivo principal que contiene la estructura y el contenido del documento. |
| `main.pdf` | Documento generado mediante la compilación del archivo LaTeX. |
| `referencias.bib` | Base de datos bibliográfica utilizada para las citas y referencias en formato IEEE. |
| `etica/` | Contiene los modelos de consentimiento informado para clientes y propietario, tanto en formato PDF como en LaTeX. |
| `evidencias/` | Almacena los documentos y registros que respaldan el desarrollo del proyecto, incluyendo cartas, registros de contacto y evidencias del uso de herramientas de inteligencia artificial. También contiene el manifiesto de evidencias. |
| `figuras/` | Contiene los recursos gráficos utilizados en el documento, como la matriz poder-interés y el diagrama de contexto en formato PNG. |
| `instrumentos/` | Contiene los instrumentos preparados para las actividades de elicitación: cuestionario, guía de observación y guion de entrevista. |
| `modelos/` | Contiene los archivos editables de los diagramas elaborados en Draw.io. |

## 3. Requisitos y dependencias

Para generar el documento PDF a partir del código fuente es necesario disponer de una distribución LaTeX y de los compiladores correspondientes.

### 3.1. Compiladores requeridos

- **pdfLaTeX (`pdflatex`):** motor utilizado para compilar el documento.
- **BibTeX (`bibtex`):** herramienta encargada de procesar las referencias bibliográficas.

### 3.2. Distribuciones LaTeX

Se puede utilizar cualquiera de las siguientes distribuciones:

- **MiKTeX:** https://miktex.org/download
- **TeX Live:** https://www.tug.org/texlive/
- **MacTeX:** https://www.tug.org/mactex/

### 3.3. Paquetes LaTeX utilizados

El archivo `main.tex` utiliza los siguientes paquetes:

| Categoría | Paquetes |
|---|---|
| Idioma y codificación | `inputenc`, `fontenc`, `babel` |
| Tipografía y formato | `helvet`, `geometry`, `setspace`, `fancyhdr` |
| Tablas | `booktabs`, `tabularx`, `xltabular`, `makecell` |
| Listas | `enumitem` |
| Gráficos y colores | `graphicx`, `xcolor`, `float` |
| Utilidades | `url`, `amssymb`, `seqsplit` |
| Hipervínculos | `hyperref` |

También se requiere el estilo bibliográfico `IEEEtran.bst` para procesar las referencias mediante BibTeX.

**Dependencias adicionales:**

- **Git:** para clonar el repositorio y administrar el control de versiones.
- **TeXstudio (opcional):** editor para trabajar con archivos LaTeX.
- **Draw.io / diagrams.net:** herramienta para visualizar y editar los modelos de diagramas almacenados en `modelos/`.
- **Overleaf (opcional):** plataforma en línea para editar y compilar documentos LaTeX.

## 4. Instalación y compilación por entorno

### 4.1. GNU/Linux (Ubuntu, Linux Mint y Debian)

En distribuciones basadas en Debian se pueden instalar las dependencias mediante el administrador de paquetes `apt`.

**Instalación de LaTeX y BibTeX:**

```bash
sudo apt update

sudo apt install -y \
texlive-latex-base \
texlive-latex-recommended \
texlive-latex-extra \
texlive-lang-spanish \
texlive-fonts-recommended \
texlive-bibtex-extra
```

Opcionalmente, se puede instalar un editor LaTeX:

```bash
sudo apt install -y texstudio
```

**Clonar el repositorio y acceder al proyecto:**

```bash
git clone <URL-DEL-REPOSITORIO>

cd <NOMBRE-DEL-REPOSITORIO>/PFC/E1
```

**Compilar el documento:**

```bash
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

### 4.2. Windows

Para Windows se recomienda instalar alguna de las siguientes distribuciones:

- **MiKTeX:** https://miktex.org/download
- **TeX Live:** https://www.tug.org/texlive/

En caso de utilizar MiKTeX, se recomienda habilitar la instalación automática de paquetes faltantes (*Install missing packages on-the-fly*).

También se puede utilizar TeXstudio como entorno de edición:

https://www.texstudio.org/

**Clonar el repositorio desde PowerShell:**

```powershell
git clone <URL-DEL-REPOSITORIO>

cd <NOMBRE-DEL-REPOSITORIO>\PFC\E1
```

**Compilar el documento:**

```powershell
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

### 4.3. macOS

Para macOS se puede instalar MacTeX desde su página oficial:

https://www.tug.org/mactex/

También es posible utilizar Homebrew:

```bash
brew install --cask mactex
```

Una vez instalada la distribución, se debe clonar el repositorio y acceder al directorio del proyecto:

```bash
git clone <URL-DEL-REPOSITORIO>

cd <NOMBRE-DEL-REPOSITORIO>/PFC/E1
```

**Compilar el documento:**

```bash
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

### 4.4. Entorno en la nube (Overleaf)

El proyecto también puede compilarse mediante Overleaf, sin necesidad de instalar una distribución LaTeX local.

**Pasos:**

1. Acceder a https://www.overleaf.com/.
2. Crear un proyecto nuevo o importar los archivos mediante un archivo ZIP.
3. Incorporar el contenido de `PFC/E1/`, incluyendo `main.tex`, `referencias.bib` y el directorio `figuras/`.
4. Abrir el menú de configuración del proyecto.
5. Seleccionar `pdfLaTeX` como compilador.
6. Establecer `main.tex` como documento principal.
7. Presionar **Recompilar** para generar el documento PDF.

## 5. Procedimiento de compilación

La secuencia de compilación recomendada es:

```text
pdflatex main.tex
       |
       v
bibtex main
       |
       v
pdflatex main.tex
       |
       v
pdflatex main.tex
       |
       v
main.pdf
```

Cada herramienta cumple una función específica:

- La primera ejecución de `pdflatex` genera los archivos auxiliares y recopila las referencias utilizadas.
- `bibtex` procesa la bibliografía definida en `referencias.bib`.
- La segunda ejecución de `pdflatex` incorpora las referencias bibliográficas.
- La tercera ejecución actualiza los índices, las referencias cruzadas, la numeración y los enlaces internos.

Por este motivo, se recomienda ejecutar la secuencia completa cuando se realicen modificaciones en el documento o en las referencias bibliográficas.

## 6. Recursos gráficos y modelos editables

El documento utiliza dos recursos gráficos principales, almacenados en el directorio `figuras/`:

- `matriz_poder_interes.png`: representación de las partes interesadas según su nivel de poder e interés.
- `diagrama_contexto.png`: representación del sistema, sus límites, los actores externos y los flujos de información.

Los archivos originales editables de estos diagramas se encuentran en el directorio `modelos/`:

- `matriz_poder_interes.drawio`
- `diagrama-contexto.drawio`

Estos archivos pueden abrirse y modificarse mediante Draw.io o diagrams.net.

El documento utiliza una macro personalizada denominada `\figuraopcional`, definida en `main.tex`, para incorporar las figuras del proyecto.

La macro verifica si cada archivo existe en el directorio `figuras/`. Si la imagen está disponible, se incorpora automáticamente al documento. Si no existe, se muestra un recuadro indicando que la figura está pendiente de incorporación.

Esto permite compilar el documento incluso cuando todavía no se han incorporado todos los recursos gráficos, sin provocar errores por archivos de imagen faltantes.

**Importante:** los nombres y las extensiones de las imágenes deben coincidir con los definidos en las llamadas a `\figuraopcional` del archivo `main.tex`.

## 7. Bibliografía y citación

Las referencias bibliográficas se encuentran centralizadas en el archivo `referencias.bib`.

El documento utiliza el estilo bibliográfico `IEEEtran`, mediante las siguientes instrucciones:

```latex
\bibliographystyle{IEEEtran}
\bibliography{referencias}
```

Para incorporar una nueva referencia se debe agregar su registro bibliográfico al archivo `referencias.bib` y utilizar su clave correspondiente mediante `\cite{clave}` dentro del documento.

## 8. Consideraciones sobre privacidad y evidencias

El proyecto contempla actividades de elicitación con participantes vinculados a la organización seleccionada. Por ello, se establecen medidas para proteger la información recopilada.

Se consideran las siguientes disposiciones:

- Los documentos públicos no deben contener información personal o confidencial de los participantes.
- Las cartas firmadas, grabaciones y demás evidencias identificables deben conservarse en un espacio privado y con acceso restringido.
- El archivo `MANIFIESTO.md` permite registrar las evidencias mediante su descripción, fecha de obtención y huella digital SHA-256.
- Los modelos de consentimiento informado se encuentran organizados en el directorio `etica/`.
- Los instrumentos de elicitación se encuentran en el directorio `instrumentos/`.
- El tratamiento de la información considera la Ley Orgánica de Protección de Datos Personales del Ecuador y su Reglamento General.

La documentación pública del repositorio debe limitarse a los archivos autorizados para su divulgación.

## 9. Control de versiones

El proyecto utiliza Git y GitHub para mantener el historial de cambios y facilitar el trabajo colaborativo.

Las modificaciones realizadas en los archivos fuente pueden registrarse mediante los siguientes comandos:

```bash
git add .
git commit -m "Actualización de la documentación PFC E1"
git push origin main
```

Para obtener los cambios más recientes del repositorio:

```bash
git pull origin main
```

Se recomienda mantener actualizados los archivos fuente, las referencias bibliográficas y los recursos gráficos para facilitar la reproducción del documento.

---

**Proyecto:** TA-PFC-E1  
**Asignatura:** Ingeniería de Requerimientos (ISR-401)  
**Grupo:** HLRS  
**Institución:** Universidad Técnica Estatal de Quevedo (UTEQ)  
**Año:** 2026
