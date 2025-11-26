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

| <small>Position</small> | <small>2</small> | <small>1</small> | <small>0</small> | <small>base 10</small> |
| :---------------------: | :--------------: | :--------------: | :--------------: | :--------------------: |
|  <small>Départ</small>  |                  |                  |        0         |           0            |
|    <small>+1</small>    |                  |                  |        1         |           1            |
|    <small>+1</small>    |                  |        1         |        0         |           2            |
|    <small>+1</small>    |                  |        1         |        1         |           3            |
|    <small>+1</small>    |        1         |        0         |        0         |           4            |
|    <small>+1</small>    |        1         |        0         |        1         |           5            |
|    <small>+1</small>    |        1         |        1         |        0         |           6            |
|    <small>+1</small>    |        1         |        1         |        1         |           7            |


De même que le décalage d'une position à gauche revient à multiplier la valeur par la base (ici 2), et le décalage à gauche revient à diviser par la base.


Voici la suite de ton cours — deux nouvelles sections : **Conversion binaire → décimal** puis **Conversion décimal → binaire**.


## Conversion binaire → décimal

À partir des elements précédents, il est possible de déterminer un tableau de quelques nombres binaires et de leur correspondance en décimal pour faire plusieurs conversions rapidement :

| <small>Position</small>  | <small>6</small> | <small>5</small> | <small>4</small> | <small>3</small> | <small>2</small> | <small>1</small> | <small>0</small> |
| :----------------------: | :--------------: | :--------------: | :--------------: | :--------------: | :--------------: | :--------------: | :--------------: |
| <small>Puissance</small> |  2<sup>6</sup>   |  2<sup>5</sup>   |  2<sup>4</sup>   |  2<sup>3</sup>   |  2<sup>2</sup>   |  2<sup>1</sup>   |  2<sup>0</sup>   |
|  <small>Valeur</small>   |        64        |        32        |        16        |        8         |        4         |        2         |        1         |

Ensuite, on décompose le nombre et on additionne les puissances / valeurs.

### Exemple

Nombre binaire `01 1011` :

1. On décompose le nombre en séparant la valeur de chaque position

```
   01 1011 (Valeur de départ)
=  01 0000
+  00 1000
+  00 0010
+  00 0001
```

2. On fait correspondre la valeur de chaque position grâce au tableau de dessus

```
01 0000 (= 2⁴ = 16)
00 1000 (= 2³ =  8)
00 0010 (= 2¹ =  2)
00 0001 (= 2⁰ =  1)
```

3. Il ne reste plus qu'à additionner

```
01 1011₂ = 2⁴ + 2³ + 2¹ + 2⁰ = 16 + 8 + 2 + 1 = 27₁₀
```


## Conversion décimal → binaire

Pour convertir un nombre écrit en décimal en binaire, il suffit de faire des divisions euclidiennes successive par 2 :

1. Diviser le nombre décimal par 2
2. Noter le reste (0 ou 1)
3. Prendre le **quotient** comme nouveau nombre à diviser
4. Répéter jusqu’à ce que le quotient soit 0.
5. Le nombre binaire est constitué des restes, lus **de bas en haut** (du dernier reste obtenu jusqu’au premier)

### Exemple

Nombre décimal `13` :

- 13 ÷ 2 = 6 → reste 1
- 6 ÷ 2 = 3 → reste 0
- 3 ÷ 2 = 1 → reste 1
- 1 ÷ 2 = 0 → reste 1 (et on s’arrête car le quotient est 0)

On lit les restes de bas en haut → `1101`. 
Donc `13₁₀ = 1101₂`.

![[Système/Images/decimal-binary-conversion.png|500]][^1]

[^1]: Source : [codefinity](https://codefinity.com/fr/courses/v2/0de038c2-b2a2-4df1-9e55-d563c652cd11/71950538-0618-424b-85de-616212cae680/5b3c1d37-8f6e-40d7-a394-ba2c268b6eda)