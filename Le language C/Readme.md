# Introduction au langage C

Le C est un langage de programmation créé dans les années 1970, connu pour sa performance et sa flexibilité. En tant que langage de bas niveau, il se situe près du matériel informatique, permettant un contrôle précis des ressources matérielles comme la mémoire et le processeur. Cela le rend idéal pour développer des systèmes d'exploitation, des logiciels et des applications embarquées. Sa simplicité et sa puissance en font un langage incontournable en informatique.

Le langage C est un langage de programmation compilé, ce qui signifie que le code source écrit par le programmeur doit être transformé en un code machine exécutable par l'ordinateur avant de pouvoir être exécuté. Ce processus de transformation est appelé compilation.

parler des macros et des commandes de préprocesseur


Parler des accolades, dans quel cas on peut s'en passer. 


## I. Les instructions

Un programme informatique est constitué d'une série d'instructions, c'est-à-dire de commandes données à l'ordinateur pour qu'il effectue des tâches spécifiques. En C, chaque instruction se termine par un point-virgule : `int number = 10;`.


## II. Les commentaires

Dans un programme, les commentaires apportent de très précieuses informations pour ceux qui sont amenées à manipuler le code. Les commentaires sont ignorés lors de l'éxecution du programme. Il existe plusieurs façons de commenter en C, mais pour rester simple, je ne parlerai que des commentaires sur une seule ligne. Pour cela, on utilise le symbole `//` suivi du commentaire :
```C
// ceci est un commentaire sur une ligne complète
int age = 42; // ceci est un commenntaire en fin d'instruction
```

## III. Les variables et les types de données

Les variables sont des conteneurs utilisés pour stocker des valeurs. En C, chaque variable doit être **déclarée** avec un **type** spécifique avant de pouvoir être utilisée. Une fois déclarée, une variable peut être **initialisée**, c'est-à-dire qu'on lui attribue une valeur. Il est possible de déclarer et d'initialiser une variable dans une même instruction.
```C
int age; // déclaration d'une variable de type int (entier) qu'on appelle age
age = 42; // initialisation de la variable age
int number = 7; // déclaration et initialisation d'une variable dans une même instruction
```

### A. Les types de données de base

Dans le langage C, les variables peuvent stocker différents types de données, tels que des nombres entiers, des nombres à virgule flottante et des caractères. Ces types de données de base déterminent la nature et la taille des valeurs que les variables peuvent contenir. Ils sont essentiels pour décrire et manipuler les informations dans un programme. Voici quelques-uns des types de données de base les plus couramment utilisés :

* les int servent à enregistrer des entiers : `int age = 42;`
* les float servent à enregistrer des nombres décimaux : `float temperature = 36.5;`
* les double servent à enregistrer des nombres décimaux avec une plus grand précision qu'un float : `double pi = 3.1415926535;`
* les char servent à enregistrer des caractères individuels : `char letter = 'A';`

###  B. Les tableaux

Les tableaux sont des collections de variables du même type qui sont stockées en mémoire de manière contigüe et sous un même nom. Ils sont particulièrement utiles pour travailler avec des séries de valeurs ou des collections de données, facilitant ainsi les opérations répétitives et les manipulations de grands ensembles de données.

#### 1. Déclaration :
Pour déclarer un tableau en C, on doit spécifier le type des éléments suivis du nom du tableau et du nombre d'éléments qu'il peut contenir :
```C
int numbers[5]; // déclaration d'un tableau de 5 entiers
```

#### 2. Initialisation :
Comme pour n'importe quelle variable, un tableau peut être initialisé au moment de la déclaration. Pour ce faire, on fournit l'ensemble des éléments entre accolades, séparés par des virgules :
```C
int numbers[3] = {1, 2, 3};
```
Dans ce cas, on peut laisser le compilateur déterminer la taille du tableau à partir de la liste des éléments fournie : 
```C
int numbers[] = {1, 2, 3};
```

