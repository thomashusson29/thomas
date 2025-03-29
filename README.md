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
