# Convolutional Neural Networks (CNN) — Deep Learning Study Repository

This repository serves as a master engineering log and theoretical notebook documenting my journey through advanced Computer Vision architectures, mathematical optimization, and structural matrix transformations.

The portfolio includes programmatically compiled technical blueprints designed to serve as a production-grade reference for deep learning deployment.

---

## 🛠️ What I Did (Project Deliverables)

I built an automated compilation pipeline using Python and high-fidelity rendering engines to generate a production-grade, publication-quality reference manual:

*   **`Convolutional_Neural_Networks_Comprehensive_Notes.pdf`** An end-to-end architectural roadmap tracing image feature extraction down to dense neural classification networks.

---

## 🧠 What I Learnt (Core Competencies Mastered)

### 1. Spatial Topology Retention & Vision Paradigms
*   **The Flaw of Standard Flattening:** Learned why flattening raw pixel matrices into a single 1D vector at the input stage drops critical localized spatial parameters.
*   **Human Vision Modeling:** Studied how CNNs mimic the human visual cortex (V1) by processing scenes hierarchically, utilizing small localized **receptive fields** to detect edges, orientations, and textures before assembling them into complex object abstractions.

### 2. The Convolution Engine & Feature Extraction
*   **Matrix Kernel Filtering:** Mastered sliding small operational matrices (**Kernels/Filters**) across input images to calculate localized *dot products*, saving parameter footprints compared to traditional fully connected layers.
*   **Feature Map Generation:** Traced how scalar results from sliding filters populate an **Activation/Feature Map** to highlight dominant structural attributes.
*   **Spatial Dimension Formulations:** Mastered the mathematical equation to determine output grid boundaries based on input width ($W$), kernel size ($K$), padding ($P$), and stride frequency ($S$):
    $$O = \left\lfloor \frac{W - K + 2P}{S} \right\rfloor + 1$$
*   **Non-Linear Layer Injectors:** Implemented **Rectified Linear Units (ReLU)** immediately after linear convolutions to zero out negative pixel activations ($f(x) = \max(0, x)$), which preserves dominant data features while boosting computational efficiency.

### 3. Pooling, Flattening, and Dense Layer Classification
*   **Max Pooling Downsampling:** Applied structural downsampling by sliding a pooling window across feature maps to extract only maximum activations. This drops up to 75% of excess pixel data, enforces translation/spatial invariance, and mitigates overfitting.
*   **Dimensional Bridging (Flattening):** Formulated the bridge that unrolls multi-channeled 3D tensors (Height × Width × Channels) row by row into a single 1D vector once feature extraction completes.
*   **Global Feature Combination:** Programmed **Fully Connected (FC) Layers** to analyze the final flattened feature configurations, learning global combinations (e.g., combining "wheels" and "headlights" traits) to map inputs to precise target classes.

### 4. Categorical Output Optimization
*   **Softmax Probability Normalization:** Learned to convert unconstrained raw network scores (**logits**) into a valid, actionable probability distribution where all category scores sum to exactly 1:
    $$P(y = i \mid x) = \frac{e^{z_i}}{\sum_{j=1}^{C} e^{z_j}}$$
*   **Categorical Cross-Entropy Loss:** Implemented loss systems to heavily penalize divergent models when they assign low probabilities to correct ground-truth targets, guiding clean weight corrections during backpropagation loops:
    $$L = - \sum_{i=1}^{C} y_i \log(p_i)$$

---

## 🎨 Architectural Schemas Developed

The pipeline embeds native, clean vector representations of the complex visual workflows I studied:
*   **The Convolution Matrix Engine (Figure 1):** Illustrates an active, color-coded visual showing an input receptive area executing sliding matrix dot products with a $3 \times 3$ kernel filter to populate activation cells.
*   **The Max Pooling Downsampler (Figure 2):** A technical graphic demonstrating a $4 \times 4$ feature map extract max parameters into a dense $2 \times 2$ pooled output quadrant grid using a stride of 2.
*   **The End-to-End Summary Blueprint (Section 8):** A multi-tier layout mapping the data format evolution of an image as it mutates from a multi-channel **3D Tensor** down into an optimized **1D Class Probability Distribution**.
