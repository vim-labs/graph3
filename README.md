# graph3

A distributed Web3 hypergraph.

### API:

**Create Node / change class (drop with empty class):**

* **node**(*string* **id**, *string* **class**, string **subclass**)

**Add a property to a node / link (drop with empty prop/value):**

* **prop**(*string* **id**, *string* **prop**, *string* **value**)

**Link nodes & links or change class (unlink with empty class):**

* **link**(*string* **from**, *string* **to**, *string* **class**) 

**Signed batch transaction:**

```json
[
  [...eventNumbers],
  [...[arg0, arg1, arg2]], 
  [...keccak256([...eventNumbers, ...args])]
]
```

* **batch**(*uint256[]* **events**, *string[3][]* **args**, *bytes32[]* **sig**)

### Mainnet contract:

```
0x9943B6aB8d6ede28D8b8fC5c69243441D7A5c48B
```