Le processeur (ou CPU), est un composant essentiel de l'ordinateur, responsable de l'exécution de tâches diverses.

# 1. Architectures
Les processeurs peuvent varier en fonction de leur architecture, ce qui influence leurs performances et leur compatibilité. Une architecture désigne l'ensemble des principes, des concepts et des spécifications qui déterminent le fonctionnement d'un processeur. Elle inclut des éléments tels que le jeu d'instructions, les modes de fonctionnement, l'organisation des unités fonctionnelles, et la manière dont les données sont traitées. Différentes architectures, comme [[#IA-32 et x86]], [[#ARM]] ou MIPS, répondent à des besoins variés, allant des ordinateurs personnels aux mobiles en passant par les appareils réseau.

## IA-32 et x86
Abréviation de _Intel Architecture 32 bits_ (communément appelée i386) est la version 32 bits de l'architecture du [jeu d'instructions x86](https://fr.wikipedia.org/wiki/Jeu_d%27instructions_x86), conçue par Intel et implémentée pour la première fois dans le microprocesseur [80386](https://fr.wikipedia.org/wiki/Intel_80386) en 1985. Par conséquent, le terme « IA-32 » peut être utilisé comme métonymie pour désigner toutes les versions x86 qui prennent en charge le calcul 32 bits. Par extension, « x86 » désigne aujourd'hui (abusivement) l'architecture IA-32.
<small><a href="https://fr.wikipedia.org/wiki/X86" target="_blank">Voir plus…</a></small>

## x86-64 ou AMD64 (et Intel 64)
Extension 64 bits du [jeu d'instructions x86](https://fr.wikipedia.org/wiki/Jeu_d%27instructions_x86), originellement annoncée par AMD en 1999. Ce n'est qu'en 2003 que AMD implémentera sa spécification dans leur processeur Opteron, après l'échec commercial de l'[[#IA-64]] d'Intel. Elle permet l'utilisation d'une plus grande quantité de mémoire et améliore les performances des applications.

L'implémentation d'Intel de cette architecture est nommée **Intel 64** ou encore **EM64T**^[_**E**xtended **M**emory **64**-bit **T**echnology_]. Ce n'est pas strictement le même jeu d'instruction implémenté par Intel car x86-64 est sous licence AMD, mais les compilateurs savent faire des programmes compatibles avec ces 2 architectures.

On retrouve aussi l'appellation « x64 » qui est un abus de langage puisqu'elle ne se réfère à rien (ni une famille, ni un numéro, ni un code).
<small><a href="https://fr.wikipedia.org/wiki/X64" target="_blank">Voir plus…</a></small>

## IA-64
Abréviation de _Intel Architecture 64 bits_, il s'agit d'une architecture implémentant un jeu d'instruction 64 bits développée par Intel en 2001 complètement différent de [[#IA-32 et x86|IA-32]] et [[#x86-64 ou AMD64 (et Intel 64)|x86-64]] et non compatible avec ceux-ci. Son exploitation étant trop compliquée, les processeurs IA-64 n'ont jamais percé jusqu'à finalement être totalement abandonnés par Intel en 2020.
<small><a href="https://fr.wikipedia.org/wiki/IA-64" target="_blank">Voir plus…</a></small>

## ARM
L'architecture ARM^[Advanced RISC Machines] développée par Acorn Computers est introduite sur le marché en 1990. ARM est connu pour ses [systèmes sur une puce (SoC)](https://fr.wikipedia.org/wiki/Système_sur_une_puce) intégrant un système complet (Microprocesseur, Processeur graphique, Contrôleurs de périphériques, …) sur une seule puce, ils sont économes en énergie ce qui les rend idéal pour l'informatique embarquée comme les portables et les tablettes.

En Juin 2020, Apple annonce vouloir faire la transition (complète de ses appareils) de Intel vers ARM, pour la terminer en Mars 2022 avec les puces de la série M (M1, M2, …) appelées « Apple Silicon ». [Microsoft s'est aussi intéressé à ARM](https://en.wikipedia.org/wiki/Windows_on_ARM) pour équiper ses tablettes Surface depuis Windows 8.
<small><a href="https://fr.wikipedia.org/wiki/Architecture_ARM" target="_blank">Voir plus…</a></small>

# 2. Registres
Les registres sont de petites zones de stockage situées à l'intérieur du processeur. Ils sont utilisés pour stocker temporairement des données et des instructions en cours de traitement. Les registres sont très rapides, ce qui permet au processeur d'accéder aux informations rapidement.

La taille des registres est souvent liée à l'architecture du processeur. Par exemple, un processeur 32 bits dispose généralement de registres de 32 bits, tandis qu'un processeur 64 bits a des registres de 64 bits.

# 3. Cœurs et Fils d'Exécution
Un cœur est une unité de traitement indépendante au sein d'un processeur. Chaque cœur peut exécuter des instructions de manière simultanée, ce qui permet au processeur de gérer plusieurs tâches en parallèle. Par exemple, un processeur quadricœur a quatre cœurs, ce qui lui permet de traiter quatre tâches distinctes à la fois. Cela améliore considérablement les performances, surtout dans les applications multitâches ou les logiciels lourds.

Un fil d'exécution est une séquence d'instructions qui peut être gérée indépendamment par un processeur. Un cœur peut généralement gérer plusieurs fils d'exécution grâce à une technologie appelée _Hyper-Threading_ (sur les processeurs Intel) ou _Simultaneous MultiThreading_ (SMT, sur les processeurs AMD). Cela permet à un cœur d'alterner rapidement entre plusieurs fils d'exécution, donnant l'impression qu'il exécute plusieurs tâches simultanément, même s'il ne le fait pas réellement.