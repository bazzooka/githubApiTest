# Introduction au HTML

## INTRO

HTML est un langage standardisé qui sert à définir la structure et le contenu
d'une page web.
Il sert à écrire du texte, afficher des images...
C'est le "squelette" d'une page web.

## OBJECTIFS

Nous voulons comprendre en quoi consiste le HTML:

* Qu'est ce qu'un document structuré ?
* Qu'est ce qu'une balise ?
* Comment écrire une page HTML ?

## COURS

Le HTML sert à afficher du contenu: texte, images, vidéos...

C'est un langage conçu pour être lu à la fois par les humains
et par un logiciel qui va s'en servir pour afficher la page:
le navigateur web (comme Chrome, Firefox, Safari ou Internet Explorer).

Vu qu'il sert à afficher du texte, il faut un moyen pour le navigateur
de distinguer ce qui sera affiché des instructions pour afficher.
C'est pour ça qu'on utilise des caractères spéciaux pour entourer le texte
qui est à destination du navigateur: `<` et `>`.

Par exemple, l'instruction qui sert à afficher un paragraphe
s'appelle `p` (comme paragraphe), et on l'entoure avec `<` et `>` pour dire
au navigateur qu'il doit en faire quelque chose:
`<p>`

On peut ensuite écrire le texte que l'on veut afficher sur la page web.
`<p>Bonjour tout le monde`

On dit que `<p>` est une **balise** (`tag` en anglais).

Le langage HTML est tout simplement un ensemble de balises.

Pour aider le navigateur à bien afficher le texte, nous devons lui dire quand
notre paragraphe est fini: pour cela on utilise une **balise fermante**:
C'est la même avec un `/` avant le nom de la balise.
Donc pour un paragraphe, la balise fermante sera `</p>`.

La façon propre d'écrire un paragraphe est donc:
`<p>Bonjour tout le monde</p>`

En résumé:

* `<p>` est la balise ouvrante: le paragraphe commence
* `Bonjour tout le monde` est le contenu de la balise
* `</p>` est la balise fermante: le paragraphe est terminé
* Tout ça ensemble forme un **élément**.

Il existe plusieurs dizaines de balises, avec chacune leur utilité (afficher une
liste, afficher un tableau, afficher une image...).

## DOCUMENTATION

* [MDN](https://developer.mozilla.org/fr/Apprendre/Commencer_avec_le_web/Les_bases_HTML)**\_**
