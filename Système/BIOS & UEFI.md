# BIOS & UEFI

## BIOS (Basic Input/Output System)
Le BIOS est un micrologiciel (*firmware*) permettant d'effectuer des opérations de bases lorsqu'un ordinateur est mis en route:
- Initialisation des composants de la carte mère
- Identification des clés USB, disques dur, lecteurs CD
- Chargements des paramètres d'amorçage
- Auto-test (*POST*^[ABD])
- Lancement du chargeur d'amorçage

Une fois que le BIOS a fini ses affaires, il va lire le [MBR](#MBR) des périphériques de stockage configurés et chargera le premier code d'amorçage trouvé.

## MBR
La table de partitionnement MBR^[Master Boot Record] (créée en 1980) est le premier **secteur** adressable d'un disque dur. Historiquement un secteur faisant 512 octets, le MBR a une taille fixe de 512 octets.

| Adresse | Description | Taille (octet) |
|:-------:|:-----------:|:--------------:|
| 0 | Routine d'amorçage | 440 |
| 440 | Signature (facultatif) | 4 |
| 444 | NUL (0x0000) | 2 |
| 446 | Table des partitions (4 x 16 octets) | 64 |
| 510 | Signature MBR (`0x55 0xAA`) | 2 |

> $440 + 4 + 2 + 64 +2 = 512$

Le taille maximum du code d'amorçage est de 440 octets et contient les instructions nécessaire au [chargeur d'amorçage](#chargeur%20d%27amor%C3%A7age) pour démarrer le système d'exploitation.

La taille d'une partition s'exprime sur 4 octets (32 bits) et se limite donc à 2 To. Pour palier à ces limitations, Intel a créé (fin des années 90) le nouveau format [GPT](#GPT) qui fait partie des spécifications de [UEFI](#UEFI).

## UEFI
Unified Extensible Firmware Interface

### GPT
GUID Partition Table
![[GUID_Partition_Table_Scheme.svg|400]]


## Chargeur d'amorçage
- NTLDR (NT LoaDeR)
- LILO (LInux LOader)
- GRUB (GRand Unified Bootloader)
- Isolinux/Syslinux (CD/Linux)

Chargement du noyau, d'un système de fichier racine ([initrd](https://fr.wikipedia.org/wiki/Initrd#initrd) ou [initramfs](https://fr.wikipedia.org/wiki/Initrd#initramfs) pour Linux), et enfin: démarrage (boot).