# misty-models

This repository provides a complete notebook for building two specialized language models for the **Misty robot**:

1. **Emotion Model of Robot Observation  (EMRO-Misty)**  
2. **Generate Robot Emotional Display(GRED-Misty)**

Both the models are trained on emotion-behavior data collected from Misty robot and are designed to classify emotions from robot behaviors and generate new behaviors from given emotion labels. The goal is to enable Misty to generate behavior sequences that reflect specific emotional states.

## Model Details
### Emotion Model of Robot Observation (EMRO-Misty)

**Purpose**: Classify robot behaviors into emotional categories.  
**Base Architecture**: Fine-tuned RoBERTa  
**Inputs**: A text sequence representing Misty robot behaviors
**Outputs**: Emotion predictions  

#### Emotion Classes:

| Class | Emotion Category                       |
|-------|----------------------------------------|
| 0     | Anger / Frustration                    |
| 1     | Interest / Desire                      |
| 2     | Confusion / Sorrow / Boredom           |
| 3     | Joy / Hope                             |
| 4     | Understanding / Gratitude / Relief     |
| 5     | Disgust / Surprise / Alarm / Fear      |

---
    

### 🤖 Generate Robot Emotional Display (GRED-Misty)

**Purpose**: Generate robot behavior sequences conditioned on given emotion labels.  
**Base Architecture**: Fine-tuned GPT-2 Medium  
**Inputs**: Emotion label  
**Outputs**: A text sequence representing Misty robot behaviors


## 📘 What's Included in the Notebook?
The notebook includes:

- ✅ **Data Preprocessing**  
  Cleaning, formatting, and tokenizing emotion-behavior dataset.

- ✅ **Model Training**
  - **EMRO**: A RoBERTa-based emotion classifier fine-tuned to predict one of six grouped emotions from behavior text.
  - **GRED**: A GPT-2-medium-based causal language model trained to generate robot behavior sequences conditioned on emotion labels.

- ✅ **Model Evaluation**
  - EMRO:  Evaluated using accuracy and confusion matrix on test data.
  - GRED: Assessed based on the novelty of generated behaviors and their emotional accuracy (e.g., via EMRO predictions ).

## 🔗 Hugging Face Model Cards
You can explore and use  the finalized models here:
- ** EMRO-Misty (Emotion Classification)**  
  [bsu-slim/emro-misty on Hugging Face](https://huggingface.co/bsu-slim/emro-misty)

- ** GRED-Misty (Behavior Generation)**  
  [bsu-slim/gred-misty on Hugging Face](https://huggingface.co/bsu-slim/gred-misty)

Each model card includes sample usage code and downloadable model files.

