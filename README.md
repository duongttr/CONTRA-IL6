<h1 align="center">🎮 CONTRA-IL6 ✈️💨</h1>
<p align="center"><a href="">📝 Paper</a> | <a href="https://1drv.ms/f/c/fa72f5f3c0e55162/EqrXX1Jbr7dIhKGKn8iSHRQB9KWFc-IxyGX-oJpX2ZEq9A?e=yZsxe7">🚩 Model & Dataset</a></p>

The official implementation of paper: **CONTRA-IL6**

## Abstract
> Update soon!

## News
> Update soon!

## TOC
This project is summarized to:
- Package installation
    - Pip
    - How to use
- Training
    - Installing environment
    - Preparing datasets
    - Training models
- Citation

## Package installation
### Pip

Require: **Python 3.9**

```zsh
pip install contra-il6
```

or

```zsh
pip install -U 'contra-il6 @ git+https://github.com/duongttr/CONTRA-IL6.git'
```

### Minimum system requirements

The package loads multiple large protein language models (ESM-2 3B, ESM-1 670M, ProtTrans T5-XL, SeqVec) simultaneously for inference. Please ensure your system meets the following requirements:

| Component | Minimum | Recommended |
|-----------|---------|-------------|
| **Python** | 3.9 | 3.9+ |
| **RAM** | 16 GB | 32 GB |
| **Disk** | 30 GB free | 50 GB free |
| **CPU** | x86_64, 4 cores | x86_64, 8+ cores |
| **OS** | Linux / macOS / Windows | Linux |
| **Internet** | Required (first run) | — |

> **Note:** On first run, the tool will automatically download pre-trained model weights (~20 GB) for ESM-2, ESM-1, ProtTrans T5-XL, and SeqVec. Subsequent runs use cached weights. No GPU is required — all inference runs on CPU.

### How to use
```
contra-il6 [OPTIONS]

Options:
  -i, --input PATH          Path to a FASTA file containing peptide sequences.
  -t, --threshold FLOAT     Threshold for classification (default: 0.46).
  -b, --batch_size INTEGER  Batch size for processing (default: 4).
  -o, --output PATH         Output file to save predictions.
  --help                    Show this message and exit.
```

Example:
```zsh
contra_il6 -i data/Validate_positive.txt -o data/Validate_positive_result.csv
```

## Training
### Installing environment
Create environment by using [conda](https://docs.conda.io/projects/conda/en/latest/user-guide/getting-started.html):
```zsh
conda create -n contra_il6 python=3.10
conda activate contra_il6
```

Clone the repo, then install the required packages:
```zsh
cd CONTRA-IL6/
python -m pip install -r requirements.txt
```

### Preparing datasets
You can check the **benchmark and external test datasets** inside [`data`](./data) folder. Or you can download 12 extracted features mentioned in paper at this [🔗 link](https://1drv.ms/f/c/fa72f5f3c0e55162/EqrXX1Jbr7dIhKGKn8iSHRQB9KWFc-IxyGX-oJpX2ZEq9A?e=yZsxe7) and extract to [`data`](./data) folder.

### Training models
To reconstruct the checkpoints, you can run following commands:
```zsh
python train.py --config_path configs/top_4_features.yaml --save_config
```

## Citation
> Update soon!