# Binaire

## Rappels sur le système décimal (`base 10`)
Dans le système décimal, la `position` la plus à droite s’appelle « unité », à sa gauche la « dizaine », puis « centaine », et ainsi de suite.

Par exemple pour le nombre `123`, nous avons le tableau de numération et des positions suivant:

|          | **Millier** | **Centaine** | **Dizaine** | **Unité** |
|:--------:|:-------:|:--------:|:-------:|:-----:|
| <small>Position</small> |    <small>4</small>    |     <small>3</small>    |    <small>2</small>    |   <small>1</small>   |
|          |         |     1    |    2    |   3   |


Le système décimal comporte 10 valeurs différentes (d’où le nom de `base 10`), allant de 0 à 9. Lorsque l’unité atteint sa valeur la plus haute (9), on la ramène à sa première valeur (0) et on incrémenté de 1 (la retenu) la position à sa gauche, dans notre cas les dizaines.

Les positions sont comptées à partir de 0, en partant de la droite:

|          | **Centaine** | **Dizaine** | **Unité** |
|:--------:|:--------:|:-------:|:-----:|
| <small>Position</small> |     <small>2</small>     |    <small>1</small>    |   <small>0</small>   |
|  <small>Départ</small>  |          |         |   0   |
|    <small>+1</small>    |          |         |   1   |
|    <small>+1</small>    |          |         |   2   |
|    <small>+1</small>    |          |         |   3   |
|     …    |    …     |    …    |   …   |
|    <small>+1</small>    |          |         |   9   |
|    <small>+1</small>    |          |    1    |   0   |


Enfin, lorsqu'on décale un chiffre d'une position vers la gauche, on le multiplie par la base (ici 10). Lorsqu'on décale un chiffre vers la droite, on le divise par la base. Fais l'exercice de tête, t'as pas besoin d'un tableau pour ça.


## Système binaire (`base 2`)
Le système binaire fonctionne strictement de la même façon, sauf qu'il n'existe que 2 valeurs: 0 et 1, et que cette « unité » s'appelle le `bit`:

| <small>Position</small> |     <small>2</small>     |    <small>1</small>    |   <small>0</small>   | <small>base 10</small> |
|:-------:|:--------:|:-------:|:-----:|:------:|
|  <small>Départ</small>  |          |         |   0   |    0   |
|    <small>+1</small>    |          |         |   1   |   1   |
|    <small>+1</small>    |          |    1    |   0   |   2   |
|    <small>+1</small>    |          |    1    |   1   |   3   |
|    <small>+1</small>    |    1     |    0    |   0   |   4   |
|    <small>+1</small>    |    1     |    0    |   1   |   5   |
|    <small>+1</small>    |    1     |    1    |   0   |   6   |
|    <small>+1</small>    |    1     |    1    |   1   |   7   |


De même que le décalage d'une position à gauche revient à multiplier la valeur par la base (ici 2), et le décalage à gauche revient à diviser par la base.