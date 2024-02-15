---
---
# Nombre de Bell

Les nombres de Bell constituent l'une des suites importantes dans le domaine du dénombrement. *Qu'est-ce que compte le nombre de Bell ?* Considérons $n$ élèves dans une classe. Imaginons que nous les numérotions (par exemple, par ordre alphabétique des prénoms et des noms) et que nous souhaitions les organiser d'une certaine manière. Par exemple, nous pourrions décider de définir des classements ou des ordres parmi tous les élèves. Cela revient alors à sélectionner un arrangement parmi $n$ numéros. Il est facile de voir qu'il y a $n!$ façons de classer nos élèves. Mais imaginons maintenant que nous voulions les regrouper. Combien de façons différentes pouvons-nous imaginer pour les organiser en groupes ? C'est ce que compte un nombre de Bell !

Ajoutons un peu de formalisme à cette définition. Nous comptons précisément le nombre de partitions possibles de l'ensemble $\{1,...,n\}$. C'est une donnée intéressante dans des domaines tels que la théorie des probabilités. De plus, il existe une bijection entre les partitions de $\{1,...,n\}$ et les relations d'équivalence que l'on peut définir. En effet, en considérant une partition $P_1,...,P_r$ de l'ensemble $\mathcal{R}$, nous pouvons définir la relation d'équivalence suivante :

$$
i \mathcal{R} j \Longleftrightarrow \exists k \in \{1,...,r\}, i \in P_k \text{ et } j \in P_k.
$$

Cela signifie que $i$ et $j$ sont en relation s'ils appartiennent à la même partition. Ainsi, les nombres de Bell dénombrent également le nombre de relations d'équivalence que l'on peut définir sur un ensemble de $n$ éléments.

## Préliminaire sur les séries génératrices exponentielles

### Séries génératrices exponentielles

Soit $(a_n)_n$ une suite de complexes. On définit la série génératrice exponentielle (sous réserve d'existence) de $(a_n)$ par :

$$
A(x) = \sum_{n\ge 0} a_n \frac{x^n}{n!}
$$

Cette définition ne révolutionne pas les conceptions sur les séries entières ; elle consiste simplement à considérer une classe plus spécifique qui permet de simplifier certains raisonnements et qui intervient dans de nombreux problèmes de dénombrement via les séries entières.

### Exercice : Facile

Montrer que si $(a_n)_n$ et $(b_n)_n$ sont des suites telles que les séries exponentielles associées convergent absolument, alors :

$$
A(x)B(x) = \sum_{n\ge 0}\sum_{k=0}^n \binom{n}{k}b_k a_{n-k} x^n.
$$

Dans la suite, nous noterons généralement la série génératrice exponentielle d'une suite $(a_n)$ par $A$, et donc celle de $(b_n)$ par $B$, etc.

## Relation de récurrence

Pour rappel, nous définissons $B_n$ comme le nombre de partitions possibles pour un ensemble de $n$ éléments. Nous adoptons la convention $B_0 = 1$ uniquement.

### Exercice : Difficile

Montrer la relation suivante :

$$
\forall n \ge 2,\; B_{n+1} = \sum_{k=1}^n\binom{n}{k}B_k 
$$

**Corrigé :** L'idée est de considérer, par exemple, une partition. Il en existe au moins une. Cette partition peut comporter $n-k$ éléments, pour autant que $1 \le n-k \le n$. Nous fixons alors $k$. Ensuite, nous devons choisir les $k$ éléments qui seront dans cette classe, ce qui donne $\binom{n}{n-k}$ choix possibles. Finalement, nous complétons le reste, pour lequel il y a $B_k$ choix possibles, car cela revient à dénombrer toutes les partitions d'un ensemble à $k$ éléments. En réunissant tous ces éléments :

$$
\forall n \ge 2,\; B_{n+1} = \sum_{k=1}^n\binom{n}{k}B_k 
$$

## Equation fonctionnelle

Considérons que nous travaillons dans le domaine de définition de $x \mapsto B(x)$ et $x \mapsto B'(x)$.

### Exercice : Moyen

Montrer que $B$ vérifie la relation suivante :

$$
B(x) = B'(x)e^x.
$$

En déduire une forme de $B(x)$.
