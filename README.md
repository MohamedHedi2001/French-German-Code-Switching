# French-German Code-Switching

This project investigates French-German code-switching using multilingual NLP models. The project covers dataset construction, conversational data classification, synthetic code-switched data generation, data augmentation, language classification, and translation comparison.

## Project Structure

```text
french-german-code-switching/
├── notebooks/
│   ├── 01_dataset_building.ipynb
│   ├── 02_dataset_preparation.ipynb
│   ├── 03_augmentation.ipynb
│   ├── 04_code_switching_classifier_finetuning.ipynb
│   ├── 05_Binary_Classifier.ipynb
│   └── 06_deepl_translation_comparison.ipynb
├── README.md
└── requirements.txt
```

## Notebooks

1. **Dataset Building**
   Cleans the OpenSubtitles data and performs Chat/Non-Chat classification using zero-shot classification and fine-tuned language-specific classifiers.

2. **Dataset Preparation**
   Constructs the final French-German dataset, including natural and synthetically generated code-switched examples.

3. **Augmentation**
   Applies language-specific transformations to introduce informal variations into the training, validation, and test data.

4. **Code-Switching Classifier Fine-Tuning**
   Fine-tunes XLM-RoBERTa for three-class classification: French, German, and Mixed.

5. **Binary Classifier**
   Fine-tunes XLM-RoBERTa to distinguish between Monolingual and Code-Switched sentences.

6. **DeepL Translation Comparison**
   Compares direct DeepL translation, segmentation-based DeepL translation, and Gemini using manual evaluation and statistical analysis.

## Data Sources

* **OpenSubtitles / OPUS** — German and French subtitle data.
* **SwitchLingua** — naturally occurring French-German code-switched data.

The datasets themselves are not included in this repository.

## Models

The project uses several multilingual NLP models, including:

* XLM-RoBERTa
* DistilBERT multilingual
* mDeBERTa
* Sentence Transformers

## Installation

Clone the repository and install the required dependencies:

```bash
pip install -r requirements.txt
```

The notebooks were developed in Google Colab and may require adapting file paths when run locally.

## API Key

The translation notebook requires a DeepL API key and may require a Gemini API key.

API keys are **not included in this repository**. Before running the translation notebook, provide your own keys in the corresponding variables.

Never commit API keys, passwords, or other credentials to the repository.

## License

This project is licensed under the MIT License.

