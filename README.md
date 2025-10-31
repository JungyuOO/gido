# Prayer Countdown Website

기도하는 손과 움직이는 후광 효과가 있는 실시간 카운트다운 웹사이트입니다. 2025년 10월 31일 오후 14:00까지의 시간을 실시간으로 표시합니다.

## 🌟 Features

- **기도하는 손 이모지**: 중앙에 위치한 기도하는 손 이모지 (🙏)
- **움직이는 후광 효과**: CSS 애니메이션으로 구현된 지속적인 후광 효과
- **실시간 카운트다운**: 2025년 10월 31일 오후 14:00까지의 정확한 시간 표시
- **반응형 디자인**: 모바일, 태블릿, 데스크톱 모든 화면 크기 지원
- **성능 최적화**: GPU 가속 애니메이션과 메모리 효율적인 타이머
- **크로스 브라우저 호환성**: 모든 주요 브라우저에서 동작

## 🚀 Live Demo

웹사이트는 GitHub Pages를 통해 배포됩니다:
- **URL**: [여기에 GitHub Pages URL이 표시됩니다]
- **배포 가이드**: [DEPLOYMENT.md](DEPLOYMENT.md) 파일을 참조하여 GitHub Pages에 배포하세요

## 📱 Screenshots

### Desktop View
- 기도하는 손과 후광 효과
- 실시간 카운트다운 타이머
- 아름다운 그라디언트 배경

### Mobile View
- 반응형 레이아웃
- 터치 친화적 인터페이스
- 최적화된 폰트 크기

## 🛠️ Technology Stack

- **HTML5**: 시맨틱 마크업과 접근성
- **CSS3**: 
  - CSS Grid & Flexbox 레이아웃
  - CSS 애니메이션 (keyframes)
  - 반응형 미디어 쿼리
  - GPU 가속 최적화
- **Vanilla JavaScript**:
  - ES6+ 클래스 문법
  - 에러 핸들링
  - 메모리 관리
  - 성능 최적화

## 📋 Project Structure

```
prayer-countdown-site/
├── index.html          # 메인 HTML 파일 (모든 CSS/JS 포함)
├── README.md           # 프로젝트 문서
├── .gitignore          # Git 무시 파일
└── .kiro/              # Kiro 스펙 파일들
    └── specs/
        └── prayer-countdown-site/
            ├── requirements.md
            ├── design.md
            └── tasks.md
```

## 🚀 Quick Start

### 로컬에서 실행하기

1. **저장소 클론**:
   ```bash
   git clone [repository-url]
   cd prayer-countdown-site
   ```

2. **웹 서버 실행** (선택사항):
   ```bash
   # Python 3가 설치된 경우
   python -m http.server 8000
   
   # Node.js가 설치된 경우
   npx serve .
   
   # 또는 단순히 index.html을 브라우저에서 직접 열기
   ```

3. **브라우저에서 열기**:
   - 웹 서버 사용 시: `http://localhost:8000`
   - 직접 열기: `index.html` 파일을 브라우저로 드래그

### GitHub Pages 배포

자세한 배포 가이드는 [DEPLOYMENT.md](DEPLOYMENT.md) 파일을 참조하세요.

**간단 요약**:
1. GitHub 저장소 생성
2. 코드 푸시: `git push -u origin main`
3. GitHub Pages 활성화 (Settings → Pages)
4. 배포된 사이트 확인: `https://[username].github.io/[repository-name]`

## ⚙️ Configuration

### 타겟 날짜 변경

`index.html` 파일의 JavaScript 섹션에서 타겟 날짜를 수정할 수 있습니다:

```javascript
// 현재 설정: 2025년 10월 31일 오후 14:00
const targetDate = '2025-10-31T14:00:00';

// 다른 날짜로 변경 예시
const targetDate = '2025-12-25T00:00:00'; // 크리스마스
```

### 언어 변경

HTML의 `lang` 속성과 텍스트 내용을 수정하여 다른 언어로 변경할 수 있습니다:

```html
<html lang="en"> <!-- 영어로 변경 -->
```

## 🎨 Customization

### 색상 테마 변경

CSS의 그라디언트 배경을 수정하여 다른 색상 테마를 적용할 수 있습니다:

```css
body {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    /* 다른 색상으로 변경 가능 */
}
```

### 애니메이션 속도 조절

후광 효과의 애니메이션 속도를 조절할 수 있습니다:

```css
.halo-effect {
    animation: halo-rotation 4s infinite ease-in-out;
    /* 4s를 다른 값으로 변경 (예: 2s, 6s) */
}
```

## 🔧 Browser Support

- **Chrome**: 60+ ✅
- **Firefox**: 55+ ✅
- **Safari**: 12+ ✅
- **Edge**: 79+ ✅
- **Mobile Safari**: iOS 12+ ✅
- **Chrome Mobile**: Android 60+ ✅

### 구형 브라우저 지원

- CSS 애니메이션 미지원 브라우저를 위한 fallback 제공
- `prefers-reduced-motion` 미디어 쿼리 지원
- 자동 에러 핸들링 및 복구

## 📊 Performance Features

- **GPU 가속**: CSS `transform` 속성 사용
- **메모리 최적화**: 타이머 정리 및 메모리 누수 방지
- **DOM 최적화**: 불필요한 DOM 업데이트 최소화
- **애니메이션 최적화**: `will-change` 속성으로 브라우저 힌트 제공

## 🐛 Troubleshooting

### 일반적인 문제들

1. **카운트다운이 표시되지 않음**:
   - 브라우저의 JavaScript가 활성화되어 있는지 확인
   - 개발자 도구 콘솔에서 에러 메시지 확인

2. **애니메이션이 작동하지 않음**:
   - 브라우저가 CSS 애니메이션을 지원하는지 확인
   - `prefers-reduced-motion` 설정 확인

3. **모바일에서 레이아웃 문제**:
   - 뷰포트 메타 태그가 올바르게 설정되어 있는지 확인
   - 브라우저 캐시 새로고침

### 에러 리포팅

문제가 발생하면 다음 정보와 함께 이슈를 생성해 주세요:
- 브라우저 및 버전
- 운영체제
- 에러 메시지 (개발자 도구 콘솔)
- 재현 단계

## 📄 License

이 프로젝트는 MIT 라이선스 하에 배포됩니다. 자유롭게 사용, 수정, 배포할 수 있습니다.

## 🤝 Contributing

기여를 환영합니다! 다음과 같은 방법으로 기여할 수 있습니다:

1. **버그 리포트**: 이슈 탭에서 버그 신고
2. **기능 제안**: 새로운 기능 아이디어 제안
3. **코드 기여**: Pull Request 생성
4. **문서 개선**: README 또는 코드 주석 개선

### 개발 가이드라인

- 코드 스타일: 기존 코드 스타일 유지
- 테스트: 주요 브라우저에서 테스트
- 문서화: 새로운 기능은 문서 업데이트 필요

## 📞 Contact

프로젝트에 대한 질문이나 제안이 있으시면 GitHub 이슈를 통해 연락해 주세요.

---

**Made with ❤️ and 🙏**