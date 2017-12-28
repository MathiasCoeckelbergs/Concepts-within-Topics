# Concepts-within-Topics

\\The table shows the results of the top 10 keywords from 50 topics extracted using the Latent Dirichlet Allocation (LDA) algorithm on a corpus the MaSTIC research group of the Université libre de Bruxelles (ULB) acquired from the European Commission. We used the 300-dimensional pre-trained word embeddings from the Google News corpus using Word2Vec (https://code.google.com/archive/p/word2vec/) to represent each of these keywords vectorially. 

By deleting the word whose vector is least close to the other words from the same topic, and iterating this approach ten times, we acquire a hierarchy of terms for each topic, informed by word embeddings. The highest ranked word is shown in the leftmost column, descending until the tenth and lowest ranked word.

Topics represent what a text is about, which is rendered explicit by the representative terms for each topic (which are the highest ranked words for each topic based on their occurrence within the texts). This means that words which appear together in a topic have a high likelihood of occurring in the same context throughout the document collection. However, this does not necessarily imply that these words are semantically close to each other. We have used word embeddings to investigate how close these words are, and whether we can discern concepts represented by topics. We used cosine similarity to find similarity between vectors, and put the threshold for each topic manually. We have found that two cases are prevalent. Firstly, it is possible that a topic represents one concept, meaning that the vectors of all top words for the topic are close to each other. These words are indicated in orange. Secondly, it is possible that two concepts are represented by the topic, meaning that two clusters of close vectorial representations can be discerned in the data. These concepts are represented in blue and red respectively. Throughout both cases we found that sometimes single words which do not belong to a particular cluster are among the top words for a topic. These words are indicate in light blue. 
