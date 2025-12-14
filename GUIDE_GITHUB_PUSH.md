# 📤 GUIDE - PUSHER LES FICHIERS SUR GITHUB

## 🎯 OBJECTIF

Envoyer tous les fichiers du projet sur ton repo GitHub pour que Netlify puisse builder le site avec Netlify CMS.

---

## 📋 PRÉREQUIS

✅ Tu as un repo GitHub créé  
✅ Tu as connecté Netlify au repo  
✅ Tu as activé Identity + Git Gateway  

---

## 🚀 MÉTHODE 1 : AVEC GITHUB DESKTOP (LE PLUS SIMPLE)

### **Si tu as GitHub Desktop installé :**

1. **Ouvre GitHub Desktop**
2. **File → Add Local Repository**
3. **Sélectionne le dossier de ton projet** (là où est index.html)
4. Si c'est pas encore un repo Git, il va demander "Create Repository" → **Accepte**
5. **Commit** :
   - Message : "Setup Netlify CMS + Blog system"
   - Clique sur **"Commit to main"**
6. **Push** :
   - Clique sur **"Push origin"** en haut
7. ✅ **C'EST FAIT !**

---

## 🚀 MÉTHODE 2 : AVEC LA LIGNE DE COMMANDE

### **Si tu préfères le terminal :**

1. **Ouvre un terminal** dans le dossier du projet

2. **Initialise Git** (si pas déjà fait) :
   ```bash
   git init
   ```

3. **Connecte au repo GitHub** :
   ```bash
   git remote add origin https://github.com/TON_USERNAME/melissa-videographie.git
   ```
   ⚠️ Remplace `TON_USERNAME` et `melissa-videographie` par tes vraies infos

4. **Ajoute tous les fichiers** :
   ```bash
   git add .
   ```

5. **Commit** :
   ```bash
   git commit -m "Setup Netlify CMS + Blog system"
   ```

6. **Push** :
   ```bash
   git push -u origin main
   ```
   
   Si erreur "branch main doesn't exist", essaie :
   ```bash
   git branch -M main
   git push -u origin main
   ```

7. ✅ **C'EST FAIT !**

---

## 🚀 MÉTHODE 3 : AVEC L'INTERFACE GITHUB WEB (SI BLOQUÉ)

### **Upload direct via GitHub.com :**

1. Va sur **github.com/TON_USERNAME/melissa-videographie**
2. Clique sur **"Add file" → "Upload files"**
3. **Drag & drop TOUS les fichiers et dossiers**
4. Message de commit : "Setup Netlify CMS + Blog system"
5. Clique sur **"Commit changes"**
6. ✅ **C'EST FAIT !**

---

## 📂 FICHIERS À ENVOYER

Assure-toi d'avoir **TOUS ces fichiers** :

```
/
├── admin/
│   ├── config.yml
│   └── index.html
├── images/
│   └── uploads/
│       └── .gitkeep
├── journal/
│   └── .gitkeep
├── index.html
└── (tous les autres fichiers .md, .txt)
```

---

## ✅ VÉRIFICATION

Une fois pushé, vérifie sur **github.com** :
- ✅ Le dossier `admin/` est visible
- ✅ Le dossier `journal/` est visible
- ✅ Le fichier `index.html` est à jour

---

## 🔄 NETLIFY VA REBUILD

1. **Netlify détecte** le push sur GitHub
2. **Rebuild automatique** (30-60 secondes)
3. **Site mis à jour** avec Netlify CMS activé

Tu peux voir le build en direct :
```
Netlify Dashboard
→ Ton site
→ Onglet "Deploys"
```

---

## 🎯 APRÈS LE PUSH

**Attends 1-2 minutes** que Netlify rebuild le site.

Ensuite, va sur : **`ton-site.netlify.app/admin`**

Tu devrais voir l'**interface admin de Netlify CMS** ! 🎉

---

## ⚠️ SI TU GALÈRES

**Pas de panique !** Voici les problèmes courants :

### Problème 1 : "Remote origin already exists"
```bash
git remote remove origin
git remote add origin https://github.com/TON_USERNAME/ton-repo.git
```

### Problème 2 : "Permission denied"
- Tu dois configurer ton authentification GitHub
- Ou utilise GitHub Desktop (plus simple)

### Problème 3 : "Branch main doesn't exist"
```bash
git branch -M main
git push -u origin main
```

---

## 💬 BESOIN D'AIDE ?

**Dis-moi :**
- Quelle méthode tu utilises (Desktop, CLI, Web)
- Où tu bloques exactement
- Screenshot si besoin

**Et je te guide pas à pas ! 🤝**

---

## 🎉 PROCHAINE ÉTAPE

Une fois que tu as pushé sur GitHub :

**DIS-MOI "C'est pushé !"** 

Et je te guide pour :
1. Inviter Mélissa sur Netlify Identity
2. Tester l'interface admin
3. Publier le premier article de blog
4. Vérifier que tout fonctionne

---

**📤 PUSH SUR GITHUB ET ON CONTINUE ! 🚀**

*Guide créé pour Romain - GitHub Push 2025*
