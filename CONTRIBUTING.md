# Contribuer au Cyclo-Terre

Merci de votre intérêt. Le Cyclo-Terre se développe avec celles et ceux qui le construisent et
l'utilisent : un retour de terrain vaut autant qu'une modification des plans.

Pas besoin de connaître GitHub pour participer : vous pouvez aussi écrire à
contact@cyclo-terre.ch.

## Les façons de contribuer

Du plus simple au plus engagé ; les deux premières lignes ne demandent aucun compte.

| Vous voulez… | Comment |
| --- | --- |
| Poser une question, partager une construction ou une idée, sans compte | Écrire à contact@cyclo-terre.ch |
| Poser une question ouverte à tous (« ça marche en sol argileux ? ») | [Discussions](https://github.com/Cyclo-Terre-Org/Cyclo-Terre/discussions) |
| Signaler une erreur dans les plans, une pièce introuvable, une casse | [Ouvrir un signalement](https://github.com/Cyclo-Terre-Org/Cyclo-Terre/issues/new?template=probleme.yml) |
| Proposer une idée d'amélioration | [Ouvrir une proposition](https://github.com/Cyclo-Terre-Org/Cyclo-Terre/issues/new?template=amelioration.yml) |
| Montrer votre Cyclo-Terre, vos adaptations, vos mesures au champ | [Partager une construction](https://github.com/Cyclo-Terre-Org/Cyclo-Terre/issues/new?template=construction.yml) |
| Corriger une faute ou une précision dans un guide | Bouton « Proposer une correction » en bas de chaque guide sur [cyclo-terre.ch](https://cyclo-terre.ch/outils/#construire), ou le crayon ✎ sur GitHub : l'éditeur en ligne prépare la proposition pour vous |
| Modifier vous-même les plans ou la CAO | Proposer une modification (ci-dessous) |

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

### Documentation (`utilisation/`, `assemblage/`, README)
- Ces guides sont affichés tels quels sur cyclo-terre.ch : un fichier = une page. Le titre est la
  première ligne `# …`. Le `README.md` d'un dossier en est le sommaire.
- Liens entre guides et images : chemins relatifs (`entretien.md`, `images/03-transmission.jpg`).
- Markdown, en français, phrases courtes, une action par étape.
- Une photo ou un schéma par étape, dans `assemblage/images/`, en JPEG ou PNG, 2000 px de large au
  plus. Décrivez chaque image (texte alternatif).

### Versions
- Numérotation `vMAJEUR.MINEUR` : majeur quand une pièce n'est plus compatible avec la version
  précédente, mineur pour le reste.
- Toute modification est notée dans [CHANGELOG.md](CHANGELOG.md).
- Publier une version : créer l'étiquette (`git tag v1.0 && git push origin v1.0`, ou
  « Releases → Draft a new release » sur GitHub). Une automatisation génère alors les PDF des guides,
  les archives des plans et de la CAO et la nomenclature, les joint à la version et met à jour
  cyclo-terre.ch.

## Licence de vos contributions

En proposant une modification, vous acceptez qu'elle soit publiée sous les mêmes licences que le
reste du dépôt : CERN-OHL-S v2 pour le matériel, CC BY-SA 4.0 pour la documentation (voir
[LICENSE.md](LICENSE.md)). Vous restez autrice ou auteur de votre contribution ; votre nom
apparaît dans l'historique du dépôt.

## Comportement

Nous attendons de chacun·e des échanges respectueux et constructifs : voir le
[code de conduite](CODE_DE_CONDUITE.md).
