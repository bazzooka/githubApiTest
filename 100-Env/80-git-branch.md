# GIT - GIT BRANCH

## INTRO

Vous maitrisez maintenant tout le flow de travail avec GIT.
Pour rappel:

* `clone` de `remote repository`
* `add` de ressources / fichiers pour stagger les nouveaux fichiers et les modifications
* `commit` pour créer votre commit d'update et l'envoyer sur votre `local repository`
* `pull` pour récupérer les modifications du `remote repository`
* `push` pour envoyer vos `commit` sur le `remote repository`

Une des fonctions très appréciée de GIT est l'utilisation des branches. GIT fonctionne sous forme d'arbre. Il y a le tronc qui est représenté grâce à la `master branch` et les branches.

Les branches adjacentes sont des divergences de la `master branch`, et les branches des branches, des divergences des divergences.

![Branches](http://www.afsyn.com/wp-content/uploads/2018/01/capture_stepup1_5_6.png)

## OBJECTIFS

Nous verrons durant ce cours:

* **POURQUOI** vous avez besoin des branches
* **QU'EST-CE QU'** une branch
* **QUAND** utiliser une branche

## COURS

### Mise en situation

Votre boss vous demande de créer une nouvelle feature. Avec votre nouveau savoir vous allez sûrement cloner le `remote repository` et faire vos modifications.
La fin de journée arrive et vous devez pousser tout votre code, pour ne pas risquer de tout garder en local sur votre machine et donc le `local repository`.

**Problème 1:** Vous ne pouvez pas pousser sur la `master branch` qui sera déployée en production, votre ===feature|feature=== n'est pas complètement terminée.

**Problème 2:** Le processus de développement impose de la `code review`. C'est une très bonne technique qui impose que quelque soit votre niveau, votre code soit `reviewer` c'est à dire "étudier" par un membre de votre équipe.
Cela permet:

* le partage de connaissance
* la correction d'erreur

Autrement dit, si votre code est plein de bugs, il ne faut pas qu'il aille directement en production.

**Solution:** La solution consisterait donc à avoir une copie du ===workspace|workspace=== de production qui ne soit pas la production et dans lequel je puisse travailler: **LES BRANCHES**

### Les branches

Les branches sont donc des divergences à un moment donné d'autres branches. Leur principale fonction étant de permettre de travailler dans un environnement avec le même code que la branche dont elles dérivent sans recopier tous les fichiers.
Seuls les fichiers modifiés y sont stockés.

Elles bénéficient donc d'actions telles que:

* `merge`: qui va permettre de fusionner 2 branches
* `rebase`: qui va permettre de fusionner 2 branches en fusionnant les commits.

Une bonne pratique est de créer des branches pour tous ses développements. **TOUTES vos modifications doivent passer par des branches.** Chaque ===feature|feature=== doit être représentée par une branche.

Chaque branche une fois `merger`(fusionner) peut être `reverter` (dé-fusionner). Une branche est composée de `commits`.

### GIT FLOW

Vous serez sûrement amené à travailler avec la méthode dite de `GIT FLOW` qui consiste à avoir 2 branches principales:

* `master`: qui peut être déployée à tout moment sur l'environnement de production
* `develop`: qui peut être déployée à tout moment sur l'environnement de test

![GIT FLOW](https://image.slidesharecdn.com/gitflowinaction-150414014750-conversion-gate01/95/git-flow-in-action-9-638.jpg?cb=1428994153)

* La branche develop est une copie à un moment donné de la branche master.
* La branche develop est la branche avec laquelle sont synchronisés les développements.
* Les branches de ===feature|feature=== sont des divergences de la branche develop
* Ces branches ===feature|feature=== sont ===mergées|merge=== avec la branche develop
* Régulièrement la branche develop est ===mergée|merge=== avec la branche master qui sera deployée sur l'environnement de production.

Lorsque vous développez une feature, il vous faudra créer votre branche depuis la branche **develop**. Pour ce faire, il vous faudra récupérer la branche develop: `git checkout develop`. Cette commande vous permettra de copier sur votre `local repository` la branche develop si cette branche n'a pas déjà présente sur votre `local repository`. Si la branche est déjà présente, alors cela ne fera que changer la branche active. Attention, dans ce dernier cas, `git checkout develop` changera la branche active mais ne mettra pas à jour votre branche sur le `local repository`. Il vous faudra faire `git pull` pour mettre à jour votre branche en local.

Une fois sur la branch `develop`, il vous faudra créer votre branche de fix, feature... Vous allez donc créer une divergence depuis le dernier `commit` pullé sur `develop`. D'où l'intérêt de bien mettre à jour votre `branch develop`. Pour créer votre branche divergente, utilisez la commande: `git checkout -b nom-de-votre-branch`.

Vous devriez noter que votre invite de commande a changé et vous donne en plus la branche sur laquelle vous travaillez.

Une fois sur votre branche, libre à vous de commiter des modifications, des fix... les commandes habituelles s'appliquent sans que rien ne change.

Pour connaitre la liste des branches:

* locales: `git branch`
* distantes: `git branch --remote`

Quand vous aurez finis de travailler sur votre branche, la branch `develop` aura elle aussi sûrement avancé. Il vous faudra donc vous récupérer les nouveautés. Pour cela, il vous faudra utiliser la commande: `git rebase develop` pour vous `rebaser` sur la branche develop.
![Git rebase](https://cdn-images-1.medium.com/max/1000/1*p0EGOtTUhzpUnF5p2c2UAw.png)

Git gère très bien les fusions de branches et normalement tout devrait très bien se passer sur la plupart de vos rebase.
Cependant, il peut arriver qu'il n'arrive pas à fusionner les deux branches et dans ce cas il vous faudra gérer un conflit. On dit alors que vous êtes en `merge conflict`.

### FIXER LES CONFLITS

Revenons aux faits qui vous ont amené ici. Vous avez travailler sur votre branche, et vous avez voulu la `rebaser` sur une autre branche. Malheureusement, il s'avère qu'entre temps une personne vous a précéder et a modifier un fichier sur lequel vous voulez vous aussi apporter des modifications.

Si les modifications sont trop fines, GIT peut ne pas arriver à fusionner les deux branches. Il vous laisse alors le soin de gérer le conflit.

* prendre les modifications de l'autre développeur actuellement sur le `remote repository`
* prendre vos modifications sur votre `repository local`

La première chose à faire est d'établir la liste des fichiers en conflits: `git status`.

```bash
git status
# On branch branch-b
# You have unmerged paths.
#   (fix conflicts and run "git commit")
#
# Unmerged paths:
#   (use "git add ..." to mark resolution)
#
# both modified:      Readme.md
#
no changes added to commit (use "git add" and/or "git commit -a")
```

GIT vous indique clairement les conflits.

Si vous ouvrez le fichier indiqué en l'occurrence `Readme.md` vous découvrirez qu'il a été modifié avec des indications
de GIT sur les bouts de code qu'il ne sait pas fusionner.

```bash
My file is named
<<<<<<< HEAD
Jonathan
=======
Thomas.
>>>>>>> branch-feature
```

Les modifications provenant du serveur seront encadré par **<<<<<<< HEAD** et **=======** et les modifications provenant
de votre branche encadrées par **=======** et **>>>>>>> BRANCH-NAME**.

C'est à vous de décider si vous préférez garder vos modifications, celle provenant du `remote repository` ou encore de faire un mix des deux. Ajoutez vos modifications avec `git add` et commitez les: `git commit -m "resolve merge conflict`.

## CONCLUSION

Vous savez maintenant:

* créer une branche pour travailler
* pusher votre branche
* régler les conflits

## DOCUMENTATION

* [Git rebase and the golden rule explained](https://medium.freecodecamp.org/git-rebase-and-the-golden-rule-explained-70715eccc372)
