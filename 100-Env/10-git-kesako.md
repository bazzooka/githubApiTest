# GIT KESAKO

## INTRO

Que vous travaillez seul ou en équipe vous avez besoin d'un gestionnaire de version.
Il permet de versionner votre code et de retrouver n'importe lequel de ses états.
GIT facilite également le travail en équipe. Nous verrons pourquoi durant ce cours.

## OBJECTIFS

Nous nous attacherons:

* dans une première partie à comprendre quels problèmes résoud GIT
* la représentation mentale que vous devez avoir de GIT

Les commandes seront présentées dans le cours suivant.

## COURS

Imaginez-vous dans votre futur environnement de travail:

* vous travaillez en équipe
* on vous demande de développer une nouvelle fonctionnalité

Bravo, belle promotion, vous êtes un nouvel architecte du web !

## Problème 1 - les conflits

Vous travaillez sur votre nouvelle fonctionnalité et cela vous amène à modifier
la représentation des users dans votre base de données. Pourquoi pas, vous êtes sûr de vous !

Dans le même temps, un de vos collegues travaille sur une autre fonctionnalité qui l'amène à
faire une autre représentation des users dans la ===BDD|BDD===. Vous avez donc travailler sur le même bout de code.

Que se passe t-il ? Qui a raison ? Comment gère t-on le problème ?
Nous verrons comment GIT permet de gérer facilement ce genre de conflit.

## Problème 2 - la gestion des versions

Cette fois on vous a demandé de fixer un bug dans le calcul du panier
lors des commandes. Vous avez trouver le bug, vous êtes fier de vous.
Vous avez modifier plus d'une centaine de fichiers.

Votre ===patch|patch=== est déployé... tout se passe bien... par contre un autre bug plus grave est apparu
dans un des 100 fichiers et tout le site tombe ! Ouch la boulette !

Il faut revenir en arrière, juste avant la mise en place de votre ===patch|patch===.
Vous vous imaginez re-modifier la centaine de fichiers que vous aviez modifier ? Ou chercher le bug à taton ? Encore une fois GIT vous permettra de gérer ces cas délicats.

## Représentation mentale de GIT

Vous pouvez imaginer que sur GIT votre projet est stocké comme sur votre disque dur,
dans un répertoire. Ce répertoire racine de votre projet est appelé `repository`.

Il existe deux type de `repository`:

* le `local repository`: il contient les fichiers qui sont sur la machine d'une personne
* le `remote repository`: il contient les fichiers qui sont sur le server GIT et qui sont partagés
  par toute l'équipe.

### Pourquoi 2 repositories ?

Toutes les commandes de GIT peuvent être utilisées sur votre `local repository`, cependant
il n'y a que vous qui pouvez y accéder. Vous travaillez donc sur votre `local repository`
et quand vous estimez que vous pouvez partager votre code avec votre team alors il vous suffit
de le partager sur le `remote repository`.

La procédure pour cela est donc de d'abord mettre à jour votre environnement local en
récupérant les informations du remote puis de pousser toutes les informations.

![Local & remote repositories](https://backlog.com/git-tutorial/en/img/post/intro/capture_intro1_2_2.png)

On parle de `pull` quand on récupère du code sur le `remote repository` et qu'on met
à jour son `local repository`
On parle de `push` quand on met à jour le `remote repository` avec le contenu de son `local repository`.
Un `commit` représente une modification du code que vous avez effectué.

### Github

Nous avons précédemment créer un compte sur [Github](Github.com).
Github vous permettra de stocker et de partager l'ensemble de votre code. Il vous servira
donc de `remote repository` et de partager avec l'ensemble du monde vos progrès et vos connaissances.

Je vous incite donc à créer pour chaque exercice de chaque lesson un repository pour
partager votre évolution au fur et à mesure des cours.

## CONCLUSION

Vous avez maintenant vu les grandes lignes de l'utilité de GIT.
Etudions maintenant son fonctionnement.

## DOCUMENTATION
