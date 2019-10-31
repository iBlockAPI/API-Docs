Monero API Docs
===========
getBlockCount
```````````
Look up how many blocks are in the longest chain known to the node

Definition::

    GET /xmr/getBlockCount/

Example Request::

    GET /xmr/getBlockCount/

Response:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": {
        "result": {
        "count": 1951488,
        "status": "OK"
        },
        "id": "1571896281490",
        "jsonrpc": "2.0"
    }
 }

onGetblockhash
```````````
Look up a block's hash by its height

Definition::

    GET /xmr/onGetblockhash?blockHeight={blockHeight}

Example Request::

    GET /xmr/onGetblockhash?blockHeight=912345

Response:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": {
        "result": "a18075437c250ce4dd3999bbfbf63a1863f422056df1733786fcc48816133fe5",
        "id": "1571900453426",
        "jsonrpc": "2.0"
    }
 }


getLastBlockHeader
```````````
Block header information for the most recent block is easily retrieved with this method

Definition::

    GET /xmr/getLastBlockHeader/

Example Request::

    GET /xmr/getLastBlockHeader/

Response:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": {
        "result": {
        "block_header": {
            "block_weight": 45702,
            "num_txes": 17,
            "reward": 2244010531416,
            "wide_difficulty": "0x9480c8821",
            "pow_hash": "",
            "cumulative_difficulty_top64": 0,
            "prev_hash": "c9caf49838a0dcc275c5a17dcff4bda46d5d248c89ff7819b58af553a3fa03a1",
            "cumulative_difficulty": 34052350008858796,
            "wide_cumulative_difficulty": "0x78fa6e920b98ab",
            "nonce": 3489661100,
            "minor_version": 11,
            "difficulty": 39863486497,
            "depth": 0,
            "major_version": 11,
            "orphan_status": false,
            "difficulty_top64": 0,
            "miner_tx_hash": "4a26ce549c063bd2d3d6337652a201685848b7fc931792e02434844c47d43c8d",
            "long_term_weight": 45702,
            "block_size": 45702,
            "hash": "9383c087dc644eed46a343c72867a020ed6ebf29f76d08b6735ce143e403a4d1",
            "height": 1951494,
            "timestamp": 1571896656
        },
        "untrusted": false,
        "status": "OK"
        },
        "id": "1571897056680",
        "jsonrpc": "2.0"
    }
 }


Return:

.. code-block:: json

 {
    block_header - A structure containing block header information.
        block_size - unsigned int; The block size in bytes.
        depth - unsigned int; The number of blocks succeeding this block on the blockchain. A larger number means an older block.
        difficulty - unsigned int; The strength of the Monero network based on mining power.
        hash - string; The hash of this block.
        height - unsigned int; The number of blocks preceding this block on the blockchain.
        major_version - unsigned int; The major version of the monero protocol at this block height.
        minor_version - unsigned int; The minor version of the monero protocol at this block height.
        nonce - unsigned int; a cryptographic random one-time number used in mining a Monero block.
        num_txes - unsigned int; Number of transactions in the block, not counting the coinbase tx.
        orphan_status - boolean; Usually false. If true, this block is not part of the longest chain.
        prev_hash - string; The hash of the block immediately preceding this block in the chain.
        reward - unsigned int; The amount of new atomic units generated in this block and rewarded to the miner. Note: 1 XMR = 1e12 atomic units.
        timestamp - unsigned int; The unix time at which the block was recorded into the blockchain.
    status - string; General RPC error code. "OK" means everything looks good.
    untrusted - boolean; States if the result is obtained using the bootstrap mode, and is therefore not trusted (true), or when the daemon is fully synced (false).
 }



getBlockHeaderByHash
```````````
Block header information can be retrieved using either a block's hash or height. 
This method includes a block's hash as an input parameter to retrieve basic information about the block


Definition::

    GET /xmr/getBlockHeaderByHash?hash={hash}

Example Request::

    GET /xmr/getBlockHeaderByHash?hash=e22cf75f39ae720e8b71b3d120a5ac03f0db50bba6379e2850975b4859190bc6

