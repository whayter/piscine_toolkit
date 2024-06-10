# Introduction au C

Voilà une bonne base pour écrire son premier programme en C. 

## Les instructions

Un programme informatique est constitué d'une série d'instructions, c'est-à-dire des commandes données à l'ordinateur pour qu'il effectue une tâche spécifique. En C, les instructions se terminent par un point-virgule (;). 

---

## Les commentaires

Il n'est pas très commun de commencer la présentation du langage C en parlant des commentaires, mais je vais m'en servir tout au long de cette présentation. il est donc possible de commenter son programme, sur une ligne complète ou à la suite directe d'une instruction. Pour ce faire, il suffit d'insérer le symbole `//` suivit de son commentaire. 

```C
// ceci est un commentaire sur une ligne complète
int age = 42; // ceci est un commenntaire en fin d'instruction
```

---

## Les variables et les types de données

Les variables sont des conteneurs pour stocker des valeurs. En C, chaque variable doit être déclarée avec un type spécifique avant de pouvoir être utilisée. Une fois déclarée, une variable peut être instanciée, c'est-à-dire qu'on lui donne une valeur. On peut déclarer et instancier une variable dans une même instruction.

```C
int age; // déclaration d'une variable de type int (entier) qu'on appelle age
age = 42; // instanciation de la variable age
int number = 7; // déclaration et instanciation d'une variable de type int qu'on appelle number

```

I. Les types de données de base

* les int servent à enregistrer des entiers : `int age = 42;`
* les float servent à enregistrer des nombres décimaux : `float temperature = 36.5;`
* les double servent à enregistrer des nombres décimaux avec une plus grand précision qu'avec un float : `double pi = 3.1415926535;`
* les char servent à enregistrer des caractères individuels : `char letter = 'A';`

II. Les tableaux

Les tableaux sont des collections de variables du même type, stockées sous un même nom et accessibles par des indices.

---

## Les fonctions

Les fonctions sont des blocs de code réutilisables qui effectuent une tâche spécifique. Elles permettent de structurer un programme en le découpant en sous-programmes plus petits et plus faciles à gérer. Une fonction prend éventuellement des paramètres en entrée, exécute une série d'instructions, et peut retourner une valeur.





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

