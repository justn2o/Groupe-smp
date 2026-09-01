# Simply Swords

![Simply Swords](https://i.imgur.com/iduZbq5.png)

Simply Swords ajoute des dizaines de nouvelles armes de mêlée — chakrams,
katanas, glaives, marteaux, rapières, faux, lances... — chacune avec son
propre style de combat, ses animations et ses capacités spéciales. Ce n'est
pas qu'un pack de skins : chaque famille d'arme joue différemment, et une
partie du contenu (les armes Uniques) n'est même pas craftable — il faut la
trouver.

- **Modrinth** : [modrinth.com/mod/simply-swords](https://modrinth.com/mod/simply-swords)

## Les familles d'armes

Il existe 15 familles d'armes "standard", chacune avec une capacité propre
qui la différencie des autres (liste non exhaustive) :

- **Katana** — peut infliger le double de dégâts sur certains coups.
- **Rapière** — ignore une partie de l'armure de la cible.
- **Chakram** — arme de jet qui revient vers le joueur.
- **Glaive / Hallebarde / Lance** — portée étendue, touche plusieurs
  ennemis alignés.
- **Grande hache / Grand marteau** — dégâts élevés, attaques lentes et
  souvent des effets de zone.
- **Faux (Scythe)** — dégâts contre plusieurs cibles autour du joueur.
- **Twinblade / Sai / Cimeterre (Cutlass)** — attaques rapides, orientées
  combos.

Deux familles supplémentaires (Dague, Marteau) n'existent que sur certaines
armes Uniques et ne sont pas disponibles en version "standard".

Astuce en jeu : maintenir **Alt** en survolant une arme dans l'inventaire
affiche des informations supplémentaires (statistiques cachées, emplacements
de gemmes, niveau d'Éveil...).

## Progression des matériaux

Chaque famille d'arme suit la progression classique des matériaux vanilla,
plus deux étages ajoutés par le mod :

**Fer → Or → Diamant → Netherite** (forgées normalement), puis :

- **Arme Runique** — on forge une arme Netherite avec une **Tablette
  Runique** (gabarit de forge) et un Diamant (ajout). L'arme obtient un
  **Pouvoir Runique** aléatoire tout en gardant son type et sa capacité de
  base. Un clic sur l'arme non identifiée révèle le pouvoir obtenu. Il est
  possible de reforger (reroll) le pouvoir en répétant la recette avec
  l'arme Runique comme base.
- **Arme Unique** — le sommet de la progression, voir plus bas.

Les armes Runiques se réparent avec des lingots de Netherite. Les Tablettes
Runiques s'obtiennent via le butin des coffres (garanties au bout de 60
ouvertures "éligibles" sans en trouver une, par défaut).

## Les armes Uniques

Les armes Uniques (~52 au total) sont les objets les plus élaborés du mod :
chaque arme a un nom, un type figé, un design unique et une capacité
signature (passive, déclenchée au coup, ou activable au clic droit).

### Comment les obtenir

- **Butin de coffres** — de nombreux coffres (y compris dans des structures
  d'autres mods) ont une chance de faire apparaître une arme Unique. La
  chance de base est très faible (0,05 %), mais un système de "pity"
  personnel augmente les chances après 25 échecs consécutifs et garantit
  une arme Unique au 75ᵉ échec. Le Wither et le Dragon de l'Ender ont des
  chances dédiées bien plus élevées (5 % et 50 %).
- **Reliques Contenues (Contained Remnants)** — objet spécial qui, utilisé
  sur le bon bloc "thématique", produit une arme Unique précise et
  déterministe (par exemple un bloc de fer pour Mjolnir, ou du feu de l'âme
  pour la Lichblade endormie). Tenir la relique en main donne des indices
  sur le bloc recherché.

### L'Éveil (Awakening)

Une arme Unique trouvée en butin commence "endormie" (niveau d'Éveil 0) :
ses dégâts et sa vitesse d'attaque de base sont réduits (50 % / 75 % des
valeurs finales), et sa capacité spéciale reste scellée jusqu'au niveau 4.
On la réveille en la nourrissant de **Tablettes Runiques** dans une **Forge
Runique**, jusqu'au niveau maximum (8), où elle atteint toutes ses
statistiques et capacités complètes. Certaines familles d'armes Uniques
(comme la Lichblade) suivent leur propre progression narrative en plus de
l'Éveil classique.

### Les emplacements de gemmes

Beaucoup d'armes Uniques (et certains objets configurés par l'admin du
serveur) possèdent des **emplacements de gemmes** Runefused et/ou
Netherfused, visibles en tenant Alt sur le tooltip. Une gemme ajoute un
second pouvoir à l'arme :

- **Gemme Runefused** — se forge avec une Tablette Runique, une Relique
  Empouvoirée et de l'Obsidienne Pleureuse.
- **Gemme Netherfused** — se forge avec une Tablette Runique, une Relique
  Empouvoirée et un lingot de Netherite.
  (la Relique Empouvoirée s'obtient en faisant fondre une arme Unique)

On sertit une gemme en la prenant en main et en cliquant sur une arme
compatible ; une gemme déjà en place est éjectée dans l'inventaire. La Forge
Runique permet aussi d'extraire, remplacer ou retirer les gemmes d'une arme.
Les pouvoirs de gemme montent en puissance avec le niveau d'Éveil de l'arme,
comme la capacité Unique elle-même.

### Exemple d'arme Unique — Mjolnir

- **Type** : Marteau — **Réparation** : Tablette Runique
- **Implicite** : réduit l'armure de la cible de 2 à 6 % par coup
- **Effet Unique "Storm"** : les coups rendent l'ennemi "Conducteur"
- **Clic droit** : invoque une tempête mobile qui frappe les ennemis
  proches à répétition avant de se terminer par un coup de tonnerre — les
  ennemis "Conducteurs" libèrent eux-mêmes un mini coup de tonnerre en
  étant touchés.

## Les pouvoirs Runiques

Un pouvoir Runique est une capacité (passive, déclenchée ou activable) qui
peut être gravée sur une arme Netherite pour créer une arme Runique, et que
l'on retrouve aussi sur les gemmes Runefused. Certains pouvoirs peuvent
apparaître en version "Supérieure" (préfixe *Greater*), une variante
renforcée du même effet.

Les capacités actives (que ce soit sur une arme Unique ou via une gemme)
s'utilisent avec les touches dédiées "Use Mainhand/Offhand Weapon Ability"
(à configurer dans les contrôles), ce qui permet de les déclencher même en
combattant à deux armes à la fois.
