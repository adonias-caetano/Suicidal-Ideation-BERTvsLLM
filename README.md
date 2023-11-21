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

## 📋 Requirements

* Google Colab

## 📖  Dataset

The <a href="https://zenodo.org/records/10070747"><strong>original dataset</strong></a> consists of 2691 sentences without suicidal ideation and 1097 sentences with suicidal ideation in PT-BR. The dataset is available in Comma-separated values (CSV) format in two columns: text and target, respectively the phrase and class 0 (negative) or 1 (positive). 

Building this dataset is detailed in <a href="https://www.mdpi.com/2227-9032/10/4/698"><strong>paper about Boamente System</strong></a>.

## Fine-tuning BERT-based Models

We use two BERT-based models pre-trained in Brazilian Portuguese, namely, BERTimbau Base (BERT-Base) and BERTimbau Large (BERT-Large) from <a href="https://github.com/neuralmind-ai/portuguese-bert/"><strong>BERTimbau - Portuguese BERT</strong></a>. The BERT-Base and BERT-Large Cased variants were trained on BrWaC (Brazilian Web as Corpus), a large Portuguese corpus, for 1,000,000 steps, using full-word masking. The third model was the <a href="https://github.com/google-research/bert/blob/master/multilingual.md"><strong>BERT multilingual base</strong></a>. This model was pre-trained on the top 104 languages with the largest Wikipedia using a masked language modeling (MLM) objective.

For the three BERT-based models, the steps of tokenization (BertTokenizer), encoding the tokens into numeric data, using the ecode function to obtain input IDs and attention masks from the datasets, pytorch Dataset and DataLoader to divide the batch data. We started Huggingface's BertForSequenceClassification model to tune the pre-trained BERT mode for classification tasks easily. The AdamW optimizer was used to adjust parameters in the model, batch size of 16, configured with a learning rate equal to 2e-6 in seven training epochs.

K-fold cross-validation was performed by dividing the pre-processed dataset into 80% for training and 20% for validation. The output of each model is the probability of the sentence belonging to the positive and negative class, with the one with the highest probability being the predicted output.

## 🤖 Access our article in International Journal of Medical Informatics

### [Science direct](https://www.sciencedirect.com/journal/international-journal-of-medical-informatics)

## 👏 Contributing
 
If there is a bug, or other improvement you would like to report or request, we encourage you to contribute.

Please, feel free to contact us for any questions: [![Gmail Badge](https://img.shields.io/badge/-ariel@lsdi.ufma.br-c14438?style=flat-square&logo=Gmail&logoColor=white&link=mailto:ariel@lsdi.ufma.br)](mailto:ariel@lsdi.ufma.br)

## 📄 License


