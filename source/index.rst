.. BlockChainApi-docs-en documentation master file, created by
   sphinx-quickstart on Tue Oct 22 13:49:09 2019.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Rest API
========================

- Overview
    
  The REST API allows you to query block info.

Base URL
`````````````````
All REST APIs in the documentation have the following base URL:

    https://api.iblockapi.com/swagger-ui.html

Basic Authentication
``````````````````````
The HTTP requests to the REST API are protected with authentication. You can apply for APIKey in Dashboard, using apiKey to authenticate.  
For example:

.. code-block:: bash

    curl -H 'apiKey: your api Key' "https://api.iblockapi.com/btc/queryTransactionInfo?txId=6f54fcaec5553af2284da5917f52be3a82295531508886a254ff767a36ae73cd"


OR

.. code-block:: bash

    curl "https://api.iblockapi.com/btc/queryTransactionInfo?txId=6f54fcaec5553af2284da5917f52be3a82295531508886a254ff767a36ae73cd&apiKey=your api key"

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