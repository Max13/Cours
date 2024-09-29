La mémoire vive, également connue sous le nom de **RAM**^[Random Access Memory], est un type de mémoire utilisée par un ordinateur pour stocker temporairement les données et les programmes en cours d'exécution. Contrairement à d'autres formes de stockage, comme les disques durs, la mémoire vive permet un accès rapide et direct aux informations, ce qui est crucial pour le bon fonctionnement du système.

## Fonctionnement de la mémoire vive
- **Accès rapide** : La RAM est conçue pour permettre un accès très rapide aux données. Contrairement à un disque dur, qui peut nécessiter du temps pour localiser et lire des données, la RAM permet au [[Le Processeur|processeur]] d'accéder à n'importe quelle adresse mémoire instantanément.

- **Structure** : La mémoire vive est composée de millions de cellules de mémoire organisées en lignes et colonnes. Chaque cellule contient un bit de donnée, qui peut être soit un 0 soit un 1. Les cellules sont regroupées en octets (8 bits), et chaque groupe a une adresse.

- **Écriture et lecture** : Lorsque vous lancez un programme, les données nécessaires sont transférées depuis le stockage (disque dur) vers la mémoire vive. [[Le Processeur]] peut alors lire et écrire des informations directement dans la RAM, ce qui améliore considérablement la vitesse de traitement.

- **Multi-tâches** : La RAM permet d'exécuter plusieurs applications simultanément. Plus il y a de mémoire disponible, plus il est possible d'ouvrir de programmes ou de traiter de grandes quantités de données sans ralentissement.

## Volatilité de la mémoire vive
Elle est dite **volatile** car elle perd toutes les données qu'elle contient lorsqu'elle n'est plus sous tension. Pour cette raison elle est principalement utilisée pour des opérations temporaires, comme le stockage de programmes en cours d'exécution et des données qui doivent être traitées rapidement. Une fois que vous fermez un programme ou éteignez l'ordinateur, ces informations deviennent inaccessibles.

> [!note]
> En réalité, la mémoire vive ne **perd** pas les données lorsqu'elle est hors tension. En réalité, lorsque [[Le Processeur]] y enregistre des informations, il retient l'adresse des zones mémoires utilisées et lorsqu'il n'en a plus besoin ou est mis hors tension, c'est en réalité les références à ces zones mémoires qui est perdues.
> 
> Une personne malveillante pourrait récupérer toutes les données temporaires qui ont été stockées dans une barrette de RAM, mais c'est une opération compliquée car les données d'un même programme ne sont pas nécessairement enregistrées de manière contigüe.