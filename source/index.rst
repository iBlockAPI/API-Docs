.. BlockChainApi-docs-en documentation master file, created by
   sphinx-quickstart on Tue Oct 22 13:49:09 2019.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Rest API
========================

- Overview
    
  The REST API allows you to query block info.

- Base URL

  All REST APIs in the documentation have the following base URL:

  .. code-block:: bash

      http(s)://host:8080/api/

- Authentication

  The HTTP requests to the REST API are protected with HTTP Basic authentication. You can create an application in Dashboard, using appid and appsecret to authenticate.  For example:

  .. code-block:: bash

      curl -v --basic -u <appsecret> -k http://localhost:8080

.. toctree::
   :maxdepth: 2

   getstarted
   bitcoin
   bitcoinabc
   cardano
   dash
   eos
   ethereum
   ethereumclassic
   libra
   litecoin
   monero
   neo
   stellar
   telegram
   tron
   zcash
   ripple