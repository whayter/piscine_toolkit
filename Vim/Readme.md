# Vim

L'outil de base d'un développeur est l'éditeur de texte. Il en existe de très nombreux et sous toutes formes. De nos jours, il est très courant d'utiliser un **IDE** (pour environnement de développement intégré) comme **Visual Studio Code**. Cependant, les examens de la piscine sont réalisés sur des ordinateurs "rincés", sur lesquels tu ne retrouveras pas ton éditeur favori. Il est donc important de savoir utiliser les éditeurs installés par défaut sur les machines et je recommande de s'en tenir à ça pour la durée de la piscine. 

Pour ma part, j'ai longtemps utilisé Vim, et c'est donc cet éditeur que je vais te présenter. Vim est un **éditeur de texte** particulièrement apprécié pour sa puissance et sa flexibilité. Il est connu pour sa rapidité, sa capacité à gérer de très gros fichiers de manière efficace, et sa configuration hautement personnalisable.

on lance Vim tout simplement depuis un terminal en tapant `vim` suivit du nom de fichier que l'on veut éditer. Si le fichier n'existe pas encore, il sera créé. 


## Les modes

Vim est un **éditeur modal**, c'est à dire qu'il possède différents modes pour réaliser des tâches variées. Il y a trois modes de base : le mode normal ou mode commande (par défaut lorsque Vim démarre), le mode insertion, et le mode ligne de commande.

### 1. Le mode normal (commande)

C'est le mode par défaut lorsque Vim est lancé. Il permet de copier des lignes ou de les déplacer grâce à des raccourcis, de mettre du texte en forme, ou de se déplacer dans le fichier. Voici quelques commandes de base qui peuvent être très utiles :

* `y` pour copier le texte sélectionné
* `yy` pour copier la ligne courante
* `d` pour couper (copier + supprimer) le texte sélectionné
* `dd` pour couper la ligne courante
* `x` pour supprimer le caractère sous le curseur ou le texte sélectionné
* `r` suivi d'un caractère de remplacement pour remplacer le caractère sous le curseur par le caractère de remplacement
  
* `u` pour annuler la dernière action
* `ctrl + r` pour rétablir la dernière action annulée

* `s` pour upprimer le texte sélectionné et passer en mode insertion
* `S` pour supprimer la ligne courante et passer en mode insertion

### 2. Le mode insertion

Le mode insertion permet tout simplement d'entrer et de modifier du texte dans un document. Pour passer du mode normal au mode insertion, on utilise la touche `i` (pour insérer). Les flèches servent à déplacer le curseur dans le document.

Pour quitter le mode insertion, on appuie sur la touche `esc`. 

### 3. Le mode ligne de commande

Pour accéder au mode ligne de commande dans Vim, on part du mode normal et on appuie sur la touche `:`. Un curseur apparaît alors en bas à gauche de l'écran : c'est là qu'on tape notre copmmande.

#### Sauvegarde et chargement de fichiers

Pour sauvegarder les modifications apporées à un fichier, on tape `:w` puis `Enter`. Il est également possible de modifier le nom du fichier lors de l'enregistrement. Il suffit de taper `:w nom_du_fichier` et d'appuyer sur `Enter`.

#### Recherche et remplacement

Pour rechercher du texte dans le fichier, on utilise la commande  `:/mot_a_rechercher`.

Pour remplacer du texte dans le fichier, on utilise la commande `:%s/mot_a_remplacer/nouveau_mot/g`. Ici, `/g` (pour global) permet de changer toutes les occurences de `mot_a_remplacer`. Si on ne souhaite modifier que la première occurence, on ne rajoute pas `/g` en fin de commande. 

#### Autres commandes utiles

Pour quitter l'édireur de texte, on tape `:q`. Si des modifications ont été apportées au fichier et qu'on ne veut pas les conserver, on tape `:q!` pour forcer la sortie.

Il est possible de sauvegarder et quitter dans une même commande. Pour ce faire, on tape `:wq` ou `:x`, puis `Enter`.

#### Historique des commandes

On peut naviguer dans l'historique des commandes en utilisant les flèches du haut et du bas.


## Personnalisation

Vim offre la possibilité de configurer presque tous les aspects de leur expérience d'édition, en utilisant des fichiers de configuration appelés `.vimrc`. Il existe également des plugins comme **Sublivim** qui sont très simples à installer et qui améliorent beaucoup l'expérience. Cependant, les examens n'ont pas lieu sur nos sessions personnelles. On ne retrouve donc pas les plugins installés. Vim étant par défaut un peu brut de décoffrage, il est très pratique de savoir comment personnaliser l'éditeur via le fichier `.vimrc`. Voici quelques paramètrees incontournables :

* `syntax on` pour activer la syntaxe en couleur
* `set mouse=a` pour pouvoir cliquer dans le document et ne pas avoir à se déplacer avec les flèches
* `set number`pour afficher les numéros de ligne
* `set autoindent` pour activer l'indentation automatique

Pour ouvrir et édituer le fichier `.vimrc`, on tape dans un terminal `vim ~/.vimrc`. 
