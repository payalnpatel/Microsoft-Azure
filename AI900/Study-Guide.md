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
- Azure AI Services built on 3 principles: prebuilt and ready to use, accessed through APIs, available on Azure
- APIs - application programming interfaces that define the information that is required for one component to use the services of the other. enable software components to communicate, so one side can be updated without stopping the other from working.
- Azure AI services are cloud-based, you need to create a resource to use them. 2 types of AI service resources: multi-service, or single-service.
- Multi-service resource: a resource created in Azure portal that provides access to multiple Azure AI services with a single key and endpoint. use this when you need several AI services or are exploring AI capabilities. when you use an Azure AI services resource, all your AI services are billed together.
- Single-service resources: a resource created in the Azure portal that provides access to a single Azure AI service, such as Speech, Vision, Language, etc. Each Azure AI service has a unique key and endpoint. These resources might be used when you only require one AI service or want to see cost info separately.
- studio interfaces provide a friendly user interface to explore Azure AI services - Vision Studio, Language Studio, Speech Studio, Content Safety Studio.
- authentication - the process of verifying that the user or service is who they say they are, and that they are authorized to use the service.
- Part of what an API does is to handle authentication. whenever a request is made to use an Azure AI services resource, that request must be authenticated. this authentication process uses an endpoint and a resource key. the resource key protects the privacy of your resource - to ensure this is always secure, this can be changed periodically.
- API - application programming interfaces (APIs) enable software components to communicate, so one side can be updated without stopping the other from working.
- Artificial Intelligence (AI) - computer programs that respond in ways that are normally associated with human reasoning, learning, and thought.
- Azure AI Services - a portfolio of AI services that can be incorporated into applications quickly and easily without specialist knowledge. Azure AI services is also the name for the multi-service resource created in the Azure portal that provides access to several different Azure AI servicdes with a single key and endpoint.
- Endpoint - the location of a resource, such as an Azure AI service.
- Key - a private string that is used to authenticate a request.
- Machine learning - the ability for computer programs to learn from large amounts of data, in a process known as "training".
- Multi-service resource - the AI service resource created in the Azure portal that provides access to a bundle of AI services.
- Single-service resource - a resource create in the Azure portal that provides access to a single Azure AI service, such as Speech, Vision, Language, etc. Each Azure AI Service has a unique key and endpoint.
- RESTful API - a scalable web application programming interface used to access Azure AI services. 

### Fundamentals of Computer Vision
- Computer vision is one of the core areas of AI, and focuses on creating solutions that enable AI applications to "see" the world and make sense of it.
- To a computer, an image is an array of numeric pixel values. each pixel has a value between 0 (black) and 255 (white); with values between these bounds representing shades of gray. a single layer of pixel values represents a grayscale image. in reality, most digital images are multidimensional and consist of 3 layers (known as channels) that represent red, green, and blue (RGB) color hues.
- Using filters to process images - a filter is defined by one or more arrays of pixel values, called filter kernels. the kernel is then convovled across the image, calculating a weighted sum for each 3x3 patch of pixels and assigning the result to a new image.
- CNNs - Convolutional neural networks - one of the most common ML model architectures for computer vision. CNNs use filters to extract numeric feature maps from images, and then feed the feature values into a deep learning model to generate a label prediction.
- During the training process for a CNN, filter kernels are initially defined using randomly generated weight values.
- CNNs have been at the core of computer vision solutions for many years. commonly used to solve image classification problems, they are also the basis for more complex computer vision models.
- Object detection models combine CNN feature extraction lyaers with the identification of regions of interest in images to locate multiple classes of object in the same image.
- in another AI discipline, natural language processing (NLP), another type of neural network architecture, called a transformer has enabled the development of sophisticated models for language. Transformers work by processing huge volumes of data, and encoding language tokens (representing individual words or phrases) as vector-based embeddings (arrays of numeric values). an image encoder extracts features from iamges based on pixel values and combines them with text embeddings by cerating a language encoder. 
- multi-modal models - model is trained using a large volume of captioned images, with no fixed labels.
- Microsoft Florenece model - multi-modal model. trained with huge volumes of captioned images from the Internet, it includes both a language encoder and an image encoder. Florenece is an example of a foundation model. in other words, a pre-trained general model on which you can build multiple adaptieve models for specialist tasks. Florence can be used as a foundation model for adaptive models that perform: image classification, object detection, captioning, tagging
- image classification - identifying which category an image belongs
- object detection - locating individual objects within an iamge
- captioning - generating appropriate descriptions of images
- tagging - compiling a list of relevant text tags for an image
- Azure AI Vision service provides prebuilt and customizable computer vision models that are based on the Florence foudnation model and provides various powerful capabilities.
- To use Azure AI Vision, a resource needs to be created in a Azure subscription.
- Azure AI Vision - a specific resource for the Azure AI Vision service - use this if you don't intend to use other Azure AI Services, or if you want to track utilization and costs for this service separately.
- Azure AI Services - a general resource that includes Azure AI Vision and other Azure AI Services.  use this resource type if you polan to use multiple AI Services and want to simlify administration and development.
- An image classification model is used to predict the category, or class of an image.
- Object detection models detect and classify objects in an image, returning bounding box coordinates to locate each object.
- Computer vision is built on the analysis and manipulation of numeric pixel values in images. ML models are trained using a large volume of images to enable common computer vision scenarios, such as image classification, object detection, automated image tagging, optical character recognition, etc. 

