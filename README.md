# Introduction au C

<br/>

Le C est un langage de programmation créé dans les années 1970, connu pour sa performance et sa flexibilité. En tant que langage de bas niveau, il se situe près du matériel informatique, permettant un contrôle précis des ressources matérielles comme la mémoire et le processeur. Cela le rend idéal pour développer des systèmes d'exploitation, des logiciels et des applications embarquées. Sa simplicité et sa puissance en font un langage incontournable en informatique.

<br/>

## Les instructions

Un programme informatique est constitué d'une série d'instructions, c'est-à-dire de commandes données à l'ordinateur pour qu'il effectue des tâches spécifiques. En C, chaque instruction se termine par un point-virgule (;).

<br/>

## Les commentaires

Commencer une introduction au langage C en parlant des commentaires n'est pas très commun, mais ils seront utilisés tout au long de cette présentation. Il est donc important de savoir comment commenter son programme. Les commentaires sont utiles pour expliquer le code, et il est recommandé d'en utiliser régulièrement. Il existe plusieurs façons de commenter en C, mais je vais me concentrer sur la méthode la plus simple : les commentaires sur une seule ligne. Pour cela, on utilise le symbole `//` suivi du commentaire.

```C
// ceci est un commentaire sur une ligne complète
int age = 42; // ceci est un commenntaire en fin d'instruction
```

<br/>

## Les variables et les types de données

Les variables sont des conteneurs utilisés pour stocker des valeurs. En C, chaque variable doit être **déclarée** avec un **type** spécifique avant de pouvoir être utilisée. Une fois déclarée, une variable peut être **initialisée**, c'est-à-dire qu'on lui attribue une valeur. Il est possible de déclarer et d'initialiser une variable dans une même instruction.

```C
int age; // déclaration d'une variable de type int (entier) qu'on appelle age
age = 42; // initialisation de la variable age
int number = 7; // déclaration et initialisation d'une variable de type int qu'on appelle number
```

### I. Les types de données de base

Dans le langage C, les variables peuvent stocker différents types de données, tels que des nombres entiers, des nombres à virgule flottante et des caractères. Ces types de données de base déterminent la nature et la taille des valeurs que les variables peuvent contenir. Ils sont essentiels pour décrire et manipuler les informations dans un programme. Voici quelques-uns des types de données de base les plus couramment utilisés en C :

* les int servent à enregistrer des entiers : `int age = 42;`
* les float servent à enregistrer des nombres décimaux : `float temperature = 36.5;`
* les double servent à enregistrer des nombres décimaux avec une plus grand précision qu'un float : `double pi = 3.1415926535;`
* les char servent à enregistrer des caractères individuels : `char letter = 'A';`

###  II. Les tableaux

Les tableaux sont des collections de variables du même type qui sont stockées en mémoire de manière contigüe et sous un même nom. ils permettent donc de gérer et de manipuler efficacement des ensembles de données. Chaque élément d'un tableau est accessible via un indice, le premier élément ayant l'indice 0.

Pour déclarer un tableau en C, on doit spécifier le type des éléments suivis du nom du tableau et du nombre d'éléments qu'il peut contenir :
```C
int numbers[5]; // déclaration d'un tableau de 5 entiers
```

Comme pour n'importe quelle variable, un tableau peut être initialisé au moment de la déclaration. Pour ce faire, on fournit l'ensemble des éléments entre accolades, séparés par des virgules :
```C
int numbers[3] = {1, 2, 3};
```

On accède ensuite aux éléments du tableau en spécifiant l'indice désiré entre crochets :
```C
int firstNumber = numbers[0]; // on enregistre la valeur du premier élément du tableau numbers dans une variable firstNumber
numbers[1] = 100; // on modifie la valeur du deuxième élément du tableau
```

Les tableaux sont particulièrement utiles pour travailler avec des séries de valeurs ou des collections de données, facilitant ainsi les opérations répétitives et les manipulations de grands ensembles de données.

<br/>

## Les fonctions

Les fonctions sont des blocs de code réutilisables qui effectuent une tâche spécifique. Elles permettent de structurer un programme en le découpant en sous-programmes plus petits et plus faciles à gérer. Les fonctions peuvent prendre des arguments en entrée et renvoyer une valeur en sortie.

### Déclaration et définition d'une fonction

Une fonction en C est **déclarée** avec un type de retour, un nom et une liste de paramètres. Par exemple, voici comment déclarer une fonction qui additionne deux entiers :
```C
int addition(int a, int b);
```

La **définition** de la fonction fournit le corps de la fonction, où les opérations sont effectuées :
```C
int addition(int a, int b)
{
    return (a + b);
}
```

Dans cette exemple, la fonction *addition* prend deux entiers *a* et *b* en paramètres et retourne également un entier, résultat de la somme de *a* et de *b.

### Appel d'une fonction

Une fois qu'une fonction est déclarée et définie, on peut l'appeler dans notre programme en utilisant son nom et en fournissant les arguments nécessaires :
```C
int result = addition(5, 3);
```
Dans cet exemple, on déclare une variable de type int qui va stocker le résultat de l'appel à la fonction addition. 

### Cas particuliers

Les fonctions peuvent aussi ne pas prendre de paramètres ou ne pas renvoyer de valeur. Voici un exemple de fonction qui affiche un message à l'écran :
```C
void printMessage()
{
    printf("Hello World!\n");
}
```
Ici, le mot clé *void* signigie que la fonction ne retourne aucune valeur. L'appel à cette fonction est fait de cette façon : 
```C
printMessage();
```






Tout programme en C a une fonction appelée main. C'est elle qui est appelée au lancement du programme. La fonction main retournera toujours un int,
```C
int main()
{
  return (0);
}

*** Exemples 

```C
int addition(int a, int b)
{
  return (a + b);
};
```

