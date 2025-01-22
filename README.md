# Llama_fine-tunig

This project focuses on fine-tuning a language model using a subset of a dataset and validating the model's performance using BLEU scores. 
---

## Tasks Overview

### Fine-Tuning
1. **Model Selection**:
   - Replace `gemma-2b` with `meta-llama/Llama-3.2-1B-Instruct` as the model for fine-tuning.
   
2. **Dataset Usage**:
   - Use 2,800 samples from the dataset for fine-tuning.
   - Reserve the remaining 200 samples for validation purposes.

3. **Hugging Face Hub**:
   - Upload the fine-tuned LoRA adapter to the Hugging Face Hub.
   - Record the model ID upon successful upload.

### Validation
4. **Adapter Loading**:
   - Load the uploaded adapter model directly from the Hugging Face Hub.

5. **Evaluation**:
   - Measure the BLEU score for each output in the validation set.
   - Compare the generated outputs against the validation set using the `sacrebleu` library.

## Requirements
- Python 3.8 or later
- Hugging Face Transformers library
- `sacrebleu` for BLEU score evaluation
