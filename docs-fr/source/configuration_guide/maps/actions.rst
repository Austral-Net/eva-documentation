==================
Actions génériques
==================

***********************
Activer le mode édition
***********************

Afin de pouvoir cloner/déplacer/modifier/supprimer des objets de d'une carte, il faut activer le mode édition

1. Etendre le menu de navigation des vues
2. Cliquer sur **modifier la vue**

.. image :: /images/configuration/menu_active_edit_mode_01.png
   :align: center 

3. Cliquer sur **Editer la carte** ==> **Tout Bloquer/Débloquer**
4. L’indicateur **Edit Mode!** apparait. Vous êtes en mode édition

.. image :: /images/configuration/menu_active_edit_mode_02.png
   :align: center 

Vous pouvez maintenant cloner/déplacer/modifier/supprimer des objets.

.. note:: Il ne faut pas oublier de désactiver le mode édition une fois le modification terminée à l'aide du menu **Editer la carte** ==> **Tout Bloquer/Débloquer**


*****************
Ajouter un objet
*****************

L’ajout d’objet sur la carte se fait depuis le menu **Editer la carte** ==> **Ajouter...** . 3 catégories d’objets sont disponibles:

1. Icône
2. Ligne
3. Objet spécial 

.. image :: /images/configuration/menu_add_object.png
   :align: center 


******************
Dupliquer un objet
******************

Principe
========

La duplication d'un objet permet de copier/cloner celui-ci afin de pouvoir réutiliser ses attributs pour la création d'un nouvel objet.
Exemple : J'ai 10 serveurs web identiques à représenter :

*	J'ajoute le premier serveur web avec tous les attributs nécessaires
*	Je duplique cet objet 9 fois
*	Je n'ai plus qu'à changer le noms de chaque duplication pour les adapter aux 9 autres serveurs web à représenter

Grâce à cette méthode, il n'est plus nécessaire de créer unitairement chaque objet.

Pratique
========

Pour dupliquer un objet :

1.	**Clic-droit sur l'objet** que vous souhaitez dupliquer
2.	Dans la menu, cliquer sur **Clone object**

.. image :: /images/configuration/map_clone_object_01.png
   :align: center 

3.	**Cliquer ensuite sur une zone de la carte** pour indiquer la position de l'objet
4.	**Modifier le nom** de l'objet puis cliquer sur **Save**

.. image :: /images/configuration/map_clone_object_02.png
   :align: center 

*****************
Changement massif
*****************

Principe
========

Les changements massifs permettent d'appliquer un changement sur plusieurs objets.

Exemple : L'ensemble des serveurs web précédemment créés changent de communauté SNMP.
Un changement massif permet de modifier cette communauté sans avoir la peine de modifier chaque fiche de chaque hôte unitairement.

Pratique
========

Pour effectuer un changement massif :

#.	Sélectionnez les objets que vous souhaitez modifier
#.	Dans le menu **More actions...** cliquez sur **Changement massif**

La fenêtre de changement s'ouvre, il existe deux types de changements :

*	Incrémentale : signifie que la modification va s'ajouter aux options déjà existantes
*	Remplacement : signifie que la modification va écraser les options déjà existantes

******************
Activer/Désactiver
******************

Principe
========

L'activation et la désactivation des objets permettent de prendre en compte ou non l'objet lors de la génération de la configuration.
Le principal intérêt est de pouvoir garder la configuration d'un objet sans pour autant l'appliquer.

Pratique
========

Pour activer/désactiver un objet :

#.	Sélectionnez les objets que vous souhaitez modifier
#.	Dans le menu **More actions...** cliquez sur **Activer/Désactiver**

Il est également possible d'activer ou de désactiver un objet via le champ "Statut" de la fiche de détails de l'objet ou en utilisant les icônes suivantes :

*	|enabled| pour activer
*	|disabled| pour désactiver

.. |enabled|    image:: /images/enabled.png
.. |disabled|    image:: /images/disabled.png
