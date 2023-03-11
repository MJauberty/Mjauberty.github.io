-----------
Théorème de Baire et applications
-----------

Nous nous proposerons dans cet article de démontrer un théorème important de topologie.

Soit A un espace topologique. On dit que A est un espace de Baire s'il vérifie la propriété suivante :

          Toute réunion au plus dénombrable de d'ouverts denses dans A est dense dans A
 
**Le théorème de Baire** donne des conditions suffisantes pour qu'un espace topologique soit de Baire :

         1) Si A est localement compact, alors A est de Baire.
         
         2) Si A est un espace métrique complet, alors A est de Baire.
         
         3) Si X est un ouvert d'un espace de Baire A, alors X est de Baire pour la topologie induite.


**Démonstration :**

Supposons que A soit un espace métrique complet. On peut déjà remarquer que les résultats sont triviaux si la famille d'ouverts est finie.

Soit une famille $(A_i)_{i\in I}$ dénombrable d'ouverts denses de A non-vides. Soit x un élément de A, il admet un voisinage $B_0 = B(x,\varepsilon)$.

Désormais, on sait que $A_1$ est un dense dans A. On peut définir $\overline{B_1}(x_1,r_1)$ une boule fermée incluse $A_1\cap B_0$. On peut par ailleurs, supposer $r_1<1$ sans problème.

On peut ensuite répéter le processus, on a un voisinage $B_1$ et $A_2$ est dense dans A donc on peut définir une nouvelle boule fermée $\overline{B_2}(x_2,r_2)$. Où $r_2<\dfrac{1}{2}$ par exemple.

Par récurrence, on construit deux suites $(x_n)$ et $(r_n)$, et une famille de boules $B_n = B(x_n,r_n)$ telle que

$$\forall n\in\mathbb{N},   B_{n+1}\subset B_n \textbf{    et    } r_n<\dfrac{1}{2^n}$$

On peut montrer $(x_n)$ est une suite de Cauchy de notre espace A. Autrement dit, elle converge vers un certain y dans A. Mais par la construction de $(B_n)$ et $(x_n)$, on a, en outre, 

$$\forall n\in \mathbb{N},  \forall p\ge n, x_p \in \overline{B_n}$$

Ce qui implique que y appartient à tous les fermés $(\overline{B_n})$.

$$y \in \bigcap_{n\in\mathbb{N}}\overline{B_n} \subset \bigcap_{n\in\mathbb{N}}A_n \subset \bigcup_{n\in\mathbb{N}}A_n$$

Autrement dit, y est dans $B(x,\varepsilon)\cap \displaystyle\bigcup_{n\in\mathbb{N}}A_n$. Ce qui prouve la densité de notre ensemble.


**Point n°1**

Supposons que A soit un espace localement compact. Autrement dit, à tout point, on peut définir un voisinage compact. 

Remarquons premièrement un résultat intéressant. Soit K un compact, soit $X\subset A$ un fermé. $X\cap K$ est un compact ou est vide. Simplement, si l'intersection n'est pas vide les éléments de l'intersection sont bornés. Par intersection, on a que l'intersection est fermée. $X\cap K$ est une partie fermée, bornée dans un compact K, donc $X\cap K$ est un compact.

En reprenant les notations précédentes, on peut alors définir à chaque fois, une suite de compact $(K_n)$ décroissante telle que le diamètre décroit vers 0.
$$\delta (K_n) = min_{x,y\in K_n} d(x,y) \text{    qui existe car K_n est compact}$$

Soit x dans A, il existe un voisinage $B(x,\varepsilon)$. On définit une boule $B_0$ fermée incluse dans $A_0\cap B(x,\varepsilon)$. On peut ensuite définir le compact K voisinage de x. Et donc $K_0 = B_0\cap K$ est un compact.

Ensuite, il existe une boule fermée incluse dans $A_1\cap K_0$. On peut définir son rayon aussi petit qu'on souhaite, par exemple $r_1 = \dfrac{1}{2}\delta{K_0}.
On peut poser K le voisinage compact de $x_1$. Et finalement, poser $K_1 = B_1\cap K$

On imagine ensuite le processus (similaire au point 1) pour obtenir une suite de compacts $(K_n)$ imbriqués.

Mais, pour rappel, la suite $(x_n)$ obtenue est de Cauchy, donc bornée. N'oublions pas qu'elle est également dans un compact, donc elle admet une valeur d'adhérence y qui appartient à $K_0$. On note $x_{\varphi(n)}$ sa suite extraite. On sait que si $n\ge p, x_n \in K_p$. Donc, $\forall n\in\mathbb{N}, x_{\varphi(n + p)}\in K_p. Donc $x_{\varphi(n + p)}$ tend vers y (c'est une suite extraite de $x_{\varphi(n)}$ et est dans le compact $K_p$ donc y est dans $K_p$.

Conclusion y appartient à l'intersection des compacts $(K_n)$. Donc il ne s'agit pas d'un singleton vide. On obtient que $(x_n)$ ne peut avoir qu'une seule valeur d'adhérence donc $(x_n)$ converge vers y.

On a que $$\bigcap_{n\in\mathbb{N}}K_n \subset \bigcap_{n\in\mathbb{N}}A_n \bigcup_{n\in\mathbb{N}}A_n$$
A fortiori, y appartient l'union ainsi qu'au voisinage de x donc $\displaystyle\bigcap_{n\in\mathbb{N}}K_n \subset \bigcap_{n\in\mathbb{N}}A_n$$ Donc $\bigcup_{n\in\mathbb{N}}A_n$ est une partie dense de A.
