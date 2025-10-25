---
title: Lab01 — Primeros pasos con MongoDB
---

# Lab01 — Primeros pasos con MongoDB

## Objetivos
- Configurar el ambiente de desarrollo (VS Code + Python + Notebooks).
- Verificar conectividad con MongoDB y recorrer documentos de una colección.

## Requisitos
- Python 3.12, VS Code, extensiones **Python** y **Jupyter**.
- Servidor MongoDB activo (local, WSL2, VM, Docker o Atlas).
- Kernel seleccionado: `Python 3.12`.

## Verificación rápida del servidor MongoDB
Crea una celda de código y ejecuta:

```python
from pymongo import MongoClient

# Conexión local por defecto: mongodb://localhost:27017
# Si usas Atlas, reemplaza por tu cadena de conexión.
client = MongoClient()

# Ping al servidor para validar conectividad
client.admin.command("ping")
print("✅ Conexión a MongoDB OK")

# Diagnóstico rápido
print("Bases de datos disponibles:", client.list_database_names())
```

> También puedes abrir el notebook: {doc}`../notebooks/lab01`
