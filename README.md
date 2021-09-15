# Sentiment Classification 

Sentiment Analysis is process of computationally identifying and categorizing opinions expressed in a piece of text, especially in order to determine whether the writer's attitude towards a particular topic, product, etc. is positive, negative, or neutral.

**Sentiment Classification** is an `End-to-End Classification model` which deployed on **Streamlit**

**Model :** **`DistilBert Base Uncased`**

**Fine-Tuned on :** **`SST-2`**

## [View Deployed Demo on Streamlit](https://share.streamlit.io/srajanseth84/all-ml-projects-streamlit/main/app.py)
- Just open above link and select Sentiment Classification



## Demo


![](extras/)

### A Few Examples

* The beautiful ruins of the ancient city of Persepolis (Iran) with the style of Van Gogh (The Starry Night) 
  <img src="images/">
* The tomb of Cyrus the great in Pasargadae with the style of a Ceramic Kashi from Ispahan 
  <img src="images/">
* A scientific study of a turbulent fluid with the style of a abstract blue fluid painting
  <img src = "images/">



## Run Locally


* Clone the project

```bash
  git clone https://github.com/srajanseth84/Sentiment-Classification.git
```

* Go to the project directory

```bash
  cd Sentiment-Classification
```
* Create venv

```bash
  python3 -m virtualenv venv 
```

* Activate the venv

```bash
  source venv/bin/activate
```

* Install dependencies

```bash
  pip install -r requirements.txt
```
* Add your API TOKEN of Hugging face from [Hugging Face 🤗](https://huggingface.co/) in app.py

* Start the server

```bash
  streamlit run app.py 
```

## BERT MODEL DESCRIPTION

BERT is a transformers model pretrained on a large corpus of English data in a self-supervised fashion. This means it was pretrained on the raw texts only, with no humans labelling them in any way (which is why it can use lots of publicly available data) with an automatic process to generate inputs and labels from those texts. More precisely, it was pretrained with two objectives:

- **Masked language modeling (MLM)**: taking a sentence, the model randomly masks 15% of the words in the input then run the entire masked sentence through the model and has to predict the masked words. This is different from traditional recurrent neural networks (RNNs) that usually see the words one after the other, or from autoregressive models like GPT which internally mask the future tokens. It allows the model to learn a bidirectional representation of the sentence.
- **Next sentence prediction (NSP)**: the models concatenates two masked sentences as inputs during pretraining. Sometimes they correspond to sentences that were next to each other in the original text, sometimes not. The model then has to predict if the two sentences were following each other or not.


This way, the model learns an inner representation of the English language that can then be used to extract features useful for downstream tasks: if you have a dataset of labeled sentences for instance, you can train a standard classifier using the features produced by the BERT model as inputs.



## Dependencies

* [Tensorflow](https://github.com/tensorflow/tensorflow)
* [Hugging Face 🤗](https://huggingface.co/)
* [Streamlit](https://github.com/streamlit/streamlit)
* [Hugging Face BERT](https://huggingface.co/bert-base-uncased)  

## Tech Stack
* **Front-End**: [Streamlit](https://github.com/streamlit/streamlit)
* **Cloud**: [Streamlit Cloud](https://streamlit.io/cloud)
* **DL-Framework**: [Hugging Face](https://huggingface.co/)


## Reference

- [Hugging Face 🤗](https://huggingface.co/)
- [Hugging Face BERT](https://huggingface.co/bert-base-uncased)

## Authors

- [@srajanseth84](https://github.com/srajanseth84)
