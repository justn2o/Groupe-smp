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
- [Un seul Totem d'immortalité](#un-seul-totem-dimmortalité)
- [Armes légendaires plus accessibles](#armes-légendaires-plus-accessibles)

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
nous que dans le mod d'origine : chaque boss en laisse tomber une garantie,
et les grandes structures ont des taux fortement relevés.

**Et elles arrivent prêtes à l'emploi.** Normalement, une arme Unique tombe
"endormie" : sa capacité au clic droit est scellée tant qu'on ne l'a pas
éveillée à la Forge Runique, ce qui demande des Tablettes Runiques. C'est
désactivé ici — toute arme ramassée fonctionne **immédiatement à son niveau
maximum**, statistiques complètes et capacité spéciale incluse.

Le pool de butin contient **40 armes** sur les 58 du mod. Les 18 autres ne
s'obtiennent que par les Reliques Contenues — c'est voulu par le mod, pas un
réglage de notre part.

Les détails complets (tableaux de chances par boss et par structure) sont sur
la page **Simply Swords**, section *Comment les obtenir*.
