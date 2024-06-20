# Git

Git est un outil qui permet de garder une trace des différentes versions d'un projet informatique. Ainsi toutes les modifications apportées dans un projet sont enregistrées et il est donc possible de revenir en arrière si nécessaire. Dans le cadre d'un travail collaboratif, Git permet à chacun de voir ce que les autres ont fait et de combiner leurs changements de manière ordonnée.


## Rapide tour d'horizon

Il est important de bien saisir certaines notions fondamentales pour aborder sereinement Git.

### 1. La notion de dépôt
Un dépôt Git est un espace de stockage qui contient tous les fichiers, dossiers, et l'historique complet de toutes les modifications apportées à un projet. Il permet de suivre les évolutions du projet au fil du temps, de gérer les versions, et de collaborer avec d'autres développeurs. Le dépôt peut être local, c'est-à-dire sur sa propre machine, ou distant, hébergé sur un serveur pour faciliter le partage et la collaboration.

### 2. La notion de branche
Une branche dans Git est une version parallèle du projet, permettant de développer des fonctionnalités, corriger des bugs ou tester des idées sans affecter la branche principale (généralement appelée master ou main). Chaque branche peut avoir son propre historique de commits et être fusionnée avec d'autres branches pour intégrer les modifications. Les branches facilitent le travail collaboratif et la gestion des différentes versions d'un projet.


## Créer un dépôt Git

Pour commencer à travailler avec Git, il faud déjà avoir un dépôt local. Pour ce faire, deux solutions : 

### 1. Cloner un dépôt distant :
Il est possible de créer une copie locale d'un dépôt distant grâce à la commande `git clone [url]`, où `[url]` est l'adresse du dépôt que l'on souhaite récupérer.

### 2. Initier un nouveau dépôt :
On peut également initier un nouveau dépôt dans le répertoire courant avec la commande `git init`. Dans ce cas, il faudra également associer ce dépôt local à un dépôt distant en utilisant la commande `git remote add origin [url]`, où `[url]` est l'adresse du dépôt distant que l'on souhaite associer.


## Gérer les modifications avec Git

Après avoir créé ou cloné un dépôt, voici les commandes essentielles pour gérer les modifications et suivre l'évolution de son projet :

### 1. Ajouter des fichiers à la zone de staging :
La **zone de staging** est une étape intermédiaire où les modifications de fichiers sont préparées et organisées avant d'être committées. Pour cela, on utilise la commande `git add`. Il est possible d'ajouter plusieurs fichiers à la fois, et même d'ajouter tous les fichiers modifiés d'un coup : 
```bash
git add [fichier]              # ajout d'un fichier spécifique
git add [fichier1] [fichier2]  # ajout de deux fichiers spécifiques
git add .                      # ajout de l'ensemble des fichiers modifiés
```

### 2. Faire un commit :
La commande `git commit` enregistre les modifications de la zone de staging dans l'historique du dépôt. Chaque commit doit être accompagné d'un message décrivant les changements : 
```bash
git commit -m "Description des modifications"
```

### 3. Vérifier l'état des fichiers :
La commande `git status` affiche l'état actuel du répertoire de travail et de la zone de staging. Elle indique les fichiers modifiés, ajoutés, ou supprimés, ainsi que ceux qui sont prêts à être committés.

### 4. Consulter l'historique des commits :
La commande `git log` affiche l'historique des commits du dépôt. Cette commande montre les messages de commit, les auteurs, et les dates des changements.

### 5. Pousser les modifications vers le dépôt distant :
Une fois les modifications committées, on peut les envoyer vers le dépôt distant avec la commande `git push`. Cette commande synchronise le dépôt local avec le dépôt distant, permettant ainsi à d'autres collaborateurs de voir nos changements.
```bash
git push origin master  # envoi des modifications vers la branche master du dépôt distant
```
* `git diff [hash1] [hash2]` : permet d'afficher les différences entre deux versions
* `git fetch`
* `git pull`

* `git merge`


## Travailler avec les branches dans Git

Les branches sont une fonctionnalité clé de Git, permettant de travailler sur différentes versions d'un projet simultanément. 

### 1. Créer une nouvelle branche :
La commande `git branch` sert à créer une nouvelle branche. Cela permet de développer des fonctionnalités ou de tester des idées sans affecter la branche principale.
```bash
git branch [nouvelle branche]
```

### 2. Basculer entre les branches :
La commande `git checkout` permet de changer de branche. Cela met à jour le répertoire de travail avec les fichiers de la branche sélectionnée. Cette commande sert également à revenir à un certain commit. On renseigne alors le **hash** du commit vers lequel on veut aller. Le hash est un identifiant unique associé à chaque commit. On peut le trouver avec la commande `git log`.
```bash
git checkout [nouvelle branche]
git checkout [hash d'un commit]
```

### 3. Fusionner les branches :
La commande `git merge` permet de fusionner les modifications d'une branche dans une autre, intégrant ainsi les nouvelles fonctionnalités ou corrections.
```bash
git checkout master  # on revient sur la branche principale sur laquel on veut intégrer les modifications
git merge [nouvelle branche]
```

### 4. Supprimer une branche :
Après avoir fusionné les modifications, on peut supprimer une branche avec la commande `git branch -d` :
```bash
git branch -d nouvelle-branche
```
