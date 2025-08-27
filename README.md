# ClarinetNet

This project was done for my bachelor thesis project in 2025. It features a clarinet specific dataset that can be used for training AI models that focus on Automatic Music Transcription (AMT). This study was done as a pilot study so as to proof a concept of the feasibility of single-instrument datasets outperforming multi-instrument datasets.

## Installation and Setup

1. Clone repo
2. Install python 3.10 (deps cannot run on newer)
3. Create venv with py 3.10: `py -3.10 -m venv .venv`
4. Install deps: `pip install -r ./unaligned-supervision-master/requirements.txt`
5. Install [SOX](https://sourceforge.net/projects/sox/)
6. Run the file: `python ./unaligned-supervision-master/make_pitch_shifted_copies.py`
7. Run the file: `python ./unaligned-supervision-master/make_parsed_tsv_from_midi.py`
8. Make sure the numpy version is below 2.0, if needed: `pip uninstall numpy && pip install numpy<2.0`
9. To enable GPU support, install pytorch with cuda
10. CUDA setup:
    - Check version with `nvcc --version`
    - Find the correct version (here)[https://pytorch.org/get-started/locally/]
11. Run `python ./unaligned-supervision-master/train.py`
12. Run `python ./unaligned-supervision-master/test.py` (change directory path in code to correct transcriber model)