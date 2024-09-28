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

## Model Training
The model is trained using the following steps:
1. Load the GPT-2 tokenizer and model.
2. Use LoRA to adapt the model for text classification.
3. Train the model using the AG News dataset.
4. Evaluate the model on the test set.

The training and evaluation code can be found in `lora_gpt2_training.ipynb`.

## How to Use
1. Clone the repository:
   ```bash
   git clone https://github.com/kkuwaran/LoRA-GPT2-AG-News-Classification.git
   cd LoRA-GPT2-AG-News-Classification
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. ```bash
   7z x lora_gpt2_ag_news/lora_adapter/adapter_model.7z -o lora_gpt2_ag_news/lora_adapter/
   ```
4. Open and run the Jupyter notebook `lora_gpt2_training.ipynb` for training and evaluation.

## Model Saving
The fine-tuned model, including LoRA weights and score weights, are saved in the `lora_gpt2_ag_news/` directory for future use. To load the model, follow the steps provided in the notebook.

### Note on Model File Compression
The original model file, `adapter_model.safetensors`, exceeded GitHub's file size limit. To resolve this, the model has been compressed into `adapter_model.7z`. You will need to extract this file before using the model. The compressed file can be found in the `lora_gpt2_ag_news/lora_adapter/` directory.

## Performance Comparison
After training, you can compare the performance of the original GPT-2 model and the LoRA fine-tuned model in terms of accuracy and loss on the test set.