Response:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": {
        "result": {
        "block_header": {
            "block_weight": 210,
            "num_txes": 0,
            "reward": 7388968946286,
            "wide_difficulty": "0x309d758b",
            "pow_hash": "",
            "cumulative_difficulty_top64": 0,
            "prev_hash": "b61c58b2e0be53fad5ef9d9731a55e8a81d972b8d90ed07c04fd37ca6403ff78",
            "cumulative_difficulty": 754734824984346,
            "wide_cumulative_difficulty": "0x2ae6d65248f1a",
            "nonce": 1646,
            "minor_version": 2,
            "difficulty": 815625611,
            "depth": 1039159,
            "major_version": 1,
            "orphan_status": false,
            "difficulty_top64": 0,
            "miner_tx_hash": "c7da3965f25c19b8eb7dd8db48dcd4e7c885e2491db77e289f0609bf8e08ec30",
            "long_term_weight": 210,
            "block_size": 210,
            "hash": "e22cf75f39ae720e8b71b3d120a5ac03f0db50bba6379e2850975b4859190bc6",
            "height": 912345,
            "timestamp": 1452793716
        },
        "untrusted": false,
        "status": "OK"
        },
        "id": "1571897903177",
        "jsonrpc": "2.0"
    }
 }




getBlockHeaderByHeight
```````````
Similar to get_block_header_by_hash above, this method includes a block's height as an input parameter to retrieve basic information about the block


Definition::

    GET /xmr/getBlockHeaderByHeight?height={height}

Example Request::

    GET /xmr/getBlockHeaderByHeight?height=912345

Response:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
  "data": {
    "result": {
      "block_header": {
        "block_weight": 210,
        "num_txes": 0,
        "reward": 7388968946286,
        "wide_difficulty": "0x309d758b",
        "pow_hash": "",
        "cumulative_difficulty_top64": 0,
        "prev_hash": "b61c58b2e0be53fad5ef9d9731a55e8a81d972b8d90ed07c04fd37ca6403ff78",
        "cumulative_difficulty": 754734824984346,
        "wide_cumulative_difficulty": "0x2ae6d65248f1a",
        "nonce": 1646,
        "minor_version": 2,
        "difficulty": 815625611,
        "depth": 1039161,
        "major_version": 1,
        "orphan_status": false,
        "difficulty_top64": 0,
        "miner_tx_hash": "c7da3965f25c19b8eb7dd8db48dcd4e7c885e2491db77e289f0609bf8e08ec30",
        "long_term_weight": 210,
        "block_size": 210,
        "hash": "e22cf75f39ae720e8b71b3d120a5ac03f0db50bba6379e2850975b4859190bc6",
        "height": 912345,
        "timestamp": 1452793716
      },
      "untrusted": false,
      "status": "OK"
    },
    "id": "1571898044641",
    "jsonrpc": "2.0"
  }
 }




getBlockHeadersRange
```````````
Similar to get_block_header_by_height above, but for a range of blocks,
This method includes a starting block height and an ending block height as parameters to retrieve basic information about the range of blocks.


Definition::

    GET /xmr/getBlockHeadersRange?startHeight={startHeight}&endHeight={endHeight}

Example Request::

    GET /xmr/getBlockHeadersRange?startHeight=1&endHeight=2

