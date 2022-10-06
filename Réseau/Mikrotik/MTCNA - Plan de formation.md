*En cours de rédaction*

# Module 1: Introduction
- À propos de MikroTik
	- Description de RouterOS
		- [Fonctionnalités](https://help.mikrotik.com/docs/display/ROS/Software+Specifications)
	- Description de RouterBoard
- Premier accès au routeur
	- WinBox et MAC-WinBox
	- WebFig et Quick Set
	- [Configuration par défaut](https://help.mikrotik.com/docs/display/ROS/Default+configurations)
- Interface en ligne de commande (CLI) RouterOS
	- Câble null modem
	- SSH et Telnet
	- Terminal sous WinBox / WebFig
- Utilisation de l'interface en ligne de commande (CLI) RouterOS
	- Tabulation, double tabulation, « ? », navigation
	- Historique des commandes et ses avantages
- Configuration initiale (accès internet)
	- WAN DHCP client
	- Adresse IP LAN et passerelle par défaut
	- Pare-feu de base, NAT
- Mise à niveau RouterOS
	- Modules de mises à jour
	- Les moyens d'effectuer une mise à niveau
	- Mise à jour du firmware RouterBOOT
- Identité du routeur
- Gérer les connexions RouterOS
- Gérer les services de RouterOS
- Gestion des sauvegardes de configuration
	- [Enregistrement et restauration d'une sauvegarde](https://help.mikrotik.com/docs/display/ROS/Backup)
	- Différences entre une sauvegarde et un export (.rsc)
	- Modification d'un export
- [Réinitialisation d'un appareil RouterOS](https://help.mikrotik.com/docs/display/ROS/Reset+Button)
- [Réinstallation d'un appareil RouterOS (Netinstall)](https://help.mikrotik.com/docs/display/ROS/Netinstall)
- [Niveaux de licences RouterOS](https://help.mikrotik.com/docs/display/ROS/RouterOS+license+keys#RouterOSlicensekeys-LicenseLevels)
- Sources d'information supplémentaires
	- wiki.mikrotik.com
	- forum.mikrotik.com
	- mum.mikrotik.com
	- Distributeur et support consultant
	- support@mikrotik.com
- **TP module 1**

# Module 2: DHCP
- Serveur et client DHCP
	- Client DHCP
	- Configuration du serveur DHCP
	- Gestion des allocations d'adresses
	- Configuration réseau du serveur DHCP
- ARP: Address Resolution Protocol
	- Modes ARP
	- Table ARP de RouterOS
- **TP module 2**

# Module 3: Pont
- Bridging (Pontage réseau)
	- Concepts et paramètres du pont réseau
	- Création de ponts
	- Ajout de ports aux ponts
- Pontage de réseaux sans fil
	- Pont de station
- **TP module 3**

# Module 4: Routage
- Vue d'ensemble de routage
	- Concepts de routage
	- Drapeaux de route
- Routage statique
	- Création d'itinéraires
	- Route par défaut
	- Routes dynamiques
	- Mise en œuvre de routage statique dans un réseau simple
- **TP module 4**

# Module 5: Sans fil
- Concepts 802.11 a/b/g/n/ac
	- Fréquences (bandes, canaux), débuts de données/chaines (puissance tx, sensibilité rx, règlementation du pays)
- Installation d'une simple liaison sans fil
	- Configuration d'un point d'accès
	- Configuration d'une station
- Sécurité et chiffrement sans fil
	- Access-list
	- Connect-list
	- Default Authenticate
	- Default Forward
	- WPA-PSK, WPA2-PSK
	- WPS accept, et clients WPS
- Outils de surveillance
	- Snooper
	- Registration table (Table d'enregistrement)