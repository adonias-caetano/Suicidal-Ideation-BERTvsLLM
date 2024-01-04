 # Comparing BERT-based Models and LLMs for Identifying Suicidal Ideation in Brazilian Portuguese Language

<p align="center">
This repository provides BERT codes used to identify suicidal ideation in non-clinical texts in Brazilian Portuguese.
</p>

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/adonias-caetano/Suicidal-Ideation-BERTvsLLM.git">
    <img src="logo_boamente.png" alt="Logo" width="80" height="80">
  </a>
</div>

<div align="justify">

 ## 📋 Requirements

* Google Colab
* python pandas library
* python unidecode library
* python word_tokenize, stopwords, sent_tokenize (nltk) libraries
* python wordcloud library
* python matplotlib.pyplot library
* python transformers library
* python seaborn library
* python imblearn.under_sampling library
* python sklearn.model_selection library

## 📖  Dataset

The <a href="https://zenodo.org/records/10070747"><strong>original dataset</strong></a> consists of 2691 sentences without suicidal ideation and 1097 sentences with suicidal ideation in PT-BR. The dataset is available in Comma-separated values (CSV) format in two columns: text and target, respectively the sentence and class 0 (negative) or 1 (positive). 

## 🛠 Fine-tuning BERT-based Models

Utilizamos dois modelos baseados em BERT pré-treinados em português brasileiro, a saber, BERTimbau Base (BERT-Base) e BERTimbau Large (BERT-Large) de <a href="https://github.com/neuralmind-ai/portuguese -bert/"><strong>BERTimbau - BERT português</strong></a>. O terceiro modelo foi a <a href="https://github.com/google-research/bert/blob/master/multilingual.md"><strong>base multilíngue do BERT</strong></a>.

O otimizador AdamW foi utilizado para ajustar parâmetros no modelo, tamanho de lote de 16, configurado com taxa de aprendizado igual a 2e-6 em sete épocas de treinamento. A validação cruzada K-fold foi realizada dividindo o conjunto de dados pré-processado em 80% para treinamento e 20% para validação.

## 🤖 Access our article in Acta Psychiatrica Scandinavica 

### [TO BE DEFINED](https://onlinelibrary.wiley.com/journal/16000447)

## 👏 Contributing
 
If there is a bug, or other improvement you would like to report or request, we encourage you to contribute.

Please, feel free to contact us for any questions: [![Gmail Badge](https://img.shields.io/badge/-ariel.teles@ifma.edu.br-c14438?style=flat-square&logo=Gmail&logoColor=white&link=mailto:ariel.teles@ifma.edu.br)](mailto:ariel.teles@ifma.edu.br )

## 📄 License

### <a href="https://doi.org/10.5281/zenodo.10070747"><img src="https://zenodo.org/badge/DOI/10.5281/zenodo.10070747.svg" alt="DOI"></a>
https://zenodo.org/badge/DOI/10.5281/zenodo.10070747.svg
 

## 📚 References

* <a href="https://www.mdpi.com/2227-9032/10/4/698"><strong>Paper about Boamente System</strong></a>.
* <a href="https://www.sciencedirect.com/science/article/pii/S1877050922009668"><strong>Paper about XAI Boamente System</strong></a>.
