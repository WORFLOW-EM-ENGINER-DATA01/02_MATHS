# Probabilité Conditionnelle

La probabilité conditionnelle est un concept fondamental en probabilité qui permet de calculer la probabilité d'un événement, en tenant compte d'une certaine condition. Autrement dit, c'est la probabilité qu'un événement se produise étant donné qu'un autre événement a déjà eu lieu.

## 1. Introduction à la Probabilité Conditionnelle

**Définition :** La probabilité conditionnelle de l'événement \( A \), sachant que l'événement \( B \) s'est produit, est notée \( P(A|B) \). Cela se lit "la probabilité de \( A \) sachant \( B \)".

**Formule :**
$$P(A|B) = \frac{P(A \cap B)}{P(B)}$$
- $$( P(A \cap B) )$$ 
*La probabilité que  A  et  B  se produisent simultanément.*
- $$P(B)$$ 
La probabilité que  B  se produise 

**Interprétation :** La formule dit que pour calculer la probabilité de \( A \) sous la condition que \( B \) s'est produit, on regarde la proportion de cas où \( A \) et \( B \) se produisent ensemble par rapport à tous les cas où \( B \) se produit.

### Exemple simple

**Problème :** Vous lancez un dé à six faces. Quel est la probabilité d'obtenir un 4 sachant que le résultat est un nombre pair ?

### Solution

1. **Définir les événements :**

   - \( A \) : Le résultat est un 4.
   - \( B \) : Le résultat est un nombre pair.

2. **Lister les résultats possibles :**

   - Un dé à six faces a les résultats possibles suivants : {1, 2, 3, 4, 5, 6}.

3. **Calculer les probabilités nécessaires :**

   - **Événement \( B \) :** Les nombres pairs sur un dé à six faces sont {2, 4, 6}. Il y a donc 3 résultats pairs sur les 6 possibles.

     La probabilité d'obtenir un nombre pair est :
    $$P(B) = \frac{\text{Nombre de résultats pairs}}{\text{Nombre total de résultats}} = \frac{3}{6} = \frac{1}{2}$$

   - **Événement \( A \cap B \) :** Le seul résultat qui est à la fois un 4 et un nombre pair est 4.

     La probabilité d'obtenir un 4 parmi les résultats pairs est :
    $$P(A \cap B) = \frac{1}{6}$$

   - **Probabilité de \( A \) sachant \( B \) :**

     La probabilité d'obtenir un 4 sachant que le résultat est un nombre pair se calcule comme suit :
    $$P(A \mid B) = \frac{P(A \cap B)}{P(B)}$$
     Ici, $$P(A \cap B) \) est \( \frac{1}{6}$$, et \( P(B) \) est \( \frac{1}{2} \). Donc :
    $$P(A \mid B) = \frac{\frac{1}{6}}{\frac{1}{2}} = \frac{1}{6} \times \frac{2}{1} = \frac{1}{3}$$

### Réponse

La probabilité d'obtenir un 4 sachant que le résultat est un nombre pair est de \( \frac{1}{3} \) ou environ 33,33 %.

### Explication

- **Total des résultats pairs :** {2, 4, 6} — 3 résultats.
- **Nombre de résultats favorables pour \( A \) parmi les nombres pairs :** 1 (le 4).

En conclusion, parmi les nombres pairs (2, 4, 6), il y a une chance sur trois que le nombre soit un 4.


## 3. Comprendre la Formule avec un autre Exemple

Supposons qu'on ait un jeu de cartes standard de 52 cartes. On veut trouver la probabilité de tirer un roi sachant que la carte tirée est une figure (roi, dame, ou valet).

- **Étape 1 :** Identifier les événements :
  - \( A \) : "Tirer un roi"
  - \( B \) : "Tirer une figure"

- **Étape 2 :** Calculer les probabilités :
  - Il y a 4 rois dans le jeu, donc 
  $$P(A) = \frac{4}{52}$$.
  - Il y a 12 figures (4 rois, 4 dames, 4 valets), donc
  $$P(B) = \frac{12}{52}$$.
$$P(A \cap B)$$ est la probabilité de tirer une carte qui est à la fois un roi et une figure. Comme les rois sont inclus dans les figures, 
  $$P(A \cap B) = P(A) = \frac{4}{52}$$

- **Étape 3 :** Appliquer la formule :
  $$P(A|B) = \frac{P(A \cap B)}{P(B)} = \frac{\frac{4}{52}}{\frac{12}{52}} = \frac{4}{12} = \frac{1}{3}$$

Cela signifie que si on sait que la carte tirée est une figure, la probabilité qu'elle soit un roi est :
$$\frac{1}{3}$$

## 4. Utilisations Pratiques

La probabilité conditionnelle est très utile dans de nombreuses situations, comme :

- **Diagnostique Médical :** Calculer la probabilité d'une maladie donnée les résultats d'un test.
- **Marketing :** Estimer la probabilité qu'un client achète un produit sachant qu'il a déjà acheté un autre produit.
- **Jeux de hasard :** Calculer les chances de gagner sachant certaines conditions.

## 5. Exercices pour Pratiquer

   
1. Dans une classe, 40% des élèves sont des filles et 60% sont des garçons. Parmi les filles, 70% aiment les maths. Quelle est la probabilité qu'un élève tiré au hasard soit une fille aimant les maths ?

2. On lance deux dés. Quelle est la probabilité que la somme soit 8 sachant que le premier dé montre un 5 ?
