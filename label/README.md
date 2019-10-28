# 레이블링 조금 잘못돼도 괜찮아요: Clova가 레이블 노이즈 잡는 법

## 

* Active Learning for Labeling Cleaning

모델이 1차 레이블링

* 사람의 도움 없이 레이블 노이즈 제거

## 레이블 노이즈 잡는법!

* AutoML

Project Khan: AutoML Project for Chatbot AI builder

* 레이블링 바로잡는 AutoML

* Split - Train - Check 알고리즘

전체 데이터를 빠짐없이 체크하는 법

-> Vote

* MultiSplit - Train - Check - Vote 알고리즘

## PICO

Checker 결과 베이지안 확률 결합
레이블링의 Iterative Probabilistic correction
레이블링 히스토리를 Hidden Markov Modeling 통해 반영

## FAQ/Chat 데이터 셋에 적용해보기

Query-

Checker model: classifier-BERT

* 데이터셋 인텐트 분포의 변화 특징

쿼리의 이동: 일반적인 답변 인텐트 -> 구체적인 답변 인텐트

일반적인 답변으로 묶여있는 인텐트 class 사이즈 감소


