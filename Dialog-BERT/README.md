# Dialog-BERT: 100억 건의 메신저 대화로 일상대화 인공지능 서비스하기

## 프리트레인

백억건의 한국어 카카오톡 데이터, 2억 건의 일본어 라인 데이터

형태소: MeCab, Khaiii

Subword 기반: SentencePiece, WordPiece 등

Combined: MeCab + SentencePiece

한국어는 공백기준으로 하면 별로다. 캐릭터 단위로 나누는게 좋다.

65억 토큰 50기가 30000보캡 코퍼스

## 프리트레인 하는 법

* 위키 vs 대화체

문장길이, 단어 변형

* Turn에 대한 구분

SEPT라는 토큰

화자별로 임베딩 부여

Turn SEP & EMB

* 일상대화 태스크

주어진 두 문장이 의미적으로 유사?

다음에 올 문장 적절?

다음에 올 리엑션 무엇?

* Semantic Textual Similarity

Query, Reply에 대해 유사도를 구함 BERT 사용

FAQ?! 질문 비슷한지!

* Query-Reply Matching

논리적으로 맞지만 감정적으로 안맞는건 답변으로 보지 않음
단순히 다음에 올 수 있는지(N

** Unpaired Data

인풋에 대해 어떤 문장이 오는 것이 적절한가

* Reaction Classification

리액션을 Class로 정의하고 Classification

우리가 하는 말 중 대부분은 리액션에 가까움: 빈도수 기준 상위 0.01% 문장이 전체 20%를 차지

* 일상대화 태스크 정리

Query Similarity, Reply Matching, Reaction

* Multi-turn 학습

## 서비스를 위한 BERT 경량화

* Knowledge Distillation

Large Model의 Softmax Output(=Knowledge)를 Small Model의 Output에 전수

BERT-Base: layer 12 head 12 hidden 768
SMall 10 8
XSmall

태스크별 선생님이 지식 전수해주기도 함


