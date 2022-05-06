# 주제 및 목표
머신러닝을 이용한 유투브 좋아요 수 예측


# 기획의도 및 배경

최근 마케팅에서 소셜미디어를 배제하고 성공하는 마케팅은 존재 하지 않는다고 말할 정도로 소셜미디어의 영향력이 매우 중요하고 큰 축을 담당하고 있다.
Youtube는 최근 3년 동안 300억만 달러를 크리에이터에게 지불했다고 밝혔다. 그리고 새로운 광고수입 채널은 2018년 초와 비교 했을 때 2배 가까이 증가세를 보이고 있다고 한다.

<img width="953" alt="image" src="https://user-images.githubusercontent.com/82385436/167084794-c9c63d15-5177-4ffe-91bc-bdda40b98be9.png">

많은 기업들이 Youtube 크리에이터의 영향력, 즉 영상의 조회수와 파급력을 예측 고려하여
비지니스 협업을 진행하며, 그에 맞는 결과를 만들어 가고 있다.
그렇다면, 높은 조회수는 구독자 혹은 시청자의 만족감의 지표인가?
동영상의 조회수와 리뷰수 그리고 채널의 구독자수로 영상의 ‘좋아요’ 수를 예측할 수 있을까? 동영상의 ‘좋아요’ 수는 어떤 상관관계를 가지며, 크리에이터에게 어떤 영향력으로 미칠 수 있을까?

# 선행자료 조사
- Youtube 조회수와 예상 수익에 대한 모델들이 크리에이터와 채널 분석으로 쓰이고 있다
- Youtube 추천 알고리즘에서 ‘좋아요’ 수가 미치는 영향을 간접적으로 확인 할 수 있다
- 조회수만으로 유익한 동영상이라고 판단할 수 없기 때문에, ‘좋아요’ 수로 많은 사람의 공감을 이끌었는지 확인 해 볼 수 있다.

# 데이터 수집 및 특성

Kaggle 에서 유투브 트렌딩에 관한 자료 https://www.kaggle.com/datasets/datasnaek/youtube-new
각 나라별로 데이터 따로 확인 할 수 있음.
<img width="880" alt="image" src="https://user-images.githubusercontent.com/82385436/167084994-c88f3e72-122d-4d39-9551-d830258ccb71.png">

# 사용할 프레임워크 및 라이브러리
1. sklearn()
- train_test_split
- LinearRegression - labelencoder
2. matplot.pyplot 
3. dt.hour()
4. dt.day_name() 

# 참고자료
‘Youtube Views Predictor’ (https://towardsdatascience.com/youtube-views-predictor-9ec573090acb)

‘A regression approach for prediction of Youtube views’ : Lau Tian Rui 외 4명 (https://beei.org/index.php/EEI/article/view/1630/1232)
