# CardioGPT
CardioGPT: A Transformer-Based Approach to Convert Tabular EHR into Clinical Narratives for Prompting a Heart Disease Expert GPT Model

In this study, heart patient data from the UCI dataset has been used, which was in a table format. But Large Language Models (LLMs), like GPT, work best with text — not tables. So, we faced two big challenges: the data was tabular, and the classes (healthy to severe heart disease) were imbalanced.

Traditionally, it’s not reliable to generate synthetic data for class imbalance correction when the features are categorical. Techniques like SMOTE, ADAYSN, and ENN work well for numeric data but struggle with categorical data — especially in medical datasets, where each category has a specific clinical meaning. So, creating synthetic data in text format, with a clear understanding of its medical value, is necessary.

To solve this, we used a table-to-text method by fine-tuning a GPT model that turned the table data into clinical text. Then, we used a clinical text generative model (MedGPT) to create more realistic examples for the underrepresented heart disease classes.

Finally, we used prompting — giving short medical texts from new patients to a trained GPT model — to see if it could predict heart disease severity.

All the GPT models used in this project were implemented using Hugging Face libraries and pre-trained models.

This project demonstrates how LLMs can be creatively applied to transform tabular data into meaningful medical texts and equip a GPT model with specialized knowledge in heart disease, even when working with imbalanced data.

**Initial Dataset:**
![image](https://github.com/user-attachments/assets/2c5b4042-ad77-456e-83c2-7f45bce0a223)

**After conversion to text:**
![image](https://github.com/user-attachments/assets/36e9a8de-7a93-4ac1-99d3-dfc3779a19b4)

**After training the model:**
![image](https://github.com/user-attachments/assets/d348d8f1-36dc-4c66-a76f-d2404355f316)

**Keywords:**
1. Large Language Models (LLMs)

2. Table-to-Text Conversion

3. Clinical Text Generation

4. Class Imbalance

5. Prompt-based Prediction
