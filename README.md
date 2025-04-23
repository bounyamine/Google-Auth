# Authentification Google

![Statut du Projet](https://img.shields.io/badge/statut-fonctionnel-brightgreen)
![Version](https://img.shields.io/badge/version-1.0.0-blue)
![Licence](https://img.shields.io/badge/licence-MIT-green)

> Système d'authentification légère utilisant Google Identity Services pour les applications web en HTML/CSS/JavaScript

## 📌 Aperçu

Cette solution permet d'intégrer facilement une authentification Google dans votre site web grâce à l'API Google Identity Services. Les utilisateurs peuvent se connecter avec leur compte Google, et leurs informations de profil sont affichées sur votre site.

![Démonstration de l'authentification Google](https://via.placeholder.com/800x400?text=D%C3%A9monstration+Authentification+Google)

## ✨ Fonctionnalités

- Authentification en un clic avec Google
- Stockage du token d'authentification en local pour maintenir la session
- Affichage des informations de profil de l'utilisateur (nom, email, photo)
- Fonctionnalité de déconnexion
- Gestion des erreurs avec promises et async/await
- Design responsive et moderne

## 🚀 Installation

1. Clonez ce dépôt ou téléchargez le fichier HTML
```bash
git clone https://github.com/bounyamine/Google-Auth.git
```

2. Ouvrez le fichier HTML dans votre éditeur et remplacez l'ID client Google par le vôtre
```html
<div id="g_id_onload"
     data-client_id="VOTRE_ID_CLIENT.apps.googleusercontent.com"
     data-callback="handleCredentialResponse">
</div>
```

3. Déployez le fichier sur votre serveur web ou testez-le localement

## 📋 Prérequis

Pour utiliser cette solution, vous devez :

1. Créer un projet dans la [Google Cloud Console](https://console.cloud.google.com/)
2. Activer l'API Google Identity
3. Configurer un écran de consentement OAuth
4. Créer des identifiants OAuth 2.0 pour votre application web
5. Définir les origines JavaScript autorisées dans la console Google Cloud

## 📝 Configuration de Google Cloud

1. Accédez à [Google Cloud Console](https://console.cloud.google.com/)
2. Créez un nouveau projet ou sélectionnez un projet existant
3. Dans le menu de navigation, allez dans "APIs & Services" > "Credentials"
4. Cliquez sur "Create Credentials" > "OAuth client ID"
5. Sélectionnez "Web application" comme type d'application
6. Donnez un nom à votre client OAuth
7. Ajoutez les URLs de votre application dans "Authorized JavaScript origins"
   - Pour le développement local : `http://localhost` ou `http://localhost:PORT`
   - Pour la production : `https://votre-domaine.com`
8. Cliquez sur "Create" et notez votre ID client

## 🔧 Personnalisation

Vous pouvez personnaliser l'apparence en modifiant les styles CSS dans la section `<style>` du fichier HTML.

```css
.container {
    background-color: #yourcolor;
    /* autres styles... */
}
```

## 📚 Structure du Code

Le code est organisé en composants clés :

- **HTML** : Structure de base avec conteneur pour le bouton de connexion et les informations utilisateur
- **CSS** : Styles pour la présentation et la mise en page
- **JavaScript** :
  - `handleCredentialResponse()` : Gère la réponse d'authentification de Google
  - `decodeJwtResponse()` : Décode le token JWT pour extraire les informations utilisateur
  - `signOut()` : Gère la déconnexion
  - Gestionnaire `onload` : Vérifie si l'utilisateur est déjà connecté

## 🛠️ Fonctionnement Technique

1. **Authentification** : Le bouton Google utilise l'API Google Identity pour authentifier l'utilisateur
2. **Traitement du Token** : Le token JWT est décodé pour extraire les informations utilisateur
3. **Stockage de Session** : Le token est stocké dans le localStorage pour maintenir la session
4. **Affichage** : Les informations de profil sont affichées à l'utilisateur

## ⚠️ Sécurité

- Cette solution utilise le localStorage pour stocker le token d'authentification
- Pour les applications nécessitant une sécurité renforcée, envisagez d'utiliser une solution serveur
- Le token JWT côté client doit être considéré comme non sécurisé pour les opérations sensibles

## 🤝 Contribuer

Les contributions sont les bienvenues ! N'hésitez pas à :

1. Fork le projet
2. Créer une branche pour votre fonctionnalité (`git checkout -b feature/amazing-feature`)
3. Commit vos changements (`git commit -m 'Ajout d'une fonctionnalité incroyable'`)
4. Push vers la branche (`git push origin feature/amazing-feature`)
5. Ouvrir une Pull Request

## 📄 Licence

Ce projet est sous licence MIT. Voir le fichier [LICENSE](LICENSE) pour plus de détails.

## 📮 Contact

Pour toute question ou suggestion, n'hésitez pas à ouvrir une issue ou à me contacter directement.

---

Développé avec ❤️ par [Votre Nom](https://github.com/bounyamine)
