# TinyStories Language Model

A lightweight Transformer-based language model trained on the TinyStories dataset, aimed at generating concise and coherent children's stories. This project showcases the design, training, and deployment of a compact language model for educational and storytelling use cases.

---

## 📚 Overview

**TinyStories** is a synthetic dataset of short stories generated with the help of large language models, curated for training small-scale generative models. Our model is designed to:

* Generate creative and coherent children's stories
* Demonstrate efficient training of transformer models on small datasets
* Serve as a foundation for educational or fine-tuning experiments

---

## 🧠 Model Architecture

* **Model Type:** GPT-like Decoder-only Transformer
* **Layers:** 6
* **Hidden Size:** 256
* **Attention Heads:** 4
* **Vocabulary Size:** 50257 (tokenized using GPT2 tokenizer)
* **Context Length:** 128
* **Parameters:** \~20M

> You can modify these values to match your actual architecture if different.

---

## 💾 Dataset

* **Name:** [TinyStories](https://huggingface.co/datasets/tiny_stories)
* **Source:** HuggingFace Datasets
* **Size:** \~2M  synthetic stories
* **Tokenization:** GPT2 BPE tokenizer
* **Preprocessing:**

  * Lowercased
  * Filtered for length < 128 tokens
  * Removed special characters and HTML tags

---

## 🚀 Training Configuration

* **Framework:** PyTorch / HuggingFace Transformers
* **Batch Size:** 64
* **Learning Rate:** 5e-4 with linear warmup
* **Optimizer:** AdamW
* **Scheduler:** Cosine Annealing
* **Epochs:** 10
* **Hardware:** NVIDIA RTX 3090 (or specify your GPU)

---

## 🧪 Evaluation

* **Perplexity:** \~12.3 on validation set
* **BLEU Score:** 14.7 (optional)
* **Generated Examples:**

```
A little girl went to the woods and she found a basket for her. In one he enjoyed the great basket and the tasty treats tall. Then, she decided to go home and the picnic.

As they walked, the little girl was getting tired and didn't want to drink. She opened her pocket to her room and got out. She was would open their new diary! She had a shower and a hug, so she pulled out a big, feeling warm and warm. She hope even when it was time to eat from the fun to eat!Once upon a time there was a little girl named Abbie. Benny loved to know what powers. Her father argued and walked for a after her. 

When he got there, Katie got excited and started to feel very tired. She said please to the hospital but sometimes he didn't have enough dessert. He sighed and decided to go home.

Bubbles was so happy and didn't like Freddy. He stayed away from the doctor and kept walking.
```

