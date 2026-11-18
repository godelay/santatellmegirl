# 스핑크스 Talk 탭 — 고민 카드 → 채팅 (11/18 확정)

06번 메모(럭 아이템 + 스핑크스 채팅 + 기억 DB)를 디벨롭한 결과. 06과 다른 부분은 **이 노트가 우선**.
시안: `시안/talk-tab-mockup.png` (① 분야 고르기 · ② 서브 질문 · ③ 채팅)

---

## 1. 목표
- 채팅을 끝낸 사용자가 **"이해받았다"** 고 느낀다. 위로·정답은 덤.
- 10/22 핵심 가치 2단계 "나를 기억하는 AI" 의 첫걸음.

## 2. 탭 구조 (4개)
| 탭 | 하는 일 |
|---|---|
| Home | 내 바퀴 · 친구 |
| Sphinx | **데일리 캡슐 굴리기만** (하루 1번, 럭 아이템·숫자·색·속담 — 지금 있는 것 그대로) |
| **Talk** | **스핑크스와 대화 (새로 생김)** |
| Me | 내 정보 · 쿠키 · 풀이 |

- 06의 "오늘의 럭 아이템"은 이미 Sphinx 탭 캡슐에 있으므로 새로 만들지 않는다. 대화는 캡슐과 **분리**.

## 3. 화면 흐름
```
① 분야 고르기
   스핑크스가 분야 카드 5장을 손패처럼 들고 있음
   "your Moon is restless today. what's on your mind?"
   [💌 Love] [🫂 Friends] [💼 Career] [🏠 Family] [🌱 Me]
        ↓ 하나를 누름
② 서브 질문
   스핑크스가 그 분야 행성으로 한 줄: "Venus is close to you this week. which one is it?"
   서브 질문 3~4개 + ✎ something else… (직접 쓰기)
        ↓ 하나를 누름
③ 채팅
   고른 질문이 첫 메시지 → 스핑크스가 차트로 먼저 읽어 줌
   사용자 메시지 3마디 무료 → "the sphinx is getting hungry… one cookie, three more questions."
   🍪 1개 = 3마디 더
```

## 4. 분야 5개
| | 분야 | 이런 고민 |
|---|---|---|
| 💌 | Love | 썸, 짝사랑, 연애 중 서운함, 이별 |
| 🫂 | Friends | 멀어짐, 서운함, 진짜 내 편 |
| 💼 | Career | 진로, 이직, 번아웃, 내 길이 맞나 (돈 고민도 여기) |
| 🏠 | Family | 부모님과의 갈등, 독립 |
| 🌱 | Me | 자존감, 정체된 느낌, 새 출발 |

- 건강은 뺀다 (민감, 운세로 다루면 위험).

### 서브 질문 초안 (분야마다 풀을 두고 매일 3~4개를 고름)
| 분야 | 서브 질문 |
|---|---|
| 💌 Love | someone I can't stop thinking about · I like them more than they like me · am I asking for too much? · why do I fall for the same type? |
| 🫂 Friends | a friend feels far away · I'm always the one who reaches out · who's actually in my corner? · I said something I can't take back |
| 💼 Career | is this the right path for me? · I'm burnt out but can't stop · should I quit? · everyone's ahead of me |
| 🏠 Family | I can't say no to my family · they don't get who I am · I want my own space · we keep having the same fight |
| 🌱 Me | I feel stuck lately · I keep overthinking everything · I want to start over · I don't know what I want |

- 쓰는 기준: 내 속마음 1인칭 · 짧게(25자 안쪽) · 예언을 바라는 질문 X("will he text back?") · 놀리는 말 X.

## 5. 스핑크스가 말하는 법
- **차트로 꿰뚫는다.** "Your Venus is in Cancer. When you like someone, you go all in… That's not too much. It's just a lot of heart."
- 단정적이고 구체적인 한 문장 (11/11 사주 상담 리서치: 기억에 남는 건 단정 · 구체 · 나와 관련된 한 문장).
- **금지: 지난 대화를 되읽어 주는 말.** "지난번에 서운하다고 했잖아" 같은 말은 절대 안 한다.
- 톤은 05번과 같이 좋게 좋게, 다정하게. 겁주지 않고 "이렇게 하면 좋은 주".

## 6. 기억 — 티 안 나게 쓴다
- 채팅 원문 전부 저장 + 메시지에서 사람·일정·고민·취향을 뽑아 저장 (06번 DB 초안 그대로).
- 고른 분야·서브 질문도 저장 (대화를 안 해도 "이 사람은 Love 를 자주 고른다").
- 기억은 **말로 꺼내지 않고**, 다음 날 보여줄 서브 질문 고르기와 차트 읽는 방향에만 반영.
  - 예: 이사 얘기를 한 사람 → 그 주엔 4하우스·달 쪽으로 읽고, Me 에 "I want to start over" 가 올라옴.
- **아이디별 저장 데이터는 볼 수 있어야 한다** (익명이든 가입자든). → 관리자 `/admin/people` 사람별 화면에 채팅·기억 칸.
- 사용자용 "What Sphinx remembers about you" (보기·지우기) 와 06번 4장 안전장치는 그대로.

## 7. 무료 / 쿠키
| | |
|---|---|
| 분야 · 서브 질문 고르기 | 무료 |
| 사용자 메시지 3마디 | **매일** 무료 (사용자 시간대 자정에 새로) |
| 그 뒤 | 🍪 1개 = 3마디 더 |

- 채팅 중 친구 이름이 나오면 궁합으로 잇기(06번 2장)는 그대로 후보.

## 8. 미리 알아둘 것
- **AI 비용:** 지금은 풀이 쓸 때만 AI 가 돈다. Talk 는 매일 · 메시지마다 + 기억 뽑기까지 돈다. 하루 상한 필요.
- **개인정보처리방침:** 채팅 원문 보관 · 운영자 열람 · 기억 지우기를 써야 함 (13세 미만 X, 위기 신호 → 988 안내, 06번 4장).
- 정책서 6장(Sphinx 탭 = 하루 가챠만)과 탭 구조가 바뀜 → 정책서 · 개발 계획서도 같이 고친다.

## 정할 것
- [ ] 스핑크스 첫 말("your Moon is restless today")을 매일 무엇으로 정할지 (오늘 달 위치?)
- [ ] 서브 질문 풀 크기 (분야당 몇 개)
- [ ] 쿠키 3마디를 다 쓰면 마무리 한 문장을 줄지
- [ ] 기억 보관 기간
