# DNS
Le DNS (Domain Name System) est un système qui permet de résoudre des noms de domaine (par exemple, `www.exemple.com`) en adresses IP numériques (par exemple, `192.0.2.1`), et vice versa. Il permet ainsi aux utilisateurs de naviguer sur Internet en utilisant des noms lisibles par l'homme plutôt que des adresses IP complexes. Ce système est un élément fondamental de l'architecture d'Internet.

Un serveur DNS est un serveur qui stocke des informations sur les noms de domaine et les adresses IP correspondantes. Lorsqu'un utilisateur souhaite accéder à un service sur un réseau, son appareil interroge un serveur DNS pour traduire le nom de domaine en une adresse IP.

## Types de Serveurs DNS
- Serveur DNS Récursif : Reçoit la demande de résolution et la transmets à un autre serveur.
- Serveur DNS Itératif : Reçoit la demande de résolution et cherche la réponse à travers plusieurs serveurs DNS.
- Serveur DNS Autoritaire : Contient les informations de résolution définitives pour un domaine spécifique.

[![](https://mermaid.ink/img/pako:eNqNlNFq2zAUhl_loKsUWq0J3S5MkzKSm8EoId7V8I0qnzimtuTK0lgpfaDtNfpiO5KcxJ6TUoHB5_g_R_8nS3phUufIEtbik0MlcVWKwog6U0BDOKuVqx_QxPheWwRTFjsLegvrZQIblDs09CRQi7LihdZFhVzqrkMjjC1l2QhlST_ObbDV1S80IFrYvP0JgTO3D2YxSZ2BiqajLAp3EWt1Y-GbklopB59gTVWoQAoyEL_7sV7C1WJxaJ3A1-gNf4u6iebg7ig_WBgW3afAYQ6P3Ghtr1o0lG25QsuPpUuDglZkAERqD5P6AiIwQpYKYcIvPNS42zkfJAseyCzvu82xtUY_B0Gv1s868h9q57Dlha3yjyP8-L7qE_hw4lsFgnGzMwRUFkycWfU9B8mOST_ViKLfYA6qnfZ_JPeeTohmA9G7uOkQ14eT4zYO0H7S_3f2CDj1wO9vtVUHnfah0xH0iSZzmN7M-OzzNZ9dT_n0y02sR5XHl4ETfzA_3uPUkoS_61flZEV3wKLK3wFP7u2v7U7ggTF8jbmu394bHfRGqxbZJavRkM-cLqAXL82Y3WGNGUvoNcetcJXNWKZeSeovo_RZSZZY4_CSGe2KHUu2omopck1OFN3ttZcQzE-t6070-g-B9o9y?type=png|500)](https://mermaid.live/view#pako:eNqNlNFq2zAUhl_loKsUWq0J3S5MkzKSm8EoId7V8I0qnzimtuTK0lgpfaDtNfpiO5KcxJ6TUoHB5_g_R_8nS3phUufIEtbik0MlcVWKwog6U0BDOKuVqx_QxPheWwRTFjsLegvrZQIblDs09CRQi7LihdZFhVzqrkMjjC1l2QhlST_ObbDV1S80IFrYvP0JgTO3D2YxSZ2BiqajLAp3EWt1Y-GbklopB59gTVWoQAoyEL_7sV7C1WJxaJ3A1-gNf4u6iebg7ig_WBgW3afAYQ6P3Ghtr1o0lG25QsuPpUuDglZkAERqD5P6AiIwQpYKYcIvPNS42zkfJAseyCzvu82xtUY_B0Gv1s868h9q57Dlha3yjyP8-L7qE_hw4lsFgnGzMwRUFkycWfU9B8mOST_ViKLfYA6qnfZ_JPeeTohmA9G7uOkQ14eT4zYO0H7S_3f2CDj1wO9vtVUHnfah0xH0iSZzmN7M-OzzNZ9dT_n0y02sR5XHl4ETfzA_3uPUkoS_61flZEV3wKLK3wFP7u2v7U7ggTF8jbmu394bHfRGqxbZJavRkM-cLqAXL82Y3WGNGUvoNcetcJXNWKZeSeovo_RZSZZY4_CSGe2KHUu2omopck1OFN3ttZcQzE-t6070-g-B9o9y)
<small>[Mermaid](https://mermaid.live/edit#pako:eNqNlNFq2zAUhl_loKsUWq0J3S5MkzKSm8EoId7V8I0qnzimtuTK0lgpfaDtNfpiO5KcxJ6TUoHB5_g_R_8nS3phUufIEtbik0MlcVWKwog6U0BDOKuVqx_QxPheWwRTFjsLegvrZQIblDs09CRQi7LihdZFhVzqrkMjjC1l2QhlST_ObbDV1S80IFrYvP0JgTO3D2YxSZ2BiqajLAp3EWt1Y-GbklopB59gTVWoQAoyEL_7sV7C1WJxaJ3A1-gNf4u6iebg7ig_WBgW3afAYQ6P3Ghtr1o0lG25QsuPpUuDglZkAERqD5P6AiIwQpYKYcIvPNS42zkfJAseyCzvu82xtUY_B0Gv1s868h9q57Dlha3yjyP8-L7qE_hw4lsFgnGzMwRUFkycWfU9B8mOST_ViKLfYA6qnfZ_JPeeTohmA9G7uOkQ14eT4zYO0H7S_3f2CDj1wO9vtVUHnfah0xH0iSZzmN7M-OzzNZ9dT_n0y02sR5XHl4ETfzA_3uPUkoS_61flZEV3wKLK3wFP7u2v7U7ggTF8jbmu394bHfRGqxbZJavRkM-cLqAXL82Y3WGNGUvoNcetcJXNWKZeSeovo_RZSZZY4_CSGe2KHUu2omopck1OFN3ttZcQzE-t6070-g-B9o9y)</small>

## Outils de Résolution DNS selon les Systèmes d'Exploitation

Chaque système d'exploitation offre des outils en ligne de commande pour interroger les serveurs DNS et résoudre des noms de domaine.

### Windows
- `nslookup` : Outil de ligne de commande permettant de résoudre des noms de domaine en adresses IP, et inversement.
	- Exemple : `nslookup www.exemple.com`
	- Exemple pour une requête inverse : `nslookup 192.168.1.1`

### Linux/macOS
- `dig` : Outil plus puissant que `nslookup`, utilisé pour interroger les serveurs DNS et obtenir des informations détaillées.
	- Exemple : `dig www.exemple.com`
	- Exemple avec un type d'enregistrement : `dig MX www.exemple.com` (pour obtenir les enregistrements MX, c'est-à-dire les serveurs de mail).

- `nslookup` : Comme sous Windows, cet outil est également disponible sur Linux et macOS pour la résolution DNS.

- `host` : Un autre outil utilisé pour interroger les serveurs DNS.
	- Exemple : `host www.exemple.com`

## Les Différents Champs DNS
Les serveurs DNS contiennent différents types d'enregistrements dans leur base de données (Liste non exchaustive) :

- NS (Name Server) : Spécifie quel serveur DNS est autoritaire pour le domaine.
	- Exemple : `exemple.com IN NS ns1.exemple.com`

- A (Address) : Enregistrement qui associe un nom de domaine à une adresse IPv4.
	- Exemple : `www.exemple.com IN A 192.2.0.1`

- AAAA (Quad A / IPv6 Address) : Enregistrement qui associe un nom de domaine à une adresse IPv6.
	- Exemple : `www.exemple.com IN AAAA 2001:db8:dead:beef::1`

- MX (Mail Exchanger) : Enregistrement qui spécifie les serveurs de messagerie pour un domaine.
	- Exemple : `exemple.com IN MX 10 mail.exemple.com`

- CNAME (Canonical Name) : Alias pour un autre nom de domaine. Utilisé pour rediriger un nom de domaine vers un autre.
	- Exemple : `www.exemple.com IN CNAME exemple.com`

- PTR (Pointer) : Enregistrement inverse, utilisé pour la résolution inverse (d'une adresse IP à un nom de domaine).
	- Exemple : `1.0.168.192.in-addr.arpa IN PTR www.exemple.com`

- SOA (Start of Authority) : Indique que l'enregistrement spécifié est le premier enregistrement d'une zone et fournit des informations sur le serveur DNS.
	- Exemple : `exemple.com IN SOA ns1.exemple.com. admin.exemple.com. (20210101 3600 1800 1209600 86400)`

- TXT : Enregistrement permettant de stocker des informations textuelles.
	- Exemple : `exemple.com IN TXT "v=spf1 include:_spf.google.com ~all"`

## Exercices Pratiques

1. Résolution DNS simple : Utilise l'outil `nslookup` ou `dig` pour résoudre l'adresse IP de `www.google.com`.  
  
2. Résolution inverse : Trouve le nom de domaine correspondant à l'adresse IP `8.8.8.8` (serveur DNS de Google) en utilisant `nslookup` ou `dig`.  
  
3. Vérification des enregistrements MX : Utilise `dig` pour trouver les serveurs de mail associés au domaine `gmail.com`.  
  
4. Vérification de l'enregistrement CNAME : Cherche l'enregistrement CNAME pour le domaine `www.facebook.com` avec l'outil `dig`.  
  
5. Exploration du cache DNS : Vérifie le cache DNS de ta machine sous Windows avec la commande `ipconfig /displaydns`. Résous un nom de domaine, puis vérifie si le cache a bien été mis à jour.  
  
6. Modifier les enregistrements DNS sur un serveur local : Crée un enregistrement `A` pour un domaine fictif (par exemple `monserveur.local`) avec une adresse IP locale dans un serveur DNS local (comme BIND sur Linux).  
  
7. Analyse des enregistrements DNS sur un site web : Utilise `dig` pour obtenir l'enregistrement SOA et les enregistrements NS pour `www.amazon.com`.  
  
8. Ping et analyse DNS : Utilise `ping` pour tester la connectivité avec `www.example.com`, puis résous son adresse IP avec `nslookup` ou `dig`.