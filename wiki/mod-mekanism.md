# Mekanism

![Mekanism](https://cdn.modrinth.com/data/Ce6I4WUE/ea185eb1300a64867f89101d4798e71a54ef6bed_96.webp)

Mekanism est un mod de **technologie lourde** : machines de traitement des
minerais (jusqu'à **×5** de rendement), réseaux d'énergie, de fluides et de
produits chimiques, stockage massif, téléportation, et un équipement de fin de
partie — la **MekaSuit** — qui demande une vraie filière **nucléaire**. Ses deux
modules les plus connus sont ici : **Mekanism** (cette page) et **Mekanism
Generators** (page séparée : générateurs, turbine, réacteurs).

- **Modrinth** : [modrinth.com/mod/mekanism](https://modrinth.com/mod/mekanism)
- **Wiki officiel** : [wiki.aidancbrady.com](https://wiki.aidancbrady.com/wiki/Main_Page)
- **Code source** : [github.com/mekanism/Mekanism](https://github.com/mekanism/Mekanism)
- **Version installée** : 10.7.19 pour NeoForge 1.21.1

> **À savoir sur les noms** — la traduction française est parfois étrange (le
> système **QIO** s'appelle *OQO*, le **SPS** s'appelle *CPC*). Cette page
> utilise les noms **français affichés en jeu**, avec le nom anglais entre
> parenthèses pour retrouver la page du wiki officiel.

## Sommaire

- [Par où commencer](#par-o%C3%B9-commencer)
- [Les minerais](#les-minerais)
- [Traiter un minerai : ×2 à ×5](#traiter-un-minerai--%C3%972-%C3%A0-%C3%975)
- [L'énergie](#l%C3%A9nergie)
- [Les machines](#les-machines)
- [Niveaux, usines et mises à niveau](#niveaux-usines-et-mises-%C3%A0-niveau)
- [Transport et stockage](#transport-et-stockage)
- [Équipement : du jetpack à la MekaSuit](#%C3%A9quipement--du-jetpack-%C3%A0-la-mekasuit)
- [Radiations et nucléaire](#radiations-et-nucl%C3%A9aire)
- [Particularités du serveur](#particularit%C3%A9s-du-serveur)
- [Progrès (advancements)](#progr%C3%A8s-advancements)

## Par où commencer

La progression de Mekanism suit un fil conducteur : **osmium → acier → alliages
→ circuits → machines**. Tout ce qui suit vient directement des recettes du mod.

1. **Trouve de l'osmium** (voir les minerais). Un minerai, un minerai brut ou
   une poussière d'osmium se fond au four (ou haut-fourneau) en **Lingot
   d'osmium**. Ça marche pareil pour l'**étain** et le **plomb**.
2. **L'acier** : on infuse du **carbone** dans du fer. Le carbone vient du
   charbon (10 unités par charbon, 20 par charbon de bois, 80 par Carbone
   enrichi), via l'**Infuseur métallurgique**. *Fer enrichi* = lingot (ou
   poussière) de fer + 10 mB de carbone ; puis, avec encore 10 mB de carbone,
   le Fer enrichi donne de la **Poussière d'acier**, qu'on fond en **Lingot
   d'acier**.
3. **Les alliages** — ils s'infusent aussi à l'Infuseur métallurgique :

   | Alliage | Ingrédient + infusion |
   |---|---|
   | **Alliage infusé** | 1 lingot de **cuivre** + 10 mB de redstone |
   | **Alliage renforcé** | 1 alliage infusé + 20 mB de diamant |
   | **Alliage atomique** | 1 alliage renforcé + 40 mB d'obsidienne raffinée |

   (La poussière de redstone, de diamant ou d'obsidienne raffinée donne 10 mB ;
   la version *enrichie* en donne 80.) L'« alliage de base » des recettes est
   simplement de la **poussière de redstone**.
4. **Les circuits de contrôle** :

   | Circuit | Fabrication |
   |---|---|
   | **de base** | 1 lingot d'osmium + 20 mB de redstone (Infuseur métallurgique) |
   | **avancé** | 1 circuit de base + 60 mB de redstone, *ou* à l'établi : alliage infusé + circuit de base + alliage infusé (en ligne) |
   | **d'élite** | 1 circuit avancé + 120 mB de diamant, *ou* à l'établi : alliage renforcé + circuit avancé + alliage renforcé |
   | **ultime** | 1 circuit d'élite + 240 mB d'obsidienne raffinée, *ou* à l'établi : alliage atomique + circuit d'élite + alliage atomique |

5. **Le Boîtier en acier** (*Steel Casing*), base de presque toutes les
   machines : `SGS / GOG / SGS` avec **S** = lingot d'acier (4 coins), **G** =
   verre (4 côtés) et **O** = lingot d'osmium (au centre).
6. **Les premières machines** : toutes ont la même forme — un Boîtier en acier
   au centre, entouré de circuits et d'alliages.

   | Machine | Recette (`ligne / ligne / ligne`) |
   |---|---|
   | **Chambre d'enrichissement** | `ACA / IXI / ACA` : A = poussière de redstone, C = circuit de base, I = lingot de fer, X = Boîtier en acier |
   | **Broyeur** (*Crusher*) | `RCR / BXB / RCR` : R = poussière de redstone, C = circuit de base, B = **seau de lave**, X = Boîtier en acier |
   | **Infuseur métallurgique** | `I#I / ROR / I#I` : I = lingot de fer, # = Fourneau, R = poussière de redstone, O = lingot d'osmium |
   | **Fonderie électrique** | `ACA / GXG / ACA` : A = redstone, C = circuit de base, G = verre, X = Boîtier en acier |
   | **Compresseur d'osmium** | `ACA / BXB / ACA` : A = alliage infusé, C = circuit avancé, B = seau, X = Boîtier en acier |
   | **Chambre de purification** | `ACA / OPO / ACA` : A = alliage infusé, C = circuit avancé, O = lingot d'osmium, P = Chambre d'enrichissement |
   | **Chambre d'injection chimique** | `ACA / I#I / ACA` : A = alliage renforcé, C = circuit d'élite, I = lingot d'or, # = Chambre de purification |
   | **Combineur** | `ACA / _X_ / ACA` : A = alliage renforcé, C = circuit d'élite, _ = pierre taillée, X = Boîtier en acier |

7. Fabrique une **Tablette d'énergie** (`RIR / AIA / RIR` : R = redstone, I =
   lingot d'or, A = alliage infusé), un **Configurateur**, et un **Cube
   énergétique de base** pour stocker l'énergie.

## Les minerais

Mekanism ajoute **5 minerais** à tous les biomes de l'**Overworld** (chacun en
version pierre et en version *des abîmes*, dans l'ardoise) : l'**osmium**,
l'**étain**, le **plomb**, l'**uranium** et la **fluorite**. Il ajoute aussi du
**sel**, en disques dans l'eau, sur le fond des **océans**. Chaque minerai a
des **filons** de plusieurs types, qui diffèrent par la profondeur et la taille.

Pour chaque ligne, « essais » = nombre de tentatives de filon **par chunk** :
un essai tombe parfois dans le vide ou dans un autre bloc, et n'en donne alors
pas. Altitudes de l'Overworld (Y de −64 à 319).

| Minerai | Filon | Profondeur (Y) | Essais / chunk | Taille max d'un filon |
|---|---|---|---|---|
| **Osmium** | haut | de **72** jusqu'en haut du monde (zone des montagnes) | 65 | 7 |
| | milieu | −32 → 56 | 6 | 9 |
| | petit | −64 → 64 (répartition uniforme) | 8 | 4 |
| **Étain** | petit | −20 → 94 | 14 | 4 |
| | gros | −32 → 72 | 12 | 9 |
| **Plomb** | normal | fond du monde → 64 | 8 | 9 |
| **Uranium** | petit | −64 → 8 | 4 | 4 |
| | enterré | fond du monde → −8 | 7 | 9 |
| **Fluorite** | normal | −64 → 23 (uniforme) | 5 | 5 |
| | enterré | −64 → 4 | 3 | 13 |
| **Sel** | disques | sur le fond de l'océan, dans l'eau | 2 | rayon 2 à 3, épaisseur 3 |

Détails utiles :

- Sauf pour le filon « petit » d'osmium et la fluorite « normale » (répartition
  uniforme), la répartition est **en trapèze** : le minerai est plus fréquent
  au milieu de la plage de profondeur qu'aux extrémités.
- Les filons **enterrés** d'uranium et de fluorite évitent l'air : le filon
  d'**uranium enterré** perd 75 % des blocs exposés à l'air, celui de
  **fluorite enterrée** ne touche jamais l'air — il ne se voit pas depuis une
  grotte.
- Le plomb perd 25 % des blocs exposés à l'air.
- Le filon d'osmium « haut » a le plus d'essais (65 par chunk), mais il n'existe
  qu'à partir de Y 72 : il se trouve sur les reliefs, et beaucoup d'essais
  tombent dans l'air.
- Osmium, étain, plomb et uranium donnent du **minerai brut** (comme le fer),
  qui se compacte en blocs bruts.
- Le **Combineur** recompose un minerai à partir de 8 minerais bruts + 1 pierre
  taillée (ou ardoise des abîmes taillée).

### Les minerais dans les zones déjà explorées

Les minerais d'un mod n'apparaissent normalement que dans les chunks générés
**après** son installation. Notre carte était déjà largement explorée avant
l'arrivée de Mekanism : le serveur utilise donc la **régénération intégrée à
Mekanism** (`enableRegeneration`). Quand un ancien chunk est rechargé, Mekanism
y ajoute ses minerais et son sel. Concrètement :

- Si tu ne vois **aucun minerai** de Mekanism dans une zone ancienne, laisse
  le chunk se recharger (éloigne-toi puis reviens, reconnecte-toi) ; ça peut
  demander **deux chargements** avant que la zone soit complète.
- Les chunks **neufs** n'ont pas besoin de ça : ils contiennent déjà les
  minerais.

## Traiter un minerai : ×2 à ×5

C'est le cœur du mod : chaque étape supplémentaire multiplie le rendement d'un
minerai. Exemple avec le **fer** (les autres métaux — osmium, étain, plomb,
uranium, cuivre, or — suivent la même chaîne) :

| Palier | Chaîne | Rendement par minerai |
|---|---|---|
| **×1** | Four | 1 lingot |
| **×2** | **Chambre d'enrichissement** | **2 poussières** |
| **×3** | **Chambre de purification** (+ oxygène) → **3 amas** → **Broyeur** → 3 poussières sales → **Chambre d'enrichissement** | **3 poussières** |
| **×4** | **Chambre d'injection chimique** (+ acide chlorhydrique) → **4 fragments** → **Chambre de purification** (+ oxygène) → 4 amas → Broyeur → 4 poussières sales → Chambre d'enrichissement | **4 poussières** |
| **×5** | **Chambre de dissolution chimique** (+ acide sulfurique) → 1000 mB de **boue sale** → **Laveuse chimique** (+ eau) → boue propre → **Cristalliseur chimique** → **5 cristaux** → Chambre d'injection (+ acide chlorhydrique) → 5 fragments → ... → 5 poussières | **5 poussières** |

Les **minerais bruts** se traitent aussi : 3 minerais bruts donnent 4 poussières
(Chambre d'enrichissement), 3 donnent 8 fragments (injection) et 3 donnent
2000 mB de boue sale (dissolution).

Les produits chimiques dont ces machines ont besoin :

| Besoin | Où le trouver |
|---|---|
| **Oxygène** | Séparateur électrolytique : 2 mB d'eau → 2 mB d'hydrogène + 1 mB d'oxygène |
| **Acide chlorhydrique** | Poussière de **sel** → 2 mB d'acide ; ou 1 mB d'hydrogène + 1 mB de chlore à l'Infuseur chimique |
| **Acide sulfurique** | Poussière de **soufre** → 2 mB d'acide ; ou dioxyde de soufre + oxygène → trioxyde de soufre, puis + vapeur d'eau |
| **Soufre** | Poudre à canon + acide chlorhydrique (Chambre d'injection), ou gazéification du charbon (Chambre de réaction pressurisée) |
| **Sel** | Cristallisation de saumure (15 mB → 1 sel), ou récolte au fond de l'océan (bloc de sel → 4 sel) |
| **Saumure** | Eau → saumure (évaporation, 10 mB d'eau → 1 mB) ou sel → saumure (oxydation, 15 mB) |

> Les paliers **×3 et plus** (et surtout ×4 et ×5) sont des machines d'élite
> et ultimes : la Chambre de dissolution, la Laveuse et le Cristalliseur
> demandent des **circuits ultimes** et de l'**obsidienne raffinée**.

## L'énergie

Mekanism calcule en **Joules (J)**, mais l'**affichage par défaut est en FE**
(Forge Energy) sur tout le jeu. La conversion est fixe sur ce serveur :

> **1 FE = 2,5 J** — soit **1 J = 0,4 FE**.

Les mods d'énergie extérieurs (comme Create Crafts & Additions) parlent FE ;
ils se branchent sur les machines et câbles de Mekanism sans adaptateur.

### Stocker l'énergie

| Niveau | Cube énergétique (capacité) | Débit max |
|---|---|---|
| **de base** | 4 000 000 J (1 600 000 FE) | 4 000 J/t (1 600 FE/t) |
| **avancé** | 16 000 000 J (6 400 000 FE) | 16 000 J/t (6 400 FE/t) |
| **d'élite** | 64 000 000 J (25 600 000 FE) | 64 000 J/t (25 600 FE/t) |
| **ultime** | 256 000 000 J (102 400 000 FE) | 256 000 J/t (102 400 FE/t) |

La **Matrice à induction** (multibloc : *Structure à induction*, *Port à induction*,
cellules et fournisseurs) stocke beaucoup plus. Capacité **par cellule** :
8 000 000 000 J (de base), 64 Md J (avancée), 512 Md J (d'élite), 4 000 Md J
(ultime). Débit **par fournisseur** : 256 000 / 2 048 000 / 16 384 000 /
131 072 000 J/t.

### Transporter l'énergie : les câbles universels

| Niveau | Débit d'énergie |
|---|---|
| **de base** | 8 000 J/t (3 200 FE/t) |
| **avancé** | 128 000 J/t (51 200 FE/t) |
| **d'élite** | 1 024 000 J/t (409 600 FE/t) |
| **ultime** | 8 192 000 J/t (3 276 800 FE/t) |

Le **Câble universel de base** se fabrique par 8 : `S#S` avec **S** = lingot
d'acier et **#** = poussière de redstone. On **améliore** les câbles (et tuyaux,
tubes, transporteurs, conducteurs) une fois posés, par un clic droit avec
l'alliage du niveau suivant.

### Produire de l'énergie

Mekanism de base ne produit **pas** d'électricité : les générateurs sont dans
**Mekanism Generators** (panneaux solaires, éoliennes, générateur thermique,
turbine, réacteurs...).

## Les machines

Consommation en J/t, avec l'équivalent en FE/t (÷ 2,5). À pleine activité.

| Machine | Rôle | Conso (J/t) | FE/t |
|---|---|---|---|
| **Chambre d'enrichissement** (*Enrichment Chamber*) | minerai → 2 poussières, et de nombreuses autres recettes | 50 | 20 |
| **Broyeur** (*Crusher*) | lingots → poussières ; amas → poussières sales | 50 | 20 |
| **Combineur** (*Combiner*) | combine poussières + pierre taillée en minerai | 50 | 20 |
| **Infuseur métallurgique** (*Metallurgic Infuser*) | infuse un matériau dans un métal (alliages, acier) | 50 | 20 |
| **Fonderie électrique** (*Energized Smelter*) | fourneau électrique | 50 | 20 |
| **Scierie de précision** (*Precision Sawmill*) | bois et sciure plus efficaces | 50 | 20 |
| **Compresseur d'osmium** (*Osmium Compressor*) | poussières + osmium → lingots raffinés | 100 | 40 |
| **Chambre de purification** (*Purification Chamber*) | minerai → 3 amas (+ oxygène) | 200 | 80 |
| **Chambre d'injection chimique** | minerai → 4 fragments | 400 | 160 |
| **Oxydateur chimique** | solide → gaz | 200 | 80 |
| **Infuseur chimique** | mélange deux gaz | 200 | 80 |
| **Chambre de dissolution chimique** | minerai → boue sale | 400 | 160 |
| **Laveuse chimique** | nettoie la boue | 200 | 80 |
| **Cristalliseur chimique** | boue propre → cristaux | 400 | 160 |
| **Séparateur électrolytique** | eau → hydrogène + oxygène ; saumure → sodium + chlore | — | — |
| **Chambre de réaction pressurisée** | réactions à plusieurs ingrédients (HDPE, soufre, pastilles de polonium...) | 5 + énergie propre à la recette | 2 + |
| **Centrifuge à isotope** (*Isotopic Centrifuge*) | déchets nucléaires → plutonium ; UF6 → carburant fissile | 200 | 80 |
| **Mineur digital** (*Digital Miner*) | mine automatiquement dans un rayon, avec des filtres | 1 000 | 400 |
| **Pompe électrique** | pompe n'importe quel fluide (portée 80 blocs) | 100 | 40 |
| **Remplisseur de fluides** (*Fluidic Plenisher*) | remplit une zone de fluide (jusqu'à 4 000 blocs) | 100 | 40 |
| **Assembleur de formules** | fabrique automatiquement d'après une formule | 100 | 40 |
| **Station de modification** | installe des modules sur l'équipement Meka | 400 | 160 |
| **Nucléosynthétiseur antiprotonique** | transforme la matière avec de l'**antimatière** | 100 000 | 40 000 |
| **Stabilisateur dimensionnel** | **garde un chunk chargé** | 5 000 | 2 000 |
| **Laser** | faisceau qui coupe des blocs / blesse | 10 000 | 4 000 |
| **Vibrateur sismique** + **Lecteur sismique** | scanne les couches du sous-sol | 50 | 20 |
| **Plaque de rechargement** (*Chargepad*) | recharge tout objet à batterie, de n'importe quel mod | jusqu'à 1 024 000 | jusqu'à 409 600 |

Autres blocs à connaître :

- **Chauffeur électrique** et **Chauffeur à combustion** (*Fuelwood Heater*) :
  produisent de la chaleur pour l'évaporateur thermique ou la chaudière. Le
  chauffeur électrique convertit l'énergie en chaleur avec 60 % d'efficacité.
- **Évaporateur thermique** (multibloc de blocs de cuivre) : eau → saumure
  (avec de la chaleur ou des panneaux solaires).
- **Chaudière thermoélectrique** (*Boiler Casing*) : transforme de l'eau en
  vapeur pour les turbines (voir Generators).
- **Alarme industrielle** : une alarme sonore, très bruyante.
- **Robit** : un petit robot compagnon qu'on place sur une Plaque de
  rechargement ; il est aussi un ingrédient du **Mineur digital**.
- **Liquéfacteur nutritionnel** : transforme n'importe quel aliment en **pâte
  nutritive** (50 mB par demi-faim) ; **Gourde** (*Canteen*, 64 000 mB) pour la
  porter.
- **Machine à peindre**, **Extracteur** et **Mixeur de pigments** : pour
  colorer blocs et objets avec des pigments stockés.
- **Oredictionificateur** : convertit des objets en leurs équivalents par
  *tags* (pour unifier les ressources entre mods).

## Niveaux, usines et mises à niveau

Presque tous les blocs de Mekanism existent en **4 niveaux** : **de base**,
**avancé**, **d'élite**, **ultime** (plus un niveau *créatif* réservé aux
admins). Les niveaux supérieurs coûtent un **Installateur de niveau**
(`ACA / IPI / ACA` : A = alliage, C = circuit, I = lingot, P = planches) :

| Installateur | Alliage | Circuit | Lingot / gemme |
|---|---|---|---|
| de base | redstone | de base | fer |
| avancé | infusé | avancé | osmium |
| d'élite | renforcé | d'élite | or |
| ultime | atomique | ultime | diamant |

### Les usines (*Factories*)

Une **Usine** est une machine « multiplicateur » : elle traite plusieurs objets
**en parallèle**. Il existe des usines d'enrichissement, de broyage, de
compression, de combinaison, d'infusion, d'injection, de purification, de
sciage et métallurgiques (fonderie). Une usine de base se fabrique à partir de
la machine d'origine :

> Usine d'enrichissement **de base** = `ACA / IPI / ACA` avec **P** = Chambre
> d'enrichissement, **A** = redstone, **C** = circuit de base, **I** = lingot de
> fer. Les niveaux supérieurs utilisent l'usine du niveau précédent comme **P**.

### Les mises à niveau (*Upgrades*)

Les machines acceptent des mises à niveau (glisse-les dans l'interface). Vitesse,
Énergie, Filtre et Ancrage se fabriquent avec `_G_ / A#A / _G_` : 2 verres, 2
alliages infusés et, au centre :

| Mise à niveau | Ingrédient central | Effet (description officielle) |
|---|---|---|
| **Vitesse** | poussière d'osmium | « Augmente la vitesse des machines » |
| **Énergie** | poussière d'or | « Augmente l'efficacité énergétique et la capacité des machines » |
| **Filtre** | poussière d'étain | « Un filtre qui sépare l'eau lourde de l'eau ordinaire » (pompe électrique : 10 mB d'eau lourde par bloc d'eau pompé) |
| **Ancrage** | poussière de diamant | « Garde chargé le tronçon (chunk) d'une machine » |
| **Étouffement** | 4 laines autour d'un lingot, d'une brique ou d'une gemme de fluorite | « Réduit le bruit généré par les machines » |
| **Générateur de roche** | seau d'eau + seau de lave + 1 alliage infusé | « Génère de la pierre ou de la roche au besoin » |

Le réglage `maxUpgradeMultiplier` (10 par défaut) borne l'effet des mises à
niveau.

## Transport et stockage

### Les réseaux

| Réseau | Câble / conduit | Capacité (de base → ultime) | Débit d'extraction |
|---|---|---|---|
| **Énergie** | Câble universel | voir « L'énergie » | — |
| **Fluides** | **Tuyau mécanique** | 2 000 / 8 000 / 32 000 / 128 000 mB | 250 / 1 000 / 8 000 / 32 000 mB/t |
| **Produits chimiques** | **Tube pressurisé** | 4 000 / 16 000 / 256 000 / 1 024 000 mB | 750 / 2 000 / 64 000 / 256 000 mB/t |
| **Objets** | **Transporteur logistique** | — | 1 / 16 / 32 / 64 objets par transfert, vitesse 5 / 10 / 20 / 50 |
| **Chaleur** | **Conducteur thermique** | isolation 10 / 400 / 8 000 / 100 000 | — |

Variantes de transporteur : **restrictif** (« utilisé uniquement si aucune
autre voie n'est disponible »), **diversif** (contrôlable par redstone). Le
**Trieur logistique** (*Logistical Sorter*) trie par filtre. Le **Lecteur
réseau** (*Network Reader*) affiche le contenu d'un réseau.

### Le stockage

| Bloc | Niveaux (base → ultime) |
|---|---|
| **Conteneur** (*Bin*) : un seul type d'objet | 4 096 / 8 192 / 32 768 / 262 144 objets |
| **Réservoir de fluide** | 32 000 / 64 000 / 128 000 / 256 000 mB |
| **Réservoir chimique** | 64 000 / 256 000 / 1 024 000 / 8 192 000 mB |
| **Réservoir dynamique** (multibloc) | **350 000 mB de fluide par bloc** de volume |

Autres solutions de stockage :

- **Coffre personnel / Baril personnel** : 54 emplacements, **s'ouvrent de
  n'importe où**, même depuis ton inventaire.
- **Système QIO (OQO)** — *Quantum Item Orchestration* : un **Serveur** (*Drive
  Array*) qui reçoit des **Disques** (*Base*, *Hyper-dense* avec des pastilles de
  plutonium, *Supermassif*, *Dilateur de temps*), un **Tableau de bord**
  (écran et établi intégré), des **Importeurs / Exporteurs** et un **Adaptateur
  redstone**. Il demande des **circuits ultimes** et des **Noyaux de
  téléportation**.
- **Entangloporteur quantique** : transmet instantanément énergie, fluides,
  produits chimiques et objets, à **n'importe quelle distance et entre
  dimensions**, via une fréquence partagée.
- **Boîte en carton** (*Cardboard Box*, 4 poussières de bois) : **déplace un bloc**
  avec son contenu. Les blocs interdits sont les lits, les portes, les
  *Trial Spawner* et les coffres-forts (*Vault*), ainsi que ce qui est marqué
  « déplacement non supporté ».

### La téléportation

- **Téléporteur** (*Teleporter*) : deux cadres reliés par une fréquence. Le
  coût en énergie d'un saut est de **1 000 J + 10 J par bloc de distance**,
  plus **10 000 J** si on change de dimension.
- **Téléporteur portable** : ouvre une liste de téléporteurs à distance. Sur ce
  serveur, la téléportation se déclenche **5 secondes (100 ticks)** après le
  clic (instantanée par défaut dans le mod).
- **Noyau de téléportation** : l'ingrédient de base de toutes ces machines
  (4 perles de l'Ender, 2 alliages atomiques, 1 diamant, 2 lingots d'or).

## Équipement : du jetpack à la MekaSuit

### Équipement de départ

| Objet | Ce qu'il fait |
|---|---|
| **Jetpack** | Vol propulsé à l'**hydrogène** (réservoir de 24 000 mB). Version **blindée** (armure 8). |
| **Masque** et **Réservoir de plongée** | Respirer sous l'eau avec de l'oxygène ; filtre aussi les contaminants. |
| **Coureuses** (*Free Runners*) | Annulent les dégâts de chute en consommant de l'énergie (64 000 J). Version blindée disponible. |
| **Tenue hazmat** (masque, robe, pantalon, bottes) | Protège des **radiations** (en plomb, teintes orange et noire). |
| **Compteur Geiger** et **Dosimètre** | Mesurent la radioactivité ambiante et la dose que tu as reçue. |
| **Lance-flamme** | Brûle ; **allume des feux** (voir réglages). Réservoir d'hydrogène 24 000 mB. Sur ce serveur, il **ne détruit pas** les objets au sol qu'il ne peut pas cuire (il le fait par défaut dans le mod). |
| **Arc électrique** | Arc à énergie (120 000 J) ; mode flamme. |
| **Configurateur**, **Carte de configuration** | Règlent les faces d'une machine / copient une configuration. |
| **Dictionnaire** | Montre les *tags* de n'importe quel bloc, objet ou fluide. |

### Le Désassembleur atomique

Une pioche-épée électrique (1 000 000 J, recharge 5 000 J/t). Modes **lent** et
**rapide** (le mode **extraction de filon** est **désactivé** sur ce serveur).
Comme arme : **jusqu'à 7 points de dégâts bonus (3,5 cœurs)** s'il lui reste au
moins 2 000 J, **4 points** sinon. C'est le niveau d'une épée en netherite ;
le mod en donne **20** par défaut (10 cœurs), réduit ici pour le PvP.

### L'Outil Meka et la MekaSuit

Les pièces **Meka** sont la fin de partie : **Casque, Plastron, Pantalon, Bottes
Meka** et l'**Outils Meka** (*Meka-Tool*). **Chaque pièce se fabrique en
améliorant la pièce en netherite correspondante** avec :

- 2 **pastilles de polonium** (`A`) ;
- 1 **circuit de contrôle ultime** (`C`) ;
- 4 **feuilles de PE-HD** (`P`) ;
- 1 **Cellule à induction de base** (`E`).

Recette : `PCP / P#P / AEA` avec **#** = la pièce en netherite (casque,
plastron, jambières ou bottes). L'**Outils Meka** suit la même logique à partir
d'un **Désassembleur atomique** : `CoC / P#P / AEA` avec **#** = le
Désassembleur, **C** = 2 circuits ultimes, **o** = un Configurateur, **P** = 2
feuilles de PE-HD, **A** = 2 pastilles de polonium, **E** = 1 Cellule à
induction de base.

**Le PE-HD** (le plastique des pièces Meka) se fabrique à la **Chambre de réaction
pressurisée** :

1. **Substrat** : 2 biocarburants + 100 mB d'hydrogène + 10 mB d'eau → 1
   *Substrat* **et** 100 mB d'éthylène.
2. **Pellet de PE-HD** : 1 Substrat + 50 mB d'éthylène (sous forme de fluide) +
   10 mB d'oxygène → 1 *Pellet de PE-HD*.
3. **Feuille de PE-HD** : 3 pellets à la Chambre d'enrichissement → 1 feuille.

Les chiffres de base (modifiables par les modules) :

- **Armure** : casque 3, plastron 8, pantalon 6, bottes 3 = **20** en tout,
  **robustesse 3** et **résistance au recul 0,1** par pièce (mêmes valeurs que
  la netherite).
- **Énergie** : 16 000 000 J de base par pièce, recharge 100 000 J/t. Elle
  augmente fortement avec les modules d'énergie.
- **Absorption** : tant que la combinaison est **complète** et a **de
  l'énergie**, elle absorbe **la moitié (50 %)** des dégâts « ordinaires »
  (coups de joueurs et de monstres, flèches, explosions : tout ce qui ne
  contourne pas l'armure), au prix de **100 000 J par point de dégât absorbé**.
  Le mod en absorbe **100 %** par défaut, ce qui rend invulnérable : c'est
  réduit ici. Le casque, avec l'Unité de purification d'inhalation, absorbe
  **50 %** des dégâts magiques (potions de dégâts, poison). Les bottes absorbent
  toujours **100 %** des chutes (50 J par demi-cœur). Les dégâts de
  l'environnement (feu, lave, foudre, cactus, wither...) restent absorbés à
  100 % tant que la combinaison a de l'énergie : c'est fixé par le mod, pas par
  un réglage.
- **Outils Meka** : 16 000 000 J, dégâts de base 4, vitesse d'attaque −2,4,
  **téléportation jusqu'à 32 blocs** sur ce serveur (100 par défaut ; 1 000 J
  pour 10 blocs), **extraction de filon étendue** (tous les blocs, pas
  seulement minerais et bûches).

Les **modules** s'installent à la **Station de modification** (qui demande des
pastilles de polonium), sur la pièce qui les accepte (casque, plastron,
pantalon, bottes ou Outils Meka). Les modules disponibles :

| Module | Effet |
|---|---|
| **Unité Jetpack** | Jetpack à hydrogène dans l'armure |
| **Unité de modulation gravitationnelle** | Vol (antimatière) |
| **Unité d'Élytres** | Élytres renforcées PE-HD intégrées (32 000 J par seconde de vol) |
| **Unité de propulsion hydraulique** | Monter et sauter plus haut |
| **Unité de Boost de Locomotive** | Vitesse de sprint et distance de saut |
| **Unité de stabilisation gyroscopique** | Agir comme si on était au sol |
| **Unité de servo motorisé** | Réduit le ralentissement de l'accroupissement |
| **Unité de répulsion hydrostatique** | Moins de résistance de l'eau |
| **Unité de Marche Givrante** | Gèle l'eau sous les pas (hydrogène) |
| **Unité Surfeur d'âme** | Surfer sur le sable des âmes |
| **Unité d'amélioration de vision** | Vision nocturne |
| **Unité de respiration électrolytique** | Oxygène depuis l'eau (et hydrogène pour le jetpack) |
| **Unité de purification d'inhalation** | Annule les effets de potion négatifs |
| **Unité d'injection nutritionnelle** | Se nourrit seul avec de la pâte |
| **Unité d'Attraction Magnétique** | Attire les objets proches |
| **Unité de téléportation** | Se téléporter sur des blocs proches |
| **Unité de bouclier antiradiation** | Protège des radiations |
| **Unité de Dissipation Laser** | Dissipe les lasers |
| **Unité d'énergie** | Augmente la capacité d'énergie |
| **Unité de distribution de charge** | Répartit la charge entre les pièces / l'inventaire |
| **Unité Geiger** / **Unité de Dosimètre** | Affichent la radioactivité et la dose dans le HUD |
| **Unité de modulation de couleur** | Change la couleur de la combinaison |
| **Unité d'amplification d'attaque** | Augmente les dégâts de mêlée |
| **Unité explosive** | Explosions contrôlées qui détruisent les blocs proches |
| **Unité d'escalade de l'excavation** | Mine plus vite |
| **Unité minière de filon** | Mine les filons de minerai et abat les arbres d'un coup |
| **Unité de touché de soie** | Les blocs minés tombent inchangés |
| **Unité de raffinage de minerai** | Augmente le rendement du minerai (Fortune) |
| **Unité de ferme** / **Unité de Cisaillement** | Labour, écorçage, cisaillement |

## Radiations et nucléaire

Les **radiations** sont **activées** sur le serveur. Une matière radioactive
laisse une dose dans l'environnement et sur les joueurs ; passé un seuil de
sévérité (0,1 sur 1), elle donne des **effets négatifs** et peut **tuer**
(progrès « Pas génial, Pas terrible »). Une source radioactive décroît très
lentement (par défaut 10 heures pour éliminer une source de 1 000 Sv/h).

**Protection** : tenue hazmat, ou Unité de bouclier antiradiation sur la
MekaSuit. **Mesure** : Compteur Geiger (environnement), Dosimètre (toi).

**Stockage des déchets** : le **Baril de déchets radioactifs** (512 000 mB) les
laisse **se désintégrer lentement** (1 mB toutes les 20 ticks). **Attention :
casser ce baril libère son contenu dans l'air.**

### La chaîne de l'uranium

1. **Minerai d'uranium** → lingots d'uranium (au four) ou poussières.
2. **Lingot d'uranium → 2 Yellowcake** (Chambre d'enrichissement).
3. **Yellowcake → Oxyde d'uranium** (Oxydateur chimique, 250 mB).
4. **Fluorite** (minerai : 6 fluorites par minerai à la Chambre d'enrichissement)
   **+ acide sulfurique → Acide fluorhydrique** (Chambre de dissolution).
5. **Oxyde d'uranium + acide fluorhydrique → Hexafluorure d'uranium (UF₆)**
   (Infuseur chimique).
6. **UF₆ → Carburant fissile** (Centrifuge à isotope).
7. Le **carburant fissile** alimente le **réacteur à fission** (page *Mekanism
   Generators*), qui produit de l'énergie et des **déchets nucléaires**.
8. **Déchets nucléaires → Polonium** (Activateur à neutrons solaires, 10 mB →
   1 mB) **ou Plutonium** (Centrifuge à isotope, 10 mB → 1 mB).
9. **Polonium / Plutonium → Pastille** (Chambre de réaction pressurisée : 1 000 mB
   de produit + 1 000 mB d'eau + poussière de fluorite → 1 pastille).
10. Le polonium permet l'**antimatière** (CPC / SPS) et les **pièces Meka**.

> La **MekaSuit** et l'**Outils Meka** demandent donc de **construire et exploiter
> un réacteur à fission** (et d'en traiter les déchets) : c'est volontairement
> très long, et ça passe par un réacteur qui peut **exploser** (voir Generators).

### Le Nucléosynthétiseur antiprotonique

Avec de l'**antimatière**, il transforme la matière. Quelques recettes (le coût
est en mB d'antimatière) :

| Entrée | Sortie | Antimatière |
|---|---|---|
| Lingot d'étain | Lingot de fer | 1 mB |
| Charbon | Diamant | 4 mB |
| Diamant | Émeraude | 4 mB |
| Pomme dorée | **Pomme dorée enchantée** | 3 mB |
| Œuf | **Œuf de dragon** | 4 mB |
| Étoile du Nether | Cœur de la mer | 5 mB |
| Épée en diamant | **Trident** | 4 mB |
| Crâne de squelette | **Crâne de Wither squelette** | 5 mB |
| Balise | Cristal de l'End | 3 mB |
| Coffre en bois | Coffre de l'Ender | 2 mB |
| Arc | Arbalète | 1 mB |
| Améthyste | Éclat d'écho | 2 mB |
| Lit | Ancre de réapparition | 3 mB |

## Particularités du serveur

### Réglages

Les réglages de Mekanism sont dans `config/Mekanism/*.toml` (⚠️ avec une
**majuscule** : sur un serveur Linux, `mekanism` et `Mekanism` sont deux
dossiers différents). Tout est aux valeurs par défaut du mod, **sauf** :

- **la régénération des minerais**, activée à cause de la carte déjà explorée
  (`world.toml` : `enableRegeneration = true`, `userWorldGenVersion = 1`) ;
- **l'équilibrage PvP** dans `gear.toml` (6 valeurs, détaillées plus bas).

| Réglage | Valeur | Conséquence |
|---|---|---|
| Régénération des minerais | **activée** | Les anciens chunks reçoivent les minerais de Mekanism en se rechargeant. |
| Affichage de l'énergie | **FE** | Les interfaces affichent des FE, pas des Joules. |
| Conversion FE → J | **2,5** | |
| Chargement de chunks | **autorisé** | Le **Stabilisateur dimensionnel** et la mise à niveau **Ancrage** gardent des chunks chargés. |
| Dégâts du monde (lasers, lance-flamme) | **activés** | Un **laser** peut casser des blocs ; le **lance-flamme** peut allumer des feux. |
| Rayon du Mineur digital | 32 blocs max | 1 bloc / 80 ticks sans mises à niveau. |
| Portée du laser | 64 blocs | 100 000 J par niveau de dureté de bloc. |
| Radiations | **activées** | |
| Protection des machines | **autorisée** | Les joueurs peuvent verrouiller leurs machines (**Bureau de sécurité**). Les opérateurs ne contournent **pas** cette protection. |
| Boîte en carton | **sans restriction de mod** | Peut déplacer des blocs de tous les mods (sauf lits, portes, *Vault*, *Trial Spawner*). |
| Désassembleur atomique : extraction de filon | désactivée | |
| Outils Meka : extraction de filon étendue | activée | |
| **PvP** — absorption des dégâts ordinaires par la MekaSuit | **50 %** (défaut : 100 %) | `unspecifiedDamageReductionRatio` |
| **PvP** — absorption des dégâts magiques (casque) | **50 %** (défaut : 100 %) | `magicDamageReductionRatio` |
| **PvP** — dégâts bonus max du Désassembleur atomique | **7** (défaut : 20) | `maxDamage` ≈ épée en netherite |
| **PvP** — portée de téléportation de l'Outils Meka | **32 blocs** (défaut : 100) | `maxTeleportReach` |
| **PvP** — délai du Téléporteur portable | **100 ticks / 5 s** (défaut : 0) | `delay` |
| **PvP** — le lance-flamme détruit les objets au sol | **non** (défaut : oui) | `destroyItems` |

### Points d'attention (pour les admins)

- **PvP — réglages appliqués** : `config/Mekanism/gear.toml` réduit les points
  qui rendaient la fin de partie injuste en combat (voir le tableau ci-dessus).
  Restent **non réglables** par config : les **modules** (par exemple l'Unité
  d'amplification d'attaque, ou le vol) ne se règlent pas en `.toml`.
  Restent **inchangés** : le **laser** (un laser et son amplificateur peuvent
  tuer à distance et casser des blocs), le **jetpack** et le vol de la MekaSuit.
  Seule la filière nucléaire (réacteur à fission et traitement de ses déchets)
  barre l'accès à la MekaSuit : à surveiller de près.
- **Pour revenir aux valeurs du mod** : remets les 6 valeurs du tableau à leur
  défaut dans `gear.toml` (serveur éteint).
- **Nucléosynthétiseur** : peut créer des **Œufs de dragon**, des **Pommes
  dorées enchantées**, des **Tridents**, des **Crânes de Wither**... avec de
  l'antimatière (donc du polonium). Voir plus haut.
- **Chunks chargés** : le Stabilisateur dimensionnel et l'**Ancrage** peuvent
  charger de nombreux chunks ; pour interdire ça, mettre
  `allowChunkloading = false` dans `general.toml`.
- **Lasers et lance-flamme** : `aestheticWorldDamage = false` les empêche de
  casser des blocs / d'allumer des feux.
- **Boîte en carton** : on peut interdire un mod entier avec
  `modBlacklist` dans `general.toml`.
- **Compatibilité** : l'énergie de Mekanism se mélange avec celle de **Create
  Crafts & Additions** (FE). Mekanism Generators est un module à part (page
  dédiée).

## Progrès (advancements)

Mekanism ajoute 97 progrès. Quelques-uns, pour t'orienter :

| Progrès | Comment l'obtenir |
|---|---|
| **Premiers pas** | Acquérir des ressources naturelles de Mekanism |
| **L'Alliage à l'origine de tout** | Infuser du cuivre avec de la redstone |
| **Révolution Industrielle** | Infuser du fer avec du carbone et répéter (acier) |
| **La Fondation Parfaite** | Fabriquer un Boîtier en acier |
| **En tirer plus avec moins** | Fabriquer une Chambre d'enrichissement |
| **Le plus fou pour votre argent** | Chambre de dissolution, Laveuse et Cristalliseur |
| **Besoin de plus de viteeeeesse !** | Fabriquer un Désassembleur atomique |
| **Piégé à l'intérieur** | Transformer son meilleur ami en Mineur digital |
| **Vol alimenté par l'hydrogène** | Voler avec un Jetpack |
| **Regarde, mais ne le mange pas** | Fabriquer du Yellowcake |
| **Polonium, pas Plutonium** / **Plutonium, pas polonium** | Raffiner les déchets nucléaires |
| **Matériau impossible** | Créer de l'antimatière |
| **Mékaniste** | Porter une MekaSuit complète avec un Outils Meka |
| **Dévouement sérieux** | Maximum de tous les modules sur la MekaSuit et l'outil |
| **Stabiliser l'Univers** | Dimensional Stabilizer et mise à niveau d'ancrage |
