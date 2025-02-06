Counteracting Misinformation by AI Using Deepfake Detection Algorithms 🤖🔍
Team
👤 Jash Dharia
👤 Austin Rodrigues
👤 Abhishek Shinde
👤 Amol Borkar

Introduction 🚀
Recent advancements in Generative AI have enabled the widespread creation of Deepfake images and videos (using tools like FaceSwap) that can easily circulate on social media. This technology poses risks as malicious actors can impersonate others and harm reputations. 😈👥

Our model 🧠 can be integrated into content moderation systems to identify whether an image uploaded by a user is a deepfake or not. Our primary stakeholders include:

Social Media Platforms 📱 (Content Moderation)
Law Enforcement 👮‍♂️
We followed a conventional deep-learning approach and developed a model from scratch that achieved 84.6% test accuracy. 🎯

Literature Review 📚
In our research, Convolutional Neural Networks (CNNs) emerged as the top method for deepfake detection. Several papers combined CNNs with techniques like attention maps 👁️ and frequency extractors to improve classification. CNNs are excellent at learning image features and perform well with limited data. 📈

Since our primary stakeholders are Social Media Platforms, we aimed to create a model with:

Excellent inference speeds ⚡ for scalable classification of millions of user-generated images
Explainability 📊 for classification results
Data and Methods 📊
Data
We worked primarily with image data 🖼️ and utilized publicly available datasets for deepfake detection:

Diverse Fake Face Dataset (msu.edu)
OpenForensics: In-The-Wild Dataset [V.1.0.0]
Given limited computing resources 💻, we created a custom dataset from DFFD consisting of:

10K real images 🖼️
6.9K deepfakes 🔴
Methods
Preprocessing involved:
Face detection using a pre-trained model 👀
Center-cropping images to 256x256 resolution 🖼️
Normalization of image data
We experimented with various CNN architectures (AlexNet, LeNet, ResNet), training them for 40 epochs ⏳ with a batch size of 75 on 16K images.

Results 📈
AlexNet achieved the highest performance:

98% training accuracy 🎯
84.6% test accuracy ✅
LeNet achieved 81% test accuracy.

Surprisingly, ResNet performed poorly with 46% accuracy despite having the highest parameter count, likely due to insufficient training data and epochs. 🤷‍♂️

Discussion 💬
It's essential for the model to learn deepfake artifacts 🔍 rather than just generic image features. While our models serve as a first-stage filter for content moderation, further testing on real-world data from social media platforms is required to improve their generalizability. 🌐

