Experiments with unsuprvised methods - The task : Identifying difrent Intent groups from a sentences file 
Final version was tailored manualy to a customer-service data 
experiments notebooks goes thrugh sevral approches , algos and such - this has been a great learning experience 

Different Approaches I Tried
Experimented with Different Embedding Models: I tested various models to generate embeddings for the sentences, including different pre-trained BERT-based models at different levels and customer-service fine-tuned models. Each run took considerable time, which extended the overall timeline.

Explored Various Clustering Algorithms: I tried different clustering algorithms to identify topics within the dataset, including K-Means, DBSCAN, and hierarchical clustering methods.

Manual Topic Naming and Merging: I used pyLDAvis for topic modeling and performed grid search to find the optimal number of topics. I manually named the topics based on their content and merged similar ones when necessary.

Defining Representative Sentences: For each identified topic, I defined a representative sentence and calculated its embedding. This served as a reference to better understand the content of each topic.

Selecting Example Sentences: I generated embeddings for the sentences in the dataset using a BERT-based model. For each intent, I selected the three most similar sentences to the representative sentence using cosine similarity.

Drawbacks of the Current Approach
Manual Effort: The approach relies heavily on manual processes for naming topics and defining representative sentences, which is time-consuming and lacks scalability.

Limited Performance: The models used were not significantly fine-tuned for this specific task. I believe that using a better-fitting model or training one from scratch would have greatly improved the results, as the embeddings did not provide enough distinction to form meaningful clusters.

What next:
Use a Fine-Tuned Model: Given more time, I would focus on finding or training a fine-tuned model specifically for this type of data to enhance accuracy and relevance.

Automate Topic Naming and Merging: I would develop automated methods for naming topics and merging similar ones using advanced NLP techniques to reduce the manual effort involved.

Improve Preprocessing Techniques: I would look into better preprocessing techniques to capture the essence of each sentence more effectively, which would likely improve the quality of topic modeling and sentence classification.
