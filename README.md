# EDM Reproduction & Ablation

Reproduction and ablation study of **Karras et al. 2022** — *Elucidating the Design Space of Diffusion-Based Generative Models* (EDM).

## Structure

```
edm-ablations/
├── configs/          # YAML experiment configs
├── src/edm_repro/    # core library
├── scripts/          # cloud/cluster utilities
├── experiments/      # run registry
├── tests/            # unit + integration tests
├── blog/             # write-up drafts
└── third_party/      # NVlabs/edm, k-diffusion submodules
```

## Setup

```bash
git submodule update --init --recursive
pip install -e ".[dev]"
```

## Quick start

```bash
# Deterministic sampling ablation
python -m edm_repro.generate --config configs/repro/sampling_det.yaml

# Run full ablation grid
python scripts/run_ablation.py --config configs/repro/sampling_det.yaml

# Training (reduced)
python -m edm_repro.train --config configs/repro/train_reduced.yaml
```

## References

- Karras et al. 2022 — https://arxiv.org/abs/2206.00364
- NVlabs/edm — https://github.com/NVlabs/edm
- crowsonkb/k-diffusion — https://github.com/crowsonkb/k-diffusion
