# Experiment No5

## Requirements
1. python 2.7
2. Tensorflow
3. Networkx 1.11

## Training

```
python train.py --epochs 500 --model feedback --edge_dropout 0.5 --learning_rate 0.01 --autoregressive_scalar 0.5#(s)Graphite-VAE
python train.py --epochs 500 --model VAE --edge_dropout 0.5 --learning_rate 0.01 --autoregressive_scalar 0.5#(s)VGAE
```
