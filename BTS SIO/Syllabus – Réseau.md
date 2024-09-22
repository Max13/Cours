### **Syllabus BTS SIO – Réseau**

---

### **0. La machine et ses composants**
- **Durée :** 1 jour
- **Contenu :** Introduction à ce qu'est un PC, ses composants, à quoi ils servent
- **Évaluations :** Kahoot logique durant la séance

---

### **1. Les bases des réseaux informatiques**
- **Durée :** 2 semaines
- **Objectifs d'apprentissage :**
  - Comprendre les principes fondamentaux des réseaux informatiques, les couches OSI et TCP/IP.
  - Apprendre les bases des communications réseau, des protocoles, et des architectures physiques.
  
- **Contenu détaillé :**
  - **Théorie :**
    - Modèle OSI : Description des 7 couches et des responsabilités de chaque couche.
    - Modèle TCP/IP : Différences avec OSI, fonctionnement détaillé des 4 couches.
    - Notions de commutation, routage, NAT (Network Address Translation), sous-réseaux.
    - Présentation des câblages (RJ45, fibre optique) et des dispositifs de connexion (hubs, switches, routeurs, passerelles).
  - **Pratique :**
    - Configuration d’un réseau de base avec différentes classes d’adresses IP (IPv4 et IPv6).
    - Utilisation de commandes réseau de base (ping, traceroute, ipconfig/ifconfig, netstat).

- **Évaluations :**
  - QCM sur les modèles OSI et TCP/IP.
  - TP : Mise en place d’une communication réseau entre deux PC via un switch.

---

### **2. Adressage IP et sous-réseaux**
- **Durée :** 2 semaines
- **Objectifs d'apprentissage :**
  - Maîtriser l’adressage IP, les calculs de sous-réseaux, et l’utilisation des masques de sous-réseau.
  
- **Contenu détaillé :**
  - **Théorie :**
    - Adressage IP v4 : Classes d’adresses, adressage privé vs public, NAT.
    - Masques de sous-réseau : Concepts, calculs de masques, VLSM (Variable Length Subnet Mask).
    - Adressage IP v6 : Format, avantages, configuration et transition avec IPv4.
    - CIDR (Classless Inter-Domain Routing) et calculs de sous-réseaux.
  - **Pratique :**
    - Calculs manuels de sous-réseaux, création de tableaux de sous-réseaux.
    - Configuration IP manuelle sur les hôtes, vérification avec `ipconfig`, `ifconfig`.
    - Implémentation et test d'un réseau en utilisant plusieurs sous-réseaux.

- **Évaluations :**
  - Exercice de calculs de sous-réseaux.
  - TP : Configuration et vérification des adresses IP dans un environnement simulé.

---

### **3. Commutation et VLANs**
- **Durée :** 3 semaines
- **Objectifs d'apprentissage :**
  - Apprendre à configurer des commutateurs et comprendre le concept des VLANs.
  
- **Contenu détaillé :**
  - **Théorie :**
    - Fonctionnement des commutateurs (switching) : Table MAC, ARP (Address Resolution Protocol), Spanning Tree Protocol (STP).
    - Virtual Local Area Networks (VLANs) : Concepts, avantages, implémentation.
    - Protocoles associés : IEEE 802.1Q, VLAN Trunking Protocol (VTP), Inter-VLAN routing.
  - **Pratique :**
    - Configuration de VLANs sur des commutateurs Cisco (via CLI).
    - Configuration d'un Trunk pour la communication entre VLANs.
    - Simulation de VLANs sur Packet Tracer ou GNS3.

- **Évaluations :**
  - TP : Création et gestion de VLANs, configuration d’inter-VLAN routing.
  - Examen pratique sur la configuration des switches et des VLANs avec des scénarios réels.

---

### **4. Routage statique et dynamique**
- **Durée :** 4 semaines
- **Objectifs d'apprentissage :**
  - Maîtriser les principes du routage IP, les protocoles de routage statiques et dynamiques.
  
