# Hidden Markov Models for Bioinformatics

Two notebooks exploring hidden Markov models for biological sequence analysis.

## Included studies

- `periodic_patterns_exons_introns.ipynb`: IID, Markov, periodic, and flexible-wheel models for nucleotide periodicity in exon/intron sequences, including validation, bootstrap, and model comparison.
- `gene_finding_hmm_tutorial_vi.ipynb`: a Vietnamese tutorial implementing synthetic gene finding, Viterbi decoding, and sequence-label evaluation.

## Result snapshots

The periodicity study selected a period-10 model and reports an improvement of 0.116432 NLL/nt over the IID baseline on its evaluation setup. The tutorial records F1 scores of approximately 0.978 for coding, 0.971 for intergenic, 0.942 for intron, and 0.877 for splice-signal labels.

The results depend on the downloaded sequence sources and synthetic-data configuration. Raw genomic data and generated outputs are intentionally not committed.

## Reproduce

Open the notebooks in Jupyter and follow the data-download cells. The periodicity notebook may require `pyfaidx` and common scientific Python packages:

```bash
python -m pip install jupyter numpy pandas scipy scikit-learn matplotlib pyfaidx
```
