# 220153_K-Means-Clustering


## Project Overview
This project implements the K-Means Clustering algorithm for Image Color Quantization using Python and Scikit-Learn. The model is trained on a standard image by clustering RGB pixel values into a smaller number of representative colors. The trained model is then applied to a custom image to perform real-world color compression.


## Dataset

### Standard Dataset
File: `dataset/standard_image.jpeg`  
Purpose: Training the K-Means model.

### Custom Dataset
File: `dataset/custom_image.jpeg`  
Purpose: Testing the trained model on a real-world image.


## Data Preprocessing
- Image loaded using PIL
- Image converted into NumPy array
- RGB pixels extracted and reshaped into 2D format
- Pixel values scaled (if used in model pipeline)


## Elbow Method
The optimal number of clusters (K) was determined using the Elbow Method by plotting Within-Cluster-Sum-of-Squares (WCSS) for different values of K.

### Elbow Curve
![image](https://github.com/aronnaiqbal/220153_K-Means-Clustering/blob/2ea914373591e22144a4229a1a3ebe34b9a8e7c4/Screenshot/Screenshot%202026-06-15%20005730.png)

## Model Training

### Algorithm
- K-Means Clustering

### Parameters
- Number of Clusters (K): 8  
- Random State: 42  
- n_init: 10  

### Saved Model
- `kmeans_image_model.pkl`



## Cluster Visualization
The clusters were visualized using PCA to reduce the RGB feature space into 2 dimensions for better interpretation.

### Cluster Scatter Plot
![image](https://github.com/aronnaiqbal/220153_K-Means-Clustering/blob/14215ecab2fa42ecb8a2a3ef18fc0706a9533044/Screenshot/Screenshot%202026-06-15%20005747.png)

## Image Compression Results

### Standard Image
![standard]()

### Custom Image
![custom]()


## Custom Prediction Output
A DataFrame was generated showing RGB values and their assigned Cluster IDs for the custom image.
![image](https://github.com/aronnaiqbal/220153_K-Means-Clustering/blob/82cbe2f9e0b54471d2525a600f5af5feedb46204/Screenshot/Screenshot%202026-06-15%20005833.png)

## Cluster Interpretation
The K-Means algorithm identified 8 dominant colour groups in the training image. Each cluster centroid represents a representative RGB colour that summarizes a group of visually similar pixels. During image reconstruction, each pixel is replaced by its nearest centroid colour, reducing the total number of colours while preserving the overall visual structure of the image. This enables effective image compression while maintaining most visual details.

---

## Conclusion
K-Means clustering effectively reduces image complexity by grouping similar pixel colours. The model successfully compresses images while preserving visual quality using only a limited number of representative colours.
