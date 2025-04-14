# 📄 Named Entity Recognition for OCR-Processed Polish Documents

This project focuses on training a Named Entity Recognition (NER) model using BERT to extract structured information from Polish text. The text is assumed to come from OCR-processed administrative documents. The current version is based on the publicly available `allegro/klej-nkjp-ner` dataset, with plans to extend the model to recognize custom entities such as PESEL, NIP, and postal codes in real-world document workflows.

## 🚀 Project Highlights

- ✅ Fine-tunes a pre-trained Polish BERT model [`dkleczek/bert-base-polish-cased-v1`](https://huggingface.co/dkleczek/bert-base-polish-cased-v1)
- ✅ Trained on the [KLEJ NKJP NER dataset](https://huggingface.co/datasets/allegro/klej-nkjp-ner)
- ✅ Uses Hugging Face Transformers, Datasets, and `Trainer` API
- ✅ Token-label alignment for subword tokenization handled correctly
- ⚙️ Modular design for easy future integration with OCR pipelines
- 🔜 Future goal: Add custom labels for PESEL, NIP, postal codes, etc.

## 🧠 Technologies

- Python 3.10+
- [Transformers](https://github.com/huggingface/transformers)
- [Datasets](https://github.com/huggingface/datasets)
- PyTorch
- spaCy
- seqeval (for evaluation)


## 📊 Model Training Overview

1. Loads and tokenizes the NKJP NER dataset.
2. Aligns labels to tokenized sequences, ignoring non-initial subwords.
3. Fine-tunes the BERT model using the Hugging Face `Trainer`.
4. Evaluates the model using precision, recall, and F1-score via `seqeval`.

## 🧩 Next Steps

- Integrate OCR pipeline for scanned document input.
- Create custom annotated datasets for PESEL, NIP, postal codes.
- Export predictions to structured formats (e.g., JSON, CSV).
- Package as an API or script for document processing.

## 📌 Example Use Cases (Planned)

- Automatic extraction of personal data from scanned administrative forms
- Preprocessing step in document digitization systems
- Anonymization of sensitive information in Polish documents

## 📜 License

MIT License

---

**Author:** _M1W33LSJ_  
Feel free to contribute or open issues if you're interested in collaborating!
```
