# Cours sur le Théorème de Bayes

Le théorème de Bayes est un des concepts fondamentaux en probabilité, particulièrement utile pour mettre à jour des probabilités en fonction de nouvelles informations. Il a des applications en statistique, en machine learning, en diagnostic médical, et bien d'autres domaines.

## 1. Introduction au Théorème de Bayes

Le théorème de Bayes permet de calculer la probabilité d'un événement à partir d'informations préalables, souvent exprimée en termes de probabilités conditionnelles.

**Formule du Théorème de Bayes :**
$$P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)}$$

( ** voir la démonstration ci-après )

$$P(A|B)$$ 
- Probabilité de l'événement \( A \) sachant que \( B \) s'est produit.
$$P(B|A)$$ 
- Probabilité de l'événement \( B \) sachant que \( A \) s'est produit.
$$P(A)$$ 
- Probabilité a priori de \( A \) (probabilité de base avant toute observation).
$$P(B)$$ 
- Probabilité de \( B \) (probabilité totale de l'événement \( B \)).

## 2. Interprétation du Théorème de Bayes

Le théorème de Bayes permet de "mettre à jour" nos croyances (probabilité a priori) après avoir observé de nouvelles données (probabilité conditionnelle). Cette mise à jour se fait en tenant compte de la probabilité que ces nouvelles données aient été observées si l'hypothèse \( A \) était vraie.

**Exemple Intuitif :**

Imaginons que vous faites un test médical pour une maladie rare. Le test est positif. Le théorème de Bayes vous aide à évaluer la probabilité que vous ayez vraiment la maladie, en prenant en compte la précision du test et la rareté de la maladie.

## 3. Calcul de la Probabilité Totale

Avant d'utiliser le théorème de Bayes, il est souvent nécessaire de calculer \( P(B) \), la probabilité totale de l'événement \( B \). Cette probabilité peut être obtenue en considérant toutes les façons dont \( B \) peut se produire.

**Formule pour la probabilité totale :**
$$P(B) = \sum_{i} P(B|A_i) \cdot P(A_i)$$
où \( A_i \) sont des événements qui forment une partition de l'espace des possibles (c'est-à-dire que l'un d'entre eux doit se produire).

## 4. Exemple Concret

**Exemple : Diagnostic Médical**

Supposons qu'une maladie touche 1 % de la population (\( P(Maladie) = 0,01 \)). Un test de dépistage détecte cette maladie avec une sensibilité de 90 % (\( P(Positive|Maladie) = 0,9 \)) et donne un faux positif 5 % du temps (\( P(Positive|Pas de maladie) = 0,05 \)).

Vous venez de recevoir un résultat positif au test. Quelle est la probabilité que vous ayez effectivement la maladie ?

**Étape 1 : Identifier les événements**
- \( A \) : Vous avez la maladie.
- \( B \) : Le test est positif.

**Étape 2 : Appliquer le théorème de Bayes**
$$P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)}$$
Avec :
$$P(B|A) = 0,9$$
$$P(A) = 0,01$$
$$P(B)$$ 
peut être calculé comme :
$$P(B) = P(B|A) \cdot P(A) + P(B|\text{Pas de maladie}) \cdot P(\text{Pas de maladie})$$
C'est-à-dire :
$$P(B) = (0,9 \times 0,01) + (0,05 \times 0,99) = 0,009 + 0,0495 = 0,0585$$

**Étape 3 : Calculer la probabilité que vous ayez la maladie**
$$P(A|B) = \frac{0,9 \times 0,01}{0,0585} \approx 0,1538$$

Donc, même avec un test positif, la probabilité que vous ayez réellement la maladie est d'environ 15,38 %. Cela montre l'importance de la rareté de la maladie dans l'interprétation des résultats du test.

## 5. Applications du Théorème de Bayes

Le théorème de Bayes est extrêmement utile dans plusieurs domaines :
- **Diagnostic Médical :** Estimer la probabilité d'une maladie en fonction des résultats des tests.
- **Machine Learning :** Utilisé dans les classificateurs bayésiens, un type de modèle de classification.
- **Économie :** Pour la mise à jour des croyances en fonction de nouvelles informations.
- **Criminologie :** Dans l'analyse des preuves et l'évaluation des probabilités conditionnelles en contexte judiciaire.

## 6. Exercices Pratiques

1. **Test de Dépistage :** Un autre test médical a une sensibilité de 95 % et un taux de faux positifs de 2 %. Si la prévalence de la maladie est de 2 %, quelle est la probabilité que vous ayez la maladie si le test est positif ?

2. **Spam :** Un filtre anti-spam détecte correctement les spams avec une probabilité de 98 % et marque incorrectement les e-mails légitimes comme spam dans 1 % des cas. Si 5 % des e-mails reçus sont des spams, quelle est la probabilité qu'un e-mail soit réellement un spam s'il est marqué comme tel ?

3. **Jeux de Cartes :** Dans un jeu de cartes, vous tirez une carte au hasard, et elle est rouge. Quelle est la probabilité que ce soit un cœur, sachant que vous avez tiré une carte rouge ?

# Conclusion

Le théorème de Bayes est un outil puissant pour raisonner en probabilités conditionnelles et réviser des croyances face à de nouvelles informations. Bien qu'il semble parfois contre-intuitif, il fournit une base mathématique solide pour la prise de décision dans des situations incertaines.

## Démonstration du théorème de Bayes

$$P(A \mid B) = \frac{P(B \mid A) \cdot P(A)}{P(B)}$$

1. **Définition de la probabilité conditionnelle :**

   Par définition, la probabilité de \( A \) conditionnellement à \( B \) est donnée par :

   $$P(A \mid B) = \frac{P(A \cap B)}{P(B)}$$

   où \( P(A \cap B) \) est la probabilité de l'intersection de \( A \) et \( B \) (c'est-à-dire que les deux événements \( A \) et \( B \) se produisent).

2. **Expression de \( P(A \cap B) \) en termes de \( P(B \mid A) \) :**

   De la même manière, on peut écrire la probabilité de l'intersection \( A \cap B \) en termes de la probabilité conditionnelle de \( B \) sachant \( A \) :

   $$P(A \cap B) = P(B \mid A) \cdot P(A)$$

3. **Substitution dans la formule de la probabilité conditionnelle :**

   En remplaçant \( P(A \cap B) \) dans l'expression de \( P(A \mid B) \) par \( P(B \mid A) \cdot P(A) \), on obtient :

   $$P(A \mid B) = \frac{P(B \mid A) \cdot P(A)}{P(B)}$$

   C'est exactement l'expression du théorème de Bayes.
