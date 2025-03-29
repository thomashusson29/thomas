# Tutoriel interactif R — thomashusson29

Ce site créé avec **[Bookdown](https://bookdown.org/)** pour partager les quelques scripts trouvés et recensés pour l'analyse de données avec **R et RStudio**.  

📍 Le site est accessible ici :  
👉 **https://thomashusson29.github.io/thomas**

---

## 🔎 Contenu du site

Le site est organisé en plusieurs sections (en cours de rédaction), incluant notamment :

- Prise en main de R et RStudio
- Manipulation de données (`dplyr`, `tidyr`, etc.)
- Analyses statistiques (régressions, tests...)
- Création de graphiques (`ggplot2`)
- Export de tableaux et graphiques
- Analyse de survie, données longitudinales...

---

## 🚀 Pour générer le site en local

1. Cloner le dépôt :

```bash
git clone https://github.com/thomashusson29/thomas.git
```

2. Ouvrir le projet dans **RStudio**
3. Installer les packages nécessaires (si besoin) :

```r
install.packages("bookdown")
```

4. Générer le site :

```r
bookdown::render_book("index.Rmd", "bookdown::gitbook")
```

5. Pour publier en ligne :  
Le site est hébergé avec **GitHub Pages** depuis la branche `gh-pages`.

---

## 🧾 Licence

Contenu publié sous licence :  
**Creative Commons Attribution - Pas d’Utilisation Commerciale - Partage dans les Mêmes Conditions (CC BY-NC-SA)**  
[https://creativecommons.org/licenses/by-nc-sa/3.0/fr/](https://creativecommons.org/licenses/by-nc-sa/3.0/fr/)

---

## 🤝 Contribuer

Tu repères une faute, une amélioration possible ou tu veux proposer un nouveau chapitre ?  
Les contributions sont les bienvenues !

- Ouvre une **Issue**
- Ou propose directement une **Pull Request**

---
---
---









## Tutoriel pour GitHub (README.md, par exemple) :

---

```markdown
# Créer un site Bookdown et le publier sur GitHub Pages

Ce tutoriel vous guide pas à pas pour créer un site web avec **Bookdown** et le publier gratuitement avec **GitHub Pages**.

## 🧰 Prérequis

- Avoir un compte GitHub
- Avoir installé R, RStudio et les packages suivants :
  ```r
  install.packages("bookdown")
  ```

- Avoir installé Git sur votre ordinateur : [https://git-scm.com/downloads](https://git-scm.com/downloads)

## 🧱 Étapes

### 1. Cloner un dépôt GitHub vide (ou le vôtre)

```bash
git clone https://github.com/votre-utilisateur/nom-du-depot.git
cd nom-du-depot
```

> ⚠️ Remplacez `votre-utilisateur` et `nom-du-depot` par les bons noms.  
> Vous pouvez aussi créer le dépôt d'abord sur GitHub, puis le cloner.

---

### 2. Créer la structure d’un site Bookdown

Dans RStudio (dans le dossier cloné) :

1. **Ouvrez un nouveau projet R dans le dossier cloné**
2. Créez un fichier `index.Rmd` avec ce contenu minimal :

```markdown
---
title: "Mon site Bookdown"
author: "Moi"
site: bookdown::bookdown_site
documentclass: book
output: bookdown::gitbook
---

# Bienvenue

Ceci est un site généré avec **Bookdown**.
```

3. (Optionnel) Créez un autre chapitre, par exemple `premier-chapitre.Rmd` :

```markdown
# Premier chapitre

Voici un chapitre d'exemple.
```

4. Créez un fichier `_bookdown.yml` :

```yaml
book_filename: "mon_site"
output_dir: "docs"
rmd_files: ["index.Rmd", "premier-chapitre.Rmd"]
```

---

### 3. Générer le site Bookdown

Dans RStudio, exécutez :

```r
bookdown::render_book("index.Rmd", "bookdown::gitbook")
```

Un dossier `docs/` sera généré avec le site web dedans.

---

### 4. Commiter et envoyer sur GitHub

Dans Git Bash ou le terminal :

```bash
git add .
git commit -m "Ajout du site Bookdown"
git push
```

---

### 5. Activer GitHub Pages

1. Aller dans **Settings > Pages** du dépôt GitHub
2. Source : **Deploy from branch**  
   Branch: `main`, folder: `/docs`
3. Valider : GitHub Pages sera actif à l’URL  
   `https://votre-utilisateur.github.io/nom-du-depot`

---

### ✅ Résultat

Votre site Bookdown est en ligne ! 🎉

---

### 🔁 Mettre à jour le site

À chaque modification :

1. Modifier vos `.Rmd`
2. Regénérer avec `bookdown::render_book(...)`
3. `git add . && git commit -m "Update site" && git push`

---

### 📌 Conseils

- Gardez tous vos `.Rmd` dans l’ordre dans `_bookdown.yml`
- N’écrivez rien manuellement dans `docs/` : c’est généré automatiquement
- Vous pouvez ajouter un fichier `README.md` dans le dépôt pour la présentation sur GitHub

---

```

Souhaite-tu que je te le mette directement dans ton dépôt GitHub en tant que `README.md` ?