### Fundamentals of Facial Recognition
- face detection and analysis is an area of AI which uses algorithms to locate and analyze human faces in images or video content.
- There are many applications for face detection, analysis, and recognition -- security, social media, advertising, missing personas, identity validation
- Face detection involves identifying regions of an image that contain a human face, typically by returning bounding box coordinates that form a rectangle around the face.
- With face analysis, facial features can be used to train machine learning models to return other information, such as facial features such as nose, eyes, eyebrows, lips, etc.
- A further application of facial analysis is to train a machine learning model to identify known individuals from their facial features. This is known as facial recognition, and uses multiple images of an individual to train a model. This trains the model so that it can detect those individuals in new images on which it was trained.
- Azure AI Face service - provides pre-trained models to detect, recognize, and analyze faces.
- Microsoft Azure provides multiple AI services that can be used to detect and analyze faces, including:
    - Azure AI Vision - offers face detection and some basic face analysis, such as returning the bounding box coordinates around an image
    - Azure AI Video Indexer - can be used to detect and identify facess in a video
    - Azure AI Face - offers pre-built algorithms that can detect, recognize, and analyze faces 
- Azure face service can return the rectangle coordinates for any human face found in an image, as well as a series of attributes related to the face such as:
    - Accessories
    - Blur - how blurred the face is
    - Exposure - whether image is under or over exposed.
    - Glasses
    - Head pose - the face's orientation in a 3D space
    - Mask - whether individual is wearing a mask
    - Noise - refers to visual noise in the image.
    - Occlusion - determines if there might be objects blocking the face in the image. 
- Responsible AI use
    - Limited access policy requires customers to submit an intake form to access add'l Azure AI Face service capabilitys -- the ability to compare faces for similarity, the ability to identify named individuals in an image.
- Azure resources for Face -- Face or Azure AI Services
- Tips for more accurate results
    - Image format - support images are JPEG, PNG, GIF, and BMP
    - File size - 6 MB or smaller
    - Face size range -- 26 x 26 up to 4096 x 4096 pixels -- smaller or larger faces will not be detected
    - Other issues - face detection can be impaired by extreme face angles, extreme lighting, and occlusion (objects block the face such as a hand) 

### Fundamentals of optical character recognition
- OCR enables AI to read text in images, enabling applications to extract information from photographs, scanned documents, and other sources of digitized text.
- Automating text processing can improve the speed and efficiency of work by removing the need for manual data entry. the ability to recognize printed and handwritten text in images is beneficial in scenarios such as note taking, digitizing medical records or historical documents, scanning checks for bank deposits, etc.
- The ability for computer systems to process written and printed text is an area of AI where computer vision intersects with natural language processing. Vision capabilities are needed to 'read' the text, and then NLP capabilities make sense of it.
- OCR is the foundation of processing text in images and uses ML models that are trained to recognize individual shapes as letters, numerals, punctuation, or other elements of text. Much of the early work on implementing this kind of capability was performed by postal services to support automatic sorting of mail based on postal codes.
- Azure AI Vision service has the ability to extract machine-readable text from images. Azure AI Vision's Read API is the OCR engine that powers text extraction from images, PDFs, and TIFF files. OCR for images is optimized for general, non-document images that makes it easier to embed OCR in your user experience scenarios.
- Read API, a.k.a., Read OCR engine, uses the latest recognition models and is optimized for images that have a significant amount of text or have considerable visual noise.
- the OCR engine takes in an image file and identifies bounding boxes, or coordinates, where items are located within an image. in OCR, the model identifies bounding boxes around anything that appears to be text in the image.
- Calling the Read API returns results arranged in the following hierarchy:
    - Pages - one for each page of text, including info about page size and orientation
    - Lines - the lines of text on a page
    - Words - the words in a line of text, including the bounding box coordinates and text itself 
