=========
Les hôtes
=========

Un hôte peut être représenté sour forme d'icône, de widget ou de ligne.

La représentation la plus adaptée est l'icône.

*****************************
Ajouter un objet de type hôte
*****************************

Tous les ajouts d'hôtes se font dans le menu **Editer la carte** ==> **Ajouter un icône** ==> **Host**.

.. image :: /images/configuration/map_add_icone_host_01.png
   :align: center 

**Cliquer ensuite sur une zone de la carte** pour indiquer la position de l'objet. La fenêtre de configuration apparait.

********************************
Configurer un objet de type hôte
********************************

Configuration minimale
======================

1. Sur l’onglet General, sélectionner le **host_name** depuis la liste déroulante
2. Cliquer sur **Save** pour créer l’hôte
3. L’hôte apparait sur la carte

.. image :: /images/configuration/map_add_icone_host_02.png
   :align: center 

Configuration avancée
=====================

Plusieurs onglets sont disponibles pour la configuration de l'objet. Chaque onglet regroupe plusieurs propriétés qui permettent de modifier l'aspect ou le comportement de l'objet hôte:

* **General** - Modifier l'hôte associé à l'objet, positionner l'objet
* **Appearance** - Modifier le type de rendu pour l'objet
* **Status** - Modifier les paramètres de calcul du statut de l'objet
* **Actions** - Modifier les paramètres d'interactions avec l'objet
* **Label** - Modifier l'apparence la positon du label
* **Worldmap** - Modifier le comportement de l'objet sur une carte de type Worldmap


Onglet General
--------------

+----------------+----------------+------------------------------------------------------+
| Valeur         | Par défaut     | Description                                          |
+================+================+======================================================+
| **host_name**  |                | Nom de l'hôte comme définit dans Centreon            |
+----------------+----------------+------------------------------------------------------+
| backend_id     | Hérité(global) | Backend-ID de type centreonbroker                    |
+----------------+----------------+------------------------------------------------------+
| x              |                | coordonées sur l'axe des X                           |
+----------------+----------------+------------------------------------------------------+
| y              |                | coordonées sur l'axe des Y                           |
+----------------+----------------+------------------------------------------------------+
| z              |                | coordonées sur l'axe des Z (profondeur)              |
+----------------+----------------+------------------------------------------------------+
| object_id      |                | Identifiant unique de l'objet généré automatiquement |
+----------------+----------------+------------------------------------------------------+

Onglet Appearance
-----------------

+---------------------+------------------------+----------------------------------------------------------------------+
| Valeur              | Par défaut             | Description                                                          |
+=====================+========================+======================================================================+
| **view_type**       | icon                   | Cette option définit le type de rendu de cet objet. Les valeurs      |
|                     |                        | possibles sont: "Icon ", "Line " ou "Gadget"                         |
+---------------------+------------------------+----------------------------------------------------------------------+
|                     | **Option pour Icon**   |                                                                      |
+---------------------+------------------------+----------------------------------------------------------------------+
| **iconset**         | Hérité(global)         | Choix du jeu d'icones                                                |
+---------------------+------------------------+----------------------------------------------------------------------+
| icon_size           | Hérité(nagvis.ini.php) | Changer la taille d'affiche du jeu d'icones sur la carte. Si elle    |
|                     |                        | est laissée vide, les images IconSet seront affichées à leur taille  |
|                     |                        | d'orignie. Vous pouvez configurer cette option avec un seul entier   |
|                     |                        | pour donner la largeur et la hauteur à la fois, mais vous pouvez     |
|                     |                        | également fournir deux entiers séparés par des virgules pour         |
|                     |                        | spécifier des valeurs différentes pour la largeur et la hauteur.     |
+---------------------+------------------------+----------------------------------------------------------------------+
|                     | **Option pour Line**   |                                                                      |
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
|                     | **Option pour Gadget** |                                                                      |
+---------------------+------------------------+----------------------------------------------------------------------+
| **gadget_url**      |                        | La valeur peut être un script gadget situé dans (nagvis/gadgets),    |
|                     |                        | par exemple "std_speedometer.php"                                    |
+---------------------+------------------------+----------------------------------------------------------------------+
| gadget_scale        |                        | L'échelle du gadget. L'échelle par défaut est 100 (pour cent). Les   |
|                     |                        | gadgets doivent pouvoir être redimensionnés par ce paramètre.        |
+---------------------+------------------------+----------------------------------------------------------------------+
| gadgets_opts        |                        | Paramêtres facultatifs spécifiques aux gadgets. Le contenu peut être |
|                     |                        | défini librement pour chaque gadget. La valeur est traitée comme GET |
|                     |                        | param "opts"                                                         |
+---------------------+------------------------+----------------------------------------------------------------------+

Onglet Status
-------------

