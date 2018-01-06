# HTML document

## INTRO

Bien que la base du HTML soit sous forme de texte, il est souvent nécessaire de
le formaliser sous forme de document.


## OBJECTIFS

Comprendre la structure de base d'un document HTML


## COURS

Une page HTML est servie par le serveur à un client qui la demande par l'intermédiaire du navigateur.
Cette page doit répondre à certaines normes pour que le navigateur sache comment l'interpréter.
Cette norme est définie par le HTML qui est un langage de balise comme nous l'avons déjà vu.

Les éléments obligatoires pour afficher une page HTML sont: 
- le DOCTYPE: qui sert à indiquer au navigateur quel type de marquage est utilisé
- une balise `html`permettant d'indiquer le début de ma page
- une balise de titre: qui donne le titre de ma page
- une balise body: qui encadre le contenu de ma page

Voilà en résumé le contenu minimal d'une page: 

```html
<!DOCTYPE html>
<html> 
    <title>Le titre de ma page</title>
    <body>
        <p>Il s'agit du contenu de ma page</p>
    </body>
</html>
```




## DOCUMENTATION
