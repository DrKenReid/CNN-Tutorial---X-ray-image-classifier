# Contributing to CNN Tutorial — X-ray Image Classifier

Thanks for your interest! Here's how to help.

## Ways to Contribute

- **Report bugs**: Something not running in Colab? Open an issue.
- **Suggest improvements**: Better models, visualizations, or techniques.
- **Fix issues**: Check the [Issues](https://github.com/DrKenReid/CNN-Tutorial---X-ray-image-classifier/issues) tab.
- **Improve docs**: Clarify explanations, fix typos, add examples.

## Setup

This project runs in Google Colab — no local setup required:

1. Open the notebook in Colab via the link in the README
2. Run all cells
3. Make your changes

For local development (advanced): the notebook is written Colab-first — it mounts Google Drive and stores data under `/content/`. The Colab-specific cells skip gracefully outside Colab, but you will need a Kaggle API token (the setup cell prompts for it and stores it at `~/.kaggle/access_token`) and to adjust the dataset and model-save paths before running:

```bash
git clone https://github.com/DrKenReid/CNN-Tutorial---X-ray-image-classifier.git
pip install -r requirements.txt
jupyter notebook
```

## PR Guidelines

- Keep notebooks clean — restart kernel and run all before committing.
- Clear output cells to keep diffs readable.
- Add markdown cells explaining new sections.
- Don't commit API keys or credentials.
