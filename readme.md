# Text Preprocessing with Stemming and Lemmatization

This repository contains the source code and resources for the **Text Preprocessing with Stemming and Lemmatization** project. The project demonstrates various text preprocessing techniques using the Natural Language Toolkit (NLTK), specifically focusing on stemming and lemmatization, which are essential steps in natural language processing (NLP) tasks.

## Table of Contents

- [Project Overview](#project-overview)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
  - [Imports](#imports)
  - [Stemming](#stemming)
  - [Lemmatization](#lemmatization)
- [License](#license)
- [Contact](#contact)

## Project Overview

The **Text Preprocessing with Stemming and Lemmatization** project demonstrates how to preprocess text data by reducing words to their base or root form. This is done using various stemming and lemmatization techniques available in NLTK.

- **Stemming**: Reducing words to their root form using different stemmers like PorterStemmer, RegexStemmer, and SnowballStemmer.
- **Lemmatization**: Converting words to their base or dictionary form using WordNetLemmatizer.

These techniques are vital for text normalization, making it easier to analyze and process text data for NLP tasks like text classification, sentiment analysis, and more.

## Project Structure

- **notebook.ipynb**: The Jupyter notebook containing the complete code for text preprocessing using stemming and lemmatization techniques.
- **LICENSE**: The Apache License 2.0 file that governs the use and distribution of this project's code.
- **requirements.txt**: A file listing all the Python libraries and dependencies required to run the project.
- **.gitignore**: A file specifying which files or directories should be ignored by Git.

## Installation

To run the project locally, follow these steps:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/your-repository-name.git
```

2. Navigate to the project directory:

``` bash 
cd your-repository-name
```

3.Create a virtual environment (optional but recommended):

``` bash 

python3 -m venv venv
source venv/bin/activate   # On Windows use `venv\Scripts\activate`
```

4. Install the required dependencies:

``` bash 
pip install -r requirements.txt
```

5. Run the Jupyter notebook:

```` bash 
jupyter notebook notebook.ipynb

````

## Usage

Imports

The notebook begins by importing the necessary libraries for stemming and lemmatization:

``` bash 
from nltk.stem import PorterStemmer
from nltk.stem import RegexpStemmer
from nltk.stem import SnowballStemmer
from nltk.stem import WordNetLemmatizer
import nltk
nltk.download('wordnet')
``` 

These imports include methods for various stemming techniques (PorterStemmer, RegexpStemmer, SnowballStemmer) and lemmatization (WordNetLemmatizer).

## Stemming
The notebook demonstrates how to apply different stemming techniques:

- PorterStemmer: A simple and widely used stemmer that reduces words to their root form.

``` bash 
stemmer = PorterStemmer()
stemmed_words = [stemmer.stem(word) for word in word_list]
```

- RegexpStemmer: A custom stemmer that uses regular expressions to remove specified suffixes.

``` bash 
reg_stemmer = RegexpStemmer(regexp='ing$|s$|able$', min=4)
stemmed_words = [reg_stemmer.stem(word) for word in word_list]

```
- SnowballStemmer: An advanced stemmer that is language-specific.

``` bash 
snowstemmer = SnowballStemmer(language='english')
stemmed_words = [snowstemmer.stem(word) for word in word_list]
``` 

## Lemmatization
The notebook also demonstrates lemmatization using the WordNetLemmatizer, which converts words to their base or dictionary form:

``` bash 
lemmatizer = WordNetLemmatizer()
lemmatized_words = [lemmatizer.lemmatize(word) for word in word_list]
``` 

Lemmatization considers the context of the word and is generally more accurate than stemming.

## License
This project is licensed under the Apache License 2.0. See the `LICENSE` file for more details.

## Contact
For any inquiries or contributions, feel free to reach out or submit an issue or pull request on GitHub.


