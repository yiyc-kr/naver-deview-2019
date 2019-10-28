# LaRva: Language Representation by Clova

## Large-Scale PLM Overview

* PLM

대량의 코퍼스를 프리트레인 후 각 태스크에 파인튜닝

BERT를 시작으로 다양하게 발전 

파라미터 수가 점점 올라가고 있음 

* 학습에 필요한 가격

XLNET: 7,300만원

* LaRva 공장 최적화

코퍼스 -> 프리프로세싱 보캡 -> 트레이닝 -> ㅇ평가

google-research/bert

* 공개코드의 문제점

비싼 티피유 한번 시도에 돈이 천만원 날아감

평가까지 시간도 많이 들어

* 평가를 쉽게

평가와 성능 리포트를 자동화 & 시각화

* Minio

AWS S3와 같은 인터페이스

checkpoint upload

* Downstream Task

태스크
기계독해, 감정분석, 

* 파인튜닝에 필요한 

reproducible

hyperparameter들 고정태스크 쉽게 추가 가능

* CLaF: Clova Language Framework

자연어 처리 프레임 워크 

* 평고와 성ㅌ능 자동화
학습진행 100케이 스텝마다 업로드

* 실시간 알림 받기 

1. Minio 서버에 체크포인트 업로드 슬랙 알림

## 전처리 효율적으로  

한국어 유니코드 토큰 비율이 적다 

멀티 케이스드 모델 

mono-lingual : ㅂ문어체 구분 

* 한국어 Vocab Benchmark

언노우토큰 Avg tokenized sequence length 줄임으로 최적화

* 스태틱 파일의 문제점  

저장 공간이 많이 든다  

소스 코퍼스  *  듀플리케이트  * 보캡

모델이 중복된 Trans를 보게 된다 

* 다이나믹 데이터 파이프라인 

마스킹을 맨 나중에 뚫음

코퍼스를 파일 여러개로 쪼갬
파일 하나에는 N개(10K~20K) 이상의 인스턴트가 존재  

* 장점 

소스 코퍼스만 있으면 되서 공간 절약  

중복  traininginstanse없이 매번 다른 마스크 만들 수 있음

* Variable Squence&Batch

성능 15퍼 정도 향상

* NSP가 필요한가 ?

## 학습을 빠르게 

V100 텐서코어 사용

BERT Large는 GPU당 16 배치 올라감

* 네트워크

RDMA: 프로토콜 오버헤드 줄이고 씨피유 안거치고 직접 메모리에 통신을 수행

GDRDMA 짱짱

* 토크나이저

Char vs Word?

Cased vs Uncased?

Uncased하면 자모음이 깨짐

* 속도 처리

cuBERT

Nvidia TensorRT 사용

* 모델 사이즈

작업해야한다


