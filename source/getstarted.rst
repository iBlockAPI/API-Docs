Get Started
===========
Intruduce infomation.

Base URL
`````````````````
All REST APIs in the documentation have the following base URL:

    https://api.iblockapi.com/

Basic Authentication
``````````````````````
The HTTP requests to the REST API are protected with authentication. You can apply for APIKey in Dashboard, using apiKey to authenticate.  
For example:

.. code-block:: bash

    curl -H 'apiKey: your api Key' "https://api.iblockapi.com/btc/queryTransactionInfo?txId=6f54fcaec5553af2284da5917f52be3a82295531508886a254ff767a36ae73cd"


OR

.. code-block:: bash

    curl "https://api.iblockapi.com/btc/queryTransactionInfo?txId=6f54fcaec5553af2284da5917f52be3a82295531508886a254ff767a36ae73cd&apiKey=your api key"