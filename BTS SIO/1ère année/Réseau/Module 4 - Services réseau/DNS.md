# DNS
Le DNS (Domain Name System) est un système qui permet de résoudre des noms de domaine (par exemple, `www.exemple.com`) en adresses IP numériques (par exemple, `192.0.2.1`), et vice versa. Il permet ainsi aux utilisateurs de naviguer sur Internet en utilisant des noms lisibles par l'homme plutôt que des adresses IP complexes. Ce système est un élément fondamental de l'architecture d'Internet.

Un serveur DNS est un serveur qui stocke des informations sur les noms de domaine et les adresses IP correspondantes. Lorsqu'un utilisateur souhaite accéder à un service sur un réseau, son appareil interroge un serveur DNS pour traduire le nom de domaine en une adresse IP.

## Types de Serveurs DNS
- Serveur DNS Récursif : Reçoit la demande de résolution et la transmets à un autre serveur.
- Serveur DNS Itératif : Reçoit la demande de résolution et cherche la réponse à travers plusieurs serveurs DNS.
- Serveur DNS Autoritaire : Contient les informations de résolution définitives pour un domaine spécifique.

[![](https://mermaid.ink/img/pako:eNqNlN9q2zAUxl_loKsUWq0J3S5MkzKSm8EoId7V8I1qnzimtuTqz1gpfaDtNfpiO5KcxJ6TUoHB5_g7R99PlvTCclUgS5jBJ4cyx1UlSi2aTAIN4aySrnlAHeN7ZRF0Ve4sqC2slwlsMN-hpieBRlQ1L5Uqa-S56jq0Qtsqr1ohLenHuQ0aVf9CDcLA5u1PCJy-fdCLSeo01DQdZVG4i1irWgvfZK6kdPAJ1lSFEnJBBuJ3P9ZLuFosDq0T-Bq94W_RtNEc3B3lBwvDovsUOMzhkWul7JVBTVnDJVp-LF1qFLQiAyBSe5jUFxCBFnklESb8wkONu53zQbLggczyvtsCjdXqOQh6tX7Wkf9QO4ctL21dfBzhx_dVn8CHE98qEIybnSGgsmDizKrvOUh2TPqpRhT9BnOQZtr_kdx7OiGaDUTv4qZDXB9Ojts4QPtJ_9_ZI-DUA7-_1VYddNqHTkfQJ5rMYXoz47PP13x2PeXTLzexHmURXwZO_MH8eI9TSxL-rl-VkxXdAYsqfwc8ube_tjuBB8bwNea6fntvdNBbJQ2yS9agJp8FXUAvXpoxu8MGM5bQa4Fb4WqbsUy-ktRfRumzzFlitcNLppUrdyzZitpQ5NqCKLrb65Almp9K7ePXfxA4j70?type=png)](https://mermaid.live/edit#pako:eNqNlN9q2zAUxl_loKsUWq0J3S5MkzKSm8EoId7V8I1qnzimtuTqz1gpfaDtNfpiO5KcxJ6TUoHB5_g7R99PlvTCclUgS5jBJ4cyx1UlSi2aTAIN4aySrnlAHeN7ZRF0Ve4sqC2slwlsMN-hpieBRlQ1L5Uqa-S56jq0Qtsqr1ohLenHuQ0aVf9CDcLA5u1PCJy-fdCLSeo01DQdZVG4i1irWgvfZK6kdPAJ1lSFEnJBBuJ3P9ZLuFosDq0T-Bq94W_RtNEc3B3lBwvDovsUOMzhkWul7JVBTVnDJVp-LF1qFLQiAyBSe5jUFxCBFnklESb8wkONu53zQbLggczyvtsCjdXqOQh6tX7Wkf9QO4ctL21dfBzhx_dVn8CHE98qEIybnSGgsmDizKrvOUh2TPqpRhT9BnOQZtr_kdx7OiGaDUTv4qZDXB9Ojts4QPtJ_9_ZI-DUA7-_1VYddNqHTkfQJ5rMYXoz47PP13x2PeXTLzexHmURXwZO_MH8eI9TSxL-rl-VkxXdAYsqfwc8ube_tjuBB8bwNea6fntvdNBbJQ2yS9agJp8FXUAvXpoxu8MGM5bQa4Fb4WqbsUy-ktRfRumzzFlitcNLppUrdyzZitpQ5NqCKLrb65Almp9K7ePXfxA4j70)

[![](https://mermaid.ink/img/pako:eNqNVMFO4zAQ_ZWRT0VQQyuWQ0SLEFyQEKoaTigX40zTiMQOjr1ahPgg9jf4MWYSKI2SVliK5LHfe2O_8eRVaJuiiESNzwGNxutcZU6ViQEaKnhrQvmIro3vrEdwebb2YFewuIpgiXqNjr4ISpUXMrM2K1Bq-6VQKedznVfKeML315ZY2-IvOlA1LD_emyC480c3H8XBQUHpaBVVOBjgWuuZF6NjEjilc4MwkgfMf5KO9sc1b7paGvR9hfvb620BDkd09FZgJTNfpPsF4q4Ah6MfCxoZU0_2utJwm_tPTqdy-udETk8mcnJ22kJt5eHGaGtMgGNYEAwNaEWOt_s8Flcwns83XkZw2RYD_6myavPCxQ9843mXdBeDhBn0fZPD1MOmAA2PPetk4MoQZNyVb2Az6Bu7MwNVpGHuuAkXrJ9mGzwD9n9rRXJNBkDTDmjXeWI-z3534_6ZBgiz4WqjSdtJp0bcaL_X-HoN7bviDn0OH_89iiNRoiORlLr9laGJ8GssMRERTVNcqVD4RCTmjaDc-fGL0SLyLuCRcDZkaxGtVFFTFKpU-e9fxWaVnvODtd_x2yeqUGMJ?type=png)](https://mermaid.live/edit#pako:eNqNVMFO4zAQ_ZWRT0VQQyuWQ0SLEFyQEKoaTigX40zTiMQOjr1ahPgg9jf4MWYSKI2SVliK5LHfe2O_8eRVaJuiiESNzwGNxutcZU6ViQEaKnhrQvmIro3vrEdwebb2YFewuIpgiXqNjr4ISpUXMrM2K1Bq-6VQKedznVfKeML315ZY2-IvOlA1LD_emyC480c3H8XBQUHpaBVVOBjgWuuZF6NjEjilc4MwkgfMf5KO9sc1b7paGvR9hfvb620BDkd09FZgJTNfpPsF4q4Ah6MfCxoZU0_2utJwm_tPTqdy-udETk8mcnJ22kJt5eHGaGtMgGNYEAwNaEWOt_s8Flcwns83XkZw2RYD_6myavPCxQ9843mXdBeDhBn0fZPD1MOmAA2PPetk4MoQZNyVb2Az6Bu7MwNVpGHuuAkXrJ9mGzwD9n9rRXJNBkDTDmjXeWI-z3534_6ZBgiz4WqjSdtJp0bcaL_X-HoN7bviDn0OH_89iiNRoiORlLr9laGJ8GssMRERTVNcqVD4RCTmjaDc-fGL0SLyLuCRcDZkaxGtVFFTFKpU-e9fxWaVnvODtd_x2yeqUGMJ)

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