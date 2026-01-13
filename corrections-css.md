## A) Effet de survol des liens peu pertinent

CSS actuel :
```
a:hover {
color: blue;
}
```

Problème :

* la couleur ne change pas → effet invisible

À améliorer :
```
a:hover {
color: darkred;
text-decoration: underline;
}
```

💡 *Un effet de survol doit être visible pour l’utilisateur.*

> *Un lien interactif doit clairement réagir au passage de la souris.*

---

## B) Ombre manquante

Aucune ombre (`box-shadow`) n’est utilisée.

À ajouter par exemple :
```
section {
box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
}
```

💡 *Les ombres aident à séparer visuellement les blocs.*

---

## C) Largeur maximale et centrage absents

Actuellement :

* le contenu prend toute la largeur de l’écran
* pas de centrage horizontal réel

À corriger :
```
main {
max-width: 800px;
margin: 0 auto;
}
```

💡 *Limiter la largeur améliore la lisibilité.*

> *Un texte trop large fatigue rapidement l’œil.*

---

## D) Images : règle correcte mais redondante

CSS actuel :
```
img {
max-width: 100%;
height: auto;
width: auto;
}
```

Remarque :

* `width: auto` est inutile ici

À simplifier :
```
img {
max-width: 100%;
height: auto;
}
```

💡 *`max-width: 100%` suffit pour rendre une image responsive.*

---


### 1️⃣ Balises non fermées ❌

Dans la section `formation` :

* `<ul>` ouvert mais jamais fermé

Impact :

* structure HTML cassée
* CSS imprévisible

