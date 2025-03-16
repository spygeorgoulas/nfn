# Notes

## Code
- paths on yaml and code in data

## NFN Architecture
### Pending
- For the IO-encoding (dimension 13)

- i have to build the architecture
- 3 equivariant NF-Layers, with 512 channels each, ReLU activations
- Followed by invariant NF-Layers (mean pooling)
- and a three-layer MLP head with 1000 hidden units and ReLU activation. Dropout applied on the MLP head only

- how many classes task
- MLP dropout = 0.5
### OK
- Batch size = 32
- Training steps 2x10^5
- Optimizer = Adam
- Learning rate = 1e-4

## NFN Experiments
python -m experiments.launch_classify_siren +setup=shapenet +mode=debug

tmux new -s nfn
tmux ls
ctrl b d
tmux attach -t nfn
tmux kill-session -t nfn