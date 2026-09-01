# Create

![Create](https://static.wikia.nocookie.net/create_mod/images/f/f3/Mechanical_Press.png/revision/latest/scale-to-width-down/268?cb=20230522013122)

Create est un mod de technologie mécanique : tout tourne autour de la
**force de rotation**, transmise dans des réseaux d'engrenages et de
courroies pour faire fonctionner des machines, des usines automatisées, des
structures mobiles ("contraptions") et même des trains.

- **Modrinth** : [modrinth.com/mod/create](https://modrinth.com/mod/create)
- **Wiki officiel de la communauté** : [create.fandom.com](https://create.fandom.com/wiki/Create_Mod_Wiki)

## Sommaire

- [La force de rotation](#la-force-de-rotation)
- [Les matériaux](#les-mat%C3%A9riaux)
- [Les machines](#les-machines)
- [Les Contraptions](#les-contraptions)
- [Les trains](#les-trains)
- [Le Schematicannon](#le-schematicannon)
- [Décoration](#d%C3%A9coration)

## La force de rotation

![Cogwheel](https://static.wikia.nocookie.net/create_mod/images/3/3c/Cogwheel_%28block%29.png/revision/latest/scale-to-width-down/268?cb=20210414111858)
![Large Cogwheel](https://static.wikia.nocookie.net/create_mod/images/5/5a/Large_Cogwheel_%28block%29.png/revision/latest/scale-to-width-down/267?cb=20210414111900)

Toutes les machines de Create fonctionnent grâce à un réseau de rotation
partagé, caractérisé par deux valeurs :

- **La vitesse (RPM)** — mesurée en tours par minute, visible avec un
  Speedometer. La vitesse maximum par défaut est de 256 RPM ; au-delà, les
  pièces se détachent. On change la vitesse avec des combinaisons
  d'engrenages (une petite roue dentée contre une grande roue tourne 2x
  plus vite car une rotation de la grande roue équivaut à deux rotations de
  la petite), un Rotation Speed Controller, ou un Adjustable Chain
  Gearshift.
- **Le stress (SU, Stress Units)** — l'énergie que consomment les
  machines. Chaque réseau a une capacité de stress totale, fournie par des
  générateurs (Manivelle, Roue à eau, Moulin à vent, Machine à vapeur...).
  Si les machines consomment plus de stress que le réseau n'en produit, le
  réseau devient "overstressed" et s'arrête entièrement jusqu'à ce que la
  capacité soit augmentée ou la consommation réduite. Deux réseaux
  distincts peuvent fusionner s'ils se rejoignent en tournant dans le même
  sens à la même vitesse.

![Water Wheel](https://static.wikia.nocookie.net/create_mod/images/2/2f/Water_Wheel.png/revision/latest/scale-to-width-down/268?cb=20230522013529)

La transmission se fait via des **arbres** (Shaft, ligne droite), **roues
dentées** (inversent le sens, changent la vitesse, tournent l'axe à 90°),
**courroies mécaniques** et **chaînes encastrées** (relais sur de longues
distances), avec des composants de contrôle comme l'**embrayage**
(Clutch, coupe la transmission via redstone) ou l'**inverseur**
(Gearshift, inverse le sens via redstone).

## Les matériaux

![Andesite Alloy](https://static.wikia.nocookie.net/create_mod/images/c/cc/Andesite_Alloy.png/revision/latest/scale-to-width-down/268?cb=20220710101556)

Le matériau de base du mod est l'**Alliage d'Andésite** (fer + andésite),
utilisé pour la plupart des premières machines. La progression continue
ensuite avec le **Cuivre** (traitement de fluides, casings décoratifs), le
**Zinc** et enfin le **Laiton** (Brass, cuivre + zinc) pour les machines
plus avancées comme le Bras mécanique ou la Table de craft mécanique.

## Les machines

![Mechanical Press](https://static.wikia.nocookie.net/create_mod/images/f/f3/Mechanical_Press.png/revision/latest/scale-to-width-down/268?cb=20230522013122)

Une fois l'énergie de rotation disponible, elle actionne des machines qui
transforment automatiquement les ressources :

- **Presse mécanique** — aplatit les objets (ex. lingots → plaques).
- **Meules (Crushing Wheels)** — broient les blocs et minerais, souvent
  avec un rendement supérieur au vanilla.
- **Scie mécanique** — coupe le bois, transforme des blocs.
- **Ventilateur encastré (Encased Fan)** — souffle de l'air pour cuire,
  fumer, laver ou faire exploser des objets à distance selon ce qui se
  trouve derrière (feu, eau, lave...).
- **Mixeur mécanique** — combine les recettes de type "mélange" (souvent
  couplé à un Spout pour manipuler des fluides).

![Mechanical Arm](https://static.wikia.nocookie.net/create_mod/images/5/5b/Mechanical_Arm.png/revision/latest/scale-to-width-down/268?cb=20230522012945)

- **Bras mécanique (Mechanical Arm)** — transfère des objets entre
  inventaires et machines selon des points désignés (pris/déposés).
- **Table de craft mécanique (Mechanical Crafter)** — reproduit une
  recette d'artisanat automatiquement, en réseau avec d'autres crafters
  pour des recettes complexes.
- **Brûleur de Blaze (Blaze Burner)** — fournit la chaleur nécessaire à
  certaines machines (four/mixeur en version "chauffée").

## Les Contraptions

![Mechanical Bearing](https://static.wikia.nocookie.net/create_mod/images/3/36/Mechanical_Bearing.png/revision/latest/scale-to-width-down/268?cb=20230522013000)
![Mechanical Piston](https://static.wikia.nocookie.net/create_mod/images/9/9f/Mechanical_Piston.png/revision/latest/scale-to-width-down/268?cb=20230522013055)

Les Contraptions sont des structures entières transformées en entités
mobiles — la mécanique signature du mod. Elles se créent via des "ancres de
mouvement" :

- **Piston mécanique** — pousse/tire une structure en ligne droite.
- **Palier mécanique (Mechanical Bearing)** — fait tourner une structure
  autour d'un axe (ex. une roue, un moulin).
- **Poulie (Rope Pulley)** — fait monter/descendre une structure le long
  d'une corde (ascenseurs).

![Rope Pulley](https://static.wikia.nocookie.net/create_mod/images/7/78/Rope_Pulley.png/revision/latest/scale-to-width-down/268?cb=20230522013344)
![Gantry Carriage](https://static.wikia.nocookie.net/create_mod/images/b/b8/Gantry_Carriage.png/revision/latest/scale-to-width-down/268?cb=20230522012825)

- **Gantry Carriage** — déplace une structure le long d'un rail de
  portique.
- **Cart Assembler** — transforme un train de wagons vanilla en
  Contraption roulante.

Pour déplacer plus d'un bloc, il faut "coller" les blocs à l'ancre avec des
utilitaires d'attache (Châssis, Super Glue, blocs de slime/miel...). Une
fois assemblée, la structure entière (blocs, coffres, mobs à bord, etc.) se
déplace comme un seul objet — la base de la plupart des machines animées,
ascenseurs, ponts mobiles ou moulins du mod.

## Les trains

![Train Track](https://static.wikia.nocookie.net/create_mod/images/c/c8/Track_Block.png/revision/latest/scale-to-width-down/268?cb=20230602205456)

Depuis la version 0.5, Create ajoute un vrai système de trains, distinct
des wagonnets vanilla :

- On pose une **voie ferrée**, une **gare (Station)**, puis on assemble le
  train en plaçant des **caisses de train (Train Casings)** sur la voie —
  elles se transforment en bogies (essieux). Une plateforme construite
  autour de deux bogies devient un wagon.

![Small Bogey](https://static.wikia.nocookie.net/create_mod/images/7/74/Small_Bogey.png/revision/latest/scale-to-width-down/267?cb=20230602212105)

- Un bloc **Train Controls** définit le poste de conduite ; un siège ou un
  Blaze Burner placé derrière sert de "conducteur".
- Contrairement aux wagonnets vanilla, un train Create continue de rouler
  même dans des chunks non chargés et peut être piloté automatiquement par
  un **Conducteur** (Auto-Piloting) sans joueur à bord, et peut même
  traverser un portail du Nether.

## Le Schematicannon

![Schematicannon](https://static.wikia.nocookie.net/create_mod/images/b/bc/Schematicannon.png/revision/latest/scale-to-width-down/268?cb=20210518151915)

Le Schematicannon construit automatiquement une structure enregistrée dans
un plan (Schematic, créé avec la Schematic and Quill ou la Table à
Schematic) en tirant des blocs depuis un inventaire fourni en ressources —
utile pour reproduire de grandes structures sans les poser bloc par bloc.

## Décoration

Au-delà de la mécanique, Create ajoute un très grand nombre de blocs
décoratifs (laiton, andésite, cuivre patiné et ses variantes d'oxydation,
verre teinté, fenêtres...) souvent utilisés pour habiller les machines ou
construire dans un style "usine/industriel".
