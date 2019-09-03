# Experiments No3

## Examples 

To run `(s)PWL-C` on `MUTAG` with 0 WL iterations and p=1, run 
```
$ cd src
$ python main.py -c -n 0 -p 1 data/MUTAG/*.gml -l data/MUTAG/Labels.txt
```

The arguments for all our methods (with `1 WL iteration` and `p=1`) are as follows:

`(*s)PWL`: `main.py -n 1 -p 1 data/...`

`(s)PWL-C`: `main.py -c -n 1 -p 1 data/...`

`(s)PWL-UC`: `main.py -u -c -n 1 -p 1 data/...`

## Installtion

P-WL is developed and maintained by members of the [Machine Learning and
Computational Biology Lab](https://www.bsse.ethz.ch/mlcb) of [Prof. Dr.
Karsten Borgwardt](https://www.bsse.ethz.ch/mlcb/karsten.html):

- Bastian Rieck ([GitHub](https://github.com/Submanifold))
- Christian Bock ([GitHub](https://github.com/chrisby))

