# Create Crafts & Additions

![Create Crafts & Additions : blocs et objets](https://cdn.modrinth.com/data/kU1G12Nn/images/cf8302e146a4073891eb5355e1b11380a6a8098d.png)

Create Crafts & Additions (souvent appelé **CCA**) apporte l'**électricité** à
**Create** : on convertit la **rotation** de Create en **énergie électrique**
(FE), on la transporte par **fils**, on la stocke dans des **accumulateurs**, et
on la reconvertit en rotation avec des **moteurs électriques**. Il ajoute aussi
le **laminoir** (tiges et fils métalliques), la **bobine Tesla**, des
combustibles liquides pour le **brûleur à Blaze** et quelques fantaisies
(gâteaux, gobelets).

- **Modrinth** : [modrinth.com/mod/createaddition](https://modrinth.com/mod/createaddition)
- **Code source** : [github.com/mrh0/createaddition](https://github.com/mrh0/createaddition)
- **Version installée** : 1.6.0 pour NeoForge 1.21.1 (nécessite **Create**, déjà
  installé — voir la page *Create*)

> **Voir une recette** — **JEI** est installé : survole un objet dans ton
> inventaire et appuie sur **R** (recette) ou **U** (utilisations).

## Sommaire

- [Principe : rotation ↔ électricité](#principe--rotation--%C3%A9lectricit%C3%A9)
- [Le laminoir, les tiges et les fils](#le-laminoir-les-tiges-et-les-fils)
- [Produire et consommer de l'énergie](#produire-et-consommer-de-l%C3%A9nergie)
- [Les fils et les connecteurs](#les-fils-et-les-connecteurs)
- [L'accumulateur](#laccumulateur)
- [La bobine Tesla](#la-bobine-tesla)
- [Le brûleur à Blaze liquide](#le-br%C3%BBleur-%C3%A0-blaze-liquide)
- [Autres objets](#autres-objets)
- [Réglages du serveur](#r%C3%A9glages-du-serveur)
- [Avec Mekanism](#avec-mekanism)

## Principe : rotation ↔ électricité

Create mesure sa puissance en **SU** (unités de contrainte) et en **tours par
minute (RPM)** ; l'électricité se mesure en **FE** (Forge Energy), la même unité
que celle affichée par Mekanism. CCA fait le pont dans les deux sens :

| Bloc | Sens | À savoir |
|---|---|---|
| **Alternateur** | rotation → **énergie** | Il faut **au moins 32 RPM**. La production dépend de la vitesse d'entrée. |
| **Moteur électrique** | énergie → **rotation** | Vitesse réglable (panneau arrière), jusqu'à **256 RPM**. La consommation dépend du régime réglé. |

Chiffres (réglages par défaut) :

- À **256 RPM**, la conversion de référence est de **480 FE/t**. L'Alternateur a un
  **rendement de 75 %** : d'après ces réglages, il produit donc au maximum
  **360 FE/t** pour une rotation de 256 RPM (la contrainte maximale de
  l'alternateur et du moteur est de **16 384 SU** à cette vitesse).
- Le **Moteur électrique** a une consommation minimale de **8 FE/t** ; il
  accepte jusqu'à **5 000 FE/t** et stocke **5 000 FE**. L'Alternateur transmet
  jusqu'à **5 000 FE/t** et stocke **5 000 FE**.

**Recettes** (à l'**Établi mécanique** de Create — *Mechanical Crafter* —, en
plaçant un ingrédient par établi) :

| Bloc | Ingrédients |
|---|---|
| **Alternateur** | 2 Alliages d'andésite, 6 plaques de fer, 4 **Bobines de fil en cuivre**, 1 tige de fer |
| **Moteur électrique** | 1 Alliage d'andésite, 6 plaques de laiton, 3 Bobines de fil en cuivre, 1 tige de fer, 1 **Condensateur** |

## Le laminoir, les tiges et les fils

Le **Laminoir** (*Rolling Mill*) transforme des lingots en **tiges** et des
plaques en **fils**. Il tourne à la **rotation** de Create : **6 secondes** (120
ticks) par opération, pour une contrainte de **8 SU**. On y dépose des objets
par le dessus (ou en automatique avec un **tapis roulant** et deux
**entonnoirs**, entrée et sortie), et on récupère le résultat avec un clic
droit.

**Recette** : `PSP / ASA / ACA` avec **P** = plaque de fer, **S** = Rotor
(*Shaft*), **A** = Alliage d'andésite, **C** = Boîtier d'andésite.

| Entrée | Sortie |
|---|---|
| Lingot de fer / cuivre / or / laiton / électrum | **2 tiges** du métal |
| Plaque de fer / cuivre / or / électrum | **2 fils** du métal |
| Papier ou bambou | **Paille** (*Straw*) |

Les **plaques d'électrum** et de **zinc** s'obtiennent à la **presse**
mécanique de Create (lingot → plaque).

### L'électrum

L'**électrum** est le métal « noble » de CCA. On l'obtient :

- en **chargeant de l'or avec la bobine Tesla** : Lingot d'or → Lingot d'électrum
  (36 000 FE), Pépite (4 000 FE), Bloc d'or → Bloc d'électrum (324 000 FE),
  Fil et Tige d'or (18 000 FE), Plaque d'or (36 000 FE). Le débit maximal est de
  360 FE/t, soit 100 ticks au minimum pour un lingot ;
- en **mélangeant** (mixeur chauffé) de l'or et de l'argent (2 lingots
  d'électrum) — cette recette ne s'active que si un mod ajoute des lingots
  d'argent ;
- en **broyant** du **Tuf** ou de l'**Ochrum** (Create) : de petites chances
  (jusqu'à 20 % pour l'ochrum, 10 % pour le tuf) de donner des pépites d'électrum.

## Produire et consommer de l'énergie

CCA ne produit pas d'énergie « par lui-même » : **toute l'énergie vient de
la rotation** de Create (roues à eau, moulins, machines à vapeur...) via
l'Alternateur (à part le *Générateur créatif*, réservé aux admins). Pour une centrale plus puissante, on utilise les générateurs de
**Mekanism Generators** (voir cette page), dont l'énergie se branche sur les
réseaux de CCA.

**Stocker de l'énergie portable** : le **Condensateur** (objet) stocke
**5 000 FE** et se recharge par **500 FE** à la fois. Il se fabrique en
colonne : une plaque de zinc et une plaque de cuivre (dans un ordre ou dans
l'autre) au-dessus d'une torche de redstone.

## Les fils et les connecteurs

L'énergie voyage par des **fils** reliant des **connecteurs**.

**Les connecteurs** :

| Connecteur | Tension | Débit | Longueur de fil | Liens max |
|---|---|---|---|---|
| **Petit connecteur** | basse | **1 000 FE/t** | **16 blocs** | 4 autres connecteurs |
| **Petit connecteur lumineux** | basse | 1 000 FE/t | 16 blocs | 4 — **émet de la lumière** (consomme 1 FE/t) |
| **Grand connecteur** | haute | **5 000 FE/t** | **32 blocs** | 6 autres connecteurs |

- Le **Petit connecteur** se fabrique par 3 : 1 tige de cuivre + 1 Alliage
  d'andésite + 1 boule de slime. Le **Grand connecteur** par 2 : 1 tige d'or
  ou d'électrum + 2 Alliages d'andésite + 1 boule de slime.
- Le **Petit connecteur lumineux** : fil de fer + bloc de verre + Petit connecteur.

**Les bobines de fil** : une **Bobine vide** (24 d'un coup avec plaque de fer /
tige de fer / plaque de fer, en colonne) + 4 fils d'un métal (en croix) donne :

| Bobine | Se connecte à |
|---|---|
| **Bobine de fil en cuivre** | connecteurs **basse tension** |
| **Bobine de fil en or** | connecteurs **haute tension** (et petits connecteurs) |
| **Bobine de fil en électrum** | connecteurs **haute tension** (et petits connecteurs) |
| **… avec lumières festives** (cuivre + redstone + biomasse) | comme le cuivre, décorative |

**Poser un fil** : tiens une bobine et fais un **clic droit sur deux
connecteurs**. La bobine devient une **Bobine vide** que tu gardes. Pour
**retirer** un fil : clic droit sur les deux connecteurs avec une Bobine vide,
qui redevient pleine.

**Les modes** : fais un **clic droit avec une clé** sur un connecteur pour le
faire passer en mode **Réception**, **Envoi** ou **Rien**.

Réglages utiles : un réseau de connecteurs a un **tampon interne** de
**80 000 FE** ; les connecteurs se posent sur n'importe quelle face (pas besoin
de support) ; un bloc simplement **collé** à un connecteur peut lui envoyer ou
en recevoir de l'énergie.

**Le Relais à redstone** : laisse passer l'énergie du connecteur d'entrée vers
le connecteur de sortie quand il reçoit un **signal de redstone**. Recette :
` R / CEC / SSS` avec **R** = poussière de redstone, **C** = Petit connecteur (×2),
**E** = Tube électronique de Create, **S** = pierre (×3).

**Les Barbelés** (*Fils barbelés*) : infligent des **dégâts** (2,0, soit 1 cœur)
à qui les traverse. Recette : 4 fils de fer en losange → 2 barbelés.

## L'accumulateur

L'**Accumulateur** est un **multibloc** de stockage d'énergie.

- **2 000 000 FE par bloc.** Dimensions maximales : **3 de large** et **5 de
  haut** (jusqu'à 8 si réglé autrement).
- **Débit** : 5 000 FE/t en entrée et 5 000 FE/t en sortie (on configure un
  connecteur d'entrée et un connecteur de sortie).
- Il **pousse** activement l'énergie vers les blocs placés sur ses faces
  **supérieure et inférieure**, pour mieux s'entendre avec d'autres mods.
- **Recette** : ` R / CBC / W` — **R** = tige de cuivre, **C** = 2 Condensateurs,
  **B** = Boîtier de laiton, **W** = fil d'électrum.

## La bobine Tesla

La **Bobine Tesla** a deux rôles :

1. **Charger des objets** placés **en dessous** : tout ce qui accepte des FE, même
   venant d'un autre mod (**5 000 FE/t**) ; et réaliser les recettes de
   « chargement » (électrum, etc. — **2 000 FE/t** pour les recettes).
2. **Frapper** : avec un **signal de redstone**, elle inflige des dégâts aux
   **joueurs et aux monstres proches** (**3 blocs** autour) et leur donne l'effet
   **Foudroyé** (*Shocking*), qui **immobilise** la cible.

| Réglage | Valeur |
|---|---|
| Énergie consommée par décharge | 1 000 FE |
| Intervalle entre deux décharges | 20 ticks (1 seconde) |
| Dégâts aux monstres | 3 demi-cœurs (1,5 cœur) |
| Dégâts aux joueurs | **2 demi-cœurs (1 cœur)** |
| Durée de l'effet Foudroyé | 20 ticks |
| Entrée max / capacité | 10 000 FE/t / 40 000 FE |

> ⚠️ **La bobine Tesla peut tuer un joueur** (message de mort : « a reçu un
> choc électrique mortel »). Fais attention à l'endroit où tu en poses une, et
> à celles que tu croises.

**Recette** (Établi mécanique) : `SSS / _A_ / CBC / PEP` avec **S** =
3 Bobines de fil en cuivre, **A** = Alliage d'andésite, **C** = 2
Condensateurs, **B** = Boîtier de laiton, **P** = 2 plaques de laiton, **E** =
Tube électronique.

## Le brûleur à Blaze liquide

Donne une **Paille** à un **Brûleur à Blaze** de Create : il devient un
**Brûleur à Blaze avec une paille** et accepte des **combustibles liquides**, par
**seau** ou par **tuyau**. Sa réserve est de **4 000 mB** de liquide et il
stocke jusqu'à **10 000 ticks** de chaleur.

**Combustibles** (durée de chaleur pour **1 000 mB**, soit un seau) :

| Liquide | Durée (ticks) | Durée | Chaleur |
|---|---|---|---|
| **Bioéthanol** (*Biofuel*) | 24 000 | 20 min | **surchauffée** |
| **Lave** | 20 000 | 16 min 40 | normale |
| **Éthanol** | 8 000 | 6 min 40 | normale |
| **Huile de graines** (*Seed Oil*) / huile végétale | 4 800 | 4 min | normale |
| Diesel, essence, biodiesel | 24 000 | 20 min | normale |
| Pétrole brut | 9 600 | 8 min | normale |
| Créosote | 4 800 | 4 min | normale |

Les lignes diesel, essence, biodiesel, éthanol, pétrole brut et créosote ne
s'appliquent que si **un mod ajoute ces liquides** (CCA les reconnaît par leurs
étiquettes de fluide). Les liquides de CCA lui-même sont l'**huile de graines**
et le **bioéthanol**.

**Fabriquer ses carburants** :

- **Huile de graines** : 1 graine compactée (bassin de Create) → 100 mB.
- **Biomasse** : au mixeur **chauffé**, des cultures, fleurs, feuilles, pousses,
  bâtons, rayons de miel ou aliments végétaux **+ 100 mB d'huile de graines**.
  La biomasse se compacte en **Granulé de biomasse** (qui rend 50 mB d'eau) :
  un puissant combustible solide ; 9 granulés se rangent en un bloc.
- **Bioéthanol** : au mixeur, 1 sucre + 1 Farine de braise + 2 biomasses →
  125 mB. Son seau « fonctionne comme un gâteau pour Blaze » : il met le brûleur
  en **surchauffe**.

## Autres objets

- **Papier de verre en diamant** : papier + poussière de diamant ; **1 024
  utilisations** ; polit les objets tenus en main secondaire ou au sol (se
  **déploie** automatiquement avec un déployeur).
- **Poussière de diamant** (*Diamond Grit*) : on **broie** un diamant (300 ticks).
- **Amulette en électrum** : « quand vous êtes au plus bas, la chance va
  tourner ». Se recharge passivement (~**2 FE/t**) quand on la tient en main.
- **Gobelets** (cuivre, or) et **Figurine en laiton** : objets décoratifs.
- **Gâteaux** (*Gâteau au chocolat*, *Gâteau au miel*) : base de gâteau (œuf, 2
  sucres, Pâte de Create) cuite au fumoir, puis remplie de chocolat (500 mB)
  ou de miel (500 mB).
- **Interface d'énergie portable** (*Portable Energy Interface*) : permet d'échanger
  de l'énergie avec un **engin mobile** (contraption) de Create, sans l'arrêter.
  Recette : Boîtier de laiton + Chute + Bobine de fil en cuivre. Un signal de
  redstone empêche l'interface fixe de s'enclencher.
- **Adaptateur numérique** : interface pour **ordinateurs ComputerCraft**. Il n'y
  a pas de ComputerCraft sur le serveur : cet objet n'a pas d'usage.

## Réglages du serveur

CCA fonctionne avec ses **réglages par défaut** (`config/createaddition-common.toml`).
Les plus importants :

| Réglage | Valeur |
|---|---|
| Conversion de référence à 256 RPM | 480 FE/t |
| Rendement de l'alternateur | 75 % |
| Contrainte max alternateur / moteur | 16 384 SU |
| Capacité d'un bloc d'accumulateur | 2 000 000 FE |
| Taille max de l'accumulateur | 3 × 3 × 5 |
| Petit / grand connecteur | 1 000 / 5 000 FE/t ; 16 / 32 blocs |
| Bobine Tesla : portée / dégâts joueur / dégâts monstre | 3 blocs / 1 cœur / 1,5 cœur |
| Effets des amulettes | activés |
| Son des machines | activé |

## Avec Mekanism

L'énergie de **Mekanism** et celle de **CCA** sont toutes deux des **FE** (Mekanism
la convertit à 1 FE = 2,5 J en interne) : on peut donc brancher un Alternateur
de CCA à une machine de Mekanism, ou un générateur de Mekanism Generators à un
réseau de fils de CCA. CCA ajoute aussi deux recettes **dans Mekanism** : le
**Quartz rose** de Create s'obtient par infusion métallurgique (quartz + 80 mB de
redstone), et se polit à la Chambre d'enrichissement.
