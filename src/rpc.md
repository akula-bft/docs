## JSONRPC
Akula supports the following standard JSONRPC calls:

### eth
- `eth_blockNumber`
- `eth_chainId`
- `eth_call`
- `eth_estimateGas`
- `eth_getBalance`
- `eth_getBlockByHash`
- `eth_getBlockByNumber`
- `eth_getBlockTransactionCountByHash`
- `eth_getBlockTransactionCountByNumber`
- `eth_getCode`
- `eth_getStorageAt`
- `eth_getTransactionByHash`
- `eth_getTransactionByBlockHashAndIndex`
- `eth_getTransactionByBlockNumberAndIndex`
- `eth_getTransactionCount`
- `eth_getTransactionReceipt`
- `eth_getUncleByBlockNumberAndIndex`
- `eth_getUncleCountByBlockHash`
- `eth_getUncleCountByBlockNumber`
- `eth_syncing`

### net
- `net_listening`
- `net_peerCount`
- `net_version`

### trace
- `trace_call`
- `trace_callMany`
- `trace_rawTransaction`
- `trace_replayBlockTransactions`
- `trace_replayTransaction`
- `trace_block`
- `trace_filter`

### erigon
- `erigon_getHeaderByNumber`

### otterscan
- `otterscan_getApiLevel`
- `otterscan_getInternalOperations`
- `otterscan_searchTransactionsBefore`
- `otterscan_searchTransactionsAfter`
- `otterscan_getBlockDetails`
- `otterscan_getBlockDetailsByHash`
- `otterscan_getBlockTransactions`
- `otterscan_hasCode`
- `otterscan_traceTransaction`
- `otterscan_getTransactionError`
- `otterscan_getTransactionBySenderAndNonce`
- `otterscan_getContractCreator`

Please consult [Ethereum Foundation docs](https://ethereum.org/en/developers/docs/apis/json-rpc/) for detailed description of each RPC call.

## gRPC
In addition to standard JSONRPC APIs, Akula supports [additional APIs resembling JSONRPC, but over gRPC protocol](https://github.com/ledgerwatch/interfaces/tree/master/web3), served by default at port 7545.
