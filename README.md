# Counteracting Misinformation by AI Using Deepfake Detection Algorithms 🤖🔍

**Team**:  
- Jash Dharia  
- Austin Rodrigues  
- Abhishek Shinde  
- Amol Borkar  

## 🚀 Introduction

Recent advancements in **Generative AI** have enabled the creation of **Deepfake** images and videos (using tools like **FaceSwap**) that can easily circulate on social media. This technology poses risks as malicious actors can impersonate others and harm reputations. 😈👥

Our **model** 🧠 is designed to be part of a **content moderation pipeline**, identifying whether an image uploaded by a user is a deepfake or not. The primary stakeholders for this project are:

- **Social Media Platforms** 📱 (Content Moderation)  
- **Law Enforcement** 👮‍♂️  

We followed a **conventional deep-learning approach** and developed a model from scratch that achieved **84.6% test accuracy**. 🎯

## 📚 Literature Review

Our research revealed that **Convolutional Neural Networks (CNNs)** are the most widely-used method for deepfake detection. Many studies combine CNNs with techniques like:

- **Attention maps** 👁️  
- **Frequency extractors** 🎶

CNNs excel at **learning image features** and are well-suited for tasks with limited data. Since **Social Media Platforms** are our primary stakeholders, we aimed to create a model that balances:

- **Excellent inference speeds** ⚡ to handle millions of user-uploaded images daily
- **Explainability** 📊 for classification results

## 📊 Data and Methods

### Data
We primarily worked with **image data** 🖼️ and used publicly available datasets:

- **Diverse Fake Face Dataset** (msu.edu)  
- **OpenForensics: In-The-Wild Dataset [V.1.0.0]**  

Due to **limited computing resources** 💻, we constructed a custom dataset from **DFFD** consisting of:

- 10,000 **real** images 🖼️  
- 6,900 **deepfakes** 🔴

### Methods
#### Preprocessing Steps:
1. **Face detection** using a **pre-trained model** 👀
2. **Center-cropping** images to 256x256 resolution 🖼️  
3. **Normalization** of image data  

We experimented with various **CNN architectures** (AlexNet, LeNet, ResNet), training for **40 epochs** ⏳ with a batch size of 75 on 16K images.

## 📈 Results

### Performance Overview:
- **AlexNet**:
  - **98% training accuracy** 🎯
  - **84.6% test accuracy** ✅

- **LeNet**:
  - **81% test accuracy** 📊

- **ResNet**:
  - Surprisingly, **46% accuracy** despite the high parameter count. This underperformance could be due to insufficient training data and epochs. 🤷‍♂️

## 💬 Discussion

Our model must **learn deepfake artifacts** 🔍 rather than just generic image features. Although our model works as an early-stage **filter** for content moderation, testing it on **real-world data** from social media platforms is necessary to enhance generalization. 🌐

