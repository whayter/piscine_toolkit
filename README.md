# Introduction au C

Le C est un langage de programmation créé dans les années 1970, connu pour sa performance et sa flexibilité. Il permet un contrôle précis des ressources matérielles et est utilisé pour développer des systèmes d'exploitation, des logiciels et des applications embarquées. Sa simplicité et sa puissance en font un langage incontournable en informatique.

## Les instructions

Un programme informatique est constitué d'une série d'instructions, c'est-à-dire de commandes données à l'ordinateur pour qu'il effectue des tâches spécifiques. En C, chaque instruction se termine par un point-virgule (;).

---

## Les commentaires

Commencer une introduction au langage C en parlant des commentaires n'est pas très commun, mais ils seront utilisés tout au long de cette présentation. Il est donc important de savoir comment commenter son programme. Les commentaires sont utiles pour expliquer le code, et il est recommandé d'en utiliser régulièrement. Il existe plusieurs façons de commenter en C, mais je vais me concentrer sur la méthode la plus simple : les commentaires sur une seule ligne. Pour cela, on utilise le symbole `//` suivi du commentaire.

```C
// ceci est un commentaire sur une ligne complète
int age = 42; // ceci est un commenntaire en fin d'instruction
```

---

## Les variables et les types de données

Les variables sont des conteneurs utilisés pour stocker des valeurs. En C, chaque variable doit être déclarée avec un type spécifique avant de pouvoir être utilisée. Une fois déclarée, une variable peut être initialisée, c'est-à-dire qu'on lui attribue une valeur. Il est possible de déclarer et d'initialiser une variable dans une même instruction.

```C
int age; // déclaration d'une variable de type int (entier) qu'on appelle age
age = 42; // initialisation de la variable age
int number = 7; // déclaration et initialisation d'une variable de type int qu'on appelle number

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