- Azure AI Vision or Azure AI services
- Once you've created a resource, can use Azure AI Visions Read API through: Vision Studio, REST API, SDKs (Python, C#, JavaScript)
- Azure AI Vision studio gives access to APIs through GUI & does not require coding to get started.
- Azure AI Vision - raw results returned in JSON -- to build OCR apps need to work with an SDK or REST API.

### Fundamentals of Text Analysis with the Language Service
- Natural Language Processing (NLP) - an area within AI that deals with understanding written or spoken language, and responding in kind.
- Text analysis - describes NLP processes that extract information from unstructured text.
- Azure AI Language - a cloud-based service that includes features for understanding and analyzing text. Includes various features that support sentiment analysis, key phrase identification, text summarization, and conversational language understanding.
- corpus - a body of text
- Tokenization 
    - the first step in analyzing a corpus, is to break it down into tokens. tokens can be generated for words, partial words, combination of words, and punctuation.
    - Text normalization - before generating tokens, you may choose to normalize the text by removing punctuation and changing all words to lower case. For word frequency analysis, this improves overall performance.  however, semantic meaning may be lost
    - stop word removal - stop words are words that can be removed from the analysis. (i.e, 'the', 'a', 'at', etc.) These words make it easier for people to read, but add little semantic meaning. by removing these words, a text analysis solution may be able to better identify the important words.
    - n-grams - multi-term phrases.  A single word is a unigram, two word phrase is a bi-gram, a three word phrase is a tri-gram, etc. by considering words as a group of words, a ML model can make better sense of the text.
    - Stemming - a technique in which algorithms are applied to consolidate words before counting them, so that words with the same root are interpetted as being the same token (i.e. power, powered, powerful)
- Frequency Analysis
    - after tokenizing the words, you can perform some analysis to count the number of occurrences of each token.
- ML for text clasification - a common application is to train a model that classifies text as positive or negative in order to perform sentiment analysis or opnion mining.
- Semantic language models
- Azure AI Language - text analysis features 
  - Named entity recognition - identifies people, places, events, and more. this feature can also be customoized to extract custom categories.
  - Entity linking - identifies known entities together with a link to Wikipedia
  - Personal identifying information (PII) detection
  - language detection
  - sentiment analysis and opinion mining
  - summarization
  - key phrase extraction

### Fundamentals of question answering with the Language Service
- Conversational AI describes solutions that enable a dialog between an AI agent and a human. generically, conversational AI agents are known as bots. People can engage with bots through channels such as web chat interfaces, email, social media platforms, etc.
- Azure AI Language's question answering feature provides ability to create conversational AI solutions.
- Question answering supports natural language AI workloads that require an automated conversational element.
- Can create a user support bot using a combination of 2 services: Azure AI Language (includes a custom question answering feature that enables you to create a knowledge base of question and answer pairs that can be queried using natural language input), and Azure AI Bot Service (provides a framework for developing, publishing, and managing bots on Azure).
- Azure AI Language customer answering feature enables you to define and pubish a knowledge base of questions and answers with support for natural language querying.
- Azure AI Bot Service - can use a knowledge base to deliver a bot that responds intelligently to user questions and over multiple communication channels. 

### Fundamentals of conversational language understanding


### Fundamentals of Azure AI Speech


### Fundamentals of Azure AI Document Intelligence


### Fundamentals of Knowledge Mining and Azure AI Search


### Fundamentals of Generative AI


### Fundamentals of Azure OpenAI Service


### Fundamentals of Responsible Generative AI

