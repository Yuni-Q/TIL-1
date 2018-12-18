# 쫄지말자 딥러닝

**인공지능은 함수이다**

**그리고 그 함수를 구현하는데에는 비선형 함수를 그 안에 넣었다**

**그리고 그 함수를 영상에 특화되도록 만든 모델이 CNN 이다**



* 딥러닝이란

  * 수학적으로 표현할 수 없었던 복잡한 인간의 두뇌를 데이터를 기반으로 흉내내는 것

* 인공지능과 머신러닝(Pattern recognition -> Machine learning)의 차이?

  * 머신러닝
    * 함수의 값이 계속 바뀐다고 생각해보자
    * 지도 학습 (Supervised learning)
    * 비지도 학습 (Unsupervised learning)
    * 강화 학습 (Reinforcement learning)

* NN이란?

  * NN = 뉴런 이 모인 것.
    * 뉴런
      * 정보가 임계치를 넘어가지 않으면, 다른 뉴런으로 넘어가지 않는다
    * 인공뉴런도, 이와 같은 베이스에서 출발하였다

* NN이 모이면 MLP가 되는건가?

* MLP (다층 레이어)

  * 여러 layer를 쌓은 black box

    * 그리고 그것을 구현하는 것의 핵심은 non-linear한 activation function 이다

  * 문제점

    * 복잡하게 내맘대로 모델을 만들 수 없는 이유

    * **Overfitting**

      * 주어진 데이터(트레이닝한 데이터)에는 높은 성능을 보이지만, 새로운 데이터(실제, 테스트 데이터)에서는 성능이 떨어진다
      * 너무 모델이 복잡하기 때문에...
        * 즉, 무조건 복잡한것이 좋은 것은 아니다
      * *Dropout*
        * 랜덤하게 뉴런을 끊음으로써, 모델을 단순하게 만듦

    * **Vanishing gradient**

      * 학습되는 양 = 미분 값 * 출력 값

        1. 어떤 활성화 함수를 사용하더라도, 대부분의 영역에서 미분값이 0에 가까워진다

        2. 따라서 매번 layer를 거치면서, 값이 0에 가까워지며 **학습이 되지 않는다**

      * 이에 새롭게 등장한 활성화 함수!

        * *ReLU* 

          * 미분값이 1이고, 출력값은 무한대이다
          * 이에, 앞서 언급한 문제(1,2) 가 해결되었다

* CNN (Convolutional Neural Network)

  * Convolution 연산이란?
    * Shift 와 곱하기 연산의 합이다
    * Convolution 연산을 통해, 영상의 특징을 뽑아낼 수 있다
  * **Convolution 연산을 하다보면, filter size가 갈수록 커지게 된다**
    * 따라서, 서로 다른 크기의 필터의 feature를 뽑아낼 수 있다 (교환법칙이 성립하니까)
  * **LeNet**
  * Hyperparameter를 learning에 도와주는 tool - **google automl**



# New Tensorflow

* Tf.layers
  * ML layer를 build하기 위함
* tf.estimator
  * training 과 evaluation

* Three keys toward TF 2.0
  * Writing eagerly
    * if .. else .. 를 사용할 수 있다 (autograph)
  * Fully compatible tf.keras
* **In TF 2.0**
  * **High level**
    * **tf.keras**
  * **High level custom**
    * **tf.keras + subclass + eaber**
  * **low level**
    * **python-style code + autograph + eager**
  * low level
    * tf.nn + eager

[다른 강의에서 - tensorflow hub](http://solarisailab.com/archives/2497)



# 이제는 딥러닝 개발환경도 Docker로 돌려보자!

## Docker로 개발환경 셋업하기

* PPT 참고





# 자연어처리

* RNNs for NLP
  * Vanishing gradient
    * Backpropagation, Chain rule에 의해 발생
* FastText
  * 오타에 강하다
* Encoder-Decoder
* ELMO -> GPT -> BERT



# 요새 같은 시절에 누가 optimizer를 직접 짜나요?

* Optimization
  * **왜 중요해**
    * minimize
* Gradient
  * minimum을 쭉쭉찾자
* *Momentum*
  * (관성)
    * Gradient descendent가 작동하지 않는 문제를 해결
      * update = velocity + gradient
  * Velocity
    * SGD
    * SGD + Momentum
    * SGD + Momentum another form
  * 구현하는 방법
* AALR Algorithms of Adaptive Learning Rates
  * Learning rate가 고정되어있지 않고, 계속 변한다
  * Algorithm
    * Adagrad
      * 갈수록 learning rate가 줄어든다
    * RMSprop
      * Adagrad 개선
    * Adam
      * Adagrad + RMSprop + Momentum
      * 잘 움직여라~
    * AdaMax
    * NAdam
  * [Code site(Github)](https://github.com/ilguyi/optimizers.numpy)

