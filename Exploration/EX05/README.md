# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 임한결
- 리뷰어 : 이현재


# PRT(Peer Review Template)
- [O]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - Test accuracy가 85.9%가 나와 기준을 만족했다.
        - ![image](https://github.com/user-attachments/assets/b5093506-539c-4704-af5b-baec3ccd2fc7)

    
- [O]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - word2vec_ko embedding을 사용해서 모델을 학습하는 코드 블럭이 무엇을 하는지 간결하게 docstring으로 작성해놔서 오히려 line by line으로 세세하게 코드의 기능을 설명하는 것보다 가독성이 좋았다.
        - ![image](https://github.com/user-attachments/assets/30ea1b63-7e69-43f5-b0e6-b559d1c92af8)

        
- [O]  **3. 에러가 난 부분을 디버깅하여 문제를 해결한 기록을 남겼거나
새로운 시도 또는 추가 실험을 수행해봤나요?**
    - LSTM을 사용한 모델에서 Dense층을 최소화하고, LSTM층의 unit 수를 늘려보는 실험이 있었다.
      또, earlystopping과 checkpoint로 과대적합을 막고, 가장 성능이 좋은 모델을 채택하는 부분을 추가해 성능을 높였다.
        - ![image](https://github.com/user-attachments/assets/0d89c7d5-b477-464f-abef-44a6a27579c5)

 
        
- [O]  **4. 회고를 잘 작성했나요?**
    - 실험결과에서 느낀 지점들을 회고에 잘 정리해 놓았다.
        - ![image](https://github.com/user-attachments/assets/f27bac24-183d-42f1-a575-3c17c976f20f)

        
- [O]  **5. 코드가 간결하고 효율적인가요?**
    - 시각화 부분을 함수화해서 코드가 더 간결해졌다.
        - ![image](https://github.com/user-attachments/assets/443af4f5-532d-4d32-9483-575daeafa1dd)



# 회고(참고 링크 및 코드 개선)
```
시각화 부분 함수화, 모델 설계에서 Dropout과 callback function을 적극 활용해야겠다는 생각이 들었다. 항상 놓치는 부분인 것 같아 반성하게 됐다.
코드 리뷰를 통해 내가 모델 성능을 높이지 못했던 이유들을 알게 되어 내 모델에서도 실험해봐야겠다.
```
