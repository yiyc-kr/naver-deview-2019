# 어디까지 깎아봤니?: 모바일 서비스를 위한 가벼운 이미지 인식/검출 딥러닝 모델 설계

## backbone

프리트레인된 딥러닝 모델을 칭함

feature extractor, 즉 모든 이미지 기반 딥러닝 기술의 근본

## transfer ?

## Finetuning

* backbone 고정하고 미세하게 튜닝

## 딥 러닝 물체 분류/검출기 트레이닝 개요도

큰 데이터세 확보 -> 딥러닝 모델 큰 데이터에 학습(프리트레인) -> 프리트레인드 백본의 성능 관찰 -> 파인튜닝

## 큰 데이터셋 imageNet

transfer learning?

## model zoo 활용!!

## backbone의 성능

좋은 backbone을 써라


## 네이버 모델

ImageNet 성능은 좋은데 finetuning 성능이 상대적으로 떨어짐

위가 좁은 이유는 flop-efficient 위해

가벼운 디텍션 모델: SSD-lite

가벼운 모델은 테스트 로스가 훅 증가하는 오버피팅이 나중에 잘 일어나는 경향이 있다.



https://deview.kr/data/deview/2019/presentation/[115]어디까지+깎아봤니_모바일+서비스를+위한+가벼운+이미지+인식_검출+딥러닝+모델.pdf
