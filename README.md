 # Comparative Analysis of BERT-Based and Generative Large Language Models for Detecting Suicidal Ideation: A Performance Evaluation Study

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

We use two BERT-based models pre-trained in Brazilian Portuguese, namely, BERTimbau Base (BERT-Base) and BERTimbau Large (BERT-Large) from <a href="https://github.com/neuralmind-ai/portuguese-bert/"><strong>BERTimbau - Portuguese BERT</strong></a>.  The third model was the <a href="https://github.com/google-research/bert/blob/master/multilingual.md"><strong>BERT multilingual base</strong></a>. 

The AdamW optimizer was used to adjust parameters in the model, batch size of 16, configured with a learning rate equal to 2e-6 in seven training epochs. K-fold cross-validation was performed by dividing the pre-processed dataset into 80% for training and 20% for validation. 

## 🤖 Access our article in Review

Article accepted for publication in the <a href="https://cadernos.ensp.fiocruz.br/ojs/index.php/csp"> <strong>Cadernos de Saúde Pública</strong></a>

### Paper Link 

## 👏 Contributing
 
If there is a bug, or other improvement you would like to report or request, we encourage you to contribute.

Please, feel free to contact us for any questions: [![Gmail Badge](https://img.shields.io/badge/-ariel.teles@ifma.edu.br-c14438?style=flat-square&logo=Gmail&logoColor=white&link=mailto:ariel.teles@ifma.edu.br)](mailto:ariel.teles@ifma.edu.br )

## 📄 License

### <a href="https://doi.org/10.5281/zenodo.10070747"><img src="https://zenodo.org/badge/DOI/10.5281/zenodo.10070747.svg" alt="DOI"></a> 

## 📚 References

* <a href="https://www.mdpi.com/2227-9032/10/4/698"><strong>Paper about Boamente System</strong></a>.
* <a href="https://www.sciencedirect.com/science/article/pii/S1877050922009668"><strong>Paper about XAI Boamente System</strong></a>.
