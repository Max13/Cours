# DHCP (Dynamic Host Configuration Protocol)
C'est un protocole de réseau utilisé pour simplifier l'administration des réseaux en automatisant l'attribution de certaines configurations (Adressage IP, Routage, Mises à jour, …), plutôt que de le faire manuellement chaque fois qu'un équipement se connecte à un réseau.

[[#1. Discover (Recherche)|D]] [[#2. Offer (Offre)|O]] [[#3. DHCP Request (Demande d'adresse)|R]] [[#Acknowledgement (Confirmation)|A]]

## Rôle et Fonctionnement
Le fonctionnement du DHCP repose sur le modèle client-serveur. Lorsqu'un appareil (**client**) se connecte à un réseau, il envoie une requête pour obtenir une adresse IP et d'autres paramètres de configuration réseau. Un **serveur DHCP** reçoit cette demande et répond en fournissant les informations demandées :

### 1. Discover (Recherche)
Envoi d'un message **DHCP Discover** sur le réseau pour découvrir le ou les serveurs DHCP disponibles. Le client n'ayant pas (à sa première connexion) d'adresses IP, le message est envoyé en **[broadcast](https://fr.wikipedia.org/wiki/Broadcast_(informatique))**.
   
### 2. Offer (Offre)
Le serveur DHCP reçoit la demande et répond avec un message **DHCP Offer**, qui contient une adresse IP disponible ainsi que d'autres informations de configuration (masque de sous-réseau, passerelle, DNS, etc.).

### 3. DHCP Request (Demande d'adresse)
Le client, après avoir reçu plusieurs offres potentielles de serveurs DHCP, choisit l'offre qui lui convient et envoie un message **DHCP Request** pour faire demander l'adresse IP et la configuration proposées.

### 4. Acknowledgement (Confirmation)
Le serveur DHCP envoie alors un message **DHCP Acknowledgement**, confirmant que l'adresse IP a été attribuée au client pour une période donnée.

### (Bonus) Renouvellement
Avant la fin de la période de validité de l'adresse IP (Bail DHCP), le client envoie une nouvelle demande de renouvellement pour conserver cette adresse. Si le serveur DHCP l'accepte, l'adresse est renouvelée.

## Paramètres Configurés par le DHCP
Le DHCP peut envoyer différentes configurations réseau :
- **Adresse IP** : L'adresse IP unique attribuée à l'appareil.
- **Masque de sous-réseau** : Indique quelle partie de l'adresse IP représente le réseau et quelle partie représente l'hôte.
- **Passerelle par défaut** : L'adresse du routeur ou de la passerelle par défaut, permettant à l'appareil d'accéder à d'autres réseaux (comme Internet).
- **Serveurs DNS** : Les adresses des serveurs DNS que l'appareil doit utiliser pour résoudre les noms de domaine en adresses IP.
- **Serveurs WINS** : Serveurs utilisés pour la résolution des noms NetBIOS dans les réseaux Windows.
- **Option de routage** : Information sur la manière dont les paquets doivent être routés à travers un réseau.
- **Serveur de temps NTP** : Adresse du serveur de temps utilisé pour la synchronisation horaire.
- **Informations sur le serveur de l'application** : Par exemple, l'adresse des serveurs de gestion de téléphonie IP ou des services VoIP.
- **Paramètres pour les périphériques spécifiques** : Comme les téléphones IP, les points d'accès Wi-Fi, ou d'autres appareils spécifiques.

## Applications du DHCP au-delà de l'adressage IP
### Téléphones IP
Le serveur DHCP peut fournir non seulement une adresse IP, mais aussi des informations telles que :
   - Le serveur de signalisation SIP (Session Initiation Protocol).
   - Les informations de serveur de configuration ou de mise à jour.

### Routeurs Wi-Fi
Certains équipements réseau, comme les routeurs Wi-Fi, peuvent récupérer l'adresse de leur serveur de gestion, leur permettant de récupérer leur configuration.

### Systèmes Compatibles

Le **DHCP** est un protocole largement compatible et utilisé dans de nombreux systèmes. Il fonctionne sur presque tous les appareils et systèmes d'exploitation modernes qui sont connectés à un réseau IP. Voici quelques-uns des systèmes compatibles :

- Systèmes d'exploitation de bureau : Tous
- Téléphones IP : Tous
- Équipements réseau : Tous (s'ils sont manageables, les commutateurs non-manageable n'ont pas besoin de configuration IP par exemple)
- Dispositifs IoT (Internet of Things) : De nombreux appareils connectés (comme les caméras de surveillance, les thermostats intelligents, les assistants vocaux) utilisent également le DHCP pour obtenir une adresse IP et se configurer automatiquement.