# 🧠 WEEK-03 — CNN, NLP & TRANSFORMERS
---

# SESSION 5 · PART A · CNN FOUNDATIONS
---

This week my tutors introduced Deep Learning concepts.

The first topic was CNN.

CNN stands for Convolutional Neural Network.

CNN is mainly used for:
- Image recognition
- Face detection
- Medical image analysis
- Object detection

CNN models are very powerful in Computer Vision.

---

# 🔹 IMPORTANT TERMS IN CNN
---

## Convolution

Convolution helps detect important features from images.

## Filters

Filters are used to detect patterns like edges and shapes.

## Pooling

Pooling helps reduce image size while keeping important features.

## Feature Maps

Feature maps store detected patterns from images.

## Fully Connected Layer

This layer gives the final prediction.

---

# 🔹 WHY CNN IS IMPORTANT
---

CNN models are better than normal neural networks for image related tasks because they can automatically detect patterns.

---

# SESSION 5 · PART B · CNN LIVE DEMO
---

In this session, my tutors showed a live demo for image classification using CNN.

The model was trained using image datasets.

The steps were:
- Loading dataset
- Training model
- Testing model
- Predicting output

We also learned that GPUs help train Deep Learning models faster.

This session was mostly practical based.

---

# 🔹 IMPORTING LIBRARIES
---

```python
import tensorflow as tf
from tensorflow import keras
```

---

# 🔹 CREATING CNN MODEL
---

```python
model = keras.Sequential()
```

---

# 🔹 TRAINING MODEL
---

```python
model.fit(X_train, y_train)
```

---

# 🔹 MODEL PREDICTION
---

```python
predictions = model.predict(X_test)
```

---

# SESSION 6 · PART A · NLP FOUNDATIONS
---

NLP stands for Natural Language Processing.

NLP helps computers understand human language.

Examples:
- Chatbots
- Google Translate
- Voice assistants
- Text summarization

---

# 🔹 NLP TASKS
---

Some common NLP tasks are:
- Text classification
- Sentiment analysis
- Translation
- Speech recognition
- Question answering

---

# 🔹 TOKENIZATION
---

Tokenization means splitting text into smaller parts called tokens.

Example:

"I love AI"

can become:

["I", "love", "AI"]

---

# 🔹 WORD EMBEDDINGS
---

Word embeddings are numerical representations of words.

They help AI models understand relationships between words.

Words with similar meanings usually have similar embeddings.

Examples:
- king
- queen
- man
- woman

---

# 🔹 VECTOR REPRESENTATION
---

In NLP, words are converted into vectors so computers can process text mathematically.

This helps models understand patterns in language.

---

# 🔹 CONTEXT UNDERSTANDING
---

Modern NLP models try to understand the meaning of words based on context.

For example, the word "bat" can mean:
- a cricket bat
- an animal

The meaning changes depending on the sentence.

---

# SESSION 6 · PART B · TRANSFORMERS LIVE
---

In this session, my tutors introduced Transformers.

Transformers are advanced Deep Learning models mainly used in NLP.

Examples:
- ChatGPT
- Gemini
- Claude
- Translation models

Transformers are very powerful because they understand context better.

---

# 🔹 ALL YOU NEED IS ATTENTION
---

"Attention Is All You Need" is one of the most important research papers in AI.

This paper introduced the Transformer architecture.

The paper was published by Google researchers in 2017.

The Transformer model changed the field of Natural Language Processing.

Before Transformers, models mainly used:
- RNN
- LSTM

But Transformers became faster and more powerful.

---

# 🔹 ATTENTION MECHANISM
---

Attention helps models focus on important words in a sentence.

Example:

"The animal didn't cross the road because it was tired."

The model understands that "it" refers to the animal.

This is one of the main reasons why Transformers are powerful.

---

# 🔹 LARGE LANGUAGE MODELS
---

Large Language Models are trained using huge amounts of text data.

These models can:
- Answer questions
- Generate text
- Summarize information
- Translate languages

Examples:
- ChatGPT
- Gemini
- Claude

---

# 🔹 TIMELINE OF AI DEVELOPMENT
---

## 1950

Alan Turing introduced the idea of machine intelligence.

---

## 1956

The term "Artificial Intelligence" was officially introduced.

---

## 1980s

Machine Learning started becoming popular.

---

## 1997

IBM Deep Blue defeated world chess champion Garry Kasparov.

---

## 2012

Deep Learning became very popular after huge improvements in image recognition.

---

## 2017

The Transformer architecture was introduced through the paper "Attention Is All You Need".

---

## 2022+

Large Language Models like ChatGPT became popular worldwide.

---

# 🧠 FINAL REFLECTION — WEEK 03
---

This week helped me understand:
- Deep Learning basics
- CNN models
- Image processing
- NLP concepts
- Transformers
- Large Language Models
- Attention mechanism
- History of AI development

This week was mostly theory based but it helped me understand how modern AI systems like ChatGPT work.
