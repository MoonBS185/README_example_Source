수평선 (구분선, 수평선을 만들려면 - or * or _을 3개를 입력)
![1](https://github.com/user-attachments/assets/7facd009-4eb1-446e-aa59-0e83b94f98ec)

---

***

___


*기울기1*
_기울기2_




# 글자크기1
## 글자크기2
### 글자크기3
#### 글자크기4




# 소스코드블록
```c
for i in range(0,5):
   print(i)
```


# 코드블록2

하나

    둘(탭, 스페이스바로 이부분 회색 될 때까지 들여쓰기)

셋



# 링크걸기
[링크를걸겠습니다.](https://www.naver.com/)

# 순서없는목록

+ 목록1
  + 목록 1-1
    + 목록 1-1-1

* 목록1
  * 목록 1-1
    * 목록 1-1-1

- 목록1
  - 목록 1-1
    - 목록 1-1-1





# BlockQuote

> "알파코1기" - 올림
>> "알파코2기" - 올림
>>> "알파코3기" - 올림





# 숫자목록 출력
1. 하나
2. 둘
3. 셋





# 테이블 만들기

프로젝트목록 | 일자 | 사용기술 | 링크
------------|------|-------|-----|
이미지 생성 | 2021 | GAN | [GAN 프로젝트 링크](https://github.com/shiny0510/FewShot_GAN-Unet3D)
객체탐지 | 2022 | YOLO | [링크를걸겠습니다.](https://github.com/shiny0510/pycaret)




# 강조
**이 부분을 집중해주세요!** 감사합니다
__이 부분을 집중해주세요!__ 감사합니다


x

# 취소선
~~취소선~~


# 이미지 넣기 

<!-- tip) 이미지 크기 조절 -->
<!-- <img src="이미지 링크" width="너비 " height="높이"> -->
ex)
<img src="https://user-images.githubusercontent.com/31477658/85016059-f962aa80-b1a3-11ea-8c91-dacba2666b78.jpeg" width="700" height="370">

![텍스트](이미지 링크 주소) <br>
![CNN-Figure-02](https://user-images.githubusercontent.com/85111065/173890872-1592710c-4711-42a0-803c-6d37ebcd2b3e.png)


<img src="./APOD.jpg" width="300"> <br>

<img src="./APOD.jpg" width="100" height="100">



# 문자열 개행
방법1. 문장 마지막에 스페이스 두 번 이상 입력  
방법2. html <br> 태그를 사용 
방법2. html <br> 태그를 사용 


다음과 같이 체크박스를 표현 할 수 있습니다. 
* [x] 체크박스
* [ ] 빈 체크박스
* [ ] 빈 체크박스




<!-- 참고: https://shields.io/ -->

<!-- <img src="https://img.shields.io/badge/이름-색상코드?style=flat-square&logo=로고명&logoColor=로고색"/> -->

# Badge (뱃지)
기술 스택이나 사용 툴 등을 간결하게 표현하고 싶을 때
인스타, 블로그 등 다양한 바로가기 링크들을 깔끔하게 나타내고 싶을때
로고와 공식컬러를 포함한 예쁜 아이콘 뱃지

<img src="https://img.shields.io/badge/Firebase-FFCA28?style=flat-square&logo=firebase&logoColor=white"/>


# 뱃지에 링크걸기

<!-- <a href="링크"><img src="위에있는뱃지코드"/></a>  -->

<a href="https://www.naver.com/"><img src="https://img.shields.io/badge/Velog-3DDC84?style=flat-square&logo=Blogger&logoColor=white"/></a>





# 실습 


# Test 모델을 이용한 Test 도출

* Github Url: https://github.com/shiny0510/FewShot_GAN-Unet3D (꼭! 하이퍼링크)

* requirement: pandas, numpy, torch, seaborn, matplotlib

* 프로젝트 수행은 2023년 1월부터 2월부터 알파코 딥러닝 부트캠프에서 진행했다. 웹과 딥러닝 두 부분을 진행했으며, 웹 부분은 플라스크를 사용했다, 딥러닝은 CNN을 사용하였으며, 데이터는 0~9의 숫자 이미지로 이루어진 MNIST train 6만장 test 3만장으로 사용하였다. 결과 이미지는 output.jpg처럼 나왔고, 전체 설계도는 architecture.jpg로 만들었다. 참고는 Krizhevsky, Alex, Ilya Sutskever, and Geoffrey E. Hinton. "Imagenet classification with deep convolutional neural networks." Advances in neural information processing systems 25 (2012). 을 하였고, 느낌점은, CNN으로는 0~9 이미지의 학습 성능이 잘 나왔지만 transform을 어떻게 주냐에 따라서 성능을 감소시키는 기법들이 뭐인지 리포트하고 싶었다.

1. 수행 기관:  알파코 딥러닝 부트캠프 (역할: Method 튜닝, 전처리, 팀장, 트러블 슈팅)

2. 데이터: 환자 데이터 10000개, 정상인 데이터 20만개

3. Method:  전처리: 이미지 Normalize + MixUp(Augmentation) + Denosing               
            모델: CNN (Medical Image Analysis, 2019.05)
	         optimizer: Adam 
            loss: L1 loss
	![architecture](https://github.com/user-attachments/assets/7e70da73-5582-4112-8cd7-1764f659f608)


4. 결과: <br>

* confusion Matrix : ![output](https://github.com/user-attachments/assets/cf0f05d4-4e34-45f5-bd0f-4f6ea74fbc8e)


* 프로젝트 수행 중 문제: CNN으로는 0~9 이미지의 학습 성능이 잘 나왔지만 transform을 어떻게 주냐에 따라서 성능을 감소시키는 기법들이 있어서
  해당 기법들에 대한 고찰이 필요하였다.

5. 참고: Krizhevsky, Alex, Ilya Sutskever, and Geoffrey E. Hinton. "Imagenet classification with deep convolutional neural networks." Advances in neural information processing systems 25 (2012).

