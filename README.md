# Kaggle-Project

## Group Members
Emily Sun,
Emmy Chen,
Emily Nadimyan,
Felicia Chen,
Grishma Shukla,
Grace Chen

## Project Brief + Connection to BTTAI
This Kaggle competition is a great chance for students in BTTAI to be able to apply their skills to a real-world problem in a flexible, safe learning space. By participating in this challenge, we as students will gain valuable experience in model development, data analysis, and ethical AI considerations, as well as be able to learn more about different skin conditions and the markers that can identify them.


## Project Objective
Our goal is to build a machine learning model that can classify dermatological conditions from images as accurately as possible. The dataset is a subset of the FitzPatrick17k dataset, containing around 4,500 labeled images representing 21 different skin conditions. We will develop a classification model that will maximize the weighted average F1 score, making sure that both precision and recall are optimized across different classes.


## Real World Significance
It goes without saying that accurate classification of dermatological conditions is critical for early diagnosis and treatment of skin diseases, including serious conditions such as melanoma. Existing AI models can struggle with classification due to biases and generalizations, especially when shown images that span a lot of different skin tones. By working on this competition, we can contribute to the development of more inclusive and fair medical AI systems. We hope that insights we uncover and conclusions we draw in this challenge can help improve diagnostic tools, assist medtech specialists and dermatologists, and expand access to healthcare.

## Data Exploration (What are we looking at?)
The dataset used in this competition is a subset of the FitzPatrick17k dataset, which consists of around 17,000 labeled images of dermatological conditions spanning a lot of different skin tones based on the FitzPatrick skin tone scale (FST). For this challenge, a subset of 4,500 images from this larger set was given, specifically covering 21 different skin conditions. Because the subset is curated, it keeps some of the representation and classification challenges seen in the full set, giving us a glimpse into the fairness and bias that can come into play in medical AI applications.

## Data Exploration (Preprocessing)
Since our target variable (skin condition labels) is categorical, we used Label Encoding to convert the labels into numerical values. Doing this allows the model to process the categorical data more effectively. In addition, we decided to split the data into 3 sets, the training, validation, and testing sets. By splitting into 3 sets instead of just 2, we are able to test our model more extensively so that we would get a better view on how accurately our model was performing.

## Model Development
To tackle this classification problem, we explored several deep learning architectures, including CNN-based models such as ResNet-50, EfficientNet, and MobileNetV2. After experimenting with different architectures and hyperparameter tuning, we selected a fine-tuned EfficientNet model as our final approach due to its strong balance between accuracy and computational efficiency.
Our training pipeline included the following key steps:
- Data Augmentation
- Transfer Learning
- Loss Function & Optimizer
- Evaluation Metrics

## Results & Key Findings


## Impact Narrative
Our work highlights the potential of AI-driven dermatological diagnosis while also uncovering key challenges that need to be addressed. The project not only contributes to improving automated skin condition classification but also emphasizes the need for more diverse and representative datasets in medical AI. By promoting fairness and robustness in machine learning models, we aim to contribute to the development of AI tools that serve all individuals equitably, regardless of skin tone.


## Next Steps & Future Improvements

