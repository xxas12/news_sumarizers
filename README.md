# News Article Summarizer and Urdu Text-to-Speech

This project provides a user-friendly interface for summarizing news articles and translating them into Urdu, along with generating an audio output of the Urdu translation.

## Technologies Used

* **Python:** The core programming language for building the application.
* **Gradio:** Used to create a web-based user interface for interaction.
* **Transformers:** A library from Hugging Face that provides pre-trained models for tasks like text summarization and translation.
* **Pegasus:** A transformer-based model used for abstractive text summarization.
* **M2M100:** A multilingual machine translation model for converting English to Urdu.
* **Newspaper3k:** A library for extracting articles from URLs.
* **Edge TTS:** Used for generating speech from text in Urdu.
* **SentencePiece:** A library for subword tokenization, essential for working with multilingual models.
* **Sacremoses:** A library for tokenization and detokenization of text.

## Functionality

1. **Article Extraction:** The user provides a URL to a news article.
2. **Summarization:** The article is processed, and a concise summary is generated using the Pegasus model.
3. **Translation:** The English summary is translated into Urdu using the M2M100 model.
4. **Text-to-Speech:** The Urdu translated text is converted into an audio file using Edge TTS.
5. **Output:** The audio file of the Urdu summary and the English summary are presented to the user.


## Code Structure

The code is organized into several functions:

* **`get_article_text(url)`:** Retrieves the text content of the article from the given URL.
* **`summarize_article(url)`:** Summarizes the article text using the Pegasus model.
* **`clean_text(text)`:** Cleans the text of any unnecessary symbols or formats.
* **`translate_to_urdu(text)`:** Translates the English text to Urdu using the M2M100 model.
* **`urdu_text_to_speech(text)`:** Converts the Urdu text into an audio file using Edge TTS.
* **`process_article(url)`:** Orchestrates the entire process by calling the above functions.

## Interface

The Gradio interface provides a user-friendly input field for entering a news article's URL. The output consists of:

* Audio output: An audio file of the translated Urdu summary.
* Text output: The English summary of the news article.

## Installation

Before running the code, you need to install the required libraries:

* ! pip install transformers torch newspaper3k sentencepiece sacremoses
* ! pip install gradio --upgrade
* ! pip install newspaper3k
* ! pip install lxml-html-clean
* ! pip install edge-tts
* ! pip install nltk