Response:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": {
        "result": {
        "headers": [
            {
            "block_weight": 383,
            "num_txes": 0,
            "reward": 17592169267200,
            "wide_difficulty": "0x1",
            "pow_hash": "",
            "cumulative_difficulty_top64": 0,
            "prev_hash": "418015bb9ae982a1975da7d79277c2705727a56894ba0fb246adaabb1f4632e3",
            "cumulative_difficulty": 2,
            "wide_cumulative_difficulty": "0x2",
            "nonce": 813497413,
            "minor_version": 0,
            "difficulty": 1,
            "depth": 1951507,
            "major_version": 1,
            "orphan_status": false,
            "difficulty_top64": 0,
            "miner_tx_hash": "52578a3816ec18ca6db2ec4f594b7c8a778caa4c52d2c1705bcbab9798a9ea7b",
            "long_term_weight": 383,
            "block_size": 383,
            "hash": "771fbcd656ec1464d3a02ead5e18644030007a0fc664c0a964d30922821a8148",
            "height": 1,
            "timestamp": 1397818193
            },
            {
            "block_weight": 382,
            "num_txes": 0,
            "reward": 17592152490000,
            "wide_difficulty": "0x1",
            "pow_hash": "",
            "cumulative_difficulty_top64": 0,
            "prev_hash": "771fbcd656ec1464d3a02ead5e18644030007a0fc664c0a964d30922821a8148",
            "cumulative_difficulty": 3,
            "wide_cumulative_difficulty": "0x3",
            "nonce": 1184456756,
            "minor_version": 0,
            "difficulty": 1,
            "depth": 1951506,
            "major_version": 1,
            "orphan_status": false,
            "difficulty_top64": 0,
            "miner_tx_hash": "f059b321c5c84f781563080f2ea5958788e16236ca65512e6d81e6e171c93d08",
            "long_term_weight": 382,
            "block_size": 382,
            "hash": "e2914694b698fb417eebaebad3fed4d13e8f670119c95c6e3fa83c1d45311520",
            "height": 2,
            "timestamp": 1397818193
            }
        ],
        "untrusted": false,
        "status": "OK"
        },
        "id": "1571898383549",
        "jsonrpc": "2.0"
    }
 }

getBlockByHeight
```````````
Full block information can be retrieved by block height


Definition::

    GET /xmr/getBlockByHeight?height={height}

Example Request::

    GET /xmr/getBlockByHeight?height=912345

Response:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": {
        "result": {
        "block_header": {
            "block_weight": 210,
            "num_txes": 0,
            "reward": 7388968946286,
            "wide_difficulty": "0x309d758b",
            "pow_hash": "",
            "cumulative_difficulty_top64": 0,
            "prev_hash": "b61c58b2e0be53fad5ef9d9731a55e8a81d972b8d90ed07c04fd37ca6403ff78",
            "cumulative_difficulty": 754734824984346,
            "wide_cumulative_difficulty": "0x2ae6d65248f1a",
            "nonce": 1646,
            "minor_version": 2,
            "difficulty": 815625611,
            "depth": 1039149,
            "major_version": 1,
            "orphan_status": false,
            "difficulty_top64": 0,
            "miner_tx_hash": "c7da3965f25c19b8eb7dd8db48dcd4e7c885e2491db77e289f0609bf8e08ec30",
            "long_term_weight": 210,
            "block_size": 210,
            "hash": "e22cf75f39ae720e8b71b3d120a5ac03f0db50bba6379e2850975b4859190bc6",
            "height": 912345,
            "timestamp": 1452793716
        },
        "blob": "0102f4bedfb405b61c58b2e0be53fad5ef9d9731a55e8a81d972b8d90ed07c04fd37ca6403ff786e0600000195d83701ffd9d73704ee84ddb42102378b043c1724c92c69d923d266fe86477d3a5ddd21145062e148c64c5767700880c0fc82aa020273733cbd6e6218bda671596462a4b062f95cfe5e1dbb5b990dacb30e827d02f280f092cbdd080247a5dab669770da69a860acde21616a119818e1a489bb3c4b1b6b3c50547bc0c80e08d84ddcb01021f7e4762b8b755e3e3c72b8610cc87b9bc25d1f0a87c0c816ebb952e4f8aff3d2b01fd0a778957f4f3103a838afda488c3cdadf2697b3d34ad71234282b2fad9100e02080000000bdfc2c16c00",
        "untrusted": false,
        "miner_tx_hash": "c7da3965f25c19b8eb7dd8db48dcd4e7c885e2491db77e289f0609bf8e08ec30",
        "json": "{\n  \"major_version\": 1, \n  \"minor_version\": 2, \n  \"timestamp\": 1452793716, \n  \"prev_id\": \"b61c58b2e0be53fad5ef9d9731a55e8a81d972b8d90ed07c04fd37ca6403ff78\", \n  \"nonce\": 1646, \n  \"miner_tx\": {\n    \"version\": 1, \n    \"unlock_time\": 912405, \n    \"vin\": [ {\n        \"gen\": {\n          \"height\": 912345\n        }\n      }\n    ], \n    \"vout\": [ {\n        \"amount\": 8968946286, \n        \"target\": {\n          \"key\": \"378b043c1724c92c69d923d266fe86477d3a5ddd21145062e148c64c57677008\"\n        }\n      }, {\n        \"amount\": 80000000000, \n        \"target\": {\n          \"key\": \"73733cbd6e6218bda671596462a4b062f95cfe5e1dbb5b990dacb30e827d02f2\"\n        }\n      }, {\n        \"amount\": 300000000000, \n        \"target\": {\n          \"key\": \"47a5dab669770da69a860acde21616a119818e1a489bb3c4b1b6b3c50547bc0c\"\n        }\n      }, {\n        \"amount\": 7000000000000, \n        \"target\": {\n          \"key\": \"1f7e4762b8b755e3e3c72b8610cc87b9bc25d1f0a87c0c816ebb952e4f8aff3d\"\n        }\n      }\n    ], \n    \"extra\": [ 1, 253, 10, 119, 137, 87, 244, 243, 16, 58, 131, 138, 253, 164, 136, 195, 205, 173, 242, 105, 123, 61, 52, 173, 113, 35, 66, 130, 178, 250, 217, 16, 14, 2, 8, 0, 0, 0, 11, 223, 194, 193, 108\n    ], \n    \"signatures\": [ ]\n  }, \n  \"tx_hashes\": [ ]\n}",
        "status": "OK"
        },
        "id": "1571896711791",
        "jsonrpc": "2.0"
    }
 }



getBlockByHash
```````````
Full block information can be retrieved by block hash


