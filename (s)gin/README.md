# Experiment No1:

## Installation
Install PyTorch following the instuctions on the [official website] (https://pytorch.org/). The code has been tested over PyTorch 0.4.1 and 1.0.0 versions.

Then install the other dependencies.
```
pip install -r requirements.txt
```

## Test run
git clone https://github.com/weihua916/powerful-gnns.git
Unzip the dataset file
```
unzip dataset.zip
```

and run

```
python main.py
```

Default parameters are not the best performing-hyper-parameters. Hyper-parameters need to be specified through the commandline arguments. Please refer to the baseline paper 

* **[GIN](https://github.com/weihua916/powerful-gnns)** from Xu *et al.*: [Representation learning on graphs: Methods and applications](https://arxiv.org/abs/1810.00826) (ICLR-2019) 

for the details of how the hyper-parameters is set.

Type

```
python main.py --help
```

to learn hyper-parameters to be specified.

