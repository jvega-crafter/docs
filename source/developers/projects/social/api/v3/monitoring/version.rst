:is-up-to-date: True

.. _crafter-social-api-monitoring-version:

===========
Get Version
===========

Returns the Crafter Social JVM version details.

--------------------
Resource Information
--------------------

.. include:: /includes/social-api-url-prefix.rst

+----------------------------+-------------------------------------------------------------------+
|| HTTP Verb                 || GET                                                              |
+----------------------------+-------------------------------------------------------------------+
|| URL                       || ``/api/3/monitoring/version``                                    |
+----------------------------+-------------------------------------------------------------------+
|| Response Formats          || ``JSON``                                                         |
+----------------------------+-------------------------------------------------------------------+

-------
Example
-------

^^^^^^^
Request
^^^^^^^

``GET .../api/3/monitoring/version.json``

^^^^^^^^
Response
^^^^^^^^

``Status 200 OK``

.. code-block:: json
  :linenos:

  {
    "packageName": "Crafter Social",
    "packageVersion": "3.1.0-SNAPSHOT",
    "packageBuild": "a68f1ff7ad84d5ecbeaa008f392e4cef0ca02f41",
    "packageBuildDate": "2019-03-07T21:03:05.422Z",
    "osName": "Mac OS X",
    "osVersion": "10.13.6",
    "osArch": "x86_64",
    "javaVersion": "1.8",
    "javaVendor": "Oracle Corporation",
    "javaVm": "Java HotSpot(TM) 64-Bit Server VM",
  }

---------
Responses
---------

+---------+--------------------------------+-----------------------------------------------------+
|| Status || Location                      || Response Body                                      |
+=========+================================+=====================================================+
|| 200    ||                               || See example above.                                 |
+---------+--------------------------------+-----------------------------------------------------+
|| 500    ||                               || ``{ "message" : "Internal server error" }``        |
+---------+--------------------------------+-----------------------------------------------------+
