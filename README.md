
---

# Child-Sentiment-Analysis
아동들의 감정을 분석하기 위한 LLM 모델입니다. 이 모델은 아동 일기의 감정을 자동으로 요약하고 평가하며, 감정 분석과 타임라인 정리를 통해 일기 내용을 심층적으로 이해할 수 있도록 지원합니다.

---

## 기능 설명

### 출력 메소드
- **`showMetaInfo`** : 메타정보 확인
- **`showSummary`** : 요약 정보 확인
- **`showEvaluation`** : 감정 평가 점수 확인 (0~100)
- **`showAnalysis`** : 감정 분석 설명 확인
- **`showTimeline`** : 타임라인별 주요 일기 내용 확인
- **`showAll`** : 전체 출력

### 모델 메소드
- **`summarize`** : 일기 요약 메소드 (return `_summary`)
- **`evaluate`** : 일기 감정 평가 메소드 (return `_evaluation`)
- **`analyze`** : 일기 감정 분석 메소드 (return `_analysis`)
- **`createTimeline`** : 일기 타임라인별 정리 메소드 (return `_timeline`)

---

## 예시
### bad case
---
Name: John, Age: 18, Gender: male
Date: 2024-11-04, Time: 13:51:24

### Summary
**요약**: 오늘은 학교에서 실수로 혼나고 친구들과 어색해져서 힘든 하루였으며, 집에 돌아오는 길에 비까지 내려 더욱 우울한 기분이 들었어요. 숙제에 집중하지 못하고 부모님의 잔소리도 많아 하루가 빨리 끝나기를 바라는 마음이 들었습니다.

### Evaluation
**감성 평가 점수**: 15

### Analysis
**감정 분석**: 부정적 - 이 일기는 전반적으로 힘든 감정을 담고 있으며, 불안함과 우울함이 두드러진다. 여러 차례의 실수로 인해 자존감이 낮아지고, 선생님과의 갈등이 불편함을 가중시킨다. 친구들과의 어색한 관계는 사회적 고립감을 느끼게 한다. 점심시간에 혼자 있는 경험은 외로움을 더욱 심화시켜, 마음의 부담을 느끼게 만든다. 집으로 돌아오는 길에 비가 내린 것은 상징적으로 감정의 우울함을 더한다. 우산을 챙기지 않아 옷이 젖는 불운은 오늘 하루의 부정적인 기분을 고스란히 반영한다. 숙제에 대한 집중력 저하는 스트레스와 불안이 겹쳐진 결과로 보인다. 부모님의 잔소리는 자신에 대한 비판으로 해석될 수 있어 감정적인 압박감을 느끼게 한다. 하루가 빨리 끝나길 바라는 것은 현재의 괴로움을 피하고자 하는 강한 바람을 나타낸다. 그러나 희망적인 결말로 언젠가 이러한 날들이 지나가길 바란다는 의지는 감정의 회복 가능성을 엿볼 수 있게 한다.

### Timeline
**타임라인**:
1. 00:00:01 - 힘든 하루의 시작
2. 00:00:04 - 학교에서 실수로 선생님께 혼남
3. 00:00:07 - 친구들과의 사이가 어색해짐
4. 00:00:10 - 점심시간에 혼자 밥을 먹음
5. 00:00:14 - 집에 오는 길에 비가 내려 우울해짐
6. 00:00:16 - 우산 없이 옷이 젖음
7. 00:00:19 - 숙제가 잘 되지 않음
8. 00:00:22 - 부모님의 잔소리가 많았음
9. 00:00:25 - 하루가 빨리 끝나길 바람
10. 00:00:28 - 이런 날들이 지나가길 기원함'



### Good case
---
Name: John, Age: 18, Gender: male
Date: 2024-11-04, Time: 13:51:24

### Summary

**요약**: 오늘 꿈에서 친구들과 함께 풍선을 타고 모험을 하며 신비한 나무와 춤추는 물고기들을 만났고, 꿈에서 깬 후 아쉬움을 느꼈다. 언젠가 이런 모험을 실제로 경험하고 싶다는 소망이 생겼다.

## Evaluation
**감성 평가 점수**: 95

## Analysis
**감정 분석**: 긍정적 - 이 일기는 주로 즐거움과 상상력으로 가득 차 있으며, 꿈의 내용이 상쾌하고 신비로운 요소들로 구성되어 있다. 하늘의 풍선, 친구들과의 모험, 그리고 말하는 나무와 춤추는 물고기들은 창의적이고 즐거운 상상력을 자극한다. 이러한 요소들은 저자에게 큰 행복과 기쁨을 제공하며, 꿈에서 깨어난 후의 아쉬움조차 긍정적인 기억으로 여겨진다. 꿈의 모험은 현실에서의 희망으로 이어지며, 저자는 그리워하는 감정을 통해 미래의 즐거운 경험을 갈망하고 있다. 전체적으로 일기는 상상력과 즐거움이 조화를 이루며, 행복한 꿈을 통해 성취하고 싶은 바람을 드러내고 있다.

## Timeline
**타임라인**:
1. 00:00 - 재미있는 꿈을 꾼 이야기 시작
2. 00:04 - 하늘에 커다란 풍선들이 떠다님
3. 00:07 - 풍선을 타고 친구들과 모험을 떠남
4. 00:10 - 숲속을 지나 무지개 다리를 건넌 이야기
5. 00:14 - 고양이가 나타나 함께 놀기 시작
6. 00:16 - 신기한 나무를 만나서 나무가 말을 함
7. 00:19 - 나무가 내 이름을 부르며 놀람
8. 00:22 - 바다로 가서 물고기들이 춤을 추는 장면
9. 00:25 - 꿈에서 깼을 때 아쉬움 느낌
10. 00:28 - 언젠가 진짜로 모험을 떠나고 싶다는 바람

---

## 확장 필요 사항

1. 로그인 페이지에서 유저 메타정보 받기
2. 녹음 기능 구현
3. STT 모델을 활용하여 녹음 메타정보 받기
4. 모델 결과를 DB에 전송

---

![Project Screenshot](https://github.com/user-attachments/assets/c484dd8a-894d-4ee9-9955-52efcfb0e898)

---

