# GIT - POUSSER SUR LE SERVEUR

## INTRO

Ca y est nous y sommes, nous allons maintenant voir comment pousser
les commits qui sont sur votre `repository local` sur le `remote repository`
autrement dit: **PARTAGER VOTRE CODE**.

## OBJECTIFS

A la fin de ce cours, vous saurez pousser vos modifications sur le
`remote repository`

## COURS

Rappel des étapes précédentes:

* `git add`: stage les nouveaux fichiers et les modifications
* `git commit`: créer un `commit` et envoie ce packet sur le `local repository`

Nous sommes maintenant en désynchronisation. Le `remote repository` est en retard de -n commits sur votre `local repository` et votre `local repository` est donc en avance de -n commits sur le `remote repository`. Il faut donc lui pousser les nouveaux `commit`.

La commande est: `git push`

Cette commande vous permet donc de pousser tous les `commits` présents sur votre `local repository` sur le `remote repository`. Tant que vous n'avez pas effectuer cette action, vos modifications ne sont pas accessibles aux autres développeurs.

## CONCLUSION

La commande `git push` est la dernière commande dans le flow des actions à mener pour partager vote code.

## DOCUMENTATION
