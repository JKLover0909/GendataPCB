# CLAUDE.md

## Overview
Synthetic PCB defect data generation: paired image-to-image translation (pix2pix / CycleGAN) to generate defective PCB images from normal ones.

## Layout
- `Test.ipynb` — Keras/TensorFlow experiment notebook.
- `Note.txt` — saved pix2pix commands (`train.py`, `test.py`, `prepare_pcb_data.py`) with the PCB dataset arguments.
- `data/train/{A,B}`, `data/test/{A,B}` — sample paired images (A = input, B = target).
- `Khuyetmach2/` — sample defect images (`N.jpg` / `Nx.jpg` pairs).
- `pytorch-CycleGAN-and-pix2pix` — gitlink (submodule-like pointer) to the upstream project; it has no `.gitmodules` entry, so it is empty after a plain clone. Fetch upstream separately: https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix

## Commands
- Train / test: run the commands from `Note.txt` inside a checkout of the upstream pix2pix repo.
- Notebook: `jupyter notebook Test.ipynb`

## Rules
- Do not commit checkpoints, generated results or large datasets (gitignored).
- Keep A/B image pairs aligned and identically named; do not rename files in `data/` or `Khuyetmach2/`.
- Do not "fix" the gitlink without being asked.
