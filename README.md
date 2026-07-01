# 3rd NELIREF Data Science and AI Summer School 2026

## Instructor (s)

Joseph L. Tsenum

## Introduction to NLP, LLM, and Generative AI

A comprehensive repository introducing the fundamental concepts behind Natural Language Processing (NLP), Large Language Models (LLMs), and Generative AI, with clear explanations, hand-built examples, and hands-on exercises.

## Overview

These interactive notebooks are designed for absolute beginners who want to understand how modern language technology actually works, from first principles. No external NLP libraries are required — every concept is built using core Python so you can see exactly what is happening under the hood, before you ever touch a pretrained model.

## What You'll Learn

- **AI & Machine Learning Foundations** - The difference between traditional programming and machine learning, and the three learning paradigms
- **Natural Language Processing (NLP)** - How computers understand, interpret, and generate human language
- **Tokenization & Text Preprocessing** - Breaking text into tokens, cleaning, and removing stopwords
- **Text Representation & Word Embeddings** - Converting words into numbers that capture meaning
- **Attention & Transformers** - Why the "Attention Is All You Need" architecture changed NLP forever
- **Language Models & LLMs** - How models predict the next word, and what makes a model "large"
- **Generative AI** - How models like GPT create new text, images, and code

## Table of Contents

1. What is Artificial Intelligence?
2. Types of Machine Learning
3. Natural Language Processing (NLP)
4. Word Embeddings
5. Transformers & Attention
6. Language Models and LLMs
7. Generative AI
8. Practice Exercises

## Getting Started

### Prerequisites

- Python 3.6 or higher
- Jupyter Notebook or JupyterLab installed
- No prior NLP/ML experience required

### Installation

#### Option 1: Install Jupyter with Anaconda (Recommended for beginners)
```bash
# Download Anaconda from https://www.anaconda.com/download
# Follow the installation instructions for your operating system

# Then open Anaconda Navigator and launch Jupyter Notebook
```

#### Option 2: Install with pip
```bash
pip install jupyter notebook
```

#### Option 3: Use Google Colab (No installation needed!)
1. Go to https://colab.research.google.com/
2. Click "File" → "Upload notebook"
3. Select `NELIREF_Basics_NLP_LLM_GenAI.ipynb` or `NLP_LLM_GenAI_Practice_Exercises.ipynb`
4. Start learning immediately!

### Running the Notebooks

```bash
# Navigate to the notebook directory
cd path/to/notebook/directory

# Start Jupyter Notebook
jupyter notebook

# Open NELIREF_Basics_NLP_LLM_GenAI.ipynb first (concepts)
# Then open NLP_LLM_GenAI_Practice_Exercises.ipynb (hands-on exercises)
```

## How to Use These Notebooks

1. **Read the explanations** - Each section starts with clear explanations of concepts
2. **Run the examples** - Execute code cells to see outputs immediately
3. **Experiment** - Modify code examples and see what happens
4. **Take notes** - Add your own markdown cells with reflections after each Part
5. **Complete exercises** - Work through the 5 practice exercises and self-check with the test cells

### Keyboard Shortcuts (Jupyter)

| Action | Shortcut |
|--------|----------|
| Run cell | `Shift + Enter` |
| Add cell below | `B` |
| Delete cell | `D D` (press D twice) |
| Switch to markdown | `M` |
| Switch to code | `Y` |
| Edit mode | `Enter` |
| Command mode | `Esc` |

## Practice Exercises

`NLP_LLM_GenAI_Practice_Exercises.ipynb` includes 5 progressive exercises:

1. **Build a Tokenizer** - Split raw text into clean, lowercase tokens
2. **Bag-of-Words Word Counter** - Represent text as word-frequency counts
3. **Text Preprocessing Pipeline** - Remove stopwords and build a full cleaning pipeline
4. **Cosine Similarity for Word Embeddings** - Measure how similar two word vectors are
5. **Mini Bigram Language Model** - Build a tiny next-word predictor from a training corpus

Each exercise has a self-check **Test Cell** that tells you immediately whether your solution passes.

**Solutions** - Try solving these yourself first! If you get stuck, ask for hints or revisit the matching Part in `NELIREF_Basics_NLP_LLM_GenAI.ipynb`.

## Learning Path

```
Week 1: What is AI/ML? → Types of Learning → NLP Basics
Week 2: Tokenization → Word Embeddings → Attention & Transformers
Week 3: Language Models & LLMs → Generative AI → Practice Exercises
Week 4: Build your own mini NLP project (chatbot / attention visualizer)!
```

