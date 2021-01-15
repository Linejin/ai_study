##1. Overview
- kind of ML
  - Supervised, Unsupervised, Reinforcement
  - Regression, Clustering
- Representation & Reasoning
- 특징 분류
- Decision Tree
- ex) 물고기 분류, 꽃 분류

##2. DataScience
- torch.tensor
  - dtype
  - type casting
  - Initialization
    - zeros(size)
    - ones(size)
    - rand(size)
    - tensor(data)
  - operater
    - 산술
    - broadcasting
    - dimention calculation
  - .dim()
  - .shape
  - slicing
  - reshape & view
  - squeeze & unsqueeze
  - concatenate & stack
		
##3. ML Basic
- KNN
  - main idea
    - 비슷한것 찾기
      - 비슷하다의 수학적 표현방법 - 거리
      - 거리 계산하는 방법(L1, L2)
    - Matrix Data
    - torch의 산술 연산으로 계산하여 비슷한것 찾기
    - Tensor Data
      - pytorch의 명령어(norm, )를 사용해 비슷한것 찾기
    - Normalization
      - Data 정규화를 하여 KNN 진행
    - KNN regression
      - regression 구현해보기
- Simple Linear Regression
  - main idea
    - KNN regression의 한계
    - 1차 방정식
      - 손으로 입력에 따른 예상값 예측해보기
      - [weight, bias] 직접 조절해 직선 그래프 만들어보기
      - pytorch(nn아님)로 직선 그래프 만들어 그래프 확인해보기		
    - 해당 그래프의 오차 계산해보기
      - MAE, MSE
      - 오차값 보면서 [weight, bias] 조정해보기
      - 만들었던 pytorch에서 오차값 계산, 최적화 진행해보기
    - 경사하강법
      - 실제 오차값 그래프를 보면서 경사하강법 설명
      - Learning rate의 필요성
    - python-pytorch
      - Simple Linear Regression 단순 구현 및 학습시키기
    - NN
      - 그림으로 설명
      - Simple Linear Regression 구현 및 학습시키기
				
- Simple Logistic Regression
  - main idea
    - Linear Regression의 한계
    - Data값에 따른 label의 확률 부여해보기
      - 부여한 확률을 그래프화
    - sigmoid 함수 소개
      - [weight, bias] 조정에 따른 sigmoid 그래프 조정해보기
      - pytorch-nn으로 model을 만들어 임의의 [weight, bias]를 넣어가며 그래프 확인해보기
    - Binary Cross Entropy
      - MAE, MSE의 제한성, Binary Cross Entropy 설명
      - sigmoid 그래프의 오차를 보며 [weight, bias]조정해보기
      - 만들었던 pytorch-nn의 model의 오차값 확인해보기
    - 경사하강법을 이용하여 학습시키기
    - NN
      - pytorch-nn으로 확률 구해보기
    - Classification
      - 확률값을 보고 2가지 상태에 대한 판별해보기
    - 다른 활성함수
      - 각 활성함수를 사용하는 상황 예시로 설명
		
- Multiple Regression & Perceptron
  - main idea
    - Multiple Regression의 필요성

	
- Neural Network & fitting

- Convolutional Neural Network

- GAN
