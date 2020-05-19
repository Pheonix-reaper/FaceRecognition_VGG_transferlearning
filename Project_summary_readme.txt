1.First,import the vgg16 pre-trained weight and declare a model of vgg16 specifying the shape of the image and make the top layer false so as to add more layers above the pre-defined layers
2.Then freeze the previous layers.Make the condition of each pre-defined layers of VGG16 Model Non-trainable.So,when we freeze the layer,we do not have to train the model again and again which reduces our training time.
3.Define a function which will creates the top or head of the model that will be placed on top of the bottom layers
4.Now,add a Fully Connected Layer as head to our VGG16 model
5.Now Load the images of our dataset for training and testing of our model
6.Previously i tried to train model with image_rows and image_columns =224 which slows down the training rate so,I resized the image to 64 rows and 64 image_columns for faster training of our model
7.Again loaded my training and testing data similar to what i had done before.Then I created and trained my model face_recog_vgg.h5 with 5 epochs and 32 batch size
8.Model created with 93.75 percent accuracy with 5 epochs and only within 40 minutes due to transfer learning.Then i imported my model for testing in another python file.
9.Then i have used cv2 module and created some function which randomly selects images from testing dataset folder and checks whether it matches my face or not.I have given my own name to the folder containing my image and for others I have given the name some_random_guy.So,if my face appears it will show my name other wise it shows message not recognised
10.These are the steps itook to complete this project