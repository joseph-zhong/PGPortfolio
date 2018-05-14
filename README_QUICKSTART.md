# Quick Start 

These are primarily summary from the [User Guide](user_guide.md)

## Instructions

Let's just get started on training and seeing some baseline results!

### Setup the repository dependencies.

```bash
# (optional use a virtualenv) virtualenv .; source bin/activate
pip install -r requirements.txt
```

### Download the data.

```bash
python main.py --mode=download_data
```

### Begin training

Copy the default `net_config.json` training configuration file to
`nntrader/nntrader`, and begin training!

```bash
mkdir -p nntrader/nntrader
cp pgportfolio/net_config.json nntrader/nntrader/net_config.json
python main.py --mode=generate --repeat=1
```

#### :train: Train! :train:

Default settings on CPU.

```bash
python main.py --mode=train --processes=1 
```

(from the [User Guide](user_guide.md), You can also modify `--device=gpu` to use
a GPU to train. For hyperparameter search you can use `--processes=<n>` to run
multiple parallel jobs.