#### 3. Accès aux éléments :
Chaque élément d'un tableau est accessible via un indice, le premier élément ayant l'indice 0. On accède donc aux éléments du tableau en spécifiant l'indice désiré entre crochets :
```C
int firstNumber = numbers[0]; // on enregistre la valeur du premier élément du tableau numbers dans une variable firstNumber
numbers[1] = 100; // on modifie la valeur du deuxième élément du tableau
```

### C. Les pointeurs

Lorsqu'une variable est déclarée, un espace en mémoire est reservé pour enregistrer sa valeur. Cet espace possède une adresse. Les pointeurs sont des variables qui permettent d'enregistrer des adresses mémoire.

#### 1. Déclaration :
Pour déclarer un pointeur en C, on utilise le type de données que le pointeur désigne, suivi de l'opérateur `*`. Par exemple, si le pointeur pointe vers un espace mémoire contenant une variable de type int, on parlera d'un "pointeur sur int" :
```C
int *ptr; // déclaration d'un pointeur sur int qu'on appelle ptr
```

#### 2. Initialisation :
En langage C, le symbole `&`, appelé **opérateur d'adresse**, est utilisé pour obtenir l'adresse mémoire d'une variable. Lorsqu'il est placé devant une variable, il renvoie l'adresse mémoire où cette variable est stockée. Pour initialiser notre pointeur sur int `ptr`, on va donc utiliser cet opérateur pour récupérer l'adresse mémoire d'un int : 
```C
int number = 42;
int *ptr = &number;
```

#### 3. Déréférencement :
Pour accéder à la valeur pointée par un pointeur, on utilise l'**opérateur de déréférencement** `*`. Par exemple, pour accéder à la valeur de number via ptr :
```C
int value = *ptr; // value vaudra alors 42
```

#### 4. Pointeurs et tableaux :
Lorsqu'on déclare un tableau en C, la variable déclarée est en fait un pointeur vers le premier élément du tableau :
```C
int numbers[3] = {1, 2, 3};
int *ptr = numbers; // pas besoin de l'opérateur d'adresse ici, puisque numbers est considéré commme un pointeur vers le premier élément du tableau
```
Si on déréférence `ptr`, on obtiendra donc la valeur du premier élément de notre tableau, c'est à dire 1 :
```C
int firstValue = *ptr; // firstValue vaudra alors 1
```

#### 5. Arithmétique des pointeurs :
On peut effectuer des opérations arithmétiques sur les pointeurs pour parcourir les éléments d'un tableau :
```C
ptr = ptr + 1; // en incrémentant ptr, on déplace le curseur d'un cran, *ptr vaut alors 2
ptr++; // ceci est une autre façon d'incrémenter un pointeur. *ptr vaut alors 3
```

#### 6. Pointeur nul :
En C, on peut assigner à un pointeur la valeur `NULL` pour signifier qu'il ne pointe vers aucune adresse valide :
```C
int *ptr = NULL;
```

#### 7. Les pointeurs de pointeur :
Puisqu'un pointeur n'est qu'une variable contenant une adresse mémoire, on peut avoir un pointeur faisant référence à un autre pointeur :
```C
int number = 42;
int *ptr1 = &number;
int **ptr2 = &ptr1; // ptr2 pointe vers ptr1
```
Voici un tableau illustrant la façon dont tout ça est enregistré en mémoire :
| **Addresse  en  mémoire** | **Nom  de la  variable** | **Valeur  contenue** |
|:-------------------------:|:------------------------:|:--------------------:|
|            0x00           |          number          |          42          |
|            0x01           |           ptr1           |         0x00         |
|            0x02           |           ptr2           |         0x01         |

La variable `number` contient `42` et est enregistrée à l'adresse `0x00`. La variable `ptr1` est enregistrée à l'adresse `0x01` et contient l'adresse de la variable `number`, c'est à dire `0x00`. La variable `ptr2` est enregistrée à l'adresse `0x02`, et contient l'adresse de `ptr1`, c'est à dire `0x01`.
Si on déréférence `ptr2`, on obtient `ptr1`. Si on déréférence deux fois `ptr2`, on obtiendra `number` :
```C
int value = **ptr2; // value vaudra 42
```


