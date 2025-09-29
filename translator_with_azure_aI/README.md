# PDF Translator with Azure AI

This project implements a **PDF translator** using **Azure AI Services Translator**. It was developed to **translate PDF documents** automatically into a target language and save the results as Word `.docx` files.

## Features
- **PDF Translation**
  - Reads PDF files page by page.
  - Translates content using **Azure Translator API**.
  - Saves translated content into Word `.docx` files with the language code appended.
- **Batch Processing**
  - Supports processing multiple PDFs from a folder.
  - Automatically detects all PDF files in the specified directory.
- **Custom Target Language**
  - Allows setting the desired target language (e.g., `'pt-br'`, `'en'`).

## How to use

1. Clone the repository:

```bash
git clone https://github.com/JessicaArauj/Azure_AI_Pojects
```

2. Navigate to the project folder:

```bash
cd translator_with_azure_ai
```

3. Set your `.env` file with your Azure credentials:

```env
SUBSCRIPTION_KEY= "your_subscription_key"
ENDPOINT= "https://api.cognitive.microsofttranslator.com"
LOCATION= "your_resource_location"
```

4. Open the Jupyter Notebook and run the code step by step.

## Installation

Install required dependencies:

```python
!pip install -q --upgrade requests
!pip install -q --upgrade PyPDF2
!pip install -q --upgrade python-dotenv
```

## Main Structure

- **Configuration**: Loads environment variables from `.env`.
- **Translator Function**: Calls Azure Translator API to translate text.
- **PDF Processing**: Reads PDFs page by page using `PyPDF2`.
- **Word Export**: Saves translated content into `.docx` files using `python-docx`.
- **Batch Processing**: Loops through all PDFs in a folder to translate them automatically.

## Example Usage

```python
translate_document("example.pdf", "pt-br")

translate_all_pdfs(".", "pt-br")
```

## Notes

- Requires an active Azure Translator subscription.
- Make sure your `.env` file contains valid keys and endpoint.
- The translation quality depends on the content and formatting of the PDF files.

## License

This project is licensed under the **MIT License**. You are free to use, modify, and distribute it as needed.
