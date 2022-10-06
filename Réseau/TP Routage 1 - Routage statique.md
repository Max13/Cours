# TP Routage 1 - Routage statique

#### Routage statique entre 2 sous réseaux distants
[Projet GNS3](https://drive.google.com/file/d/1KyCG-vBxdGorEKgG9TFwMDRsh9IpBjyP/view?usp=sharing) (bit.ly/gns3-2r4sr)

![[Schémas/Routage Statique 1.png]]

### Constat
- **R1** est directement connecté à:
	- 0.0/30
	- 1.0/30
	- 2.0/30
- **R2** est directement connecté à:
	- 0.0/30
	- 3.0/30
	- 4.0/30

### Problèmes:
- **R1** ne connait pas <u>3.0/30</u> ni <u>4.0/30</u>
- **R2** ne connait pas <u>1.0/30</u> ni <u>2.0/30</u>

### Solution ?
Allez y, cherchez.