# Speech-Command-Recognition
Compared three models for speech commands, the dataset used is [Speech Commands](https://arxiv.org/abs/1804.03209). [Speech Commands](https://arxiv.org/abs/1804.03209) is an audio dataset consiting of isloated-word commands spoken by different speakers.
Train set conists of 12000 such speech commands and test set consists of 4000 speech commands.
## M5
First M5 model was tested. This model consists of four convolution layers, each followed by a maxpool layer. This model consists of 0.5M parameters. Testing accuracy of 69% was achieved training this model for 20 epochs. More details about the modle can be found [here](https://arxiv.org/pdf/1610.00087.pdf)

## M11
Next, another model M11 was tested from the same paper. This model consists of five convolution layers, each followed by a maxpool layer. This model consists of 1.8M parameters. Using this model, testing accuracy of 69% was achieved.

## LSTM
Finally, LSTM was used to utilize the contextual information of speech commands. First 12 MFCC features are extracted from the audio. Then these features are fed to a LSTM model using a GRU layer of input size = 12, hidden features = 48. Then two fully connected layers are used. Using this model a test accuracy of 85% was achieved.