- **Contenu détaillé :**
  - **Théorie :**
    - Routage statique : Définition, utilisation, configuration sur des routeurs.
    - Protocoles de routage dynamique : RIP (Routing Information Protocol), OSPF (Open Shortest Path First), EIGRP (Enhanced Interior Gateway Routing Protocol).
    - Tables de routage, algorithmes de routage, convergence des réseaux.
  - **Pratique :**
    - Configuration d'un routage statique sur des routeurs Cisco (via CLI).
    - Implémentation de RIP, OSPF et EIGRP dans un réseau multi-sites.
    - Analyse des tables de routage et des processus de mise à jour des routes.

- **Évaluations :**
  - Examen pratique : Configuration d’un réseau avec plusieurs protocoles de routage.
  - TP : Analyse et optimisation d’une table de routage.

---

### **5. Services réseau essentiels**
- **Durée :** 3 semaines
- **Objectifs d'apprentissage :**
  - Comprendre et configurer les services réseaux essentiels : DHCP, DNS, NAT, VPN.
  
- **Contenu détaillé :**
  - **Théorie :**
    - Serveur DHCP : Délégation dynamique d’adresses IP, configuration et gestion des baux.
    - Serveur DNS : Résolution de noms, hiérarchie DNS, enregistrement A, CNAME, MX, PTR.
    - NAT (Network Address Translation) : Concepts, configuration de NAT et PAT.
    - VPN : Tunnels sécurisés, IPsec, SSL VPN.
  - **Pratique :**
    - Configuration d’un serveur DHCP et DNS sur un réseau local.
    - Configuration de NAT pour l’accès internet.
    - Création d’un VPN site à site en utilisant des routeurs Cisco.

- **Évaluations :**
  - TP : Configuration d'un réseau local avec DHCP, DNS et NAT.
  - Examen pratique : Configuration d’un VPN sécurisé pour un site distant.

---

### **6. Sécurité réseau**
- **Durée :** 4 semaines
- **Objectifs d'apprentissage :**
  - Appliquer les principes de sécurité dans les infrastructures réseau : pare-feu, ACL, filtrage, IDS/IPS.
  
- **Contenu détaillé :**
  - **Théorie :**
    - Concepts de sécurité réseau : pare-feu (Firewall), listes de contrôle d’accès (ACL).
    - Introduction à la cryptographie, sécurisation des communications (SSL/TLS).
    - IDS/IPS : Surveillance des réseaux, détection d’intrusions.
    - Protection contre les attaques réseau : DDoS, spoofing, phishing.
  - **Pratique :**
    - Configuration d’un pare-feu Cisco ASA pour filtrer le trafic entrant et sortant.
    - Création et test d’ACLs pour filtrer des paquets sur des routeurs.
    - Déploiement et configuration de systèmes IDS/IPS pour la détection d’attaques.

- **Évaluations :**
  - Examen pratique : Configuration d’un pare-feu avec filtrage d'accès.
  - TP : Analyse et réponse à une attaque réseau simulée avec IDS/IPS.

---

### **7. Supervision et monitoring de réseau**
- **Durée :** 2 semaines
- **Objectifs d'apprentissage :**
  - Apprendre à surveiller et diagnostiquer les réseaux pour anticiper et résoudre les problèmes.
  
- **Contenu détaillé :**
  - **Théorie :**
    - Outils de supervision : SNMP (Simple Network Management Protocol), NetFlow, syslog.
    - Analyse des journaux réseau, utilisation des MIBs pour superviser les équipements.
    - Introduction à Nagios, Zabbix, et Wireshark pour le diagnostic réseau.
  - **Pratique :**
    - Configuration d’une surveillance SNMP sur des équipements réseau.
    - Utilisation de Wireshark pour capturer et analyser le trafic réseau.
    - Mise en place d’un monitoring de serveur avec Nagios ou Zabbix.

- **Évaluations :**
  - TP : Mise en place d’une infrastructure de monitoring et analyse de la disponibilité du réseau.
  - QCM sur les outils de monitoring réseau.

---

**Évaluation finale :**
- **Projet final :** Conception et implémentation d’une infrastructure réseau complète, incluant la gestion du routage, VLANs, services réseau et sécurité.
- **Examen pratique :** Résolution de cas techniques complexes en temps limité.