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
Utilisation des breakpoints
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
