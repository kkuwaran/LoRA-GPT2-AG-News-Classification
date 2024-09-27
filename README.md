# LoRA-GPT2-AG-News-Classification

This repository contains the implementation of a GPT-2 model fine-tuned using Low-Rank Adaptation (LoRA) on the AG News dataset for news article classification. The categories for classification are:
- World
- Sports
- Business
- Sci/Tech

## Features
- Use of the LoRA technique to adapt GPT-2 for sequence classification tasks.
- Efficient training with smaller memory footprints using LoRA.
- Training and evaluation of the model on the AG News dataset using Hugging Face Transformers.
- LoRA configuration focused on attention modules for adaptation.

## Dataset
We use the AG News dataset available from Hugging Face's datasets library:
- [AG News](https://huggingface.co/datasets/fancyzhx/ag_news)
  
The dataset contains 120,000 training and 7,600 test samples classified into four categories.

## Dependencies
Make sure to install all dependencies before running the notebook. The required packages are listed in `requirements.txt`. You can install them using:

```bash
pip install -r requirements.txt
