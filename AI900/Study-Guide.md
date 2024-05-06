# AI-900 Study Guide

Study Guide / Notes created using: 
- https://learn.microsoft.com/en-us/training/courses/ai-900t00
- https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/ai-900

## Skills Measured / Objective Notes 
- https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/ai-900


### Describe Artificial Intelligence workloads and considerations (15–20%)
#### Identify features of common AI workloads 
- Identify features of content moderation and personalization workloads 
- Identify computer vision workloads 
- Identify natural language processing workloads 
- Identify knowledge mining workloads 
- Identify document intelligence workloads 
- Identify features of generative AI workloads 
#### Identify guiding principles for responsible AI 
- Describe considerations for fairness in an AI solution 
- Describe considerations for reliability and safety in an AI solution 
- Describe considerations for privacy and security in an AI solution 
- Describe considerations for inclusiveness in an AI solution 
- Describe considerations for transparency in an AI solution 
- Describe considerations for accountability in an AI solution 


### Describe fundamental principles of machine learning on Azure (20–25%)
Identify common machine learning techniques 
- Identify regression machine learning scenarios 
- Identify classification machine learning scenarios 
- Identify clustering machine learning scenarios 
- Identify features of deep learning techniques 
Describe core machine learning concepts 
- Identify features and labels in a dataset for machine learning 
- Describe how training and validation datasets are used in machine learning 
Describe Azure Machine Learning capabilities 
- Describe capabilities of automated machine learning 
- Describe data and compute services for data science and machine learning 
- Describe model management and deployment capabilities in Azure Machine Learning 



### Describe features of computer vision workloads on Azure (15–20%)
Identify common types of computer vision solution 
- Identify features of image classification solutions 
- Identify features of object detection solutions 
- Identify features of optical character recognition solutions 
- Identify features of facial detection and facial analysis solutions 
Identify Azure tools and services for computer vision tasks 
- Describe capabilities of the Azure AI Vision service 
- Describe capabilities of the Azure AI Face detection service 



### Describe features of Natural Language Processing (NLP) workloads on Azure (15–20%)
#### Identify features of common NLP Workload Scenarios 
- Identify features and uses for key phrase extraction 
- Identify features and uses for entity recognition 
- Identify features and uses for sentiment analysis 
- Identify features and uses for language modeling 
- Identify features and uses for speech recognition and synthesis 
- Identify features and uses for translation 
#### Identify Azure tools and services for NLP workloads 
- Describe capabilities of the Azure AI Language service 
- Describe capabilities of the Azure AI Speech service 



### Describe features of generative AI workloads on Azure (15–20%)
#### Identify features of generative AI solutions 
- Identify features of generative AI models 
- Identify common scenarios for generative AI 
- Identify responsible AI considerations for generative AI 
#### Identify capabilities of Azure OpenAI Service 
- Describe natural language generation capabilities of Azure OpenAI Service 
- Describe code generation capabilities of Azure OpenAI Service 
- Describe image generation capabilities of Azure OpenAI Service 


## AI Fundamentals - Course Notes 
- https://learn.microsoft.com/en-us/training/courses/ai-900t00


### Fundamental AI Concepts
- Machine learning - often the foundation of an AI system, and is the way we "teach" a computer model to make predictions and draw conclusions from data.
  - Microsoft Azure provides the Azure Machine Learning services - a cloud-based platform for creating, managing, and publishing machine learning models. Azure Machine Learning Studio offers multiple authoring experiences such as: automated machine learning, Azure Machine Learning Designer (no-code development of ml solutions), Data metric visulaization, and Notebooks 
- Computer vision - capabilities within AI to interpret the world visually through cameras, video, and images
  - area of AI that deals with visual processing
  - Seeing AI app - designed for the blind and low vision community, this app harnesses AI to open up the visual world and describe nearby people, text and objects
  - most computer vision solutions are based on ML models that can be applied to visual input from cameras, videos, or images.
  - Common computer vision tasks:
      - Image classification - training a ML model to classify images based on their contents.
      - Object classification - these ML models are tarined to classify individual objects within an image, and identify their location with a bounding box. ex. idenitfy the location of different classes of vehicle.
      - semantic segmentation - an advanced ML technique in which individual pixels in the image are classified accordoing to the object to which they belong.
      - Image analysis - extract information from images, including 'tags', that can help catalog the image or even descriptive captions that summarize the sceen show in the image
      - Face detection, analysis, and recognition - face detection is a specialized form of object detection that locates human faces in an image.
      - Optical character recognition (OCR) - a technique used to detect and read text in images. you can use OCR to read text in photographs or to extract information from scanned documents such as letters, invoices, or forms.
  - Computer vision services in Microsoft Azure
    - Microsoft's Azure AI vision to develop computer vision solutions. some features include: image analysis, face, and optical character recognition (OCR) 
