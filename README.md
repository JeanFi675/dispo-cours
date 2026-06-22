# Dispo Cours

Site statique hébergé sur GitHub Pages affichant les places disponibles dans les cours d'escalade.

## Fonctionnement

- `data.json` est mis à jour automatiquement (quotidiennement à 13h) par un script externe.
- `index.html` charge `data.json` et affiche les cours filtrables par catégorie et niveau.
- Les données sont rafraîchies automatiquement toutes les 5 minutes côté client.

## Configuration de l'affichage

En haut du `<script>` dans `index.html`, une constante permet de choisir le mode d'affichage :

```javascript
const DISPLAY_MODE = 'list';   // toutes les infos visibles directement
const DISPLAY_MODE = 'toggle'; // affichage accordéon — cliquer sur un cours pour voir horaire + prof
```

Modifier uniquement cette ligne selon la période, sans toucher à `data.json`.

## Structure

- `index.html` — application complète (HTML + CSS + JS)
- `data.json` — données des places disponibles (mis à jour automatiquement, ne pas modifier)
