# 36pixels CSS grid

Grille CSS utilisant le display flex.

## Démarrer le développement

Ces instructions vous fourniront une copie du projet opérationnel sur votre ordinateur local à des fins de développement et de test.

### Pré-réquisites

```
npm
webpack
git
```

### Installation

Installation du projet via shell

```
npm install
```

Pour lancer Webpack et commencer à tester

```
npm run build
```

## Utilisation  

### Les classes

Le grille fonctionne avec des breakpoints qui sont définits dans le fichier variable.scss. De base, on propose trois breakpoints : small, medium et large.

La grille se compose de :

=> container : fixe la largeur globale de la grille

=> row : fixe la structure de base de la row

=> column/columns // small-X medium-X large-X : fixe la taille du contenu en fonction des breakpoints.

Classe possible pour la row :
```
.row / .row-fluid
=> taille de la variable $global-width / 100% de l'écran.

--justify-start
--justify-end
--justify-center
--justify-around
--justify-between
=> justification horizontal de la row

--align-star
--align-center
--align-end
--align-stretch
=> justification verticale de la row

.hide-for-small
.hide-for-medium
.hide-for-large
.show-for-small
.show-for-medium
.show-for-large
=> Afficher ou cacher certains éléments pour certains breakpoints
```

Exemple basique de structure de grille :
```
<div class="container">
    <div class="row--justify-center--align-stretch hide-for-medium show-for-small">
        <div class="columns small-12 large-6"></div>
        <div class="columns small-12 large-6"></div>
    </div>
</div>
```

### Les Breakpoints

En CSS, il est possible d'utiliser des breakpoints pour donner un style spécifique à certains élements selon la taille de l'écran.

```
@include breakpoint( $size ou $breakpoint, $direction) {
    //CSS
}
Exemple :
@include breakpoint( 'large', 'down') {}
@include breakpoint( '1024px', 'down') {}
```

### Autres

=> Pour reproduire un equalizer, on peut utiliser la fonction '--align-stretch' qui va permettre à tous les enfants directs de la row d'avoir la même hauteur.

=> Pas besoin de renseigner tous les breakpoints en HTML, par exemple si on veut que en small et en medium un colonne soit à 12 il suffit de mettre : class="small-12 large-6 column".
