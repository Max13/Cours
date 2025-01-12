# Modèle TCP/IP
Le modèle TCP/IP (*Transmission Control Protocol* **sur** *Internet Protocol*) est le 2e modèle le plus utilisé pour la communication de données sur un réseau informatique (Le premier étant le [[BTS SIO/1ère année/Réseau/Module 1 - Bases des réseaux informatiques/Modèle OSI|Modèle OSI]])

## Couches

### 1. Couche Accès au Réseau
- Équipements : Commutateurs, cartes réseau, câbles.
- Fonctions : Transmission physique des données, gestion des supports de transmission (Ethernet, Wi-Fi).

### 2. Internet
- Équipements : Routeurs, pare-feu.
- Fonctions : Routage des paquets, adressage IP, fragmentation.

### 3. Transport
- Équipements : Pare-feu, serveurs qui gèrent des connexions TCP/UDP.
- Fonctions : Contrôle des erreurs, gestion de la congestion, multiplexage (ex : TCP, UDP).

### 4. Application
- Équipements : Serveurs web, serveurs de messagerie, applications.
- Fonctions : Communication entre applications, gestion des services (ex : HTTP, FTP, DNS, SMTP).

## Comparaison avec le Modèle OSI
Le [[BTS SIO/1ère année/Réseau/Module 1 - Bases des réseaux informatiques/Modèle OSI|Modèle OSI]] est plus détaillé et théorique, avec une séparation stricte des responsabilités entre ses 7 couches. À l'inverse, le modèle TCP/IP est plus simple et plus orienté vers la pratique, avec seulement 4 couches :
- Les couches 1, 2 et 3 ([[BTS SIO/1ère année/Réseau/Module 1 - Bases des réseaux informatiques/Modèle OSI#1. Couche Physique|Physique]], [[BTS SIO/1ère année/Réseau/Module 1 - Bases des réseaux informatiques/Modèle OSI#2. Couche Liaison de Données|Liaison de données]] et [[BTS SIO/1ère année/Réseau/Module 1 - Bases des réseaux informatiques/Modèle OSI#3. Couche Réseau|Réseau]]) du modèle OSI sont combinées dans les couches [[#1. Couche Accès au Réseau|Accès au Réseau]] et [[#2. Internet|Internet]] du modèle TCP/IP.
- La couche 4 ([[BTS SIO/1ère année/Réseau/Module 1 - Bases des réseaux informatiques/Modèle OSI#4. Couche Transport|Transport]]) du modèle OSI correspond directement à la couche [[#3. Transport|Transport]] du modèle TCP/IP.
- Les couches 5 et 6 ([[BTS SIO/1ère année/Réseau/Module 1 - Bases des réseaux informatiques/Modèle OSI#5. Couche Session|Session]] et [[BTS SIO/1ère année/Réseau/Module 1 - Bases des réseaux informatiques/Modèle OSI#6. Couche Présentation|Présentation]]) du modèle OSI sont souvent combinées dans la couche [[#4. Application|Application]] du modèle TCP/IP.
- Enfin, la couche 7 ([[BTS SIO/1ère année/Réseau/Module 1 - Bases des réseaux informatiques/Modèle OSI#7. Couche Application|Application]]) du modèle OSI couvre tout ce qui est fait dans la couche 4 ([[#4. Application|Application]]) du modèle TCP/IP.

## Visuel
![[Modèle TCP-IP.png|500]]