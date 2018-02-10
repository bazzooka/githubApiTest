# React introduction

## INTRO

React est un framework développé par Facebook qui permet de constuire des applications en Javascript. Quelques grands
projets développés avec React:

* 6Play
* Airbnb
* Amazon Video
* Americna Express
* BBC
* BNPParibas
* Dailymotion
* [La suite ici...](https://github.com/facebook/react/wiki/sites-using-react)

Ce framework est constamment mis à jour par les ingénieurs de Facebook pour nous permettre d'être à la pointe de l'état
de l'art dans le développement d'application web.

C'est sur ce framework que votre expertise portera et c'est celle que nous avons choisi de vous enseigner. Le marché se
porte bien et c'est une expertise très recherchée actuellement.

Vous allez durant ce cours faire vos premières expériences avec React et apporter vos premières modifications.

## OBJECTIFS

A la fin de ce cours vous serez capable de créer votre première application avec React.

## COURS

Le navigateur Web (client) ne peut comprendre que certaines instructions. Ces instructions peuvent être faites dans 3
langages:

* le HTML qui permet de créer des éléments du DOM (vous l'avez entrevu)
* Le CSS qui permet d'ajouter du style à nos pages (nous le verrons bientôt)
* Le Javascript qui permet de gérer la logique d'affichage et des applications

React est fait en Javascript et vous apporte une couche d'abstraction pour développer vos applications.

Procédons étape par étape pour créer votre première application en React.

### NPX

Comme vous travaillez dans le web, vous travaillerez la plus part du temps dans le monde de l'open source. C'est à dire
que la communauté accepte de partager son code et vous le partage. React est open source, vous pouvez donc voir comment
il est fait si vous voulez en savoir plus et vous pouvez même proposer une modification de son code.

`npx` permet d'executer des commandes javascript que vous avez soit téléchargé soit qui sont sur le serveur `NPM
REGISTRY` qui contient beaucoup des packets développés en Javascript.

Pour votre première commande vous exécuterez donc:

```bash
npx create-react-app stackerine-react-hello
```

qui va créer automatiquement votre première application en utilisant la command `create-react-app`.

Des paquets vont être téléchargé et la structure de votre application créee.

### yarn start

Entrez dans le répertoire de votre application grâce avec:

```bash
cd stackerine-react-hello
```

et exécutez votre application avec la commande:

```bash
yarn start
```

Cette commande va compiler les fichiers javascript et vous les proposer à travers un serveur. Voter navigateur devrait
se lancer et votre première application devrait s'afficher.

Pour arrêter l'exécution du programme, il vous suffira d'utiliser le raccourci `CTRL + C`

### En savoir un peu plus sur votre nouvelle application

Le premier fichier utilisé par votre application est le fichier `public/index.html`. C'est la base de votre application.

`yarn start` est un script qui va ensuite dynamiquement compiler les fichiers javascript, les concaténer en un seul grand fichier javascript et l'ajouter dynamiquement à la page `index.html`.

Le fichier de départ est le fichier `src/index.js`. Nous verrons par la suite quelles sont les instructions contenues dans ce fichier.

## CONCLUSION

Bravo, vous savez désormais créer une application React. Dans les exercices relatifs à cette leçon, nous apporterons les
premières modifications à notre application.

## DOCUMENTATION
