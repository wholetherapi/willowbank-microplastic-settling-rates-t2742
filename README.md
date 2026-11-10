# Settling velocities of microplastic fibres in slow-moving rivers

> **Release status: public release** — v1.1.3 (2025-06-18).
> Archived at https://doi.org/10.5281/zenodo.47881260.

We measured settling velocities for 1,140 synthetic fibres in a recirculating flume. Fibre length and biofilm growth explained most of the variance; the empirical model reproduces the observed deposition patterns in two lowland rivers.

## Repository layout

```
src/            reference implementation
data/           small example inputs and schemas
experiments/    configuration files used for the paper's runs
tests/          smoke tests for the public entry points
```

## Installation

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Quick start

```bash
python -m src.pipeline --config experiments/config.yaml --out results/run01
```

The sample configuration in `experiments/` runs end to end on the bundled
miniature input in under a minute.

## Data availability

The full field data set is archived by the regional monitoring agency.
`data/README.md` documents the schema and the subset that can be redistributed.

## Reproducing the reported results

1. Prepare the environment as above.
2. Run `python -m src.pipeline --config experiments/paper.yaml`.
3. Compare `results/run01/summary.json` with the values in the paper's Table 2.

## Citation

If you use this code, please cite the paper listed in `CITATION.cff`.

## License

MIT. See `LICENSE`.

## Contact

Willowbank Watershed Lab <lab@willowbank-labs.org>
