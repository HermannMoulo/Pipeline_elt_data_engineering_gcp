# Pipeline ELT complet pour l'ingestion, la transformation et l'analyse des données des taxis verts de NYC, avec modélisation ML dans BigQuery.

Projet réalisé dans le cadre d'une formation sur Udemy Google Cloud Platform pour Data Engineers : Projet pratique
Les données utilisées sont des fichiers parquet de taxis jaunes de New York City à partir du site https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page. 

## 1. Architecture du Projet
```bash
nyc_yellow_taxis_tips/
├── 📂 data/                              
│   └── 📜 taxi_zone_lookup.csv           # Codification des zones/arrondissements
│
├── 📂 notebooks/                         
│   ├── 📜 Custom Model.ipynb             # Entraîne des modèles (RF, Boosted Tree)
│   ├── 📜 Report 2.ipynb                 # Split train/test/val + évaluation
│   └── 📜 Report Notebook.ipynb          # Analyses temporelles et saisonnières
│
├── 📂 queries/                           
│   ├── 📜 modeling_queries.sql           # Crée les modèles ML dans BigQuery
│   ├── 📜 MarketDemand_and_CustomerBehavior.sql  # Vues de demande client
│   ├── 📜 Financial_and_Pricing.sql      # Vues de coûts et tarification
│   └── 📜 CompetitiveInsights.sql       # Vues de volumes et fréquences
│
├── 📜 download_taxi_data.py              # Télécharge depuis NYC TLC
├── 📜 load_raw_trips_data.py             # Charge dans BigQuery
├── 📜 exploratory_data_analysis.py       # Analyse exploratoire
├── 📜 create_data_sets.py                # Datasets intermédiaires
├── 📜 transform_trips_data.py            # Nettoyage des données
├── 📜 create_ml_dataset_table.py         # Préparation pour ML
├── 📜 README.md                          # Documentation
└── 📜 requirements.txt                   # Dépendances Python

