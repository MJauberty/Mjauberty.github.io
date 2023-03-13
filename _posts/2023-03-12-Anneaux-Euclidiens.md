---
---
### Anneaux euclidiens

Soit $$ (\mathcal{A},+,\times) $$ un anneau intègre unitaire commutatif. $$ (\mathcal{A},f) $$ est dit "euclidien" si f est une application $$ \mathcal{A}^* \longrightarrow \mathbb{N} $$ 
qui vérifie les propriétés suivantes.

(i) $$ \forall x,y\in\mathcal{A}^*, \textbf{     }f(xy)\ge f(y) $$

(ii) $$ \forall a \in\mathcal{A}, \forall b\in\mathcal{A}^*, \exists q,r\in\mathcal{A}, a = bq+r \text{   où   } f(r) < f(b) \text{  ou  } r = 0 $$

Pour être plus clair, c'est un anneau dans lequel on peut faire plus ou moins une sorte de division euclidienne. Mais attention, nous n'avons, a priori, pas unicité
du couple (q,r).

Remarque : $$ f : n \mapsto \lvert n\rvert $$ dans $$ \mathbb{Z} $$ ou $$ f: P\mapsto deg(P) $$ sont des applications qui vérifient ces propriétés.

f est appelé un stathme.

#### Anneaux principaux et idéaux

Pour être certain de savoir de quoi nous parlons, rappelons la définition d'un idéal.

I est un idéal de A signifie que 
$$\forall x\in I, \forall a \in\mathcal{A},\textbf{     }xa \in I$$

Et I est un sous-groupe additif de $$(\mathcal{A},+)$$.

L'idéal permet de généraliser l'arithmétique et la notion de divisibilité, quand cela se passe bien, je vous laisse vous en convaincre avec la définition d'idéal principal.

Un idéal est dit **principal** si il est de la forme $$ x\mathcal{A} = \{xa, a\in\mathcal{A}\} $$. Si vous vous rappelez de l'arithmétique de $$\mathbb{Z}$$, on a ici
un idéal _multiple de x_. (Je laisse la preuve au lecteur)

Simplement, on dit qu'un anneau est principal si tous ses idéaux sont principaux. Autrement dit... on sent que faire de l'arithmétique dedans sera plus aisé.

#### Tout anneau euclidien est un anneau principal

On peut déjà remarquer que l'idéal $$I = \{0\}$$ sera bien de la forme $$0\mathcal{A}$$. Considérons maintenant un idéal I différent de celui-là.

Je vais poser x l'élément qui minimise f restreinte à $$I^*$$. Cet élément existe car l'image est une partie de $$\mathbb{N}$$.

Pour expliquer ce choix étrange, on peut voir f comme une mesure arithmétique. Or, nous avons vu que arithmétique et idéaux sont assez proches.

Dans $$\mathbb{Z}$$ par exemple, pour déterminer l'ensemble des multiples de n, on prend comme générateur l'élément qui a la plus petite mesure arithmétique.
C'est-à-dire, 4 ou -4 (cf. remarque introduction $$f(n) = \lvert n \rvert$$).

Concrètement, on veut s'assurer qu'un autre élément y ne puisse pas "diviser" notre élément x. Et cela ne pourrait arriver qu'à la condition où la mesure arithmétique
de x puisse déjà être inférieure à celle de y.

Reprenons notre démonstration. Il est clair que $$x\mathcal{A}\subset I$$ puisque x est un élément de I.

Soit y dans I. Utilisons la propriété (ii)

$$\exists q,r\in\mathcal{A}, y = xq+r \text{   où   } f(r) < f(x) \text{  ou  } r = 0$$

Or, si $$r\neq 0$$, alors $$f(r) < f(x)$$ et $$r = y - xq \in I$$. Donc $$r\in I^*$$. Cela contredit la définition de x.

Donc r est nul. Finalement : $$y = xq \in x\mathcal{A}$$. D'où l'égalité : $$x\mathcal{A} = I$$.

Notre anneau est bien un anneau principal.

Ce résultat est assez intéressant ! Premièrement, montrer qu'un anneau est principal n'est pas toujours évident. Cela donne une nouvelle méthode plus ou moins simple.
Mais surtout, l'existence d'une mesure arithmétique permet à elle-seule de définir une arithmétique.

#### Condition d'unicité de (q,r)

Si nous ajoutons une troisième propriété à notre application f : 

$$\forall x,y \in\mathcal{A}^*, f(x-y)\leq \max \{f(x),f(y)\}$$. 

Nous pouvons montrer l'unicité du
couple (q,r).
Soit a dans $$\mathcal{A}$$, et b un élément non nul. On se donne deux couples (q,r) et (q',r') qui vérifient les propriétés de (ii).

