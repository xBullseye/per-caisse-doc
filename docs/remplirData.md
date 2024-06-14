# Remplir la base de données
L'application utilise Flask pour gérer les routes qui permettent de remplir la base de données avec des données. Les scripts pour ces routes sont organisés dans des fichiers séparés selon leur fonctionnalité dans le dossier `backend > Base > api`.

## Processus Automatique de Remplissage
L'application a été conçue pour simplifier le processus de remplissage des données. Par exemple, en utilisant la route `products/real_data`, les tables des produits et des catégories sont remplies dans l'ordre correct, assurant l'intégrité des données.

!!! tip "Bon à savoir"
    Assurez-vous que le serveur Flask est en cours d'exécution avant d'accéder aux routes de remplissage des données. Cela garantit que les requêtes sont correctement traitées et que les données sont ajoutées à la base de données sans erreur.

## Utilisation des Routes pour le Remplissage des Données

### Données "Dummy"
Pour remplir les tables avec des données fictives (dummy), utilisez les routes suivantes :

- **Produits:** Accédez à `http://127.0.0.1:8000/products/dummy` pour remplir la table des produits avec des données dummy.
- **Catégories, Clients, etc.:** Similairement, remplacez `products` par la table correspondante dans l'URL pour les autres données dummy.

### Données Réelles
Pour remplir les tables avec des données réelles du client, suivez ces étapes :

- **Produits et Catégories:** En accédant à `http://127.0.0.1:8000/products/real_data`, la table des produits et des catégories sera automatiquement remplie avec des données réelles.
- **Clients:** Pour remplir la liste des clients, accédez à `http://127.0.0.1:8000/clients/real_data`.

### Initialisation Complète de la Base de Données
Pour initialiser complètement la base de données avec les données de clients, produits, catégories, tarifs et paiements, utilisez la route `http://127.0.0.1:8000/init-db`. Cette route permet de remplir toutes les tables nécessaires en une seule fois. Cette opération peut être effectuée via un client HTTP comme Postman ou en utilisant `curl` en ligne de commande.

**Exemple avec Postman :**
1. Ouvrez Postman.
2. Créez une nouvelle requête POST.
3. Entrez l'URL `http://127.0.0.1:8000/init-db`.
4. Assurez-vous que la méthode est définie sur POST.
5. Cliquez sur "Send" pour exécuter la requête.

**Exemple avec `curl` :**
```sh
curl -X POST http://127.0.0.1:8000/init-db
