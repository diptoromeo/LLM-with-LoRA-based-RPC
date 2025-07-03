# 🦙 LLaMA 3 + LoRA Fine-Tuning for RPC(Research Paper Classification)
This repository contains a Google Colab-compatible notebook demonstrating how to fine-tune the Meta LLaMA 3 model using LoRA (Low-Rank Adaptation) with Hugging Face's transformers, peft, and trl libraries. It also shows how to generate responses from the fine-tuned model and save/load adapter weights.

# 🚀 Key Features
✅ Loads the 8B parameter meta-llama/Meta-Llama-3-8B-Instruct model using transformers.

✅ Applies parameter-efficient fine-tuning via LoRA using the PEFT library.

✅ Uses a custom small dataset to train the model on prompt-response pairs.

✅ Demonstrates LoRA adapter saving and loading.

✅ Generates output responses after fine-tuning.

# 🛠️ Requirements
Install required packages:

pip install transformers accelerate peft trl bitsandbytes

You will also need:
A Hugging Face token with access to meta-llama/Meta-Llama-3-8B-Instruct

GPU support (preferably T4 or better)

# 📂 Notebook Structure
Section	Description
1. Setup	Load libraries, define LoRA and training configuration.
2. Dataset	Defines a small set of prompt-response training pairs.
3. Model Loading	Loads the base LLaMA-3 model in 4-bit precision.
4. LoRA Injection	Applies LoRA to q_proj, v_proj, and gate_proj layers.
5. Training	Trains with the SFTTrainer on the toy dataset.
6. Inference	Uses the fine-tuned model for generating responses.
7. Save/Reload	Saves and loads the LoRA adapters.

# 🧪 Example
prompt = "What are the advantages of solar energy?"

response = model.generate(prompt)

print(response)

# 💡 Tips
You can modify the dataset list in the notebook to include your custom domain-specific prompts.

For large datasets, consider switching from in-notebook definition to dataset loading via Hugging Face Datasets.

#📎 References
Meta AI: LLaMA 3

PEFT Library

Transformers Library

TRL (Transformers Reinforcement Learning)
