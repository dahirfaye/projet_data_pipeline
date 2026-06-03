# Projet de pipeline de données météo

## description

Ce projet a pour objectif de créer unn pipeline de données permettant : 

- l'extraction de données météorologiques depuis une API
- la transformation des données JSON
- le stockage dans un DataFrame Pandas
- la sauvegarde dans un fichier CSV
- le stockage dans une base SQLite
- l'interrogation des données avec SQL

## Technologies utilisées

- Python
- Requests
- Pandas
- SQLite

## Architecture

```mermaid
flowchart TD
    A[open-API météo] --> B[Extraction Python]
    B --> C[Transformation]
    C --> D[DataFrame Pandas]
    D --> E[Fichier CSV]
    E --> F[Base SQLite]
    F --> G[Requêtes SQL]
```

## Auteur 

Cheikh Dahir FAYE

