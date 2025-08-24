# Stoic-Sage
Fine-tuning of an LLM into a Stoic philosopher chatbot. The AI is trained on a custom dataset of Stoic dialogues to provide wise, reasoned advice in the style of philosophers like Marcus Aurelius, Seneca, and Epictetus.

This project fine-tunes the `unsloth/llama-3.1-8b-bnb-4bit` model to emulate a Stoic philosopher. Using a custom dataset of Stoic principles and dialogues, the model is trained to provide wise, reasoned, and calming advice in the style of ancient Stoics like Marcus Aurelius, Seneca, and Epictetus.

The project leverages the power of LoRA (Low-Rank Adaptation) for efficient fine-tuning, making it possible to adapt an 8B parameter model for a specialized task.

### Live Models & Datasets

* **Fine-Tuned Model**: [AlbertoB12/Stoicism2_Llama3.1-8b-lora on Hugging Face](https://huggingface.co/AlbertoB12/Stoicism2_Llama3.1-8b-lora)
* **Dataset**: [AlbertoB12/Stoicism2 on Hugging Face](https://huggingface.co/datasets/AlbertoB12/Stoicism2)

## Overview

The goal was to create an AI that can answer questions and provide guidance from a Stoic perspective. The model was fine-tuned on the `AlbertoB12/Stoicism2` dataset, which contains 1,040 prompt-response pairs covering various aspects of Stoic philosophy. The `unsloth` library was used to significantly speed up the training process and reduce memory usage.

## Model & Dataset Details

* **Base Model**: `unsloth/llama-3.1-8b-bnb-4bit`
* **Fine-Tuning Technique**: LoRA with 4-bit quantization.
* **Dataset**: The `AlbertoB12/Stoicism2` dataset is a collection of question-and-answer pairs designed for instruction fine-tuning. Each entry consists of a user `prompt` and a detailed `response` from a Stoic viewpoint.

### Prompt Format

The model was trained using the ChatML prompt format. To get the best results, your prompts should follow this structure:

```
<|start_header_id|>user<|end_header_id|>

{Your Question Here}<|eot_id|><|start_header_id|>assistant<|end_header_id|>

```

## Getting Started

### Example

**Prompt:**
"How can I deal with my anger in a Stoic way?"

**Model Response:**
To deal with anger in a Stoic way, you must first understand its nature. The Stoics viewed anger not as an uncontrollable force, but as a product of our judgments. It arises when we believe that we have been wronged or that things are not as they should be. This judgment is a product of our reason, and as such, it is within our power to change it.

Here is a path to follow:

1.  **Recognize the First Movement**: When you feel the initial flush of anger—the racing heart, the tensed muscles—recognize it for what it is: a 'first movement.' This is a natural, physiological reaction and is not yet the emotion of anger itself. It is not shameful, but it is a signal to be mindful.

2.  **Withhold Assent**: The crucial step is to not assent to the judgment that fuels the anger. Do not immediately agree with the thought, 'I have been wronged, and this is terrible.' Instead, create a space between the stimulus and your response. As Epictetus would say, "Do not be carried away by the appearance."

3.  **Examine Your Judgments**: Question the thoughts that give rise to your anger. Ask yourself: Is this event truly harmful to my character, which is the only thing that is truly mine? Is the person who angered me acting out of malice, or out of ignorance? Remember the words of Marcus Aurelius: "People exist for the sake of one another. Teach them then, or bear with them." Often, others do not act to harm us, but because they do not know any better.


This project is licensed under the MIT License.
