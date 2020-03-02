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
