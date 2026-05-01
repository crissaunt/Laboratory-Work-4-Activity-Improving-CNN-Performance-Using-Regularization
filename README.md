# Laboratory-Work-4-Activity-Improving-CNN-Performance-Using-Regularization

https://colab.research.google.com/drive/105hNi2P3WXXDNk7mK5rlGl8R7wYnAIqR?usp=sharing



#part 7  Highleighted region is the correct object , the mdoel is learning properly



| Metric | Baseline Model | Improve Model |
| :--- | :---: | ---: |
| Training Accuracy | 0.81 | 0.79 |
| Validation Accuracy | 0.80 | 0.79 |
| Precision | 83 | 79 |
| Recall | 80 | 77 |
| F1-score | 81 | 77 |
| AUC Score  |0.96 | 0.94 |

#Guide Questions
A. model analysis
  1. Makahiya: ,Sitao:  ,Casava
  2. The precision, recall, and F1-score for the baseline model varied widely across classes, indicating inconsistent performance.
  3. A low recall indicates that the model is failing to identify a large portion of the actual positive instances, resulting in many false negatives.
  4. AUC measures how well a model separates classes across all thresholds, while accuracy measures correctness at a single threshold.

B. Model Improvement
  5. Data augmentation contributed to more stable training and reduced overfitting, though the validation accuracy for the improved model (0.77) ended up slightly lower than the baseline (0.80 because the model was still converging.
  6. Batch normalization is important because it stabilizes and accelerates the training process by normalizing layer inputs, allowing for higher learning rates and reducing sensitivity to weight initialization.
  7. Dropout improves the model by randomly deactivating neurons during training, which prevents the network from over-relying on specific features and encourages it to learn more robust, generalized patterns to reduce overfitting.

  8. Early stopping prevents overfitting by monitoring the validation loss during training and halting the process as soon as performance starts to degrade on unseen data, ensuring the model retains its ability to generalize.

C Performance Comparison
  9.The improved model showed enhanced robustness through data augmentation and better training stability from batch normalization, although it achieved a slightly lower validation accuracy of 0.77 compared to the baseline's 0.80 due to early stopping at an earlier stage of convergence.
  10. Data Augmentation was the most impactful enhancement. It prevents overfitting by teaching the model to recognize objects regardless of their position or angle, making it much more reliable for real-world use.
  11 Yes, it decreased. By using data augmentation and dropout, the model stopped 'memorizing' the training data and started generalizing better, bringing the training and validation scores much closer together.

D Explainability (Grad-Cam Integration)
  12. Grad-CAM creates a heatmap that shows exactly which pixels the model focused on to make its decision. It helps verify if the model is looking at the actual object (like the leaves of a plant) or just irrelevant background noise.
  13. Yes, Grad-CAM showed that the model focused on more relevant features. Grad-CAM heatmaps focused on lettuce textures and edges, not the background, showing the model used relevant features.
  14. Explainability is crucial in the real world because it builds trust and safety.





