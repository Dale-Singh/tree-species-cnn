# Tree Species Classification Using Convolutional Neural Networks

## Project Overview
This project explores the application of convolutional neural networks (CNNs) for the classification of tree species using the TreeSatAI Benchmark Archive dataset. The primary objective is not to build a highly accurate model but to understand how different techniques, such as residual links, class weighting, and data augmentation, influence model performance on complex, real-world data.

## Usage
- **Review the Notebooks**: Explore the Jupyter Notebooks to understand the applied methodologies and view the cached results.

## Background
The dataset used comprises over 50,000 images of publicly managed forests in Lower Saxony, Germany. These images are classified into three hierarchical levels: leaf types, forest management categories, and specific tree species. The project leverages this data to evaluate the effectiveness of various CNN architectures and data processing techniques.

## Objectives
- **Baseline Model**: Develop a CNN that can reasonably classify tree species based on aerial imagery, serving as a control for evaluating other techniques.
- **Residual Links**: Assess the impact of integrating residual connections into the CNN architecture to facilitate gradient flow and potentially improve model performance.
- **Class Weighting**: Implement class weighting to address imbalances in the dataset and observe its effect on the model's sensitivity to minority classes.
- **Data Augmentation**: Apply data augmentation to artificially increase the diversity of the dataset, testing its ability to improve model robustness.
- **Class Complexity**: Investigate how the model performs when applied to different levels of classification complexity within the dataset.

## Methodology
- **Data Preprocessing**: The images were resized and batched to optimize the training process. The dataset was split into training, validation, and test sets, with the model trained on the level 2 classification (forest management categories).
- **Model Training**: A sequential CNN model was trained using categorical cross-entropy as the loss function and ADAM as the optimizer. The model was trained over 25 epochs, with performance evaluated based on accuracy, precision, recall, and F1 score.

## Current Status
- **Data Availability**: The original dataset used for this project is no longer available. The Jupyter Notebooks in this repository contain cached outputs, allowing you to review the methodology, model architecture, and results without needing the underlying data. These notebooks demonstrate the effects of various techniques on model performance using the TreeSatAI data.

## Results
- **Baseline Model**: Provided a solid foundation with moderate accuracy, though it exhibited signs of overfitting.
- **Residual Links**: Contrary to expectations, adding residual links exacerbated overfitting, leading to poorer model performance.
- **Class Weighting**: Stabilized the training process by reducing overfitting but resulted in slower convergence and lower overall performance metrics.
- **Data Augmentation**: Significantly improved the model’s robustness, eliminating overfitting and suggesting potential for further training.
- **Class Complexity**: As classification complexity increased, model performance declined, underscoring the importance of data structure in CNN-based classification tasks.

## Detailed Results
For a more comprehensive breakdown of the results, including detailed analyses and discussions, please refer to the `EMA.docx` document included in this repository.

## Conclusion
This investigation highlights the profound impact of data structure and model architecture on the performance of CNNs in classifying tree species from aerial imagery. The results emphasize that while techniques like data augmentation can enhance model robustness, the inherent complexity of the classification task and model architecture significantly influence outcomes. This project serves as a stepping stone for further exploration into optimizing CNNs for ecological data and underscores the importance of understanding the limitations and ethical considerations of using machine learning in environmental management.

## Acknowledgements
Special thanks to [The Open University](https://www.open.ac.uk/) for providing resources and support throughout this project.
