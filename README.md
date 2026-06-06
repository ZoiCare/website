# ZoiCare Marketing Website

Landing page Astro pour ZoiCare, application de rendez-vous avec des professionnels animaliers et carnet de santé animal.

Le site est prévu pour `https://zoicare.fr` et contient une version française, une version anglaise, les pages légales françaises et le SEO de base.

## Stack

- Astro
- TypeScript
- CSS natif
- Déploiement Vercel
- GitHub Actions

## Commandes

Installer les dépendances :

```bash
npm install
```

Lancer le serveur local :

```bash
npm run dev
```

Vérifier et générer le site :

```bash
npm run build
```

Prévisualiser le build :

```bash
npm run preview
```

## Pages

- `/` : landing page française
- `/en/` : landing page anglaise
- `/mentions-legales/` : mentions légales
- `/politique-confidentialite/` : politique de confidentialité RGPD/CNIL
- `/cookies/` : politique cookies
- `/conditions-utilisation/` : conditions générales d’utilisation
- `/plan-du-site/` : plan du site HTML

## SEO

Le site inclut :

- balises title et meta description par page principale
- canonical URL
- `hreflang` français/anglais sur les landing pages
- Open Graph
- Twitter Card
- JSON-LD `MobileApplication`
- JSON-LD `FAQPage`
- JSON-LD `WebSite` / `Organization`
- sitemap XML généré par `@astrojs/sitemap`
- `robots.txt`

Sitemap XML :

```text
https://zoicare.fr/sitemap-index.xml
```

## Assets principaux

Les assets publics sont dans `public/` :

- `zoicare-logo.svg`
- `favicon.svg`
- `apple-logo.svg`
- `google-play-logo.svg`
- `IMG_3020.jpg` : screenshot Home
- `health.jpg` : screenshot Santé
- `charte.jpg` : charte graphique

## Déploiement Vercel

La configuration Vercel est dans :

- `vercel.json`
- `.github/workflows/vercel.yml`

Secrets GitHub nécessaires :

- `VERCEL_TOKEN`
- `VERCEL_ORG_ID`
- `VERCEL_PROJECT_ID`

Comportement du workflow :

- pull request : déploiement preview
- push sur `main` : déploiement production

## Points à compléter avant publication

- Remplacer les liens App Store et Google Play dans `src/pages/index.astro` et `src/pages/en/index.astro` quand les fiches officielles sont publiées.
- Compléter les informations éditeur dans `src/pages/mentions-legales.astro` : dénomination, adresse, SIRET/RCS, TVA, directeur de publication, etc.
- Vérifier la politique cookies si un outil d’analytics est ajouté.

## Structure utile

```text
src/
  layouts/
    LegalLayout.astro
  pages/
    index.astro
    en/index.astro
    mentions-legales.astro
    politique-confidentialite.astro
    cookies.astro
    conditions-utilisation.astro
    plan-du-site.astro
  styles/
    global.css
public/
  *.svg
  *.jpg
.github/workflows/
  vercel.yml
```

## Contact

Contact officiel : `contact@zoicare.fr`
