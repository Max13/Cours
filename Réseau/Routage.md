# Qu'est-ce qu'une route en réseau ?

Une route désigne le chemin qu'un paquet de données emprunte pour se rendre d'un point à un autre dans un réseau, en passant par quel dispositif (généralement un routeur).

ℹ️ _Route = Destination + Passerelle_
La destination étant l'adresse d'un réseau et son masque (ou d'une machine [/32]), la passerelle étant le routeur par lequel passer pour l'atteindre.

## Importance des routes
Les routes sont cruciales pour :
- **Optimiser la transmission des données** : Assurer que les paquets prennent le chemin le plus efficace.
- **Gérer la congestion** : Éviter les goulots d'étranglement en redirigeant le trafic.
- **Assurer la redondance** : Offrir des chemins alternatifs en cas de défaillance d'un lien.

## La table de routage
C'est une base de données qui contient la liste des routes connues par un routeur.

### Contenu
- **Destination** : Le réseau de destination (et son masque).
- **Passerelle (ou next hop)** : L'adresse IP du routeur suivant sur le chemin vers la destination.
- **Interface** : L'interface réseau par laquelle les paquets doivent être envoyés, cette information est ==généralement déterminée== par le routeur grâce à l'adresse de la passerelle.
- **Distance** : Un indicateur de la « distance » ou du coût associé à cette route (peut inclure des critères comme la bande passante ou la latence).

> [!info]
> Dès lors qu'on assigne une adresse IP à une interface, la table de routage de l'appareil contient au minimum une route pour ce réseau.

![[TP_Routage-statique_Ex1.jpg]]

| PC1 | Destination      | Passerelle    | Interface | Coût |
| :-: | :--------------- | :------------ | :-------: | :--: |
|  1  | `192.168.1.0/30` | eth0          |  *eth0*   |  0   |
|  2  | `0.0.0.0/0`      | `192.168.1.2` |  *eth0*   |  1   |

| R1  | Destination      | Passerelle | Interface | Coût |
| :-: | :--------------- | :--------- | :-------: | :--: |
|  1  | `192.168.1.0/30` | ether1     | *ether1*  |  0   |
|  2  | `192.168.2.0/30` | ether2     | *ether2*  |  0   |

| R2  | Destination      | Passerelle | Interface | Coût |
| :-: | :--------------- | :--------- | :-------: | :--: |
|  1  | `192.168.2.0/30` | ether1     | *ether1*  |  0   |
|  2  | `192.168.3.0/30` | ether2     | *ether2*  |  0   |

| PC2 | Destination      | Passerelle    | Interface | Coût |
| :-: | :--------------- | :------------ | :-------: | :--: |
|  1  | `192.168.3.0/30` | eth0          |   eth0    |  0   |
|  2  | `0.0.0.0/0`      | `192.168.3.1` |   eth0    |  1   |

### Fonctionnement
Lorsqu'un paquet arrive à un routeur :
1. Le routeur examine l'adresse de destination du paquet.
2. Il consulte sa table de routage pour trouver la meilleure route vers la destination. Il analyse les destinations connues possibles en partant des destinations les plus petites jusqu'à la plus grande, éventuellement la destination par défaut `0.0.0.0/0`.
3. Il transmet le paquet à l'interface spécifiée, en direction de la passerelle suivante indiquée dans la route correspondante.

## Protocoles de routage
Les routes peuvent être apprises de différentes manières, notamment via :
- **Protocoles de routage statiques** : Les routes sont configurées manuellement et ne changent pas, sauf si l'administrateur les modifie.
- **Protocoles de routage dynamiques** : Ces protocoles permettent aux routeurs d'échanger des informations sur les routes. Exemples : RIP, OSPF, BGP.