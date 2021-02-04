# Super-AI1
## flow
1. 문제 발생
2. 문제를 해결할 idea 
3. idea에 따라 퀴즈 풀어보기 
4. 해당 퀴즈에 내재된 개념 설명(구체화) 
5. 개당 개념을 반영하여 코드 작성

## 1. Overview
- kind of ML
  - Supervised, Unsupervised, Reinforcement
  - Regression, Clustering
- Representation & Reasoning
- 특징 분류
- Decision Tree
- ex) 물고기 분류, 꽃 분류, 성적 향상 예상

## 2. DataScience
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
		
## 3. ML Basic
- KNN
  - main idea
    - 비슷한것 찾기   # drag & drop과 같은 활동으로 진행, 그림 -> 행렬데이터로 진행
      - 비슷하다의 수학적 표현방법 - 거리
      - 거리 계산하는 방법(L1, L2)
    - 2차원 Data KNN   # 앞에서 진행했던 활동을 코드로 구현, K = 1로 진행
      - torch의 산술 연산으로 계산하여 비슷한것 찾기
    - 다차원 Data KNN  
      - pytorch의 명령어(norm, argsort 등) 사용해 비슷한것 찾기
    - Normalization   # 정규화가 필요한 이유
      - Data 정규화를 하여 KNN 진행
    - KNN regression   # regression 파트로 넘어가기 위한 발판
      - regression 구현해보기
- Simple Linear Regression
  - main idea
    - KNN regression의 한계
    - 1차 방정식
      - 손으로 입력에 따른 예상값 예측해보기
      - [weight, bias] 직접 조절해 직선 그래프 만들어보기
      - pytorch(nn아님)로 직선 그래프 만들어 그래프 확인해보기
    - 해당 그래프의 오차 계산해보기   # 직선과 점사이의 오차 계산 방법
      - MAE, MSE
      - 오차값 보면서 [weight, bias] 조정해보기
      - 만들었던 pytorch에서 오차값 계산, 최적화 진행해보기
    - 경사하강법   # 학생들이 그래프를 직접 옮겨갔던 과정을 기록하여 설명(대체적으로 경사하강법과 유사한 방식으로 진행했을 거라 가정)
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
    - sigmoid 함수 소개   #(지수, 로그 함수를 모르기에 직접 값들을 조절해가며 감각적으로 학습)
      - [weight, bias] 조정에 따른 sigmoid 그래프 조정해보기
      - pytorch-nn으로 model을 만들어 임의의 [weight, bias]를 넣어가며 그래프 확인해보기
    - Binary Cross Entropy
      - MAE, MSE의 제한성, Binary Cross Entropy 설명
      - sigmoid 그래프의 오차를 보며 [weight, bias]조정해보기
      - 만들었던 pytorch-nn의 model의 오차값 확인해보기
    - 경사하강법을 이용하여 학습시키기   # MAE, MSE, BCE 각각 사용해보기
      - pytorch-nn으로 확률 구해보기
    - Classification
      - 확률값을 보고 2가지 상태에 대한 판별해보기
    - 다른 활성함수
      - 각 활성함수를 사용하는 상황 예시로 설명
		
- Multiple Regression & Perceptron
  -main idea
    - Multiple Regression의 필요성
      - Multiple Linear Regression 구현해보기
    - 3차원 그래프 그려보기
      - 다대일 모델
    - Multiple ogistic Regression 구현해보기
      - 다대다 모델
      - one-hot-encoding
    - Perceptron 소개

	
- Neural Network & fitting
  - main idea
     - Perceptron과 Neural & Neural Network와 Brain
       - DATA값에 따라 label을 분류해보기
       - Decision Tree Algorithm
       - Perceptron을 Decision Tree에 대입해보기
       - Feature 소개
     - Deep Learning
       - Neural Network의 작동 방식 살펴보기
       - Deep Learning 방식의 Neural Network
       - Black Box
     - NN
       - pytorch-nn으로 Neural Net 구성해보기
     - Overfitting, Underfitting
       - Decision Tree로 살펴보는 Overfitting, Underfitting
       - Overfitting과 Underfitting을 최소화 할 방법 구상하기
       - Dropout 소개
     - NN
       - pythorch-nn으로 Dropout이 포함되는 Neural Net 구성해보기
			
			
- Convolutional Neural Network
  - main idea
    - image data의 data구성
      - image data의 특징(인접 data와의 연관성)
    - image data의 nn - classification(non CNN)
    - 인접 data에 대하여 feature 추출 후 nn - classification(CNN)
    - Max-pooling
- GAN


항상 model 이름은 model로 통일
단, GAN은 model_g, model_d로 사용

Challenge & practice는 model의 정확도로 판정 - RunCodeRule
단, 일부 ContainCodeRule이 적용될 수 있음
이를 위하여 사전에 채점용 DATA가 등록되어 있어야 함


$$\begin{bmatrix} F_{n+1} & F_n\\ F_n & F_{n - 1} \end{bmatrix}=\begin{bmatrix} F_{2} & F_1\\ F_1 & F_{2} \end{bmatrix} = \begin{bmatrix} 1 & 1\\ 1 & 0 \end{bmatrix}$$
