# Mental Health Assistance

This project presents an empathetic conversational AI chatbot built to provide preliminary mental health support. It uses the Mistral-7B-Instruct-v0.2 language model, fine-tuned with QLoRA on real therapist-client dialogues. The chatbot is capable of holding context-aware conversations and responding with emotional sensitivity.

## Project Overview

The goal is to make mental health support more accessible through a scalable AI-powered chatbot. While not a substitute for professional therapy, it serves as a confidential and supportive first contact for individuals experiencing emotional distress.

## Features

* Multi-turn, context-aware conversations
* Emotionally sensitive and supportive responses
* Fine-tuned on real counselor-patient dialogue
* Memory-efficient 4-bit quantized model (QLoRA)
* Lightweight training via TF32 and PEFT

## Key Tools Used

* PyTorch
* Transformers
* PEFT (QLoRA)
* Mistral-7B-Instruct-v0.2
* Mixed Precision Training (TF32)
* Datasets
* Tokenizers

## Dataset

* Source: [mental\_health\_counseling\_conversations (Hugging Face)](https://huggingface.co/datasets/Amod/mental_health_counseling_conversations)
* Description: A curated set of anonymized therapist-client question–response pairs sourced from online therapy platforms.
* Language: English

## Training Configuration

* Epochs: 3
* Learning Rate: 1e-4
* Optimizer: Paged AdamW (8-bit)
* Batch Size: 4
* Scheduler: Constant LR with warmup ratio of 0.03
* Mixed Precision: TF32
* Max Gradient Norm: 0.3
* Evaluation: End of each epoch
* Logging: Every 10 steps

## Results

* Final Validation Loss: 0.6432
* Demonstrated strong fluency and contextual consistency
* Empathetic tone improved compared to base model

## Limitations

* Not designed for emergency or crisis response
* May miss subtle emotional cues or complex conditions
* Not intended to replace licensed mental health professionals

## How to Use

1. Clone the repository
2. Install dependencies: Transformers, PEFT, Datasets, PyTorch
3. Load the fine-tuned model (see /outputs folder)
4. Run the chatbot interaction script from a terminal or notebook
5. Extend or integrate with a UI for production deployment

## Model Trained (Huggingface link)

[https://huggingface.co/sridevisundar21/MentalHealthAssistant/tree/main](https://huggingface.co/sridevisundar21/MentalHealthAssistant/tree/main)

## License

This project is intended for educational and research purposes only. For real mental health support, please consult a qualified professional.
