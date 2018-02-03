# Quelques tags HTML

## INTRO

Maintenant que vous savez créer une page HTML il convient d'y ajouter
un peu de forme. On ne peut pas tout représenter sous forme de texte.
Ma page peut contenir des images, des vidéos, des graphiques mais
aussi tout simplement une structure de page avec des titres...

## OBJECTIFS

Gagner quelques mots dans le vocabulaire HTML. Nous apprendrons durant ce
cours l'utilité des balises les plus courantes:

* h1, h2, h3...
* span
* div

## COURS

### Les titres

Les titres sont représentés grâce aux balises: h1, h2, h3, h4, h5, h6.
`<h1>`étant le roi des titres et `<h6>`le plus petit titre.
Normalement la balise `<h1>` n'est présente qu'une fois par page et un
titre de type `<h4>` est un sous-titre d'une balise `<h3>` qui doit être
un sous-titre d'une balise `<h2>`.
Exemple:

```html
<h1>Titre de niveau 1</h1>
<h2>Titre de niveau 2</h2>
<h3>Titre de niveau 3</h3>
```

### Le texte

Comme nous l'avons déjà vu, votre page peut contenir du texte
sous forme de paragraphe grâce à la balise `<p>`.
Vous l'avez remarquer la balise `<p>` créer un paragraphe ou plus simplement
une zone de texte qui est situé sous l'élément suivant.

Parfois il est nécessaire d'afficher du texte sans retour à la ligne,
à la suite de l'élément précédent. Pour cela, nous utiisons
la balise `<span>`.
Exemple:

```html
<span>Mon texte est en ligne</span>
```

### Les conteneurs

Pour encapsuler ou grouper les élements ensemble, on utilise la balise `<div>`.
Cette balise est très pratique quand on souhaite grouper les élements par
section. Par exemple, si je souhaite cacher ma barre de navigation qui contient
plusieurs éléments, je ne vais pas cacher chaque élement un par un, je
peux directement cacher le conteneur qui représente ma barre de navigation.
Exemple:

```html
<div>
    <h2>Un titre</h2>
    <p>Un paragraphe</p>
    <span>Et un texte</span>
</div>
```

### Conclusion

Vous ne le savez pas encore mais le HTML est un langage que l'on peut qualifier
de riche. Il existe beaucoup de tag.
Vous pourrez en avoir un aperçu sur cette page: [Liste de tag HMTL](https://developer.mozilla.org/fr/docs/Web/HTML/Element)
J'attire également votre attention sur une notion qui aura de l'importance
quand il s'agira de styliser votre page: le positionnement des élement.
Certains ont un positionnement de type `block` et d'autres de type `inline`.
Comme vous l'aurez deviné, les éléments de type `block` se mettent verticalement
à la suite les uns des autres, et les élements de type `inline` se mettent
horizontalement les uns à la suite des autres.

## DOCUMENTATION

* [Les titres](https://developer.mozilla.org/fr/docs/Web/HTML/Element/Heading_Elements)
* [Les textes](https://developer.mozilla.org/fr/docs/Web/HTML/Element/span)
* [Les containeurs](https://developer.mozilla.org/fr/docs/Web/HTML/Element/div)
