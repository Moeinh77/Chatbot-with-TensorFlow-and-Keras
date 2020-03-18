# Chatbot-with-TensorFlow-and-Keras

### Some interesting answers from the bot:

* Q: Hello ?  A: hi tommy 
* Q: Who are you ?  A: i am the one that is all 
* Q: What are you doing ?  A: i am not listening you are going to report to the lab 
* Q: What are you doing ?  A: i steel
* Q: Do you want to go out ?  A: i am sorry niece 
### Dataset:  

 Cornell Movie Dialogs corpus contains a large metadata-rich collection of fictional conversations extracted from raw movie scripts.
 The corpus includes:
- 220,579 conversational exchanges between 10,292 pairs of movie characters
- involves 9,035 characters from 617 movies
- in total 304,713 utterances

I have used only 96048 pairs of these dialogs.

### Model:

The model is a 2 layer RNN with GRU as cells. The encoder is Bi-directional with 256 units and decoder is Uni-directional 512 units. Glove vectors with 100 dimensions is used az word embeddings. 

### Results:

### Tips for training the model:

* Instead of feeding a whole sequence to the network, I have fed time step x of a batch of data to the network.
* I used bidirectional GRU as the encoder, but decoder is unidirectional. It is due to the fact that input is known but output is generated at each step.
* I used Masked Loss. The loss for the padding inputs are considered 0.

### Setup:

### Related links:
