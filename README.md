## 💬 **Natural Language Processing (NLP) Assignment Submission** <img src="https://img.shields.io/badge/-NLTK-000000?style=flat&logo=nltk&logoColor=white">
> by Abenezer Tesfaye

Submission for NLP Frontier assignment demonstratating various techniques in Natural Language Processing (NLP) using Python libraries such as NLTK and SpaCy. With sections like text preprocessing, vectorization, named entity recognition, and bigram generation completed as per requirement for the assignment.

**Libraries Used**
  - ``nltk``
  - ``spacy``
  - ``sklearn``
  - ``wordcloud``
  - ``numpy``
  - ``pandas``


### **Key Sections**

**Text Preprocessing**

```python
  text = "Natural Language Processing is a fascinating field. It combines linguistics and computer science!"
  
  def preprocess(text):
      text = text.lower()
      text = word_tokenize(text)   
      stop_words = stopwords.words('english')
      filtered_tok = [word for word in text if not word in stop_words]
      text = ' '.join(filtered_tok)
      text = re.sub('[^a-zA-Z ]+', '', text)
      return text
  
  #final output 
  cleaned_tokens = preprocess(text)
  print(cleaned_tokens)
```


**Bigrams Generation**

```python
  bigrams = list(ngrams(cleaned_tokens, 2))
  print("Bigrams:", bigrams)
```


**Word Embeddings**

```python
  vector_store = {}
  
  for text in cleaned_tokens:
      doc = nlp(cleaned_tokens)
      vector_store[cleaned_tokens] = doc.vector
  
  vector_store

```
