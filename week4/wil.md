## 3.Loss Function & Optimization

>### Loss Function

입력 이미지를 정확하게 분류하기 위한 weight matrix를 최적화하는 방법         
loss function을 사용하여 현재 weight matrix의 <span style="color:blue"> 예측과 실제 정답 간의 차이를 수치화 </span>          
loss 값을 최소화하여 분류 정확도 최대화        

#### 회귀 문제에서 사용되는 loss         
1. Mean Squared Error           
연속형 변수를 예측할 때 사용
 
#### 분류 문제에서 사용되는 loss    
1. Support Vector Machine (hinge loss)        
safety margin을 두고 정답 클래스 점수와 예측 클래스 점수의 대소 비교      
SVM은 허용가능한 오류범위 내에서 최대 margin을 만드는 것이 목표    

   -SVM: 분류 경계에 가장 가까운 데이터 포인트들(support vector)을 이용해 최적의 결정 경계를 찾는 알고리즘       
   -margin: 결정 경계를 기반으로 support vector까지의 거리       

2. Cross-Entropy loss       
softmax 함수를 사용하여 출력을 의미 있는 확률 분포로 변환      
(확률 분포의 차이에 더욱 민감하게 반응함)

>### Regularization
목적: 적절한 가중치를 유지하면서, 필요 이상으로 큰 가중치를 줄이는 것, 과적합 방지                
loss함수에 parameter에 대한 term을 추가하여 적용     
가중치 w가 작아지도록 학습한다 (불필요한 parameter들의 영향을 줄이기 위해서)    
#### L2 Regularization
매끄러운 그래프를 원할때       
큰 가중치에 더 큰 패널티를 부과하여 모든 특성이 적당히 기여하도록 유도

#### L1 Regularization
분류기가 복잡하다고 느껴질때     
가중치값에 0이 많도록 하여 단순한 식으로 만들어줌

>### Optimization
loss function 이 줄어들도록 조정하는 방법      
1. Gradient Descent      
가장 가파르게 감소하는 방향으로 옮겨가며 최소지점으로 가는 것이 목표     
->local minimum 발생 우려      
2. Momentum        
이전 단계의 업데이트 방향을 고려하여 현재 업데이트에 반영       
3. Adaptive Learning rate      
과거의 그래디언트 정보를 활용하여 각 파라미터마다 서로 다른 학습률 사용       
4. Learning rate scheduler       
초기에 높은 학습률을 사용하면 빠르게 최저점 근처로 접근         
적절한 시점에 학습률을 높이면 local minimum에서 벗어날 수 있음        






