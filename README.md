# Hidden Markov Models: Bioinformatics and Saga

A practical HMM portfolio covering the core algorithms and two application tracks: biological sequence modeling and the Saga project exercises.

## Repository map

### `notebooks/saga/`

Step-by-step implementations of:

- sequence likelihood with the forward algorithm;
- Viterbi decoding and backpointers;
- forward–backward quantities;
- Baum–Welch-style parameter updates and HMM training;
- a compact end-to-end HMM implementation.

### `notebooks/bioinformatics/`

Research-style notebooks for:

- periodic nucleotide patterns in exon/intron sequences;
- synthetic gene finding with HMMs and Viterbi decoding.

## Result snapshots

The bioinformatics work selected a period-10 model and reported a 0.116432 NLL/nt improvement over an IID baseline in its evaluation setup. The gene-finding tutorial recorded F1 scores of approximately 0.978 for coding, 0.971 for intergenic, 0.942 for intron, and 0.877 for splice-signal labels.

The Saga notebooks use a small weather-style toy sequence to make each dynamic-programming step inspectable. Their purpose is algorithmic clarity and transfer to the Saga task, not a production benchmark.

## Reproduce

```bash
python -m pip install jupyter numpy pandas scipy scikit-learn matplotlib pyfaidx
```

Open the notebooks in Jupyter or Google Colab. The bioinformatics notebooks may download sequence data on demand; raw genomic data and generated outputs are intentionally not committed.
