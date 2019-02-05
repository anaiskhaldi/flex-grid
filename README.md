# Grid System
-	Dependendices:
    -   npm
    -   webpack
    -   git
-	Version: 0.0.1

## Install Project
Installation du projet via shell
```shell
$ npm install
```

## Work
Pour lancer webpack
```shell
$ npm run build
```

## Grid
## Utilisation des classes de la grille
```shell
<div class="row--class1--class2">
    <div class="columns small-x medium-x large-x">
```
Exemple
```shell
<div class="row--justify-center--align-stretch">
    <div class="columns small-12 medium-6 large-4">
```

## Utilisation des breakpoints
@mixin breakpoint($size, $direction) {}
```shell
@include breakpoint(large, down) {
    display: none;
}
```
ou
```shell
@include breakpoint(650px, down) {
    display: none;
}
```
