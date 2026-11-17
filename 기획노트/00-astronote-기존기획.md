# Astronote 기획 메모

원본: Notion "Astrology / 점성술 웹 서비스 / 점성술" 페이지 (2026-09-27 마지막 수정)

## 왜 만드나
- 사람들이 궁합을 보는 이유는 **확신**을 얻고 싶어서다.
- Astronote가 답하려는 질문은 "나와 내 주변 사람들의 관계는 어떤가"이다.
- 한 줄 가치: *서로의 성향을 이해하고 더 오래 함께하기 위한 지혜*
- 모든 사람은 특별하고 싶어 한다. Astronote는 모든 사람을 특별하게 만들어 주는 경험이다.
- 아직 열린 질문: 사람들이 친구 별(카드)을 **수집하고 싶어 할까?**

## 궁합 표시 방식 (각도)
| 기호 | 이름 | 각도 | 모양 |
|---|---|---|---|
| ☌ | 합 | 0° | 두 점이 겹침 |
| ⚹ | 육각 | 60° | 별표 |
| □ | 사각 | 90° | 네모 |
| △ | 삼각 | 120° | 세모 |
| ☍ | 충 | 180° | 양끝 선 |

⊙ 태양 · ☽ 달 · ↑ 상승궁

## 화면
### 1. 랜딩
- 목적: 본인 차트 만들기 유도
- 다음 액션: 별 눌러보기 / 내 차트 만들기
- 로고 Astronote
- 제목 "What do the stars say about relationships?"
- 초대 문구 "Create your chart and invite friends to add their birth dates. Discover how you connect, how you differ, and what makes your relationship unique."
- 버튼 Create my Chart / Log in
- 예시 차트와 "Tap a star to see your compatibility", 버튼 Create my Chart

### 2. 내 차트
- 목적: (1) 차트 공유와 친구 초대, (2) 궁합 결제
- My Chart, 차트에 남은 별 개수
- 버튼 invite a friend / my profile
- My people: 카드 형식으로 수집
- Patterns in your stars: 친구가 10명 이상일 때만 관계 패턴 분석

### 3. 초대받은 화면
- 목적: 친구 차트에 별을 남기게 하고, 그다음 자기 차트를 만들게 유도
- 3-1 별 남기기:
  - 제목 "Your compatibility with XX"
  - 문구 "Leave your birthday. Ten seconds, no account." / "XX friends are already on this chart."
  - 입력 항목: 이름, 생일, 태어난 시간(모름 가능), 태어난 도시
  - 관계(선택): Friends / Seeing each other / Partners / Family / We work together
  - 메모(선택)
  - 버튼 See our compatibility
- 3-2 궁합 결과:
  - 궁합 내용
  - 버튼 "XX의 차트 보러가기" / Create my chart

## 정해야 할 것
- [ ] 궁합 결제를 어디서 걸지 (무료 범위 vs 유료 상세)
- [ ] 로그인 방식
- [ ] 출생 시간·도시까지 정확히 계산할지 (달·상승궁은 이게 있어야 계산됨)
- [ ] Patterns(10명 이상)에서 무엇을 보여줄지

## 지금 사이트 상태 (astronote.me, 2026-11-12 확인)
- 로그인: 구글만
- 친구가 내 차트(휠)에 "하트"를 남김
- 무료: 궁합 이름과 점수, 해석 첫 줄까지
- 유료 "쿠키"로 친구 전체 해석 열기: 1개 $1.99 · 3개 $4.99 · 5개 $7.99 · 10개 $14.99
- 안내 캐릭터 "스핑크스", 데일리 캡슐
- 운영: 디노트(Dnote)
