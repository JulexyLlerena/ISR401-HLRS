# Proyecto Fin de Curso (PFC) - Entrega 1: Ingeniería de Requerimientos (ISR-401)

**Institución:** Universidad Técnica Estatal de Quevedo (UTEQ)  
**Facultad:** Facultad de Ciencias de la Computación  
**Carrera:** Ingeniería de Software (4.º Nivel, Paralelo A)  
**Docente:** Gleiston Cicerón Guerrero Ulloa, PhD  
**Grupo:** HLRS  
- Herrera Moran Gilmar Javier
- Llerena Abril Angelina Julexy
- Rivera Rodriguez Joseph Jeremy
- Saltos Tello Joseph Orlando

---

## Descripción del Repositorio

Este repositorio contiene el código fuente en LaTeX, los recursos gráficos, los instrumentos de elicitación y el manifiesto de evidencias correspondientes a la primera entrega (`TA-PFC-E1`) del Proyecto Fin de Curso. El documento establece la visión, el alcance, la identificación de partes interesadas, el contexto del sistema y el plan de elicitación bajo los lineamientos de la norma **ISO/IEC/IEEE 29148:2018**.

---

## Estructura del Proyecto

```text
PFC/E1/
├── main.tex                  # Archivo principal del documento LaTeX
├── referencias.bib           # Archivo de referencias bibliográficas (formato IEEEtran)
├── README.md                 # Documentación de compilación, dependencias y entornos
├── figuras/                  # Recursos gráficos del documento
│   ├── matriz_poder_interes.pdf
│   └── diagrama_contexto.pdf
├── instrumentos/             # Instrumentos de elicitación (entrevista, cuestionario, observación)
└── evidencias/               # Registro público de integridad de evidencias privadas
    └── MANIFIESTO.md
```

---

## Requisitos y Dependencias

Para garantizar la compilación reproducible del documento PDF (`main.pdf`) a partir del código fuente, el entorno debe contar con una distribución TeX completa o los paquetes individuales detallados a continuación.

### Compiladores requeridos
* **`pdflatex`**: Motor de compilación principal (configurado para codificación UTF-8).
* **`bibtex`**: Procesador de citas y referencias bibliográficas (`IEEEtran`).

### Dependencias de paquetes LaTeX
El archivo `main.tex` requiere los siguientes paquetes instalados en la distribución TeX:
* **Idioma y codificación:** `inputenc` (`utf8`), `fontenc` (`T1`), `babel` (`spanish`, `es-tabla`).
* **Tipografía y diseño:** `helvet`, `geometry`, `setspace`, `fancyhdr`.
* **Tablas y listas:** `enumitem`, `booktabs`, `tabularx`, `float`.
* **Gráficos, color y cajas:** `graphicx`, `xcolor` (`table`), `tcolorbox` (`most`), `amssymb`.
* **Enlaces y bibliografía:** `url`, `hyperref` (`hidelinks`), `IEEEtran`.

---

## Instalación de Dependencias y Compilación por Entorno

### 1. Entornos GNU/Linux (Ubuntu MATE, Linux Mint MATE, Debian)
En distribuciones basadas en Debian/Ubuntu que utilizan el entorno de escritorio **MATE**, las dependencias y el editor ligero recomendado se instalan mediante `apt`:

```bash
# 1. Actualizar repositorios e instalar TeX Live (paquetes base, español y extras)
sudo apt update
sudo apt install -y texlive-latex-base texlive-latex-recommended texlive-latex-extra texlive-lang-spanish texlive-fonts-recommended texlive-bibtex-extra

# (Opcional) Instalar editor ligero compatible con MATE
sudo apt install -y texmaker
```

**Compilación desde la terminal de MATE (`mate-terminal`):**
```bash
git clone <URL-DEL-REPOSITORIO>
cd <NOMBRE-DEL-REPOSITORIO>/PFC/E1

pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

---

### 2. Entornos Windows
1. Descargar e instalar **MiKTeX** (`https://miktex.org/download`) o **TeX Live** para Windows.
2. Durante la instalación de MiKTeX, habilitar la opción *"Install missing packages on-the-fly: Yes"* para que descargue automáticamente paquetes como `tcolorbox`, `tabularx` o `babel-spanish`.
3. Abrir **PowerShell**, **CMD** o el editor de su preferencia (TeXstudio / VS Code con *LaTeX Workshop*) en la carpeta `PFC/E1/` y ejecutar:

```powershell
git clone <URL-DEL-REPOSITORIO>
cd <NOMBRE-DEL-REPOSITORIO>\PFC\E1

pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

---

### 3. Entornos macOS
1. Instalar **MacTeX** mediante Homebrew (`brew install --cask mactex`) o descargando el instalador oficial (`https://www.tug.org/mactex/`).
2. Abrir la Terminal, navegar al directorio del proyecto y ejecutar la secuencia de compilación:

```bash
git clone <URL-DEL-REPOSITORIO>
cd <NOMBRE-DEL-REPOSITORIO>/PFC/E1

pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

---

### 4. Entorno en la Nube (Overleaf)
1. Comprimir el contenido de la carpeta `PFC/E1/` en un archivo `.zip` (o vincular directamente mediante GitHub).
2. Crear un nuevo proyecto en **Overleaf** subiendo los archivos.
3. Verificar en **Menú > Compilador** que esté seleccionado **`pdfLaTeX`** y como **Documento principal** esté definido **`main.tex`**.
4. Hacer clic en **Recompilar**.

---

## Notas sobre la Reproducibilidad
* El orden de ejecución (`pdflatex` $\rightarrow$ `bibtex` $\rightarrow$ `pdflatex` $\rightarrow$ `pdflatex`) es obligatorio para resolver correctamente los índices (`\tableofcontents`, `\listoffigures`, `\listoftables`), las referencias cruzadas de tablas y la bibliografía IEEE.
* El documento incluye la macro `\figuraopcional`, por lo que si los diagramas en `figuras/` aún no existen en formato `.pdf`, el archivo compilará sin errores mostrando un recuadro marcador de posición.