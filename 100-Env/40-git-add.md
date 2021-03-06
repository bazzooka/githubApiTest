# GIT - ADD A FILE TO GIT

## INTRO

Maintenant que vous savez cloner un repository nous allons nous
attarder à ajouter des fichiers sur le `local repository`.

## OBJECTIFS

A la fin de ce cours vous saurez:

* ===tagger|tagger=== des fichiers comme `stagged`
* ajouter des fichiers au `repository local`

## COURS

Vous l'aurez compris l'étape d'ajout de fichiers au `repository local` se fait en
deux étapes.

### Marquer les nouveaux fichiers comme stagged

GIT n'ajoute pas tous les fichiers que vous créer directement à votre `repository local`.
Pour que GIT voit vos fichiers, il faut que vous les déclariez.
Pour cela rien de plus simple, il suffit d'utiliser la commande: `git add <chemin de votre fichier>`
Par exemple, si je veux ajouter à GIT mon fichier `server.js`, il suffit de faire:
`git add server.js`.

Si je veux ajouter un répertoire entier, il suffit de faire: `git add myDirectory/`

Pour résumer cette étape: `git add` permet de d'ajouter les nouveaux fichiers au repository lors dun prochain `commit`.

### Marquer les modifications comme à ajouter

Lorsque vous modifiez des fichiers qui étaient déjà sur le `repository`, il faut aussi indiquer que vous souhaitez les ajouter.
Pour cela rien de plus simple, une fois encore il suffit d'utiliser la commande:
`git add <chemin de votre fichier>`.

## CONCLUSION

Vous savez désormais comment déclarer des fichiers pour que GIT en tienne compte.
Attention, ce qui est ===tracké|tracke=== n'est pas encore ajouté à votre `local repository`, ce sera l'objet de la prochaine leçon.

## DOCUMENTATION
