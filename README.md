# Chatbot-with-TensorFlow-and-Keras

### Dataset:                       
 Cornell Movie Dialogs corpus contains a large metadata-rich collection of fictional conversations extracted from raw movie scripts.
 The corpus includes:
- 220,579 conversational exchanges between 10,292 pairs of movie characters
- involves 9,035 characters from 617 movies
- in total 304,713 utterances

### Model:


### Results:

### Tips for training the model:

* Instead of feeding a whole sequence to the network, I have fed time step x of a batch of data to the network.
* I used bidirectional GRU as the encoder, but decoder is unidirectional. It is due to the fact that input is known but output is generated at each step.
* I used Masked Loss. The loss for the padding inputs are considered 0.

### Setup:

### Related links:
