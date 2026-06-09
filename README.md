# Projet de pipeline de données météo

## description

Ce projet a pour objectif de créer un pipeline de données permettant : 

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
    A[Open-Meteo API] --> B[Extraction Python]
    B --> C[Transformation]
    C --> D[DataFrame Pandas]
    D --> E[Fichier CSV]
    D --> F[Base SQLite]
    F --> G[Requêtes SQL]
```

## SQL queries

### Hottest city
```sql
SELECT city, temperature 
FROM weather 
ORDER BY temperature DESC
LIMIT 1;
```
Résultat : 
```text
Marseille | 20.9°C
```


### Average temperature
```sql
SELECT AVG(temperature) AS average_temperature
FROM weather;
```
Résultat : 
```text
20.0°C
```

### Classement des villes par temperature
```sql
SELECT city, temperature
FROM weather
ORDER BY temperature DESC;
```
Résultat:
```text
Marseille | 20.9°C
Lyon      | 20.3°C
Toulouse  | 20.1°C
Paris     | 18.7°C
```

## Future improvements

- Historical weather data collection
- Automated daily data ingestion
- Docker containerization
- Apache Airflow orchestration
- Data visualization dashboard


## Auteur 

Cheikh Dahir FAYE

