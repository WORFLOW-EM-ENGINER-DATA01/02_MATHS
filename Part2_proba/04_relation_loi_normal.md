# Loi Normale 

```python
import random
import matplotlib.pyplot as plt
import numpy as np

# Fonction pour simuler un lancé de pièce (0 pour Pile, 1 pour Face)
def toss_coin():
    return random.randint(0, 1)

# Fonction pour simuler 5 lancés de pièce et compter le nombre de "Pile"
def simulate_5_coin_tosses():
    num_piles = 0
    for _ in range(5):
        if toss_coin() == 0:
            num_piles += 1
    return num_piles

# Simuler et collecter les résultats des 10 000 simulations
total_simulations = 10000
results = [simulate_5_coin_tosses() for _ in range(total_simulations)]

# Calculer la fréquence de chaque résultat
num_piles_counts = [results.count(i) / total_simulations for i in range(6)]

# Tracer l'histogramme empirique
plt.bar(range(6), num_piles_counts, color='skyblue', edgecolor='black', alpha=0.7, label='Empirique')

# Calculer la moyenne et l'écart type théoriques pour la distribution binomiale
n = 5
p = 0.5
mean = n * p
std_dev = np.sqrt(n * p * (1 - p))

# Générer les valeurs pour la distribution normale
x = np.arange(0, 6, 0.1)
y = [1 / (std_dev * np.sqrt(2 * np.pi)) * np.exp(-(i - mean)**2 / (2 * std_dev**2)) for i in x]

# Tracer la courbe de la distribution normale
plt.plot(x, y, color='red', label='Normale')

# Configurer le graphique
plt.xlabel('Nombre de "Pile"')
plt.ylabel('Fréquence / Densité')
plt.title('Distribution du Nombre de "Pile" sur 5 Lancés de Pièce')
plt.xticks(range(6))
plt.legend()
plt.grid(axis='y', linestyle='--', alpha=0.7)
plt.show()
```