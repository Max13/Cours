# Carte Réseau
Il s'agit d'un composant matériel qui permet à un ordinateur de se connecter à un réseau pour échanger des données. Essentiellement, la carte réseau agit comme une interface entre l'appareil et le réseau, facilitant la communication en convertissant les données de l'ordinateur en un format qui peut être transmis via les différents types de médias de communication disponibles.

## Les Médias de Transmission
Pour que les données circulent d'un appareil à un autre, elles doivent emprunter un support physique ou un canal de transmission. Il existe principalement trois types de médias de transmission, chacun ayant ses propres caractéristiques, avantages et limites :

- **Cuivre** (Câbles à paires torsadées ou coaxial) :
	- Le câble en cuivre est le média le plus couramment utilisé dans les réseaux locaux (LAN). Les câbles Ethernet utilisent des paires torsadées de fils en cuivre pour transmettre les données sous forme de signaux électriques.
	- Avantages : Coût relativement faible, facile à installer.
	- Inconvénients : Sensible aux interférences électromagnétiques, distance de transmission limitée sans amplification ou répétition.
   
- **Radio** (Wi-Fi, Bluetooth, RFID, NFC, …) :
	- Les technologies sans fil utilisent des ondes radio à plus ou moins grande portée pour transmettre des données dans l'air.
	- Avantages : Mobilité, flexibilité, facilité d’installation.
	- Inconvénients : Sensibilité aux interférences (appareils électroménagers, fluides, matériaux, …), portée limitée, risques de sécurité (clé partagée).
   
- **Optique** (Fibre optique) :
	- Ce média utilise des brins de verre ou de plastique pour transmettre des données sous forme d'impulsions lumineuses. La fibre optique est principalement utilisée dans les réseaux longue distance, ainsi que dans les infrastructures où de très grandes quantités de données doivent être échangées à haute vitesse.
	- Avantages : Grande capacité de transmission (débit élevé), immunité aux interférences électromagnétiques, longue distance sans perte de signal significative.
	- Inconvénients : Coût plus élevé que le cuivre, installation plus complexe.

## Fonctionnement
Son fonctionnement peut-être découpé en plusieurs étapes. Prenons l'exemple de l'ouverture d'une page web (ex: example.com) depuis un navigateur :
1. La requête « affiche moi *example.com* » est créée dans les couches supérieures (ou couches logicielles) du [[Modèle OSI]].
2. Les données sont encapsulées dans un format approprié pour le transport à travers le réseau, par exemple en paquets ou en trames, puis converties en signaux (électriques, radio, ou lumineux) en fonction du média utilisé.
3. Ces signaux sont ensuite envoyées sur le réseau et acheminées vers leur destination.
4. Enfin, de la même manière (mais à l'inverse), la carte réseau reçoit les signaux de l'expéditeur, décapsule les données contenues et envoie ces données dans les couches supérieures pour être interprétées par un programme.

> [!info] Voir [[Modèle OSI]]
