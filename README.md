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
   
<img src="/image/3.JPG" width="80%" height="80%" title="img1" alt="img1"></img>

>Grad-Cam heatmap Image   

<img src="/image/4.JPG" width="80%" height="80%" title="img1" alt="img1"></img>
<img src="/image/5.JPG" width="80%" height="80%" title="img1" alt="img1"></img>

>predict Test Image   

<img src="/image/6.JPG" width="80%" height="80%" title="img1" alt="img1"></img>

>Confustion_matrix

<img src="/image/7.JPG" width="80%" height="80%" title="img1" alt="img1"></img>

4000개의 Test image로 predict 결과 acc: 91.95%를 달성   
Grad-CAM heatmap 출력 결과 대상의 얼굴을 중점으로 개, 고양이를 판별하는 것으로 추정   
Confustion_matrix 확인 결과 고양이 인식 성능이 개 인식 성능보다 조금 떨어지는 것을 확인   
자세한 모델 구조 및 hyper parameter는 vgg16.ipynb를 참고하시길 바랍니다.   
   
***

#### Grad-CAM & Featuremap 구현 Tensorflow Code
>Featuremap Visualization tensorflow2.0 code<https://github.com/AhnYoungBin/Featuremap_visualization>   
>Grad_CAM tensorflow2.0 code<https://github.com/AhnYoungBin/Grad_cam>   

