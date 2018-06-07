==========
Les Lignes
==========

Les lignes permettent des créer des liens entre les éléments. Il existe 3 types de lignes:


* **Les lignes dynamiques**: une ligne dont la couleur change en fonction du statut de la ressource
* **Les lignes weathermap**: un ligne qui affiche une données de performance (métrique %, Mbps...) et qui change de couleur en fonction de sa valeur
* **Les lignes apatrides**: une ligne simple sans statut ni données de performance

******************************
Lignes Dynamique et Weathermap
******************************

Lignes Dynamiques
=================

**Les lignes dynamiques**: Une ligne dont la couleur change en fonction du statut d'un hôte ou d'un service

.. image :: /images/configuration/map_line_stateful_collection.png
   :align: center 

Options de configuration "line_type"
------------------------------------

+------------------------+--------------------------------------+
| lignes                 | Description                          |
+========================+======================================+
| \-------><-------\     | Flèches à l'intersection             |
+------------------------+--------------------------------------+
| \--------------->\     | Flèche à une seule extrémité         |
+------------------------+--------------------------------------+
| \----------------\     | Ligne simple sans flèche             |
+------------------------+--------------------------------------+

Lignes Weathermap
=================

**Les lignes weathermap**: un ligne qui affiche une données de performance (métrique %, Mbps...) et qui change de couleur en fonction de sa valeur

.. image :: /images/configuration/map_line_weathermap_collection.png
   :align: center 

Options de configuration "line_type"
------------------------------------

+----------------------+---------------------------------------------------------------------+
| lignes               | Description                                                         |
+======================+=====================================================================+
| \---%---><---%---\   | Flèches à l'intersection + pourcentage. Nécessite un service qui    |
|                      | renvoie des données de performances adaptées                        |
+----------------------+---------------------------------------------------------------------+
| \--%+BW-><-%+BW--\   | Flèches à l'intersection + pourcentage + bande passante. Nécessite  |
|                      | un service qui renvoie des données de performances adaptées         |
+----------------------+---------------------------------------------------------------------+
| \---BW--><--BW---\   | Flèches à l'intersection + bande passante. Nécessite un service qui |
|                      | renvoie des données de performances adaptées                        |
+----------------------+---------------------------------------------------------------------+

Modifier l'apparence d'une ligne
================================

Pour modifier l'apparence d'une ligne, faire un **clic droit sur l'objet** ==> **Modify Object**.

Depuis l'onglet **Appearance**, s'assurer que le champ **view_type** est configuré sur **line**.

Cocher la case **line_type**, puis sélectionner le nouveau type de ligne depuis le **champ déroulant** 


Onglet Appearance
-----------------

+---------------------+------------------------+----------------------------------------------------------------------+
| Valeur              | Par défaut             | Description                                                          |
+=====================+========================+======================================================================+
| **view_type**       | icon                   | Cette option définit le type de rendu de cet objet. Les valeurs      |
|                     |                        | possibles sont: "Icon ", "Line " ou "Gadget"                         |
+---------------------+------------------------+----------------------------------------------------------------------+
| **line_type**       | Hérité(global)         | Spécifier le type de ligne (sans flèche, avec une flèche ou avec     |
|                     |                        | deux flèches)                                                        |
+---------------------+------------------------+----------------------------------------------------------------------+
| line_cut            | 0.5                    | Les lignes avec deux parties ont un espace au milieu de la ligne.    |
|                     |                        | Cela équivaut à une valeur de coupe de ligne de "0.5 ". Il est       |
|                     |                        | possible de déplacer la coupe en changeant cette valeur. Les valeurs |
|                     |                        | valides sont 0.0 à 1.0.                                              |
+---------------------+------------------------+----------------------------------------------------------------------+
| line_witdh          | Hérité(global)         | Définir la largeur de la ligne en px                                 |
+---------------------+------------------------+----------------------------------------------------------------------+
| line_weather_colors | Hérité(global)         | Cela définit les couleurs des couleurs weathermap en fonction des    |
|                     |                        | différents niveaux de pourcentage.                                   |
+---------------------+------------------------+----------------------------------------------------------------------+

**************
ligne apatride
**************

La ligne apatride est un objet spécial sans statut. Détails de la configuration par :ref:`ici<apatride_line>`








