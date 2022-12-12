# Manual de Políticas LACNIC

Hecho con MKDocs, demuestra cómo se podría mantener el manual de políticas en un repositorio Git.

## ¿Cómo se usa?

```bash
git clone https://github.com/aweher/manual-lacnic.git
cd manual-lacnic
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
mkdocs serve # Para previsualizar localmente en http://localhost:8000
```

Al hacer commit al branch `master` o `main` el sitio se despliega automáticamente haciua `GitHub Pages`.

## Versión Online

[Aquí](https://aweher.github.io/manual-lacnic/)