+------------------------+----------------+---------------------------------------------------------------------------+
| Valeur                 | Par défaut     | Description                                                               |
+========================+================+===========================================================================+
| exclude_members        |                | Il est possible d'exclure complètement les objets membres lors de la      |
|                        |                | récupération des informations sur l'objet à partir du backend. Les        |
|                        |                | éléments filtrés n'apparaîtront pas dans cet objet. Pour plus de détails  |
|                        |                | sur la syntaxe du filtre, consultez la définition d'exclusion regex.      |
+------------------------+----------------+---------------------------------------------------------------------------+
| exclude_members_states |                | Il est possible d'exclure un ou plusieurs états des membres lors du       |
|                        |                | calcul de l'état récapitulatif des objets. Les éléments filtrés           |
|                        |                | apparaîtront dans les listes de membres mais ne seront pas utilisés pour  |
|                        |                | les calculs de résumé d'état. Pour plus de détails sur la syntaxe du      |
|                        |                | filtre, consultez la définition d'exclusion regex.                        |
+------------------------+----------------+---------------------------------------------------------------------------+
| only_hard_states       | Hérité(global) | Définit si les états soft doivent être ignorés.                           |
+------------------------+----------------+---------------------------------------------------------------------------+
| recognize_services     | Hérité(global) | Définit si les services de l'hôte affectent l'état affiché. S'il est      |
|                        |                | défini sur "1", un service critique sur l'hôte entraînera également un    |
|                        |                | affichage de l'état de l'hôte. S'il est réglé sur "Oui", seul l'état de   |
|                        |                | l'hôte Centreon (UP ou DOWN) sera utilisé et les services de l'hôte       |
|                        |                | seront ignorés.                                                           |
+------------------------+----------------+---------------------------------------------------------------------------+

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
| hover_delay        | Hérité(nagvis.ini.php) | Délai d'apparition du *hover menu*                                     |
+--------------------+------------------------+------------------------------------------------------------------------+
| hover_template     | Hérité(global)         | *Hover template* pour cet objet                                        |
+--------------------+------------------------+------------------------------------------------------------------------+
| hover_url          |                        | URL qui doit être affichée dans le menu de survol au lieu de           |
|                    |                        | l'information standard. Il y a quelques macros disponibles:            |
|                    |                        | [host_name]: cette macro représente le nom de l'objet.                 |
+--------------------+------------------------+------------------------------------------------------------------------+
| hover_childs_show  | Hérité(nagvis.ini.php) | Activer/Désactiver l'affichage des objets enfants                      |
+--------------------+------------------------+------------------------------------------------------------------------+
| hover_childs_sort  | Hérité(nagvis.ini.php) | Méthode de trie des objets enfants                                     |
+--------------------+------------------------+------------------------------------------------------------------------+
| hover_childs_order | Hérité(nagvis.ini.php) | Ordre d'affichage des objets enfants                                   |
+--------------------+------------------------+------------------------------------------------------------------------+
| hover_child_limit  | Hérité(nagvis.ini.php) | Nombre maximum d'enfants à afficher. Configurer sur -1 pour désactiver |
|                    |                        | la limite.                                                             |
+--------------------+------------------------+------------------------------------------------------------------------+
| url                |                        | URL à laquelle l'icône doit être liée. Le lien par défaut est pour les |
|                    |                        | CGI Nagios. Les macros [host_name], [htmlcgi] et [htmlbase] sont       |
|                    |                        | disponibles. La valeur peut être définie sur "#" pour désactiver le    |
|                    |                        | lien.                                                                  |
+--------------------+------------------------+------------------------------------------------------------------------+
| url_targert        | _self                  | Cible du lien Icône, cette option utilise <a target=""> (_self est la  |
|                    |                        | même fenêtre). La macro [name] est disponible.                         |
+--------------------+------------------------+------------------------------------------------------------------------+

Onglet Label
------------

+-----------------------+----------------+----------------------------------------------------------------------------------+
| Valeur                | Par défault    | Description                                                                      |
+=======================+================+==================================================================================+
| **label_show**        | Hérité(global) | Activer/Désactiver le label pour cet objet                                       |
+-----------------------+----------------+----------------------------------------------------------------------------------+
| **label_text**        | [name]         | Texte du label. Macros disponibles: [name], [alias], [output]                    |
+-----------------------+----------------+----------------------------------------------------------------------------------+
| label_x               | Hérité(global) | Label Position X (si préfixe + ou -, relatif au coin supérieur gauche des        |
|                       |                | icônes, sinon position absolue)                                                  |
+-----------------------+----------------+----------------------------------------------------------------------------------+
| label_y               | Hérité(global) | Label Position Y (si préfixe + ou -, relatif au coin supérieur gauche des        |
|                       |                | icônes, sinon position absolue)                                                  |
+-----------------------+----------------+----------------------------------------------------------------------------------+
| label_width           | Hérité(global) | largeur du label en pixel                                                        |
+-----------------------+----------------+----------------------------------------------------------------------------------+
| **label_background**  | Hérité(global) | Couleur d'arrière-plan du label. La couleur doit être donnée en hexcode. Peut    |
|                       |                | aussi prendre "transparent".                                                     |
+-----------------------+----------------+----------------------------------------------------------------------------------+
| **label_broder**      | Hérité(global) | Couleur des bordures du label. La couleur doit être donnée en hexcode. Peut      |
|                       |                | aussi prendre "transparent".                                                     |
+-----------------------+----------------+----------------------------------------------------------------------------------+
| label_style           | Hérité(global) | Style personnalisé pour le texte du label. A configurer comme le contenu de      |
|                       |                | l'attribut de style HTML. Exemple: font-family:sans;font-weight:bold;            |
+-----------------------+----------------+----------------------------------------------------------------------------------+
| label_maxlen          | Hérité(global) | Nombre maximum de caractère à afficher pour le label                             |
+-----------------------+----------------+----------------------------------------------------------------------------------+

Onglet Worldmap
---------------

+----------+------------+----------------------------------------------------------+
| Valeur   | Par défaut | Description                                              |
+==========+============+==========================================================+
| min_zoom | ?          | Valeur de zoom minimum. Doit être compris entre 2 et 18. |
+----------+------------+----------------------------------------------------------+
| max_zoom | ?          | Valeur de zoom maximum. Doit être compris entre 2 et 18. |
+----------+------------+----------------------------------------------------------+