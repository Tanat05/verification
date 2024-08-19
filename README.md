모든 비속어/욕설 판별기의 대한 성능을 비교합니다.
Compare the performance of all profanity/cursive discriminator.
# 데이터
- [korean-malicious-comments-dataset](https://github.com/ZIZUN/korean-malicious-comments-dataset): 한국어 악성댓글 데이터셋 (10,000문장)
- [Curse-detection-data](https://github.com/2runo/Curse-detection-data): 각종 커뮤니티 사이트의 댓글의 욕설 여부를 분류한 한글 데이터셋 (5,825문장)
- [kmhas_korean_hate_speech](https://huggingface.co/datasets/jeanlee/kmhas_korean_hate_speech): 온라인 뉴스의 댓글를 8가지로 세분화하여 분류한 데이터셋 (78,978문장)
- [Korean Extremist Website Womad Hate Speech Data](https://www.kaggle.com/datasets/captainnemo9292/korean-extremist-website-womad-hate-speech-data/data): 한국 극단주의 웹사이트의 데이터를 분류한 데이터셋 (2,081문장)
- [LGBT-targeted HateSpeech Comments Dataset (Korean)](https://www.kaggle.com/datasets/junbumlee/lgbt-hatespeech-comments-at-naver-news-korean): 네이버 뉴스 성소수자 관련 댓글을 분류한 데이터셋 (8,837문장)
- [korean-hate-chat-data](https://www.kaggle.com/datasets/tanat05/korean-hate-chat-data): korcen으로 분류한 korcen-ml의 학습 파일 중 일부(3,000,000문장)(랜덤 10,000문장만 사용)

# 모델
> PYHTON
- [korcen](https://github.com/KR-korcen/korcen): 키워드 기반 비속어 판단 모듈
- [korcen-ml](https://github.com/KR-korcen/korcen-ml/blob/main/README.md): korcen으로 분류한 데이터를 학습한 딥러닝 기반 비속어 판별 모델
- [badword_check](https://github.com/Nam-SW/badword_check): 입력한 글(한글)이 욕설인지 아닌지를 딥러닝을 통해 판별하는 모델
- [CurseDetector](https://github.com/mangto/CurseDetector): 한글 유사도와 한글 발음 유사도를 이용한 욕설/비속어/금지어 필터링
> C

> JAVA
- [BadWordFiltering](https://github.com/VaneProject/bad-word-filtering)

> JAVASCRIPT
- [Cenkor](https://github.com/sh9351/cenkor): 손쉬운 비속어 검열(korcen 데이터셋 이용)

> etc....


# 성능 검증
> 데이터와 결과가 일치한 개수 / 전체 데이터 개수

|  | [korean-malicious-comments-dataset](https://github.com/ZIZUN/korean-malicious-comments-dataset) | [Curse-detection-data](https://github.com/2runo/Curse-detection-data) | [kmhas_korean_hate_speech](https://huggingface.co/datasets/jeanlee/kmhas_korean_hate_speech) | [Korean Extremist Website Womad Hate Speech Data](https://www.kaggle.com/datasets/captainnemo9292/korean-extremist-website-womad-hate-speech-data/data) | [LGBT-targeted HateSpeech Comments Dataset (Korean)](https://www.kaggle.com/datasets/junbumlee/lgbt-hatespeech-comments-at-naver-news-korean) | [korean-hate-chat-data](https://www.kaggle.com/datasets/tanat05/korean-hate-chat-data) | 평균 처리 속도 |
|------|------|------|------|------|------|------|------|
| [korcen](https://github.com/KR-korcen/korcen) | 0.7121 | 0.8415 | 0.6773 | 0.6305 | 0.4479 | 0.9857 | 9ms |
| [korcen-ml](https://github.com/KR-korcen/korcen-ml/blob/main/README.md) | **0.8395** | **0.8432** | **0.8851** | **0.7130** | 0.6919 | **0.9941** | 40ms |
| [badword_check](https://github.com/Nam-SW/badword_check) | 0.5829 | 0.6761 |  | 0.6410 | 0.4738 | 0.7980 | 43ms |
| [CurseDetector](https://github.com/mangto/CurseDetector) |  | 0.5679 |  | 0.5785 |  | 0.6657 | 267ms |
| [Cenkor](https://github.com/sh9351/cenkor) |  | 0.8317 |  | 0.6275 |  |  | **0.2**ms |

# 테스트 환경
> i7-11800H @ 2.30GHz
> 32GB 3200MHZ
> RTX 3060 Laptop
