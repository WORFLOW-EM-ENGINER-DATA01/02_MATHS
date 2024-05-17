#  Temps de service dans un Restaurant

## Contexte 

⏲️ Un restaurant souhaite estimer le temps moyen que ses clients passent à la caisse pour payer. 
Les temps de service individuels peuvent varier en fonction de nombreux facteurs (comme le nombre d'articles achetés, le mode de paiement, etc.) et ne suivent pas nécessairement une distribution normale. 

Le manager souhaite utiliser ces temps pour prévoir le personnel nécessaire pour éviter les longues files d'attente.

⚠️ Temps de service individuels : Ces temps peuvent être très variables et peuvent ne pas suivre une distribution normale.

**Approche TCL :**

Vous simulerez cette problématique en Python afin de répondre aux questions suivantes.

1. **Collecter les données :**
   Le restaurant collecte les temps de service pour 10000 clients.

1. **Calculer les moyennes d'échantillons :**
   Diviser ces 10000 temps de service en groupes de 1000 (par exemple), puis calculer la moyenne des temps de service pour chaque groupe. Cela donne 20 moyennes d'échantillons.

1. **Distribution des moyennes :**
   Selon le TCL, la distribution de ces moyennes d'échantillons sera approximativement normale, même si la distribution des temps de service individuels ne l'est pas.

## Annexes

Voilà ce que vous pourriez faire avec la loi normale.
   
🍅 Supposons que la moyenne des moyennes d'échantillons (μₙ) est de 150 secondes. 

Si un caissier travaille pendant une période de 3600 secondes (1 heure), vous pouvez estimer qu'un caissier peut servir environ 3600 / 150 ≈ 24 clients par heure.

Si vous attendez 240 clients en une heure, vous aurez besoin d'environ 240 / 24 = 10 caissiers.

- En résumé

- Moyenne des moyennes d'échantillons : C'est le temps moyen de service estimé.
  
- Écart type des moyennes d'échantillons : Mesure de la dispersion des temps de service moyens.

- Nombre de clients qu'un caissier peut servir par heure : Utilisé pour estimer le nombre de caissiers nécessaires.
  
- Nombre de caissiers nécessaires : Indique combien de caissiers sont requis pour gérer efficacement la charge de travail prévue.

Bon développement.