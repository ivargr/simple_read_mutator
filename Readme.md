# Simple read mutator
Extremely simple and quite fast module for adding SNVs and Indels to a genomic sequence (read). 
Uses no error rate models in order to be as fast as posssible.

## Install
Clone repo and enter directory, then run:
```bash
pip3 install .
```

## Usage
```python
from simple_read_mutator import Mutator
m = Mutator(sequence_length=5)
mutated_sequence = m.mutate_sequence("ACGTA")
mutated_sequence2 = m.mutate_sequence("AAAAA", snv_prob=0.01, insertion_prob=0.001, deletion_prob=0.00001)  
```