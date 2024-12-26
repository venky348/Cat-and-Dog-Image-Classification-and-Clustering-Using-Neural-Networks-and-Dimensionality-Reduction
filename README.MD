# Cat and Dog Image Classification and Clustering Using Neural Networks and Dimensionality Reduction

This project develops a pipeline for classifying and clustering cat and dog images using convolutional neural networks (CNNs) and advanced dimensionality reduction techniques. The project aims to accurately classify images while visualizing and analyzing clustering patterns in the dataset.

## Features
- **Neural Network-Based Classification**: Utilizes CNNs to classify images into "Cat" or "Dog" categories with high accuracy.
- **Clustering Analysis**: Implements K-Means and Gaussian Mixture Models (GMM) to identify patterns and clusters in the data.
- **Dimensionality Reduction**: Employs techniques like PCA, t-SNE, LLE, and MDS to reduce the high-dimensional image data for visualization and analysis.
- **Visualization**: Generates insightful scatter plots and overlays images on clusters for better interpretability.

## Dataset
- **Name**: Cat and Dog Dataset
- **Size**: Contains over 10,000 images in `.jpg` format, split into training and testing sets.
- **Source**: [Kaggle Dataset](https://www.kaggle.com/datasets/tongpython/cat-and-dog)
- **Preprocessing**:
  - Images resized to 100x100 pixels for uniformity.
  - Pixel values normalized to [0, 1] to enhance model performance.

## Methodology
### 1. Preprocessing
- **Image Resizing**: All images resized to 100x100 pixels.
- **Flattening**: Transformed into 1D arrays suitable for PCA and clustering.
- **Normalization**: Scaled pixel values to ensure uniform input to models.

### 2. Dimensionality Reduction
- **PCA**:
  - Reduced the dimensionality to 121 components while preserving 90% variance.
  - Efficiently captures global structures in the dataset.
- **t-SNE and LLE**:
  - Visualized local clusters effectively, highlighting non-linear relationships.
- **MDS**:
  - Focused on preserving global pairwise distances.

### 3. Clustering
- **K-Means Clustering**:
  - Determined optimal clusters using the elbow method.
  - Evaluated separation using silhouette scores.
- **Gaussian Mixture Models (GMM)**:
  - Applied AIC and BIC to determine the optimal number of clusters.
  - Generated synthetic samples for further analysis.

### 4. Neural Network Classification
- **Architecture**:
  - Convolutional and pooling layers for feature extraction.
  - Fully connected layers for classification.
- **Optimization**:
  - Adam optimizer and categorical cross-entropy loss for fast and stable convergence.
- **Evaluation**:
  - Model performance measured with accuracy, precision, and recall.

## Observations
- **Dimensionality Reduction**:
  - PCA effectively captures global patterns, making it suitable for clustering and visualization.
  - t-SNE and LLE provide detailed local clustering but are computationally intensive.
- **Clustering**:
  - K-Means formed two main clusters, but some overlaps exist due to data similarities.
  - GMM suggested additional sub-clusters but highlighted data complexity.
- **Neural Network Classification**:
  - CNN achieved high classification accuracy by leveraging robust preprocessing and a well-designed architecture.

## Visualizations
- 2D and 3D scatter plots for dimensionality reduction techniques.
- Clustering results with image overlays for interpretability.
- Image reconstruction from PCA-reduced data.

