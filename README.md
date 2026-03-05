# COSASVARIAS

mi-repositorio/
│
├── README.md
├── index.html
├── documento.tex
├── cv.tex
├── notebook.ipynb
└── metadatos.R
```

# ✅ EJERCICIO 1 — Crear, modificar y hacer el archivo README.md

### 📌 Archivo: `README.md`

```markdown
# Mi Proyecto de Práctica GitHub

Este repositorio contiene ejercicios prácticos de:

- Creación de README.md
- Archivo HTML manual
- Documento LaTeX
- Notebook Jupyter
- CV en LaTeX
- Archivo con metadatos en R

## Autor
Tu Nombre

## Fecha
2026

## Descripción
Repositorio creado para practicar estructuras básicas de proyectos académicos.
```

---

# ✅ EJERCICIO 2 — Creación de archivo HTML manual

### 📌 Archivo: `index.html`

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Mi Página HTML</title>
</head>
<body>

    <h1>Bienvenido a mi página</h1>
    <p>Este archivo fue creado manualmente.</p>

    <h2>Lista de tecnologías:</h2>
    <ul>
        <li>HTML</li>
        <li>LaTeX</li>
        <li>Python</li>
        <li>R</li>
    </ul>

</body>
</html>
```

---

# ✅ EJERCICIO 3 — Crear archivo LaTeX (para usar en Overleaf)

📌 Plataforma: [https://overleaf.com](https://overleaf.com)

### 📌 Archivo: `documento.tex`

```latex
\documentclass{article}
\usepackage[spanish]{babel}
\usepackage{amsmath}

\title{Documento de Práctica}
\author{Tu Nombre}
\date{\today}

\begin{document}

\maketitle

\section{Introducción}

Este es un documento creado en LaTeX usando Overleaf.

\section{Ejemplo de ecuación}

\[
E = mc^2
\]

\section{Conclusión}

LaTeX permite crear documentos científicos con excelente formato.

\end{document}
```

---

# ✅ EJERCICIO 4 — Creación de Notebook (Jupyter)

### 📌 Archivo: `notebook.ipynb`

Podés crear el notebook en Jupyter y pegar este contenido en una celda:

```python
# Notebook de práctica

import numpy as np
import matplotlib.pyplot as plt

# Generar datos
x = np.linspace(0, 10, 100)
y = np.sin(x)

# Graficar
plt.plot(x, y)
plt.title("Gráfico de seno")
plt.xlabel("x")
plt.ylabel("sin(x)")
plt.show()
```

Si querés generarlo desde terminal:

```bash
jupyter notebook
```

---

# ✅ EJERCICIO 5 — CV en LaTeX

### 📌 Archivo: `cv.tex`

```latex
\documentclass[12pt]{article}
\usepackage[margin=1in]{geometry}

\begin{document}

\begin{center}
    {\LARGE \textbf{Tu Nombre}} \\
    Email: tunombre@email.com \\
    Teléfono: 123456789
\end{center}

\section*{Perfil}
Estudiante de Ingeniería con interés en programación y ciencia de datos.

\section*{Educación}
\textbf{Ingeniería} \\
Universidad X \\
2020 - Presente

\section*{Habilidades}
\begin{itemize}
    \item Python
    \item R
    \item LaTeX
    \item GitHub
\end{itemize}

\end{document}
```

---

# ✅ EJERCICIO 6 — Archivo con metadatos en R

### 📌 Archivo: `metadatos.R`

```r
# Crear lista de metadatos

metadatos <- list(
  titulo = "Análisis de Datos",
  autor = "Tu Nombre",
  fecha = Sys.Date(),
  version = "1.0",
  descripcion = "Archivo de ejemplo con metadatos en R"
)

# Mostrar metadatos
print(metadatos)

# Guardar metadatos en archivo
saveRDS(metadatos, file = "metadatos.rds")
```

---

# 🚀 Cómo subir todo a GitHub

En la terminal:

```bash
git init
git add .
git commit -m "Subida ejercicios prácticos"
git branch -M main
git remote add origin https://github.com/tuusuario/turepositorio.git
git push -u origin main
```
