Stellar API Docs
===========
Stellar is a privacy-protecting, digital currency built on strong science. `Official website`_.

.. _Official website: https://www.stellar.org/


accountBalance
`````````````````
Returns the balance of a account.

Definition::

    GET /xlm/accountBalance?accountId=GAMI7WKVJHV3MJSMOSM4TG6L43K7TMBI4GHSMHK33RBAAAQIOM4IDZDC
    
Example Request::

    GET /xlm/accountBalance?accountId=GAMI7WKVJHV3MJSMOSM4TG6L43K7TMBI4GHSMHK33RBAAAQIOM4IDZDC

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": 35.3643691  // account balance
    }

accountInfo
`````````````````
Returns one account data.

Definition::

    GET /xlm/accountInfo?accountId=GAMI7WKVJHV3MJSMOSM4TG6L43K7TMBI4GHSMHK33RBAAAQIOM4IDZDC
    
Example Request::

    GET /xlm/accountInfo?accountId=GAMI7WKVJHV3MJSMOSM4TG6L43K7TMBI4GHSMHK33RBAAAQIOM4IDZDC

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "accountId": "GAMI7WKVJHV3MJSMOSM4TG6L43K7TMBI4GHSMHK33RBAAAQIOM4IDZDC",
            "sequenceNumber": 110266379017388030,
            "subentryCount": 0,
            "inflationDestination": null,
            "homeDomain": null,
            "lastModifiedLedger": 25690261,
            "thresholds": {
            "lowThreshold": 0,
            "medThreshold": 0,
            "highThreshold": 0
            },
            "flags": {
            "authRequired": false,
            "authRevocable": false,
            "authImmutable": false
            },
            "balances": [
            {
                "assetType": "native",
                "assetCode": null,
                "assetIssuer": null,
                "limit": null,
                "balance": "35.3643691",
                "buyingLiabilities": "0.0000000",
                "sellingLiabilities": "0.0000000",
                "lastModifiedLedger": null,
                "asset": {
                "type": "native"
                },
                "authorized": null
            }
            ],
            "data": {}
        }
    }

checkAccount
`````````````````
Returns check account is already register.

Definition::

    GET /xlm/checkAccount?accountId=GAMI7WKVJHV3MJSMOSM4TG6L43K7TMBI4GHSMHK33RBAAAQIOM4IDZDC
    
Example Request::

    GET /xlm/checkAccount?accountId=GAMI7WKVJHV3MJSMOSM4TG6L43K7TMBI4GHSMHK33RBAAAQIOM4IDZDC

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": true  // account is already register
    }

getTransaction
`````````````````
Returns transaction data.

Definition::

    GET /xlm/getTransaction?txId=3f9435d4a2280f4c10a8dfa014f8e1dd33387b52dfd100e43d20705eae1b3089
    
Example Request::

    GET /xlm/getTransaction?txId=3f9435d4a2280f4c10a8dfa014f8e1dd33387b52dfd100e43d20705eae1b3089

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": {
            "rateLimitLimit": 0,
            "rateLimitRemaining": 0,
            "rateLimitReset": 0,
            "id": 110335923127869440,
            "sourceAccount": "GBFG33MU4ZN3AFC52N5IL62VG2IEJDCGCELYBC3M2LH3QOH26UT4WQVD",
            "pagingToken": "110335923127869441",
            "createdAt": "2019-09-06T07:26:47Z",
            "transactionHash": "3f9435d4a2280f4c10a8dfa014f8e1dd33387b52dfd100e43d20705eae1b3089",
            "transactionSuccessful": true,
            "type": "payment",
            "amount": "20.4262877",
            "assetType": "native",
            "assetCode": null,
            "assetIssuer": null,
            "from": "GBFG33MU4ZN3AFC52N5IL62VG2IEJDCGCELYBC3M2LH3QOH26UT4WQVD",
            "to": "GBSHHLDIKLZ3I652S5KNZM2SUOK7DKQY3OK4IZEFZMOD2WJQ2L74BM2N",
            "asset": {
            "type": "native"
            }
        }
    }

