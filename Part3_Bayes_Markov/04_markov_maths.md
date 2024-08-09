# Les Chaînes de Markov

### 1. **Introduction aux Chaînes de Markov**

Une chaîne de Markov est un type particulier de processus stochastique (c'est-à-dire aléatoire) où l'évolution d'un système ne dépend que de son état actuel et pas de l'historique des états précédents. Autrement dit, "l'avenir" du système ne dépend que de "ce qui se passe maintenant" et non de "ce qui s'est passé avant".

**Exemple simple** : Imaginez que vous êtes sur une grille avec trois cases : A, B, et C. À chaque étape, vous lancez un dé pour décider de votre prochaine position. Votre position future dépend uniquement de votre position actuelle et des résultats du dé, pas des positions où vous étiez auparavant.

### 2. **Définition Formelle**

Une chaîne de Markov est définie par :
- **Un ensemble d'états** :
$$S = \{s_1, s_2, \dots, s_n\}$$
- **Probabilités de transition** :
$$P_{ij}$$ est la probabilité de passer de l'état 
$$s_i$$ 
à l'état 
$$s_j$$ 

en une seule étape.

Ces probabilités de transition peuvent être représentées dans une **matrice de transition** \( P \) :

$$P = \begin{pmatrix}
P_{11} & P_{12} & \dots & P_{1n} \\
P_{21} & P_{22} & \dots & P_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
P_{n1} & P_{n2} & \dots & P_{nn}
\end{pmatrix}$$

Chaque élément \( P_{ij} \) représente la probabilité de transition de l'état \( s_i \) vers \( s_j \).

**Propriété importante** : La somme des probabilités sur chaque ligne de la matrice de transition doit être égale à 1 :

$$\sum_{j=1}^{n} P_{ij} = 1, \quad \text{pour tout } i$$

### 3. **Propriété de Markov**

La propriété de Markov stipule que la probabilité de se trouver dans un état donné à l'étape \( n+1 \) dépend uniquement de l'état à l'étape \( n \), pas des états précédents :

$$P(X_{n+1} = s_j \mid X_n = s_i, X_{n-1} = s_{i_{n-1}}, \dots, X_0 = s_{i_0}) = P(X_{n+1} = s_j \mid X_n = s_i)$$
### Exercice

Imaginons un petit jeu où un joueur peut se déplacer entre trois pièces dans une maison : **A**, **B**, et **C**. À chaque étape, le joueur choisit au hasard de se déplacer vers une pièce adjacente ou de rester dans la pièce où il se trouve.

Voici les règles de déplacement :

- Si le joueur est dans la pièce **A**, il a 50% de chances de rester dans **A** et 50% de chances d'aller dans **B**.
- Si le joueur est dans la pièce **B**, il a 25% de chances d'aller dans **A**, 25% de chances d'aller dans **C**, et 50% de chances de rester dans **B**.
- Si le joueur est dans la pièce **C**, il a 50% de chances de rester dans **C** et 50% de chances d'aller dans **B**.

#### Questions

1. Construisez la matrice de transition \( P \) pour ce système.
   
2. Si le joueur commence dans la pièce **A**, quelle est la probabilité qu'il soit dans la pièce **C** après deux étapes ?

