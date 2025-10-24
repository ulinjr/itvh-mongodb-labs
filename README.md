# Laboratorios MongoDB – ITVH (Jupyter Book)

Repositorio oficial de laboratorios de la asignatura **Nuevas Tecnologías de Acceso a Bases de Datos No Relacionales** (Instituto Tecnológico de Villahermosa).
Sitio público: `https://ulinjr.github.io/itvh-mongodb-labs/`

- Autor: José Juan Ulín (ITV)
- Repo: https://github.com/ulinjr/itvh-mongodb-labs

## Estructura
- `_config.yml`, `_toc.yml`: configuración de Jupyter Book.
- `labs/`: capítulos y ejercicios (Markdown MyST) con botón **Copiar**.
- `notebooks/`: notebooks `.ipynb` para ejecución (VS Code / Colab).
- `.github/workflows/deploy.yml`: CI para publicar en **GitHub Pages**.
- `requirements.txt`: dependencias mínimas.
- `LICENSE` (MIT para el código) y `LICENSE-CONTENT.md` (CC BY 4.0 para materiales).

## Uso local (WSL2 / conda)
```bash
conda activate py312
pip install -r requirements.txt
jupyter-book build .
explorer.exe `_build/html/index.html`
```

## Publicación en GitHub Pages
1. Crea el repo en GitHub: `ulinjr/itvh-mongodb-labs` y sube este contenido.
2. El workflow `deploy.yml` construye y publica el sitio en `gh-pages`.
3. En **Settings → Pages** selecciona Source: `Deploy from a branch`, Branch: `gh-pages`.
