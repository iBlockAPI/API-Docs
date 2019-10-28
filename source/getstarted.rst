Get Started
===========
Intruduce infomation.

Base URL
`````````````````
All REST APIs in the documentation have the following base URL:

    http(s)://host:8080/api/

Basic Authentication
``````````````````````
The HTTP requests to the REST API are protected with HTTP Basic authentication. You can create an application in Dashboard, using appid and appsecret to authenticate.  For example:

.. code-block:: bash

    curl -v --basic -u <appsecret> -k http://localhost:8080