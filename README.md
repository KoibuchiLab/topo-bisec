# topo-bisec
This repo creates a graph with (possible) largest bisection bandwidth.

## Prerequisite
* networkx
* metis

In case of problems with *gpmetis*, install *metis* as follows.
```shell
$ apt-get install metis
```
Or put the executable *gpmetis* in the same folder. 
* You also need to modify the line 282 in [bisec.rb](bisec.rb) accordingly: gpmetis --> ./gpmetis.


## Run
```shell
$ python3 topo-bisec.py <nnodes> <degree> [-i <iteration>] #default iteration is 1,000
```

## Source Files
### [topo-bisec.py](topo-bisec.py)
* This is the main program.
### [bisec.rb](bisec.rb)
* This includes the calculation of bisection bandwidth (authored by ikki).

## Output
The generated topology (edge file) and output information are stored in the output/ folder. 