## IV. Les opérateurs

### 1. Les opérateurs arithmétiques :
On utilise en C les opérateurs arithmétiques classiques (`+`, `-`, `*`, `/`) auxquelles il faut ajouter le *modulo* (`%`) qui sert à calculer le reste d'une division.

### 2. Les opérateurs de comparaison :
On utilise en C les opérateurs de comparaison classiques (`<`, `<=`, `>`, `>=`). Pour vérifier une égalité, on utilise l'opétateur `==`, à ne pas confondre avec `=`qui sert à assigner une valeur. On utilise aussi `!=` pour vérifier une inégalité.

### 3. Les opérateurs logiques :
* `&&` : l'opérateur ET
* `||` : l'opérateur OU
* `!` : l'opérateur de négation

### 4. Les opérateurs d'affectation :
Outre le traditionnel `=` pour affecter, on utilise aussi les opérateurs `+=` et `-=` qui s'utilisent de cette façon :
```C
int a = 10;
a -= 2;        // cette instruction peut aussi s'écrire "a = a - 2;". a vaut maintenant 8
a += 5;        // cette instruction peut aussi s'écrire "a = a + 5;". a vaut maintenant 13
```

### 5. Les opérateurs d'incrémentation et de décrémentation :
On utilise les opérateurs `++` et `--` pour incrémenter ou décrémenter une valeur.
```C
int a = 10;
a++; // a vaut maintenant 11
a--; // a vaut à nouveau 10
```
Ces opérateurs peuvent aussi être placés devant la variable. L'ordre a son importance, comme le montre cet exemple : 
```C
int a = 10;
int result1 = a++; // result1 prend la valeur de a puis est incrémenté
int result2 = ++a; // a est incrémenté puis result2 prend la valeur de a
```


## V. Les conditions

Les conditions en C permettent de contrôler le flux d'exécution du programme en fonction de l'évaluation d'expressions booléennes (vrai ou faux). La structure conditionnelle la plus couramment utilisée est `if`, qui exécute un bloc de code si une condition donnée est vraie. Il est souvent accompagné de `else` pour spécifier un bloc de code alternatif à exécuter si la condition est fausse. Une autre variante, `else if`, permet de vérifier plusieurs conditions en séquence.

```C
int number = 0;

if (number < 0)
{
    // code à éxécuter si number est négatif
}
else if (number > 0)
{
    // code à éxécuter si number est positif
}
else
{
    // code à éxécuter si number vaut 0
}
```


## VI. Les boucles

Les boucles sont des mécanismes qui permettent de répéter une série d'instructions plusieurs fois. C'est une fonctionnalité essentielle pour effectuer des tâches répétitives de manière efficace. Il existe différents types de boucles, mais seule la boucle `while` est autorisée pendant la piscine, et on va donc se concentrer sur celle-ci.

#### 1. La boucle while :
La boucle `while` exécute un bloc d'instructions tant qu'une condition spécifiée est vraie. La condition est vérifiée avant chaque exécution du bloc. Si la condition est fausse dès le début, le bloc d'instructions ne sera jamais exécuté :
```C
while (condition)
{
    //code à éxécuter
}
```

#### 2. La commande break :
La commande `break` permet de sortir immédiatement de la boucle, même si la condition est encore vraie :
```C
int i = 0;
while (i < 5)
{
    if (i == 3)
    {
        break;
    }
    i++;
}
```
Dans cet exemple, la boucle `while` s'exécute jusqu'à ce que `i` soit égal à 3, moment où la commande `break` est exécutée pour sortir de la boucle.

