# Comment fonctionne le web ?

## INTRO

Le web est un systeme distribué qui sert a consulter des sites et applications.
Le web inclue differentes technologies qui permettent de fonctionner.
Ces technologies sont ouvertes et gratuites, nous pouvons donc démarrer
l'apprentissage.

## OBJECTIFS

Nous voulons comprendre comment fonctionne le web dans les grandes lignes:

* Avoir une idée générale de ce qui se passe quand on tape une URL dans Chrome
* Comprendre la séparation client / serveur (Front / Back)
* Connaitre les 3 technologies Front (HTML, CSS, JavaScript)

## COURS

### Une requête web

Lorsqu'on tape l'addresse (URL) d'un site web dans Chrome, on envoie ce qu'on appelle une requête.
Nous demandons à Chrome de télécharger plusieurs fichiers sur un ordinateur distant en passant par Internet. L'URL sert à trouver cet ordinateur distant, puis à savoir quels fichiers télecharger.
Cet ordinateur distant sur lequel on a récupéré les fichiers est souvent appelé _serveur_ (car il sert des requêtes).
Le navigateur (Chrome par exemple) est souvent appelé le _client_ (car il envoie une requête).

Parfois, le serveur a besoin de faire un peu de travail avant de pouvoir répondre au client, il crée le fichier à renvoyer au client. On parle dans ce cas d'application web plutot que de site web.

Dès qu'on fait une action sur un site web (chercher sur Google, mettre à jour son statut Facebook, acheter sur Amazon...), on envoie des requêtes aux serveurs du site web (Google, Facebook ou autres...)

### Les langages du web

Lorsque le serveur répond, il renvoie un fichier contenant du code.
Le navigateur (Chrome) lit ce code et affiche la page web à l'écran.

Ce code est écrit dans un langage appelé **HTML**.
Il sert à décrire le texte à afficher à l'écran.

Un deuxième langage appelé **CSS** est utilisé pour aider le navigateur à dire dans quel style il faut afficher ce texte.

Enfin, un troisième langage appelé **JavaScript** sert à ajouter du comportement à la page, par exemple pour dire ce qu'il doit se passer quand on clique sur un bouton.

## DOCUMENTATION

* Version plus technique de ce cours sur [MDN](https://developer.mozilla.org/fr/Apprendre/Commencer_avec_le_web/Le_fonctionnement_du_Web)

* Vidéo d'introduction sur [Youtube](https://youtu.be/qb_Hvve8JKY)
