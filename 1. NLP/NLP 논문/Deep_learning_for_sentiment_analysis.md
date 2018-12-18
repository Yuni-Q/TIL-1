# Deep learning for sentiment analysis
* Written by __Lina Maria Rojas‐Barahona__

### 3. DEEP LEARNING
* High layer는 Lower layer의 복잡한 비선형 함수를 이용하여 훈련한다.
* High layer는 Lower layer보다 추상적이다.  
###
* DNN은 많은 input을 바탕을 하여, approximate하는 model이다.
* 그리고 DNN은 ANN에서, input과 output layer 사이에 많은 은닉층이 있다.
  * 따라서 은닉층을 통해 input에서 다양한 feature를 학습할 수 있으며, 그것들로 classification이 가능해진다.
  * (DNN은 ANN에서 발전된 모습이다와 비슷한 의미라 생각함)
* DNN은 NLP의 다양한 분야에서 유용하게 쓰인다.
###

#### 3.1 Feed-forward neural network
* ANN은 neuron으로 구성되어 있으며, 각 neurone들은 weighted connection으로 연결되어 있다.
* 그리고 neuron들은 signal을 받으면 activate 되고, activation은 연결된 neuron들에 전달된다.
  * 은닉층(hidden layer)과 output layer에서 쓰이는 활성화 함수는 비선형 함수로, sigmoid, hyperbolic tangent 함수 등이 그것이다.
###
* 또한 Softmax 함수는 network의 output인 확률 분포를 (target) category로 바꾸는 데에 좋은 성능을 보여준다.
