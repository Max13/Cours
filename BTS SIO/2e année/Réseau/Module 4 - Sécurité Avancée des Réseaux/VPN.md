# Introduction
Un VPN (Virtual Private Network) est une technologie permettant d'intégrer plusieurs machines distantes dans un même domaine de diffusion. La connexion de ces machines par VPN peut être en clair, chiffrée, avec ou sans vérification d'intégrité, sur des ports standards ou aléatoires, suivant les différents protocoles.

# Utilités
- Accéder à un réseau privé à distance (utile pour les entreprises).
- Sécuriser les connexions sur des réseaux non sécurisés (Wi-Fi public, etc.).
- Contourner les restrictions géographiques en masquant l'adresse IP.
- Assurer l'anonymat en cachant l'identité en ligne.
- Protéger les transferts de données dans les environnements sensibles.

# Types de VPN
## 1. Client-Serveur
- Fonctionnement : Un client se connecte à un serveur, qui agit comme un intermédiaire entre l'utilisateur et internet ou le réseau local accessible par le serveur.
- Exemples : PPTP, SSTP, L2TP, OpenVPN, Wireguard.

## 2. Bidirectionnel
- Fonctionnement : Nécessite de créer une connexion dans les deux sens (contrairement à un client qui se connecte à un serveur).
- Exemples : GRE, EoIP (Ethernet over IP) de MikroTik, IPIP, MPLS.

# Protocoles et Couches OSI concernées
| **Protocole** | **Sécurité** | **Performance** | **Couche OSI**        | **Utilisation**                      |
| ------------- | ------------ | --------------- | --------------------- | ------------------------------------ |
| PPTP          | Faible       | Bonne           | 2 & 3 (Encapsulation) | Ancien, peu sécurisé                 |
| L2TP/IPSec    | Bonne        | Moyenne         | 2 & 3 (Encapsulation) | VPN grand public                     |
| OpenVPN       | Très bonne   | Moyenne         | 4 (Transport)         | VPN sécurisé flexible                |
| WireGuard     | Excellente   | Très bonne      | 3 (Réseau)            | Léger et moderne                     |
| SSTP          | Bonne        | Moyenne         | 4 (Transport)         | Windows natif, utilise le port HTTPS |
| IKEv2/IPSec   | Très bonne   | Bonne           | 3 (Réseau)            | Mobile, résistant aux interruptions  |

# Protocoles et Compatibilités
| **Protocole** | **Windows** | **MacOS** | **Linux** | **Android/iOS** | **Routeurs** |
|---------------|-------------|-----------|-----------|-----------------|--------------|
| PPTP          | ✅          | ✅         | ✅        | ✅              | ⚠️ (Obsolète) |
| L2TP/IPSec    | ✅          | ✅         | ✅        | ✅              | ✅            |
| OpenVPN       | ✅          | ✅         | ✅        | ✅              | ✅            |
| WireGuard     | ✅          | ✅         | ✅        | ✅              | ✅            |
| SSTP          | ✅          | ❌         | ⚠️         | ❌              | ❌            |
| IKEv2/IPSec   | ✅          | ✅         | ✅        | ✅              | ✅            |