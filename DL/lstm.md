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




