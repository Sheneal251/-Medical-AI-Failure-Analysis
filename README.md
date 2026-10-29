# Medical AI Failure Analysis

## Project Overview

This project evaluates how accurately Qwen2.5-1.5B-Instruct answers medical questions and identifies situations where it generates incorrect or potentially unsafe information. I used the MedQuAD dataset to compare AI-generated responses with reference medical answers.

The analysis focuses on two types of failures: incorrect genetic inheritance information and inappropriate medical procedure recommendations.

## Tools and Technologies

- Python
- Google Colab
- Hugging Face Transformers
- Qwen2.5-1.5B-Instruct
- Pandas
- MedQuAD Dataset

## Methodology

I started by loading and cleaning the MedQuAD dataset, checking for missing values and duplicate records. I then randomly selected 30 medical questions and generated answers using Qwen2.5-1.5B-Instruct.

I compared the generated responses with the reference answers to identify medical inaccuracies. After finding errors, I tested different versions of selected questions to examine how question wording affected the model's responses.

## Key Findings

**1. Genetic Inheritance Errors**

The model correctly identified galactosialidosis as an autosomal recessive condition but later introduced incorrect X-linked inheritance information. Shorter follow-up questions produced correct answers.

**2. Incorrect Medical Procedure Recommendations**

When asked about cardiac tamponade, the model sometimes recommended paracentesis instead of pericardiocentesis.

I tested five variations of cardiac tamponade questions. One response correctly identified the procedure, two were partially correct, and two contained incorrect or potentially unsafe information.

## Limitations

This was a small exploratory analysis involving 30 initial questions and additional targeted tests. The findings highlight specific failures rather than the model's overall medical accuracy.

## Conclusion

This project showed that an AI model can provide correct medical information while also introducing misleading details. It also demonstrated how question phrasing can affect the reliability of generated answers.

The findings highlight the importance of evaluating AI-generated medical information carefully, especially when accuracy and patient safety are involved.
