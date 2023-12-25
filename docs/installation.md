# Etapes d'installation

* `Cloner le projet.`
* `Installation de npm.`
* `Installation de Python.`
* `Creation de la base de données.`
* `Lancer le projet mode developement.`

## Cloner le projet
```bash
git clone https://git.enib.fr/h1serhan/logiciel-caisse.git
```

## Installation de npm
```bash
npm install
```

## Installation de Python et de Flask

Cette section guide à travers les étapes d'installation de Python et de Flask, nécessaires pour exécuter le backend de l'application.

### 1. Installation de Python
Téléchargez et installez la dernière version de Python depuis le [site officiel de Python](https://www.python.org/downloads/). Python est essentiel pour exécuter le serveur Flask et gérer les dépendances de l'application.

### 2. Création et Activation d'un Environnement Virtuel
Un environnement virtuel (`venv`) isole les dépendances du projet pour éviter tout conflit avec d'autres projets ou avec le système global.

- **Pour Windows :**
```bash
# Creation d'un environnement virtuel nommé "venv"
python -m venv venv

# Activation de "venv"
venv/scripts/activate
```

- **Pour Linux :**
```bash
# Creation d'un environnement virtuel nommé "venv"
python3 -m venv venv

# Activation de "venv"
source venv/bin/activate
```

### 3. Installation des Dépendances avec Pip
Après avoir activé l'environnement virtuel, installez Flask et les autres dépendances requises en utilisant `pip`. Ces dépendances sont définies dans le fichier `requirements.txt`.
```bash
# Naviguer dans le Répertoire du Backend
cd backend

# Installation des dépandances
pip install -r requirements.txt
```

## Création de la base de données
Pour initialiser et configurer la base de données de l'application, suivez les étapes suivantes :

```bash
# Naviguer dans le Répertoire du Backend
cd backend

# Initialisation de la Base de Données avec Flask
flask db init

# Migration de la Base de Données
flask db migrate

# Mise à jour de la Base de Données
flask db upgrade
```
Ces commandes prépareront la base de données pour le bon fonctionnement de l'application. Assurez-vous d'exécuter ces commandes dans le répertoire du backend où se trouve le serveur Flask.

## Lancer le projet en mode developement
En suivant ces étapes, vous serez prêt à lancer et à utiliser le serveur Flask avec votre application ReactJS.
```bash
# Lancer le serveur Flask avec l'application ReactJS
npm run app
```