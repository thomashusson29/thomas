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
# Créer un site Bookdown et le publier sur GitHub Pages 🚀

Voici un guide simple pour créer un site avec **Bookdown**, l’héberger sur **GitHub Pages**, et pouvoir le mettre à jour facilement.

---

## 🧰 Prérequis

- Un compte GitHub
- R et RStudio installés sur ton ordinateur
- Le package `bookdown` installé dans R :

```r
install.packages("bookdown")
```

---

## 🛠️ Étapes de création

### 1. Cloner ton dépôt GitHub

```bash
git clone https://github.com/<TON-UTILISATEUR>/<NOM-DEPOT>.git
cd <NOM-DEPOT>
```

Remplace `<TON-UTILISATEUR>` et `<NOM-DEPOT>` par les bons noms.

### 2. Créer les fichiers Bookdown dans RStudio

Dans le dossier cloné, créer un projet RStudio (`.Rproj`) puis ajouter ces fichiers :

- `index.Rmd` → page d’accueil du site
- `mon_premier_chapitre.Rmd` → un chapitre du site
- `_bookdown.yml` → indique le nom du fichier HTML de sortie :

```yaml
book_filename: "index"
output_dir: "docs"
```

- `_output.yml` → spécifie le style du site :

```yaml
bookdown::gitbook:
  css: style.css
  split_by: chapter
  config:
    toc:
      collapse: none
      before: |
        <li><a href="./index.html">Accueil</a></li>
    download: ["pdf", "epub"]
```

Tu peux aussi ajouter un fichier `README.md` pour décrire ton projet.

### 3. Générer le site dans RStudio

Dans la console RStudio :

```r
bookdown::render_book("index.Rmd", "bookdown::gitbook")
```

Le site est généré dans le dossier `docs/`.

---

## 🚀 Mettre en ligne sur GitHub Pages

### 1. Commits & push

Dans le terminal ou Git Bash :

```bash
git add .
git commit -m "Ajout du site Bookdown"
git push
```

### 2. Activer GitHub Pages

- Va dans **Settings > Pages** de ton dépôt GitHub
- Choisis **Source : branch `main`, folder `/docs`**
- Clique sur **Save**

Ton site sera disponible à l’adresse :

```
https://<TON-UTILISATEUR>.github.io/<NOM-DEPOT>
```

---

## ✅ Astuce pour mise à jour

À chaque fois que tu veux mettre à jour :

1. Modifier les fichiers `.Rmd`
2. Re-lancer `bookdown::render_book(...)`
3. Faire `git add .`, `git commit -m "update"` puis `git push`

---

## 📁 Exemple de structure minimale

```
.
├── index.Rmd
├── mon_premier_chapitre.Rmd
├── _bookdown.yml
├── _output.yml
├── README.md
├── thomas.Rproj
└── docs/











