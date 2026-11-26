# Emotion Detection with fine-tuned BERT

A Jupyter notebook that fine-tunes `bert-base-uncased` to classify text into six emotions: anger, fear, joy, love, sadness, and surprise.

## Project files

- `Emotion Detection using fine-tuned BERT.ipynb`: preprocessing, model training, and evaluation workflow.
- `train.txt`, `val.txt`, `test.txt`: labeled examples, one `text;emotion` record per line.
- `requirements.txt`: Python dependencies.

## Run locally

Use Python 3.10 or 3.11. From the repository folder, create and activate a virtual environment, then install the dependencies:

```powershell
py -3.11 -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
python -m notebook
```

Open the notebook in Jupyter and run the cells from top to bottom. The first model run downloads the pretrained BERT tokenizer and weights, so internet access is needed. Fine-tuning can take substantial time and memory; a GPU is recommended. Training saves `emotion_detector.h5` in the working directory; this generated model is ignored by Git.

## Dataset format

Each dataset file is a semicolon-delimited text file without a header. The notebook reads these files from the repository directory. Keep the supplied data files alongside the notebook when running it.

## Push to GitHub

The repository is already configured with an `origin` remote. After reviewing your changes, run:

```powershell
git add .
git commit -m "Prepare project for GitHub"
git push
```

Review `git status` before committing to ensure only intended files are included.
