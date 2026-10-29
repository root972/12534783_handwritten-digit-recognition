# 12534783_handwritten-digit-recognition
Research and project planning for handwritten digit recognition using TensorFlow/Keras, comparing traditional machine learning with a convolutional neural network (CNN) on the MNIST dataset.
Handwritten Digit Recognition: Traditional Machine Learning vs. Deep Learning

Matriculation Number: 12534783 Course: Applied Deep Learning Project Type: Beat the Classics

1. //Project Idea

I want to build a system that recognises handwritten digits from 0 to 9, and I want to compare two ways of doing it. The first is Logistic Regression, a traditional machine learning method. The second is a Convolutional Neural Network (CNN), which is a deep learning method.

I picked this topic because it's a good way to learn how image classification actually works. It also lets me put a simple model next to a neural network and see how each one does on exactly the same data.

I'll use Python with TensorFlow/Keras for the CNN and a standard machine learning library for Logistic Regression.

2. Project Type: Beat the Classics

In "Beat the Classics" you take a traditional method and compare it with a deep learning approach.

In my project, Logistic Regression is the classic baseline and the CNN is the deep learning model. Both get the same dataset, so the comparison is fair.

I'll look at accuracy, training time and the kinds of mistakes each model makes. What I want to find out is whether the CNN is really better at reading handwritten digits, and if it is, whether that comes with a higher computational cost.

3. Related Research
3.1 Paper 1: Comparison of Classical Machine Learning Algorithms in the Task of Handwritten Digits Classification

Authors: Oleksandr Voloshchenko and Małgorzata Plechawska-Wójcik Year: 2021 Journal: Journal of Computer Sciences Institute, Volume 21, pages 279–286.

Journal article
Full-text PDF
DOI

Summary and relevance to my project

This paper compares several traditional machine learning algorithms on MNIST: Logistic Regression, Support Vector Machines, Decision Trees, Random Forests and k-Nearest Neighbours. The authors don't only look at accuracy. They also measure training speed, prediction speed and how heavily each algorithm loads the machine.

It's useful for me because it shows there are plenty of ways to recognise digits without deep learning, and it backs up my choice of Logistic Regression as a baseline to compare the CNN against.

3.2 Paper 2: Recognition of Handwritten Number using Convolutional Neural Network with TensorFlow

Authors: Vaibhav Taank, Atish Kumar and Ravi Sharma Year: 2024 Source: SSRN

Paper and abstract
DOI

Summary and relevance to my project

This paper uses a CNN built with TensorFlow to recognise handwritten numbers. CNNs work well for images because the convolutional layers pick up patterns like edges and shapes by themselves, instead of treating every pixel as unrelated.

For me it's a good example of how TensorFlow is used for this task, so it gives me a starting point for my own CNN.

Two notes. The paper uses a split of 42,000 training images and 28,000 test images, but I'll use the standard MNIST split instead. Also, the paper is on SSRN and I haven't been able to check whether it was peer reviewed.

3.3 What I Learned from the Papers

Together the papers show that digit recognition can be done with traditional machine learning and with deep learning. The traditional methods are a solid starting point, while CNNs can learn image features straight from the data.

So I'll compare Logistic Regression and a CNN on the same dataset. I don't want to assume one of them wins before I've tested it, so the results from my own experiments will decide that.

4. Dataset Description

I'll use the MNIST handwritten digits dataset, which is public and very commonly used for image classification.

It has 70,000 grayscale images of digits from 0 to 9, each 28 × 28 pixels. The standard split is 60,000 images for training and 10,000 for testing.

I'll load it directly through TensorFlow/Keras, so there's nothing to collect or label by hand. Before training I'll look at some of the images and labels, check the dimensions and normalise the pixel values.

Both models will use the same training and test data, which keeps the comparison meaningful.

Dataset source: MNIST dataset in the Keras documentation

5. Proposed Methodology
5.1 Traditional Machine Learning Model

I'll start with Logistic Regression as the baseline. Each 28 × 28 image gets flattened into a vector of 784 pixel values, and the model predicts which of the ten digit classes it belongs to. It's a fairly simple model, which makes it a good thing to compare the CNN against.

5.2 Deep Learning Model

For the deep learning side I'll build a CNN in TensorFlow/Keras. It will have convolutional layers to learn patterns from the images, followed by pooling and classification layers. I'll train it on the MNIST training set and try a few settings, like the learning rate and the number of epochs.

5.3 Evaluation and Comparison

Once both models are trained, I'll evaluate them on the same held-out test set and compare:

Accuracy: the share of digits classified correctly.
Confusion matrix: which digits get mixed up with which.
Training time: how long each model takes to train.

I'll keep the test set out of any tuning decisions so it doesn't leak into training. The results will go into a table or simple plots.

5.4 Simple Demonstration Application

If time allows, I'll build a small web app where you can draw a digit and get a prediction from the trained model. The app will convert the drawing into the format the model expects and show the predicted digit. It makes the project easier to demo than just showing accuracy numbers.

6. Work Breakdown Structure and Time Estimates

This is my first estimate of the time for the whole project. It might shift a bit once I start implementing.

Task	Planned work	Estimated time
Dataset collection and preparation	Load MNIST, inspect images and labels, prepare inputs	5 hours
Designing and building the models	Implement Logistic Regression and the CNN	7 hours
Training and fine-tuning	Train both models, try settings and record results	8 hours
Building the application	Create a drawing interface and connect the trained model	7 hours
Writing the final report	Explain methods, results and limitations	6 hours
Preparing the presentation	Slides, visualisations and a demo	5 hours
Total		38 hours
Breakdown of the Work

1. Dataset collection and preparation: 5 hours Load MNIST, look at sample images, check labels and dimensions, and prepare the pixel values for training.

2. Designing and building the models: 7 hours Implement the Logistic Regression baseline and the CNN, and set up the loss function, optimiser and evaluation metrics for the network.

3. Training and fine-tuning: 8 hours Train both models, compare results and try different CNN settings. I'll record accuracy, training time and confusion matrices.

4. Building the application: 7 hours Make a simple interface for drawing digits, connect it to the trained model and make sure the input is processed correctly before prediction.

5. Writing the final report: 6 hours Describe the dataset, explain the models, present the results and discuss how the two approaches differ. I'll also cover limitations and check the report for clarity and spelling.

6. Preparing the presentation: 5 hours Make slides on the idea, dataset, methods and results, plus a short demo if the app is working.

7. Expected Outcome

At the end I want two working models for digit recognition and a clear comparison of how they perform.

I expect this to help me understand how a traditional model and a CNN differ on image data. I'm not assuming the result in advance; the experiments will show it.

The planned app will give a simple way to demo the trained model with a digit drawn by hand.

8. Repository Plan

I'll use GitHub to keep the files and documentation organised.

Repository name: 12534783_handwritten-digit-recognition

I'm starting with this README, which has the project idea, references, dataset description, methodology and time estimates. As the project moves forward I'll add the code, evaluation results, the app and the final documentation.
