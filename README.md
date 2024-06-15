# Introduction au C

Le C est un langage de programmation créé dans les années 1970, connu pour sa performance et sa flexibilité. En tant que langage de bas niveau, il se situe près du matériel informatique, permettant un contrôle précis des ressources matérielles comme la mémoire et le processeur. Cela le rend idéal pour développer des systèmes d'exploitation, des logiciels et des applications embarquées. Sa simplicité et sa puissance en font un langage incontournable en informatique.


## Les instructions

Un programme informatique est constitué d'une série d'instructions, c'est-à-dire de commandes données à l'ordinateur pour qu'il effectue des tâches spécifiques. En C, chaque instruction se termine par un point-virgule.

par exemple
```C
int number = 10; // déclaration d'un entier. Cette variable est enregistrée quelque part dans la mémoire de l'ordinateur. Cet espace en mémoire a une adresse. Sans elle, on ne serait pas capable de retrouver l'emplacement où la valeur a été enregistrée. 
```


## Les commentaires

Commencer une introduction au langage C en parlant des commentaires n'est pas très commun, mais je vais les utiliser tout au long de cette présentation. Il est donc important de savoir comment commenter son programme. Les commentaires sont utiles pour expliquer le code, et il est recommandé d'en utiliser régulièrement. Il existe plusieurs façons de commenter en C, mais je vais me concentrer sur la méthode la plus simple : les commentaires sur une seule ligne. Pour cela, on utilise le symbole `//` suivi du commentaire :

```C
// ceci est un commentaire sur une ligne complète
int age = 42; // ceci est un commenntaire en fin d'instruction
```


## Les variables et les types de données

Les variables sont des conteneurs utilisés pour stocker des valeurs. En C, chaque variable doit être **déclarée** avec un **type** spécifique avant de pouvoir être utilisée. Une fois déclarée, une variable peut être **initialisée**, c'est-à-dire qu'on lui attribue une valeur. Il est possible de déclarer et d'initialiser une variable dans une même instruction.

```C
int age; // déclaration d'une variable de type int (entier) qu'on appelle age
age = 42; // initialisation de la variable age
int number = 7; // déclaration et initialisation d'une variable dans une même instruction
```

### I. Les types de données de base

Dans le langage C, les variables peuvent stocker différents types de données, tels que des nombres entiers, des nombres à virgule flottante et des caractères. Ces types de données de base déterminent la nature et la taille des valeurs que les variables peuvent contenir. Ils sont essentiels pour décrire et manipuler les informations dans un programme. Voici quelques-uns des types de données de base les plus couramment utilisés :

* les int servent à enregistrer des entiers : `int age = 42;`
* les float servent à enregistrer des nombres décimaux : `float temperature = 36.5;`
* les double servent à enregistrer des nombres décimaux avec une plus grand précision qu'un float : `double pi = 3.1415926535;`
* les char servent à enregistrer des caractères individuels : `char letter = 'A';`

###  II. Les tableaux

Les tableaux sont des collections de variables du même type qui sont stockées en mémoire de manière contigüe et sous un même nom. Ils sont particulièrement utiles pour travailler avec des séries de valeurs ou des collections de données, facilitant ainsi les opérations répétitives et les manipulations de grands ensembles de données.

#### Déclaration

Pour déclarer un tableau en C, on doit spécifier le type des éléments suivis du nom du tableau et du nombre d'éléments qu'il peut contenir :
```C
int numbers[5]; // déclaration d'un tableau de 5 entiers
```

#### Initialisation

Comme pour n'importe quelle variable, un tableau peut être initialisé au moment de la déclaration. Pour ce faire, on fournit l'ensemble des éléments entre accolades, séparés par des virgules :
```C
int numbers[3] = {1, 2, 3};
```
Dans ce cas, on peut laisser le compilateur déterminer la taille du tableau à partir de la liste des éléments fournie : 
```C
int numbers[] = {1, 2, 3};
```

