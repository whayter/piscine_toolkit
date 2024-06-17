# Vim

Vim est un **éditeur de texte** particulièrement apprécié pour sa puissance et sa flexibilité. Il est connu pour sa rapidité, sa capacité à gérer de très gros fichiers de manière efficace, et sa configuration hautement personnalisable.

## Les modes

Vim est un **éditeur modal**, c'est à dire qu'il possède différents modes pour réliser des tâches variées. Il y a trois modes de base : le mode normal ou mode commande (dans lequel on est lorsque Vim démarre), le mode insertion, et le mode ligne de commande.

### 1. Le mode normal (commande)

C'est le mode par défaut lorsque Vim est lancé. Il permet de copier des lignes ou de les déplacer grâce à des raccourcis, de mettre du texte en forme, ou de se déplacer dans le fichier.

### 2. Le mode insertion

Le mode insertion permet d'entrer et de modifier du texte dans un document. Contrairement au mode normal, où les touches ont des fonctions spécifiques de navigation et de commande, le mode insertion ressemble davantage à l'expérience d'édition de la plupart des autres éditeurs de texte.

Pour passer du mode normal au mode insertion, on utilise la touche `i` (pour insérer). Les touches du clavier agissent alors comme dans n'importe quel autre éditeur de texte. On peut taper du texte, supprimer des caractères, et utiliser les flèches pour déplacer le curseur.

Pour quitter le mode insertion, on appuie sur la touche `esc`. 

### 3. Le mode ligne de commande

Pour accéder au mode ligne de commande dans Vim, on part du mode normal et on appuie sur la touche `:`. Un curseur apparaît alors en bas de l'écran, à gauche, où on peut taper nos commandes.

#### Sauvegarde et chargement de fichiers

Taper `:w` et appuyer sur `Enter`.
Pour enregistrer le ficheir sous un autre nom, taper `:w nom_du_fichier` et appuyer sur `Enter`.

#### Recherche et remplacement

Pour rechercher du texte dans le fichier, on utilise la commande  `:/mot_a_rechercher`.
Pour remplacer du texte dans le fichier, on utilise la commande `:%s/mot_a_remplacer/nouveau_mot/g`.

#### Autres commandes utiles

Pour quitter Vim, on tape `:q`. Si des modifications ont été apportées au fichier et qu'on ne veut pas les conserver, on tape `:q!` pour forcer la sortie.

Pour sauvegarder et quitter on tape `:wq` ou `:x`.

#### Historique des commandes

On peut naviguer dans l'historique des commandes en utilisant les flèches du haut et du bas.


## Personnalisation

Personnalisable : Vim permet aux utilisateurs de configurer presque tous les aspects de leur expérience d'édition, en utilisant des fichiers de configuration appelés `.vimrc`.






Extensibilité : Il existe des milliers de plugins Vim disponibles pour ajouter des fonctionnalités supplémentaires, ce qui en fait un outil extrêmement flexible.

Intégration avec le terminal : Vim s'intègre bien avec les terminaux et peut être utilisé de manière efficace sur des serveurs distants ou via des sessions SSH.

Vim et la communauté : Vim possède une communauté active qui partage des astuces, des plugins et des configurations, contribuant ainsi à son évolution continue.

Pourquoi utiliser Vim ?

Productivité accrue : Une fois maîtrisé, Vim permet une édition rapide et efficace du texte, ce qui peut considérablement augmenter la productivité.

Disponibilité : Vim est préinstallé sur la plupart des systèmes Unix/Linux, ce qui en fait un choix populaire pour les environnements de développement et d'administration système.

Apprentissage progressif : Bien que Vim ait une courbe d'apprentissage initiale raide en raison de sa modalité et de ses nombreuses commandes, les utilisateurs constatent souvent une amélioration rapide de leur flux de travail une fois les bases maîtrisées.

En résumé, Vim est un éditeur de texte puissant et très flexible, idéal pour ceux qui passent beaucoup de temps à manipuler du texte, écrire du code ou gérer des fichiers sur des systèmes Unix/Linux. Sa richesse en fonctionnalités et sa personnalisation en font un choix populaire parmi les développeurs expérimentés à la recherche d'un outil efficace et robuste pour leur travail quotidien.