#### 3. La commande continue :
La commande `continue` permet de passer directement à l'itération suivante de la boucle, en sautant les instructions restantes dans le bloc de la boucle pour l'itération en cours :
```C
int i = 0;
while (i < 5)
{
    i++;

    if (i == 3)
    {
        continue;
    }
    // code à éxéctuer
}
```
Dans cet exemple, lorsque `i` vaut 3, la commande `continue` est exécutée et le reste des instructions dans la boucle est ignoré pour cette itération.


## VII. Les fonctions

Les fonctions sont des blocs de code réutilisables qui permettent de diviser un programme en segments plus petits et plus faciles à gérer. Elles facilitent la compréhension, la maintenance et la réutilisation du code.

### A. Définition et déclaration des fonctions

Une fonction en C se compose d'un type de retour, d'un nom de fonction et d'une liste de paramètres. La définition de la fonction inclut le corps de la fonction, c'est-à-dire le code à exécuter lorsque la fonction est appelée :
```C
type_de_retour nom_de_fonction(paramètres)
{
    // Corps de la fonction
}
```

Voilà un exemple simple : 
```C
int addition(int a, int b)
{
    return (a + b);
}
```
Dans cette exemple, la fonction *addition* prend deux entiers `a` et `b` en paramètres et retourne un entier, résultat de la somme de `a` et de `b`.

Une fois qu'une fonction est déclarée et définit, on peut l'appeler dans notre programme : 
```C
int result = addition(2, 7); // result vaudra 9
```

Les fonctions peuvent aussi ne pas prendre de paramètres ou ne pas renvoyer de valeur. Voici un exemple de fonction qui affiche un message à l'écran :
```C
void printMessage()
{
    printf("Hello World!\n");
}
```
Ici, le mot clé `void` signigie que la fonction ne retourne aucune valeur. L'appel à cette fonction est fait de cette façon : `printMessage();`


### B. La fonction *main*

En C, la fonction *main* est le point d'entrée de tout programme. Elle est la première à être exécutée et doit systématiquement être présente. Essentielle, elle dirige l'exécution globale. La fonction *main* peut être déclarée de plusieurs façons, mais les deux formes les plus courantes sont les suivantes :

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
Dans ce deuxième cas, l'argument `argv` est un tableau de pointeur sur char, c'est à dire un tableau de chaînes de caractères. L'arguement `argc` donne la taille de `argv`. De cette façon, on peut donner un nombre variable d'arguments à l'execution de notre programme. 

Dans tous les cas, la fonction *main* retourne un entier. Le type de retour int indique le code de sortie du programme. Par convention, un retour de 0 signifie que le programme s'est terminé avec succès.

#### C. Portée des variables

La portée d'une variable détermine où elle peut être utilisée dans le programme. Il existe deux types de portée :
* portée locale : les variables déclarées à l'intérieur d'une fonction sont locales à cette fonction et ne peuvent pas être utilisées en dehors de celle-ci.
* portée globale : les variables déclarées en dehors de toutes les fonctions sont globales et peuvent être utilisées par toutes les fonctions du programme.

**À noter** : une variable déclarée dans un bloc d'instruction est local à ce bloc. Par exemple, une variable déclarée dans une boucle `while` n'existe pas hors de la boucle.  


### VIII. Les bibliothèques en C

Les bibliothèques (ou *librairies*) en C sont des collections de fonctions et de macros pré-compilées qu'on peut utiliser dans nos programmes. Elles permettent de réutiliser du code sans avoir à le réécrire, ce qui facilite la maintenance et la modularité des programmes.

Voici quelques bibliothèques très utilisées :
* `stdio.h` : contient notamment la fonction `printf()`
* `stdlib.h` : contient notamment les fonctions `malloc`, `free`


### IX. La compilation

Le langage C est un langage de programmation compilé, ce qui signifie que le code source écrit par le programmeur doit être transformé en un code machine exécutable par l'ordinateur avant de pouvoir être exécuté. Ce processus de transformation est appelé compilation.

Il existe différents compilateurs, mais on va se concentrer sur `gcc`. 


