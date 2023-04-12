# 🎯 사파고
![image](https://user-images.githubusercontent.com/119157378/231580536-b3eca26e-0ed9-4d34-b737-d482b649dc0d.png)


## 📊프로젝트 PPT 링크
발표용 슬라이드: https://docs.google.com/presentation/d/1PogaIb9RDD5M4xf4nUrF3TJtWUwVQ_cf/edit#slide=id.p11

## ✨ 프로젝트 소개
![image](https://user-images.githubusercontent.com/119157378/231584076-95d4c972-5e31-4a72-bd1f-26f802875040.png)


#### 사투리 발화는 고유의 억양과 특성이 있어 별도의 음성인식 구축이 필요하다. 이를 통해 사투리를 표준어로 번역하거나 음성인식 분야에 활용 가능하게 하는것이 목표
*출처 : MBC 아빠! 어디가?.  "'모닸재..?' 할머니의 사투리에 당황한 후와 찬형이, #16, 일밤 20140216" MBCentertainment, 2014년 4월 15일, 동영상 2:50-3:10, https://www.youtube.com/watch?v=2QkyNzASWt8*

-----------------------------------------------------------------------------------------------------------------------------
#### 데이터 설명
![image](https://user-images.githubusercontent.com/119157378/231585104-f5f66ee7-e8b5-4d92-b7ea-1a3131ef926e.png)




## ✨ 프로젝트 과정
### **사파고 프로세스**

  ![image](https://user-images.githubusercontent.com/119157378/231585329-1078e58f-cacd-4e21-8245-196ba2bd9631.png)


  - 입력받은 데이터의 특징 벡터 추출 
  - Random Forest로 학습시켜 표준어와 사투리를 분류함
  - 사투리로 분류가 된다면 음성파일을 텍스트로 변환  
  - 위 텍스트를 Vectorizer 와 TF-IDF 를 이용하여, 미리 생성한 말뭉치에서 가장 유사한 표준어를 텍스트로 출력.


### **문장 유사도 측정 방식**
  
  ![image](https://user-images.githubusercontent.com/119157378/231586388-821c28fd-df53-4657-97b9-1fe97058d305.png)
  
1) CountVectorizer
  - 단어들의 카운트(출현 빈도(frequency))로 여러 문서들을 벡터화
  - 문서 단어 행렬 (Term-Document Matrix, TDM))
2) TF-IDF
  - 단어마다 중요도를 고려하여 가중치를 주는 통계적인 단어 표현 방법
  - 가중치 계산 : 단어의 출현 빈도(TF) X 역문서 빈도(IDF)


### **3. Test Data 결과**

![image](https://user-images.githubusercontent.com/119157378/231586977-b37e449e-b022-43eb-85f5-cede30f9cfde.png)

### **4. 결과**

  - 테스트 데이터에서는 멜스펙토그램, 랜덤포레스트의 조합이 최고성능을 보였음 
  - 텍스트화 과정 중 일부 발음 뭉개지는 현상이 발견됨
  - 전반적으로 경상 지역의 사투리가 가장 잘 분류됨
  - 방대한 양의 말뭉치와 다수의 발화자를 확보한다면, 세세한 부분까지 표준어로 번역 할 것으로 보임




## 📜 기술 스택
![image](https://user-images.githubusercontent.com/119157378/231590080-36019f46-a9b3-4050-93cb-c0f09571a897.png)

