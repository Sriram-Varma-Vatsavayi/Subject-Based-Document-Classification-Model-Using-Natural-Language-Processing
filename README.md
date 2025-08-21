# Subject-Based Document Classification Model Using Natural Language Processing

[![Python](https://img.shields.io/badge/Python-3.7%2B-blue)](https://python.org)
[![SpaCy](https://img.shields.io/badge/SpaCy-v3.x-green)](https://spacy.io)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

A Python-based document classification system that automatically categorizes academic documents into subjects (Mathematics, Physics, Chemistry) using Natural Language Processing techniques and semantic similarity analysis.

## 📋 Table of Contents

- [Description](#description)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Dependencies](#dependencies)
- [How It Works](#how-it-works)
- [Sample Documents](#sample-documents)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## 🔍 Description

This project implements an intelligent document classification system that uses NLP to automatically sort academic documents into three subject categories: Mathematics, Physics, and Chemistry. The system analyzes document content, extracts key features using spaCy's language model, and uses semantic similarity to determine the most appropriate subject classification.

## ✨ Features

- **Automated Document Classification**: Classifies Word documents (.docx) into Math, Physics, or Chemistry categories
- **NLP-Based Analysis**: Uses spaCy's large English language model for advanced text processing
- **Semantic Similarity**: Employs word embeddings and similarity scores for accurate classification
- **Keyword-Based Training**: Uses predefined keyword sets for each subject domain
- **Noun Extraction**: Focuses on nouns for better subject identification
- **File Organization**: Automatically moves classified documents to appropriate folders
- **Text Preprocessing**: Handles special characters and normalizes text content

## 🚀 Installation

### Prerequisites

- Python 3.7 or higher
- pip package manager

### Step 1: Clone the Repository

```bash
git clone https://github.com/yourusername/Subject-Based-Document-Classification-Model-Using-Natural-Language-Processing.git
cd Subject-Based-Document-Classification-Model-Using-Natural-Language-Processing
```

### Step 2: Install Required Packages

```bash
pip install python-docx
pip install spacy
pip install numpy
pip install rake-nltk
pip install nltk
```

### Step 3: Download spaCy Language Model

```bash
python -m spacy download en_core_web_lg
```

### Step 4: Download NLTK Data

```python
import nltk
nltk.download('punkt')
nltk.download('stopwords')
```

## 📖 Usage

### Command Line Usage

```bash
python organise.py path/to/your/document.docx
```

### Example

```bash
python organise.py "/Users/username/Documents/calculus_notes.docx"
```

### Jupyter Notebook Usage

1. Open `Organise_v1.ipynb` in Jupyter Notebook or JupyterLab
2. Update the file paths in the code cells to match your system
3. Run all cells sequentially
4. Provide the document path when prompted

## 📁 Project Structure

```
Subject-Based-Document-Classification-Model-Using-Natural-Language-Processing/
│
├── organise.py                 # Main classification script
├── Organise_v1.ipynb          # Jupyter notebook version
├── README.md                   # Project documentation
├── Batch_16.pptx              # Project presentation
├── Mini_final.docx            # Project report
│
├── Datasets/                   # Sample documents and keywords
│   ├── KeyWords/              # Subject-specific keyword files
│   │   ├── MathKeywords2.docx # Mathematics keywords
│   │   ├── PhysKeywords.docx  # Physics keywords
│   │   └── chemKeywords.docx  # Chemistry keywords
│   │
│   ├── Newton_laws.docx       # Sample physics document
│   ├── Salts.docx            # Sample chemistry document
│   ├── calc.docx             # Sample mathematics document
│   ├── isomers.docx          # Sample chemistry document
│   ├── regression.docx       # Sample mathematics document
│   └── relativity.docx       # Sample physics document
```

## 🛠 Dependencies

| Package | Version | Purpose |
|---------|---------|---------|
| python-docx | Latest | Reading Word documents |
| spacy | 3.x | NLP processing and language modeling |
| numpy | Latest | Numerical computations |
| rake-nltk | Latest | Keyword extraction |
| nltk | Latest | Natural language processing toolkit |

### Language Model
- **en_core_web_lg**: Large English language model for spaCy (685MB)

## ⚙️ How It Works

1. **Keyword Loading**: The system loads predefined keywords for each subject from Word documents
2. **Document Processing**: Input document is read and preprocessed to remove special characters
3. **Feature Extraction**: Nouns are extracted using spaCy's POS tagging
4. **Similarity Calculation**: Semantic similarity is computed between document features and subject keywords
5. **Classification**: Document is classified based on the highest similarity score
6. **File Organization**: Classified document is moved to the appropriate subject folder

### Algorithm Flow

```python
# Simplified workflow
keywords = load_subject_keywords()  # Math, Physics, Chemistry
document_content = extract_document_text()
document_nouns = extract_nouns(document_content)
similarities = calculate_similarities(document_nouns, keywords)
subject = classify_document(similarities)
move_document_to_folder(subject)
```

## 📚 Sample Documents

The repository includes sample documents for testing:

- **Mathematics**: calc.docx, regression.docx
- **Physics**: Newton_laws.docx, relativity.docx  
- **Chemistry**: Salts.docx, isomers.docx

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

### How to Contribute

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Areas for Improvement

- Add support for PDF files
- Implement machine learning models for better accuracy
- Create a web interface
- Add support for more subject categories
- Improve preprocessing techniques

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Contact

**Project Maintainer**: Sriram Varma

- GitHub: [@yourusername](https://github.com/yourusername)
- Email: your.email@example.com

## 🙏 Acknowledgments

- [spaCy](https://spacy.io/) for the excellent NLP library
- [python-docx](https://python-docx.readthedocs.io/) for Word document processing
- [NLTK](https://nltk.org/) for natural language processing tools

---

⭐ If you found this project helpful, please consider giving it a star!