## Resources for Further Learning

### Foundational Papers
- Vaswani et al. (2017) - *Attention Is All You Need*
- Devlin et al. (2019) - *BERT: Pre-training of Deep Bidirectional Transformers*
- Brown et al. (2020) - *Language Models are Few-Shot Learners* (GPT-3)
- Mikolov et al. (2013) - *Efficient Estimation of Word Representations in Vector Space* (Word2Vec)

### Interactive Learning
- [Hugging Face NLP Course](https://huggingface.co/learn/nlp-course)
- [Stanford CS224N: NLP with Deep Learning](https://web.stanford.edu/class/cs224n/)
- [Python.org Interactive Shell](https://www.python.org/)

### Books
- *Speech and Language Processing* by Dan Jurafsky & James H. Martin (free draft online)
- *Deep Learning* by Goodfellow, Bengio & Courville (MIT Press)

### YouTube Channels
- [3Blue1Brown - Neural Networks & Transformers series](https://www.youtube.com/@3blue1brown)
- [Andrej Karpathy](https://www.youtube.com/@AndrejKarpathy)
- [StatQuest with Josh Starmer](https://www.youtube.com/@statquest)

## Tips for Success

**Code along** - Type the examples yourself, don't just copy-paste  
**Build by hand first** - Understand tokenization, embeddings, and attention with small examples before using libraries like `transformers`  
**Debug systematically** - Read error messages carefully, especially `KeyError` on dictionaries  
**Practice daily** - Even 15 minutes a day compounds over time  
**Ask "why," not just "what"** - Understanding why attention helps is more valuable than memorizing the formula  
**Join communities** - Connect with other learners for support  

## Common NLP Patterns

### Tokenization
```python
# Lowercase + strip punctuation before comparing words
import string
def tokenize(text):
    return [t.lower().strip(string.punctuation) for t in text.split()]
```

### Commenting Best Practices
```python
# Use comments to explain WHY, not WHAT
# Good: Remove stopwords so rare, meaningful words stand out
tokens = [t for t in tokens if t not in STOPWORDS]

# Avoid: Loop through tokens
```

### Function Naming
```python
# Functions should describe what they do
def cosine_similarity(v1, v2):
    pass

def build_bigram_model(tokens):
    pass

def predict_next_word(word, model):
    pass
```

## Troubleshooting

### "ModuleNotFoundError" when importing libraries
```bash
pip install module_name
# Example: pip install numpy
```

### Cosine similarity returns `NaN` or a `ZeroDivisionError`
- Check that neither vector has magnitude 0 (a zero vector has no direction)
- Print the vectors before dividing to confirm they look correct

### `KeyError` when looking up a word in the bigram model or embeddings
- The word may not exist in your dictionary — print the dictionary's keys to confirm
- Add a check like `if word not in model: return None`

### Jupyter kernel keeps crashing
- Restart the kernel: Kernel → Restart
- Close other applications using RAM
- Update Jupyter: `pip install --upgrade jupyter`

## Contributing

Found an error? Have a suggestion?
1. Fork this repository
2. Create a new branch
3. Make your changes
4. Submit a pull request

## License

This notebook is released under the MIT License - feel free to use, modify, and share!

## Getting Help

- **In the notebook** - Hover over error messages and read them carefully
- **Online** - Search your error message on Stack Overflow
- **Communities** - Join NELIREF's Telegram at https://t.me/neliref
- **Official Docs** - The Hugging Face NLP Course is an excellent next step

## What's Next After These Notebooks?

Once you've mastered the basics:

1. **Real Word Embeddings** - Word2Vec, GloVe, and contextual embeddings (BERT, GPT)
2. **Hugging Face Transformers** - Using pretrained models for real NLP tasks
3. **Fine-Tuning** - Adapting a foundation model to your own dataset
4. **Prompt Engineering & In-Context Learning** - Getting the most out of LLMs
5. **Multimodal AI** - Combining text with images, audio, and video
6. **Responsible AI** - Bias, fairness, and safety in NLP systems
7. **Build a Project** - A chatbot, sentiment classifier, or summarizer of your own

## Author

Created for the 3rd NELIREF Data Science & AI Summer School 2026.

---

**Happy Coding!**

Questions? Issues? Reach out at contact@neliref.org, www.neliref.org or on Telegram at https://t.me/neliref

Remember: Every expert was once a beginner. Keep practicing, stay curious, and enjoy the learning journey!
