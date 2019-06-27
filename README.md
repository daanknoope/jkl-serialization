# jkl-serialization
Python library for (de)serializing **jkl** data as used by the Bayesian Network Structure Learner [GOBNILP](https://www.cs.york.ac.uk/aig/sw/gobnilp/) and proposed by Jaakkola et al. in [Learning Bayesian Network Structure using LP Relaxations](https://people.csail.mit.edu/dsontag/papers/structure_aistats10.pdf). 

## Example

### JKL String
```
3
0 4
-2.772589 2 1 2
-2.865831 0
-2.963209 1 2
-2.963209 1 1
1 4
-2.772589 2 0 2
-2.865831 0
-2.963209 1 2
-2.963209 1 0
2 4
-2.772589 2 0 1
-2.865831 0
-2.963209 1 1
-2.963209 1 0
```

###  Serialized Python Object
```python
{
  '0': [('-2.772589', ['1', '2']),
        ('-2.865831', []),
        ('-2.963209', ['2']),
        ('-2.963209', ['1'])],
 '1': [('-2.772589', ['0', '2']),
       ('-2.865831', []),
       ('-2.963209', ['2']),
       ('-2.963209', ['0'])],
 '2': [('-2.772589', ['0', '1']),
       ('-2.865831', []),
       ('-2.963209', ['1']),
       ('-2.963209', ['0'])]
  }
```

## Build Status
[![Build Status](https://travis-ci.org/daanknoope/jkl-serialization.svg?branch=master)](https://travis-ci.org/daanknoope/jkl-serialization)
[![codecov](https://codecov.io/gh/daanknoope/jkl-serialization/branch/master/graph/badge.svg)](https://codecov.io/gh/daanknoope/jkl-serialization)

