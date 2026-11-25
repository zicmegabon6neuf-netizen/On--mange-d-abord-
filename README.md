# ON MANGE D'ABORD — version professionnelle

Cette version est une application web avec pages HTML/CSS/JS, serveur Node.js et base SQLite.
L'espace administrateur est protégé côté serveur : création initiale avec confirmation du mot de passe, hachage bcrypt, sessions HTTP-only/SameSite, limitation des tentatives de connexion. Les commandes sont centralisées dans SQLite.

## Installation
Prérequis : Node.js 20+.
```bash
npm install
export SESSION_SECRET="$(openssl rand -hex 32)"
NODE_ENV=production npm start
```
Ouvrir `http://localhost:3000`. Pour créer le compte, ouvrir `/admin.html`. Définis un identifiant et un mot de passe d'au moins 12 caractères puis confirme-le. La création initiale est possible une seule fois.

## Mise en ligne
Déployer sur un hébergeur Node.js, activer HTTPS, définir `NODE_ENV=production`, utiliser un stockage de session persistant et configurer sauvegardes et protection CSRF. Cette archive ne crée pas elle-même un hébergement ni un nom de domaine.

## Paiements
Le site enregistre le mode choisi. La validation du paiement reste manuelle par l'administrateur. Aucun PIN client n'est collecté. Vérifier les codes et procédures marchands Moov/Airtel auprès des opérateurs. Numéros initiaux à confirmer dans Réglages : WhatsApp +24162098889, Moov 062098889, Airtel vide.
Les plats/prix initiaux sont des exemples modifiables.
