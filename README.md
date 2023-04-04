
# Rumor Detection using Deep Learning techniques

There have been several attempts to detect and classify rumors in social media using traditional machine learning techniques, such as support vector machines (SVMs), decision trees, and naive Bayes. However, these methods are limited by their inability to capture the complex relationships and dependencies between the words in the text data. More recent studies have investigated the use of deep learning techniques, such as RNNs and CNNs, for rumor detection and classification. However, these methods are still in their early stages and there is much room for improvement in terms of accuracy, efficiency, and scalability.

To increase the performance of the model during rumor detection we developed hybrid or ensembling models by combining two or many techniques. A hybrid model is defined as a model which combines two deep learning techniques such as LSTM or CNN or other networks. In the hybrid model normally the models feed their output to one another to get the outcome whereas the ensembling model works independently to predict an output.

## Proposed model w.r.t Deep learning:

![ProposedModel](https://user-images.githubusercontent.com/118846871/229832204-d5d5a5ef-e205-4964-91ff-270863cd8e8b.png)


The first step involves pre-processing the data which uses various techniques such as Part-of-Speech (POS) tagging, data cleaning, and lemmatization to prepare the data for further processing. 

After this step, word tokens are generated with POS tags, and centrality calculation and seed word identification are performed.

For every word or tag identification, a vector generation step is carried out, which involves seed vector generation, tag filtration, and similarity calculation with seed vectors to generate feature vectors.

To predict the veracity of rumors, the model identifies salient features of rumors by examining three aspects of information spread: linguistic style used to express rumors, characteristics of people involved in propagating information, and network propagation dynamics.

The model also takes into account users' behavior to combat rumors, which is influenced directly by personal norms, altruism, social ties, and knowledge, and indirectly by perceived severity and perceived vulnerability through the personal norm.

In summary, the proposed model uses a GCN-based approach for rumor detection on social media, which involves various techniques such as data preprocessing, vector generation, and examining various aspects of information spread and users' behavior to combat rumors.

The model consists of several layers that perform different operations on the preprocessed text data, such as tweets or social media posts.

The input layer takes in the preprocessed text data and passes it to the next layer, the word embedding layer. The word embedding layer converts the text into word embeddings, which can capture the semantic meaning of the text. Word embeddings are numerical representations of words that enable the machine learning model to understand the context and meaning of words in the text.

The output of the word embedding layer is a sequence of word embeddings, which is passed into the Bi-LSTM layer. The Bi-LSTM layer captures the context of the text by processing the sequence of word embeddings in both forward and backward directions. It consists of multiple Bi-LSTM layers (Layer 1 to Layer n), and each layer processes the sequence of word embeddings to capture the context of the text.

The output of the Bi-LSTM layer is passed into a Graph Convolutional Network (GCN) layer. The GCN layer can capture the relational information among the different pieces of text, such as retweets or replies. It consists of multiple layers of graph convolution operations, which process the input from the Bi-LSTM layer. The GCN layer can capture the relational information among different pieces of text by learning the structure of the graph and its nodes.

The output of the GCN layer is passed through an attention layer. The attention layer helps to focus on the most relevant parts of the graph and text for rumor detection. It consists of multiple layers of attention operations that process the output from the GCN layer. The attention mechanism helps to weigh the importance of different parts of the text and graph and focuses on the most relevant parts for rumor detection.

In summary, the proposed deep learning model for rumor detection on social media consists of several layers, including the input layer, word embedding layer, Bi-LSTM layer, GCN layer, and attention layer. These layers perform different operations on the preprocessed text data and help to capture the context, relational information, and relevant parts of the text for rumor detection.