- Natural language processing - capabilities within AI for a computer to interpret written or spoken language, and respond in kind
  - NLP is the area of AI that deals with creating software that understands written and spoken language.
  - NLP enables you to: analyze and interpret text in documents, email messages, and other sources; interpret spoken language and syntehsize speech resposnes; automatically translate spoken or written phrases between languages; interpet commands and determine appropriate actions.
  - Microsoft's Azure AI Language tool - can be used to build NLP solutions. Azure AI speech used to buiold NLP solutions too.
- Document intelligence - capabilities within AI that deal with managing, processing, and using high volumes of data found in forms and documents
  - deals with managing, processing, and using high volumes of a variety of data found in forms and documents.
  - Azure AI Document Intelligence - build solutions that manage and accelerate data collection from scanned documents. 
- Knowledge mining - capabilities within AI to extract information from large volumes of often unstructured data to create a searchable knowledge store
  - solutions that involve extracting information from large volumes of often unstructured data to create a searchable knowledge store.
  - Azure AI Search - has a tool for buiding indexews. The indexes can be used for internal use only, or to enable searchable content on public facing internet assets. 
- Generative AI - capabilities within AI that create original content in a variety of formats including natural language, image, code, and more
  - describes a category of capabilities within AI that create original content. people typically interact with gen AI that has been built into chat apps.
  - Gen AI apps take in natural language input, and return appropriate responses in a variety of formats including natural language, image, code, and audio.
  - Azure OpenAI service - cloud solution for deploying, customizing, and hosting gen AI models.
 
- Challenges and risks with AI
  - bias can affect results
  - errors may cause harm
  - data could be exposed
  - solutions may not work for everyone
  - users must trust a complex system
  - who's liable for AI-driven decisions?
 
- Responsible AI
  - Fairness
  - Reliability and safety
  - Privacy and security
  - Inclusiveness
  - Transparency
  - Accountability 


### Fundamentals of Machine Learning
- goal of ML is to use data to create a predictive model that can be incorporated into a software app or service.
- ML has it's origins in statistics and mathematical modeling of data. fundamental idea of ML is to use data from past observations to predict unknown outcomes or values.
- Types of ML
    - Supervised ML - ML algorithms in which the training data includes both feature values and known label values.
      - Regression - label predicted by the model is a numeric value
      - Classification - label represents a categorization, or class.
        - Binary Classification
        - Multiclass Classification 
    - Unsupervised ML - involves training models using data that consists of only feature values without any known labels.
        - Clustering - these algorithms identify similarities between observations based on their features, and groups them into discrete clusters. 
- Regression
    - these models are trained to predict numeric label values based on training data that includes both features and known labels.
    - Regression evaluation metrics
        - Mean Absolute Error (MAE)
        - Mean Squared Error (MSE)
        - Root Mean Squared Error (RMSE)
        - Coefficient of Determination (R-squared) 
    - Iterative training 
- Binary Classification
    - supervised ML technique. these algorithms are used to train a model that predicts one of two possible labels or a single class.
    - Binary classification evaluation metrics
        - Confusion matrix - a matrix of the number of correct and incorrect predictions for each possible class label. 
        - Accuracy - the proportion of predictions that the model got right
        - Recall - a metric that measures the proportion of positive cases that the model identified correctly.
        - Precision - measures the proportion of predicted positive cases where the true label is actually positive.
        - F1-score - an overall metrics that combines recall and precision.
        - Area under the curve (AUC) - another name for the true positive rate (TPR). equivalent metric is the false positive rate (FPR).  these metrics are used to evaluate a model by plotting a received operator characteristic (ROC) curve that compares the TPR and FPR for every possible threshold value between 0.0 and 1.0. 
- Multiclass classification
    - used to calculate probability for multiple class labels.
    - one-vs-rest (OvR) algorithms - trains a binary classification function for each class, each calculating the probability that the observation is an example of the target class. each function calculates the probability of the observation being a specific class compared to any other class.
    - Multinomial algorithms - creates a single function that returns a multi-valued output.  the output is a vector (an array of values) that contains the probability distribution of all possible classes - with a probability score for each class which when totaled add up to 1.0
- Clustering
    - form of unsupervised ML. Observations are grouped into clusters based on similarities in their data values, or features.
    - no known labels in the dataset, just features.
    - evaluating a clustering model: average distance to clusetr center, average distance to other center, max distance to cluster center, silhoutette 
- Deep Learning - an adv. form of ML that tries to emulate the way the human brain learns. the creation of an artificial neural network that simulates electrochemical activity in biological neurons by using mathematical functions. 
- Azure Machine Learning

### Fundamentals of Azure AI Services


### Fundamentals of Computer Vision


### Fundamentals of Facial Recognition


### Fundamentals of optical character recognition


### Fundamentals of Text Analysis with the Language Service


### Fundamentals of question answering with the Language Service


### Fundamentals of conversational language understanding


### Fundamentals of Azure AI Speech


### Fundamentals of Azure AI Document Intelligence


### Fundamentals of Knowledge Mining and Azure AI Search


### Fundamentals of Generative AI


### Fundamentals of Azure OpenAI Service


### Fundamentals of Responsible Generative AI

