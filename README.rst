pack-elasticsearch
#############

Shinken configuration pack for elasticsearch status check.

Installation
============

install via shinken.io

.. code::

	shinken install elasticsearch

usage
=====

this pack provide a host template named ``elasticsearch``. just use it in your host and add if required extra definitions.

.. code::

   _ES_HOST $HOSTADDRESS$
   _ES_PORT 9200
   _ES_EXTRA     # extra switch like --auth --username and --password
   _ES_WARNING   yellow
   _ES_CRITICAL  red


Status
======

	the status of the plugin is only related to the status of the cluster:

	health=red => critical
	health=yellow => warning
	health=green => ok.

this can be customized via _ES_WARNING and _ES_CRITICAL.



credit
======

this pack use orthecreedence's scripts to check the server.
https://github.com/orthecreedence/check_elasticsearch
