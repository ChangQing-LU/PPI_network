# PPI_network

Rare disease dual-anchor PPI scoring workflow.

The runnable code lives in `script1/`. The repository intentionally excludes
large reference databases, local Python environments, logs, and generated
outputs so that others can clone the code and reproduce the workflow with their
own data directory.

## Quick Start

```bash
git clone https://github.com/ChangQing-LU/PPI_network.git
cd PPI_network/script1

./setup_env.sh
./download_data.sh
```

Run a small command-line scoring job:

```bash
../ppi_env/bin/python Network.py \
  --data-dir ../data \
  --candidate-file candidates.txt \
  --hpo-ids HP:0000488 HP:0000505 \
  --output-csv ../output/result.csv \
  --audit-json ../output/audit.json
```

Start the API:

```bash
cd script1
./run_api.sh
```

For the full method description, required data files, API routes, and case-level
entry points, see [script1/README.md](script1/README.md).
