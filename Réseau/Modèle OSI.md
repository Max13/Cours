# Modèle OSI
Le modèle OSI (Open Systems Interconnection) est le standard utilisée pour expliquer le fonctionnement des réseaux de communication. Il est composé de sept couches, chacune ayant un rôle précis dans le processus de transmission et réception de données sur un réseau.

*[[#1. Couche Physique|P]]etit [[#2. Couche Liaison de Données (Data Link Layer)|L]]apin [[#3. Couche Réseau (Network Layer)|R]]ose [[#4. Couche Transport (Transport Layer)|T]]rouvé à la [[#5. Couche Session (Session Layer)|S]].[[#6. Couche Présentation (Presentation Layer)|P]].[[#7. Couche Application (Application Layer)|A]]*

## 1. Couche Physique
- Unité de donnée : Bit
- Équipements : Concentrateur/Hub, Périphérique USB (Clavier, Souris, …), Télécommande.
- Fonction principale : Cette couche est responsable de la transmission brute de données sous forme de bits sur le [[Carte réseau#Les Médias de Transmission|média de transmission]].

## 2. Couche Liaison de Données
- Unité de donnée : Trame
- Équipement : Commutateur / Switch.
- Fonction principale : Elle assure un transfert de données fiable entre deux nœuds sur le même réseau physique.
- Informations : Adresses MAC (Source et Destination).

## 3. Couche Réseau
- Unité de donnée : Paquet
- Équipement : Routeur.
- Fonction principale : Cette couche est responsable du routage des paquets d'une machine à une autre à travers différents réseaux, en utilisant des adresses logiques. Elle gère également la fragmentation et l'assemblage des paquets.
- Informations : Adresses IP (Source et Destination).

## 4. Couche Transport
- Unité de donnée : Segment (pour TCP) ou Datagramme (pour UDP).
- Fonction principale :
	- Dans le cas de TCP, la couche de transport garantit un transfert de données fiable et ordonné entre les applications, en utilisant des mécanismes tels que l'accusé de réception et la retransmission en cas de perte. Elle assure aussi la division des messages en segments. C'est un protocole connecté et fiable.
	- En UDP, les données sont envoyées en masse sans tenir compte de l'état « connecté » et « en attente de données » du destinataire, sans contrôle d'intégrité, sans vérification de l'ordre ni d'accusé de réception. C'est un protocole déconnecté et non fiable.
- Informations : Protocole, Numéros de ports, contrôle de flux, contrôle d'erreurs, segmentation, réassemblage.

## 5. Couche Session
- Unité de donnée : Message ou données.
- Fonction principal : Cette couche gère l'établissement, la maintenance et la terminaison des sessions de communication entre les applications. Elle synchronise également le dialogue et fournit des points de reprise en cas de coupure.
- Informations : Informations de session, synchronisation, gestion des dialogues (ouverture et fermeture).

## 6. Couche Présentation
- Unité de donnée : Message ou données.
- Fonction principale : La couche de présentation est responsable de la traduction des données entre le format utilisé par l'application et celui utilisé sur le réseau. Elle peut également compresser et chiffrer les données pour améliorer la sécurité et l'efficacité.
- Informations : Encodage des caractères, chiffrement, compression, traduction des formats.

## 7. Couche Application
- Unité de donnée : Message ou données.
- Fonction principale : La couche application est celle avec laquelle les utilisateurs interagissent directement. Elle fournit des services de réseau aux applications telles que le courrier électronique, la navigation web, le transfert de fichiers, etc…
- Informations : Protocole HTTP, FTP, SMTP, etc…

## Visuel
![[Modèle OSI.png|500]]

<!-- https://ipelsht.rnu.tn/useruploads/files/Réseaux%20informatique.pdf -->