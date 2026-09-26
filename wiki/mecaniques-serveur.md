# Mécaniques du Groupe SMP

Cette page décrit les règles de jeu **propres à notre serveur** — celles que
tu ne trouveras dans aucun wiki de mod, parce qu'elles ont été codées ou
réglées spécialement pour nous.

## Sommaire

- [Se connecter : mot de passe obligatoire](#se-connecter--mot-de-passe-obligatoire)
- [Se protéger du PvP](#se-protéger-du-pvp)
- [Poser une prime](#poser-une-prime)
- [Le Cœur de Vie](#le-cœur-de-vie)
- [Le Lait Infini](#le-lait-infini)
- [Solidité V et Protection V](#solidité-v-et-protection-v)
- [Pomme dorée moins chère](#pomme-dorée-moins-chère)
- [Trade infini](#trade-infini)
- [Dupliquer un livre enchanté](#dupliquer-un-livre-enchanté)
- [Un seul Totem d'immortalité](#un-seul-totem-dimmortalité)
- [Armes légendaires plus accessibles](#armes-légendaires-plus-accessibles)
- [La Poubelle](#la-poubelle)
- [Générer une map art : `/mapart`](#générer-une-map-art--mapart)
- [Le classement : `/classement`](#le-classement--classement)
- [Le Coffre de l'End agrandi](#le-coffre-de-lend-agrandi)

## Se connecter : mot de passe obligatoire

Le serveur tourne en mode hors-ligne pour que le launcher fonctionne sans
compte Microsoft. Conséquence : **n'importe qui pourrait se connecter avec le
pseudo de quelqu'un d'autre**. Un mot de passe personnel referme cette porte.

### À ta première connexion

```
/register <motdepasse> <motdepasse>
```

Le mot de passe est répété pour éviter une faute de frappe.

### À chaque connexion suivante

```
/login <motdepasse>
```

Tant que tu n'es pas identifié, tu ne peux ni bouger, ni parler, ni toucher
quoi que ce soit — et tu es déconnecté au bout d'une minute. C'est normal.

Pour changer de mot de passe : `/changepassword <ancien> <nouveau>`.

> **Choisis un mot de passe que tu n'utilises nulle part ailleurs.** Il est
> stocké haché (BCrypt), donc illisible en clair même pour un administrateur,
> mais la règle vaut pour tous les serveurs de jeu.

Si tu l'oublies, demande à un administrateur : il peut effacer ton
enregistrement pour que tu refasses un `/register`.

## Se protéger du PvP

Tu peux te retirer du PvP :

```
/pvp          → active ou désactive la protection
/pvp statut   → affiche ton état et le temps d'attente restant
```

**La protection marche dans les deux sens.** Protégé, tu ne peux pas être
frappé par les autres joueurs, mais **tu ne peux pas les frapper non plus**.
Impossible donc de s'en servir pour attaquer sans risque.

Ça couvre aussi les coups indirects : flèches, potions, tout ce qui remonte à
un joueur.

### Trois garde-fous

Le changement est refusé si :

1. **Tu es en combat** — 15 secondes après le dernier coup donné ou reçu.
2. **Un joueur est à moins de 20 blocs** — le message te dit qui.
3. **Moins de 15 minutes** se sont écoulées depuis ton dernier changement.

Ces règles empêchent d'activer la protection en plein combat, ou de la couper
juste le temps de porter un coup. Le compte à rebours de 15 minutes utilise
l'heure réelle : un redémarrage du serveur ne le remet pas à zéro.

Le réglage survit à la mort et à la déconnexion.

## Poser une prime

Tu peux mettre la tête de quelqu'un à prix — **avec des objets, jamais de
l'argent**. Le serveur n'a pas d'économie, et une prime qui ne coûte rien de
réel ne vaudrait rien.

```
/bounty set <joueur>       → ouvre un coffre : dépose les objets qui forment la prime
/bounty                    → liste toutes les primes en cours
/bounty voir <joueur>      → détaille ce qu'il y a sur une tête
/bounty annuler <joueur>   → récupère ta contribution sur ce joueur
```

### Comment ça marche

`/bounty set` ouvre un coffre de 27 cases. Tu y déposes ce que tu veux offrir,
exactement comme dans un coffre normal, et tu le refermes. **Les objets quittent
ton inventaire à ce moment-là** — c'est le prix de la prime. Tout le serveur est
prévenu, la cible comprise.

Quand cette personne est ensuite **tuée par un autre joueur**, le tueur reçoit
d'un coup tout ce qui avait été mis sur sa tête, par tout le monde. Ce qui ne
rentre pas dans son inventaire tombe à ses pieds.

### Les règles

- Une mort par lave, chute ou mob ne donne la prime à personne : elle reste
  jusqu'à ce que quelqu'un la mérite.
- Plusieurs joueurs peuvent poser une prime sur la même tête. Chacun ne peut
  annuler que la sienne.
- Impossible de se mettre une prime à soi-même.
- La cible doit s'être connectée au serveur au moins une fois — elle peut être
  hors ligne quand tu poses la prime.
- Les primes sont enregistrées avec le monde : un redémarrage ne les efface pas.

### Avec la protection PvP

Un joueur protégé par `/pvp` ne peut pas être tué par un joueur : la prime sur
sa tête reste en attente tant qu'il ne la désactive pas. Comme le changement
demande qu'aucun joueur ne soit à moins de 20 blocs, puis 15 minutes de délai
avant de pouvoir revenir en arrière, désactiver sa protection avec une prime
sur la tête est un vrai pari.

**Se planquer derrière la protection a un prix.** Tant qu'un joueur reste
protégé avec une prime active sur sa tête :

- il ne **gagne plus d'XP**, peu importe la source (minage, fonte, mobs,
  troc...) ;
- il ne peut **garder aucun effet positif** (Force, Vitesse, Régénération...)
  — ils sont retirés automatiquement, encore et encore ;
- il subit en permanence **Lenteur I**.

La pénalité s'arrête à l'instant où la protection ou la prime disparaît — pas
de minuteur à attendre, pas de compte à rebours : juste le temps que l'un des
deux cesse d'être vrai.

## Le Cœur de Vie

Un objet créé sur mesure pour le serveur. Le consommer donne **+1 cœur de
vie maximum, définitivement**.

### La recette

Très coûteuse, volontairement — c'est un objet de fin de progression.

|  |  |  |
|---|---|---|
| Heavy Core | Bloc de diamant | Totem d'immortalité |
| Bloc de diamant | **Pomme dorée enchantée** | Bloc de diamant |
| Pomme dorée | Bloc de diamant | Carotte dorée |

Soit, au total : 4 blocs de diamant, 1 Heavy Core, 1 Totem d'immortalité,
1 pomme dorée enchantée, 1 pomme dorée et 1 carotte dorée.

### Comment ça marche

- Il se **mange** comme un aliment (maintiens le clic droit). L'animation et
  le son sont ceux d'un repas normal.
- Une fois consommé, tu gagnes **1 cœur maximum de façon permanente** — il
  reste après une déconnexion, après une mort, après un redémarrage du
  serveur.
- L'effet est accompagné de l'animation du **Totem d'immortalité** (l'éclair
  doré plein écran et les particules), mais avec le cœur affiché à la place
  du totem.

### La limite : 5 cœurs bonus

Tu ne peux pas dépasser **5 cœurs bonus**, soit 15 cœurs au total au lieu de
10. Au-delà, le jeu refuse de consommer l'objet et te le dit à l'écran — tu
ne gaspilles donc jamais un Cœur par erreur.

### Comment on en perd

**Uniquement en te faisant tuer par un autre joueur.** Tu perds alors
**1 seul** cœur bonus, pas toute ta réserve.

Toutes les autres morts — chute, lave, creeper, noyade, faim, un mob
quelconque — **ne coûtent rien**. Tu peux mourir bêtement sans perdre ta
progression : seul le PvP a un prix.

## Le Lait Infini

Un seau qui ne se vide jamais.

### La recette

Aussi coûteuse que le Cœur de Vie, dans un autre registre : un bloc de
netherite entouré de seaux de lait.

|  |  |  |
|---|---|---|
| Seau de lait | Seau de lait | Seau de lait |
| Seau de lait | **Bloc de netherite** | Seau de lait |
| Seau de lait | Seau de lait | Seau de lait |

Soit, au total : 8 seaux de lait et 1 bloc de netherite (9 lingots de
netherite).

### Comment ça marche

- Il se **boit** exactement comme un seau de lait (même animation, même
  son, maintiens le clic droit).
- Contrairement à un vrai seau de lait, **il ne se vide jamais** — il reste
  dans ton inventaire après chaque utilisation, réutilisable à l'infini.
- Il ne retire que les **effets néfastes** (poison, Faiblesse, Lenteur,
  Cécité...). Contrairement au lait normal, il **ne touche pas** aux effets
  positifs — un buff pris avant (Force, Vitesse, Régénération...) survit.

## Solidité V et Protection V

Sur ce serveur, **Solidité** et **Protection** montent un niveau plus haut
que dans le jeu de base : **niveau V** au lieu de IV pour Protection et III
pour Solidité.

### Comment les obtenir

- **Table d'enchantement** : comme n'importe quel autre enchantement, en
  tentant ta chance avec assez de niveaux et de lapis-lazuli.
- **Enclume** : combine deux livres (ou objets) au niveau IV identique pour
  monter à V, exactement comme la combinaison classique III+III → IV.
- **Villageois bibliothécaire** : ses offres de livre enchanté peuvent
  directement proposer du niveau V.

Aucune autre règle ne change : coût en XP, poids dans la table
d'enchantement, objets compatibles (armure pour Protection, tout objet qui
s'use pour Solidité) restent ceux du jeu de base, juste étendus jusqu'à V.

## Pomme dorée moins chère

La recette de la **pomme dorée** (celle qui donne Résistance + Absorption,
pas la pomme dorée enchantée) est allégée : **4 lingots d'or** et une pomme,
au lieu des 8 lingots habituels. N'importe quel agencement dans la grille
de craft fonctionne.

## Trade infini

Un joueur peut se voir accorder le **trade infini** avec les villageois par
un admin : les offres ne se bloquent plus après utilisation, et les prix
qui montent avec la demande reviennent à zéro à chaque échange.

C'est un privilège accordé au cas par cas (`/inftrade enable <joueur>`),
pas une règle générale du serveur.

## Dupliquer un livre enchanté

Combine un livre enchanté avec un livre vierge sur une **enclume** pour en
obtenir une copie. Le coût en XP dépend des enchantements copiés. Maintenir
Maj en validant duplique en masse (coûte de l'XP à chaque copie).

## Un seul Totem d'immortalité

**Tu ne peux garder qu'un seul Totem d'immortalité à la fois.**

Cette limite est vérifiée automatiquement par le serveur, environ une fois
par seconde. Elle couvre :

- ton inventaire et ta barre d'action,
- ta main secondaire,
- **l'intérieur des shulker box** que tu transportes,
- **l'intérieur des bundles**.

Impossible, donc, de contourner la règle en planquant tes totems dans une
shulker box au fond du sac.

Si tu en as plusieurs, les exemplaires en trop sont **supprimés** et un
message te prévient à l'écran. Le premier trouvé est conservé.

> **À savoir** : la vérification est correctrice, pas préventive. Peu importe
> comment un deuxième totem arrive dans ton inventaire (craft, butin, coffre,
> échange, shulker ramassée qui en contenait déjà un), il sera retiré à la
> vérification suivante. Ne stocke pas tes totems sur toi : laisse-les dans
> un coffre.

## Armes légendaires plus accessibles

Les armes Uniques de **Simply Swords** sont bien plus faciles à obtenir chez
nous que dans le mod d'origine : chaque boss a de bonnes chances d'en laisser
tomber une (100 % pour le Dragon de l'Ender, 50 % pour les trois autres), et
les grandes structures ont des taux fortement relevés.

**Et elles arrivent prêtes à l'emploi.** Normalement, une arme Unique tombe
"endormie" : sa capacité au clic droit est scellée tant qu'on ne l'a pas
éveillée à la Forge Runique, ce qui demande des Tablettes Runiques. C'est
désactivé ici — toute arme ramassée fonctionne **immédiatement à son niveau
maximum**, statistiques complètes et capacité spéciale incluse.

Le pool de butin contient **40 armes** sur les 58 du mod. Les 18 autres ne
s'obtiennent que par les Reliques Contenues — c'est voulu par le mod, pas un
réglage de notre part.

**Chaque arme Unique n'existe qu'en un seul exemplaire sur tout le
serveur, peu importe comment elle a été obtenue** — boss, coffre de
structure, Relique Contenue, tout est couvert. Si un boss est sur le point
de donner une épée déjà possédée par quelqu'un d'autre, elle est
automatiquement remplacée par une autre Unique pas encore distribuée avant
même de toucher le sol — un kill réussi donne donc toujours quelque chose,
jamais un doublon. Pour les autres sources (coffres, Reliques...), une
vérification tourne en permanence en arrière-plan et corrige le tir en
quelques secondes si un doublon apparaît malgré tout dans un inventaire.

Les détails complets (tableaux de chances par boss et par structure) sont sur
la page **Simply Swords**, section *Comment les obtenir*.

## La Poubelle

Un bloc pour se débarrasser définitivement d'objets, sans avoir à les jeter
au sol ou à les brûler dans un feu.

### La recette

|  |  |  |
|---|---|---|
| Lingot de fer |  | Lingot de fer |
| Lingot de fer |  | Lingot de fer |
| Lingot de fer | Lingot de fer | Lingot de fer |

Soit 5 lingots de fer au total.

### Comment ça marche

- **Clic droit** sur le bloc pour l'ouvrir : ça affiche une interface comme
  un coffre, avec une seule rangée de cases.
- Dépose ce que tu veux supprimer. **Tant que tu n'as pas confirmé, rien
  n'est perdu** — les objets restent dans la Poubelle exactement comme dans
  un coffre normal : tu peux les reprendre, fermer l'interface, revenir plus
  tard, ou même redémarrer le serveur, ça ne change rien.
- Un bouton rouge **"Supprimer"** est affiché sous les cases. C'est le seul
  geste qui détruit le contenu — et il est irréversible.

> **Attention** : une fois le bouton pressé, les objets sont supprimés
> définitivement, sans confirmation supplémentaire. Vérifie ce que tu as mis
> dedans avant de cliquer.

Casser le bloc avec des objets encore dedans (avant confirmation) les fait
tomber au sol comme un coffre cassé — ils ne sont perdus qu'après avoir
cliqué sur "Supprimer".

## Générer une map art : `/mapart`

Une fenêtre pour transformer une image (lien direct vers un `.png`/`.jpg`...)
en tableau de maps posables sur un mur, sans avoir à deviner la bonne
résolution.

```
/mapart
```

Ouvre un formulaire : colle le lien de l'image, choisis le style de tramage
(**Floyd-Steinberg** par défaut — le plus fidèle aux couleurs ; **Erreur
minimisée** et **Aucun** sont les deux autres options du mod), règle la
largeur et la hauteur **en blocs** (1 à 32), puis clique sur **Générer**.

- **1 bloc de large × 1 bloc de haut** = une seule carte, tient dans un seul
  cadre.
- Au-delà, le jeu te donne un item "aperçu" à poser : il déploie tout seul la
  grille de cartes dans les cadres, dans le bon ordre.
- Plus c'est grand, plus il y a de détails visibles — mais plus il faut de
  cadres et de cartes vierges pour le poser.

> Cette fenêtre ne fait qu'écrire la commande `/map4image create` à ta place
> avec les bons chiffres — c'est le mod **Map4Image**, installé côté serveur,
> qui fait le vrai travail. Si jamais ce mod est retiré du serveur, `/mapart`
> arrête de fonctionner exactement comme taper la commande à la main.

## Le classement : `/classement`

```
/classement
```

Ouvre une fenêtre avec cinq onglets — **Primes** (piles d'objets récoltées
en tuant des cibles à prix), **Kills**, **Morts**, **Temps de jeu** et
**Cœurs de Vie** — chacun affichant le top 10, trié automatiquement. Si tu
n'es pas dans le top 10 d'un onglet, ta propre position s'affiche quand même
en dessous.

Les stats comptent à partir du moment où cette fonctionnalité a été mise en
ligne — pas de reconstitution de l'historique d'avant. Rien à faire de
particulier : primes, kills, morts, temps de jeu et Cœurs de Vie consommés
s'enregistrent automatiquement, en jouant normalement.

## Le Coffre de l'End agrandi

Le Coffre de l'End (celui qui suit ton stockage privé partout, pas besoin
de le rapporter) tient maintenant **3 fois plus** — 81 cases au lieu de 27.
Rien à changer dans ta façon de jouer : clique droit dessus comme
d'habitude, la fenêtre s'ouvre juste plus grande.

Les 27 premières cases restent ton vrai Coffre de l'End vanilla, exactement
comme avant — les 54 en plus sont un espace de rangement séparé accolé au
même endroit. Aucune perte possible : le contenu d'origine n'est ni
déplacé, ni recréé, seulement affiché à côté du nouvel espace.
