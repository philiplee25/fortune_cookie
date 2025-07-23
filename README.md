# 🥠 Flutter 포춘쿠키 앱 개발 가이드

## 📋 프로젝트 개요

**앱 이름**: Fortune Cookie App  
**개발 플랫폼**: Flutter  
**타겟**: 개인 프로젝트

### 핵심 기능
- 메인 화면에 6개의 포춘쿠키 이미지 표시
- 사용자가 쿠키를 선택하면 오늘의 행운 메시지 표시
- 직관적이고 재미있는 UI/UX

---

## 🎯 앱 구조 설계

### 1. 화면 구성
```
Main Screen (메인 화면)
├── App Bar (앱바)
├── Fortune Cookie Grid (6개 쿠키 그리드)
└── Footer (하단 정보)

Fortune Detail Screen (행운 상세 화면)
├── Selected Cookie Animation
├── Fortune Message
└── Back Button
```

### 2. 주요 위젯 구조
- **GridView**: 6개의 포춘쿠키를 2x3 또는 3x2 그리드로 배치
- **GestureDetector**: 쿠키 선택 이벤트 처리
- **Container/Card**: 쿠키 이미지와 스타일링
- **Navigator**: 화면 전환 관리

---

## 🛠️ 개발 단계별 계획

### Phase 1: 프로젝트 셋업
- [ ] Flutter 프로젝트 생성
- [ ] 필요한 의존성 추가
- [ ] 기본 폴더 구조 설정
- [ ] 에셋 폴더 생성 및 이미지 추가

### Phase 2: 메인 화면 개발
- [ ] 앱바 디자인 및 구현
- [ ] 6개 포춘쿠키 그리드 레이아웃 구성
- [ ] 쿠키 이미지 및 호버 효과 추가
- [ ] 반응형 디자인 적용

### Phase 3: 인터랙션 구현
- [ ] 쿠키 선택 이벤트 처리
- [ ] 행운 메시지 데이터 모델 생성
- [ ] 랜덤 행운 메시지 로직 구현
- [ ] 화면 전환 애니메이션 추가

### Phase 4: 상세 화면 개발
- [ ] 행운 메시지 표시 화면 구성
- [ ] 선택된 쿠키 애니메이션 효과
- [ ] 뒤로가기 기능 구현
- [ ] 공유 기능 (선택사항)

### Phase 5: 최적화 및 배포
- [ ] 성능 최적화
- [ ] 다양한 화면 크기 테스트
- [ ] 앱 아이콘 및 스플래시 스크린 추가
- [ ] 빌드 및 테스트

---

## 📁 프로젝트 구조

```
fortune_cookie_app/
├── lib/
│   ├── main.dart
│   ├── screens/
│   │   ├── home_screen.dart
│   │   └── fortune_detail_screen.dart
│   ├── models/
│   │   └── fortune_model.dart
│   ├── widgets/
│   │   ├── fortune_cookie_widget.dart
│   │   └── fortune_grid_widget.dart
│   └── utils/
│       └── fortune_data.dart
├── assets/
│   ├── images/
│   │   ├── cookie1.png
│   │   ├── cookie2.png
│   │   ├── ...
│   │   └── cookie6.png
│   └── fonts/ (선택사항)
└── pubspec.yaml
```

---

## 🎨 디자인 컨셉

### 색상 팔레트
- **Primary**: `#FFA726` (따뜻한 오렌지)
- **Secondary**: `#FFE0B2` (연한 복숭아)
- **Accent**: `#FF7043` (진한 오렌지)
- **Background**: `#FFF8E1` (크림색)

### 폰트 스타일
- **제목**: Bold, 24px
- **본문**: Regular, 16px
- **행운 메시지**: Medium, 18px

### 애니메이션 효과
- 쿠키 선택 시 살짝 확대되는 효과
- 화면 전환 시 페이드 인/아웃
- 행운 메시지 표시 시 타이핑 효과 (선택사항)

---

## 💡 구현 아이디어

### 1. 포춘쿠키 선택 방식
- 각 쿠키에 고유한 ID 부여
- 선택 시 해당 쿠키가 "깨지는" 애니메이션
- 랜덤하게 행운 메시지 할당

### 2. 행운 메시지 카테고리
- 🍀 **행운**: "오늘은 특별한 기회가 찾아올 거예요!"
- 💕 **사랑**: "소중한 사람과의 만남이 기다리고 있어요"
- 💰 **재물**: "예상치 못한 좋은 소식이 있을 거예요"
- 🏆 **성공**: "노력한 만큼 좋은 결과가 따라올 거예요"
- 🌟 **행복**: "작은 것에서 큰 기쁨을 발견하게 될 거예요"
- 🔮 **미래**: "새로운 시작을 위한 완벽한 타이밍이에요"

### 3. 추가 기능 아이디어
- 하루에 한 번만 선택 가능한 제한 기능
- 선택한 행운 기록 보관
- 소셜 미디어 공유 기능
- 다국어 지원 (한국어/영어)

---

## 🚀 시작하기

### 1. 개발 환경 준비
```bash
flutter create fortune_cookie_app
cd fortune_cookie_app
```

### 2. 의존성 추가 (pubspec.yaml)
```yaml
dependencies:
  flutter:
    sdk: flutter
  cupertino_icons: ^1.0.6
  
dev_dependencies:
  flutter_test:
    sdk: flutter
  flutter_lints: ^3.0.0
```

### 3. 에셋 설정
```yaml
flutter:
  assets:
    - assets/images/
```

---

## 📚 참고 자료

- [Flutter 공식 문서](https://flutter.dev/docs)
- [Material Design 가이드라인](https://material.io/design)
- [Flutter 애니메이션 가이드](https://flutter.dev/docs/development/ui/animations)

---

## ✅ 완성 목표

이 프로젝트를 통해 다음을 달성할 수 있습니다:

- Flutter의 기본 위젯 활용 능력 향상
- 상태 관리 및 화면 전환 이해
- 사용자 인터페이스 디자인 경험
- 완전한 앱 개발 프로세스 경험

**예상 개발 기간**: 1-2주  
**난이도**: 초급~중급

---

*행운이 가득한 포춘쿠키 앱을 만들어보세요! 🥠✨*