# Mini-sistema de videojuegos (Flask)

[![CI](https://github.com/CharlieRod27/Hello-Git_Charlie/actions/workflows/ci.yml/badge.svg)](https://github.com/CharlieRod27/Hello-Git_Charlie/actions/workflows/ci.yml)
[![codecov](https://codecov.io/gh/CharlieRod27/Hello-Git_Charlie/branch/main/graph/badge.svg)](https://codecov.io/gh/CharlieRod27/Hello-Git_Charlie)

Aplicación web para administrar un catálogo de videojuegos. Incluye registro e inicio de sesión de usuarios, CRUD de juegos y una API REST en `/api/juegos`.

## Tecnologías

- Python 3.11
- Flask
- MySQL con PyMySQL
- pytest y pytest-cov
- GitHub Actions para integración continua

## Instalación

Clona el repositorio y entra a la carpeta del proyecto:

```bash
git clone https://github.com/CharlieRod27/Hello-Git_Charlie.git
cd Hello-Git_Charlie
```

Crea y activa un entorno virtual en Windows:

```bash
python -m venv venv
venv\Scripts\activate
```

Instala las dependencias:

```bash
pip install -r requirements.txt
```

Antes de ejecutar la aplicación, configura la conexión a MySQL según el archivo de configuración del proyecto.

## Ejecución

```bash
python app.py
```

## Pruebas y cobertura

Para correr las pruebas unitarias con reporte de cobertura:

```bash
python -m pytest --cov=. --cov-report=term-missing
```

## Integración continua

El workflow `.github/workflows/ci.yml` se ejecuta en cada `push` y `pull request` hacia `main` o `master`. Realiza los siguientes pasos:

1. Descarga el código del repositorio.
2. Instala Python y las dependencias del proyecto.
3. Ejecuta las pruebas con pytest y genera el reporte de cobertura.
4. Sube el reporte de cobertura a Codecov.

El estado de la última ejecución se puede consultar en la pestaña **Actions** del repositorio.