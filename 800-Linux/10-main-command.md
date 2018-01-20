# Commandes principales

## INTRO

Linux est un système d'exploitation open source (tout le monde peu voir les sources).
C'est un système très prisé par les développeurs parce que :
- il permet de maitriser totalement ce que l'on fait
- est open source (modifiable par la communauté)
- beaucoup d'outils ne fonctionnent qu'avec cet environnement
- bug beaucoup moins
- plus hype quand on est développeur :)

## OBJECTIFS

Vous devez apprendre à utiliser votre système en ligne de commande
pour les actions les plus simples.
- parcourir les répertoires
- lister les fichiers et les répertoires
- créer un répertoire
- créer un fichier
- supprimer un répertoire
- supprimer un fichier
- interroger l'aide

## COURS
Pour que vous aider à représenter mentalement le contenu de votre ordinateur il
faut imaginer un arbre avec une racine et des branches qui en découlent.
En informatique, on parle réellement du répertoire racine. Sur Windows il s'agit souvent
du `C:` et sur Linux / OSX, il s'agit de `/`
Quand vous ouvrez votre terminal vous n'êtes pas à la racine.

### Pour savoir où vous êtes
Executer la commande `pwd`
Elle vous retournera votre position dans l'arborescence sour la forme de: 
`/Users/joe/projets` par exemple.

### Lister les fichiers et les répertoires
Pour lister les fichiers et les répertoires du répertoire courant, executez la commande:
`ls`. Elle vous retournera la liste des fichiers et des répertoires dans votre `pwd`.
La commande `ls` peut accepter des paramètres.
Par exemple `ls -l`: Listera les fichiers / répertoires sous forme de liste avec des
informations complémentaires comme la date de modification, le propriétaire...
Autre example: `ls -a` permet de lister les fichiers cachés ceux qui commencent par un `.`
Vous pouvez également cumuler les options en faisant par exemple: `ls -al` 
qui vous rendra les fichiers / répertoires sous forme de liste avec les fichiers cachés.
Vous aurez remarquer quand je fais `ls -al` que j'ai un répertoire `.`
et un répertoire `..`. Ils désignent respectivement le répertoire courant et le
répertoire parent.
Vous avez donc le droit de faire: `ls -al .` et `ls -al ..` qui listeront respectivement
le contenu du répertoire courant et celui du répertoire parent.
A part la racine, tous les répertoires possèdent les répertoires `.` et `..`.  

### Naviguer entre les répertoires
Pour changer de répertoire, il vous suffira d'utiliser la commande `cd`
qui sert d'abbréviation à "Change Directory".
Pour me dirigier vers le répertoire parent, il me suffit donc de faire `cd ..`
Si je fais `cd .`, rien ne se passe même si c'est une commande valide !
Pour descendre dans un répertoire qui serait présent et nommé `monRepertoire`,
il me suffit de faire: `cd monRepertoire`

### Créer un répertoire
Pour créer un répertoire, il faut utiliser la commande: `mkdir' abbréviation de 
"MaKe DIRectory".
`mkdir monRepertoire` créera dans mon `pwd` le répertoire "monRepertoire"

### Créer un fichier
Pour créer un fichier dans ce répertoire, il existe la commande `touch`
`touch monFichier` créera le fichier "monFichier" dans mon `pwd`.

### Supprimer un fichier
Pour supprimer un fichier, il faut utiliser la commande: `rm` abbréviation de
"ReMove".

### Supprimer un répertoire
Pour supprimer un répertoire, il faut utiliser la commande `rm -r`.
Le paramètre `-r` permet d'indiquer que la suppression est récurssive, c'est à dire
qu'il faut entrer dans chaque sous-repertoire pour y supprimer les fichiers.

## Conclusion
Vous avez vu les principales commandes permettant de naviguer et de gérer vos fichiers.
Je vous recommande fortement de ne plus utiliser une interface graphique
pour effectuer ces tâches. Cela vous permettra de vous familiariser beaucoup plus
vite avec votre environnement Linux.
Ce cours vous permet d'avoir les principales commandes de Linux. Si vous
souhaitez en savoir plus sur chaque commande, il existe sur la plupart des commandes
le paramètre `-h` ou `--help` qui vous permettront d'avoir une explication sur les
options de la commande.
Par exemple, `ls --help`

Pour sortir de la documentation il suffit d'appuyer sur la touche `q`
pour **Q**uitter.<span title="This is a tooltip example">tooltip.</span>

<span title="This is a tooltip example">tooltip.</span>
===STRONG TEXT|STRONG POPUP===

## DOCUMENTATION

- [Linux Help](https://www.computerhope.com/unix.htm)