Definition::

    GET /xmr/getBlockByHash?hash={hash}

Example Request::

    GET /xmr/getBlockByHash?hash=e22cf75f39ae720e8b71b3d120a5ac03f0db50bba6379e2850975b4859190bc6

Response:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": {
        "result": {
        "block_header": {
            "block_weight": 210,
            "num_txes": 0,
            "reward": 7388968946286,
            "wide_difficulty": "0x309d758b",
            "pow_hash": "",
            "cumulative_difficulty_top64": 0,
            "prev_hash": "b61c58b2e0be53fad5ef9d9731a55e8a81d972b8d90ed07c04fd37ca6403ff78",
            "cumulative_difficulty": 754734824984346,
            "wide_cumulative_difficulty": "0x2ae6d65248f1a",
            "nonce": 1646,
            "minor_version": 2,
            "difficulty": 815625611,
            "depth": 1039186,
            "major_version": 1,
            "orphan_status": false,
            "difficulty_top64": 0,
            "miner_tx_hash": "c7da3965f25c19b8eb7dd8db48dcd4e7c885e2491db77e289f0609bf8e08ec30",
            "long_term_weight": 210,
            "block_size": 210,
            "hash": "e22cf75f39ae720e8b71b3d120a5ac03f0db50bba6379e2850975b4859190bc6",
            "height": 912345,
            "timestamp": 1452793716
        },
        "blob": "0102f4bedfb405b61c58b2e0be53fad5ef9d9731a55e8a81d972b8d90ed07c04fd37ca6403ff786e0600000195d83701ffd9d73704ee84ddb42102378b043c1724c92c69d923d266fe86477d3a5ddd21145062e148c64c5767700880c0fc82aa020273733cbd6e6218bda671596462a4b062f95cfe5e1dbb5b990dacb30e827d02f280f092cbdd080247a5dab669770da69a860acde21616a119818e1a489bb3c4b1b6b3c50547bc0c80e08d84ddcb01021f7e4762b8b755e3e3c72b8610cc87b9bc25d1f0a87c0c816ebb952e4f8aff3d2b01fd0a778957f4f3103a838afda488c3cdadf2697b3d34ad71234282b2fad9100e02080000000bdfc2c16c00",
        "untrusted": false,
        "miner_tx_hash": "c7da3965f25c19b8eb7dd8db48dcd4e7c885e2491db77e289f0609bf8e08ec30",
        "json": "{\n  \"major_version\": 1, \n  \"minor_version\": 2, \n  \"timestamp\": 1452793716, \n  \"prev_id\": \"b61c58b2e0be53fad5ef9d9731a55e8a81d972b8d90ed07c04fd37ca6403ff78\", \n  \"nonce\": 1646, \n  \"miner_tx\": {\n    \"version\": 1, \n    \"unlock_time\": 912405, \n    \"vin\": [ {\n        \"gen\": {\n          \"height\": 912345\n        }\n      }\n    ], \n    \"vout\": [ {\n        \"amount\": 8968946286, \n        \"target\": {\n          \"key\": \"378b043c1724c92c69d923d266fe86477d3a5ddd21145062e148c64c57677008\"\n        }\n      }, {\n        \"amount\": 80000000000, \n        \"target\": {\n          \"key\": \"73733cbd6e6218bda671596462a4b062f95cfe5e1dbb5b990dacb30e827d02f2\"\n        }\n      }, {\n        \"amount\": 300000000000, \n        \"target\": {\n          \"key\": \"47a5dab669770da69a860acde21616a119818e1a489bb3c4b1b6b3c50547bc0c\"\n        }\n      }, {\n        \"amount\": 7000000000000, \n        \"target\": {\n          \"key\": \"1f7e4762b8b755e3e3c72b8610cc87b9bc25d1f0a87c0c816ebb952e4f8aff3d\"\n        }\n      }\n    ], \n    \"extra\": [ 1, 253, 10, 119, 137, 87, 244, 243, 16, 58, 131, 138, 253, 164, 136, 195, 205, 173, 242, 105, 123, 61, 52, 173, 113, 35, 66, 130, 178, 250, 217, 16, 14, 2, 8, 0, 0, 0, 11, 223, 194, 193, 108\n    ], \n    \"signatures\": [ ]\n  }, \n  \"tx_hashes\": [ ]\n}",
        "status": "OK"
        },
        "id": "1571900658875",
        "jsonrpc": "2.0"
    }
 }


