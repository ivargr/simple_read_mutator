# Simple read mutator
Extremely simple and quite fast module for adding SNVs and Indels to a genomic sequence (read). 
Errors are uniformly distributed (i.e. no error model is used) in order to be as fast as possible.

This package is only tested with Python 3.

## Install
Use pip:
```bash
pip3 install simple_read_mutator
```
Or install locally, by cloning repo, entering the directory and running:

```bash
pip3 install -e .
```

## Usage
```python
from simple_read_mutator import Mutator
m = Mutator(sequence_length=5)
mutated_sequence = m.mutate_sequence("ACGTA")
mutated_sequence2 = m.mutate_sequence("AAAAA", snv_prob=0.01, insertion_prob=0.001, deletion_prob=0.00001)  
```

NB: Always re-use `Mutator` object when dealing with sequences of the same length. There is an overhead when creating this object.