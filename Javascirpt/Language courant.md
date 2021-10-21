# Javascript (variables et autres fonctions)

## - Les variables
||Scope|Reassignable|Mutable|Temporal Dead Zone|
|-|-|-|-|-|
const|Block|No|Yes|Yes
let|Block|Yes|Yes|Yes
var|Function|Yes|Yes|No

## - Les sélécteurs

- **.document** : point d'entrée dans le contenu de la page Web, qui est l'arborescence DOM.
- **.getElementById()** : Récupère un élément grace a son ID.
- **.getElementById()** : Récupère des éléments grace a sa classe.
- **.querySelectorAll()** : Récupere tous les éléments selectionnés (renvoie un array).
- **.querySelector()** : Récupere l'éléments selectionnés

## - .textContent :
- Change le contenue text ou l'ajoute dans la balise.

## - innerHtml

- Insert du html avec du contenue text dans la balise parente séléctionné 
## - .style.color :
- Permet de changer le style selctionné , ici on change la couleur.

## - .classlist.add :
- Permet de modifier le contenue des class en HTML , ici on ajoute une class.

## - prompt('contenue text'):
- Affiche une fenetre pop-up avac le text redigé.

## - NaN 

- « Not a Number », en français « Pas un Nombre ou Non Numérique ».
## - .find

```
const greaterThanZero = numbers.find(function(n) {
  return n > 0; // return number just greater than 0 is present
});
console.log(greaterThanZero); // 1
```





