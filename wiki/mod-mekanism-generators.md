# Mekanism Generators

![Mekanism Generators](https://cdn.modrinth.com/data/OFVYKsAk/ea185eb1300a64867f89101d4798e71a54ef6bed_96.webp)

Mekanism Generators est le module **énergie** de Mekanism : des générateurs
simples (solaire, éolien, thermique, biomasse, gaz) et trois **multiblocs de
fin de partie** — la **turbine industrielle**, le **réacteur à fission** (uranium)
et le **réacteur à fusion** (deutérium + tritium). Il ne fonctionne qu'avec
**Mekanism**, dont il utilise les machines, câbles et produits chimiques :
lis d'abord la page *Mekanism*.

- **Modrinth** : [modrinth.com/mod/mekanism-generators](https://modrinth.com/mod/mekanism-generators)
- **Wiki officiel** : [wiki.aidancbrady.com](https://wiki.aidancbrady.com/wiki/Main_Page)
- **Version installée** : 10.7.19 pour NeoForge 1.21.1

> **Les unités** — Mekanism calcule en **Joules (J)** mais **affiche des FE** :
> **1 FE = 2,5 J**. Les productions ci-dessous sont données dans les deux unités.
> Une valeur « par tick » est « par 1/20 de seconde » : × 20 pour avoir des FE/s.

## Sommaire

- [Les générateurs simples](#les-g%C3%A9n%C3%A9rateurs-simples)
- [La turbine industrielle](#la-turbine-industrielle)
- [Le réacteur à fission](#le-r%C3%A9acteur-%C3%A0-fission)
- [Le réacteur à fusion](#le-r%C3%A9acteur-%C3%A0-fusion)
- [Les modules de MekaSuit](#les-modules-de-mekasuit)
- [Particularités du serveur](#particularit%C3%A9s-du-serveur)
- [Progrès (advancements)](#progr%C3%A8s-advancements)

## Les générateurs simples

| Générateur | Production (J/t) | Production (FE/t) | Stockage interne |
|---|---|---|---|
| **Panneau solaire** (*Solar Generator*) | **50** (en pointe) | 20 | 96 000 J |
| **Panneau solaire avancé** | **300** (en pointe) | 120 | 200 000 J |
| **Éolienne** (*Wind Generator*) | **60 à 480**, selon l'altitude | 24 à 192 | 200 000 J |
| **Bio-Générateur** | **350** | 140 | 160 000 J |
| **Générateur thermique** (*Heat Generator*) | **200** + 30 par face contre de la lave + 100 dans le Nether | 80 + 12 par face + 40 dans le Nether | 160 000 J |
| **Générateur à combustion de gaz** | selon le gaz brûlé | — | — |

À savoir pour chacun :

- **Solaire** : il lui faut le **ciel** et la **lumière du jour**. La valeur de
  production est un **maximum** — « elle peut aller plus haut dans des
  environnements extrêmes ». L'avancé produit 6 fois plus.
- **Éolienne** : « plus efficace en haute altitude ». Elle ne produit à plein
  que haut dans le monde ; la plage d'altitude prise en compte commence à **Y 24**
  (en dessous, c'est le minimum de 60 J/t) et va jusqu'en haut du monde. Si son
  interface affiche **Pas de vent** ou **Ciel caché** (un bloc la couvre), elle ne
  produit rien : il lui faut un ciel dégagé.
- **Bio-Générateur** : il brûle du **biocarburant** (réservoir de 24 000 mB).
  On obtient du biocarburant en **broyant des plantes** au Broyeur de Mekanism :
  par exemple, *Tarte à la citrouille* → 7, *Citrouille* ou *Pastèque* ou
  *Gâteau* → 6, *Pain* → 4, *Pomme* → 2.
- **Thermique** : il brûle de la **lave** ou d'autres combustibles ; un réservoir
  de 24 000 mB de lave. La base de 200 J/t est augmentée de 30 J/t pour chaque
  côté touchant de la lave, et de 100 J/t s'il est dans une dimension « ultra
  chaude » (le Nether). Il consomme 10 mB de lave pour produire sa base de 200 J.
- **À combustion de gaz** : il brûle des **gaz combustibles** — dont l'**éthylène**
  (« éthène ») et l'**hydrogène** — avec un réservoir de 18 000 mB.

### Les recettes

| Générateur | Recette (`ligne / ligne / ligne`) |
|---|---|
| **Panneau solaire** (objet) | `GGG / RAR / OOO` : G = vitre, R = poussière de redstone, A = alliage infusé, O = lingot d'osmium |
| **Panneau solaire** (le bloc générateur) | `### / AIA / OEO` : # = 3 panneaux solaires (objets), A = alliage infusé, I = lingot de fer, O = lingot d'osmium, E = tablette d'énergie |
| **Panneau solaire avancé** | `PAP / PAP / III` : P = 4 **blocs** Panneau solaire, A = alliage infusé, I = lingot de fer |
| **Éolienne** | ` O / OAO / ECE` : O = lingot d'osmium, A = alliage infusé, E = tablette d'énergie, C = circuit de base |
| **Bio-Générateur** | `RAR / BCB / IAI` : R = redstone, A = alliage infusé, B = biocarburant, C = circuit de base, I = lingot de fer |
| **Générateur thermique** | `III / WOW / CFC` : I = lingot de fer, W = planches, O = lingot d'osmium, C = lingot de cuivre, F = fourneau |
| **Générateur à combustion de gaz** | `OAO / XCX / OAO` : O = lingot d'osmium, A = alliage infusé, X = Boîtier en acier, C = Noyau électrolytique |

## La turbine industrielle

La **Turbine industrielle** transforme de la **vapeur** en électricité.
C'est un multibloc : on la construit à la main et elle se « forme » quand la
structure est valide (l'interface indique sinon ce qui manque). Un mB de vapeur
rapporte au maximum **10 J** (4 FE).

**Les blocs** (recettes) :

| Bloc | Rôle | Recette |
|---|---|---|
| **Structure de Turbine** (×4) | murs et coque | ` S / SOS / S` : S = lingot d'acier, O = lingot d'osmium |
| **Vanne de Turbine** (×2) | entrée de vapeur, sortie d'énergie | 4 Structures de Turbine en croix autour d'un circuit avancé |
| **Ventilation de Turbine** (×2) | évacue la vapeur en excès | 4 Structures de Turbine en croix autour de barreaux de fer |
| **Rotor de Turbine** | axe central | `SAS / SAS / SAS` : S = lingot d'acier, A = alliage infusé |
| **Pale de Turbine** | s'ajoute sur un rotor | ` S / SAS / S` : S = lingot d'acier, A = alliage infusé |
| **Complexe de Rotation** | transmet la rotation aux bobines | `SAS / CAC / SAS` : S = lingot d'acier, A = alliage infusé, C = circuit avancé |
| **Bobine électromagnétique** | convertit en électricité | `SIS / IEI / SIS` : S = lingot d'acier, I = lingot d'or, E = tablette d'énergie |
| **Disperseur de pression** (Mekanism) | répartit la vapeur | `S#S / #A# / S#S` : S = lingot d'acier, # = barreaux de fer, A = alliage infusé |
| **Condensateur à saturation** | recondense la vapeur en eau | `SIS / IBI / SIS` : S = lingot d'acier, I = lingot d'étain, B = seau |

**Les règles de construction** — tirées des messages d'erreur du mod :

- La structure est un **pavé à base carrée dont le côté est un nombre impair** (la
  largeur et la longueur sont **identiques et impaires**), et assez large pour
  contenir la turbine.
- Au centre : une **colonne de rotors** d'un seul tenant, **centrée sous** le
  **Complexe de Rotation**. Il faut **au moins une Pale** sur les rotors.
- Le **Complexe de Rotation** est **centré au-dessus des rotors**.
- Les **Bobines électromagnétiques** se posent **au-dessus du complexe**, en
  contact les unes avec les autres **et** avec le complexe. Il en faut au moins
  une ; chacune supporte **4 pales**.
- Les **Disperseurs de pression** forment **une couche horizontale complète autour
  du Complexe de Rotation**.
- Les **Condensateurs à saturation** sont **au-dessus** de la couche des
  disperseurs (jamais en dessous).
- Les **Ventilations** sont **au même niveau ou au-dessus** de la couche des
  disperseurs (jamais en dessous). Il en faut au moins une.

**Les chiffres** (réglages) : chaque Ventilation débite **32 000 mB/t** de vapeur,
chaque Disperseur **1 280 mB/t**, chaque Condensateur recondense **64 000 mB/t**.
Capacité : **16 000 000 J** d'énergie et **64 000 mB** de vapeur **par bloc de
volume** de la turbine.

La vapeur vient d'une **chaudière thermoélectrique** de Mekanism (eau chauffée),
d'un **réacteur à fission** refroidi à l'eau ou d'un **réacteur à fusion**
refroidi à l'eau.

## Le réacteur à fission

Le **réacteur à fission** brûle du **carburant fissile** (issu de l'uranium,
voir la filière nucléaire dans la page *Mekanism*) et produit de la **chaleur**,
qu'un liquide de refroidissement transforme en vapeur pour une turbine. Son
résidu, les **déchets nucléaires**, est **radioactif**. C'est lui qui donne accès
au **polonium** et au **plutonium**, donc à l'équipement Meka.

**Les blocs** (recettes) :

| Bloc | Recette |
|---|---|
| **Boîtier de réacteur à fission** (×4) | ` I / IXI / I` : I = lingot de plomb, X = Boîtier en acier |
| **Assemblage de Carburant à Fission** | `ISI / ITI / ISI` : I = lingot de plomb, S = lingot d'acier, T = Réservoir chimique de base |
| **Assemblage de Tige de Contrôle** | `ICI / SIS / SIS` : I = lingot de plomb, C = circuit d'élite, S = lingot d'acier |
| **Port de réacteur à fission** (×2) | ` F / FCF / F` : F = Boîtier de réacteur, C = circuit d'élite |
| **Adaptateur logique** | ` R / RFR / R` : R = redstone, F = Boîtier de réacteur |
| **Verre de réacteur** (×4) | `SIS / IGI / SIS` : S = Fer enrichi, I = lingot de plomb, G = verre |

**Principe** — le multibloc est un pavé de boîtiers, avec des **tours
d'Assemblages de Carburant** (empilables) dont chacune est **surmontée d'une
Tige de Contrôle**. Les **Ports** laissent entrer le carburant et le
refroidissement, et sortir le refroidissement chauffé et les déchets ; un port
peut être réglé en **entrée seulement**, **sortie de refroidissement** ou
**sortie de déchets**. L'**Adaptateur logique** permet de surveiller ou
commander le réacteur à la redstone.

**Les chiffres** (réglages) :

- **Vitesse de réaction** maximale = **1 mB/t par assemblage** de carburant ;
  par défaut le réacteur démarre à **0,1 mB/t**. Chaque assemblage contient
  **8 000 mB** de carburant (et de déchets).
- Chaque mB de carburant produit **1 000 000** de chaleur.
- Chaque bloc du multibloc contient **100 000 mB** de refroidissement
  froid et **1 000 000 mB** de refroidissement chauffé.
- Un **liquide de refroidissement** est indispensable (eau → vapeur, ou sodium).
  Un réacteur mal refroidi monte en **dégâts**.
- Si la sortie de **déchets** est remplie à 90 %, le réacteur signale un excès
  de déchets.

> ### ⚠️ La fusion du cœur (meltdown)
>
> Sur ce serveur, **les fusions du cœur sont activées** (réglage par défaut du
> mod). Quand les dégâts du réacteur dépassent **100 %**, il a une chance de
> **fondre** (0,1 % par défaut, qui augmente avec les dégâts) :
>
> - **explosion de rayon 8 blocs** ;
> - la **radioactivité** du carburant et des déchets du réacteur est
>   **multipliée par 50** au moment de l'explosion ;
> - un réacteur reconstruit repart à **75 % de dégâts**.
>
> Si les fusions étaient désactivées, le réacteur se couperait de lui-même au
> lieu d'exploser, et ne pourrait être rallumé qu'après être revenu à des
> températures et des dégâts sûrs. (Le bouton **SCRAM** de l'interface permet
> aussi de l'arrêter à la main.) **Construis le réacteur loin de ta base** et de tout
> ce que tu veux garder.

## Le réacteur à fusion

Le **réacteur à fusion** brûle un mélange **deutérium + tritium** et c'est la
source d'énergie la plus puissante de Mekanism. Il demande de la **fission
d'abord** : ses blocs de structure utilisent des **pastilles de polonium**.

**Les blocs** (recettes) :

| Bloc | Recette |
|---|---|
| **Structure de réacteur à fusion** (×4) | `A#A / #X# / A#A` : A = alliage atomique, # = pastille de polonium, X = Boîtier en acier |
| **Contrôleur de réacteur à fusion** | `CGC / FTF / FFF` : C = circuit ultime, G = vitre, F = Structure de réacteur, T = Réservoir chimique de base |
| **Port de réacteur à fusion** (×2) | ` F / FCF / F` : F = Structure de réacteur, C = circuit ultime |
| **Adaptateur logique** | ` R / RFR / R` : R = redstone, F = Structure de réacteur |
| **Matrice de focalisation laser** (×2) | ` G / GRG / G` : G = Verre de réacteur, R = bloc de redstone |
| **Verre de réacteur** (×4) | `SIS / IGI / SIS` (voir fission) |

La **Matrice de focalisation laser** est un panneau de verre qui absorbe
l'énergie lumineuse d'un **Laser** de Mekanism pour **chauffer** le réacteur et
l'allumer.

**Le combustible** (D-T) :

| Étape | Comment |
|---|---|
| **Eau lourde** | Pompe électrique avec une mise à niveau **Filtre** (10 mB d'eau lourde par bloc d'eau) |
| **Deutérium** | Séparateur électrolytique : 2 mB d'eau lourde → 2 mB de deutérium + 1 mB d'oxygène |
| **Lithium** | Saumure → lithium (évaporation, 10 mB → 1 mB), ou poussière de lithium → 100 mB (oxydation) |
| **Tritium** | Activateur à neutrons solaires : 1 mB de lithium → 1 mB de tritium |
| **Carburant D-T** | Infuseur chimique : 1 mB de deutérium + 1 mB de tritium → **2 mB** de carburant D-T |
| **Hohlraum** | Infuseur métallurgique : 4 poussières d'or + 10 mB de carbone → 1 Hohlraum |

Le **Hohlraum** est une **capsule de carburant** : elle contient jusqu'à
**10 mB** de carburant D-T (se remplit à 1 mB/t) ; elle indique *Prêt pour la
réaction!* quand elle est pleine. Le réacteur stocke jusqu'à **1 000 mB** de
carburant et **1 000 000 000 J** d'énergie. Il peut être refroidi par **air**
(production passive) ou par **eau** (production de vapeur pour la turbine) ; son
interface affiche la température de la structure et celle du plasma.

## Les modules de MekaSuit

Mekanism Generators ajoute deux modules pour la **MekaSuit** (installés à la
Station de modification ; recette `A#A / APA / HHH` : A = alliage renforcé, P =
Base de module, H = pastille de polonium) :

| Module | Recette (centre `#`) | Effet |
|---|---|---|
| **Unité de recharge solaire** | Panneau solaire avancé | Recharge la MekaSuit au soleil : **500 J/t** par module installé |
| **Unité de Générateur Géothermique** | Générateur thermique | Recharge avec la chaleur de l'environnement (**10 J/t** par degré au-dessus de l'ambiant, par module) et réduit les **dégâts de chaleur** (jusqu'à **80 %** avec le maximum de modules) |

## Particularités du serveur

Mekanism Generators fonctionne avec ses **réglages par défaut**
(`config/Mekanism/generators.toml`, `generator-storage.toml`,
`generators-gear.toml`). Point notable :

| Réglage | Valeur | Conséquence |
|---|---|---|
| Fusion du cœur du réacteur à fission | **activée** | Explosion de rayon **8**, radioactivité ×50. |
| Chance de fusion (au-dessus de 100 % de dégâts) | 0,1 % | Augmente avec les dégâts. |
| Dégâts après reconstruction | 75 % | |

> **Pour les admins** : la filière du **polonium** passe par les déchets du réacteur
> à fission ; or le polonium est nécessaire à la MekaSuit, à l'Outils Meka, à
> l'antimatière et au réacteur à fusion. Le réacteur à fission est donc le
> verrou de toute la fin de partie. Pour désactiver les explosions : dans
> `generators.toml`, section `[fission_reactor.meltdowns]`, mets
> `enabled = false`.

## Progrès (advancements)

| Progrès | Comment l'obtenir |
|---|---|
| **Votre premier générateur** | Fabriquer un générateur thermique |
| **Le pouvoir du soleil** | Fabriquer un panneau solaire (« énergie de jour renouvelable ») |
| **Tourne bébé tourne !** | Fabriquer une éolienne |
| **Brûler le gaz** | Fabriquer un générateur à combustion de gaz pour brûler de l'éthène |
