# SK FLUX MASTER v12.0

Elite Arbitrage System — Dual-Asset · Sniper IA · Predictor · Logistique · Comparatif

## 🎯 À propos

SK FLUX MASTER est une application React 18 de pointe pour l'analyse et l'arbitrage de véhicules d'occasion. Système intelligent avec:

- ✅ Analyse IA des défauts
- ✅ Scoring et scoring de rotation de stock
- ✅ Coût d'opportunité (ROI par jour)
- ✅ Messages "Sniper" générés
- ✅ Vision plaque (prototype)
- ✅ Comparaison face-à-face
- ✅ Cartographie Prix/ROI

## 🚚 Structure du projet

```
.
├── src/
│   ├── App.jsx              # Composant principal React
│   ├── main.jsx             # Point d'entrée React
│   └── index.css            # Styles Tailwind
├── index.html               # Template HTML
├── package.json             # Dépendances nettoyées
├── vite.config.js           # Configuration Vite
├── tailwind.config.js       # Configuration Tailwind
├── postcss.config.js        # PostCSS pour Tailwind
└── dist/                    # Dossier de déploiement (généré par build)
```

## 🛠️ Installation & Développement

### Prérequis
- Node.js >= 16.x
- npm >= 8.x

### Installation

```bash
npm install --legacy-peer-deps
```

### Développement

```bash
npm run dev
```

L'application sera accessible à `http://localhost:5173`

### Build pour la production

```bash
npm run build
```

Cela génère les fichiers optimisés dans le dossier `dist/`

### Vérifier le build

```bash
npm run preview
```

## 🚀 Déploiement

### Option 1 : Vercel (Recommandé)

```bash
npm install -g vercel
vercel
```

### Option 2 : Netlify

```bash
npm install -g netlify-cli
netlify deploy --prod --dir=dist
```

### Option 3 : Any Static Hosting

Uploadez le contenu du dossier `dist/` sur:
- GitHub Pages
- AWS S3
- Azure Static Web Apps
- Cloudflare Pages
- Etc.

### Option 4 : Docker

```dockerfile
FROM node:18-alpine
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm install --legacy-peer-deps
COPY . .
RUN npm run build
FROM nginx:alpine
COPY --from=0 /app/dist /usr/share/nginx/html
EXPOSE 80
```

## 📦 Dépendances clés

- **React** 18.3.1 - Framework UI
- **Vite** 5.0.8 - Build tool
- **Tailwind CSS** 3.3.6 - Styling
- **Recharts** 3.8.1 - Graphiques
- **Lucide React** 0.365.0 - Icônes

## ✅ Corrections et améliorations

✓ Restructuration en projet Vite propre
✓ HTML template approprié
✓ Configuration build optimisée
✓ Dépendances actualisées et complètes
✓ Scripts npm prêts pour production
✓ Tailwind CSS configuré
✓ Assets minifiés avec esbuild

## 🐛 Dépannage

**Q: Le build échoue?**
R: Assurez-vous que `npm install --legacy-peer-deps` a été exécuté.

**Q: La page est blanche?**
R: Vérifiez la console pour les erreurs. Assurez-vous que le dossier `dist/` a bien été généré.

**Q: Comment ajouter de nouvelles dépendances?**
R: `npm install --legacy-peer-deps <package-name>`

## 📝 Build Info

- Build: 2026.05.02
- Version: 12.0.0
- Stack: React 18 · Vite · Tailwind · Recharts
