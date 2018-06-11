===========
Les Gadgets
===========

Les gadgets sont de petits programmes qui génèrent des images ou du code HTML à partir d'informations provenant des ressources. L'idée principale est de fournir les données de performance de Centreon à ces programmes pour les visualiser sous forme de graphes, gauges, textes, camembert, speedomètres, thermomètres, etc.

Les gadgets sont particulièrements adaptés pour représenter des services, mais peuvent aussi être utilisés avec d'autres types de ressources.

Exemple de gadget pour un service Cpu:

.. image :: /images/configuration/gadgets/cpu_speedometer.png 


Modifier l'apparence d'une icône en gadget
==========================================

Pour modifier l'apparence d'une icône et lui attribuer un gadget, faire un **clic droit sur l'objet** ==> **Modify Object**.

Depuis l'onglet **Appearance**, s'assurer que le champ **view_type** est configuré sur **gadget**.

Cocher la case **gadget_url**, puis sélectionner un gadget depuis le **champ déroulant** 


Onglet Appearance
-----------------

+---------------------+------------------------+----------------------------------------------------------------------+
| Valeur              | Par défaut             | Description                                                          |
+=====================+========================+======================================================================+
| **view_type**       | icon                   | Cette option définit le type de rendu de cet objet. Les valeurs      |
|                     |                        | possibles sont: "Icon ", "Line " ou "Gadget"                         |
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

Biliothèque de Gagets
=====================

Gadgets génériques pour services
--------------------------------

00_Service_Generic_Percent_Speed_Meter
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. image :: /images/configuration/gadgets/00_Service_Generic_Percent_Speed_Meter.png 

*Utilisation*:

* Prise en charge de l'option gadget_scale: **oui**
* Prise en charge de l'option gadgets_opts: **non**

00_Service_Generic_Percent_Gauge
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. image :: /images/configuration/gadgets/00_Service_Generic_Percent_Gauge_Horizontal.png 

.. image :: /images/configuration/gadgets/00_Service_Generic_Percent_Gauge_Vertical.png 

*Utilisation*:

* Prise en charge de l'option gadget_scale: **oui**
* Prise en charge de l'option gadgets_opts: **oui**
* Version Horizontale: par défaut
* Version Verticale: configurer l'option **gadgets_opts** avec la valeur **vertical**

00_Service_Generic_Size_Gauge
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. image :: /images/configuration/gadgets/00_Service_Generic_Size_Gauge_Horizontal.png 

.. image :: /images/configuration/gadgets/00_Service_Generic_Size_Gauge_Vertical.png 

*Utilisation*:

* Prise en charge de l'option gadget_scale: **oui**
* Prise en charge de l'option gadgets_opts: **oui**
* Version Horizontale: par défaut
* Version Verticale: configurer l'option **gadgets_opts** avec la valeur **vertical**

00_Service_Generic_Size_Pie
^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. image :: /images/configuration/gadgets/00_Service_Generic_Size_Pie.png 

*Utilisation*:

* Prise en charge de l'option gadget_scale: **oui**
* Prise en charge de l'option gadgets_opts: **non**

00_Service_Generic_Value_Text
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. image :: /images/configuration/gadgets/00_Service_Generic_Value_Text_Circle.png 

.. image :: /images/configuration/gadgets/00_Service_Generic_Value_Text_Square.png 

*Utilisation*:

* Prise en charge de l'option gadget_scale: **oui**
* Prise en charge de l'option gadgets_opts: **oui**
* Choix de la données de perfomrance: 
	* Configurer l'option **gadgets_opts** avec la valeur **label=nom_perfdata**
	* Configurer l'option **gadgets_opts** avec la valeur **description=Ma_description_perssonalisee**
	* Exemple: **label=connection_time description=Temps_de_Connexion**
  


Gadgets spécifiques pour ESX
----------------------------

Esx-Memory-Global
^^^^^^^^^^^^^^^^^

.. image :: /images/configuration/gadgets/Esx-Memory-Global.png 

*Utilisation*:

* Prise en charge de l'option gadget_scale: **oui**
* Prise en charge de l'option gadgets_opts: **non**

Esx-Vm-Count-Global
^^^^^^^^^^^^^^^^^^^

.. image :: /images/configuration/gadgets/Esx-Vm-Count-Global.png 

*Utilisation*:

* Prise en charge de l'option gadget_scale: **oui**
* Prise en charge de l'option gadgets_opts: **non**

Datastore-Usage-Global
^^^^^^^^^^^^^^^^^^^^^^

.. image :: /images/configuration/gadgets/Datastore-Usage-Global.png 

*Utilisation*:

* Prise en charge de l'option gadget_scale: **oui**
* Prise en charge de l'option gadgets_opts: **non**

Datastore-Latency-Global
^^^^^^^^^^^^^^^^^^^^^^^^

.. image :: /images/configuration/gadgets/Datastore-Latency-Global.png 

*Utilisation*:

* Prise en charge de l'option gadget_scale: **oui**
* Prise en charge de l'option gadgets_opts: **non**

Datastore-Iops-Global
^^^^^^^^^^^^^^^^^^^^^

.. image :: /images/configuration/gadgets/Datastore-Iops-Global.png 

*Utilisation*:

* Prise en charge de l'option gadget_scale: **oui**
* Prise en charge de l'option gadgets_opts: **non**


Gadgets spécifiques Pour PDU
----------------------------

Hardware-Pdu-Power-Usage
^^^^^^^^^^^^^^^^^^^^^^^^

.. image :: /images/configuration/gadgets/Hardware-Pdu-Power-Usage.png 

*Utilisation*:

* Prise en charge de l'option gadget_scale: **oui**
* Prise en charge de l'option gadgets_opts: **non**

Gadgets spécifiques pour Sondes Environmentales
-----------------------------------------------

Hardware-Sensors-Serverscheck-Status
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. image :: /images/configuration/gadgets/Hardware-Sensors-Serverscheck-Status-Flooding.png 
.. image :: /images/configuration/gadgets/Hardware-Sensors-Serverscheck-Status-Power.png 
.. image :: /images/configuration/gadgets/Hardware-Sensors-Serverscheck-Status-Door.png 

*Utilisation*:

* Prise en charge de l'option gadget_scale: **oui**
* Prise en charge de l'option gadgets_opts: **non**

Hardware-Sensors-Serverscheck
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. image :: /images/configuration/gadgets/Hardware-Sensors-Serverscheck-Temperature.png 
.. image :: /images/configuration/gadgets/Hardware-Sensors-Serverscheck-Humidity.png 

*Utilisation*:

* Prise en charge de l'option gadget_scale: **oui**
* Prise en charge de l'option gadgets_opts: **non**

Gadgets spécifiques pour Imprimantes
------------------------------------

printer_level
^^^^^^^^^^^^^

.. image :: /images/configuration/gadgets/printer_level.png 

*Utilisation*:

* Prise en charge de l'option gadget_scale: **non**
* Prise en charge de l'option gadgets_opts: **non**

Gadgets spécifiques pour Windows
--------------------------------

Os_Cpu
^^^^^^

.. image :: /images/configuration/gadgets/Os_Cpu.png 

*Utilisation*:

* Prise en charge de l'option gadget_scale: **oui**
* Prise en charge de l'option gadgets_opts: **non**

Os_Memory
^^^^^^^^^

.. image :: /images/configuration/gadgets/Os_Memory.png 

*Utilisation*:

* Prise en charge de l'option gadget_scale: **oui**
* Prise en charge de l'option gadgets_opts: **non**










