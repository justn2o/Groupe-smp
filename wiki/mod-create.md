# Create

Create est un mod de technologie mécanique : tout tourne autour de la
**force de rotation**, transmise dans des réseaux d'engrenages et de
courroies pour faire fonctionner des machines, des usines automatisées, des
structures mobiles ("contraptions") et même des trains.

- **Modrinth** : [modrinth.com/mod/create](https://modrinth.com/mod/create)
- **Wiki officiel de la communauté** : [create.fandom.com](https://create.fandom.com/wiki/Create_Mod_Wiki)

## La force de rotation

Toutes les machines de Create fonctionnent grâce à un réseau de rotation
partagé, caractérisé par deux valeurs :

- **La vitesse (RPM)** — mesurée en tours par minute, visible avec un
  Speedometer. La vitesse maximum par défaut est de 256 RPM ; au-delà, les
  pièces se détachent. On change la vitesse avec des combinaisons
  d'engrenages (une petite roue dentée contre une grande roue tourne 2x
  plus vite), un Rotation Speed Controller, ou un Adjustable Chain
  Gearshift.
- **Le stress (SU, Stress Units)** — l'énergie que consomment les
  machines. Chaque réseau a une capacité de stress totale, fournie par des
  générateurs (Manivelle, Roue à eau, Moulin à vent, Machine à vapeur...).
  Si les machines consomment plus de stress que le réseau n'en produit, le
  réseau devient "overstressed" et s'arrête entièrement jusqu'à ce que la
  capacité soit augmentée ou la consommation réduite.

La transmission se fait via des **arbres** (ligne droite), **roues
dentées** (inversent le sens, changent la vitesse, tournent l'axe à 90°),
**courroies mécaniques** et **chaînes encastrées** (relais sur de longues
distances), avec des composants de contrôle comme l'**embrayage**
(Clutch, coupe la transmission via redstone) ou l'**inverseur**
(Gearshift, inverse le sens via redstone).

## Les machines

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
  couplé à une Bec verseur/Spout pour manipuler des fluides).
- **Bras mécanique (Mechanical Arm)** — transfère des objets entre
  inventaires et machines selon des points désignés.
- **Table de craft mécanique (Mechanical Crafter)** — reproduit une
  recette d'artisanat automatiquement, en réseau avec d'autres crafters
  pour des recettes complexes.
- **Brûleur de Blaze (Blaze Burner)** — fournit la chaleur nécessaire à
  certaines machines (comme un four mécanique amélioré).

## Les Contraptions

Les Contraptions sont des structures entières transformées en entités
mobiles — la mécanique signature du mod. Elles se créent via des "ancres de
mouvement" :

- **Piston mécanique** — pousse/tire une structure en ligne droite.
- **Palier mécanique (Mechanical Bearing)** — fait tourner une structure
  autour d'un axe (ex. une roue, un moulin).
- **Poulie (Rope Pulley)** — fait monter/descendre une structure le long
  d'une corde (ascenseurs).
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

Depuis la version 0.5, Create ajoute un vrai système de trains, distinct
des wagonnets vanilla :

- On pose une **voie ferrée**, une **gare (Station)**, puis on assemble le
  train en plaçant des **caisses de train (Train Casings)** sur la voie —
  elles se transforment en bogies (essieux). Une plateforme construite
  autour de deux bogies devient un wagon.
- Un bloc **Train Controls** définit le poste de conduite ; un siège ou un
  Blaze Burner placé derrière sert de "conducteur".
- Contrairement aux wagonnets vanilla, un train Create continue de rouler
  même dans des chunks non chargés et peut être piloté automatiquement par
  un **Conducteur** (Auto-Piloting) sans joueur à bord, et peut même
  traverser un portail du Nether.

## Décoration

Au-delà de la mécanique, Create ajoute un très grand nombre de blocs
décoratifs (laiton, andésite, cuivre patiné et ses variantes d'oxydation,
verre teinté, fenêtres...) souvent utilisés pour habiller les machines ou
construire dans un style "usine/industriel".
