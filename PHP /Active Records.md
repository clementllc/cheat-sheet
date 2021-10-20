# Active records

## Etape 1

Je fabrique autant de classe que de TABLES dans ma BDD
Ces classes vont porter le nom des tables qu'elles représentent (a une difference près, MAJUSCULE sur la première lettre du fichier qui va contenir ma classe)

## Etape 2 

Dans ces classes, je vais fabriquer autant de propriétés que de colonnes, et ces dernières vont porter le même nom que mes colonnes

## Etape 3 

Pour chaque propriété je fabrique un Getter/setter (Sauf l'id !).
Je peux faire clic droit sur une propriété et clic sur "Insert Getter/setter"

ATTENTION, si j'ai un underscore dans le nom de ma propriété, je vais modifier le nom de mon Getter et Setter pour passer en camelCase

## Etape 4

Il ne me reste plus qu'a coder des methodes dans cette classe pour pouvoir récupérer les données en BDD 


Un Modèle est une classe et donc un plan de fabrication 
représentant une entité de la BDD.
Pour fabriquer ce plan, on va se calquer sur le nom et les 
champs de la table correspondante dans la BDD. Un modèle 
possède des proporétés et des méthodes.
Les modèles sont codés dans des classes spécifiques qui permettent de manipuler les données utilisées par notre site web.
Avec Active Records ce sont les modèles qui s'occupent d'aller chercher les informations dans la BDD (pour cela, on créé des methodes dans la classe du modèle)
Les objets sont des instanciations de classes. Des objets issus de la meme classes possedent les mêmes propriétés et ont acces aux même methodes mais ils peuvent avoir chacun des valeurs de proprétés differentes

Exemple pour le modele Brand : LEs objets crées à partir de la classe modèle Brand correspondent chacun a UNE LIGNE de la table 'brand' dans la BDD
