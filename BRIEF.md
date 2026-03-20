# Databridge Hospital2 빌드 브리프

## 레포
https://github.com/seoyeon924/Hospital2

## 제품
피부과·성형외과 원장님 대상 매출/시술 데이터 분석 플랫폼 "Databridge"

## 빌드할 파일
1. `index.html` — 랜딩 페이지 (전체 섹션)
2. `demo.html` — 대시보드 데모 (차트 포함, 샘플 데이터)
3. `netlify.toml` — 배포 설정

## 디자인 레퍼런스 (ref-*.jpg 파일 참고)
- 화이트/라이트그레이 배경 (no dark mode)
- 카드형 레이아웃, 둥근 코너 (12-16px)
- 파랑 계열 accent (#2563EB)
- 도넛 차트, 라인 차트, 바 차트
- 좌측 사이드바 (대시보드)
- Pretendard 폰트

## 디자인 시스템 (반드시 준수)
- 폰트: Pretendard Variable (CDN)
- Primary: #0F1117
- Accent: #2563EB  
- Neutral: #F8F9FC → #EDF1F7 → #8B95A1 → #2E3B55 → #0F1117
- Semantic: success #16A34A, warning #F59E0B, error #EF4444
- 8px spacing grid
- touch target 최소 44px
- H1:56px/900, H2:40px/800, H3:28px/700, H4:20px/600, body:16px/400

## 금지사항 (절대 금지)
- 이모지 아이콘 (SVG만)
- 보라/바이올렛 그라디언트
- Inter, Roboto, Poppins 폰트
- 3-column feature grid with colored circle icons
- transition: all

## 랜딩 페이지 섹션 구성

### 1. 네비게이션
- 로고 "Databridge" + SVG 로고마크
- 링크: 기능, 요금제, 고객사례, 데모 보기
- 버튼: 무료 체험 (accent blue)
- sticky, backdrop-blur
- 모든 링크 padding 12px 16px (touch target)

### 2. Hero 섹션
- 배지: "피부과·성형외과 전용 데이터 플랫폼"
- 헤드라인: "원장님 시간은\n진료에만 쓰세요"
- 서브: "매출, 시술, 환자 데이터를 자동으로 분석합니다. 오늘 3건만 입력하면 이번 주 흐름이 바로 보입니다."
- CTA: "무료로 시작하기" (primary) + "데모 보기" (ghost)
- 소셜 증명: "현재 127개 클리닉 사용 중"
- 배경: 미묘한 그리드 패턴 or 라이트 그레이

### 3. KPI 통계 섹션
- 4개 숫자: "127개 클리닉", "평균 2.3시간 절약/주", "납품 4주 이내", "만족도 4.8/5"
- 숫자 크게 (48px weight 900), 레이블 작게

### 4. 기능 소개 섹션 (대시보드 스크린샷 포함)
- 제목: "원장님이 필요한 것, 전부 담았어요"
- 탭 or 토글 방식으로 기능 전환
- 기능들: 시술 매출 분석, 환자 재방문율, 경쟁사 모니터링, 마케팅 채널 분석
- 각 기능 설명 + 우측에 대시보드 목업 (Chart.js로 인라인 렌더링)

### 5. 이런 원장님께 섹션
- 4개 카드: "엑셀로 관리 중인데 분석이 어렵다", "경쟁 병원 리뷰가 얼마나 늘었는지 궁금하다", "광고 효과를 모르겠다", "재방문 환자 비율을 높이고 싶다"
- 체크마크 아이콘 + 텍스트

### 6. 요금제 섹션
- 스타터: 무료 (3개월), 프로: 49,000원/월, 엔터프라이즈: 문의
- 추천 뱃지 (프로에)
- 각 플랜 features 리스트

### 7. FAQ 섹션
- 6개 질문, 아코디언

### 8. CTA 섹션
- 다크 카드 배경
- "오늘 시술 3건만 입력하면 이번 주 매출 흐름이 바로 보여요"
- 버튼 2개

### 9. 푸터
- 로고, 소셜, 이용약관, 개인정보처리방침

## 데모 대시보드 (demo.html)

### 레이아웃
- 좌측 사이드바 (240px): 로고, nav 메뉴, 하단 사용자 정보
- 메인 컨텐츠: 헤더 + 그리드 레이아웃

### 사이드바 메뉴
- 대시보드 (홈)
- 시술 입력
- 매출 분석
- 환자 분석
- 경쟁사 모니터링
- 마케팅 채널
- 설정

### 대시보드 메인
- 상단: "안녕하세요, 원장님 👋" + 날짜
- KPI 카드 4개: 이번 주 매출 / 전주 대비 / 시술 건수 / 재방문율
- 차트 행 1: 주간 매출 라인 차트 (Chart.js) + 시술별 도넛 차트
- 차트 행 2: 마케팅 채널 바 차트 + 환자 재방문 현황 테이블
- 하단: 최근 시술 기록 테이블

### 차트 데이터 (샘플)
- 주간 매출: [월 2.1M, 화 1.8M, 수 3.2M, 목 2.7M, 금 4.1M, 토 5.3M, 일 1.2M]
- 시술별: 보톡스 35%, 필러 28%, 리프팅 22%, 기타 15%
- 마케팅: 인스타 42%, 네이버 31%, 카카오 18%, 기타 9%

## 기술 스택
- 순수 HTML/CSS/JavaScript (프레임워크 없음)
- Tailwind CSS CDN
- Chart.js CDN
- Pretendard CDN
- Lucide Icons (SVG 직접 인라인)

## 완료 후 작업
1. git add -A
2. git commit -m "feat: complete Databridge hospital landing + dashboard"
3. git remote add origin https://github.com/seoyeon924/Hospital2.git
4. git push -u origin main
5. openclaw system event --text "Done: Hospital2 랜딩+대시보드 빌드 완료. GitHub push 완료." --mode now

