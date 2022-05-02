# Analysis of songs according to the weather AND Lyrics
# 날씨와 가사에 따른 노래분석
---
## 기획의도 및 배경
---
무더운 여름날 친구들과 즐거운 밤을 보내고 있을 때, 
우리의 감성과 맞는 노래를 찾기 위해 시간을 흘려 보낸 경험이 모두 있을 것이다. 

노래는 많고, 정보는 넘쳐 나는데, 모든 노래를 생각나는 대로 들어보고 고르는게 그 감성의 찰나의 시간이 모두 흘러버리는데 사용되기도 한다. 사용자 니즈에 맞춰 탐색지점을 줄여 주고, 사람들의 다양한 음악 감상 니즈를 충족 시킬 수 있다면 더 많고 다양한 음악들을 즐길 수 있다.

계절에 맞춰서 날씨에 맞춰, 지금 내가 느끼는 직관적인 감정들을 나열해서 음악을 추천 받을 수 있다면, 무더웠던 그 여름의 밤이 조금 더 풍성하지 않았을까? 


그렇다면, 과연 이러한 추천을 이용할 사람들은 많을까?
현재 국내의 음악 스트리밍 서비스 산업의 시장규모 이다. 2017년 1조 4416억원의 규모 였으며, 2022년에는 2조 6079억원 으로 연평균 12.6% 성장률로 꾸준한 성장세를 보이고있다

   <img width="374" alt="image" src="https://user-images.githubusercontent.com/82385436/166190662-43668b8d-773e-48da-ac4e-078313fc6393.png">

그렇다면, 스트리밍 사용자들은 얼마나 자주 음악을 듣는가?

   <img width="293" alt="image" src="https://user-images.githubusercontent.com/82385436/166190698-1b413d59-8a36-4152-88dc-15e9a6b09abe.png">


스트리밍 사용자의 전체 40%의 사람들은 거의 매일 음악을 듣고 있다.

매일매일 듣는 음악에서 날씨에 반영된 기분에 따라 음악을 들을 수 있다면, 사용자에게 매일 새롭고 다른 경험을 제공할 수 있지 않을까?

## 선행자료 조사 
 + 기존 음악 스트리밍 서비스
	 * 현재의 대부분의 음원사이트의 추천 시스템은, 선호도를 기반으로 추천하고 있다. 
   * Content- Based filtering 과 Collaborative filtering 을 기반으로 사용자에 추천 서비스를 제공하고 있다.
   * 선호도에 따른 음악을 추천되고, 사용자별 많이 듣는 음악 차트를 제공하고 있기 때문에 트렌드에 맞는 음악에 듣는데 초점이 되고 있다.
   * 특정 가수, 가사, 장르에 대해서 검색할 수 있으나, 해당 정보가 없을 경우 노래 검색에 제약이 많다. 오차 범위가 크거나, 검색이 아에 되지 않는 경우가 발생 한다.
 + 날씨를 키워드로 기존 스트리밍 서비스 검색 결과
	* “ 더운 여름밤 신나는 노래” 에 대한 검색결과
   <img width="518" alt="image" src="https://user-images.githubusercontent.com/82385436/166191209-2276ddc6-0857-4176-ab11-1fdb464bff3b.png">

<img width="568" alt="image" src="https://user-images.githubusercontent.com/82385436/166191269-4c11ff6e-d669-43f0-aeb0-fd529e7e6602.png">
 
* 멜론과 Spotify 모두 가수, 가사, 혹은 장르별 검색은 활성화 되어 있으나, 앞서 언급한 세 분류를 제외한 특정 키워드에는 검색오차가 크며, 멜론의 경우에는 아에 검색이 불가 할 때가 있다.
* 멜론과 Spotify 두 군데 모두, 사용자가 편집해서 직접 올리는 플레이 리스트가 존재하며, 계절에 따른 분류로는 이러한 특정 사용자의 취향에 맞게 편집되어서 올라오는 리스트만 확인 가능하다.이는, 편집자의 취향이 반영되어 만들어진 리스트로 같은 분류의 여러가지 리스트를 직접 듣고 확인 해 봐야 나에게 맞는 리스트를 찾을 수 있다는 단점이 있다. 
* 기존의 스트리밍 사이트의 추천 시스템을 벗어나, 날씨에 반응하는 음악을 추천, 검색 할 수 있는 차별화가 있다. 
* 날씨와 + 감성이 결합된 검색어는 기존 스트리밍 서비스에서는 검색이 불가 하거나 추천 장르가 제한적(클래식이나, 동요로 한정) 이다. 

<img width="568" alt="image" src="https://user-images.githubusercontent.com/82385436/166191284-8bb659d8-157c-4951-9055-d0c61ca5c6db.png">

## 데이터 수집선행자료 조사
* 지니뮤직 API 
	+ 일간차트별로 크롤링 할수 있게끔 페이지 창이 직관적임
* 네이버지도 API 
  + 날씨가 직관적으로 표현되어있어서 크롤링후 나누기가 쉽다고 생각

## 사용할 프레임워크 및 라이브러리

1 . KoNLPy : 
- 한글 자연어 처리를 쉽고 간결하게 처리할 수 있도록 만들어진 오픈소스 라이브러리 
Okt함수 사용예정	
 tag 함수 사용예정 ( - Lucy Park 님의 추천)

2 . matplotlib

3 . Numpy

4 . tqdm

5 . pandas

6 . urllib.request

7 . json

8 . NaiveBayesClassifier

9 . wordcloud

## 참고자료
* '날씨에 맞는 노래 추천’
(https://github.com/Park-JE/NoraeChuchun)

* ‘개인의 감성분석과 머신러닝을 적용한 노래 추천 서비스’ :김동준, 이지연, 정수진, 김윤재, 김웅섭5 동국대학교 정보통신공학과
 (https://www.koreascience.or.kr/article/CFKO201735553776760.pdf)

* ‘MusicMood: Predicting the mood of music from song lyrics using machine learning’  :Sebastian Raschka
(https://paperswithcode.com/paper/musicmood-predicting-the-mood-of-music-from)


