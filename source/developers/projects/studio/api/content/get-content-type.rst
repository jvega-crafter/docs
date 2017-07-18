.. .. include:: /includes/unicode-checkmark.rst

.. _crafter-studio-api-content-get-content-type:

================
Get Content Type
================

Get content type configuration.

--------------------
Resource Information
--------------------

+----------------------------+-------------------------------------------------------------------+
|| HTTP Verb                 || GET                                                              |
+----------------------------+-------------------------------------------------------------------+
|| URL                       || ``/api/1/services/api/1/content/get-content-type.json``          |
+----------------------------+-------------------------------------------------------------------+
|| Response Formats          || ``JSON``                                                         |
+----------------------------+-------------------------------------------------------------------+
|| Required Role             || N/A                                                              |
+----------------------------+-------------------------------------------------------------------+

----------
Parameters
----------

+---------------+-------------+---------------+--------------------------------------------------+
|| Name         || Type       || Required     || Description                                     |
+===============+=============+===============+==================================================+
|| site         || String     || |checkmark|  || Site to use                                     |
+---------------+-------------+---------------+--------------------------------------------------+
|| type         || String     || |checkmark|  || Content type                                    |
+---------------+-------------+---------------+--------------------------------------------------+

-------
Example
-------

^^^^^^^
Request
^^^^^^^

.. code-block:: guess

    GET .../api/1/services/api/1/content/get-content-type.json?site=mysite&type=/page/category-landing

^^^^^^^^
Response
^^^^^^^^

``Status 200 OK``

.. code-block:: json

    {
        "name":"/page/category-landing",
        "label":"Page - Category Landing",
        "form":"/page/category-landing",
        "formPath":"simple",
        "type":"page",
        "contentAsFolder":true,
        "useRoundedFolder":false,
        "modelInstancePath":"NOT-USED-BY-SIMPLE-FORM-ENGINE",
        "allowedRoles":[ ],
        "lastUpdated":"2017-07-07T20:08:57+02:00",
        "copyDepedencyPattern":[ ],
        "imageThumbnail":"page-category-landing.png",
        "noThumbnail":false,
        "pathIncludes":
            [
                "^/site/website/(?!articles/)(.*)"
            ],
        "pathExcludes":[ ],
        "nodeRef":null,
        "deleteDependencyPattern":[ ],
        "previewable":true
    }


---------
Responses
---------

+---------+-------------------------------------------+---------------------------------------------------+
|| Status || Location                                 || Response Body                                    |
+=========+===========================================+===================================================+
|| 200    ||                                          || See example above.                               |
+---------+-------------------------------------------+---------------------------------------------------+