# LSTM

### Reference site

* https://brunch.co.kr/@chris-song/9
* https://www.slideshare.net/ByoungHeeKim1/recurrent-neural-networks-73629152
* https://www.edwith.org/deeplearningchoi/lecture/15840/



### Instead of LSTM... Why?

* 왜 RNN 잘쓰다가 LSTM이 필요하다고 생각했을까?

* 왜긴 RNN문제점이 있었으니까!

  * **장기 의존성 문제** 라고 해서, **입력 데이터가 길어질수록 적절하게 예측하지 못한다** 는것이 바로 그것이다

  * 예를 들어

  * > The clouds in the [sky] 와 같이 짧은 문장에서는 sky를 쉽게 예측할 수 있으나
    >
    > I grew up in France …… I speak fluent [French] 와 같이 긴 문장에서는 French를 맞추기 위해서는 **앞의 데이터에 대해 모조리** 기억을 하고 있어야 한다는 것

* 이런 문제가 발생하게 되는 이유는

  * 나도 질문을 스택오버플로우에 올려서 답변을 기다리고 있다 ㅠㅠ 아시면알려주세유
  * https://stackoverflow.com/questions/53467271/why-big-rnn-model-multi-layer-rnn-model-can-not-learn-well


### LSTM의 등장

* 여튼 그렇게 **장기 의존성 문제** 를 해결하자! 라는 생각에서 LSTM이 등장하게 되었다
* LSTM은 Long Short Term Memory 말 그대로 장단기 메모리.. 이다



### 어떻게 장기 의존성 문제를 해결하게 되었는데?

* Forget gate, Input gate, Output gate 세개로!

![unrolled rnn cell structure](https://d3ansictanv2wj.cloudfront.net/figure1-4ee485edcb5d51bbed8e4fa14d54a649.jpg)



* 위에거가 RNN, 아래거가 LSTM이다. 딱 봐도 LSTM이 훠어어어얼씬 복잡하게 생겼다.



### Detail

* 그러면 이제 구조를 좀더 자세히 봐보자
* ![LSTM architecture.png](/snaag/TIL/blob/master/Img/DL/LSTM%20architecture.png?raw=true)
  * Forget gate
    * 여기서는 이전 연산결과로 나온 output(이하 ht-1)과 새롭게 들어온 Input(xt) 중에서 **어떤 정보를 얼마나 버릴지**(잊을지) 를 결정한다
  * Input gate
    * 여기서는 ht-1과 xt 를 tanh로 계산한 후, 시그모이드를 거쳐 **어떤 정보를 얼마나 살릴지** 를 결정한다
  * **따라서 forget, input gate 를 거치면서 어떤 정보를 날리고, 살릴지를 결정한다는 것**
  * Output gate
    * 이렇게 계산한 것들을, 얼마나 다음 state로 넘길지 (ht로 만들지) 결정한다



### Question

* 하지만 아직도 헷갈리는건 **복잡한 연산과 이저어어언 데이터의 보존과의 상관관계** 이다.
* 수학을 잘하는 친구에게 수식에 대해 자세히 물어봐야겠다







