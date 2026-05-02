# WebParcial

Aplicación web con **Python (Flask)**: mensaje **Bienvenido** y **Nombre: xxx** (personalizable con `?nombre=TuNombre` en la URL). El nombre se renderiza en el servidor con Jinja2 (escapado automático).

## Probar en local

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
python app.py
```

Abre en el navegador: `http://127.0.0.1:5000` (o `http://127.0.0.1:5000/?nombre=Ana`).

## Subir a GitHub

1. Crea un repositorio vacío en GitHub (sin README si ya tienes uno aquí).
2. En esta carpeta:

```bash
git init
git add .
git commit -m "Initial commit: página de bienvenida"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/TU_REPO.git
git push -u origin main
```

## Subir a Azure DevOps

1. En Azure DevOps: **Repos** → **New repository** → copia la URL HTTPS o SSH.
2. Mismos comandos que arriba, cambiando `origin` por la URL de Azure DevOps:

```bash
git remote add origin https://dev.azure.com/TU_ORG/TU_PROYECTO/_git/TU_REPO
git push -u origin main
```

Para publicarla en Azure puedes usar **Azure App Service** (Python 3.x), configurando el comando de inicio como `gunicorn app:app` o el stack de Flask que indique el portal, y subiendo este repo.
