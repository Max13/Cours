Que ce soit pour donner un nouveau souffle à votre routeur, résoudre un problème de configuration, ou simplement pour tester la réinitialisation d’usine, voici un tutoriel sympa pour remettre votre routeur MikroTik à zéro ! Deux options s’offrent à vous : la réinitialisation à froid (pour ceux qui aiment mettre la main à la pâte) ou la réinitialisation à chaud (pour ceux qui préfèrent la méthode douce via Winbox).

[[#Méthode 1 Réinitialisation à Froid (bouton reset)]]

[[#Méthode 2 Réinitialisation à Chaud (reset logiciel)]]

## Méthode 1 : Réinitialisation à Froid (bouton reset)
Parfait si vous n’avez pas d’accès au routeur via Winbox ou si vous préférez l’approche « physique » ! 🚀
1. Débrancher le routeur : Déconnectez l’alimentation pour commencer. Rien de bien compliqué, mais c’est essentiel !
2. Appuyer sur le bouton Reset : Sur votre RouterBOARD, localisez le bouton « Reset » (souvent tout petit). Gardez-le enfoncé.
3. Rebrancher le routeur : Tout en maintenant le bouton reset enfoncé, rebranchez l’alimentation. C’est un peu d’acrobatie, mais on y arrive !
4. Compter 5 secondes : Après environ 5 secondes, une LED (souvent marquée « USR ») devrait clignoter. Quand elle clignote, vous pouvez relâcher le bouton reset.
5. Patienter : Le routeur se réinitialise en configuration d’usine. Ça y est ! 🎉

> [!tip] Si votre modèle de routeur est un peu ancien et n’a pas de bouton reset, vous devrez peut-être ouvrir le boîtier pour accéder aux points de contact de réinitialisation. Attention à ne pas endommager les composants !

## Méthode 2 : Réinitialisation à Chaud (reset logiciel)
Si vous êtes déjà connecté à votre routeur et préférez une approche plus digitale, cette méthode est pour vous. 💻
1. Connexion à Winbox : Lancez l’application Winbox et connectez-vous à votre routeur (en IP ou MAC, bonjour bouton reset virtuel !).
2. Accéder au Menu Reset : Rendez-vous dans le menu System puis sélectionnez Reset Configuration :
    - Keep Users : Cochez cette option si vous voulez garder les utilisateurs existants. Utile si vous avez des accès spécifiques configurés.
	- CAPS Mode : Activez le mode CAPS si vous voulez que le routeur cherche un serveur CAPsMAN pour récupérer une configuration CAPs.
	- No Default Configuration : Cochez si vous voulez un routeur vierge sans config par défaut. Attention, cela signifie pas de firewall, pas de bridge sur les ports, et pas de serveur DHCP !
	- Do Not Backup : Évite la création d'une sauvegarde de la configuration actuelle. Pratique si vous êtes sûr de ne rien vouloir garder, en plus ça vous fait gagner quelques secondes.
	- Run After Reset : Sélectionnez un script à lancer après réinitialisation, si besoin.
3. Lancer la Réinitialisation : Enfin, cliquez sur le bouton Reset Configuration. Le routeur va redémarrer et se réinitialiser. 🎉

Vous avez maintenant un routeur fraîchement réinitialisé, prêt à repartir sur de nouvelles bases.