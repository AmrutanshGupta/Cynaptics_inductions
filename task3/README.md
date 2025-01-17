# GPT-2 Fine-Tuning with LoRA

## Overview
This repository contains scripts and resources for fine-tuning a GPT-2 model using the LoRA (Low-Rank Adaptation) technique. The fine-tuned model is designed to enhance performance on specific downstream tasks while maintaining efficiency.

## Choice of LLM
We have selected **GPT-2** as the base language model due to its:
- Open-source availability.
- Proven capabilities in text generation and completion.
- Moderate size, making it feasible for fine-tuning on limited hardware.
- **Suitability for Persona-Based Applications**: GPT-2 excels at maintaining context and generating responses that align with a given persona, making it ideal for chatbots, storytelling, and other personalized AI applications.

## Choice of Fine-Tuning Method
We employ **LoRA (Low-Rank Adaptation)** for fine-tuning due to the following reasons:
- **Parameter-Efficient Fine-Tuning**: LoRA introduces trainable low-rank matrices instead of updating all parameters, significantly reducing computational cost.
- **Memory Efficiency**: LoRA allows fine-tuning large models on limited GPU resources.
- **Maintaining Pre-Trained Knowledge**: It enables targeted adaptation without catastrophic forgetting of general language abilities.

## Justifications
- **Efficiency**: Fine-tuning GPT-2 with LoRA reduces memory requirements compared to full fine-tuning while achieving competitive results.
- **Flexibility**: LoRA allows task-specific adaptation without modifying the entire model.
- **Scalability**: The approach can be extended to larger models without excessive computational demands.

## Model Weights
The fine-tuned model weights have been uploaded to a public Hugging Face repository and can be accessed at:
[Hugging Face Model Repository](https://wandb.ai/amrutanshgupta-iit-indore/huggingface/runs/750z4m3q?nw=nwuseramrutanshgupta)
