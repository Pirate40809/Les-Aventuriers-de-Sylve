# 📜 Les Aventuriers de Sylve

Une application web **isekai gamifiée** pour gérer des quêtes, des profils d'aventuriers et une messagerie en temps réel avec amis ! 🗡️✨

## 🎮 Fonctionnalités

✅ **Profil d'Aventurier**
- Système de rangs (E à SSS+)
- Accumulation de points et progression
- **Pseudo personnalisable**

⚔️ **Système de Quêtes**
- Accepter des quêtes via scan de codes QR
- Terminer des quêtes et gagner des points
- Suivi des quêtes en cours et terminées

📷 **Scanner QR Code**
- Scan de codes pour les quêtes
- Gestion robuste des permissions

📸 **Caméra**
- Bouton séparé pour activer la caméra
- Accès direct aux permissions

💬 **Messagerie en Temps Réel**
- Chat public avec la guilde entière
- **Chat privé avec tes amis** 🎭
- Notifications instantanées
- Socket.io pour la synchronisation

👥 **Système d'Amis**
- Ajouter des amis par pseudo
- Chat privé exclusif
- Notifications de messages

🔔 **Notifications**
- Messages reçus
- Amis en ligne
- Quêtes complétées

💾 **Backend Serveur**
- Node.js + Express
- MongoDB pour les données
- Socket.io pour le temps réel
- Déployé sur Render (gratuit)

## 🚀 Démarrage Rapide

### Online (Déployé)
👉 [Les Aventuriers de Sylve](https://pirate40809.github.io/Les-Aventuriers-de-Sylve/)

⚠️ **Important** : Configure d'abord le backend pour que tout fonctionne !
Voir [INSTALLATION.md](INSTALLATION.md)

### Local
1. Clonez le dépôt :
```bash
git clone https://github.com/Pirate40809/Les-Aventuriers-de-Sylve.git
cd Les-Aventuriers-de-Sylve
```

2. Installez le backend :
```bash
cd backend
npm install
```

3. Configurez `.env` :
```bash
cp .env.example .env
# Édite .env avec tes infos MongoDB
```

4. Lancez le serveur :
```bash
npm start
```

5. Ouvrez `index.html` dans votre navigateur

## 📱 Codes QR Disponibles

| Code | Action |
|------|--------|
| `quete1` | Accepter la quête "Nettoyer la taverne (Rang E)" |
| `fin1` | Terminer la quête en cours et gagner 250 points |

### Créer vos propres codes QR
1. Allez sur [QR Code Generator](https://www.qr-code-generator.com/)
2. Entrez le code (ex: `quete1`)
3. Générez et imprimez le code QR
4. Scannez avec l'application !

## 🛠️ Architecture

```
Les-Aventuriers-de-Sylve/
├── index.html              # Frontend isekai
├── backend/
│   ├── server.js          # Backend Node.js
│   ├── package.json       # Dépendances
│   └── .env.example       # Config
├── INSTALLATION.md        # Guide complet
└── README.md             # Ce fichier
```

## 📊 Stack Technique

**Frontend:**
- HTML5 + CSS3 (Design isekai/fantasy)
- JavaScript Vanilla
- Socket.io (client)
- html5-qrcode (Scanner QR)

**Backend:**
- Node.js + Express
- Socket.io (serveur)
- MongoDB Atlas (base de données)
- CORS pour la sécurité

**Déploiement:**
- Frontend : GitHub Pages
- Backend : Render.com (gratuit)
- Base de données : MongoDB Atlas (gratuit)

## 🎨 Design Isekai

- 🎭 Couleurs fantasy (or, pourpre, marron)
- 📜 Polices élégantes (Cinzel, Crimson Text)
- ✨ Animations fluides et éléments visuels
- 📱 Responsive et mobile-friendly
- 🌙 Thème sombre immersif

## 📝 Fonctionnalités Avancées

### Chat Privé
1. Ajoute des amis via le bouton "Ajouter"
2. Clique sur le bouton 💬 d'un ami
3. Chat privé synchronisé en temps réel

### Système de Notifications
- Notifications toast pour tous les événements
- Notification de nouveaux messages
- Historique des notifications

### Gestion du Pseudo
1. Modifie ton pseudo dans la section "Profil"
2. Clique ✓ pour valider
3. Tous les autres joueurs verront ton nouveau pseudo

## 🎯 Prochaines Fonctionnalités Possibles

- [ ] Guildes/Clans
- [ ] Système de difficulté des quêtes
- [ ] Tableau de bord avec statistiques
- [ ] Quêtes quotidiennes
- [ ] Système de récompenses avancé
- [ ] Base de données cloud (optionnel)
- [ ] Achievements/Badges
- [ ] Classement global

## 🐛 Rapporter un Bug

Si tu trouves un bug :
1. Allez sur [Issues](https://github.com/Pirate40809/Les-Aventuriers-de-Sylve/issues)
2. Cliquez sur "New Issue"
3. Décrivez le problème en détail

## 💡 Contribuer

Les contributions sont bienvenues !
1. Fork le dépôt
2. Créez une branche (`git checkout -b feature/amelioration`)
3. Committez vos changements (`git commit -m 'Ajout de...'`)
4. Poussez vers la branche (`git push origin feature/amelioration`)
5. Ouvrez une Pull Request

## 📜 Licence

Ce projet est sous licence MIT. Voir le fichier `LICENSE` pour plus de détails.

## ✉️ Contact

Créé par [Pirate40809](https://github.com/Pirate40809)

---

## 🔗 Liens Importants

- 📖 [Guide Installation Complet](INSTALLATION.md)
- 🌐 [Application Live](https://pirate40809.github.io/Les-Aventuriers-de-Sylve/)
- 🐙 [GitHub Repository](https://github.com/Pirate40809/Les-Aventuriers-de-Sylve)
- 💾 [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)
- 🚀 [Render.com](https://render.com)

---

**Bienvenue à la Guilde des Aventuriers de Sylve ! ⚔️✨**

Rejoins des milliers d'aventuriers et deviens une légende !