getFeeEstimate
```````````
Gives an estimation on fees per byte

Definition::

    GET /xmr/getFeeEstimate

Example Request::

    GET /xmr/getFeeEstimate

Response:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
  "data": {
    "result": {
      "untrusted": false,
      "fee": 14917,
      "quantization_mask": 10000,
      "status": "OK"
    },
    "id": "1571900764457",
    "jsonrpc": "2.0"
  }
 }


Return:

.. code-block:: json

 {
    fee - unsigned int; Amount of fees estimated per byte in atomic units
    quantization_mask - unsigned int; Final fee should be rounded up to an even multiple of this value
 }


getHeight
```````````
Get the node's current height

Definition::

    GET /xmr/getHeight

Example Request::

    GET /xmr/getHeight

Response:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": {
        "untrusted": false,
        "hash": "cea0baafaf626dba2fd53b2ff9b6d3e7f514e759303da7985a819e8fe665b735",
        "height": 1951534,
        "status": "OK"
    }
 }




getTransactions
```````````
Look up one or more transactions by hash

Definition::

    GET /xmr/getTransactionsgetTransactions?{tx_hash}&decodeAsJson=true

Example Request::

    GET /xmr/getTransactions?txsHashes=d6e48158472848e6687173a91ae6eebfa3e1d778e65252ee99d7515d63090408&decodeAsJson=true

Response:

.. code-block:: json

 {
    "status": 0,
    "message": "success",
    "data": {
        "status": "OK",
        "txs": [{
            "as_hex": "...",
            "as_json": "",
            "block_height": 993442,
            "block_timestamp": 1457749396,
            "double_spend_seen": false,
            "in_pool": false,
            "output_indices": [198769,418598,176616,50345,509],
            "tx_hash": "d6e48158472848e6687173a91ae6eebfa3e1d778e65252ee99d7515d63090408"
        }],
        "txs_as_hex": ["..."],
        "untrusted": false
    }
 }

Return:

.. code-block:: json

 {
    missed_tx - array of strings. (Optional - returned if not empty) Transaction hashes that could not be found.
    status - General RPC error code. "OK" means everything looks good.
    txs - array of structure entry as follows:
    as_hex - string; Full transaction information as a hex string.
    as_json - json string; List of transaction info:
    version - Transaction version
    unlock_time - If not 0, this tells when a transaction output is spendable.
    vin - List of inputs into transaction:
    key - The public key of the previous output spent in this transaction.
    amount - The amount of the input, in atomic units.
    key_offsets - A list of integer offets to the input.
    k_image - The key image for the given input
    vout - List of outputs from transaction:
    amount - Amount of transaction output, in atomic units.
    target - Output destination information:
    key - The stealth public key of the receiver. Whoever owns the private key associated with this key controls this transaction output.
    extra - Usually called the "payment ID" but can be used to include any random 32 bytes.
    signatures - List of signatures used in ring signature to hide the true origin of the transaction.
    block_height - unsigned int; block height including the transaction
    block_timestamp - unsigned int; Unix time at chich the block has been added to the blockchain
    double_spend_seen - boolean; States if the transaction is a double-spend (true) or not (false)
    in_pool - boolean; States if the transaction is in pool (true) or included in a block (false)
    output_indices - array of unsigned int; transaction indexes
    tx_hash - string; transaction hash
    txs_as_hex - string; Full transaction information as a hex string (old compatibility parameter)
 }


getAltBlocksHashes
```````````
Get the known blocks hashes which are not on the main chain


