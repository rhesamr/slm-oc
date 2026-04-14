# SLM-Assisted Open Coding with Sliding Windows

This repository contains a Jupyter Notebook workflow for qualitative transcript analysis with locally deployed small language models (SLMs). The workflow has two stages: transcript chunking with a sliding window, and SLM-assisted open coding with output verification.

## Workflow

- **Stage 1:** split `.txt` transcripts into overlapping word-based chunks and save them as CSV files.
- **Stage 2:** read the chunks, run a local SLM through Ollama, extract coding outputs, verify quoted text, and save results.

## Requirements

- Python 3
- Jupyter Notebook or JupyterLab
- Ollama
- Python packages:

```bash
pip install torch tqdm ollama psutil notebook
```

You also need to pull at least one local model in Ollama. Example:

```bash
ollama pull qwen2.5-7b:q4_k_m
```

Optional example:

```bash
ollama pull granite3.1-8b:q4_k_m
```

## Usage

1. Open the notebook.
2. Edit the folder paths and model settings in the configuration cells.
3. Run **Stage 1** to generate chunked transcript CSV files.
4. Run **Stage 2** to generate coding outputs, codebooks, and logs.

## Input and Output

**Input**
- Plain-text interview transcripts (`.txt`)

**Stage 1 output**
- CSV files with chunked transcript windows

**Stage 2 output**
- Coding result files
- Codebook files
- Run logs and summary outputs

## Citation

If you use this repository, please cite:

```bibtex
@inproceedings{ramadhan2025slmopencoding,
  author = {Ramadhan, Rhesa M. and Sushandoyo, Dedy},
  title = {Enabling Qualitative Research with Small Language Models: A Sliding Window Method for Open Coding on Resource-Constrained Hardware},
  booktitle = {2025 International Seminar on Intelligent Technology and Its Applications (ISITIA)},
  year = {2025}
}
```

## License

GNU Affero General Public License v3.0 (AGPL-3.0)

## Author

Rhesa Muhammad Ramadhan  
29024002@mahasiswa.itb.ac.id
