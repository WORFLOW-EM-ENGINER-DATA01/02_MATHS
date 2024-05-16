#  Introduction aux Probabilités

Les probabilités sont une branche des mathématiques qui nous permettent de quantifier et d'analyser l'incertitude. Elles sont utilisées dans de nombreux domaines tels que la science, l'économie, la finance et bien d'autres. Comprendre les probabilités est essentiel pour prendre des décisions éclairées dans un monde où l'incertitude est omniprésente.

## Concepts Fondamentaux

### 1. Espace Probabilisé

Lorsque nous étudions les probabilités, nous travaillons généralement avec des expériences aléatoires, c'est-à-dire des expériences dont le résultat n'est pas déterminé à l'avance. 

🚀 L'ensemble de tous les résultats possibles d'une expérience aléatoire est appelé l'espace probabilisé, noté Ω.

### 1. Qu'est-ce qu'un Phénomène Aléatoire ?

Un phénomène est dit aléatoire lorsqu'on ne peut pas prédire son issue avec certitude avant qu'il ne se produise. 

Par exemple, lancer un dé, tirer une carte d'un jeu, ou prédire si une journée sera ensoleillée sont tous des phénomènes aléatoires. Les probabilités nous permettent de quantifier l'incertitude associée à ces phénomènes.

### 1. Notion d'Expérience Aléatoire

Une expérience aléatoire est une expérience dont le résultat ne peut être prédit avec certitude. Les résultats possibles de cette expérience sont appelés les issues.

Exemples d'Expériences Aléatoires :

- Tirer une carte d'un jeu de 52 cartes.
- Lancer un dé à six faces.
- Tirer une boule d'une urne contenant des boules de différentes couleurs.

### 1. Événements

Un événement est un sous-ensemble de l'espace probabilisé, c'est-à-dire un ensemble de résultats possibles. Par exemple, si nous lançons un dé à six faces, l'espace probabilisé est {1, 2, 3, 4, 5, 6}, et un événement pourrait être "obtenir un nombre pair", noté E.

### 1. Probabilité

La probabilité d'un événement est une mesure de la chance qu'il se produise. Elle est généralement exprimée comme un nombre compris entre 0 et 1, où 0 signifie que l'événement est impossible et 1 signifie qu'il est certain. La probabilité d'un événement A est notée P(A).

## Calcul des Probabilités

### 1. Probabilité Équiprobable

Lorsque tous les résultats possibles ont la même chance de se produire, nous avons une probabilité équiprobable. Dans ce cas, la probabilité d'un événement est le rapport entre le nombre de résultats favorables et le nombre total de résultats possibles.

### 1. Probabilité Complémentaire

La probabilité complémentaire d'un événement A, notée P(A'), est la probabilité que l'événement A ne se produise pas. Elle est donnée par 1 - P(A).

### 1. Probabilité Conditionnelle

La probabilité conditionnelle d'un événement A sachant que l'événement B s'est produit, notée P(A|B), est la probabilité que A se produise sachant que B s'est produit. 

Elle est calculée comme le rapport entre la probabilité de l'intersection de A et B et la probabilité de B.

### Exercice d'application tirage sans remise

💊 Supposons que nous ayons une urne contenant des boules rouges et des boules vertes. 

Nous voulons calculer la probabilité de tirer une boule rouge sachant que nous avons déjà tiré une boule verte. Nous opterons pour un tirage sans remise.

Soit A l'événement "tirer une boule rouge" et B l'événement "tirer une boule verte".
La probabilité de B, P(B), est le nombre de boules vertes divisé par le nombre total de boules.

La probabilité de l'intersection de A et B, P(A ∩ B), est le nombre de boules rouges et vertes divisé par le nombre total de boules.

Par conséquent, la probabilité conditionnelle de tirer une boule rouge sachant que nous avons tiré une boule verte, P(A|B), est calculée comme P(A ∩ B) / P(B).


### (🍄 🍄) 01 Exercice boules rouges et vertes tirage sans remise

Supposons que nous avons une urne contenant :

🎱 5 boules rouges
🎱 5 boules vertes

Nous voulons calculer la probabilité de tirer une boule rouge sachant que nous avons déjà tiré une boule verte (tirage sans remise ).

1. Simulez le tirage d'une Urne sans remise en créant une fonction draw_ball.
1. Créez maintenant une fonction qui calcule la probabilité conditionnelle et comparez avec le résultat théorique.

## (🍄 🍄) 02 Exercice boules rouges et vertes tirage avec remise

Supposons que nous avons une urne contenant :

🎱 3 boules rouges
🎱 2 boules vertes

Calculez la probabilité de tirer une boule rouge sachant que nous avons tiré une boule verte, en supposant que chaque boule est remise dans l'urne après chaque tirage (tirage avec remise) 

### (🍄) 03 Exercices et Applications

Faites ces exercices en Python, simulez les résultats afin de vérifier la théorie

1. Vérifiez que chaque face de dé à la même chance d'apparaitre avec un script Python
1. **Lancers de Dé** : Calculer la probabilité d'obtenir un nombre pair en lançant un dé à six faces.
1. **Tirage de Cartes** : Déterminer la probabilité d'obtenir un roi en tirant une carte d'un jeu de 52 cartes.


