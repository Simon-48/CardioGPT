# CardioGPT
CardioGPT: A Transformer-Based Approach to Convert Tabular EHR into Clinical Narratives for Prompting a Heart Disease Expert GPT Model

In this study, heart patient data from the UCI dataset has been used, which was in a table format. But Large Language Models (LLMs), like GPT, work best with text — not tables. So, we faced two big challenges: the data was tabular, and the classes (healthy to severe heart disease) were imbalanced.

Traditionally, it’s not reliable to generate synthetic data for class imbalance correction when the features are categorical. Techniques like SMOTE, ADAYSN, and ENN work well for numeric data but struggle with categorical data — especially in medical datasets, where each category has a specific clinical meaning. So, creating synthetic data in text format, with a clear understanding of its medical value, is necessary.

To solve this, we used a table-to-text method by fine-tuning a GPT model that turned the table data into clinical text. Then, we used a clinical text generative model (MedGPT) to create more realistic examples for the underrepresented heart disease classes.

Finally, we used prompting — giving short medical texts from new patients to a trained GPT model — to see if it could predict heart disease severity.

All the GPT models used in this project were implemented using Hugging Face libraries and pre-trained models.

This project demonstrates how LLMs can be creatively applied to transform tabular data into meaningful medical texts and equip a GPT model with specialized knowledge in heart disease, even when working with imbalanced data.

**Initial Dataset:**
![image](https://github.com/user-attachments/assets/94080208-65d8-4fa0-842f-7a17dd5d1de8)

**After conversion to text:**
![image](https://github.com/user-attachments/assets/4728dc42-61fa-469d-b7f0-7cd6bd46e537)

**After training the model:**
![image](https://github.com/user-attachments/assets/4a937cc1-8551-46fc-b97a-b6e2bb4013d2)

**Keywords:**
1. Large Language Models (LLMs)

2. Table-to-Text Conversion

3. Clinical Text Generation

4. Class Imbalance

5. Prompt-based Prediction
