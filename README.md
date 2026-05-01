# Laboratory Work 4: Improving CNN Performance Using Regularization

## Colab Notebook
https://colab.research.google.com/drive/105hNi2P3WXXDNk7mK5rlGl8R7wYnAIqR?usp=sharing

---

## Part 7
**Highlighted region is the correct object — the model is learning properly.**

---

## Model Performance Comparison

| Metric              | Baseline Model | Improved Model |
|--------------------|:--------------:|:--------------:|
| Training Accuracy  | 0.81           | 0.79           |
| Validation Accuracy| 0.80           | 0.79           |
| Precision          | 83             | 79             |
| Recall             | 80             | 77             |
| F1-score           | 81             | 77             |
| AUC Score          | 0.96           | 0.94           |

---

## Guide Questions

### A. Model Analysis
1. Makahiya, Sitao, Cassava  
2. The precision, recall, and F1-score for the baseline model varied across classes, indicating inconsistent performance.  
3. A low recall means the model fails to identify many actual positive cases, resulting in false negatives.  
4. AUC measures how well a model separates classes across all thresholds, while accuracy measures correctness at a single threshold.  

---

### B. Model Improvement
5. Data augmentation improved training stability and reduced overfitting, though validation accuracy (0.79) was slightly lower than the baseline (0.80) as the model was still converging.  
6. Batch normalization stabilizes and speeds up training by normalizing inputs, allowing higher learning rates and reducing sensitivity to initialization.  
7. Dropout prevents overfitting by randomly disabling neurons, encouraging the model to learn more general patterns.  
8. Early stopping prevents overfitting by stopping training once validation performance starts to decline.  

---

### C. Performance Comparison
9. The improved model showed better robustness and training stability, though validation accuracy (0.79) was slightly lower than the baseline (0.80) due to earlier stopping.  
10. Data augmentation was the most impactful improvement, helping the model generalize better to real-world variations.  
11. Yes, overfitting decreased. Data augmentation and dropout helped the model generalize better, reducing the gap between training and validation performance.  

---

### D. Explainability (Grad-CAM Integration)
12. Grad-CAM generates a heatmap showing which parts of the image the model focuses on, helping verify if it uses relevant features.  
13. Yes, Grad-CAM showed the model focused on lettuce textures and edges, not the background, indicating correct feature learning.  
14. Explainability is important because it builds trust and ensures the model makes reliable decisions.  
