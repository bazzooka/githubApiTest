# GIT - GIT BRANCH

## INTRO
Vous maitrisez maintenant tout le flow de travail avec GIT.
Pour rappel:
 - `clone` de `remote repository`
 - `add` de ressource pour les stagger les nouveauc fichiers et les modifications
 - `commit` pour créer votre commit d'update et l'envoyer sur votre `local repository`
 - `pull` pour récupérer les modifications du `remote repository`
 - `push` pour envoyer vos `commit` sur le `remote repository`
 Une des fonctions très appréciée de GIT est l'utilisation des branches.
 GIT fonctionne sous forme d'arbre. Il y a la tronc qui est représenté grâce à la `master branch` et les branches.
 Les branches adjacentes sont des divergences de la `master branch`, et les branches des branches, des divergences 
 des divergences.
 ![Branches](https://wac-cdn.atlassian.com/dam/jcr:746be214-eb99-462c-9319-04a4d2eeebfa/01.svg?cdnVersion=jm)

## OBJECTIFS
Nous verrons durant ce cours: 
 - **POURQUOI** vous avez besoin des branches
 - **QU'EST-CE QU'** une branch
 - **QUAND** utiliser une branche

## COURS
### Mise en situation
Votre boss vous demande de créer une nouvelle feature. Avec votre nouveau savoir vous allez sûrement cloner le 
`remote repository` et faire vos modifications.
La fin de journée arrive et vous devez pousser tout votre code, pour ne pas risquer de tout garder en local sur votre
`local repository`.

**Problème 1:** Vous ne pouvez pas pousser sur la `master branch` qui sera déployé en production votre code pas
complètement terminé. 

**Problème 2:** Le processus de développement impose de la `code review`. C'est une très bone technique qui impose que 
quelque soit votre niveau, votre code soit `reviewer` c'est à dire "étudier" par un membre de votre équipe.
Cela permet: 
 - le partage de connaissance
 - la correction d'erreur
Or si votre code est plein de bugs, il ne faut pas qu'il aille directement en production.

**Solution:** La solution consisterait donc à avoir une copie du workspace de production qui ne soit pas la production
et dans lequel je puisse travailler: **LES BRANCHES**

### Les branches
Les branches sont donc des divergences à un moment donné d'autres branches. Leur principale fonction étant de permettre
de travailler dans un environnement avec le même code que la branche dont elles dérivent sans recopier tous les fichiers, 
seuls les fichiers modifiés y sont stockés.

Elles bénéficient donc d'action telles que: 
 - `merge`: qui va permettre de fusionner 2 branches
 - `rebase`: qui va permettre de fusionner 2 branches en fusionnant les commits.
 
Une bonne pratique est de créer des branches pour tous ces développements. **TOUT doit passer par des branches.**
Chaque branche une fois `merger`(fusionner) peut être `reverter` (dé-fusionner). Une branche est composée de `commits`.

### GIT FLOW
Vous serez sûrement amené à travailler avec la méthode de `GIT FLOW` qui consiste à avoir 2 branches: 
 - `master`: qui peut être déployé à tout moment sur l'environnement de production
 - `develop`: qui peut être déployé à tout moment sur l'environnement de test
 
 Lorsque vous développer une feature, il vous faudra créer votre branche depuis la branche **develop**. Pour ce faire,
 il vous faudra récupérer la branche develop: `git checkout develop`. Cette commande vous permettra de switcher de
 branche. Vous aurez accès au code qui va être pousser sur la production. Attention, le `checkout` ne met pas à jour
 votre branche, il vous faudra faire `git pull` pour la mettre à jour.
 
 Une fois sur la branch `develop`, il vous faudra créer votre branche de fix, feature... Vous allez donc créer 
 une divergence depuis le dernier `commit` pullé sur `develop`. D'où l'intérêt de bien mettre à jour votre `branch
 develop`. Pour créer votre branche divergente, utilisez la commande: `git checkout -b nom-de-votre-branch`.
 
 Voud devriez noter que votre invite de commande a changé et vous donne en plus la branche sur laquelle vous travailler.
 Une fois sur votre branche, libre à vous de commiter des modifications, des fix... les commandes habituelles
 s'appliquent sans que rien ne change. Vous poussez donc votre branche sur le `remote repository`.
 Pour connaitre la liste des branches:
  - locales: `git branch`
  - distantes: `git branch --remote`
Quand vous aurez finis de travailler sur votre branche, la branch `develop` aura elle aussi sûrement avancé. Il vous
faudra donc vous récupérer les nouveautés. Pour cela, il voud faudra utiliser la commande: `git rebase develop` pour
vous `rebaser` sur la branche develop.
![Git rebase](https://wac-cdn.atlassian.com/dam/jcr:e4a40899-636b-4988-9774-eaa8a440575b/02.svg?cdnVersion=jm)

Git gère très bien les fusions de branches et normalement tout devrait très bien se passer sur la plupart de vos rebase.
Cependant, il peut arriver qu'il n'arrive pas à fusionner les deux branches et dans ce cas il vous faudra gérer un 
conflit. On dit alors que vous êtes en `merge conflict`.

### FIXER LES CONFLITS
Revenons aux faits qui vous ont amené ici. Vous avez travailler sur votre branche, et vous avez voulu la `rebaser` sur 
une autre branche. Malheureusement, il s'avère qu'entre temps une personne vous a précéder et a modifier un fichier sur 
lequel vous voulez vous aussi apporter des modifications.

Si les modifications sont trop fines, GIT peut ne pas arriver à fusionner les deux branches. Il vous laisse alors le 
choix de ce que vous souhaiter prendre:
 - prendre les modifications de l'autre développeur actuellement sur le `remote repository`
 - prendre vos modifications sur votre `repository local`
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

Si vous ouvrez le fichier indiqué en l'occurence `Readme.md` vous découvrirez qu'il a été modifié avec des indications
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

C'est à vous de décider si vous préférez garder vos modifications, celle provenant du `remote repository` ou encore de 
faire un mix des deux. Ajoutez vos modifications avec `git add` et commitez les: `git commit -m "resolve merge conflict`. 
 
## CONCLUSION
Vous savez maintenant:
 - créer une branche pour travailler
 - pusher votre branche
 - régler les conflits

## DOCUMENTATION

