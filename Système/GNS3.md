# GNS3
`GNS3`^[Graphical Network Simulator-3] est une suite de logiciels permettant de simuler une topologie réseau dans un environnement virtualisé. Elle est constituée de 3 éléments:
- Le client de bureau GNS3, appelée `GNS3` ou `Client GNS3`.
- Le serveur local de GNS3, appelé `gns3 server`.
- La VM GNS3, appelée `GNS3 VM` basée sur `Ubuntu`.

## Pré-requis
- Hyperviseur (Pour Windows et macOS): **VMware** (Workstation Player, Workstation Pro ou Fusion) conseillé. <small>(voir [[Virtualisation]])</small>
- [Installeur GNS tout en un](https://gns3.com/software/download) <small>(Nécessite un compte)</small>
- [La machine virtuelle GNS3](https://gns3.com/software/download-vm) <small>(Optionnelle pour Windows car inclut dans l'installeur)</small>
- [Pour les étudiants d'ITIC Paris](https://gofile.me/6XgKH/fO4SW39UZ)

## Client de bureau
Le client de bureau est un programme permettant de contrôler graphiquement GNS3 dans son ensemble. Il permet de:
- Créer des « appliances », qui sont des « appareil » avec des caractéristiques pré-définis (Disque dur, RAM, nombre d’interfaces réseau, etc…). Techniquement ce sont des machines virtuelles.
- Placer et connecter des « appliances » entre elles ou au réseau externe.
- Démarrer et arrêter des appliances.
- Lancer des terminaux pour se connecter aux appliances.
- […]

Le client de bureau ne contrôle pas directement GNS3 mais plutôt le [Serveur local](#Serveur%20local%20GNS3).

## Serveur local GNS3
Il est en charge de toutes les actions effectuées dans GNS3. Lorsqu’une appliance est créée, le client de bureau indique au serveur local qu’elle appliance il souhaite créer et démarrer, et sur quel système, en local ou sur la [machine virtuelle de GNS3](#GNS3%20VM), puis une fois que le serveur valide l’action, le client affiche le résultat.

## GNS3 VM
Afin d’éviter un maximum d’encombrer la machine hôte, `GNS3` se repose sur une machine virtuelle pour simuler les topologies les plus complexes, comprenant par exemple des services sous Windows ou Linux.

Étant donné que le serveur a besoin d’un environnement connu, GNS3 est livré avec une machine virtuelle Ubuntu. C’est DANS cette machine virtuelle que GNS3 lance les appliances désirées et les connecte entre elles. Lancer une machine virtuelle dans une machine virtuelle s'appelle « de la virtualisation imbriquée » donc la machine hôte doit supporter « VT-X » pour les processeurs Intel ou « AMD-V » pour les processeurs AMD.

Ces options doivent être activées dans le BIOS si ce n’est pas déjà fait, puis dans l’hyperviseur.

Les utilisateurs de Linux, notamment Ubuntu, n'ont pas besoin de la machine virtuelle étant donné que le [Serveur local](#Serveur%20local%20GNS3) peut directement travailler avec le système hôte.

## Tutoriels
- [Google Drive](https://drive.google.com/drive/folders/1HtbuORcTzsO0YnHsUe7eRUnN925MLzpv?usp=sharing) (bit.ly/ttgns3)

## Dépannage
- Windows
	- 1 seule boule (Votre PC) : GNS3 ne voit pas la VM GNS3 sur l'hyperviseur.
	- Boule rouge (🔴) ou carré rouge (🟥) sur GNS3 VM
		- Mettez la souris dessus et lisez le message d'erreur.
	- (Windows) Boule grise (⚪) sur GNS3 VM pendant plus d'une minute après démarrage
		1. Vérifiez que GNS3 VM soit démarrée en ouvrant manuellement l'hyperviseur.
		2. Vérifiez que le port sur lequel GNS3 VM fonctionne est le même que dans les réglages de `GNS3 > Edit > Preferences > GNS3 VM`.
		3. Fermez GNS3 et l'hyperviseur, désactivez les cartes réseau de l'hyperviseur (dans Windows), réactivez les, relancez GNS3.
	- (Windows) Message d'erreur indiquant que « VT-X » ou « AMD-V » doit être activé
		- [Fixing VT-x or AMD-v not available in Windows 11 with VMware WS Pro and Player](https://gns3.com/community/featured/fixing-vt-x-or-amd-v-not-available-in-windows-11-with-vmware-ws-pro-and-player) :
			1. Vérifiez que la virtualisation imbriquée (aussi appelée « VT-X », « AMD-V », « Nested virtualization », ou autre) soit activée dans le BIOS/UEFI.
			2. Désactivez complètement Hyper-V : [VMware (WebArchive)](https://web.archive.org/web/20230313174320/https://kb.vmware.com/s/article/2146361) ou [Broadcom](https://knowledge.broadcom.com/external/article?legacyId=2146361) (C'est le même article)
			3. (Windows 11) Désactivez l'isolation du noyau
			4. (Windows 11) Si rien de tout ça ne fonctionne… Essayez avec VirtualBox.