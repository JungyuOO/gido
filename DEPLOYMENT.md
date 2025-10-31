# GitHub Pages Deployment Guide

이 가이드는 Prayer Countdown Website를 GitHub Pages에 배포하는 방법을 설명합니다.

## 📋 Prerequisites

- GitHub 계정
- Git이 설치된 로컬 환경
- 이미 초기화된 Git 저장소 (✅ 완료됨)

## 🚀 Step-by-Step Deployment

### 1. GitHub 저장소 생성

1. **GitHub.com에 로그인**
2. **새 저장소 생성**:
   - 우측 상단의 "+" 버튼 클릭
   - "New repository" 선택
   - Repository name: `prayer-countdown-site` (또는 원하는 이름)
   - Description: `기도하는 손과 후광 효과가 있는 카운트다운 웹사이트`
   - Public으로 설정 (GitHub Pages 무료 사용을 위해)
   - README, .gitignore, license 추가하지 않음 (이미 로컬에 있음)
   - "Create repository" 클릭

### 2. 로컬 저장소를 GitHub에 연결

터미널에서 다음 명령어를 실행하세요:

```bash
# GitHub 저장소를 원격 저장소로 추가
git remote add origin https://github.com/[YOUR_USERNAME]/[REPOSITORY_NAME].git

# 기본 브랜치를 main으로 설정
git branch -M main

# 코드를 GitHub에 푸시
git push -u origin main
```

**예시**:
```bash
git remote add origin https://github.com/johndoe/prayer-countdown-site.git
git branch -M main
git push -u origin main
```

### 3. GitHub Pages 활성화

1. **GitHub 저장소 페이지로 이동**
2. **Settings 탭 클릭**
3. **왼쪽 사이드바에서 "Pages" 클릭**
4. **Source 설정**:
   - "Deploy from a branch" 선택
   - Branch: "main" 선택
   - Folder: "/ (root)" 선택
   - "Save" 버튼 클릭

### 4. 배포 확인

1. **배포 상태 확인**:
   - Actions 탭에서 배포 진행 상황 확인
   - 녹색 체크마크가 나타나면 배포 완료

2. **웹사이트 접속**:
   - URL: `https://[YOUR_USERNAME].github.io/[REPOSITORY_NAME]`
   - 예시: `https://johndoe.github.io/prayer-countdown-site`

3. **기능 테스트**:
   - 기도하는 손 이모지 표시 확인
   - 후광 효과 애니메이션 동작 확인
   - 카운트다운 타이머 정상 작동 확인
   - 모바일/데스크톱 반응형 레이아웃 확인

## 🔧 배포 후 설정

### Custom Domain (선택사항)

1. **도메인이 있는 경우**:
   - Settings → Pages → Custom domain
   - 도메인 입력 후 Save
   - DNS 설정에서 CNAME 레코드 추가

### HTTPS 강제 활성화

1. **Settings → Pages**
2. **"Enforce HTTPS" 체크박스 활성화**

## 📱 배포된 사이트 공유

배포가 완료되면 다음과 같이 URL을 공유할 수 있습니다:

### 공유 URL 형식
```
https://[YOUR_USERNAME].github.io/[REPOSITORY_NAME]
```

### QR 코드 생성 (선택사항)
- 온라인 QR 코드 생성기 사용
- 모바일 사용자들이 쉽게 접속할 수 있도록 QR 코드 생성

## 🔄 업데이트 배포

코드를 수정한 후 업데이트를 배포하려면:

```bash
# 변경사항 추가
git add .

# 커밋 생성
git commit -m "Update: [변경 내용 설명]"

# GitHub에 푸시 (자동으로 재배포됨)
git push origin main
```

## ⚠️ 주의사항

1. **배포 시간**: 첫 배포는 최대 10분 정도 소요될 수 있습니다
2. **캐시**: 브라우저 캐시로 인해 변경사항이 즉시 반영되지 않을 수 있습니다
3. **Public 저장소**: GitHub Pages 무료 버전은 public 저장소만 지원합니다
4. **파일 크기**: 개별 파일은 100MB, 전체 저장소는 1GB 제한이 있습니다

## 🐛 문제 해결

### 배포가 실패하는 경우

1. **Actions 탭 확인**: 에러 로그 확인
2. **파일 경로 확인**: 대소문자 구분 확인
3. **브랜치 확인**: main 브랜치에 코드가 있는지 확인

### 사이트가 로드되지 않는 경우

1. **URL 확인**: 올바른 GitHub Pages URL 사용
2. **브라우저 캐시 삭제**: Ctrl+F5 또는 시크릿 모드 사용
3. **DNS 전파 대기**: 최대 24시간 소요 가능

### 애니메이션이 작동하지 않는 경우

1. **HTTPS 확인**: HTTP가 아닌 HTTPS 사용
2. **브라우저 호환성**: 최신 브라우저 사용 권장
3. **JavaScript 활성화**: 브라우저 설정 확인

## 📊 성능 모니터링

배포 후 다음 도구들로 성능을 확인할 수 있습니다:

- **Google PageSpeed Insights**: 페이지 속도 분석
- **GTmetrix**: 상세한 성능 분석
- **Browser DevTools**: 네트워크 및 성능 탭

## 🎯 배포 완료 체크리스트

- [ ] GitHub 저장소 생성 완료
- [ ] 로컬 코드를 GitHub에 푸시 완료
- [ ] GitHub Pages 활성화 완료
- [ ] 배포된 사이트 접속 확인
- [ ] 기도하는 손 이모지 표시 확인
- [ ] 후광 효과 애니메이션 동작 확인
- [ ] 카운트다운 타이머 정상 작동 확인
- [ ] 모바일 반응형 레이아웃 확인
- [ ] 데스크톱 레이아웃 확인
- [ ] 공유 가능한 URL 확보
- [ ] HTTPS 접속 확인

모든 항목이 완료되면 배포가 성공적으로 완료된 것입니다! 🎉