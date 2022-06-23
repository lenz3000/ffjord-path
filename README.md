# Path Gradients for Continuous Normalizing Flows

Code for reproducing the experiments in the paper:

> Lorenz Vaitl, Kim A. Nicoli, Shinichi Nakajima, Pan Kessel. "Path-Gradient Estimators for Continuous Normalizing Flows."International Conference on Machine Learning (2022).
> [[arxiv]](https://arxiv.org/abs/2206.09016)

We have forked the repository for [[ffjord]](https://github.com/rtqichen/ffjord) and implemented the path gradient estimator for "cnf" and "cnf_rank", the corresponding options are "cnf_stl" and "cnf_rank_stl".
## Setup:

```
pip install -e requirements.txt
chmod +x download.sh
./download.sh
```

## Usage:
For training with the path gradient e.g. on MNIST:
```
python train_vae_flow.py --dataset mnist --flow=cnf_rank_stl --epochs=5000 --dims=1024-1024 --rank 64 --num_blocks 2 --num_flows 2 
```

## Bibtex:
If you use this code please cite:
@article{vaitl2022path,
  title={Path-Gradient Estimators for Continuous Normalizing Flows},
  author={Vaitl, Lorenz and Nicoli, Kim A. and Nakajima, Shinichi and Kessel, Pan},
  journal={International Conference on Machine Learning},
  year={2022}
}
