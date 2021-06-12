1. Take the last code  (+tweet dataset) and convert that in such a war that:
   1. *encoder:* an RNN/LSTM layer takes the words in a sentence one by one and finally converts them into a single vector. **VERY IMPORTANT TO MAKE THIS SINGLE VECTOR**
   1. this single vector is then sent to another RNN/LSTM that also takes the last prediction as its second input. Then we take the final vector from this Cell
   1. and send this final vector to a Linear Layer and make the final prediction. 
   1. This is how it will look:
      1. embedding
      1. *word from a sentence +last hidden vector ->* encoder *-> single vector*
      1. *single vector + last hidden vector -> decoder -> single vector*
      1. *single vector -> FC layer -> Prediction*
1. Your code will be checked for plagiarism, and if we find that you have copied from the internet, then -100%. 
1. The code needs to look as simple as possible, the focus is on making encoder/decoder classes and how to link objects together
1. Getting good accuracy is NOT the target, but must achieve at least **45%** or more
1. Once the model is trained, take one sentence, "print the outputs" of the encoder for each step and "print the outputs" for each step of the decoder. ← **THIS IS THE ACTUAL ASSIGNMENT**

Dataset: <https://canvas.instructure.com/courses/2734517/files/138795503?wrap=1>

The Tweets.csv dataset is divided into 3 classes: Positive, Neutral, Negative

![](https://github.com/JahnaviRamagiri/END2.0/blob/main/Session6/images/tweets_label.png)

**Encoder Decoder Architecture:** 

Embedding: Every unique word in the input is converted to a 300 vector embedding

Encoder: The Embedding vector is passed on to an LSTM to get a 100 dimension vector output

Decoder: The encoder LSTM output is sent to the Decoder LSTM to get a 100 dimension vector output

Fully connected Layer: The decoder output is given to the fully connected layer to classify the output into 3 classes (Negative, Positive, Neutral)

The  Defined Parameters for each class are as mentioned below:

**Model Parameters**

![](https://github.com/JahnaviRamagiri/END2.0/blob/main/Session6/images/Model_param.png)

**Encoder and Decoder Outputs:**

![](https://github.com/JahnaviRamagiri/END2.0/blob/main/Session6/images/Encoder_decoder_output.png)

**Accuracy:**

![](https://github.com/JahnaviRamagiri/END2.0/blob/main/Session6/images/Acuracy.png)

