# Assignment-2
<h1>Encoder-Decoder Models using RNN and LSTM</h1>
<h2>Model structure </h2>
<p>
The proposed model for English-to-French translation is based on a Sequence-to-Sequence (Seq2Seq) architecture implemented using Recurrent Neural Networks (RNNs), specifically Long Short-Term Memory (LSTM) units.

The architecture comprises two primary components:

Encoder:
The encoder processes the input English sentence. It includes an Embedding layer that converts input tokens into dense vector representations, followed by an LSTM layer that captures the temporal dependencies within the input sequence. The encoder outputs its internal states—hidden and cell states—which are used to initialize the decoder.

Decoder:
The decoder generates the translated French sentence. It also begins with an Embedding layer, followed by an LSTM layer that takes the encoder’s final states as its initial states. The decoder predicts each word step-by-step, and a Dense layer with softmax activation is used to produce a probability distribution over the target vocabulary at each time step.

The model is trained using the categorical cross-entropy loss function and optimized with an appropriate optimizer such as Adam. The training process monitors accuracy as the key performance metric.

This architecture enables the model to learn meaningful alignments between input and output sequences without the use of explicit attention mechanisms.
</p>
<hr>
<h2>Instructions to run the code </h2>
<p>
  To execute the Encoder-Decoder based English-to-French translation model:

1.Set up the Environment:
Ensure that Python, Jupyter Notebook, and the required libraries (numpy, pandas, matplotlib, tensorflow) are installed.

2.Load the Dataset:
Use the fra.txt dataset from Tatoeba, containing English-French sentence pairs. The dataset must be placed in the project directory.

3.Data Preprocessing:

Clean and normalize the text data.

Tokenize and pad both input (English) and target (French) sequences.

Split the data appropriately for training and validation.

4.Model Architecture:
Define an encoder-decoder structure using LSTM layers in Keras, including embedding layers and dense output layers for softmax-based prediction.

5.Training:
Compile the model using categorical crossentropy loss and train it using the prepared sequences. A subset of data (e.g., 10,000 samples) may be used for faster execution.

6.Evaluation:
Translate and print multiple test sentences using the trained model to verify the correctness of the sequence generation.

7.Visualization:
Plot the training and validation loss curves using matplotlib to analyze model performance and training stability.
</p>
<hr>
<h2>Sample outputs </h2>
<p>
  Input: hello<br>
Output: bonjour

Input: how are you<br>
Output: comment ça va

Input: i love you<br>
Output: je t'aime

Input: thank you<br>
Output: merci

Input: what is your name<br>
Output: comment tu t'appelles
</p>