getAccountTransactions
`````````````````
Returns account transactions.

Definition::

    GET /xlm/getAccountTransactions?accountId=GBSHHLDIKLZ3I652S5KNZM2SUOK7DKQY3OK4IZEFZMOD2WJQ2L74BM2N&cursor=110335923127869441&limit=10
    
Example Request::

    GET /xlm/getAccountTransactions?accountId=GBSHHLDIKLZ3I652S5KNZM2SUOK7DKQY3OK4IZEFZMOD2WJQ2L74BM2N&cursor=110335923127869441&limit=10

Response:

.. code-block:: json

    {
        "status": 0,
        "message": "success",
        "data": [
            {
            "hash": "1c1e51c342fdc9a92889edb49313f062e5d83c630129c3e9a431cefc13682e12",
            "ledger": 25689658,
            "createdAt": "2019-09-06T07:33:27Z",
            "sourceAccount": "GBFG33MU4ZN3AFC52N5IL62VG2IEJDCGCELYBC3M2LH3QOH26UT4WQVD",
            "successful": null,
            "pagingToken": "110336240955473920",
            "sourceAccountSequence": 110323781255299070,
            "feePaid": 100,
            "operationCount": 1,
            "envelopeXdr": "AAAAAEpt7ZTmW7AUXdN6hftVNpBEjEYRF4CLbNLPuDj69SfLAAAAZAGH8uUAAAAEAAAAAAAAAAEAAAAOMTkwOTA2MDAwMDc5ODUAAAAAAAEAAAAAAAAAAQAAAABkc6xoUvO0e7qXVNyzUqOV8aoY25XEZIXLHD1ZMNL/wAAAAAAAAAAAdzWUAAAAAAAAAAAB+vUnywAAAEBPg68dFsOzDLPRjdS9G2bwV2wVOqBcau4S0KFSZVcNfyBC4QpIwOP/mkJM9HI058OSBhAR2MtO29GoXt300yQF",
            "resultXdr": "AAAAAAAAAGQAAAAAAAAAAQAAAAAAAAABAAAAAAAAAAA=",
            "resultMetaXdr": "AAAAAQAAAAIAAAADAYf+OgAAAAAAAAAASm3tlOZbsBRd03qF+1U2kESMRhEXgIts0s+4OPr1J8sAAAAAje2GagGH8uUAAAADAAAAAAAAAAAAAAAAAAAAAAEAAAAAAAAAAAAAAAAAAAAAAAABAYf+OgAAAAAAAAAASm3tlOZbsBRd03qF+1U2kESMRhEXgIts0s+4OPr1J8sAAAAAje2GagGH8uUAAAAEAAAAAAAAAAAAAAAAAAAAAAEAAAAAAAAAAAAAAAAAAAAAAAABAAAABAAAAAMBh/3wAAAAAAAAAABkc6xoUvO0e7qXVNyzUqOV8aoY25XEZIXLHD1ZMNL/wAAAAAAhv6xLAYe9RgAAABMAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAEBh/46AAAAAAAAAABkc6xoUvO0e7qXVNyzUqOV8aoY25XEZIXLHD1ZMNL/wAAAAACY9UBLAYe9RgAAABMAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAMBh/46AAAAAAAAAABKbe2U5luwFF3TeoX7VTaQRIxGEReAi2zSz7g4+vUnywAAAACN7YZqAYfy5QAAAAQAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAEBh/46AAAAAAAAAABKbe2U5luwFF3TeoX7VTaQRIxGEReAi2zSz7g4+vUnywAAAAAWt/JqAYfy5QAAAAQAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAA==",
            "memoStr": "19090600007985"
            },
            {
            "hash": "7cf437856090d7d42a2a1b74e0f3984059ac23bd84ec8fb7398ae5701ce11cab",
            "ledger": 25689680,
            "createdAt": "2019-09-06T07:35:30Z",
            "sourceAccount": "GBSHHLDIKLZ3I652S5KNZM2SUOK7DKQY3OK4IZEFZMOD2WJQ2L74BM2N",
            "successful": null,
            "pagingToken": "110336335444742144",
            "sourceAccountSequence": 110264824239226900,
            "feePaid": 100,
            "operationCount": 1,
            "envelopeXdr": "AAAAAGRzrGhS87R7updU3LNSo5XxqhjblcRkhcscPVkw0v/AAAAAZAGHvUYAAAAVAAAAAQAAAAAAAAAAAAAAAF1yDPUAAAABAAAACjEwMDcyNzU0MjEAAAAAAAEAAAAAAAAAAQAAAAAOr5CG1ax6qG2fBEgXJlF0sw5W0irOS6N/NRDbavBm4QAAAAAAAAAAl/3pgAAAAAAAAAABMNL/wAAAAEAabm2jLR0n6NLUPogKF8Yvqnr2OI/CoUf2WdCT+B03h8HeNX8IdmStaXAwItffzzBYndydUvqkvPOPxd9TxbMB",
            "resultXdr": "AAAAAAAAAGQAAAAAAAAAAQAAAAAAAAABAAAAAAAAAAA=",
            "resultMetaXdr": "AAAAAQAAAAIAAAADAYf+UAAAAAAAAAAAZHOsaFLztHu6l1Tcs1KjlfGqGNuVxGSFyxw9WTDS/8AAAAAAmPU/gwGHvUYAAAAUAAAAAAAAAAAAAAAAAAAAAAEAAAAAAAAAAAAAAAAAAAAAAAABAYf+UAAAAAAAAAAAZHOsaFLztHu6l1Tcs1KjlfGqGNuVxGSFyxw9WTDS/8AAAAAAmPU/gwGHvUYAAAAVAAAAAAAAAAAAAAAAAAAAAAEAAAAAAAAAAAAAAAAAAAAAAAABAAAABAAAAAMBh/5GAAAAAAAAAAAOr5CG1ax6qG2fBEgXJlF0sw5W0irOS6N/NRDbavBm4QAAALG/wcD3AOOFugAAatwAAAAAAAAAAQAAAACdpD9sS2jlS4+g0cF9ZjMgNJrm2J2L7tIPDnaA6sV7hQAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAEBh/5QAAAAAAAAAAAOr5CG1ax6qG2fBEgXJlF0sw5W0irOS6N/NRDbavBm4QAAALJXv6p3AOOFugAAatwAAAAAAAAAAQAAAACdpD9sS2jlS4+g0cF9ZjMgNJrm2J2L7tIPDnaA6sV7hQAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAMBh/5QAAAAAAAAAABkc6xoUvO0e7qXVNyzUqOV8aoY25XEZIXLHD1ZMNL/wAAAAACY9T+DAYe9RgAAABUAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAEBh/5QAAAAAAAAAABkc6xoUvO0e7qXVNyzUqOV8aoY25XEZIXLHD1ZMNL/wAAAAAAA91YDAYe9RgAAABUAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAA==",
            "memoStr": "1007275421"
            },
            {
            "hash": "2011e0ed77a61245cb2798850a2efe7a31dcb5f166ca5287234a5fced4797028",
            "ledger": 25689738,
            "createdAt": "2019-09-06T07:40:46Z",
            "sourceAccount": "GBFG33MU4ZN3AFC52N5IL62VG2IEJDCGCELYBC3M2LH3QOH26UT4WQVD",
            "successful": null,
            "pagingToken": "110336584552824832",
            "sourceAccountSequence": 110323781255299070,
            "feePaid": 100,
            "operationCount": 1,
            "envelopeXdr": "AAAAAEpt7ZTmW7AUXdN6hftVNpBEjEYRF4CLbNLPuDj69SfLAAAAZAGH8uUAAAAFAAAAAAAAAAEAAAAOMTkwOTA2MDAwMDgwMzkAAAAAAAEAAAAAAAAAAQAAAABkc6xoUvO0e7qXVNyzUqOV8aoY25XEZIXLHD1ZMNL/wAAAAAAAAAAAFEP9AAAAAAAAAAAB+vUnywAAAECtgSC4E2wGq3is+f5Zf8B2C1Q8o/4vY9TuzeG7yXm5XpkJQZ6jsT2WVdUWamb9XSqoXA42POiEpguMJRz13hwL",
            "resultXdr": "AAAAAAAAAGQAAAAAAAAAAQAAAAAAAAABAAAAAAAAAAA=",
            "resultMetaXdr": "AAAAAQAAAAIAAAADAYf+igAAAAAAAAAASm3tlOZbsBRd03qF+1U2kESMRhEXgIts0s+4OPr1J8sAAAAAFrfyBgGH8uUAAAAEAAAAAAAAAAAAAAAAAAAAAAEAAAAAAAAAAAAAAAAAAAAAAAABAYf+igAAAAAAAAAASm3tlOZbsBRd03qF+1U2kESMRhEXgIts0s+4OPr1J8sAAAAAFrfyBgGH8uUAAAAFAAAAAAAAAAAAAAAAAAAAAAEAAAAAAAAAAAAAAAAAAAAAAAABAAAABAAAAAMBh/5QAAAAAAAAAABkc6xoUvO0e7qXVNyzUqOV8aoY25XEZIXLHD1ZMNL/wAAAAAAA91YDAYe9RgAAABUAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAEBh/6KAAAAAAAAAABkc6xoUvO0e7qXVNyzUqOV8aoY25XEZIXLHD1ZMNL/wAAAAAAVO1MDAYe9RgAAABUAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAMBh/6KAAAAAAAAAABKbe2U5luwFF3TeoX7VTaQRIxGEReAi2zSz7g4+vUnywAAAAAWt/IGAYfy5QAAAAUAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAEBh/6KAAAAAAAAAABKbe2U5luwFF3TeoX7VTaQRIxGEReAi2zSz7g4+vUnywAAAAACc/UGAYfy5QAAAAUAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAA==",
            "memoStr": "19090600008039"
            },
            {
            "hash": "aabdd16d455dbe0ddcb4985d5272ff46e7c2f16b65ffb88905a218b51783661e",
            "ledger": 25690261,
            "createdAt": "2019-09-06T08:28:15Z",
            "sourceAccount": "GAMI7WKVJHV3MJSMOSM4TG6L43K7TMBI4GHSMHK33RBAAAQIOM4IDZDC",
            "successful": null,
            "pagingToken": "110338830820737024",
            "sourceAccountSequence": 110266379017388030,
            "feePaid": 100,
            "operationCount": 1,
            "envelopeXdr": "AAAAABiP2VVJ67YmTHSZyZvL5tX5sCjhjyYdW9xCAAIIcziBAAAAZAGHvrAAAAAFAAAAAAAAAAEAAAAOMTkwOTA2MDAwMDk1NjYAAAAAAAEAAAAAAAAAAQAAAABkc6xoUvO0e7qXVNyzUqOV8aoY25XEZIXLHD1ZMNL/wAAAAAAAAAAAdpz9gAAAAAAAAAABCHM4gQAAAECANgtGnfb8gcYJUJEC/I7ht9bRPuERIKu4bmqaMzAlRo/C8MCCu2HUa0R+FZ3LIHMxp9/DoRDobV0510I2Wh0M",
            "resultXdr": "AAAAAAAAAGQAAAAAAAAAAQAAAAAAAAABAAAAAAAAAAA=",
            "resultMetaXdr": "AAAAAQAAAAIAAAADAYgAlQAAAAAAAAAAGI/ZVUnrtiZMdJnJm8vm1fmwKOGPJh1b3EIAAghzOIEAAAAAi7EqKwGHvrAAAAAEAAAAAAAAAAAAAAAAAAAAAAEAAAAAAAAAAAAAAAAAAAAAAAABAYgAlQAAAAAAAAAAGI/ZVUnrtiZMdJnJm8vm1fmwKOGPJh1b3EIAAghzOIEAAAAAi7EqKwGHvrAAAAAFAAAAAAAAAAAAAAAAAAAAAAEAAAAAAAAAAAAAAAAAAAAAAAABAAAABAAAAAMBh/6KAAAAAAAAAABkc6xoUvO0e7qXVNyzUqOV8aoY25XEZIXLHD1ZMNL/wAAAAAAVO1MDAYe9RgAAABUAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAEBiACVAAAAAAAAAABkc6xoUvO0e7qXVNyzUqOV8aoY25XEZIXLHD1ZMNL/wAAAAACL2FCDAYe9RgAAABUAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAMBiACVAAAAAAAAAAAYj9lVSeu2Jkx0mcmby+bV+bAo4Y8mHVvcQgACCHM4gQAAAACLsSorAYe+sAAAAAUAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAEBiACVAAAAAAAAAAAYj9lVSeu2Jkx0mcmby+bV+bAo4Y8mHVvcQgACCHM4gQAAAAAVFCyrAYe+sAAAAAUAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAA==",
            "memoStr": "19090600009566"
            },
            {
            "hash": "6947ae7947db11862606efe3cf94a8bffecb0887a4a07282ad123d079cf917da",
            "ledger": 25690357,
            "createdAt": "2019-09-06T08:36:55Z",
            "sourceAccount": "GCO2IP3MJNUOKS4PUDI4C7LGGMQDJGXG3COYX3WSB4HHNAHKYV5YL3VC",
            "successful": null,
            "pagingToken": "110339243137613824",
            "sourceAccountSequence": 64034663849112160,
            "feePaid": 100,
            "operationCount": 1,
            "envelopeXdr": "AAAAAJ2kP2xLaOVLj6DRwX1mMyA0mubYnYvu0g8OdoDqxXuFAAAAZADjfzAACbJfAAAAAQAAAAAAAAAAAAAAAF1yGq0AAAABAAAAAAAAAAEAAAAAAAAAAQAAAABkc6xoUvO0e7qXVNyzUqOV8aoY25XEZIXLHD1ZMNL/wAAAAAAAAAAAI8G/YAAAAAAAAAAB6sV7hQAAAECLiJ0WdhQauZGWUeeDxO3erVnl7Dg3u0zkx9kD1j/pZej6HfR4+0l62Hu2BAoaEgF2wElta5nhwvYPDosHHwAI",
            "resultXdr": "AAAAAAAAAGQAAAAAAAAAAQAAAAAAAAABAAAAAAAAAAA=",
            "resultMetaXdr": "AAAAAQAAAAIAAAADAYgA9QAAAAAAAAAAnaQ/bEto5UuPoNHBfWYzIDSa5tidi+7SDw52gOrFe4UAAKs/Lq/e2ADjfzAACbJeAAAAAAAAAAEAAAAAnaQ/bEto5UuPoNHBfWYzIDSa5tidi+7SDw52gOrFe4UAAAAAAAAAAAEAAAAAAAAAAAAAAAAAAAAAAAABAYgA9QAAAAAAAAAAnaQ/bEto5UuPoNHBfWYzIDSa5tidi+7SDw52gOrFe4UAAKs/Lq/e2ADjfzAACbJfAAAAAAAAAAEAAAAAnaQ/bEto5UuPoNHBfWYzIDSa5tidi+7SDw52gOrFe4UAAAAAAAAAAAEAAAAAAAAAAAAAAAAAAAAAAAABAAAABAAAAAMBiACVAAAAAAAAAABkc6xoUvO0e7qXVNyzUqOV8aoY25XEZIXLHD1ZMNL/wAAAAACL2FCDAYe9RgAAABUAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAEBiAD1AAAAAAAAAABkc6xoUvO0e7qXVNyzUqOV8aoY25XEZIXLHD1ZMNL/wAAAAACvmg/jAYe9RgAAABUAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAMBiAD1AAAAAAAAAACdpD9sS2jlS4+g0cF9ZjMgNJrm2J2L7tIPDnaA6sV7hQAAqz8ur97YAON/MAAJsl8AAAAAAAAAAQAAAACdpD9sS2jlS4+g0cF9ZjMgNJrm2J2L7tIPDnaA6sV7hQAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAEBiAD1AAAAAAAAAACdpD9sS2jlS4+g0cF9ZjMgNJrm2J2L7tIPDnaA6sV7hQAAqz8K7h94AON/MAAJsl8AAAAAAAAAAQAAAACdpD9sS2jlS4+g0cF9ZjMgNJrm2J2L7tIPDnaA6sV7hQAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAA==",
            "memoStr": ""
            },
            {
            "hash": "a33b85bcb0e57805ba071abdf4d37c5056c574ed3b28c81ab3b8fd8efeb2f71e",
            "ledger": 25690369,
            "createdAt": "2019-09-06T08:37:59Z",
            "sourceAccount": "GBSHHLDIKLZ3I652S5KNZM2SUOK7DKQY3OK4IZEFZMOD2WJQ2L74BM2N",
            "successful": null,
            "pagingToken": "110339294677217280",
            "sourceAccountSequence": 110264824239226900,
            "feePaid": 100,
            "operationCount": 1,
            "envelopeXdr": "AAAAAGRzrGhS87R7updU3LNSo5XxqhjblcRkhcscPVkw0v/AAAAAZAGHvUYAAAAWAAAAAQAAAAAAAAAAAAAAAF1yG5cAAAAAAAAAAQAAAAAAAAABAAAAAEpt7ZTmW7AUXdN6hftVNpBEjEYRF4CLbNLPuDj69SfLAAAAAAAAAACqCnq/AAAAAAAAAAEw0v/AAAAAQG4J++Bvcc4M3+CDC3Y68xImqTQapCMIOo3v3Nn2H+dsRGRb4FvV3jZlmNZRwRlFbUYwNIVmZ9yDocyIpSFsVQk=",
            "resultXdr": "AAAAAAAAAGQAAAAAAAAAAQAAAAAAAAABAAAAAAAAAAA=",
            "resultMetaXdr": "AAAAAQAAAAIAAAADAYgBAQAAAAAAAAAAZHOsaFLztHu6l1Tcs1KjlfGqGNuVxGSFyxw9WTDS/8AAAAAAr5oPfwGHvUYAAAAVAAAAAAAAAAAAAAAAAAAAAAEAAAAAAAAAAAAAAAAAAAAAAAABAYgBAQAAAAAAAAAAZHOsaFLztHu6l1Tcs1KjlfGqGNuVxGSFyxw9WTDS/8AAAAAAr5oPfwGHvUYAAAAWAAAAAAAAAAAAAAAAAAAAAAEAAAAAAAAAAAAAAAAAAAAAAAABAAAABAAAAAMBh/6KAAAAAAAAAABKbe2U5luwFF3TeoX7VTaQRIxGEReAi2zSz7g4+vUnywAAAAACc/UGAYfy5QAAAAUAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAEBiAEBAAAAAAAAAABKbe2U5luwFF3TeoX7VTaQRIxGEReAi2zSz7g4+vUnywAAAACsfm/FAYfy5QAAAAUAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAMBiAEBAAAAAAAAAABkc6xoUvO0e7qXVNyzUqOV8aoY25XEZIXLHD1ZMNL/wAAAAACvmg9/AYe9RgAAABYAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAEBiAEBAAAAAAAAAABkc6xoUvO0e7qXVNyzUqOV8aoY25XEZIXLHD1ZMNL/wAAAAAAFj5TAAYe9RgAAABYAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAA==",
            "memoStr": ""
            },
            {
            "hash": "be0f79fafc6be369bd505274bd639ed706f60b9770a6673dafa41f0a441c9225",
            "ledger": 25690505,
            "createdAt": "2019-09-06T08:50:13Z",
            "sourceAccount": "GBFG33MU4ZN3AFC52N5IL62VG2IEJDCGCELYBC3M2LH3QOH26UT4WQVD",
            "successful": null,
            "pagingToken": "110339878792744960",
            "sourceAccountSequence": 110323781255299070,
            "feePaid": 100,
            "operationCount": 1,
            "envelopeXdr": "AAAAAEpt7ZTmW7AUXdN6hftVNpBEjEYRF4CLbNLPuDj69SfLAAAAZAGH8uUAAAAGAAAAAAAAAAEAAAAOMTkwOTA2MDAwMTAxNTUAAAAAAAEAAAAAAAAAAQAAAABkc6xoUvO0e7qXVNyzUqOV8aoY25XEZIXLHD1ZMNL/wAAAAAAAAAAAq9cWwAAAAAAAAAAB+vUnywAAAEAyGMFqVULgbbHhl6yM+ijCHvE8hPyLvlMuoqQ3AYgpF2ttlaKIvIP2ggAa+JCoWGDACzwzc7ErzmNpPORr1tsD",
            "resultXdr": "AAAAAAAAAGQAAAAAAAAAAQAAAAAAAAABAAAAAAAAAAA=",
            "resultMetaXdr": "AAAAAQAAAAIAAAADAYgBiQAAAAAAAAAASm3tlOZbsBRd03qF+1U2kESMRhEXgIts0s+4OPr1J8sAAAAArH5vYQGH8uUAAAAFAAAAAAAAAAAAAAAAAAAAAAEAAAAAAAAAAAAAAAAAAAAAAAABAYgBiQAAAAAAAAAASm3tlOZbsBRd03qF+1U2kESMRhEXgIts0s+4OPr1J8sAAAAArH5vYQGH8uUAAAAGAAAAAAAAAAAAAAAAAAAAAAEAAAAAAAAAAAAAAAAAAAAAAAABAAAABAAAAAMBiAEBAAAAAAAAAABkc6xoUvO0e7qXVNyzUqOV8aoY25XEZIXLHD1ZMNL/wAAAAAAFj5TAAYe9RgAAABYAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAEBiAGJAAAAAAAAAABkc6xoUvO0e7qXVNyzUqOV8aoY25XEZIXLHD1ZMNL/wAAAAACxZquAAYe9RgAAABYAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAMBiAGJAAAAAAAAAABKbe2U5luwFF3TeoX7VTaQRIxGEReAi2zSz7g4+vUnywAAAACsfm9hAYfy5QAAAAYAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAEBiAGJAAAAAAAAAABKbe2U5luwFF3TeoX7VTaQRIxGEReAi2zSz7g4+vUnywAAAAAAp1ihAYfy5QAAAAYAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAA==",
            "memoStr": "19090600010155"
            },
            {
            "hash": "3473a1f976e64aeb48b3150765458a4960ff49799ccc1661611b53f3c457c72a",
            "ledger": 25690530,
            "createdAt": "2019-09-06T08:52:27Z",
            "sourceAccount": "GBSHHLDIKLZ3I652S5KNZM2SUOK7DKQY3OK4IZEFZMOD2WJQ2L74BM2N",
            "successful": null,
            "pagingToken": "110339986166919168",
            "sourceAccountSequence": 110264824239226900,
            "feePaid": 100,
            "operationCount": 1,
            "envelopeXdr": "AAAAAGRzrGhS87R7updU3LNSo5XxqhjblcRkhcscPVkw0v/AAAAAZAGHvUYAAAAXAAAAAQAAAAAAAAAAAAAAAF1yHv4AAAAAAAAAAQAAAAAAAAABAAAAAEpt7ZTmW7AUXdN6hftVNpBEjEYRF4CLbNLPuDj69SfLAAAAAAAAAAB0+wUaAAAAAAAAAAEw0v/AAAAAQMeJXVSclBGqh9H8wEfXB7G95+IuiMt70mp/nYVek+B2/bHIizkJ/CMX8Ojfj5CsIdda6Hkxs8tEyAXIzTerywc=",
            "resultXdr": "AAAAAAAAAGQAAAAAAAAAAQAAAAAAAAABAAAAAAAAAAA=",
            "resultMetaXdr": "AAAAAQAAAAIAAAADAYgBogAAAAAAAAAAZHOsaFLztHu6l1Tcs1KjlfGqGNuVxGSFyxw9WTDS/8AAAAAAsWarHAGHvUYAAAAWAAAAAAAAAAAAAAAAAAAAAAEAAAAAAAAAAAAAAAAAAAAAAAABAYgBogAAAAAAAAAAZHOsaFLztHu6l1Tcs1KjlfGqGNuVxGSFyxw9WTDS/8AAAAAAsWarHAGHvUYAAAAXAAAAAAAAAAAAAAAAAAAAAAEAAAAAAAAAAAAAAAAAAAAAAAABAAAABAAAAAMBiAGJAAAAAAAAAABKbe2U5luwFF3TeoX7VTaQRIxGEReAi2zSz7g4+vUnywAAAAAAp1ihAYfy5QAAAAYAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAEBiAGiAAAAAAAAAABKbe2U5luwFF3TeoX7VTaQRIxGEReAi2zSz7g4+vUnywAAAAB1ol27AYfy5QAAAAYAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAMBiAGiAAAAAAAAAABkc6xoUvO0e7qXVNyzUqOV8aoY25XEZIXLHD1ZMNL/wAAAAACxZqscAYe9RgAAABcAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAEBiAGiAAAAAAAAAABkc6xoUvO0e7qXVNyzUqOV8aoY25XEZIXLHD1ZMNL/wAAAAAA8a6YCAYe9RgAAABcAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAA==",
            "memoStr": ""
            },
            {
            "hash": "347a8733c1b02c745ebe189221c86bdcc6ca24a9d9e00414674ef43f7884a5f6",
            "ledger": 25690537,
            "createdAt": "2019-09-06T08:53:07Z",
            "sourceAccount": "GBSHHLDIKLZ3I652S5KNZM2SUOK7DKQY3OK4IZEFZMOD2WJQ2L74BM2N",
            "successful": null,
            "pagingToken": "110340016231788544",
            "sourceAccountSequence": 110264824239226910,
            "feePaid": 100,
            "operationCount": 1,
            "envelopeXdr": "AAAAAGRzrGhS87R7updU3LNSo5XxqhjblcRkhcscPVkw0v/AAAAAZAGHvUYAAAAYAAAAAQAAAAAAAAAAAAAAAF1yHyQAAAABAAAACjEwMDcyNzU0MjEAAAAAAAEAAAAAAAAAAQAAAAAOr5CG1ax6qG2fBEgXJlF0sw5W0irOS6N/NRDbavBm4QAAAAAAAAAAO5rKAAAAAAAAAAABMNL/wAAAAED/jaTrpo/Mjvlb5rtPE9oIC1SICpkP3HWFyw8pCL5JvkIAqZNyydiYGqf+WkgpiPPSZcJITIxiXU6RizLJOGgD",
            "resultXdr": "AAAAAAAAAGQAAAAAAAAAAQAAAAAAAAABAAAAAAAAAAA=",
            "resultMetaXdr": "AAAAAQAAAAIAAAADAYgBqQAAAAAAAAAAZHOsaFLztHu6l1Tcs1KjlfGqGNuVxGSFyxw9WTDS/8AAAAAAPGulngGHvUYAAAAXAAAAAAAAAAAAAAAAAAAAAAEAAAAAAAAAAAAAAAAAAAAAAAABAYgBqQAAAAAAAAAAZHOsaFLztHu6l1Tcs1KjlfGqGNuVxGSFyxw9WTDS/8AAAAAAPGulngGHvUYAAAAYAAAAAAAAAAAAAAAAAAAAAAEAAAAAAAAAAAAAAAAAAAAAAAABAAAABAAAAAMBiAGFAAAAAAAAAAAOr5CG1ax6qG2fBEgXJlF0sw5W0irOS6N/NRDbavBm4QAAADZBUq0jAOOFugAAat8AAAAAAAAAAQAAAACdpD9sS2jlS4+g0cF9ZjMgNJrm2J2L7tIPDnaA6sV7hQAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAEBiAGpAAAAAAAAAAAOr5CG1ax6qG2fBEgXJlF0sw5W0irOS6N/NRDbavBm4QAAADZ87XcjAOOFugAAat8AAAAAAAAAAQAAAACdpD9sS2jlS4+g0cF9ZjMgNJrm2J2L7tIPDnaA6sV7hQAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAMBiAGpAAAAAAAAAABkc6xoUvO0e7qXVNyzUqOV8aoY25XEZIXLHD1ZMNL/wAAAAAA8a6WeAYe9RgAAABgAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAEBiAGpAAAAAAAAAABkc6xoUvO0e7qXVNyzUqOV8aoY25XEZIXLHD1ZMNL/wAAAAAAA0NueAYe9RgAAABgAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAA==",
            "memoStr": "1007275421"
            },
            {
            "hash": "f474f1bccb52b93b0d1baaa8158fe49782a96b8c3c0d45165b8c70c975d5b7fe",
            "ledger": 25690754,
            "createdAt": "2019-09-06T09:12:37Z",
            "sourceAccount": "GCO2IP3MJNUOKS4PUDI4C7LGGMQDJGXG3COYX3WSB4HHNAHKYV5YL3VC",
            "successful": null,
            "pagingToken": "110340948239597568",
            "sourceAccountSequence": 64034663849112170,
            "feePaid": 100,
            "operationCount": 1,
            "envelopeXdr": "AAAAAJ2kP2xLaOVLj6DRwX1mMyA0mubYnYvu0g8OdoDqxXuFAAAAZADjfzAACbJrAAAAAQAAAAAAAAAAAAAAAF1yIwoAAAABAAAAAAAAAAEAAAAAAAAAAQAAAABkc6xoUvO0e7qXVNyzUqOV8aoY25XEZIXLHD1ZMNL/wAAAAAAAAAAAwk4gYAAAAAAAAAAB6sV7hQAAAEDvmqTIVzG64QItN6OLlabdzfoNZkPmJbYDwS4hmJrpwojp8kpmYrP7MqP5Z8HioVBk7dnTpDsu54RhDiWfjawH",
            "resultXdr": "AAAAAAAAAGQAAAAAAAAAAQAAAAAAAAABAAAAAAAAAAA=",
            "resultMetaXdr": "AAAAAQAAAAIAAAADAYgCggAAAAAAAAAAnaQ/bEto5UuPoNHBfWYzIDSa5tidi+7SDw52gOrFe4UAAKp/GZQl9gDjfzAACbJqAAAAAAAAAAEAAAAAnaQ/bEto5UuPoNHBfWYzIDSa5tidi+7SDw52gOrFe4UAAAAAAAAAAAEAAAAAAAAAAAAAAAAAAAAAAAABAYgCggAAAAAAAAAAnaQ/bEto5UuPoNHBfWYzIDSa5tidi+7SDw52gOrFe4UAAKp/GZQl9gDjfzAACbJrAAAAAAAAAAEAAAAAnaQ/bEto5UuPoNHBfWYzIDSa5tidi+7SDw52gOrFe4UAAAAAAAAAAAEAAAAAAAAAAAAAAAAAAAAAAAABAAAABAAAAAMBiAGpAAAAAAAAAABkc6xoUvO0e7qXVNyzUqOV8aoY25XEZIXLHD1ZMNL/wAAAAAAA0NueAYe9RgAAABgAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAEBiAKCAAAAAAAAAABkc6xoUvO0e7qXVNyzUqOV8aoY25XEZIXLHD1ZMNL/wAAAAADDHvv+AYe9RgAAABgAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAMBiAKCAAAAAAAAAACdpD9sS2jlS4+g0cF9ZjMgNJrm2J2L7tIPDnaA6sV7hQAAqn8ZlCX2AON/MAAJsmsAAAAAAAAAAQAAAACdpD9sS2jlS4+g0cF9ZjMgNJrm2J2L7tIPDnaA6sV7hQAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAEBiAKCAAAAAAAAAACdpD9sS2jlS4+g0cF9ZjMgNJrm2J2L7tIPDnaA6sV7hQAAqn5XRgWWAON/MAAJsmsAAAAAAAAAAQAAAACdpD9sS2jlS4+g0cF9ZjMgNJrm2J2L7tIPDnaA6sV7hQAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAA==",
            "memoStr": ""
            }
        ]
    }

