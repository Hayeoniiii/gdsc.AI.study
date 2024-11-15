## 7. Attention

>### What is Attention?
입력 데이터의 서로 다른 부분들 간의 관련성을 계산하는 방법         
중요한 데이터에 더 집중할 수 있도록!      

#### Attention이 제시된 맥락

#문장을 해석하는 attention이 없는 seq2seq 모델에서의 문제     
하나의 고정된 크기의 벡터를 압축하여 순차적으로 들어가면서 앞에 들어갔던 단어의 영향력이 줄어든다.           
-> 정보 손실 발생, 번역 품질 떨어짐
           
#seq2seq with Attention       
디코더에서 출력 단어를 예측하는 매 시점마다, 인코더에서 해당 시점에서 예측해야 할 단어와 연관이 있는 입력 단어 부분을 집중(attention)하여 보는 것이다.         

어텐션함수는 쿼리에 대해서 모든 키와의 유사도를 각각 구하여, 키와 맵핑되어 있는 각각의 값에 반영해준다.     

>### Vision Transformer
transformer구조 (attention mechanism) Vision 적용     
패치 단위로 잘라 CLS Token을 이용
          
#### CNN
컨볼루션 필터로 지역 특징 추출      
인접 영역끼리 계층적 전달        
컨볼루션 연산에 내재된 위치 정보       
-> 이미지의 Inductive Bias를 효과적으로 활용

#### ViT
패치 단위로 분할 후 Self-Attention      
모든 패치 간 직접적인 정보 교환        
Position Embedding으로 명시적 추가    
-> Inductive Bias를 효과적으로 활용하지 못함 (좀 더 유연한 추론)