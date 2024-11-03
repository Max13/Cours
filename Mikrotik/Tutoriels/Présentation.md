# MikroTik - Qu'est-ce que c'est ?
Fondée en 1996, *Mikrotīkls SIA* (plus connue sous le nom **MikroTik** à l'internationale) est une entreprise lettone spécialisée dans le développement de solutions de connectivité Internet. Forte d’une expertise unique en systèmes de routage, MikroTik propose une gamme complète de matériel conçue pour répondre aux besoins des fournisseurs d'accès Internet, des entreprises de télécommunications à travers le monde, ou encore des clients finaux.

En 1997, MikroTik a lancé RouterOS, un système logiciel innovant offrant une flexibilité, une stabilité et des fonctionnalités avancées de contrôle, répondant aux exigences de divers types d'infrastructures réseau. Face au succès grandissant de cette solution, MikroTik a introduit sa propre gamme de matériel en 2002 sous la marque RouterBOARD, renforçant ainsi sa position de leader dans les technologies réseau.

Aujourd'hui, MikroTik opère depuis Riga, en Lettonie, avec une équipe de plus de 280 collaborateurs engagés dans l'innovation et l'excellence. Nos solutions sont désormais utilisées dans la plupart des pays, connectant le monde grâce à des technologies réseau de pointe.


![[map_lv.jpg]]

## RouterOS
Il s'agit du système d'exploitation conçu par MikroTik pour transformer n'importe quel RouterBOARD en une solution réseau complète et flexible. Il offre une vaste gamme de fonctionnalités avancées pour la gestion et le contrôle des réseaux :

### Routage avancé
   - Routage statique et dynamique : Prise en charge de divers protocoles de routage comme BGP, OSPF et RIP, permettant une configuration flexible et adaptée aux grandes infrastructures.
   - Routage par politique (Policy-Based Routing) : Permet de définir des règles de routage basées sur des critères spécifiques pour un contrôle personnalisé du trafic.

### Firewall et Sécurité
   - Filtrage des paquets : Contrôle du trafic entrant et sortant avec des règles de filtrage avancées.
   - NAT^[Network Address Translation] : Options de translation d'adresses pour gérer les communications avec des réseaux internes et externes.
   - Mangle : Permet de marquer des paquets ou des connexions selon des critères définis, comme l'adresse IP, le protocole ou le port, afin de faciliter la gestion avancée du trafic comme le routage basé sur des politiques (Policy-Based Routing), la gestion de la bande passante et la priorisation (QoS).

### Gestion de la bande passante et QoS^[Quality of Service]
   - File d'attente et gestion de la bande passante : Contrôle du trafic pour assurer une répartition optimale de la bande passante.
   - Priorisation du trafic : Classement des types de trafic pour garantir une meilleure performance sur les applications critiques, comme la VoIP et la vidéo.
   - Traffic Shaping : Ajustement de la forme du trafic pour éviter la congestion et maintenir une qualité de service élevée.

### Tunnels VPN^[Virtual Private Network]
   - Support multi-protocole : IPsec, PPTP, L2TP, OpenVPN, SSTP et Wireguard pour créer des connexions sécurisées entre différents sites.
   - Transit opérateur : MPLS, VPLS, …

### Portail captif / Hotspot
   - Portail captif intégré : Permet la connexion des utilisateurs à travers un portail d'authentification personnalisé, idéal pour les environnements publics comme les cafés ou les hôtels.
   - RADIUS / Dot1X : Permet la délégation de l'authentification aux différents services fournis par RouterOS (Connexion au routeur, VPN, portail captif, WPA Entreprise, …), à un système externe.

### Support de la connectivité sans fil (Wi-Fi)
   - Points d'accès et stations sans fil : Configuration individuelle ou centralisée des périphériques sans-fil en point d'accès (diffuse un réseau) ou station (se connecte à un réseau).
   - Sécurité sans fil avancée : Gestion de la sécurité des réseaux Wi-Fi avec WPA, WPA2, WPA3, personnel ou entreprise, sans oublier OWE^[Opportunistic Wireless Encryption]
   - Contrôle de fréquence et gestion des interférences : Options de configuration des canaux pour minimiser les interférences et maximiser la couverture.

### Monitoring et outils de diagnostic
   - Graphiques et rapports en temps réel : Surveillance des performances réseau en temps réel pour un aperçu précis de l’utilisation de la bande passante, du CPU, et des statistiques de réseau.
   - Outils de diagnostic intégrés : Utilitaires comme Ping, Traceroute, Bandwidth Test, et Torch pour faciliter le dépannage des réseaux.
   - SNMP^[Simple Network Management Protocol] : Support pour SNMP (v1, v2, v3), permettant une intégration facile dans les systèmes de gestion réseau externes.

### Automatisation et Scripts
   - Tâches planifiées : Programmation de tâches automatisées pour la gestion et la maintenance du réseau.
   - Scripts avancés : Possibilité de créer des scripts personnalisés pour automatiser des tâches complexes, simplifier la gestion du réseau et optimiser les opérations.

### Gestion et Configuration à distance
   - Interface Web et Winbox : Accès au système via une interface Web intuitive ou via Winbox, un utilitaire de configuration graphique spécifique à MikroTik.
   - API et CLI : Interface en ligne de commande (SSH, Telnet et Console) et API pour une intégration et une gestion avancées via des scripts ou des applications tierces.
   - Cloud Management : Possibilité d'intégration avec des services cloud pour gérer et surveiller des appareils MikroTik sur des sites distants.

RouterOS se distingue par sa capacité à combiner toutes ces fonctionnalités dans un seul système d'exploitation, offrant une flexibilité et une puissance qui le rendent adapté aux environnements réseau variés, des TPE, PME, aux grandes entreprises et aux FAI.