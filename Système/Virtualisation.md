# Virtualisation
- [Wikipedia](https://fr.wikipedia.org/wiki/Virtualisation)

De manière très simplifiée, un hyperviseur (logiciel de virtualisation) peut-être vu comme un programme capable d'interpréter du code habituellement lisible par un [[BIOS & UEFI]], et de lancer un chargeur d'amorçage dans un environnement isolé (Une machine virtuelle, ou « VM » pour Virtual Machine). A part sous certaines conditions et configurations bien précises, les VM ne partagent rien entre elles ni avec le système qui execute l'hyperviseur. Les ressources matérielles (espace disque dur, mémoire RAM, …) sont réservées et allouées par l'hyperviseur pour une VM. Tant qu'une VM est démarrée, ses ressources sont bloquées pour elle.

Le système virtualisé est appelé « invité » (ou « guest » en Anglais), tandis que le système qui execute l'hyperviseur est appelé « hôte » (ou « host »).

## Hyperviseur de type 1
- Environnement d'entreprise
- S'installe sur les ressources matérielles directement.
- Noyau très léger et optimisé pour donner accès à l'architecture matérielle physique, aux machines virtuelles.
- Ne permet pas d'utiliser la machine hôte pour autre chose que de la virtualisation.
- Hyperviseurs connus:
	- Proxmox VE ([Wikipedia](https://fr.wikipedia.org/wiki/Proxmox_VE))
	- VMware ESXi / VMware vSphere ([Wikipedia](https://fr.wikipedia.org/wiki/VMware_vSphere))
	- Citrix Xen Server ([Wikipedia](https://fr.wikipedia.org/wiki/Xen))
	- Microsoft Hyper-V Server ([Wikipedia](https://fr.wikipedia.org/wiki/Hyper-V))
	- Oracle VM ([Wikipedia](https://fr.wikipedia.org/wiki/Oracle_vm))
	- KVM ([Wikipedia](https://fr.wikipedia.org/wiki/Kernel-based_Virtual_Machine))

![[type-1-hypervisor-diagram.png|600]]


## Hyperviseur de type 2
- Environnement de test, sur ordinateurs personnels.
- S'installe et s'execute sur un système d'exploitation.
- Permet d'utiliser la machine hôte pour faire autre chose en même temps, mais les ressources matérielles réservées restent allouées à une VM en marche.
- Hyperviseurs connus:
	- Microsoft Virtual PC ([Wikipedia](https://fr.wikipedia.org/wiki/VirtualPC))
	- Parallels Desktop ([Wikipedia](https://fr.wikipedia.org/wiki/Parallels_Desktop))
	- VirtualBox ([Wikipedia](https://fr.wikipedia.org/wiki/Oracle_VM_VirtualBox))
	- VMware Fusion/Player/Workstation ([Wikipedia](https://fr.wikipedia.org/wiki/VMware))
	- QEMU ([Wikipedia](https://fr.wikipedia.org/wiki/QEMU))

![[type-2-hypervisor-diagram.png|600]]