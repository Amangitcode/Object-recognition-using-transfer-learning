# Object-recognition-using-transfer-learning: Please read before you use the model 

Transfer learning is a method where you can classify image by using KERAS/other pre-trained model. All you need to do is, choose your model from KERAS/OTHER pre-trained models based on your application and load them into your kernel and tune last few layers as your application requires and train only those few layer/s then you are good to go 

This model can classify your image based on the url you provide for data_path variable. Inside your data_path folder you create folders as many as class you want to predict and put at least 10 images of each class. Model will read all the folders name as class name. Model will augment data using KERAS ImageDataGenerator tools from keras.preprocessing library augment your data.  

This ImageDataGenerator tools will take your given number of images to generate millions of images to create training set and later train the model.  

Once model is trained, you can test your model by using a unseen image. Use your won url for test_path variable to get your test image. 
