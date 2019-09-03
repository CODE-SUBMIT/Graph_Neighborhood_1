# Experiment No2 & Experiment No6

### Requirements

The code is written Python 3.6 and TensorFlow version 1 (tested on versions 1.12 and 1.16). 
It requires scikit-learn >= 0.21.2 and the python 
packages 
- `FAR-HO`, available [here](https://github.com/lucfra/FAR-HO) (advised branch: final_ICML2019)
- `GCN`, available [here](https://github.com/tkipf/gcn) 


##### Datasets

UCI datasets should be loaded automatically, while graph-based datasets (Cora and Citeseer) should be downloaded and
included in the `lds/data` folder.
FMA dataset should also be downloaded, please email the authors if interested.

### Installation (optional)

```
python setup.py install
```

The scripts contained in `lds.py` should work also without installing the package. 

## Run

Navigate to `lds_gnn` folder.

The main script is in the file `lds.py`. The options are
```
-d: the evaluation dataset. Available datasets are iris, wine, breast_cancer, digits, 20newstrain, 
            20news10, cora, citeseer, fma. Default breast_cancer
-m: the method: lds or knnlds. Default knnlds
-s: the random seed. Default 1
-e: the percentage of missing edges (valid only for cora and citeseer dataset). Default 50
```

For experiments with incomplete graphs on Cora and Citeseer, run 
```
#Experiment No6
python lds.py -m lds -e {an integer between 0 and 100} -d {cora or citeseer} -s {if you want to specify random seed}#(s)lds
```

For experiments in semi-supervised learning (with no input graph), run
```
#Experiment No2
python lds.py -m knnlds -d {any available dataset} -s {if you want to specify random seed}#(s)knn-lds
```

