Arabic T5 — Arabic News Classification

<p align="center">
  <strong>A Large-Scale Arabic Natural Language Processing Project</strong>
</p><p align="center">
  <em>Dataset Engineering · Arabic NLP · Custom Tokenizer · Transformer Fine-Tuning · Text Classification</em>
</p>---

Overview

Arabic T5 is an Arabic Natural Language Processing (NLP) project focused on building a multi-level news classification system using a Text-to-Text Transformer architecture.

The project processes Arabic news articles and generates structured classification outputs, including:

- Main Category: Identifies the general topic of an article.
- Subcategory: Provides a more specific classification within the main category.
- Country: Identifies the country associated with the article.

The development workflow covers large-scale dataset preparation, Arabic text preprocessing, custom tokenizer development, model fine-tuning, and evaluation.

The project aims to explore how Transformer-based language models can be adapted to structured Arabic news understanding tasks.

Key Features

- Large-scale Arabic news dataset preparation.
- Processing of more than 270K news records.
- Arabic text cleaning and preprocessing.
- Custom tokenizer development.
- T5-based sequence-to-sequence model fine-tuning.
- Multi-level Arabic news classification.
- Separate training, validation, and testing datasets.
- Structured text generation for classification outputs.

Dataset

The dataset was collected from Al Ain News and prepared specifically for this project.

Dataset Statistics

Stage| Records
Initially collected| 270,560
After preprocessing| 270,107
Training set| 189,074
Validation set| 40,516
Test set| 40,517

Dataset Preparation

The data preparation pipeline includes:

1. Collecting news records.
2. Organizing the collected data.
3. Cleaning and preprocessing Arabic text.
4. Preparing the classification information.
5. Splitting the processed dataset into training, validation, and testing sets.

«The original dataset is not included in this repository.»

Methodology

The project consists of several development stages.

1. Data Collection

News records were collected from Al Ain News through a set of data collection notebooks.

The collection stage established the raw dataset used in subsequent processing stages.

2. Data Preprocessing

The collected records were cleaned and prepared for model development.

This stage produced the processed dataset used in the tokenizer and model training workflows.

3. Custom Tokenizer Development

A custom tokenizer was developed as part of the project.

The tokenizer vocabulary was designed for the Arabic text-processing workflow.

Vocabulary size: 35,003 tokens, including special tokens.

This component represents a dedicated tokenizer-development effort within the project.

4. Model Architecture

The project uses the Text-to-Text Transfer Transformer (T5) architecture.

The base checkpoint used is:

"bakrianoo/t5-arabic-base"

T5 follows an encoder-decoder architecture that formulates NLP tasks as text-to-text transformations.

This allows the classification task to be represented as generating structured textual outputs rather than relying only on conventional classification heads.

5. Model Fine-Tuning

The base model is adapted to the Arabic news classification task using the prepared dataset.

The training workflow includes:

- Preparing model inputs and target outputs.
- Loading the base T5 checkpoint.
- Configuring the training process.
- Fine-tuning on the training dataset.
- Monitoring development using the validation dataset.

6. Model Evaluation

A separate test dataset is maintained for evaluating the trained model.

The evaluation stage is intended to examine classification quality and the consistency of generated outputs.

Quantitative performance metrics will be documented when the final verified evaluation results are available.

Dataset Split

The processed dataset was divided as follows:

Split| Number of Records| Percentage
Training| 189,074| 70%
Validation| 40,516| 15%
Testing| 40,517| 15%
Total| 270,107| 100%


Project Screenshots

<p align="center">
  <img src="assets/%D9%84%D9%82%D8%B7%D8%A9%20%D8%B4%D8%A7%D8%B4%D8%A9%202026-10-29%20154621.png" width="90%" alt="Arabic T5 Screenshot 1">
</p><p align="center">
  <img src="assets/%D9%84%D9%82%D8%B7%D8%A9%20%D8%B4%D8%A7%D8%B4%D8%A9%202026-10-29%20154831.png" width="90%" alt="Arabic T5 Screenshot 2">
</p><p align="center">
  <img src="assets/%D9%84%D9%82%D8%B7%D8%A9%20%D8%B4%D8%A7%D8%B4%D8%A9%202026-10-29%20155721.png" width="90%" alt="Arabic T5 Screenshot 3">
</p><p align="center">
  <img src="assets/%D9%84%D9%82%D8%B7%D8%A9%20%D8%B4%D8%A7%D8%B4%D8%A9%202026-10-29%20155924.png" width="90%" alt="Arabic T5 Screenshot 4">
</p>

Project Workflow

       Al Ain News
            |
            v
      Data Collection
            |
            v
     Raw News Dataset
            |
            v
    Data Preprocessing
            |
            v
   Processed Dataset
            |
            v
   Custom Tokenizer
            |
            v
      Dataset Split
            |
            v
    T5 Model Fine-tuning
            |
            v
      Model Evaluation
            |
            v
  Structured Classification

Repository Structure

arabic-t5-news-classification/
│
├── README.md
├── .gitignore
├── requirements.txt
├── CONTRIBUTING.md
│
├── assets/
│
└── notebooks/
    └── data_collection/
        ├── collection_notebook_1.ipynb
        ├── collection_notebook_2.ipynb
        ├── collection_notebook_3.ipynb
        ├── collection_notebook_4.ipynb
        └── collection_notebook_5.ipynb

The repository is being organized to document the complete development workflow. Additional directories for preprocessing, tokenizer development, and model training will be added as the project files are organized.

Technologies & Tools

Technology| Purpose
Python| Main programming language
PyTorch| Deep learning framework
Hugging Face Transformers| Transformer model implementation
T5| Encoder-decoder architecture
Tokenizers| Tokenization development
SentencePiece| Tokenization ecosystem
NumPy| Numerical operations
Pandas| Dataset processing
Scikit-learn| Data splitting and evaluation utilities
Jupyter Notebook| Experimentation and development
Google Colab| Development environment

Installation

Clone the repository:

git clone https://github.com/esmailemrany/arabic-t5-news-classification.git

Move into the project directory:

cd arabic-t5-news-classification

Install the required dependencies:

pip install -r requirements.txt

«The notebooks may require access to the prepared dataset and the corresponding model and tokenizer files. These resources must be available before reproducing the complete training workflow.»

Reproducibility

The project notebooks document the development and experimentation process.

Reproducing the complete workflow requires:

- The prepared Arabic news dataset.
- The required Python dependencies.
- The appropriate base model checkpoint.
- The tokenizer files used by the training workflow.
- The training configuration and saved model artifacts, where applicable.

The original collected dataset is not distributed with this repository.

Limitations and Future Work

Potential future improvements include:

- Publishing a complete model evaluation report.
- Performing detailed classification error analysis.
- Testing generalization on news from additional Arabic sources.
- Improving classification consistency across overlapping categories.
- Optimizing inference performance.
- Preparing a reproducible inference interface.
- Publishing model and tokenizer artifacts with appropriate documentation.

Acknowledgments

This project uses the publicly available Arabic T5 checkpoint:

"bakrianoo/t5-arabic-base"

Credit for the original checkpoint and its authors is retained.

Author

Esmail Emrany

AI & Data Science Student

GitHub: "@esmailemrany" (https://github.com/esmailemrany)

---

<p align="center">
  <strong>Arabic Natural Language Processing · Transformer Models · Text Classification</strong>
</p>
