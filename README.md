# brutxav.github.io

Site personnel de Xavier Bruant, construit avec [Quarto](https://quarto.org).

## Travailler en local

```bash
quarto preview      # aperçu live dans le navigateur, recharge à chaque sauvegarde
quarto render       # génère le site HTML dans _site/
```

## Où modifier quoi

| Quoi | Fichier |
|---|---|
| Contenu (profil, sections, cours, CV) | `index.qmd` |
| Items du bandeau, menu déroulant, footer | `_quarto.yml` |
| Couleurs, polices, **dégradé de fond** (`--bg-gradient`) | `styles.scss` |
| Rail de navigation à droite + scrollspy | `assets/scroll.html` |
| Images | `images/` |

Ajouter une section : copier un bloc `::: {#id .block}` dans `index.qmd`,
puis ajouter le lien dans `_quarto.yml` (bandeau) et dans `assets/scroll.html` (rail).

## Slides Quarto

Un fichier `.qmd` avec `format: revealjs` placé dans le projet (par ex. `slides/mon-talk.qmd`)
est compilé avec le site et publié à `https://brutxav.github.io/slides/mon-talk.html`.

## Publication

Chaque push sur `main` déclenche `.github/workflows/publish.yml`, qui compile le site
et le déploie sur GitHub Pages (réglage du repo : *Settings → Pages → Source : GitHub Actions*).
