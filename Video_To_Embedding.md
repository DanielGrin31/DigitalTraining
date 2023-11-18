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
	3. [Bert](#bert)
	4. [GPT](#gpt)
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
### Why do we need it
### Bert
### GPT
## Cross-Modal Retrieval