Definition::

    GET /xmr/getAltBlocksHashes
Example Request::

    GET /xmr/getAltBlocksHashes
Response:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
  "data": {
    "untrusted": false,
    "blks_hashes": [
      "d4c8ed9449351113d6805a5c0b39b87c0d13a2cf6cb03db0f4bac62cff54fcac",
      "85a66fc974d7897f6c0260fd29febf0a62edfa9d3d38b19a8caf133009c0e8ff",
      "e8b3812fa85c33064d2e00bbe840fccc7b0463f680f979eb87fda2c15326f950",
      "7d1fb2490985031c68e2ae1e61d613a4fef028292e40b2cd73d47875a8431f52",
      "f82201e30050f8740dae0696a828ec0fc5af99b35cd06ab4cefa0028d4841163",
      "943ca363c0a9c7bf9689340f7657904b3f6d21f3e9f4fdd0306aa9da42b75e6e",
      "0e8e65e30d63222f4fdf96103689af8e3251fc8ee7b3c6e68702b7c45e32e382",
      "2a84592df5a60aa905e71a85e6899a731d49c8480220ece6165c55191d81b0aa",
      "2781adfbef757528b6fe19b178cd4f96fec298131317df7704d014d839738990",
      "7b63a9104d8bb92ab31aaf3fc944e21d0243efe39744b2db48577bb0f836c585",
      "893151868470cc94742b5171e5dfd8a42c02ebdf2de0ace127bd583e6a6a8824",
      "a984f9dc66ed910f478d9899fb16cc18e13750af08062b38daff4d2986a79291",
      "365882ffa7e40cb3517ec9f6f22aa62e533e5a553a0d3de50b85914420864f0e",
      "fa247f9152af67e5667fc040ea6d9f62b360a055291c8607ee38b899d921723d",
      "8a00a265a4f069b79e1fe6eddad4da941c91efd41600826707778b0d48a095cd"
    ],
    "status": "OK"
  }
 }

Return:

.. code-block:: json

 {
   blks_hashes - array of strings; list of alternative blocks hashes to main chain
 }



isKeyImageSpent
```````````
Check if outputs have been spent using the key image associated with the output

Definition::

    GET /xmr/isKeyImageSpent?keyImages=xxxxxxxx
Example Request::

    GET /xmr/isKeyImageSpent?keyImages=xxxxxxxxx
Response:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
  "data": {
    "spent_status": [1,2],
    "untrusted": false,
    "status": "OK"
  }
 }

Return:

.. code-block:: json

 {
  spent_status - unsigned int list; List of statuses for each image checked. Statuses are follows: 0 = unspent, 1 = spent in blockchain, 2 = spent in transaction pool
 }


sendRawTransaction
```````````
Broadcast a raw transaction to the network

Definition::

    GET /xmr/sendRawTransaction?txAsHex=xxxxxxxx&doNotRelay=true
Example Request::

    GET /xmr/sendRawTransaction?txAsHex=xxxxxxxxx&doNotRelay=true
Response:

.. code-block:: json

 {
  "status": 0,
  "message": "success",
  "data": {
    "status": "OK"
  }
 }