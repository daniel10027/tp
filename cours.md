# Cours SQL
_____________
Base du langage SQL et des bases de données

SQL SELECT

L’utilisation la plus courante de SQL consiste à lire des données issues de la base de données. 
Cela s’effectue grâce à la commande SELECT, qui retourne des enregistrements dans un tableau de
résultat.
Cette commande peut sélectionner une ou plusieurs colonnes d’une table.

Commande basique

L’utilisation basique de cette commande s’effectue de la manière suivante :

>>> SELECT nom_du_champ
>>> FROM nom_du_tableau

Cette requête va sélectionner (SELECT) le champ « nom_du_champ » provenant (FROM) du
tableau appelé « nom_du_tableau ».

Exemple

Imaginons une base de données appelée « client » qui contient des informations sur les clients d’une
entreprise.
Table « client » :

>>> identifiant     prenom    nom       ville
>>> 1               Pierre    Dupond    Paris
>>> 2               Sabrina   Durand    Nantes
>>> 3               Julien    Martin    Lyon
>>> 4               David     Bernard   Marseille
>>> 5               Marie     Leroy     Grenoble
