# graph3

A distributed Web3 stateless smart contract hypergraph.

### API:

**Create Node / change class (drop with empty class):**

- **node**(_string_ **id**, _string_ **class**, string **subclass**)

**Add a property to a node / link (drop with empty prop/value):**

- **prop**(_string_ **id**, _string_ **prop**, _string_ **value**)

**Link nodes & links or change class (unlink with empty class):**

- **link**(_string_ **from**, _string_ **to**, _string_ **class**)

**Signed batch transaction:**

```
[
  [...eventNumbers],
  [...[arg0, arg1, arg2]],
  [...keccak256([...eventNumbers, ...args])]
]
```

- **batch**(_uint256[]_ **events**, _string[3][]_ **args**, _bytes32[]_ **sig**)

### Mainnet contract:

```
0x9943B6aB8d6ede28D8b8fC5c69243441D7A5c48B
```

### ABI:

```json
[
  {
    "anonymous": false,
    "inputs": [
      {
        "indexed": false,
        "internalType": "uint256[]",
        "name": "_events",
        "type": "uint256[]"
      },
      {
        "indexed": false,
        "internalType": "string[3][]",
        "name": "_args",
        "type": "string[3][]"
      },
      {
        "indexed": false,
        "internalType": "bytes32[]",
        "name": "_sig",
        "type": "bytes32[]"
      }
    ],
    "name": "Batch",
    "type": "event"
  },
  {
    "anonymous": false,
    "inputs": [
      {
        "indexed": true,
        "internalType": "string",
        "name": "_from",
        "type": "string"
      },
      {
        "indexed": true,
        "internalType": "string",
        "name": "_to",
        "type": "string"
      },
      {
        "indexed": true,
        "internalType": "string",
        "name": "_class",
        "type": "string"
      }
    ],
    "name": "Link",
    "type": "event"
  },
  {
    "anonymous": false,
    "inputs": [
      {
        "indexed": true,
        "internalType": "string",
        "name": "_id",
        "type": "string"
      },
      {
        "indexed": true,
        "internalType": "string",
        "name": "_class",
        "type": "string"
      },
      {
        "indexed": true,
        "internalType": "string",
        "name": "_subclass",
        "type": "string"
      }
    ],
    "name": "Node",
    "type": "event"
  },
  {
    "anonymous": false,
    "inputs": [
      {
        "indexed": true,
        "internalType": "string",
        "name": "_id",
        "type": "string"
      },
      {
        "indexed": true,
        "internalType": "string",
        "name": "_prop",
        "type": "string"
      },
      {
        "indexed": true,
        "internalType": "string",
        "name": "_value",
        "type": "string"
      }
    ],
    "name": "Prop",
    "type": "event"
  },
  {
    "inputs": [
      {
        "internalType": "uint256[]",
        "name": "_events",
        "type": "uint256[]"
      },
      {
        "internalType": "string[3][]",
        "name": "_args",
        "type": "string[3][]"
      },
      {
        "internalType": "bytes32[]",
        "name": "_sig",
        "type": "bytes32[]"
      }
    ],
    "name": "batch",
    "outputs": [],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "string",
        "name": "_from",
        "type": "string"
      },
      {
        "internalType": "string",
        "name": "_to",
        "type": "string"
      },
      {
        "internalType": "string",
        "name": "_class",
        "type": "string"
      }
    ],
    "name": "link",
    "outputs": [],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "string",
        "name": "_id",
        "type": "string"
      },
      {
        "internalType": "string",
        "name": "_class",
        "type": "string"
      },
      {
        "internalType": "string",
        "name": "_subclass",
        "type": "string"
      }
    ],
    "name": "node",
    "outputs": [],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "string",
        "name": "_id",
        "type": "string"
      },
      {
        "internalType": "string",
        "name": "_prop",
        "type": "string"
      },
      {
        "internalType": "string",
        "name": "_value",
        "type": "string"
      }
    ],
    "name": "prop",
    "outputs": [],
    "stateMutability": "nonpayable",
    "type": "function"
  }
]
```
