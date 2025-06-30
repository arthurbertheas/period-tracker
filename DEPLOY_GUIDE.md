# Déploiement Gratuit - Guide Simple avec Railway

Render.com pose des problèmes de build avec notre configuration. Railway.app est plus simple et fonctionne mieux pour les applications Node.js.

## Option 1 : Railway.app (RECOMMANDÉ)

### Étape 1 : Préparer GitHub
1. Crée un repository "period-tracker" sur GitHub
2. Upload tous les fichiers SAUF `node_modules/` et `.replit`
3. Assure-toi d'inclure le fichier `railway.json`

### Étape 2 : Déployer sur Railway
1. Va sur railway.app
2. Inscris-toi avec GitHub
3. "New Project" → "Deploy from GitHub repo"
4. Sélectionne ton repository
5. Railway détecte automatiquement Node.js
6. Clique "Deploy"

### Résultat
- URL gratuite : `https://period-tracker-production.up.railway.app`
- Application en ligne 24h/24
- Identifiants : mot de passe `mon-amour-2024`

## Option 2 : Render.com (si Railway ne marche pas)

Essaie la configuration corrigée dans `render.yaml` qui installe Vite globalement.

## Option 3 : Vercel (Frontend seulement)

Si tu n'as besoin que du frontend, Vercel est gratuit et très simple.

**Railway reste la meilleure option pour ton cas d'usage.**