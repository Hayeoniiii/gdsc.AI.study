## 4. Backpropagation and Neural Network

>### Backpropagation 
인공신경망을 학습시키기 위한 알고리즘       
내가 구하려는 target 값과 실제 모델이 계산한 output이 얼마나 차이나는지 구한 후 그 오차값을 다시 뒤로 전파해가면서 각 노드가 가지고 있는 변수들을 갱신하는 알고리즘 

**backpropagation 이 없다면?**      
수치적 미분 사용       
n개의 가중치가 있다면 손실 함수의 출력(=순전파)를 총 n번 계산해야함           
**backpropagation**     
순전파 1번과 한번의 역전파로 계산 가능      
미분 연쇄 법칙 사용      
파라미터 x값이 오르면 최종 Loss에 어떠한 영향을 주는가에 대해 미분값을 통해 계산      
              
#### 신경망에서 backpropagation이 어떻게 이루어지는가
1. 데이터 입력 (image input)
2. 순전파 (feed-forwarding)
3. 손실 계산
4. **역전파**
5. 최적화시킨 weight를 model에 적용
6. 1~5번 반복
