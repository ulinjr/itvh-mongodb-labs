---
title: Lab01 — Ejercicio 1 (recorrer cursor y pretty print)
---

# Lab01 — Ejercicio 1 (recorrer cursor y pretty print)

**Descripción:** Realizar una consulta general a la colección `Libros` y mostrar cada documento de forma legible.

```python
from pprint import pprint
from pymongo import MongoClient

client = MongoClient()         # localhost:27017 por defecto
db = client["Biblioteca"]
col = db["Libros"]             # CUIDADO: nombres y mayúsculas

cursor = col.find({})          # puedes aplicar filtros aquí si lo deseas

print("Total documentos:", col.count_documents({}))
for doc in cursor:
    pprint(doc)
```

**Variantes (opcional):**

- Solo `titulo` y `precio`:
```python
for doc in col.find({}, {"_id": 0, "titulo": 1, "precio": 1}):
    pprint(doc)
```

- Ordenar por título ascendente:
```python
for doc in col.find({}).sort("titulo", 1):
    pprint(doc)
```
