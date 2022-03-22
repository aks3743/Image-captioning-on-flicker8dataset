# Image-captioning-on-flicker8dataset


Image Captioning is the process of generating textual description of an image. It uses both Natural Language Processing and Computer Vision to generate the captions. The dataset will be in the form [image → captions]. The dataset consists of input images and their corresponding output captions.

Encoder

The Convolutional Neural Network(CNN) can be thought of as an encoder. The input image is given to CNN to extract the features. The last hidden state of the CNN is connected to the Decoder.

 

Decoder

The Decoder is a Recurrent Neural Network(RNN) which does language modelling up to the word level. The first time step receives the encoded output from the encoder and also the <START> vector
  
  
  Read the pickle file (https://drive.google.com/file/d/1A8g74ohdb_5d2fPjc72yF7GxufE9GRcu/view?usp=sharing) (Links to an external site.) and convert the data into the correct format which could be used for ML model. 
 Pickle file contains the image id and the text associated with the image.

Eg: '319847657_2c40e14113.jpg#0\tA girl in a purple shirt hold a pillow .

Each image can have multiple captions.

319847657_2c40e14113.jpg -> image name

#0 -> Caption ID

\t  -> separator between Image name and Image Caption

A girl in a purple shirt hold a pillow . -> Image Caption

Corresponding image wrt image name can be found in the image dataset folder.

 

Image dataset Folder : https://drive.google.com/file/d/1-mPKMpphaKqtT26ZzbR5hCHGedkNyAf1/view?usp=sharing (Links to an external site.)

 
## Tasks
Plot at least two samples and their captions (use matplotlib/seaborn/any other library). 
Bring the train and test data in the required format. 
 

### Model Building 
Use Pretrained Resnet-50 model trained on ImageNet dataset (available publicly on google) for image feature extraction.
Create 5 layered LSTM layer model and other relevant layers for image caption generation.
Add L1 regularization to all the LSTM layers. 
Add one layer of dropout at the appropriate position and give reasons. 
Choose the appropriate activation function for all the layers. 
Print the model summary. 
 

### Model Compilation 
Compile the model with the appropriate loss function. 
Use an appropriate optimizer. Give reasons for the choice of learning rate and its value. 
### Model Training 
Train the model for an appropriate number of epochs. Print the train and validation loss for each epoch. Use the appropriate batch size. 
Plot the loss and accuracy history graphs for both train and validation set. Print the total time taken for training. 
### Model Evaluation
Take a random image from google and generate caption for that image.
