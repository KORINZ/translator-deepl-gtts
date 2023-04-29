# Translation and Text-to-Speech Tool

This project contains a script for translating text or documents from one language to another using the DeepL API, and a text-to-speech tool for converting translated text to audio using Google Text-to-Speech (gTTS).

## Requirements

- Python 3.7+
- `deepl` Python library
- `vlc` Python library
- `gtts` Python library

To install the required libraries, run:

```bash
pip install deepl vlc gtts
```

## Usage

### Translation

The translation script supports translating text, text files, and documents (.pdf, .docx, .pptx). To use the script, follow these steps:

1. Make sure you have a valid DeepL API key.
2. Create a `config.py` file in the same directory as the translation script with the following content:

```python
DEEPL_API_KEY = "your_api_key_here"
```

Replace `your_api_key_here` with your actual DeepL API key.

3. Run the script with the appropriate arguments:

- For translating text:

```bash
python translate.py -t "your_text_here" target_language
```

- For translating a text file:

```bash
python translate.py -f input_file_path target_language
```

- For translating a document:

```bash
python translate.py -d input_document_path target_language
```

Replace `target_language` with the target language code, e.g., 'sv' for Swedish. You can also optionally specify the source language with `-s source_language`.

To see the full list of supported arguments, run:

```bash
python translate.py --help
```

### Text-to-Speech

The text-to-speech script converts a given text to audio and plays it using the `vlc` library. To use the script, simply run:

```bash
python text_to_speech.py
```

The example text is hardcoded in the script. You can replace it with your desired text and language.

## Example

Here's an example of using both the translation and text-to-speech scripts together:

1. Translate a Japanese text to Swedish:

```bash
python translate.py -t "your_japanese_text_here" sv
```

2. Pass the translated text to the text-to-speech script:

```bash
python text_to_speech.py
```

Make sure to replace the hardcoded text and language in the `text_to_speech.py` script with your translated text and target language.

## License

This project is released under the [MIT License](LICENSE).