#### Accès aux éléments

Chaque élément d'un tableau est accessible via un indice, le premier élément ayant l'indice 0. On accède donc aux éléments du tableau en spécifiant l'indice désiré entre crochets :
```C
int firstNumber = numbers[0]; // on enregistre la valeur du premier élément du tableau numbers dans une variable firstNumber
numbers[1] = 100; // on modifie la valeur du deuxième élément du tableau
```

### III. Les pointeurs

Lorsqu'une variable est déclarée, un espace en mémoire est reservé pour enregistrer sa valeur. Cet espace possède une adresse. Les pointeurs sont des variables qui permettent d'enregistrer des adresses mémoire.

#### Déclaration

Pour déclarer un pointeur en C, on utilise le type de données auquel le pointeur va pointer, suivi de l'opérateur `*`. Si le pointeur pointe vers une variable de type int, on parlera alors d'un "pointeur sur int". 
```C
int* ptr; // déclaration d'un pointeur sur int qu'on appelle ptr
```

#### Initialisation

Puisqu'un pointeur enregistre une adresse, on ne peut pas l'initialiser ainsi :

```C
int number = 42;
int* ptr = &number;
```
Dans cet exemple, on utilise l'opérateur `&` qui sert à **déréférencer** une variable. `number` vaut 42, mais `&number` vaut l'adresse mémoire qui contient la variable `number`.


Pour récupérer la valeur contenue à une adresse, on utilise l'**opérateur de déréférencement** `*` :
```C
int number = 42;
int* ptr = &number;
int ptrValue = *ptr;
```

Les pointeurs peuvent se cululer :
```C

int*** ptr;

Dans ce cas, ptr a pour valeur l'adresse de *ptr. *ptr a pour valeur l'adresse de **ptr. **ptr a pour valeur l'adresse de ***ptr

int number = 42;
int* ptr1 = &number;
int** ptr2 = &ptr1;
```

|: Addresse en mémoire   |: 0x00   :|: 0x01 :|: 0x02 :|: 0x03 :|: 0x04 :|: 0x05 :|
|: Nom de la variable    |: number :|:      :|: ptr1 :|:      :|:      :|: ptr2 :|
|: Valeur contenue       |: 42     :|:      :|: 0x00 :|:      :|:      :|: 0x02 :|



Un pointeur est une variable qui enregistre une addresse en mémoire. Elle aura deux types de valeurs possibles :
* NULL si la variable ne pointe vers aucune zone mémoire occupée
* une addresse valide sinon

Une adresse est un entier représenté en hexadécimal et préfixé de `0x`. Exemple : `0x1abe13ff`.








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

Dans cette exemple, la fonction *addition* prend deux entiers *a* et *b* en paramètres et retourne également un entier, résultat de la somme de *a* et de *b*.

### Appel d'une fonction

Une fois qu'une fonction est déclarée et définie, on peut l'appeler dans notre programme en utilisant son nom et en fournissant les arguments nécessaires :
```C
int result = addition(5, 3);
```
Dans cet exemple, on déclare une variable de type int qui va stocker le résultat de l'appel à la fonction addition. 

### Les fonctions sans paramètres et / ou sans retour

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

### La focntion *main*

En C, la fonction main est le point d'entrée de tout programme. Elle est la première à être exécutée et doit systématiquement être présente. Essentielle, elle dirige l'exécution globale. La fonction *main* peut être déclarée de plusieurs façons, mais les deux formes les plus courantes sont les suivantes :

1. sans arguments :

```C
int main(void)
{
    // code à exécuter
    return (0);
}
```

2. avec arguments :

```C
int main(int argc, char *argv[])
{
    // code à exécuter
    return (0);
}
```

La fonction *main* retourne généralement un entier. Le type de retour int indique le code de sortie du programme. Par convention, un retour de 0 signifie que le programme s'est terminé avec succès.


### Les appels systèmes / les librairies


