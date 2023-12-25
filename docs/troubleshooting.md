# Troubleshooting

Cette section fournit des solutions aux problèmes courants pouvant survenir lors de la manipulation de la base de données.

## Problème avec la Base de Données

Si vous rencontrez des problèmes avec la base de données, suivez ces étapes pour réinitialiser et recréer la base:

!!! warning "Attention"
    La suppression de la base de données et du répertoire 'migrations' entraînera la perte de toutes les données actuelles. Assurez-vous d'avoir une sauvegarde ou de ne pas avoir besoin des données existantes avant de procéder.

### 1. **Suppression du Répertoire 'Migrations'**
Dans le répertoire `backend`, supprimez le dossier `migrations`. Ce dossier contient les fichiers de migration de la base de données.

```bash
cd backend
rm -rf migrations
```

### 2. Suppression de la Base de Données
Dans le répertoire `backend`, supprimez le dossier `migrations`. Ce dossier contient les fichiers de migration de la base de données.

```bash
cd backend/Base
rm pos.db
```

### 3. Recréation de la Base de Données
Après avoir supprimé les éléments nécessaires, recréez la base de données. Pour cela, veuillez vous référer à la section [Création de la base de données](https://jsaghbini.github.io/per-caisse-doc/installation/#creation-de-la-base-de-donnees) de la documentation.

### 4. Remplissage de la Base de Données
Une fois la base de données recréée, remplissez-la de nouveau avec les données nécessaires en suivant les instructions fournies dans la section [Remplir la base de données](https://jsaghbini.github.io/per-caisse-doc/remplirData/) de la documentation.