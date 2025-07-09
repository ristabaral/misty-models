# misty-models

This repository provides a complete notebook pipeline for building two specialized language models for the **Misty robot**:

1. **Emotion Model of Robot Observation  (EMRO-Misty)**  
2. **Generate Robot Emotional Display(GRED-Misty)**

Both the models are trained on emotion-behavior data collected from Misty robot and are designed to classify emotions from robot behaviors and generate new behaviors from given emotion labels. The goal is to enable Misty to generate behavior sequences that reflect specific emotional states.

## 📘 What's Included in the Notebook?
The notebook includes:

- ✅ **Data Preprocessing**  
  Cleaning, formatting, and tokenizing emotion-behavior dataset.

- ✅ **Model Training**
  - **EMRO**: A RoBERTa-based emotion classifier fine-tuned to predict one of six grouped emotions from behavior text.
  - **GRED**: A GPT-2-medium-based causal language model trained to generate robot behavior sequences conditioned on emotion labels.

- ✅ **Model Evaluation**
  - EMRO:  Evaluated using ccuracy and confusion matrix on test data.
  - GRED: Assessed based on the novelty of generated behaviors and their emotional accuracy (e.g., via EMRO predictions ).

## 🔗 Hugging Face Model Cards
You can explore and use  the finalized models here:
- ** EMRO-Misty (Emotion Classification)**  
  [bsu-slim/emro-misty on Hugging Face](https://huggingface.co/bsu-slim/emro-misty)

- ** GRED-Misty (Behavior Generation)**  
  [bsu-slim/gred-misty on Hugging Face](https://huggingface.co/bsu-slim/gred-misty)

Each model card includes sample usage code and downloadable model files.

