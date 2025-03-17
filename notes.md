# Notes

# Resources problem
- ..

## NFN Architecture

- 3 equivariant NF-Layers, with 512 channels each, ReLU activations
- Followed by invariant NF-Layers (mean pooling)
- 3 inputs - 1 output

----
----
### OK
- Batch size = 32
- Training steps 2x10^5
- Optimizer = Adam
- Learning rate = 1e-4
- how many classes task 10 ok on head mlp
- data utils code
- data paths, labels, files, etc
- and a three-layer MLP head with 1000 hidden units and ReLU activation. Dropout applied on the MLP head only . MLP dropout = 0.5

## NFN Experiments
python -m experiments.launch_classify_siren +setup=shapenet +mode=debug

tmux new -s nfn
tmux ls
ctrl b d
tmux attach -t nfn
tmux kill-session -t nfn


# No Need
- shapenet10_128x2_3000S_SPYROS / siren_shapenet10_wts
- For the IO-encoding (dimension 13)