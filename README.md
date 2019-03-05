# Object/Face recognition using transfer learning: 
Transfer learning is the reuse of a pre-trained model on a new problem. It is currently very popular in the field of Deep Learning because it enables you to train Deep Neural Networks with comparatively little data.

# Project Architecture
-Set data_path: Url for all class folders. Class folder name is the name of that class

-Read image and labels: Read class names and number of classes. Read all images and put them in a nd-array. In image_read function all images have been normalized between -1 and 1, nulls are removed. All images have been rolled into 1 row. Nd-array shape will be [1, #images, imageWidth, imageLength, channels] 

-Data augmentation: Data augmentation was done using keras preprocessing tools. Random rotation, random zoom and random width shift operations were performed to augment data. After running augmentation operation all were read and appended in an nd-array. 

-Encoding: Label encoding and one hot encoding were performed using keras utils tool and all images with their label were shuffled by using sklearn utils tool. 

-Model selection and transfer learning: Keras VGG16 model was loaded and last layer was replaced with a Dense layer with required number of classes and softmax activation. All the parameters in each layers were turned non-trainable except the last (new/custom) layer. Only last layer parameters will be trained and all other layers parameters will be as is in VGG16 model. This process called transfer learning. 

-Model compilation: Model was compiled with ‘rmsprop’ optimizer, ‘categorical_crossentropy’ loss function and ‘accuracy’ matrics. Model fit was performed with batch_size=30, epochs=1, verbose=1, validation_split=0.2, shuffle=True. 

-Test and result: For testing this model, Test image was read and preprocessed same way as train images were read. Model prediction was performed and displayed. 


## use your won data_path and test_path. My paths are as below. 
data_path = r'C:\Users\aman0\Desktop\ME\My_project\Data Sink\GIW'
test_path = r'C:\Users\aman0\Desktop\ME\Tutorial\Data Sink\TransferF_course\validation_data\test.jpg'
