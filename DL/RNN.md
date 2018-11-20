# What is RNN?

### Reference

* [강의] 김성훈 교수님의 모두의 딥러닝 강의 (lec 12: NN의 꽃 RNN 이야기)
* [책] 골빈해커의 3분 딥러닝



### What is the meaning of RNN?

* Recurrent Neural Network
  * Recurrent (되풀이되는, 반복되는, 재발되는)



### Why RNN?

* 연속적인 데이터를 다루기에, 이전에 사용하던 CNN은 적합하지 않았다

* Sequence data를 다루기 위함

  * Sequence data

    * 문장과 같이, 이전의 것이(state) 그 다음것에 영향을 미치는 경우

    * > RNN은 ... 순서가 있는 데이터를 처리하는데 강점을 가진 신경망 입니다.
      >
      > 예를 들어 "우와~ 영화 참 재밌네" 와 "망할! 영화 참 재밌네" 라는 문장이 있을 때, "영화 참 재밌네" 라는 뜻은 앞의 "우와~" 또는 "망할!" 이라는 단어에 따라 달라질 것 입니다.
      >
      > -골빈해커의 3분 딥러닝

  * 기존의 Network는 X라는 하나의 입력이 있으면 Y라는 하나의 output을 만들어내는 network였기 때문에, sequence data를 처리하는데 불편함이 있었음



### How to do operation? (Vanilla RNN)

1. State를 먼저 계산하고, 그 다음에 y를 계산한다

   1. 이전의 state(ht-1)와 현재의 입력값을 input으로 한다
   2. 어떤 함수 fw를 거친다
   3. 현재의 state ht를 구하게 된다

   ![스크린샷 2018-11-21 오전 12.26.49](/Users/isang-a/Desktop/스크린샷 2018-11-21 오전 12.26.49.png)

![스크린샷 2018-11-21 오전 12.30.33](/Users/isang-a/Desktop/스크린샷 2018-11-21 오전 12.30.33.png)

* 김성훈 교수님의 모두의 딥러닝 강의 lec12: NN의 꽃 RNN 이야기 강의자료 중





### Architecture of RNN

![스크린샷 2018-11-21 오전 12.28.37](/Users/isang-a/Desktop/스크린샷 2018-11-21 오전 12.28.37.png)

* 김성훈 교수님의 모두의 딥러닝 강의 lec12: NN의 꽃 RNN 이야기 강의자료 중
* 사실은 옆에 많은 cell들이 있는데, 왜 하나의 cell만 그렸을까?
  * 모든 State가 사용하는 함수 fw가 동일하기 때문에 그렇게 그린 것





![스크린샷 2018-11-21 오전 12.44.26](/Users/isang-a/Desktop/스크린샷 2018-11-21 오전 12.44.26.png)

* (위에) Multi-layer RNN





### RNN applications

* Language modeling
* Sppech Recognition
* Machine Translation
* Conversation Modeling/Question Answering
* Image/Video Captioning
* Image/Music/Dance Generation







