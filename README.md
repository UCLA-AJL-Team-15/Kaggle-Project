# Kaggle-Project

### **👥 Team Members**

| Name | GitHub Handle | Contribution |
| ----- | ----- | ----- |
| Emily Nadimyan | @euromii | Did data preprocessing, built model, performed data augmentation, visualized dataset distributions, helped with Github readme |
| Emily Sun | @errsun | Helped make needed changes to model, did Github readme |
| Emmy Chen | @eachen1010 | Helped make needed changes to model, helped with Github readme |
| Felicia Chen | @feliciafchen | Helped make needed changes to model, helped with Github readme |
| Grishma Shukla | @grish-ma | Helped make needed changes to model, helped with Github readme |
| Grace Chen |  | Helped make needed changes to model, helped with Github readme |

---

## **🎯 Project Highlights**

* Built an EfficientNet model using transfer learning and data augmentation to solve the classification of dermatological conditions problem n the Kaggle BTTAI AJL 2025 competition.
* Achieved a final accuracy of 0.48 after 72 epochs, with a validation loss of 1.8 and a ranking of 54/74 on the final Kaggle Leaderboard
* Used Label encoding to convert categorical skin condition labels into numerical values for model processing
* Implemented data augmentation (rotation, zoom, flipping) to increase model generalization and reduce overfitting.

🔗 [Equitable AI for Dermatology | Kaggle Competition Page](https://www.kaggle.com/competitions/bttai-ajl-2025/overview)

---

## **👩🏽‍💻 Setup & Execution**

Follow these steps to reproduce the project:

### 🛠️ Set Up the Environment
- Ensure you are using Python 3.8+
- Install TensorFlow 2.x for deep learning
- Use the Kaggle API to download and access the dataset

### 📥 Download the Dataset
- Go to the Kaggle Competition Page
- Download the following files:
  train.csv
  test.csv
  sample_submission.csv
- Unzip and place them into the data directory within your project

### 🚀 Run the Notebook
1. Open notebook.ipynb using Jupyter Notebook or any compatible environment.
2. Run all the cells to:
   - Preprocess the data
   - Train the model
   - Generate predictions

---

## **🏗️ Project Overview**

#### The Kaggle Competition and BTTAI Connection
This Kaggle competition was organized by Break Through Tech AI to provide students an opportunity to apply their knowledge of machine learning and data science to solve a real-world medical AI problem. By participating in this challenge, we as students will gain valuable experience in model development, data analysis, and ethical AI considerations, as well as be able to learn more about different skin conditions, the markers that can identify them, and the importance of fair unbiased systems in medicine.

#### Objective of the Challenge
Our goal was to develop a machine learning model that can classify dermatological conditions from images as accurately as possible. The dataset is a subset of the FitzPatrick17k dataset, containing around 4,500 labeled images representing 21 different skin conditions. We will develop a classification model that will maximize the weighted average F1 score, making sure that both precision and recall are optimized across all classes.

#### Real World Significance
Accurate classification of dermatological conditions is critical for early diagnosis and treatment of skin diseases, including conditions such as melanoma. Existing AI models can struggle with classification due to biases inherent in the training data and generalizations, especially when shown images that span a lot of different skin tones. By working on this competition, we can contribute to the development of more inclusive and fair medical AI systems. We hope that the insights we uncover and conclusions we draw in this challenge can help improve diagnostic tools, assist medtech specialists and dermatologists, and expand access to healthcare.

---

## **📊 Data Exploration**

#### Dataset Overview
The dataset used in this competition is a subset of the FitzPatrick17k dataset, which consists of around 17,000 labeled images of numerous different skin conditions. It also covers a variety of different skin tones based on the FitzPatrick skin tone scale (FST). For this challenge, a subset of 4,500 images from this larger set was given, specifically covering 21 different skin conditions. Because the subset is curated, it keeps some of the representation and classification challenges seen in the full set, giving us a glimpse into the fairness and bias that can come into play in medical AI applications.

#### Preprocessing & Label Encoding
Since our target variable (skin condition labels) is categorical, we used Label Encoding to convert the labels into numerical values. Doing this allows the model to process the categorical data more effectively. In addition, we decided to split the data into 3 sets, the training, validation, and testing sets. By splitting into 3 sets instead of just 2, we were able to test our model more extensively so that we would get a better view of how accurately our model was performing.

---

## **🧠 Model Development**
To tackle this classification problem, we explored several deep learning architectures, including CNN-based models such as ResNet-50, EfficientNet, and MobileNetV2. After experimenting with different architectures and hyperparameter tuning, we selected a fine-tuned EfficientNet model as our final approach due to its strong balance between accuracy and computational efficiency.

Training Pipeline
1. Data Augmentation: Used techniques such as rotation, width/height shift, shear, zoom, and horizontal flipping.
2. Transfer Learning: Loaded pretrained weights for EfficientNet and fine-tuned the model.
3. Loss Function & Optimizer: Used categorical_crossentropy and Adam optimizer with a learning rate of 1e-5.
4. Validation Strategy: Monitored val_loss and restored the best model using EarlyStopping

---

## **📈 Results & Key Findings**
We trained the model for 72 epochs after which the accuracy stagnated at around 0.48, with a value loss of 1.8.

We found that the EfficientNet model outperformed the other models both in terms of accuracy and computational efficiency. Our data augmentation process improved the generalization issue but it also required fine-tuning to prevent overfitting, which increased computational overhead. Hyperparameter tuning had a significant effect on the model's efficacy. 

---

## **🖼️ Impact Narrative**
Our work highlights the potential of AI-driven dermatological diagnosis while also uncovering key challenges that need to be addressed. The project not only contributes to improving automated skin condition classification but also emphasizes the need for more diverse and representative datasets in medical AI. Development of AI models like ours for this application has great potential to benefit marginalized groups both in improving diagnosis accuracy and by improving accessibility to dermatalogical care. Of course, there exist well-known limitations to AI models in medical applications, such as transparency and explainability in model predictions as well as ensuring adherence to medical standards, but by promoting fairness and robustness in machine learning models, we aim to contribute to the development of AI tools that serve all individuals equitably, regardless of skin tone---our findings can be used by medical researchers to refine existing AI models. 


## **🚀 Next Steps & Future Improvements**
Given that both our training accuracy and test accuracy was low, we could further refine our model by making several improvements. In the data preprocessing phase, we could use stratified sampling to mitigate class imbalance in the original data, and use more complex data augmentation techniques. In model development, we could perform further hyperparameter optimization to fine-tune our model to accomadate for data augmentation, as well as add visualizations to better diagnose what is causing the low accuracy. Of course, the incorporation of more data and simply training the model for longer would improve the model as well, though at the cost of increasing computational overhead.

