Configuration de l'ordonnanceur
===============================

Une fois l'installation réalisée, il faut intégrer ce collecteur distant dans la configuration Centreon.

#. Rendez-vous dans le menu **Configuration > Collecteurs**
#. Dupliquez le fichier de configuration du serveur Central et éditez-le
#. Modifiez les paramètres suivants, puis sauvegardez :

* Changez le **Nom du collecteur**.
* Entrez l'adresse IP du collecteur dans le champ **Adresse IP**.
* Activez le collecteur en cliquant sur **Activé** dans le champ **Statut**.

.. image:: doc/fr/images/guide_utilisateur/configuration/10advanced_configuration/07addpoller.png
   :align: center

#. Rendez-vous dans le menu **Configuration > Collecteur > Configuration du moteur de collecte**
#. Sélectionnez la configuration qui correspond au dernier poller ajouté
#. Modifiez les paramètres suivants, puis sauvegardez :

* Dans l'onglet **Fichiers**

  * Modifiez le **Nom de la configuration**
  * Vérifiez que le **Collecteur lié** est bien celui précédemment créé
  * Modifiez si besoin le **Fuseau horaire / Localisation**

.. image:: /images/guide_utilisateur/configuration/10advanced_configuration/07addengine.png
   :align: center

* Dans l'onglet **Données** - Champ **Multiple module broker** vérifiez / ajoutez les configurations entrées suivantes ::

   /usr/lib64/centreon-engine/externalcmd.so
   
   /usr/lib64/nagios/cbmod.so /etc/centreon-broker/poller-module.xml

.. image:: /images/guide_utilisateur/configuration/10advanced_configuration/07addpoller_neb.png
   :align: center 

Configuration de Centreon Broker
================================

Il est nécessaire de générer un fichier de configuration pour le broker Centreon Broker :

#. Rendez-vous dans le menu **Configuration > Collecteurs >Configuration de Centreon Broker**
#. Cliquez sur le bouton **Ajouter**

* Dans l'onglet **Général**

  * Sélectionnez le **Collecteur**
  * Saisissez le **Nom** de la configuration
  * Saisissez le **Nom du fichier de configuration** qui doit être identique à celui défini dans la configuration de Centreon Engine, par exemple poller-module.xml
  * Cochez la case **Non** pour la configuration **Link to cbd service**

.. image:: /images/guide_utilisateur/configuration/10advanced_configuration/07_Addbroker.png
   :align: center

* Dans l'onglet **Output**

  * Ajoutez une configuration de type **TCP - IPv4**
  * Saisissez le **Nom**
  * Saisissez le **Port de connexion**, par défaut **5669**
  * Saisissez l'adresse IP (**Hôte distant**) du serveur Centreon central vue par ce collecteur

.. image:: /images/guide_utilisateur/configuration/10advanced_configuration/07_Addbroker_output.png
   :align: center

* Sauvegardez la configuration

Configuration de Centreontrapd
==============================

Il est nécessaire de modifier les fichiers de configuration de Centreontrapd afin que le service puisse interroger la base de données SQLite (voir chapitre :ref:`configuration_advanced_snmptrapds`).

Synchronisation des sondes
==========================

Vous pouvez synchroniser les sondes entre votre serveur Central et vos serveurs collecteur distants en utilisant l'utilitaire **rsync**.

.. warning::
   Ne pas réaliser cette action si vos sondes dépendent de librairies tierces devant au préalable être installées.

Echange de clés SSH
===================

Afin que le serveur central puisse exporter les fichiers de configuration du moteur de supervision, il est nécessaire d'effectuer un échange de clé SSH entre le serveur central et le nouveau serveur collecteur distant.

Sur le serveur collecteur distant :

#. Connectez-vous en tant que 'root'
#. Modifiez le mot de passe de l'utilisateur centreon :

::

	# passwd centreon

Sur le serveur central :

1. Connectez-vous en tant que 'centreon'

::

    # su - centreon

2. Si vous n'avez pas déjà généré une paire de clé publique/privée, tapez la commande suivante (laissez les options par défaut) :

::

	$ ssh-keygen
	
3. Puis exportez votre clé SSH vers le serveur collecteur distant :

::

	$ ssh-copy-id -i /var/spool/centreon/.ssh/id_rsa.pub centreon@[ADRESSE_IP_DU_POLLER]

4. Vérifiez que vous pouvez vous connecter depuis le serveur central vers le serveur collecteur distant en tant qu'utilisateur centreon. Vous pouvez utiliser la commande :

::

	$ ssh centreon@[ADRESSE_IP_DU_POLLER]

Exportation de la configuration
===============================

Il ne reste plus qu'à exporter la configuration afin de vérifier que l'installation du serveur collecteur distant s'est bien déroulée.

.. note::
    Référez-vous à la documentation :ref:`Déployer la configuration<deployconfiguration>`
