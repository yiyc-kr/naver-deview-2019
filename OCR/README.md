# 문자인식(OCR), 얼마나 정확하지? (문자인식 성능을 정확하게 측정하는 방법)

## 성능평가의 중요성 

* 어떤 모델을 적용해야 하나

## 인식 과정 

* 문자 검출 -> 

## 기존 평가 방법

Recall: TP/(TP+FN)
Precision: TP/(TP+FP)
위 둘은 반비례관계라 둘 다 보아야 함

문자 검출 -> 문자 인식 
IoU: 정답(Ground Truth)와 예측(Prediction) 박스가 얼마나 겹치는지 확인
WEM(Word Based Exactly Matching): 정답과 에측 단어가 정확히 일치하는지 체크
1-NED(Normalized Edit Distance) 인식 평가 방법: 두 단어간 편집 거리를 측정한 뒤 긴 단어의 길이로 정규화
End-to-End(검출+인식) 평가: 순차 평가처리 

## 기존 방법의 문제점

검출알고리즘: EAST, PixelLink
고유명사!
One-to-Many 문제

## 매우 간단하지만 정확하고 정교한 방법

엣지케이스

검증 방법을 바꿈

## 신규 방법에 대한 검증 사항

One-to-Many, Many-to-One 문제는 얼마나 발생하나?

기본 평가셋(=단어 단위)과 호환 가능한가?

신규 평가 방법은 믿을만 한가?

검출기:EAST, pixel link /  인식기: grcnn, aster

Arbitrary text shape 대응 가능

논문: arxiv.org/abs/1908.11060
git: github.com/naver/popeval
