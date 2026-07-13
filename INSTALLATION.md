# 📜 Les Aventuriers de Sylve - Guide Installation

## 🚀 Déploiement Complet (Frontend + Backend)

### Architecture
```
Frontend (GitHub Pages) ↔️ Backend (Render) ↔️ Database (MongoDB Atlas)
```

---

## 📋 Étape 1 : MongoDB Atlas (Gratuit)

### 1. Créer un compte MongoDB
1. Va sur [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)
2. Clique sur "Try Free"
3. Crée un compte (email/password ou Google)

### 2. Créer un cluster gratuit
1. Clique sur "Create a Deployment"
2. Sélectionne "Free" (M0 Sandbox)
3. Choisis ta région (Europe si possible)
4. Clique "Create Deployment"
5. Attends 5-10 minutes que le cluster se crée

### 3. Créer un utilisateur de base de données
1. Va dans "Database Access"
2. Clique "Add Database User"
3. Crée un username et password (note-les!)
4. Clique "Add User"

### 4. Autoriser ton IP
1. Va dans "Network Access"
2. Clique "Add IP Address"
3. Sélectionne "Allow Access from Anywhere" (0.0.0.0/0)
4. Clique "Confirm"

### 5. Récupérer la connection string
1. Va dans "Databases"
2. Clique "Connect" sur ton cluster
3. Choisis "Node.js"
4. Copie la connection string
5. Remplace `<username>` et `<password>` par tes identifiants
```
mongodb+srv://username:password@cluster.mongodb.net/aventuriers-sylve?retryWrites=true&w=majority
```

---

## 🖥️ Étape 2 : Déployer le Backend sur Render

### 1. Pousser le backend sur GitHub
```bash
git add backend/
git commit -m "Ajout du backend Node.js"
git push origin main
```

### 2. Créer un compte Render
1. Va sur [Render.com](https://render.com)
2. Clique "Sign Up"
3. Connecte-toi avec GitHub
4. Autorise Render à accéder à tes repos

### 3. Créer un service Web
1. Clique "New +" → "Web Service"
2. Connecte ton repo "Les-Aventuriers-de-Sylve"
3. Configure :
   - **Name** : `aventuriers-sylve-api`
   - **Root Directory** : `backend`
   - **Build Command** : `npm install`
   - **Start Command** : `npm start`
   - **Plan** : Free (gratuit)

### 4. Ajouter les variables d'environnement
1. Scroll down jusqu'à "Environment"
2. Clique "Add Environment Variable"
3. Ajoute :
   - **MONGODB_URI** : `mongodb+srv://username:password@cluster.mongodb.net/aventuriers-sylve?retryWrites=true&w=majority`
   - **CLIENT_URL** : `https://pirate40809.github.io/Les-Aventuriers-de-Sylve`
   - **NODE_ENV** : `production`

### 5. Déployer
1. Clique "Create Web Service"
2. Attends 5-10 minutes le déploiement
3. Tu recevras une URL comme : `https://aventuriers-sylve-api.onrender.com`

---

## 🌐 Étape 3 : Configurer le Frontend

### Mettre à jour l'URL du backend
Dans `index.html`, change :
```javascript
const BACKEND_URL = 'http://localhost:5000';
```

Par :
```javascript
const BACKEND_URL = 'https://aventuriers-sylve-api.onrender.com';
```

Puis pousse sur GitHub :
```bash
git add index.html
git commit -m "Mise à jour URL backend"
git push origin main
```

---

## 🎮 Test Local (Avant de déployer)

### 1. Cloner et installer
```bash
git clone https://github.com/Pirate40809/Les-Aventuriers-de-Sylve.git
cd Les-Aventuriers-de-Sylve
cd backend
npm install
```

### 2. Créer `.env`
```bash
cp .env.example .env
```

Puis édite `.env` avec tes infos MongoDB.

### 3. Lancer le serveur
```bash
npm start
```

Tu dois voir :
```
✅ MongoDB connecté
🚀 Serveur lancé sur le port 5000
```

### 4. Ouvrir le frontend
```bash
# Dans un autre terminal
cd ..
# Ouvre index.html dans ton navigateur
```

---

## 🔧 Troubleshooting

### ❌ "MongoDB connection failed"
- ✅ Vérifies ton MONGODB_URI (username, password, spécial characters)
- ✅ Ajoute l'IP 0.0.0.0/0 dans Network Access

### ❌ "Cannot GET /api/users"
- ✅ Le backend n'est pas lancé
- ✅ Vérifies que BACKEND_URL est correcte dans index.html

### ❌ "Socket.io connection refused"
- ✅ CORS_ORIGIN doit avoir la bonne URL du frontend

### ❌ Render dit "Build failed"
- ✅ Vérifies que `backend/package.json` existe
- ✅ Vérifies que `backend/server.js` existe
- ✅ Regarde les logs Render pour plus de détails

---

## 📱 Ajouter ton domaine personnalisé

### Sur Render
1. Va dans "Settings" de ton service
2. Scroll jusqu'à "Custom Domain"
3. Ajoute `api.lesaventuriersdeSylve.com`
4. Ajoute les DNS records fournis

### Sur ton registrar (Namecheap, OVH, etc.)
1. Va dans DNS settings
2. Ajoute les CNAME records de Render

---

## 🚀 Commandes Utiles

```bash
# Démarrer le serveur
npm start

# Développement (avec hot reload)
npm run dev

# Vérifier MongoDB
# Dans MongoDB Atlas, va dans "Collections" pour voir les data

# Voir les logs Render
# Va sur le dashboard Render, clique "Logs"
```

---

## ✅ Checklist Finale

- [ ] MongoDB Atlas cluster créé
- [ ] Utilisateur BD créé
- [ ] IP autorisée (0.0.0.0/0)
- [ ] Backend sur Render déployé
- [ ] Variables d'environnement Render configurées
- [ ] Frontend `index.html` mis à jour avec URL Render
- [ ] Test local OK
- [ ] Domaine personnalisé configuré (optionnel)

---

## 🎉 C'est fini!

Ton app est maintenant :
- ✅ En ligne sur GitHub Pages
- ✅ Backend live sur Render
- ✅ Base de données dans MongoDB Atlas
- ✅ Chat en temps réel avec Socket.io
- ✅ Prête pour des centaines d'aventuriers!

**Accède à ton app :**
👉 https://pirate40809.github.io/Les-Aventuriers-de-Sylve/

---

## 📞 Support

Si tu as des problèmes :
1. Regarde les logs Render
2. Regarde la console du navigateur (F12)
3. Vérifie ta connection MongoDB
4. Redéploie sur Render (Push on GitHub triggère auto-redeploy)
