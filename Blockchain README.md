# Documentation for Blockchain.py

## Importing
The Blockchain Class can be imported and instantiated as follows:
```
from Blockchain import Blockchain
bc = Blockchain()
```
The newly created object contains a genesis block with index=0 and data=None.

## Usage
The Blockchain Object has 3 external functions.

- `mine_block`
    - Takes data as input in the format of Prescription (See Models.py for details)
    - Performs PoW to generate new nonce and creates new block.
    - Inserts new block into blockchain object with a sequential index.
- `get_block_from_index`
    - Takes an integer value as input.
    - Returns the contents of a block given its index value.
- `is_chain_valid`
    - Takes no input.
    - Checks the hash value of each block to be valid.
    - Returns boolean value after all blocks are checked.

These functions can be used to store data in the blockchain object as follows:
```
# Prescription objects are required to be stored on the blockchain.
for p in prescriptions:
    bc.mine_block(p)

print(bc.get_block_from_index(1))
print(bc.is_chain_valid)
```
