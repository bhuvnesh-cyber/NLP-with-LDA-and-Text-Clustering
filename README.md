# NLP-with-LDA-and-Text-Clustering

## Introduction
The current pandemic has triggered an unprecedented amount of published medical research with the aim to find treatments and vaccinations as soon as possible. This has also led to efforts to gather these research publications and conduct text information retrieval and text mining on them. We will use a fragment of the most widely used resource of this kind: CORD-19. This resource has been made available via several outlets, probably the most popular of which is Kaggle:

https://www.kaggle.com/allen-institute-for-ai/CORD-19-research-challenge

We used Kaggle's subset stored in the file metadata.csv. The data is organised in columns containing the following information (among others):

* Source (e.g. PMC, Medline, etc)
* Publication title
* Journal title
* DOI
* Abstract
* Date of publication

## Goal 🎯

Performing a in-depth Analysis on research publications and conducting text information retrieval and text mining techniques along with LDA (Latent Dirichlet Allocation) and Text Clustering, to find answers to questions like:

1. What is the distribution of journals per source?
2. What are the main clusters?
3. For each cluster, what are the most representative words?
4. What are the most common topics?

## Apporach
* Identified the 10 most frequent journals. Then, for each publication source, displayed the distribution of publications in each journal. The final result was presented as a clustered column chart.

![1](https://user-images.githubusercontent.com/57914889/151689441-138cb8e0-a065-4c86-a1fe-adab92595e3d.PNG)

* Using the text from the abstracts, clustered the data set and visualized the clusters. To cluster the data, I used KMeans. Choosing a reasonable metric to determine the similarity between abstracts, and choosing a reasonable number of clusters. To visualise the clusters, I produced a 2D plot where the axes represent a 2Drepresentation of each document, each document is represented as a marker, and the colour of the marker indicates the cluster to which the document belongs.

![2](https://user-images.githubusercontent.com/57914889/151689448-1aaa996c-bff5-42c3-87b3-e6f7269e87cd.PNG)

* Created a word cloud for each cluster so that the size of each word in a word cloud represents the importance of the word in the corresponding cluster. For example, I removed stop words, and remove other words that are common across all clusters.

![3](https://user-images.githubusercontent.com/57914889/151689450-cecc01b0-836c-4965-b891-850d2d8dc169.PNG)

* Implemented Topic Modelling in order to identify the main topics of the opinions expressed in the abstracts. For example, I performed Latent Dirichlet Allocation. Presenting the results in the appropriate chart. To perform topic modelling we normally need to specify the number of topics.

![4](https://user-images.githubusercontent.com/57914889/151689452-01f4f38c-b8a0-423f-8e38-4e1b41a5fa13.PNG)

![5](https://user-images.githubusercontent.com/57914889/151689454-d007a56c-93da-4edd-b6c2-d253fc323259.PNG)

## Latent Dirichlet Allocation (LDA)
Topic modeling is a type of statistical modeling for discovering the abstract “topics” that occur in a collection of documents. Latent Dirichlet Allocation (LDA) is an example of topic model and is used to classify text in a document to a particular topic. It builds a topic per document model and words per topic model, modeled as Dirichlet distributions.

## Opinion
This project was challenging, because it involved advanced NLP techniques. I had to google numerous resources to gain intuition and understanding of how does it work.

## Working enviroment
Google Colab
  - Keras 
  - Python 3
  - sklearn
  - scipy
  - nltk
  - gensim
