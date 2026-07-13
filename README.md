# 📜 Les Aventuriers de Sylve

Une application web gamifiée pour gérer des quêtes, des profils d'aventuriers et une messagerie en temps réel. Scannez des codes QR pour accepter et terminer des quêtes !

## 🎮 Fonctionnalités

✅ **Profil d'Aventurier**
- Gestion du nom et du pseudo
- Système de rangs (E à SSS+)
- Accumulation de points et progression

⚔️ **Système de Quêtes**
- Accepter des quêtes via scan de codes QR
- Terminer des quêtes et gagner des points
- Suivi des quêtes en cours et terminées

📷 **Scanner QR Code**
- Accès à la caméra du téléphone/ordinateur
- Scan de codes pour les quêtes
- Gestion robuste des permissions et erreurs

💬 **Messagerie de la Guilde**
- Chat en direct avec les autres aventuriers
- Notifications du système
- Historique sauvegardé localement

💾 **Stockage Local**
- Données persistantes (localStorage)
- Aucun serveur requis
- Données sauvegardées automatiquement

## 🚀 Démarrage Rapide

### Accès Direct
L'application est déployée sur GitHub Pages :
👉 [Les Aventuriers de Sylve](https://pirate40809.github.io/Les-Aventuriers-de-Sylve/)

### Utilisation Locale
1. Clonez le dépôt :
```bash
git clone https://github.com/Pirate40809/Les-Aventuriers-de-Sylve.git
cd Les-Aventuriers-de-Sylve
```

2. Ouvrez `index.html` dans votre navigateur
```bash
# Sur Windows
start index.html

# Sur Mac
open index.html

# Sur Linux
xdg-open index.html
```

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
├── index.html          # Application principale (HTML + CSS + JS)
├── README.md          # Ce fichier
└── .gitignore         # Fichiers ignorés par Git
```

## 📝 Améliorations Apportées

✨ **Version 2.0** :
- ✅ Correction de la bibliothèque QR Code (`html5-qrcode`)
- ✅ Suppression du HTML en double
- ✅ Gestion robuste des erreurs de caméra
- ✅ Système de notifications (succès/erreur)
- ✅ États de chargement visuels
- ✅ Meilleure accessibilité
- ✅ Code mieux documenté
- ✅ CSS optimisé et responsive

## 🎯 Prochaines Fonctionnalités Possibles

- [ ] Système de difficulté des quêtes
- [ ] Tableau de bord avec statistiques
- [ ] Quêtes quotidiennes
- [ ] Système de récompenses avancé
- [ ] Base de données cloud (optionnel)
- [ ] Mode multijoueur

## 🐛 Rapporter un Bug

Si vous trouvez un bug :
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

**Bienvenue à la Guilde des Aventuriers de Sylve ! 🗡️**
