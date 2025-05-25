# 📐 자기계발 미션 트래커 - 기획/설계 및 개발환경 설정

---

## ✅ 1. 기획 / 설계

### 1-1. 앱 화면 목록 (App Screens)

| 화면 이름 | 설명 |
|-----------|------|
| 홈 화면(Home) | 오늘의 루틴 리스트 & 체크 UI |
| 루틴 등록 화면 | 루틴 이름, 반복 요일 설정 |
| 통계 화면 | 달성 이력 달력, 그래프 등 시각화 |
| 설정 화면 | 알림 설정, 초기화 등 (선택) |

---

### 1-2. 기능 흐름도 (기본 로직)

[홈 화면]   
└─ 오늘 루틴 조회 → 체크 여부 표시 (체크박스 클릭) → Hive에 저장

[루틴 등록 화면]   
└─ 이름 입력 + 반복 요일 선택 → 저장 → 홈에 반영

[통계 화면]   
└─ 일자별 완료 여부 → 달력에 시각화 → 루틴별 성공률 계산

[뱃지 시스템]   
└─ 연속 성공 여부 감지 → 뱃지 발급 → UI에 표시 (선택적 MVP)

---

### 1-3. 데이터 모델 설계

---

### 1-4. 저장소 구조 설계

| Box 이름      | 저장 데이터                         |
|---------------|--------------------------------------|
| `routinesBox` | 루틴 리스트 (`Routine` 객체)         |
| `dailyBox`    | 일별 체크 데이터 (`DailyRecord` 객체) |
| `badgeBox`    | 획득한 뱃지 리스트 (`Badge` 객체)     |

---

### 1-5. MVP 스펙 정의

| 기능               | 포함 여부                  |
|--------------------|----------------------------|
| 루틴 등록/삭제     | ✅                         |
| 반복 요일 설정     | ✅                         |
| 일별 체크 기능     | ✅                         |
| 달력 기반 통계     | ✅                         |
| 뱃지 시스템         | ❌ (차후 구현 예정)        |

---

## ✅ 2. 개발환경 설정

### 2-1. 사용 프로그램

Android Studio Meercat 2024.3.1 patch 2
Flutter_windows_3.29.1-stable

---

### 2-2. 디렉토리 구조 예시

lib/   
├── main.dart   
├── models/   
│ └── routine.dart   
├── screens/   
│ ├── home_screen.dart   
│ ├── add_routine_screen.dart   
│ └── stats_screen.dart   
├── widgets/   
│ └── routine_card.dart   
└── services/   
└── storage_service.dart   

---

### 2-3. 의존성 패키지 추가 (pubspec.yaml)

<pre>
<code>
dependencies:
  flutter:
    sdk: flutter
  hive: ^2.2.3
  hive_flutter: ^1.1.0
  path_provider: ^2.0.11
  table_calendar: ^3.0.9
  provider: ^6.1.1
</code>
</pre>