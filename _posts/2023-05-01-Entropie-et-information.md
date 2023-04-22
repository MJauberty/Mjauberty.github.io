---
---
Dans ce petit article, nous allons aborder une notion importante de la théorie de l'information. Si cette théorie vous est étrangère, on peut grossièrement la résumer
(et c'est largement suffisant) en un domaine qui étudie le contenu d'une information, comment le transmettre efficacement, secrètement, ou bien comment le décoder, l'interpréter.

### Petit préambule de formalisme

En théorie de l'information, on modélise nos messages reçus par des variables aléatoires. Imaginons que je vous envoie successivement des lettres de l'alphabet.

On note par coutume du domaine $$\chi$$ ("chi" prononcé "ki") l'alphabet, l'ensemble des messages. Dans notre cas, le mot est bien choisi, il s'agit de l'alphabet latin.
Sans vous choquer, je pense affirmer :
$$|\chi| = 26$$

Si je distibuais aléatoirement mes lettres, on utiliserait pour formaliser une loi uniforme sur $$\llbracket1,26\rrbracket$$.
Du côté récepteur, on s'attend à recevoir un "e" une fois sur 26.

On pourrait aussi respecter les [fréquences "usuelles"](https://fr.wikipedia.org/wiki/Fr%C3%A9quence_d%27apparition_des_lettres#Base_statistique_de_calcul_:_la_hit_clair) des lettres. On observe davantage de "e" que de "z" en français par exemple.

#### Petit rappel de la loi de Bernoulli

C'est l'occasion de rappeler une loi simple et fondamentale, la loi de Bernoulli. On attribue à un évènement la qualité de "succès", l'évènement complémentaire est alors un "échec".
Par exemple, dans un lancer de pièce, on peut dire que faire face est un "succès" et faire pile devient un "échec".

On peut attribuer une probabilité $$p$$ à notre succès. La loi de Bernoulli renvoie simplement 1 quand le succès est réalisé, 0 sinon.

$$X({\text{succès}}) = 1 \text{     }\text{     } X({\text{échec}}) = 0$$

Dans le cadre de la théorie de l'information, elle sert à modéliser des envoies de codes binaires (succession de 1 et de 0) ou encore la question "ai-je reçu... ?".
Par exemple, je vous envoie des lettres de manière uniforme. Vous vous demandez "Est-ce que je reçois un "a" ?". Le succès est de recevoir le "a".

$$P(X = 1) = \dfrac{1}{26} \text{     }\text{      et     } P(X = 0) = \dfrac{25}{26}$$

On remarque alors que la modélisation probabiliste dépend autant de l'envoi que de la réception. En général, l'un est fixé.

### Entropie d'information

La notion d'entropie n'est pas totalement obscure à l'élève de classe prépa tant elle est fondamentale en thermodynamique. Une première approche de l'entropie est de dire qu'elle est une fonction croissante du désordre.
Cela vaut aussi physiquement. L'entropie d'un gaz est supérieure à l'entropie d'un solide, le premier est désordonné et le second est ordonné.
