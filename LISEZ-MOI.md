# 📱 Shop-comp PWA — version iPhone / Web

L'app Shop-comp en version web installable (PWA). Fonctionne sur **iPhone** (Safari),
Android (Chrome) et ordinateur — mêmes données Firebase que l'app Android.

## ✨ Fonctions
- 📷 Scan code-barres avec la caméra (html5-qrcode)
- 📝 OCR multi-lignes avec sélection par cases à cocher (Tesseract.js)
- 🧠 Remplissage automatique du nom du produit depuis le cloud
- 📍 GPS + détection du magasin via OpenStreetMap
- ☁️ Prix partagés via Firebase (même base que l'appli Android)
- 🎨 5 thèmes (Indigo, Émeraude, Océan, Sunset, Mode sombre)
- 📴 Fonctionne hors-ligne une fois installée (sauf données cloud)

## 🚀 Mise en ligne (OBLIGATOIRE pour la caméra — HTTPS requis)

### Option A : GitHub Pages (gratuit, 5 minutes)
1. Va sur github.com → **New repository** → nomme-le `shopcomp-pwa` → **Public** → Create
2. **Add file → Upload files** → glisse TOUS les fichiers de ce dossier
   (`index.html`, `manifest.json`, `sw.js`, le dossier `icons/`)
3. **Commit changes**
4. **Settings → Pages** → Source: **Deploy from a branch** → Branch: `main` → Save
5. Attends 1-2 minutes → ton site est sur :
   `https://TON-NOM-UTILISATEUR.github.io/shopcomp-pwa/`

### Option B : Netlify Drop (encore plus simple)
1. Va sur **app.netlify.com/drop**
2. Glisse le dossier entier → tu obtiens une adresse HTTPS immédiate

## 📲 Installation sur iPhone
1. Ouvre l'adresse HTTPS dans **Safari**
2. Bouton **Partager** (carré avec flèche) → descendre → **Sur l'écran d'accueil**
3. Ajouter → l'app apparaît avec son icône, plein écran, comme une vraie app !

Sur Android/Chrome : menu ⋮ → **Installer l'application**.

## ⚠️ Notes
- La **caméra** (scan + photo OCR) ne fonctionne QUE sur un site **HTTPS**
  (GitHub Pages et Netlify le fournissent). Ouvrir `index.html` en local ne
  donne pas accès à la caméra.
- Le premier OCR télécharge le moteur (quelques Mo) — ensuite c'est en cache.
- Les données sont partagées avec l'appli Android : même base Firebase,
  mêmes règles de sécurité.