$$b(q-q') = r'-r$$

Supposons que $$q-q'\neq 0$$. On a d'après (i) $$f(r'-r) = f(b(q-q'))\ge f(b)$$

Nous ne pouvons avoir $$r'=r$$ car b et q-q' sont non nuls (et par intégrité...).

Si $$r' = 0$$ et $$r\neq 0$$.

$$f(r'-r) = f(r) \ge f(b)$$

Ce qui est impossible. On montre symétriquement qu'on ne peut avoir $$r = 0$$ et $$r' = 0$$.

Ne reste que le cas où $$r,r'\neq 0$$. On obtient d'après la propriété qu'on
a ajouté : 

$$f(r-r')\leq \max \{f(r),f(r')\}$$

$$\text{Donc   }\text{    }f(b)\leq f(r'-r) \leq f(r) \text{      et     }f(b)\leq f(r'-r) \leq f(r')$$

C'est encore une contradiction. Aucune issue n'est possible, notre premier hypothèse était fausse : $q = q'$. Il s'en suit que $r=r'$.

#### Condition d'inversibilité dans un anneau euclidien.

On pose directement $$\alpha = f(1)$$. Soit x un élément inversible de $$\mathcal{A}$$.

On peut déjà remarquer avec la propriété (i) $$\forall x\in \mathcal{A}^*, f(x\times 1)\ge f(1) = \alpha$$

Qui plus est, x est inversible donc $$\alpha = f(1) = f(x^{-1}x)\ge f(x)$$

Donc on trouve que $$f(x) = \alpha$$


Supposons que $$f(x) = \alpha$$. On peut prendre q,r tel que 1 = xq + r. Si r est non nul, $$f(r) < f(x) = \alpha$$ (Or on a vu que $$\alpha$$ minorait les éléments non nuls).

Donc $$r = 0$$. Il existe donc un élément q de $$\mathcal{A}$$ tel que $$xq = 1$$. Donc x est inversible.

#### Application non triviale, les entiers de Gauss.

On appelle _Entiers de Gauss_ l'ensemble $$\mathbb{Z}[i]$$.

$$\mathbb{Z}[i] := \{a + ib ; a,b\in\mathbb{Z}\}$$

Je vous laisse démontrer qu'il s'agit bien d'un anneau intègre commutatif unitaire.

Posons $$\forall z\in\mathbb{Z}[i]^*, \text{    }f(z) = \lvert z\rvert^2 \in\mathbb{N}$$. On a déjà la première propriété vérifiée.

$$(i)\forall z,z'\in\mathbb{Z}[i]^*, \text{    }f(zz') = f(z)f(z') \ge f(z')$$

La deuxième est un peu plus subtile. Pour $$x$$ un réel, on note $$[x]$$ le reste décimal le plus petit en valeur absolue. 

Explicitement, $$[x] = \lfloor x \rfloor$$ si $$\lvert x-\lfloor x \rfloor \rvert\leq \dfrac{1}{2}$$ et $$[x] = \lceil x \rceil$$ si $$\lvert x-\lceil x \rceil\rvert < \dfrac{1}{2}$$.

Fastidieux à écrire mais terriblement simple à voir sur un dessin, cette application est bien définie. Autrement dit, on peut toujours définir un entier $$x_0$$
tel que $$\lvert x - x_0 \rvert \leq \dfrac{1}{2}$$.

Soit $$z\in\mathbb{C}$$, on peut définir $$z_0 \in \mathbb{Z}[i]$$ tel que $$\lvert z-z_0\rvert^2 < 1$$. On pose simplement $$z_0 = [\Re (z)] + i [\Im (z)]$$

Très bien, désormais, prenons z un entier de Gauss, z' un élément non nul. $$\dfrac{z}{z'}\in\mathbb{C}$$.

$$\exists z_0 \in \mathbb{Z}[i], \lvert z_0-\dfrac{z}{z'}\rvert^2 < 1$$

 $$\text{Donc   }\text{     }\lvert z_0z' - z \rvert^2 < 1\times \lvert z z' \rvert^2 = f(1)f(z') = f(z')$$

Posons $$r = z-z_0z'$$ et $$q = z_0$$. On obtient :

$$z = qz' + r \text{    avec    } r = 0 \text{    ou   } f(r) < f(z')$$.

Conclusion ! $$\mathbb{Z}[i]$$ est un anneau euclidien, et donc un anneau principal (imaginez l'arithmétique ensuite). Et nous pouvons obtenir à moindre frais
les inversibles de l'ensemble. (1,-1,i,-i)






