---
title: "Making Sense of Vector Similarity Metrics"
datePublished: Mon Aug 07 2023 19:05:23 GMT+0000 (Coordinated Universal Time)
cuid: cll18su2p000809jr9ye8axwp
slug: making-sense-of-vector-similarity-metrics
tags: vector-db

---

Vector similarity metrics are a critical component of many machine learning systems today. When using vector representations of data, whether for text, images, audio or any other modality, we need ways to quantify how similar two vectors are. This similarity score is then used for search, recommendation, retrieval, and more tasks.

This article will provide an overview of standard vector similarity metrics and when each might be appropriate. The vector embeddings we discuss here are typically generated from deep learning models, and capture semantic information about the original data in their dimensions.

## Cosine Similarity

Cosine similarity is one of the most popular metrics for comparing vector similarity. It measures the cosine of the angle between two vectors, quantifying their orientations' similarity.

Cosine similarity has some excellent properties that make it very useful for search and retrieval with vector embeddings:

* It is invariant to vector length, only depends on orientation. This makes it practical for comparing sentence or document vectors where absolute size is not meaningful.
    
* Works well for high-dimensional normalized vectors like those output by transformer models. The focus is on semantic direction rather than magnitude.
    
* Efficient to calculate, especially for sparse vectors.
    

For these reasons, cosine similarity is widely used for text search and retrieval applications built using sentence transformers like SBERT. It excels at assessing the semantic similarity of language vectors.

## Euclidean Distance

Euclidean distance measures the straight-line distance between two vector points in multidimensional space. It is calculated using the Pythagorean formula.

Euclidean distance considers both the magnitude and orientation of vectors. Some key properties:

* Sensitive to differences in vector lengths. Vectors with large values will be more distant than those with small weights.
    
* Intuitive and easy to interpret geometrically. Distance directly correlates with the closeness of vectors.
    
* It works better for low-dimensional dense vectors where magnitude is meaningful.
    

Euclidean distance is commonly used for visual embeddings, like those from CNNs, for image classification and recognition. The sensitivity to vector intensity makes it appropriate for comparing pixel values.

## Dot Product

The dot product between two vectors measures the component-wise multiplication and sum. It can also be defined in terms of the cosine of the angle between vectors and their magnitudes.

Dot product similarity has a mix of properties from both cosine and Euclidean:

* Accounts for both orientation and relative magnitude but not absolute magnitude.
    
* It can be made invariant to an extent by normalizing vectors.
    
* Fast and straightforward to calculate.
    

The dot product is standard for recommendation systems based on matrix factorization and collaborative filtering. For example, taking the dot product of a user vector and an item vector produces a score reflecting the predicted rating.

## Additional Metrics

There are several other standard vector similarity metrics, including:

* **Manhattan distance** - Sum of absolute differences, more robust to outliers.
    
* **Hamming distance** - Counts difference in dimensions, suitable for binary data.
    
* **Jaccard similarity** - Compares intersection over union, often used for sets.
    
* **Dice similarity** - Related to Jaccard but lessens the impact of outliers.
    

Ultimately, the "best" metric depends on your specific use case. For text, start with cosine similarity; for vision, try Euclidean; and for recommendations, consider dot product. Evaluate multiple metrics and choose the one that produces the highest quality results.