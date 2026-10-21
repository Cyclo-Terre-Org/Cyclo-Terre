# Contribuer au Cyclo-Terre

Merci de votre intérêt. Le Cyclo-Terre se développe avec celles et ceux qui le construisent et
l'utilisent : un retour de terrain vaut autant qu'une modification des plans.

Pas besoin de connaître GitHub pour participer : vous pouvez aussi écrire à
contact@cyclo-terre.ch.

## Les façons de contribuer

| Vous voulez… | Comment |
| --- | --- |
| Signaler une erreur dans les plans, une pièce introuvable, une casse | [Ouvrir un signalement](https://github.com/Cyclo-Terre-Org/Cyclo-Terre/issues/new?template=probleme.yml) |
| Proposer une idée d'amélioration | [Ouvrir une proposition](https://github.com/Cyclo-Terre-Org/Cyclo-Terre/issues/new?template=amelioration.yml) |
| Montrer votre Cyclo-Terre, vos adaptations, vos mesures au champ | [Partager une construction](https://github.com/Cyclo-Terre-Org/Cyclo-Terre/issues/new?template=construction.yml) |
| Modifier vous-même les fichiers | Proposer une modification (ci-dessous) |

Avant d'ouvrir un sujet, regardez s'il n'existe pas déjà dans les
[issues](https://github.com/Cyclo-Terre-Org/Cyclo-Terre/issues).

## Proposer une modification

1. Ouvrez d'abord une proposition pour en discuter, sauf pour une petite correction (faute, cote,
   référence de pièce).
2. Faites une copie du dépôt (*fork*) et créez une branche : `git switch -c sarcloir-plus-large`.
3. Faites la modification en suivant les conventions ci-dessous.
4. Ouvrez une *pull request* qui explique **quoi**, **pourquoi**, et **comment vous l'avez testé**
   (au champ, à l'atelier, en simulation). Joignez des photos si possible.
5. Nous relisons et testons. Une modification qui touche à la sécurité (cadre, freinage, attelage)
   n'est fusionnée qu'après un essai sur un prototype.

## Conventions

### CAO (`cao/`)
- Logiciel de référence : [À COMPLÉTER]. Publiez toujours le fichier natif **et** un export STEP
  à côté, pour celles et ceux qui utilisent un autre logiciel.
- Unités : millimètres.
- Noms de fichiers en minuscules, sans espace ni accent : `cadre-arriere.step`, `porte-outil.step`.
- Une pièce = un fichier ; l'assemblage complet dans `cao/assemblage/`.

### Plans (`plans/`)
- PDF cotés, format A4 ou A3, avec dans le cartouche : nom de la pièce, matière, quantité, version
  et date.
- Fichiers de découpe en DXF, à l'échelle 1:1.

### Nomenclature (`nomenclature/`)
- Un seul tableau `nomenclature.csv`, une ligne par pièce. Préférez des pièces de vélo standard
  que l'on trouve partout ; indiquez au moins une alternative quand c'est possible.

### Documentation (`assemblage/`, README)
- Markdown, en français, phrases courtes, une action par étape.
- Une photo ou un schéma par étape, dans `assemblage/images/`, en JPEG ou PNG, 2000 px de large au
  plus. Décrivez chaque image (texte alternatif).

### Versions
- Numérotation `vMAJEUR.MINEUR` : majeur quand une pièce n'est plus compatible avec la version
  précédente, mineur pour le reste.
- Toute modification est notée dans [CHANGELOG.md](CHANGELOG.md).

## Licence de vos contributions

En proposant une modification, vous acceptez qu'elle soit publiée sous les mêmes licences que le
reste du dépôt : CERN-OHL-S v2 pour le matériel, CC BY-SA 4.0 pour la documentation (voir
[LICENSE.md](LICENSE.md)). Vous restez autrice ou auteur de votre contribution ; votre nom
apparaît dans l'historique du dépôt.

## Comportement

Nous attendons de chacun·e des échanges respectueux et constructifs : voir le
[code de conduite](CODE_DE_CONDUITE.md).
