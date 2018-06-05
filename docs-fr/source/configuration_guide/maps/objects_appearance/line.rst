==========
Les Lignes
==========

Les lignes permettent des créer des liens entre les éléments. Il existe 3 types de lignes:

* Les lignes apatrides: une ligne simple sans statut ni données de performance
* Les lignes dynamiques: une ligne dont la couleur change en fonction du statut d'un hôte ou d'un service
* Les lignes weathermap: un ligne qui affiche une données de performance (métrique %, Mbps...) et qui change de couleur en fonction de sa valeur

**************
ligne apatride
**************

Une ligne simple sans statut ni données de performance

.. image :: /images/configuration/map_line_stateless_collection.png
   :align: center 

Les paramètres à retenir
========================

* **line_type**: Modifier la forme de la ligne
* **line_color**: Modifier la couleur de la ligne
* **line_color_border**: Modifier la couleur de bordure de la ligne

Paramètres
==========

Les paramètre suivants sont disponibles pour l'objet ligne apatride

Onglet General
--------------

+--------------------------+----------------+------------------------------------------------------+
| Valeur                   | Par défaut     | Description                                          |
+==========================+================+======================================================+
| x                        |                | coordonées sur l'axe des X                           |
+--------------------------+----------------+------------------------------------------------------+
| y                        |                | coordonées sur l'axe des Y                           |
+--------------------------+----------------+------------------------------------------------------+
| z                        |                | coordonées sur l'axe des Z (profondeur)              |
+--------------------------+----------------+------------------------------------------------------+
| object_id                |                | Identifiant unique de l'objet généré automatiquement |
+--------------------------+----------------+------------------------------------------------------+


Onglet Appearance
-----------------

+------------------------+------------------------+----------------------------------------------------------------------+
| Valeur                 | Par défaut             | Description                                                          |
+========================+========================+======================================================================+
| **line_type**          | Hérité(global)         | Spécifier le type de ligne (sans flèche, avec une flèche ou avec     |
|                        |                        | deux flèches)                                                        |
+------------------------+------------------------+----------------------------------------------------------------------+
| line_cut               | 0.5                    | Les lignes avec deux parties ont un espace au milieu de la ligne.    |
|                        |                        | Cela équivaut à une valeur de coupe de ligne de "0.5 ". Il est       |
|                        |                        | possible de déplacer la coupe en changeant cette valeur. Les valeurs |
|                        |                        | valides sont 0.0 à 1.0.                                              |
+------------------------+------------------------+----------------------------------------------------------------------+
| line_witdh             | Hérité(global)         | Définir la largeur de la ligne en px                                 |
+------------------------+------------------------+----------------------------------------------------------------------+
| **line_color**         | Hérité(global)         | Définir la couleur de la ligne                                       |
+------------------------+------------------------+----------------------------------------------------------------------+
| **line_color_border**  | Hérité(global)         | Définir la couleur de bordure de la ligne                            |
+------------------------+------------------------+----------------------------------------------------------------------+


Onglet Actions
--------------

+--------------------+------------------------+------------------------------------------------------------------------+
| Valeur             | Par défaut             | Description                                                            |
+====================+========================+========================================================================+
| context_menu       | Hérité(nagvis.ini.php) | Activer/Désactiver le menu contextuel pour cet objet.                  |
+--------------------+------------------------+------------------------------------------------------------------------+
| context_template   | Hérité(nagvis.ini.php) | *Context template* pour cet objet.                                     |
+--------------------+------------------------+------------------------------------------------------------------------+
| hover_menu         | Hérité(nagvis.ini.php) | Activer/Désactiver le *hover menu*                                     |
+--------------------+------------------------+------------------------------------------------------------------------+
| url                |                        | URL à laquelle l'icône doit être liée. Le lien par défaut est pour les |
|                    |                        | CGI Nagios. Les macros [host_name], [htmlcgi] et [htmlbase] sont       |
|                    |                        | disponibles. La valeur peut être définie sur "#" pour désactiver le    |
|                    |                        | lien.                                                                  |
+--------------------+------------------------+------------------------------------------------------------------------+
| url_targert        | _self                  | Cible du lien Icône, cette option utilise <a target=""> (_self est la  |
|                    |                        | même fenêtre). La macro [name] est disponible.                         |
+--------------------+------------------------+------------------------------------------------------------------------+



Onglet Worldmap
---------------

+----------+------------+----------------------------------------------------------+
| Valeur   | Par défaut | Description                                              |
+==========+============+==========================================================+
| min_zoom | ?          | Valeur de zoom minimum. Doit être compris entre 2 et 18. |
+----------+------------+----------------------------------------------------------+
| max_zoom | ?          | Valeur de zoom maximum. Doit être compris entre 2 et 18. |
+----------+------------+----------------------------------------------------------+


***************
ligne dynamique
***************

Une ligne dont la couleur change en fonction du statut d'un hôte ou d'un service

.. image :: /images/configuration/map_line_stateful_collection.png
   :align: center 


