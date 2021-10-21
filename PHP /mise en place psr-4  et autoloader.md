# Mise en place PSR4 & autoloader


## Etape 1 

On va aller dans notre composer.json et on va rajouter quelques lignes de code.
Initialement, mon composer.json :

```
{
    "require": {
        "symfony/var-dumper": "^5.3",
        "altorouter/altorouter": "^2.0"
    }
}

```

Je vais ajouter la section autoload !


```
{
    "require": {
        "symfony/var-dumper": "^5.3",
        "altorouter/altorouter": "^2.0"
    },
    "autoload": {
        "psr-4": {"X\\": "Y/"}
    }
}

```

Ou X : Est un nom de dossier virtuel que j'image de toute pièce et qui sera le dossier virtuel principal de mon projet

Ou Y : Est le nom du dossier physique qui contient toutes les classes

### Exemple concret avec oshop : 

```
{
    "require": {
        "symfony/var-dumper": "^5.3",
        "altorouter/altorouter": "^2.0"
    },
    "autoload": {
        "psr-4": {"Oshop\\": "app/"}
    }
}

```


Ici j'ai donc imaginé un dossier Oshop qui va etre mon dossier virtuel "principal" et d'ai indiqué le dossier app qui contient toutes les classes de mon projetS


## Etape 2

Je vais ranger toutes les classe en respectant la structure suivante 

```

NomDuDossierVirtuelPrincipal\NomDuDossierPhysique
```

Exemple pour le controller MainController qui est dans le dossier Controllers je vais faire :


```php
namespace Oshop\Controllers
```


## Etape 3 

Dans les classes que nous venons de ranger dans des dossier virtuels j'utilise d'autre classe !!
Donc tout est cassé :o ! 
Il faut donc que je corrige mes erreurs

Exemple, dans mon CatalogController j'utilise la classe Product

```php
 public function product($params)
    {
        ...
        $productModel = new Product();
        ...
    }
```

Mais apres rangement dans nos namespace, cette classe Product est soulignée en rouge....
POURQUOI ? 
Car mon CatalogController est rangé dans le namespace
oShop\Controllers

Et la classe produit est rangée dans 
oQhop\Models ! 

Quand je fais new Product, PHP essaye de chercher la classe Product dans le dossier virtuel oShop\Controllers ! 

Il me faut donc rajouter la ligne de code suivante : 

use Oshop\Models\Product


## Etape 4

Une fois que toutes les erreurs sont corrigé, je peux générer mon autoload :
Dans le terminal et a la racine de mon projet je vais taper la commande suivante 

```
composer dumpautoload
```
Je vais avoir le message suivant : 

Generated autoload files


A PARTIR DE MAINTENANT JE PEUX ENLEVER TOUS MES REQUIRE SAUF L'AUTOLOAD