# About
## Abstract
This repository presents a Recurrent Neural Network (RNN) model capable of classifying sounds into 10 distinct categories, covering nature sounds, human non-speech sounds, and more. The model boasts an impressive accuracy of 90% in achieving its classification task.The model operates by analyzing the processed spectrum of a WAV file, a two-dimensional representation of the sound's frequency content. Based on the processed data, the model predicts the corresponding sound category.This repository offers a clear and concise overview of a sound classification system utilizing RNNs, potentially serving as a valuable resource for those interested in exploring this field.


The repository consists of 4 key files, with the Natural_Sound_Recognition.ipynb housing the implementation code of the model and also facilitating the conversion of the WAV file into a spectrogram. Additionally, the requirements.txt file contains the necessary dependencies to run the model, while the instructions.txt provides detailed guidance for comprehending the repository's contents and utility. This comprehensive repository not only showcases the capabilities of RNNs in sound classification but also serves as a practical guide for individuals interested in exploring and implementing similar systems.

# Details
In this project we are using RNN(Recurrent Neural Network) model, I'll be explaining the working of RNN model:
A Recurrent Neural Network (RNN) is a type of artificial neural network specifically designed to handle sequential data, where the order of the data points matters. This makes them suitable for tasks like language translation, speech recognition, and time series analysis. Unlike traditional neural networks, RNNs have an internal memory (hidden state) that allows them to process information from previous steps in the sequence, influencing their output for the current step.


Recurrent Neural Networks (RNNs) are a class of artificial neural networks designed to handle sequential data, where the order of information matters. Unlike traditional neural networks, which treat each data point independently, RNNs can process information by considering the context of past data points.

## Key Concepts

### Sequential Data: 
RNNs are designed to handle data that comes in a sequence, where the order matters. Examples include text, time-series data (like stock prices), or audio signals.

### Hidden State (Memory): 
The core feature of an RNN is its "hidden state." This acts like a memory, allowing it to remember information from previous steps in the sequence.

### Looping Structure: 
RNNs process data in a loop. At each step of the sequence:
The RNN takes the current input and the previous hidden state as inputs.
It processes these inputs to produce a new output and an updated hidden state.
The updated hidden state is passed on to the next step in the sequence.

## Understanding the Process

### Initialization: 
The RNN starts with an initial hidden state (often set to zeros).
Input Processing: At each time step:
The current input (e.g., a word in a sentence) is combined with the hidden state from the previous step.
A neural network within the RNN processes this combined information.

### Output and Update:
The RNN generates an output (e.g., predicts the next word, classifies the sentiment of the text).
The hidden state is updated based on the current input and previous state, preserving relevant information across the sequence.
Repetition: This process repeats for each element in the sequence.

Here's a breakdown of how RNNs work:

1. The basic unit: The Cell:

The core of an RNN is a cell, which takes input, processes it, and outputs a value. This cell also has a memory state that allows it to store information from previous inputs.
During training, the cell learns how to update its internal parameters based on the current input and its previous state.

2. Information Flow:

An RNN processes data one step at a time. At each step, it:
Receives an input: This can be a new data point from the sequence.
Combines the input with its current memory state: This allows the network to consider the context of previous data points.
Activates its internal function: This function processes the combined input and memory, generating an output.
Updates its memory state: The cell updates its internal state based on the current input and its previous state. This allows it to "remember" relevant information for future processing.

3. Unfolding the RNN:

Imagine stacking multiple copies of the same cell one after another. This is how we create an unfolded RNN.
Each cell in the sequence receives the output from the previous cell as part of its input, allowing information to flow throughout the network.

4. Types of RNNs:

While the basic concept remains the same, there are different types of RNNs with specific functionalities:
Vanilla RNNs: These suffer from the vanishing gradient problem, where long-term dependencies become difficult to learn.
Long Short-Term Memory (LSTM) networks: These have additional mechanisms to better handle long-term dependencies.
Gated Recurrent Units (GRUs): Another variation that addresses the vanishing gradient problem with a simpler architecture than LSTMs.

5. Applications of RNNs:

RNNs are powerful tools for various tasks involving sequential data, such as:
Speech recognition
Machine translation
Music generation
Financial forecasting
Text summarization

The above explanation provides a basic understanding of how RNNs work. It's important to remember that RNNs are complex models with ongoing research and development. If you'd like to delve deeper, you can explore resources on LSTMs and GRUs, which are the most widely used RNN architectures in practice.


## Highlights

### WAV to Spectrum
First we have  understand the basic structure of a WAV file and how it's handled in Python. Just like an image is made up of pixels, a WAV file consists of audio samples. The sample rate represents the number of samples captured per second to convert analog audio to digital form. In this case, the sample rate is 44100 Hz, meaning each second of audio comprises 44100 samples. As the WAV file is 4 seconds long, it contains a total of 176400 samples.

The conversion from a WAV file to a spectrum involves traversing through different stages:

#### WAV to Waveform: 
In this stage, the digital representation of the audio samples is transformed into a waveform, which depicts the amplitude of the audio signal over time. This step involves reading the digital audio data from the WAV file and interpreting it as a continuous waveform.

![Wav](https://github.com/Akash8292/Natural_Sound_Recognition/assets/98084760/7d093421-0a8e-489c-9c12-b8392fd01f78)

![image](https://github.com/Akash8292/Natural_Sound_Recognition/assets/98084760/46086bb3-4288-4a44-8fad-0dc805eb23e4)

#### Waveform to Spectrogram:
The waveform is then transformed into a spectrogram, which is a visual representation of the spectrum of frequencies in the audio signal as they vary with time. This is achieved through techniques such as Short-Time Fourier Transform (STFT), which converts the audio signal into its frequency domain representation.

![image](https://github.com/Akash8292/Natural_Sound_Recognition/assets/98084760/902fd2ee-0ed0-4856-9d42-eb9cd493e0e2)



## Prerequisites

Python>=3.6

1. Clone the repository or download the zip file.
2. Install necessary packages using pip install -r requirements.txt
6. Run the Natural_Sound_Recognition.ipynb file to use the pretrained model on custom wav file, change path of model and wav file accordingly.
7. Read the instructions.txt for better understanding of repository.

## Future Scope

In future, I am looking forward to increasing the accuracy using data preprocessing (like data cleaning, data analysis) and also improve via trying out different models.
