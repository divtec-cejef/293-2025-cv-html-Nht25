## A) Normalize.css doit être en local dans `css/`
- Veuillez placer Normalize en local dans `./css/normalize.css`
- Et modifier le lien dans le `<head>` :
```
<link rel="stylesheet" href="./css/normalize.css">
```

## B) Chemins des favicons : retirer les espaces et utiliser `./`
- Vos chemins contiennent un espace au début (`" ./favicon..."`) ce qui peut casser le chargement
- Veuillez écrire par exemple :
```
<link rel="icon" type="image/png" sizes="32x32" href="./favicon-32x32.png">
```
- Même principe pour les autres fichiers (apple-touch-icon, manifest, etc.)
- Utilisez les bonnes favicon selon les tailles définies (attribut : `size`)

## C) Image du header : doit être dans `img/` + lien cliquable correct
- Votre image est dans `./img/img_Nihat.jpg`
- Veuillez faire en sorte que le lien ouvre cette image :
```
<a href="./img/img_Nihat.jpg" target="_blank" rel="noopener noreferrer">
  <img src="./img/img_Nihat.jpg" alt="Avatar de Nihat">
</a>
```
- Et supprimez tout fichier image placé à la racine si ce n’est pas demandé

## D) Navigation : ne pas utiliser `target="_blank"` pour des ancres
- Les liens du menu pointent vers des sections de la même page (`#...`)
- Veuillez enlever `target="_blank"` sur ces liens, sinon cela ouvre un nouvel onglet inutilement

## E) Ajouter `rel="noopener noreferrer"` quand vous utilisez `target="_blank"`
- Pour tous les liens qui ont `target="_blank"`, veuillez ajouter :
  - `rel="noopener noreferrer"`

## F) Corriger le HTML invalide (listes et balises non fermées)
- Vous avez des listes `<ul>` placées à l’intérieur de `<p>` : ce n’est pas valide
- Veuillez fermer le paragraphe avant d’ouvrir une liste
- Il manque aussi des fermetures de balises dans certaines listes (ex: `<ul>` / `<li>`)
- Exemple correct :
```
<p>Mon texte…</p>
<ul>
  <li>Élément 1</li>
  <li>Élément 2</li>
</ul>
```

## G) Mettre les styles dans le CSS (pas dans le HTML)
- Vous utilisez `style="background-color: red;"`
- Veuillez déplacer cela dans `css/main.css` (c’est plus propre et plus facile à maintenir)

## Autres
- Attention à l'indentation et à la lisibilité du code
- Description dans le `<head>`
