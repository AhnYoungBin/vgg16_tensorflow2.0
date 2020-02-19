VGG16_tensorflow2.0 Code
===================

Dataset
-------
#### Cat vs Dog dataset Download Site : <https://www.kaggle.com/c/dogs-vs-cats/data>
Train dataset을 Train iamge 17000장, vaildation image 4000장, test image 4000장으로 나누어서 실험하였다.(그림1 참조)   
   
>그림1   

<img src="/image/1.JPG" width="80%" height="80%" title="img1" alt="img1"></img>

VGG Architecture
----------------
<img src="/image/2.JPG" width="80%" height="80%" title="img1" alt="img1"></img>
***

Option
------
#### input_shape : [224,224,3], Batch_size : 32, epochs = 400
#### compile option : optimizers= 'Adadelta', loss='binary_crossentropy', metrics=['acc']
   
Result
------

>Conv layer feature map   
   
<img src="/image/1.JPG" width="80%" height="80%" title="img1" alt="img1"></img>

