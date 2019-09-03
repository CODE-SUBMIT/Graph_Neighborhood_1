# Experiment 7 & Experiment 8 & Experiment 9

## Test run
git clone https://github.com/bknyaz/graph_nn.git
cp data

```bash
python graph_unet.py --model gcn  # to run (s)GCN
python graph_unet.py --model unet  # to run (s)Graph U-Net
python graph_unet.py --model mgcn  # to run (s)Multigraph GCN
python graph_unet.py --model mgcn -K 2  # to run (s)Multigraph ChebNet with filter scale K = 2
```


```bash
# Experiment No7
# Examples
# no use -c flag
```python graph_unet.py -D ENZYMES -f 128,128,128 --n_hidden 256 --lr 0.0005 --epochs 100 --lr_decay_step 150 -g


# use -c flag
```bash
```python graph_unet.py -D ENZYMES -f 128,128,128 --n_hidden 256 --lr 0.0005 --c --epochs 100 --lr_decay_step 150 -g


# use batch normalization
```bash
```python graph_unet.py -D ENZYMES -f 128,128,128 --n_hidden 256 --lr 0.0005 --c --bn --epochs 100 --lr_decay_step 150 -g


# Experiment No8
# Examples

```bash
```python graph_unet.py -M mgcn -K 2 -f 32,32,32 --n_hidden 96 --bn --epochs 50 --lr_decay_steps 25,35,45 --lr 0.001


```bash
```python graph_unet.py -M mgcn -f 32,32,32 --n_hidden 96 --bn --epochs 50 --lr_decay_steps 25,35,45 --lr 0.001


```bash
```python graph_unet.py -M gcn -K 2 -f 32,32,32 --n_hidden 96 --bn --epochs 50 --lr_decay_steps 25,35,45 --lr 0.001


# Experiment No9
# Examples
Repeating 10 times for different seeds:
```bash
for i in $(seq 1 10); do seed=$(( ( RANDOM % 10000 )  + 1 )); python graph_unet.py --model gcn --seed $seed | tee logs/gcn_proteins_"$i".log; done
