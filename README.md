# Chatbot-with-TensorFlow-and-Keras

### Some interesting answers from the bot:

* Q: Hello ?  A: hi tommy 
* Q: Who are you ?  A: i am the one that is all 
* Q: What are you doing ?  A: i am not listening you are going to report to the lab 
* Q: What are you doing ?  A: i steel
* Q: Do you want to go out ?  A: i am sorry niece 
* Q: Do you want ice ?  A: i am not a witch 
* Q: Let go ?  A: suit yourself  
* Q: i am sorry ?  A: you are not
 
### Dataset:  

 Cornell Movie Dialogs corpus contains a large metadata-rich collection of fictional conversations extracted from raw movie scripts.
 The corpus includes:
- 220,579 conversational exchanges between 10,292 pairs of movie characters
- involves 9,035 characters from 617 movies
- in total 304,713 utterances

I have used only 96048 pairs of these dialogs.

### Model:

The encoder is 1-layer Bi-directional GRU with 256 units and decoder is 2-layer Uni-directional GRU with 512 units.

### Results:

### Tips for training the model:

* I used small batch size of 32 for more stable training.
* Instead of feeding a whole sequence to the network, I have fed time step x of a batch of data to the network.
* I used bidirectional GRU as the encoder, but decoder is unidirectional. It is due to the fact that input is known but output is generated at each step.
* I used Masked Loss. The loss for the padding inputs are considered 0.
* Using a simpler model with a low dimenstion word embeddings turned out to be more effective. I used just one layer for encoder and 50-d GloVe word vectors.
* I applied dropout with a chance of 0.2 to encoder's input word embeddings .

### Setup:

* I trained the model on a Nvidia 1070-Ti GPU. Each epoch took about 3.5 mins

### Related links:
