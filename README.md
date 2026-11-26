# AutoLux – Gestion de véhicules premium

Application web de **gestion de voitures** (vente et location) réalisée en HTML, CSS et JavaScript, sans framework ni serveur : il suffit d'ouvrir `index.html` dans un navigateur.

## Vidéo de démonstration

🎥 [Voir la démonstration de l'application (Google Drive)](https://drive.google.com/file/d/1-kYX_8K-6zWjCataKrKYLQ0ocIeg4yIL/view?usp=sharing)

## Fonctionnalités

**Espace public**
- Catalogue de voitures **à vendre** et **à louer**, avec recherche, filtre par marque et par tranche de prix
- Fiche détaillée de chaque voiture
- Demande d'achat et demande de location (calcul automatique du prix selon la durée, dates validées)
- Formulaire de contact

**Espace administrateur**
- Ajout, modification et suppression de voitures
- Tableau de bord (stock, ventes, locations, dernières voitures ajoutées)
- Boîte de réception des messages et des demandes clients (marquer comme lu, supprimer)

## Utilisation

1. Télécharger ou cloner le dépôt.
2. Ouvrir `index.html` dans un navigateur récent.
3. Cliquer sur **Connexion Admin**. Au premier lancement, l'application demande de **créer l'identifiant et le mot de passe** de l'administrateur (8 caractères minimum). Aucun identifiant n'est écrit dans le code.

```bash
git clone https://github.com/elmahdaouia241-lang/gestion-voitures.git
```

## Données et sécurité

- Les voitures, les messages et le compte administrateur sont enregistrés dans le **localStorage** du navigateur : ils survivent au rechargement de la page, mais restent propres à chaque navigateur.
- Le mot de passe administrateur n'est jamais conservé en clair : seul un hash SHA-256 salé est stocké.
- Tout texte saisi par les utilisateurs est échappé avant affichage (protection contre l'injection de HTML/JavaScript) et seules les images `http(s)` sont acceptées.

## Limites

Projet pédagogique, entièrement côté client : un utilisateur qui maîtrise les outils de développement du navigateur peut modifier les données locales ou contourner l'écran de connexion. Pour une vraie mise en production, il faudrait un back-end (API et base de données) pour l'authentification et le stockage. L'envoi d'e-mails est simulé (affichage dans la console).

## Technologies

HTML5 · CSS3 · JavaScript (ES6) · localStorage · Web Crypto API
