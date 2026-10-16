# ZemScale

Site vitrine statique : 13 pages HTML, sans installation ni compilation.
Cette copie correspond à la dernière version validée dans la conversation.

## Contenu

- `site/` : les pages du site, leurs styles, scripts et illustrations SVG intégrés.
- `.github/workflows/pages.yml` : publication automatique sur GitHub Pages.

## Mise en ligne

1. Créer un dépôt GitHub, par exemple `zemscale`.
2. Importer **le contenu de ce dossier**, avec `.github/` et `site/`, dans le dépôt sur la branche `main`.
3. Dans le dépôt : **Settings → Pages → Source → GitHub Actions**.
4. Dans **Actions**, ouvrir **Publier ZemScale sur GitHub Pages**, puis **Run workflow**, branche `main`.
5. À la fin du déploiement, ouvrir l’URL affichée dans le résultat du workflow.

Chaque nouveau push sur `main` publie les modifications. Les liens relatifs fonctionnent aussi sous `/zemscale/`.

Avec GitHub Free, utiliser un dépôt public pour GitHub Pages. Un dépôt privé nécessite un forfait compatible.

## Import avec Git depuis votre ordinateur

Extraire l’archive, puis ouvrir un terminal dans `zemscale-github/`.
Remplacer `VOTRE-COMPTE` par votre identifiant GitHub ; créer au préalable le dépôt vide `zemscale`.

```bash
git init -b main
git add .
git commit -m "Ajouter le site ZemScale"
git remote add origin https://github.com/VOTRE-COMPTE/zemscale.git
git push -u origin main
```

L’authentification GitHub doit être configurée sur votre ordinateur. Aucun identifiant n’est inclus dans cette archive.

## Modifier le site

Modifier les fichiers de `site/`, puis pousser les changements sur `main`.
Les styles et scripts sont intégrés à chaque page. Le site ne dépend pas de Sites pour fonctionner.

Pour une consultation locale :

```bash
python3 -m http.server 8000 --directory site
```

Ouvrir http://localhost:8000.

## À connaître

- Le formulaire prépare une demande à copier. Il n’envoie pas d’email.
- La carte Google Maps montre la zone ZAD à Ouagadougou, pas une adresse de bureau vérifiée.
- Les produits présentés sont en préparation ou à l’étude.

## Documentation

- https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
- https://docs.github.com/en/get-started/start-your-journey/deploying-your-website-automatically
