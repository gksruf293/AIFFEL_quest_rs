# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 임한결
- 리뷰어 : 조성호


# PRT(Peer Review Template)
- [ ]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - 예시 질문에 대한 대답이 나오는 트랜스포머 모델 학습 & 테스트 코드가 제출되었다.
    - 학습 전에 데이터를 증강하는 코드가 포함되어 있다.
![image](https://github.com/user-attachments/assets/05e6e964-1109-4e54-bbff-6a44d6e6b907)

![image](https://github.com/user-attachments/assets/6ed3f6ef-fc48-4540-aa56-f84774beff73)

    
- [ ]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - 데이터 증강 과정에서 코드만 보면 무엇을 한지 알기 어려웠는데, 각각의 의미를 주석으로 작성하여 이해할 수 있었다.
    - 각 태그의 의미, 유의어를 치환하는 방식 등
![image](https://github.com/user-attachments/assets/c8ad168a-bf0a-4195-b59f-93760d9efff7)

        
- [ ]  **3. 에러가 난 부분을 디버깅하여 문제를 해결한 기록을 남겼거나
새로운 시도 또는 추가 실험을 수행해봤나요?**
    - 시행착오의 과정을 남겨 우리 팀의 실험과 비교하기 편하게 작성되었다.
    - 특히 sentencepiece의 bpe로 vocab을 구성한 경우 단어장의 크기가 크게 증가하는 것을 확인할 수 있었다.
    - 추가 실험으로는 하이퍼 파라미터 중 d_ff와 dropout을 바꿔 실험해 보았다. 또한 epoch을 바꾸는 것도 확인되었다.
![image](https://github.com/user-attachments/assets/85a2bf5c-3677-491c-9a47-995b92fdfc9a)

![image](https://github.com/user-attachments/assets/09c3340e-ae3d-43b4-a97e-b028f9f0bb6e)

![image](https://github.com/user-attachments/assets/416d039a-bce8-4ba3-8957-988636d0277c)

![image](https://github.com/user-attachments/assets/452e7ed1-9c30-406a-a8eb-7093a001eeec)
        
- [ ]  **4. 회고를 잘 작성했나요?**
    - 코드 중간중간 작성된 시행착오를 정리해 이번 실험에서 특별한 점과 아쉬운 점을 회고로 작성하였다.
![image](https://github.com/user-attachments/assets/179066c4-9bbc-48b4-bd8b-e5cd42f23acf)
        
- [ ]  **5. 코드가 간결하고 효율적인가요?**
    - 증강 데이터를 만드는 과정에서 반복적으로 사용되는 유사 단어 찾기를 함수로 구현하였다.
![image](https://github.com/user-attachments/assets/c830634b-41a2-4066-bc35-003ae009b6cb)

    - 토크나이저 생성 과정도 함수화하여 sentencepiece의 설정을 바꿀 수 있도록 구현하였다.
![image](https://github.com/user-attachments/assets/3c4766e9-a25c-43ee-9455-fe3997df74f2)

    - perplexity 계산도 함수화하여 점수 계산이 필요할 때마다 불러와 사용했다.
![image](https://github.com/user-attachments/assets/1a5d9815-4da2-49f8-b31e-2ff5d9a37240)


# 회고(참고 링크 및 코드 개선)
```
vocab을 만드는 과정에서 저희 팀과 다른 점이 많아 배울 점이 많았습니다.
특히 저희 팀은 sentencepiece를 사용하지 않아 성능이 낮았다는 것을 인지하게 되었습니다.
validation set을 사용하지 않은 점도 특이하다고 생각했습니다.
설명을 들어보니 loss 값이나 Bleu 점수에 따라 학습을 평가하기 힘들다는 것일 인지했고,
앞으로 있을 실험에서 특히 챗봇과 같은 다양성이 중요한 언어 모델의 경우 무엇을 기준으로 평가할지
더 고민해볼 수 있는 시간이였습니다.
```
