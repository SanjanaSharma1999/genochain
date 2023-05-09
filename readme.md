# GenoChain Implementation

This is a Python implementation of a simple blockchain. 
It has the following features:
Creation of a genesis block with a given FASTA sequence
Addition of new blocks with a given FASTA sequence, associated ID, and version changes
Versioning of FASTA sequences
Checking and printing the blockchain


## Requirements
Python 3.x

## Usage 
Import the BlockChain class from blockchain.py:
```python
from genochain.genochain import BlockChain
```
Create a blockchain instance:
```python
blockchain = BlockChain(genesis_fasta)
```
Add blocks to the blockchain:
```python
blockchain.add_block(data, version_changes)
```
Check the blockchain for versioning:
```python
blockchain.check_version(id, fasta)
```
Print the blockchain:
```python
blockchain.print_blockchain()
```

Example
```python
from genochain.genochain import BlockChain


# Create a blockchain with a given FASTA sequence
blockchain = BlockChain("GATTACA")

# Add a block with a new FASTA sequence and version changes
blockchain.add_block({"id": "Sequence 1", "fasta": "GATTAAC"}, {"version-1": "Added new sequence"})

# Check the blockchain for versioning
blockchain.check_version("Sequence 1", "GATTCAC")

# Print the blockchain
blockchain.print_blockchain()
```

License
This code is licensed under the MIT License. Please see the LICENSE.txt file for more details.
