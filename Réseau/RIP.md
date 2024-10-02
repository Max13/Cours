# RIP : Routing Information Protocol
C'est un protocole de routage dynamique conçu pour déterminer le meilleur chemin pour acheminer des paquets dans les réseaux IP. Apparue dans les années 1980, cette solution convient bien aux réseaux de petite à moyenne taille.

## Caractéristiques principales
RIP est un protocole de **routage à vecteur de distance** utilisant l'[algorithme de Bellman-Ford](https://fr.wikipedia.org/wiki/Algorithme_de_Bellman-Ford). Pour choisir un itinéraire, il se base sur une métrique simple : le **nombre de sauts** (ou hop count). Le seuil de **15 sauts** est défini comme le maximum autorisé, au-delà duquel une destination est jugée inatteignable. Il existe deux versions de RIP : **RIP v1** qui est classful (ne transmet pas d'informations de sous-réseau), et **RIP v2** qui est classless (supporte les sous-réseaux de longueur variable avec VLSM et CIDR).

## Fonctionnement
Chaque routeur sous RIP entretient une table de routage qui répertorie les réseaux connus, les distances associées et la direction (ou le voisin) pour y accéder. RIP effectue des mises à jour périodiques (toutes les **30 secondes**) pour partager sa table avec les voisins, utilisant l'adresse multicast (224.0.0.9 pour RIP v2) ou le broadcast (pour RIP v1). L'algorithme de **Bellman-Ford** est utilisé pour ajuster les chemins optimaux selon le nombre de sauts.

## Limites du Protocole
RIP est limité en termes de **scalabilité** à cause de sa restriction du nombre de sauts, ce qui le rend inadapté aux réseaux complexes. Sa méthode de mise à jour périodique ralentit également le processus de **convergence**, augmentant le temps nécessaire pour que les routeurs aient une vision cohérente du réseau après des modifications. Enfin, il est vulnérable aux **boucles de routage**, bien que des mécanismes tels que le **split horizon** et le **comptage à l'infini** (limité à 16) soient employés pour limiter ces problèmes.

## Avantages et Cas d'Usage
La **simplicité** d’implémentation de RIP le rend approprié pour les réseaux modestes. Il est également largement compatible avec une variété de dispositifs, y compris des équipements plus anciens, ce qui facilite son intégration. Ces caractéristiques permettent d’utiliser RIP dans des scénarios où la complexité du routage doit être minimisée.

## Alternatives
Pour les réseaux plus grands, des protocoles plus performants sont souvent utilisés à la place de RIP. Par exemple, **OSPF** utilise une métrique de coût plus sophistiquée et converge rapidement, tandis que **EIGRP** offre un compromis entre les avantages des routages par vecteur de distance et par état de lien. Pour le routage entre des systèmes autonomes, **BGP** est plus approprié.

## **Conclusion**
RIP est idéal pour les réseaux simples où des solutions de routage avancées ne sont pas nécessaires. Bien qu'il soit limité en termes de capacité et de vitesse de convergence, il reste un protocole d’apprentissage intéressant et un choix pratique pour certains scénarios particuliers. Pour des réseaux de plus grande envergure, des solutions comme OSPF ou BGP sont mieux adaptées.