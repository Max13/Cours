# Guide : Installer une Configuration d'Usine sur MikroTik
<small>Mise à jour: 3 novembre 2024</small>

Besoin d'installer une configuration personnalisée en mode usine sur un routeur MikroTik ? Suivez ce guide pour préparer votre configuration, exporter les paramètres, utiliser Netinstall et appliquer la configuration facilement.

## Étape 1 : Créer la configuration souhaitée
### Option A : Exporter la configuration d'un appareil source
Tout commence par la configuration initiale sur un routeur de référence, qu'on exportera ensuite pour la transférer sur d’autres appareils.

1. Configurer l’Appareil : Connectez vous sur le routeur de référence et effectuez les configurations nécessaires (IP, firewall, NAT, etc…).
2. Exporter la Configuration : Dans Winbox, ouvrez un terminal et tapez la commande suivante pour exporter la configuration : `/export file=config terse`. Un fichier nommé `config.rsc` sera créé dans les fichiers du routeur (Menu « Files »)
3. Récupérer le Fichier : Allez dans le menu « Files » de Winbox, localisez `config.rsc`, puis téléchargez-le.

### Option B : Écrire une configuration à la main
Là… Rien de spécial à expliquer, allez voir la section [Scripting](https://help.mikrotik.com/docs/spaces/ROS/pages/47579229/Scripting) sur la base de connaissance de MikroTik, et tapez votre script de configuration. L'extension est `.rsc`.

## Étape 2 : Netinstall
Netinstall est l’outil officiel de MikroTik pour installer le firmware d'un routeur (y comprit pour le mettre à jour ou le rétrograder), et permet également d'enregistrer une configuration qui sera appliquée à chaque fois que le routeur sera réinitialisé.

1. Télécharger [Netinstall](https://mikrotik.com/download) et le firmware de RouterOS
	- Pour Netinstall, par experience, je vous suggère de télécharger la version correspondante à la version du firmware de backup de votre routeur. Vous pouvez l'avoir dans Winbox > System > RouterBOARD, il s'agit du champ « Factory Firmware ».
	- Pour RouterOS, il faut évidemment sélectionner l'image correspondant à la bonne architecture de votre appareil.
2. Configurer le PC
	- Désactivez la carte WiFi de votre PC (le cas échéant).
	- Connectez votre ordinateur par câble sur le port « Etherboot » du routeur (généralement **ether1**), de préférence sans passer par un adaptateur USB/RJ45.
	- Configurez l'adresse IP `192.168.88.2` et le masque `255.255.255.0` sur la carte filaire de votre PC.
3. Activer le serveur PXE de Netinstall : Ouvrez Netinstall, dans la section « Router/Drives » (dans le quart haut gauche), cliquez sur le bouton « Net booting », une petite fenêtre s'ouvre. Activez la case « Boot server enabled » et dans le champ « Client IP address » indiquez `192.168.88.3`.

## Étape 3 : Mettre le routeur en mode Etherboot ou Netinstall
<small>C'est la même chose…</small>

Soit à la main : Débranchez le routeur, rebranchez le <u>EN MAINTENANT LE BOUTON RESET ENFONCÉ</u> jusqu'à ce qu'il apparaisse dans Netinstall. Cela peut prendre 30 sec au maximum.

Soit via Winbox : System > RouterBOARD > Settings. Dans cette fenêtre, réglez le champ « Boot Device » sur `try-ethernet-once-then-nand`. Et redémarrez votre routeur. Il devrait apparaitre tout seul dans Netinstall.

> [!tip] Sinon…
> Si le routeur n'apparaît pas, soit vous n'avez pas correctement appuyé sur le bouton reset AVANT de le brancher, ET PENDANT 30 secondes. Soit vous utilisez un adaptateur USB/RJ45, certains modèles ne permettent pas de détecter un routeur en Etherboot, dans ce cas il peut-être nécessaire de brancher le PC et le routeur au même switch.

## Étape 4 : Appliquez la configuration et GO !
- Dans la section « Packages » (quart bas gauche), cliquez sur « Browse » et choisissez le dossier dans lequel vous avez téléchargé le firmware de votre routeur. Si vous avez téléchargé plusieurs firmware pour plusieurs architectures, seules les firmwares de l'architecture du routeur affiché et sélectionné apparaîtront dans la liste.
- A droite, la case « Keep old configuration » permet de conserver la configuration installée. On la garde décochée.
- La case « Apply default config » permet d'activer la configuration par défaut du routeur à sa réinitialisation. Le but est de remplacer la configuration d'usine, donc on garde la case décochée.
- Enfin, ce qui nous intéresse, « Configure script » à cocher. Puis dans le champ, sélectionnez le fichier de config de l'[[#Étape 1 Créer la configuration souhaitée|Étape 1]].

GO ! Appuyez sur le bouton « Install » et l'installation se lancera. À la fin, le routeur sera automatiquement redémarré.

> [!tip] Vérifiez votre configuration
> N'oubliez pas de vérifier si la configuration a bien été installée, vous pouvez tenter de vous connecter à votre routeur pour vérifier si tout est OK ainsi que les logs. S'ils contiennent une ligne rouge indiquant un souci avec un script, c'est qu'il y a eu une erreur dans l'application de votre script de configuration, et qu'elle est incomplète.

---

Voilà, vous avez maintenant un routeur MikroTik réinitialisé avec une configuration d’usine personnalisée et prêt à l’emploi !

<small style="text-align:right">&mdash; Rédigé par Adnan R. pour <a href="https://redvi.se/" target="_blank">Redvise Ltd.</a></small>