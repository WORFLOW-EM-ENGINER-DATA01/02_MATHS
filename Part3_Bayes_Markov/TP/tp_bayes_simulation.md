# TP : Application du Théorème de Bayes avec Python et Pandas

## Durée : 2 heures

# Partie 1 : Introduction et Théorie 

**Rappels théoriques :**
1. **Théorème de Bayes** :
$$ P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)} $$
2. **Probabilité totale** : 
$$ P(B) = \sum_{i} P(B|A_i) \cdot P(A_i) $$

**Exemples d'application** :
- Diagnostic médical.
- Filtrage de spams.
- Probabilités en jeux de cartes.

**Questions théoriques**  :
1. Que représente \( P(A|B) \) dans le contexte d'un test médical ?
2. Comment la rareté d'une maladie affecte-t-elle l'interprétation des résultats d'un test ?

# Partie 2 : Simulation en Python 

## Objectif :
Simuler un cas de diagnostic médical en Python et estimer la probabilité conditionnelle avec le théorème de Bayes.

**Étape 1 : Simuler des Données**
- Simulez une population de 1000 individus.
- La probabilité qu'une personne soit malade est de 1 %.
- Le test de dépistage a une sensibilité de 90 % et un taux de faux positifs de 5 %.

**Code à implémenter :**

```python
import numpy as np
import pandas as pd

# Fixer la seed pour la reproductibilité
np.random.seed(42)

# Nombre d'individus
n = 1000

# Probabilité d'avoir la maladie
p_maladie = 0.01
maladie = np.random.choice([1, 0], size=n, p=[p_maladie, 1 - p_maladie])

# Générer les résultats de test
test_positif = np.where(maladie == 1,
                        np.random.choice([1, 0], size=n, p=[0.9, 0.1]),
                        np.random.choice([1, 0], size=n, p=[0.05, 0.95]))

# Créer le DataFrame
data = pd.DataFrame({
    'Maladie': maladie,
    'Test_Positif': test_positif
})

# Afficher les premières lignes du DataFrame
print(data.head())
```

**Questions :**
1. Combien de personnes sont malades dans votre simulation ?
2. Combien de tests positifs ont été obtenus ?
3. Calculez la probabilité conditionnelle que quelqu'un soit malade sachant que son test est positif.

**Réponse :**

```python
# Nombre total de tests positifs
total_test_positif = data['Test_Positif'].sum()

# Nombre de personnes malades parmi les tests positifs
malade_et_positif = data[(data['Maladie'] == 1) & (data['Test_Positif'] == 1)].shape[0]

# Probabilité conditionnelle
P_M_given_P = malade_et_positif / total_test_positif

print(f"La probabilité d'avoir la maladie sachant que le test est positif est : {P_M_given_P:.4f}")
```

# Partie 3 : Manipulation de Données avec Pandas 

## Objectif :
Explorer et analyser les données simulées en utilisant des techniques plus avancées avec Pandas.

**Étape 1 : Analyse Descriptive**
- Utilisez Pandas pour décrire les données et visualiser la distribution des tests positifs et négatifs.

**Exercice :**
- Calculez et affichez la proportion de tests positifs et négatifs dans votre simulation.

```python
# Distribution des tests positifs et négatifs
distribution_tests = data['Test_Positif'].value_counts(normalize=True)
print(distribution_tests)
```

**Étape 2 : Analyse des Sous-Groupes**
- Séparez les données en deux sous-groupes : ceux qui sont malades et ceux qui ne le sont pas.
- Calculez la proportion de tests positifs dans chacun de ces sous-groupes.

**Exercice :**
- Affichez la proportion de tests positifs pour les individus malades et non malades.

```python
# Proportion de tests positifs pour les malades
positif_malades = data[data['Maladie'] == 1]['Test_Positif'].mean()
print(f"Proportion de tests positifs chez les malades : {positif_malades:.4f}")

# Proportion de tests positifs pour les non malades
positif_non_malades = data[data['Maladie'] == 0]['Test_Positif'].mean()
print(f"Proportion de tests positifs chez les non malades : {positif_non_malades:.4f}")
```

# Partie 4 : Discussion et Extension (20 min)

## Objectif :
Interpréter les résultats obtenus et discuter de leur signification dans un contexte réel.

**Discussion :**
- Comparez la probabilité conditionnelle obtenue par simulation avec la valeur théorique calculée à l'aide du théorème de Bayes.
- Pourquoi est-il important de connaître la prévalence de la maladie dans la population lors de l'interprétation des résultats d'un test ?

**Extension :**
- Simulez un autre scénario où la maladie est plus courante (par exemple, 10 % de la population) et comparez les résultats.
- Comment les probabilités changent-elles avec une prévalence plus élevée ?

**Code à modifier :**

```python
# Modifier la probabilité d'avoir la maladie
p_maladie = 0.1  # 10 % de la population
# Répétez les étapes de simulation et d'analyse avec cette nouvelle probabilité.
```

--- Partie 2

## Simulation 

Créons un DataFrame avec des colonnes indiquant si une personne est malade et si son test est positif.

```python
import pandas as pd
import numpy as np

# Fixer la seed pour la reproductibilité
np.random.seed(42)

# Simuler 1000 individus
n = 1000

# Probabilité d'avoir la maladie
p_maladie = 0.01
maladie = np.random.choice([1, 0], size=n, p=[p_maladie, 1 - p_maladie])

# Générer les résultats de test
# Si malade: 90% de probabilité d'avoir un test positif
# Si non malade: 5% de probabilité d'avoir un test positif (faux positif)
test_positif = np.where(maladie == 1,
                        np.random.choice([1, 0], size=n, p=[0.9, 0.1]),
                        np.random.choice([1, 0], size=n, p=[0.05, 0.95]))

# Créer le DataFrame
data = pd.DataFrame({
    'Maladie': maladie,
    'Test_Positif': test_positif
})

# Afficher les premières lignes du DataFrame
print(data.head())
```

1. Calculer les Probabilités 

$$ P(Maladie | Test\ Positif) $$.