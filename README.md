# P7-OC-DataScientist-FASTAPI

## Projet : Implémentez un modèle de scoring
C'est une partie du projet 7 de la formation OpenClassrooms du parcours data scientist

## Objectifs du projet

Une société financière, nommée "Prêt à dépenser", qui propose des crédits à la consommation pour des personnes ayant peu ou pas du tout d'historique de prêt souhaite mettre en œuvre un outil de “scoring crédit” pour calculer la probabilité qu’un client rembourse son crédit, puis classifie la demande en crédit accordé ou refusé.

Elle souhaite donc développer un algorithme de classification en s’appuyant sur des sources de données variées (données comportementales, données provenant d'autres institutions financières, etc.). De plus, les chargés de relation client ont fait remonter le fait que les clients sont de plus en plus demandeurs de transparence vis-à-vis des décisions d’octroi de crédit. Cette demande de transparence des clients va tout à fait dans le sens des valeurs que l’entreprise veut incarner.

Ce projet a donc pour but de déployer le modèle via une API (FAST API) dans le Web via Heroku en utilisant un dashboard interactif (Streamlit) pour présenter le travail de modélisation. Il comporte aussi un test unitaire à l'aide de Pytest. Le code source de l'API contient entre autres un calculateur de score pour une demande de crédit bancaire qui retourne au Dashboard la probabilité que le client puisse le rembourser, et qui indique donc si le crédit est accordé ou non.

Cette partie est l'API qui a été build and deploy on Heroku.


## Découpage des dossiers
- main.py : fichier python de l'API FAST API
- Procfile : Le Procfile contient le code qui donne les commandes pour indiquer quels fichiers doivent être exécutés par l’application lors de son ouverture. Ouvrez le fichier que vous avez créé et tapez cette ligne de code.
- requirements.txt : contient la liste des packages et des dépendances nécessaires à l’exécution de l’application Web. Vous trouverez ci-dessous un exemple de la façon dont vous devez remplir ce fichier.
- setup.sh : contient le script shell requis pour configurer l’environnement shell pour nos besoins.
- dossier .github : contient le fichier build-test-deploy.yml qui permet de mettre en production l'applicatio sur Heroku via les “actions” de Github
- test_app.py : fichier contenant les tests unitaires avec Pytest
- dossier data :
  - X_test_reduit.csv contient les données client de test scalées
  - X_test_reduit_unsc.csv contient les données client test réduit non scalés qui va servir a créer le fichier df_streamlit en rajoutant les informations de prediction
  - df_streamlit.csv contient les données client non scalées et la réponse de la banque
- model.pkl : contient le model de prédiction lightgbm choisi et entrainé sur les données d'entrainement test
- logo.png : logo de la société
- requirements.txt : stocke des informations sur toutes les bibliothèques, modules et packages utilisés lors du développement du projet


## Lien utiles
- URL github du code du dashboard Streamlit : https://github.com/juliesaubot/Saubot_Julie_streamlit_102023
- URL API déployé dans le Cloud : https://saubot-julie-fastapi-102023-5cca48d2a8d1.herokuapp.com/
- URL dashboard déployé dans le Cloud : https://saubot-julie-dashboard-102023-00ee4bc4d00a.herokuapp.com/ 

