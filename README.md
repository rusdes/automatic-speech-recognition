# Project: DNN Speech Recognizer

A deep neural network that functions as part of an end-to-end automatic speech recognition (ASR) pipeline.

We begin by investigating the LibriSpeech dataset that will be used to train and evaluate the models. First we convert any raw audio to feature representations that are commonly used for ASR. We will then move on to building neural networks that can map these audio features to transcribed text. After implementing the basic types of layers that are often used for deep learning-based approaches to ASR, we create the final model which incorporates:
- A convolution layer: we saw that it leads to better results because these find patterns.
- Batch Normalization: Batch Normalization helps to fasten the learning
- 2 bidirectional RNN layers: I added two bidirectional RNN layers because we've seen that the results are better with them than simple RNN. Since the speech outputs words are related to both the words spoken before and after that word, a bidirectional layer makes the most sense. Also, two layers would work better than a single layer because the increased complexity would help.
- Dropout: to avoid overfitting.
- TimeDistributed layer: This will be used to find more complex patterns in the dataset.
- Softmax activation function: output probabilities

At the end we have 1,246,829 parameters and great results with a training loss of 60.5124 and a validation loss of 113.4239.
