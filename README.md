# Timbre-Transfer-Using-Autoenocder-Generative-Model



# Autoencoder
An autoencoder is a type of artificial neural network used to learn data encodings in an unsupervised manner.
The encoder can then be used as a data preparation technique to perform feature extraction on raw data that can be used to train a different machine learning model.
In general, autoencoders work on the premise of reconstructing their inputs.


# Timbre of a Sound
Unlike other characteristics of a sound, it's hard to define timbre in terms of features. So instead of extracting the features to represent the timbre, we can use autoencoder to learn timbre representation from data itself. Which we can then use for timbre transfer purpose.
For this project I've trained Autoencoder learn to transfer flute timbre to any other sound of instruments.


# Project Pipeline


* Extracting fundamental frequency from given input audio
* Preprocessing audio datasets for training ( Audio to Spectrogram )
* Training model with fundamental frequency
* Training ends when output resembles the characteristics of input data
* Testing model with unseen data


# Result
#### Spectrogram of Accordian passed as input
![Original Spectrogram of Accordian](/output_audio/original.png)


https://user-images.githubusercontent.com/68271682/218297860-7c306719-3629-4cf5-9b0f-e13408d13804.mp4


#### Spectrogram of Flute reconstructed as output
![Generated Spectrogram of Flute](/output_audio/generated.png)

# Output Audio 
Reconstructed audio resembles the characteristics of flute but posses some noise due to noise in training data set & phase artifacts due to poor phase reconstruction in output audio.


https://user-images.githubusercontent.com/68271682/218297912-9dc0eda1-70d6-4fc3-8081-30be7499ba23.mp4



https://user-images.githubusercontent.com/68271682/218297884-a7bfdffb-19a1-4699-9210-7752682c844d.mp4


# Constraints of Project Workflow

This project approaches from the perpective that for given fundamental frequency of given input sound Autoencoder can generate a sound of flute for that fundamental frequency by learning the patterns of flute from training data. Following are the constraint for running this model:

* Works only for monophonic sound ( YIN algorithm works only for monophonic sound )
* Size of input and output are fixed ( Autoencoder accepts only predefined size for input and generates output of same size )
