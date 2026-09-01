# Simply Swords

Ajoute des lances, glaives, chakrams, katanas, marteaux/haches à deux
mains, rapières et bien d'autres armes — 14 variantes d'armes uniques, avec
des styles de jeu et animations différentes selon l'arme.

- **Modrinth** : [modrinth.com/mod/simply-swords](https://modrinth.com/mod/simply-swords)
- **Catégories** : Équipement, Magie
- **Téléchargements** : ~9,3 M
- **Licence** : Custom (voir la page Modrinth)

## Compatibilité

- Minecraft **1.20.1**, loader **Forge** ✓ (compatible avec la config
  actuelle du serveur)
- **Doit être installé côté client ET côté serveur** — ce n'est pas un mod
  cosmétique client-only.

## Fonctionnalités

- Butin unique : ouvrir des coffres a une chance de donner des armes
  spéciales avec des capacités propres (non craftables).
- Support additionnel pour Mythic Metals et Gobber (plus de 200 armes au
  total si ces mods sont aussi installés).

## ⚠️ Dépendances obligatoires

Simply Swords **ne fonctionne pas seul** — la dernière version compatible
1.20.1 Forge (`1.70.2-1.20.1`) nécessite ces mods en plus, sinon le
chargement du jeu échoue :

| Mod | Modrinth ID | Rôle |
|---|---|---|
| **Architectury API** | `architectury-api` | requis |
| **Simply Tooltips** | `simply-tooltips` | requis |
| **Fzzy Config** | `fzzy-config` | requis |

**Optionnel mais recommandé** : **Better Combat** (`better-combat`) — anime
les animations d'attaque uniques par arme ; sans lui, les armes
fonctionnent mais avec l'animation d'attaque vanilla.

## Ajouter ce mod au serveur

Pour l'ajouter réellement (pas juste le documenter ici), suis le § 3 de
`SETUP.md` dans le repo du launcher — il faut ajouter **une entrée par mod
ci-dessus** (Simply Swords + ses 3 dépendances requises) dans
`manifest.json`, pas seulement Simply Swords seul.
