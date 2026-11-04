# Olist — analyse des ventes avec pandas

Projet d'analyse exploratoire du jeu de données public **Brazilian E-Commerce Public Dataset by Olist**. Le notebook étudie les commandes, les ventes, les catégories de produits, les régions de livraison et la satisfaction des clients à l'aide de Python, pandas et Matplotlib.

## Contenu du projet

- [`3_adapter_pandas_olist.ipynb`](3_adapter_pandas_olist.ipynb) : notebook principal, organisé en six missions.
- [`data_olist/`](data_olist/) : fichiers CSV sources du jeu de données Olist. Le notebook en charge six : commandes, articles, clients, produits, avis et traduction des catégories.
- [`ventes_olist.csv`](ventes_olist.csv) et [`ventes_olist.parquet`](ventes_olist.parquet) : exports de la table d'analyse construite dans le notebook.
- [`consigne_olist.md`](consigne_olist.md) : consignes détaillées du travail.
- [`Schema_Relationnel_Olist.pdf`](Schema_Relationnel_Olist.pdf), [`Schema_Relationnel_Olist.png`](Schema_Relationnel_Olist.png) et [`Schema_Relationnel_Olist_Nom_dans_Pandas.jpg`](Schema_Relationnel_Olist_Nom_dans_Pandas.jpg) : schémas des tables et de leurs relations.
- [`venv.bat`](venv.bat) : script Windows de création d'environnement et d'installation des bibliothèques.

## Missions du notebook

1. Auditer les tables, leurs types, leurs valeurs manquantes et leurs clés.
2. Joindre les données et créer la table `ventes`.
3. Analyser l'évolution mensuelle des ventes.
4. Comparer les catégories de produits et les régions.
5. Étudier les délais de livraison et leur lien avec les avis clients.
6. Exporter les résultats et rédiger une synthèse.

## Installation et lancement

Depuis le dossier du projet, créez un environnement virtuel et installez les dépendances :

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install pandas matplotlib pyarrow jupyterlab
```

Lancez JupyterLab :

```powershell
jupyter lab
```

Ouvrez `3_adapter_pandas_olist.ipynb` et exécutez les cellules dans l'ordre. Le dossier `data_olist` doit rester à côté du notebook pour que le chargement des données fonctionne. L'export CSV est produit par le notebook ; l'export Parquet nécessite `pyarrow`.

## Données

Les données proviennent du jeu public [Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce). Les fichiers locaux permettent de reproduire l'analyse. Le fichier `data_olist/olist_geolocation_dataset.csv` est volumineux ; GitHub peut afficher un avertissement de taille à son sujet.
