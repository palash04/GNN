# Recommender System using Graph Neural Networks
This project was made as a part of my individual projects.

#### -- Project Status: [Completed]

## Project Objective
`Recommend items of interest to users.` </br>
Recommendation has gathered lots of attention in the last few years. Tech giants such as Amazon, Netflix, etc. are recommending users their products, or any type of content, that are considered as interesting for them. Those recommendations are usually based on user-item interactions, their characteristics, or on the user's previous purchasing history, and previous clicks.

## Approach
Graph Neural Networks are extremely helpful to tackle the recommender system task, as the available data might be better represented in a graph.
GNNs can leverage content information (i.e., user, item features) and graph data structure (relationship between user and items). In contrast, typical traditional models can leverage only one of the two. 
This project makes use of graph convolutional neural network. </br>
So the approach used incorporates representational learning. It is divided into two steps:
- Generate high-quality embeddings for both users and items. These embeddings are generated using message passing framework, or simply information propagation through network.
- Using the generated embeddings, predict the item preferences.</br>
During the inference, a cosine similarity between user embeddings and all items embeddings are calculated. The item giving lower cosine similarity is picked for recommendation.



## Dataset Description
The dataset can be found in the data directory of this repository.
Dataset contains 
1. Train Data csv file - Here the user-item interaction is given. Their purchasing details.
2. Train Data Target csv file - Here for each user the ground truth predictions are given.
3. Test Data csv file - User-item interaction. For each user, we need to recommend top 3 prdocuts.

## Prerequisites
- Python 3.7.10 or above
- [PyTorch](https://pytorch.org/) 1.9.0 or above
- CUDA 10.2 (or other version corresponding to PyTorch) to utilize any compatible GPU present for faster training
- Google Colab

## Results achieved on test dataset</br>
- Mean Relevance Rank (MRR): 0.627 </br>
- Precision: 0.717

Note: Range of MRR and Precision lies between 0 and 1. Higher the value better the performance of the model.

## Authors
- Palash Mahendra Kamble - [palash04](https://github.com/palash04/)
