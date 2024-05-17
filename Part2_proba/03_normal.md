# TP Loi normale 

## Théorème centrale limite

Le théorème central limite (TCL) stipule que, quelle que soit la forme de la distribution d'une variable aléatoire, la somme d'un grand nombre d'observations indépendantes de cette variable aléatoire suit approximativement une distribution normale, à condition que le nombre d'observations soit suffisamment grand.

Plus formellement, soit X1, X2, ..., Xn des variables aléatoires indépendantes et identiquement distribuées (i.i.d.) avec une moyenne μ et un écart type σ. Alors, lorsque n devient grand (typiquement n ≥ 30), la distribution de la somme ∑ᵢ₌₁ⁿ Xi se rapproche d'une distribution normale avec une moyenne μₙ = n × μ et un écart type σₙ = √n × σ.

🚀 En d'autres termes, même si les variables aléatoires Xi ne suivent pas une distribution normale individuellement, la distribution de leur somme converge vers une distribution normale lorsque n devient suffisamment grand. 

Cela rend la distribution normale extrêmement importante et largement utilisée dans la modélisation statistique, car elle permet de simplifier et de généraliser de nombreux problèmes pratiques.

🍅 Pour ce dernier exemple voir le TP à réaliser pour la prochaine fois.

## Exercice 

Mettez en évidence ce principe à l'aide d'un script Python.

1. Fonction pour simuler un lancé de dé.
1. Simuler les lancés de dés et calculer la somme des résultats.
1. Tracer l'histogramme de la distribution des sommes 