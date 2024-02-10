# Video-Text Clustering Summary:

## Table of contents
- [Video To Embedding](#video-to-embedding)
	1. [What is Video to Embedding?](#what-is-video-to-embedding)
	2. [Why do we need it?](#why-do-we-need-it)
	3. [The steps of Video to embedding](#the-steps-of-video-to-embedding)
	4. [I3D Model](#i3d-model)
- [Text Embedding](#text-embedding)
	1. [What is Text to Embedding?](#what-is-video-to-embedding)
	2. [Why do we need it?](#why-do-we-need-it)
	3. [Transformers](#transformers)
		1. [Bert](#bert)
		2. [GPT](#gpt)
- [Cross-Modal Retrieval](#cross-modal-retrieval)
	1. [What is Cross-Modal Retrieval?](#what-is-cross-modal-retrieval)


## Video To Embedding
### What is video to embedding
Video to embedding refers to the process of converting a video media file to a vector representation,those vectors are called **Embeddings** and their purpose is to capture the important elements of the video and their relationships,that way its easier for algorithms to work with the data.
### Why do we need it
Extracting the embeddings of videos is essential for performing such as video classification,complex analysis,video search,recommendation systems and content understanding.  
it can allow you to detect similar videos or even duplicate videos.  
Video embeddings can be used in conjunction with other modalities, such as text or audio embeddings, for more comprehensive analysis and understanding of multimedia content. 
### The steps of video embedding
There are two types of video to embedding techniques, the first includes splitting all of the frames into individual objects and the performing some kind of inference on them while the second approach involves using the video as is and feeding into a 3D CNN that is essentially a normal CNN that has a sliding window in 3 dimensions
To Extract Embeddings out of a Video there are multiple steps:

##### 1. <ins>Pre-Processing</ins>
Pre-processing has two forms when it comes to video data,first you break the video into individual frames,that is called **Frame Extraction**  
Instead of using all frames to create vector embeddings which may be computationally intensive we can use **Frame Sampling** which means only taking some of the frames,either chosen by intervals(10 frames per second) or choosing a fixed amount of frames per video and calculating the interval accordingly.  
Now you either process each frame separately or reconstruct the video with the preprocessed frames depending on your model(we use 3D CNNs so we reconstruct the video).
##### 2. <ins>Feature Extraction</ins>


### I3D Model
I3D, or Inflated 3D ConvNet, is a 3D convolutional neural network architecture designed for video classification and action recognition. It was introduced to extend the success of 2D convolutional neural networks (CNNs) in image classification to the domain of spatiotemporal video data. I3D was proposed by researchers from Facebook AI Research (FAIR) and Google.  

I3D starts with pre-trained 2D CNN models, such as Inception or ResNet, that were originally trained on large-scale image datasets like ImageNet.  

The 2D filters of the pre-trained models are "inflated" to 3D by replicating the 2D filters along the temporal dimension. This process allows the model to capture spatiotemporal features in video data.

#### Two Stream Architecture
Two Streams of information are used when processing and analyzing the video,one of the is the **RGB stream** which describes each frame and its RGB values at each pixel and the second one is the motion information,commonly represented by optical flow.  

Optical flow is a representation of the apparent motion of objects in a scene based on pixel intensity changes between consecutive frames.  
It provides information on how objects move between frames.  

In summary, the two-stream architecture in video analysis involves:

- **RGB Stream:** Capturing spatial appearance information by processing raw color frames.
- **Motion (Optical Flow) Stream:** Capturing temporal information related to the motion of objects in the video.
## Text Embedding

### What is text embedding
Text embedding refers to converting some text into tokens by a process called **Tokenization** and then feeding those tokens into a machine learning model which converts them into their vector representation
### Why do we need it
Text embedding provides a way to capture semantic meaning of words or phrases to then further perform ML Tasks such as semantic search over data,Classification of text and document summarization.

### Transformers
Transformers a class of deep learning models which are primarly used for NLP Tasks,although they have been extended to other domains like Computer Vision,Their usage is common due to their ability to handle long-range dependencies in sequences efficiently(Words that are far apart from each other in a sentence for example).
Here are the key points about Transformers:  

- **Self Attention Mechanism:** This allows the transformer model to weigh the importance of different words in a sequence when encoding or decoding information, the mechanism can capture the context between words that are far apart better than methods like RNN or CNN
- **Encoder-Decoder Architecture:** Transformers contain an encoder to understand the input text and a decoder to generate output text.  
the encoder processes the data in a bidirectional manner using self-attention mechanisms  
the decoder generates the output data based on the previously generated data in the output sequence and it incorporates encoder-decoder attention where it to the output of the encoder and leverages the contextual information encoded during the input processing stage

- **Positional Encoding:** Transformers incorporate positional encoding to understand the order of words in a sequence,to capture the sequential nature of sentences effectively.
- **Multi-Head Attention:** Transformers use these attention mechanisms to attend and capture aspects of context and meaning from multiple parts of the text simultaneously.	 

#### Bert
Bert  (Bidirectional Encoder Representations from Transformers) is an advanced NLP model developed by google,here are some of its defining features:  

1. **Bi-Directional**: unlike other models which are uni-directional,this means they only capture context from preceding or succeeding words in a sentence,Bert can capture contextual information from both, this allows it to better understand the meaning of words.  
2. **Large-Scale Pre-training:** BERT is pre-trained on large-scale corpora of text, including vast amounts of web text and books. This extensive pre-training data allows BERT to learn rich and generalizable representations of language, which can be fine-tuned for various downstream tasks.
3. **PreTraining Tasks:** Bert employs two main pre-training tasks:
	- MLM(Masked Language Model) which means random words in an input sentence are masked or removed and the model neeeds to guess the missing words,making it use the context of words around.
	- NSP(Next Sentence Prediction),The model is trained to predict whether two sentences appear consecutively in the original text or not. This encourages BERT to capture relationships between sentences and understand discourse-level context.
#### GPT

GPT is a generative model, meaning it can generate new text based on the patterns it learned during pre-training. By sampling from the learned probability distribution over the vocabulary, GPT can produce sequences of text that resemble human-written language.  

```This Basically means the gpt guesses what is the most likely to be the next word based on all previous words```

## Cross-Modal Retrieval
### What is Cross-Modal Retrieval
