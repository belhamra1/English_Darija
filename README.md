# Project Title

**Project Title**: Question and Answer Generation using LLMs with Translation and Fine-Tuning

## Overview

This project demonstrates a pipeline for generating and translating questions and answers using large language models (LLMs). It includes both the data extraction and fine-tuning code needed to create a chatbot that answers queries in Darija. Additionally, the project incorporates a translation mechanism to handle English-Darija translations, enabling a more flexible chatbot experience.

## Folder Structure

- **Extraction Code + Extracted Q&A Documents**: This folder contains:
  - **Data**: Q&A documents with questions and answers extracted from various sources.
  - **Extraction Code**: Code used to extract and structure Q&A data. The data serves as the basis for the fine-tuning process, preparing the model for effective response generation.

- **finetunning_chatbot.ipynb**: This Jupyter Notebook covers:
  - **Fine-Tuning**: Step-by-step code for fine-tuning an initial LLM to generate answers specific to our Q&A dataset.
  - **Translation Integration**: Importation and integration of a separate model to handle translations between English and Darija.
    - The fine-tuned LLM generates answers in English.
    - The translation model converts answers from English to Darija to create responses suited for Darija-speaking users.
  - **User Interface**: Code for a simple user interface (chatbot) at the end of the notebook, allowing users to interact directly with the model.

## Usage

1. **Data Extraction**:
   - Run the scripts in the **Extraction Code + Extracted Q&A Documents** folder to create a structured dataset for Q&A.

2. **Fine-Tuning**:
   - Open `finetunning_chatbot.ipynb` and run the cells to fine-tune the LLM on the extracted Q&A data.

3. **Translation and Response Generation**:
   - The notebook imports a separate model specifically for translating from Darija to English.
   - After generating responses in English, it then uses the translation model to convert these responses back into Darija.

4. **Chatbot Interface**:
   - At the end of the notebook, a simple chatbot interface is provided, allowing users to interact with the fine-tuned and translated model.


![image](https://github.com/user-attachments/assets/72c1247e-251a-4812-acf9-66e810c83ddc)





## Requirements

Ensure the following Python libraries are installed:
- `transformers` for handling LLMs
- `torch` for PyTorch models
- `gradio` (or similar) for the chatbot interface

Install dependencies with:
```bash
pip install transformers torch gradio
