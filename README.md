# Deep_Learning

## HW01
딥러닝의 일반화 성능을 높이기 위해 Regularization을 해봄으로써 Overfitting을 줄이고 Test accuracy을 높힌다. 그 과정에서 Dropout, Batch Normalization, Data Augmentation와 같은 대표적인 Regularization 기법을 학습한다.

## HW02
Convolution Neural Network를 이용하여 개와 고양이의 종을 분류하는 모델인, Pet 분류기를 만들어본다. 만든 Pet 분류기가 Test set에서 높은 성능을 보여줄 수 있도록 Data augmentation, Validation set 생성, 모델의 레이어 구조, 학습 파라미터 등을 고려하여 CNN모델을 개선하여 test set에 대해서 일반화된 모델을 만들어본다.

## HW03
Recurrent Neural Network (RNN)을 이용하여 주가를 예측하는 모델을 만들어본다. 만든 주가 예측 RNN 모델이 Test Set에서 높은 성능을 보여줄 수 있도록 Data Augmentation, Validation Set 생성, RNN 모델의 레이어 구조 변경, 학습 파라미터 변경 등을 고려하여 RNN 모델을 개선하여 Test Set에 대해서 일반화된 모델을 만들어본다.

## DeepLearningProject
청각장애인과 같이 언어장애를 가지고 있는 사람과 수화로 대화를 하거나 소리를 낼 수 없는 군 전쟁 지역이나, 작전 지역에서는 제스처만을 이용해 소통을 해야 하기 때문에 원활한 소통이 어려울 수 있다. 따라서 카메라를 통해 손 모양을 인식하고 각 손 모양의 관절에 따른 랜드마크들 간에 관계를 활용해, 해당 제스처 Data를 수집 하고 이를 분류를 하는 연구를 진행한다. 카메라를 통해 받아온 영상을 ‘Mediapipe’를 이용해 손 모양, 즉 특정 수화나 제스처를 인식하고, 인식한 손 모양의 관절에 따른 21개의 랜드마크들의 (x, y, z) 좌표를 통해 손가락 마 디의 벡터 좌표를 구하고, 최종적으로 인접한 손마디 간에 각도를 구한다. 움직이는 제스처까지 분류하기 위해, 구한 해당 각도 Data를 각 시간에 따른 Sequential한 Data로 저장하여 수집한다. 수집한 Data를 이용해 RNN 모델을 직접 구성하고 학습하여 모델의 성능을 확인하고, 실제로 해당 RNN 학습 모델이 제스처를 정확히 분류 하는지 확인한다.

- create_dataset.py : 데이서 수집
  ![Uploading 데이터 수집 영상.gif…]()

- train.ipynb :  수집한 데이터를 이용한 RNN 모델 학습

- test.py : 학습된 RNN 모델, 실시간 영상을 이용한 모델 성능 확인
  
