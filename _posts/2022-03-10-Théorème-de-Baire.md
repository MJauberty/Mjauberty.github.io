-----------
layout: post
title: Théorème de Baire et applications
-----------

Nous nous proposerons dans cet article de démontrer un théorème important de topologie.

Soit A un espace topologique. On dit que A est un espace de Baire s'il vérifie la propriété suivante :

          Toute réunion au plus dénombrable de d'ouverts denses dans A est dense dans A
 
**Le théorème de Baire** donne des conditions suffisantes pour qu'un espace topologique soit de Baire :

         1) Si A est localement compact, alors A est de Baire.
         
         2) Si A est un espace métrique complet, alors A est de Baire.
         
         3) Si X est un ouvert d'un espace de Baire A, alors X est de Baire pour la topologie induite.


**Démonstration :**

On ne fait pas tout de suite de d'hypothèse sur A.

On peut déjà remarquer que les résultats sont triviaux si la famille d'ouverts est finie.

Soit une famille $(A_i)_{i\in I}$ dénombrable d'ouverts denses de A non-vides.

Soit x un élément de A, il admet un voisinage $B_0$.

Désormais, on sait que $A_1$ est un dense dans A. On peut définir $\overline{B_1}(x_1,r_1)$ une boule fermée incluse $A_1\cap V$.

On peut par ailleurs, supposer $r_1<1$ sans problème.

On peut ensuite répéter le processus, on a un voisinage $B_1$ et $A_2$ est dense dans A donc on peut définir une nouvelle boule fermée $\overline{B_2}(x_2,r_2)$.

Où $r_2<\dfrac{1}{2}$ par exemple.

Par récurrence, on construit deux suites $(x_n)$ et $(r_n)$, et une famille de boules $B_n = B(x_n,r_n)$ telle que

$$\forall n\in\mathbb{N},   B_{n+1}\subset B_n \textbf{}$$
