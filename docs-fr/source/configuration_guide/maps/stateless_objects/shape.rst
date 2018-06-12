===========
Les Figures
===========

L'objet Figure permet d'afficher une image. L'objet Figure peut être déplacé et positionné n'importe où sur la carte afin d'améliorer la mise en page. Une liste d'image est fournie avec la solution EVA, mais vous pouvez également importer vos propores images.

Importer une image
==================

Pour importer une image, depuis le menu d'édition:

1. Cliquer sur **Options** ==> **Gérer les Figures**. La fenêtre de gestion des figures apparaît.
2. Depuis la section **Upload Shape** => **Choose an Image**, cliquer sur **Choisir un fichier**, puis naviguer jusqu'à votre fichier
3. Cliquer sur **Upload**
4. Le message "The shape has been uploaded" apparaît. Fermer la fenêtre **Gérer les Figures**
   
Les formats suivants peuvent être utilisés:

* PNG
* GIF
* JPEG
   
.. note:: Les images ne peuvent pas être redimensionnée à l'affichage, il faut uploader l'image aux bonnes dimensions.



Créer un objet Figure
=====================

Pour créer une objet Figure, depuis le menu d'édition

1. Cliquer sur **Ajouter un objet spécial** ==> **Figure**. La fenêtre Create Object apparaît.
2. Depuis l'onglet **General**, sélectionner l'image à afficher depuis le champ déroualant **Icon**
3. Cliquer sur **Save**. L'objet Figure apparaît sur la Carte.
   


Onglet General
--------------

+---------------------+------------------------+----------------------------------------------------------------------+
| Valeur              | Par défaut             | Description                                                          |
+=====================+========================+======================================================================+
| icon                |                        | Nom du fichier image. Les fichiers doivent être placés dans le       |
|                     |                        | répertoire shape (par défaut: images / shapes). Il est également     |
|                     |                        | possible d'utiliser une url. L'URL doit être entourée de [ et ]      |
+---------------------+------------------------+----------------------------------------------------------------------+
| x                   |                        | coordonées sur l'axe des X                                           |
+---------------------+------------------------+----------------------------------------------------------------------+
| y                   |                        | coordonées sur l'axe des Y                                           |
+---------------------+------------------------+----------------------------------------------------------------------+
| z                   | 1                      | coordonées sur l'axe des Z (profondeur)                              |
+---------------------+------------------------+----------------------------------------------------------------------+
| enable_refresh      | non                    | Cette option active les mises à jour régulières. Ceci n'est          |
|                     |                        | nécessaire que pour les images dynamique qui changent                |
+---------------------+------------------------+----------------------------------------------------------------------+
| object_id           |                        | Identifiant unique de l'objet généré automatiquement                 |
+---------------------+------------------------+----------------------------------------------------------------------+
