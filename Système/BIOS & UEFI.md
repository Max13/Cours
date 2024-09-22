# BIOS & UEFI

## Introduction
Lorsqu'un ordinateur démarre, il doit initialiser ses composants matériels et charger un système d'exploitation pour être opérationnel. Cette phase critique repose sur des systèmes de micrologiciels (_firmware_) comme le [[#BIOS]] et l'[[#UEFI]], qui gèrent la configuration matérielle et le démarrage. Nous explorerons ici les différences et les fonctions essentielles du [[#BIOS]], de l'[[#UEFI]], ainsi que des formats d'amorçage tels que le [[#MBR]] et le [[#GPT]], et enfin, nous examinerons les chargeurs d'amorçage.

## BIOS
Le **BIOS**^[Basic Input/Output System] est un micrologiciel (_firmware_) installé directement sur la carte mère d'un ordinateur. Son rôle est de préparer la machine pour qu'elle puisse lancer le système d'exploitation, en effectuant plusieurs opérations fondamentales :

- **Initialisation matérielle** : il active et teste les composants matériels comme le processeur, la mémoire vive (RAM), et les périphériques connectés (claviers, disques durs, etc…).
- **Identification des périphériques de stockage** : le BIOS détecte les disques durs, clés USB, lecteurs CD/DVD pour permettre l'amorçage.
- **Chargement des paramètres d'amorçage** : il détermine l'ordre des périphériques à partir desquels l'ordinateur doit tenter de démarrer.
- **Auto-test POST (Power-On Self Test)** : il vérifie que le matériel fonctionne correctement avant de continuer.
- **Lancement du chargeur d'amorçage** : une fois les tests et l'initialisation terminés, le BIOS passe la main au chargeur d'amorçage (situé sur le [[#MBR]]) pour démarrer le système d'exploitation.

### MBR
Le **MBR**^[Master Boot Record] est un standard de partitionnement des disques durs, introduit en 1980. Il s'agit du tout premier secteur adressable d'un disque dur, avec une taille fixe de 512 octets. Il contient des informations essentielles pour le démarrage de l'ordinateur, notamment la routine d'amorçage et les informations sur la table des partitions.

| Adresse |             Description              | Taille (octet) |
| :-----: | :----------------------------------: | :------------: |
|    0    |          Routine d'amorçage          |      440       |
|   440   |        Signature (facultatif)        |       4        |
|   444   |             NUL (0x0000)             |       2        |
|   446   | Table des partitions (4 x 16 octets) |       64       |
|   510   |     Signature MBR (`0x55 0xAA`)      |       2        |

> $440 + 4 + 2 + 64 +2 = 512$

La **routine d'amorçage** (440 octets) contient les instructions nécessaires pour lancer le [[#chargeurs d'amorçage]] qui démarre le système d'exploitation. Cependant, le MBR présente des limitations :

- Il ne supporte que des disques d'une taille maximale de 2 To, car la taille des partitions est exprimée sur 32 bits, par blocs de 512 octets.
- Il ne peut gérer que 4 partitions primaires.

Pour surmonter ces contraintes, Intel a introduit le format **[[#GPT]]** dans les années 90, associé à la spécification **[[#UEFI]]**.

## UEFI
L'**UEFI**^[Unified Extensible FIrmware] est le successeur du [[#BIOS]], offrant plus de fonctionnalités et une interface plus moderne. Son rôle reste le même : initialiser les composants matériels et amorcer le système d'exploitation, mais il améliore plusieurs aspects techniques :

- **Interface graphique** : l'UEFI peut afficher des interfaces graphiques et prendre en charge la navigation à la souris, contrairement au [[#BIOS]] qui fonctionne via des interfaces textuelles rudimentaires.
- **Compatibilité avec [[#GPT]]** : l'UEFI utilise le format **[[#GPT]]** qui permet de gérer des disques de grande taille (plus de 2 To) et de créer jusqu'à 128 partitions.
- **Amorçage sécurisé (Secure Boot)** : l'UEFI peut vérifier la signature numérique du système d'exploitation pour s'assurer qu'il n'a pas été altéré.

### GPT
Le **GPT**^[GUID Partition Table] est un système de partitionnement moderne qui, contrairement au [[#MBR]], peut gérer des disques beaucoup plus volumineux et offrir une plus grande flexibilité dans la gestion des partitions. Il fait partie intégrante de la spécification [[#UEFI]] et permet une meilleure gestion de l'espace disque pour les systèmes récents.

#### Avantages du GPT par rapport au [[#MBR]] :

- **Support des disques de plus de 2 To**.
- **Nombre quasi-illimité de partitions** (généralement 128 partitions contre 4 dans le [[#MBR]]).
- **Fiabilité accrue** : Le GPT stocke plusieurs copies de la table des partitions à différents endroits du disque, réduisant les risques de corruption des données.

![[GUID_Partition_Table_Scheme.svg|400]]


## Chargeurs d'amorçage
Une fois que le [[#BIOS]] ou l'[[#UEFI]] a terminé son travail, il passe le relais au **chargeur d'amorçage**. Celui-ci est responsable de charger le noyau du système d'exploitation et de démarrer l'ordinateur.

### Exemples de chargeurs d'amorçage :

- **NTLDR**^[NT LoaDeR] : Utilisé par les anciennes versions de Windows (jusqu'à Windows XP).
- **BCD**^[Boot Configuration Data] : Remplaçant de NTLDR (à partir de Windows Vista et Windows Server 2008)
- **LILO**^[LInux LOader] : un ancien chargeur d'amorçage pour Linux, aujourd'hui rarement utilisé.
- **GRUB**^[GRand Unified Bootloader] : un chargeur d'amorçage populaire pour [[Linux]], capable de gérer plusieurs systèmes d'exploitation et très flexible.
- **Syslinux/Isolinux** : utilisé principalement pour les systèmes Linux démarrant à partir de supports amovibles comme les CD ou clés USB.

Ces chargeurs d'amorçage ont pour mission de charger le **noyau** du système d'exploitation, puis de monter le système de fichiers racine (via [initrd](https://fr.wikipedia.org/wiki/Initrd#initrd) ou [initramfs](https://fr.wikipedia.org/wiki/Initrd#initramfs) pour [[Linux]]) et de lancer enfin le système d'exploitation complet.