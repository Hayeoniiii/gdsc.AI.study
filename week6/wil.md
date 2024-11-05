## 5.CNN, Activation Function, Batch Normalization

>### CNN
FNN은 인접 픽셀간의 상관관계가 무시되어 이미지를 벡터화하는 과정에서 정보손실이 발생할 수 있음

#### CNN (Convolutional Neural Network)
CNN은 Convolution Layer를 통해 입력 이미지에 다양한 필터를 적용하여 특징을 추출한다.    
A convolution layer = convolution + activation     

>### Activation Function (활성화함수)
선형 변환의 연속만으로는 복잡한 함수를 표현할 수 없다.       
활성화함수 없이 여러 층을 쌓으면, 결국 하나의 선형 변환으로 축소된다.       
ex) f(x)=dot(W2,(dot(W2,x)+b1))+b2=dot(W,X)+b       
비선형 활성화 함수는 각 층에서 더 복잡하고 추상적인 특징을 학습할 수 있게 해준다.

>### Batch Normalization 
정규화없이는 큰 스케일을 가진 특성이 모델에 과도한 영향을 미칠 수 있다.      
#### Mini-Batch
전체 데이터셋이 아닌 현재 미니배치 내의 데이터만에 집중하는 것      
병렬 처리 가능      
일반적으로 32~256개의 데이터를 1 batch size으로 사용
#### 배치 정규화란? 
딥러닝 모델의 학습을 안정화하고 속도를 향상시키기 위해 개발된 기법      
각 미니배치에서 입력 데이터의 평균과 분산을 계산하여 해당 데이터의 분포를 정규화          
-> 각 층의 입력이 일정한 분포를 유지하게 됨      

#### 언제 적용하는가?
1. Internal Covariant Shift: Batch 단위로 학습하여 학습 과정에서 계층 별로 입력의 데이터 분포가 달라지는 현상
2. 연산 전/후에 데이터 간 분포가 달라지는 경우       
3. Batch 단위간에 데이터 분포의 차이가 발생하는 경우      

>### Transfer Learning
이미 학습된 모델의 지식을 새로운 작업에 활용하는 기법     
주로 대량의 데이터로 훈련된 모델을 기반으로, 특정 문제를 해결하기 위한 데이터가 부족할 때 사용된다.      
#### LoRA (Low-Rank Adaption)
대규모 언어 모델 및 기타 머신러닝 모델의 파인튜닝을 효율적으로 수행하기 위해 개발된 방법    

>### Knowledge Distillation 
대규모 모델에서 학습한 지식을 작은 모델로 전이하는 기법       
모델읙 경량화와 효율성을 높이는 데 사용 됨 



