==========
Les Cartes
==========

Les cartes vous permettent de visualiser vos données de supervision de manière conviviale.

Chaque utilisateur possède une carte principale à partir de laquelle il va pouvoir accèder à une arboresence de cartes enfants.

Configurer la carte principale d'un utilisateur
===============================================

Depuis le menu principal:

1. Cliquer sur **Outils** ==> **Configuration** ==> **Utilisateurs**. La liste des utilisateurs apparait
2. Dans la liste déorulante **Main View** de l'utilisateur, sélectionner la carte principale à attribuer à l'utilisateur.
3. Cliquer sur le boutton **Modify**

.. note:: Il est nécessaire de déconnecter puis de reconnecter l'utilisateur pour que le changement soit pris en compte



Créer un nouvelle carte
=======================

Depuis le menu principal:

1. Cliquer sur **Outils** ==> **Configuration** ==> **Vues**. La liste des vues apparait
2. Depuis la formulaire situé en haute de page, renseigner les champs **Name**, **Description**, **Image** et **Type**.
3. Cliquer sur le boutton **Add**
   
Description des champs
^^^^^^^^^^^^^^^^^^^^^^

+-------------------+-------------------------------------------------------------------------------+
| Nom               | Description                                                                   |
+===================+===============================================================================+
| **Name**          | Nom unique, correspond au fichier de configuration de la carte                |
+-------------------+-------------------------------------------------------------------------------+
| **Description**   | Description utilisée dans le menu latéral                                     |
+-------------------+-------------------------------------------------------------------------------+
| **Image**         | Image utilisée dans le menu latéral                                           |
+-------------------+-------------------------------------------------------------------------------+
| **Type**          | Type de carte (Classic ou Automap)                                            |
+-------------------+-------------------------------------------------------------------------------+

   

Créer des liens entre les cartes
================================

Afin de créer un arboresence et permettre à l'utilisateur de naviger entre les différentes cartes, il faut créer des liens entre les cartes.

.. image:: /images/configuration/maps/maps-tree.png
   :align: center 

Le point de départ de l'arboresence est la carte principale. Sur cette carte, il faut créer des liens vers les cartes enfants. Le menu latéral gauche sera automatiquement créé en fonction des liens existant entre les cartes.

.. note:: Après avoir créé de nouveaux liens entre les cartes, il est nécessaire de recharger l'interface Web pour voir apparaitre les changements au niveau du menu


Pour créer un lien, il faut **ajouter une icône de type carte**

Ajouter un icône de type Carte
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1. Se placer sur la carte parent et activer le mode édition
2. Depuis le menu, cliquer sur **Ajouter un icône** ==> **Carte**
3. **Cliquer sur un zone** de la carte
4. Depuis la fenêtre **Create Object**, sur l'onglet **General** sélectionner la carte enfant dans le champ déroulant **map_name**
5. L'apparence du lien peut être modifier depuis l'onglet **Appearance** en sélectionnant un autre :ref:`iconset<iconset>`
   


