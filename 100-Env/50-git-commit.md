# GIT - COMMIT A FILE TO GIT

## INTRO

Les fichiers sont ===trackés|tracke===, maintenant nous allons les envoyer sur notre
`repository local`.

## OBJECTIFS

A la fin de ce cours vous saurez:

* créer un `commit`
* envoyer ce `commit` sur votre `repository local`

## COURS

Alors qu'est-ce qu'un `commit` ? Un `commit` est un état de votre `repository`.
Il est identfié par un numéro `hash` et représente tous les fichiers que vous avez modifié
durant la modification.
Exemple de commit:

```bash
commit babeb34f13428b87604242f9e1ab1c701403d62e <= numéro de commit
Author: Joe <jsouied@stackerine.com>            <= email du commiter
Date:   Sat Mar 10 16:27:20 2018 +0100          <= date du commit

    review 30-git-status                        <= message de commit
```

Attention, pour pousser un `commit` et donc une modification il faudra que vous ayez déclarer ces modifications. Je vous rappelle que vous pouvez les déclarer avec la commande `git add`.

Pour pousser (commiter) votre `commit` sur votre `local repository` il vous faudra utiliser la commande:
`git commit`.

Un `commit` est toujours accompagné d'un message de `commit` qui permet aux autres
développeurs de connaitre le contenu du `commit` sans avoir à inspecter son contenu.

Pour `commiter` des fichiers avec un message il faut utiliser la commande:
`git commit -m "Mon message de commit"`

## CONCLUSION

La commande `git commit` vous permet donc de faire un packet identifié par un hash et de le `commiter`, de l'envoyer sur votre **`repository local`**.

## DOCUMENTATION
