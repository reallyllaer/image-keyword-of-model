**대중들이 생각하는 광고모델의 이미지 키워드 추출 - 2023.07.10 - 2023.08.04(1개월)**   

  ****

<aside>
💡 **기획의도: 광고주들이 원하는 연예인에 대한 대중들의 생각을 알아내어 적합한 모델을 선정**

</aside>

* 맡은 역할 : 데이터 수집 및 전처리, 말뭉치 구축, 시각화
* 데이터 요약 : 네이버 뉴스와 블로그에서 최근 3개월간의 뉴진스와 블랙핑크 데이터 수집

### 데이터 전처리

[1] 수집한 데이터의 토큰화하기 위한 사전학습모델 성능 확인 → 품사를 선택할 수 있는Kiwipiepy 선정

[2] KKM 꼬꼬마 세종 말뭉치에서 인물과 연관된 품사(’VA’:형용사, ‘XR’:어근)를 선택 → 해당 품사에서 이미지에 해당되는 단어들만 한 번 더 추출하고 해당 품사에 없는 단어는 추가함으로써 최종적으로 1476개의 인물 키워드 말뭉치 구축 

[3] 형용사와 어근을 명사화

### 인사이트 도출

[1] 단어의 중요도와 문서 간의 관계를 고려하여 TF-IDF 방식으로 TOP20 키워드 추출

[2] BPI(Brand Personality Index)의 5가지 지표(Sincerity, Excitement, Competence, Sophistication, Ruggedness)와 인물의 키워드 간의 유사도를 Word2Vec을 활용하여 최종 분류

[3] 방사형 차트를 이용해서 후보 간 비교를 통해 원하는 이미지에 더 어울리는 모델 선정 가능

### 개인적 성과

광고 모델 추천 알고리즘의 만들어 보면서 향후 개선된 비즈니스 모델에 대한 구상을 할 수 있었음

크롤링에 소요되는 시간이 길어서 다른 연예인들의 데이터를 수집하지 못한 점이 아쉬웠음. 미처 활용하지 못했던 추가적인 텍스트 분석을 진행했다면 더 의미있는 인사이트와 결과물을 만들었을 걸로 기대함