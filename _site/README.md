# 오사카 여행 가이드

오사카 여행 정보를 정리한 Jekyll 사이트입니다. 숙박, 교통, 음식점 정보를 탭 형식으로 제공합니다.

## 🌐 사이트

**[https://253eosam.github.io/travel-osaka](https://253eosam.github.io/travel-osaka)**

## 📁 프로젝트 구조

```
.
├── _layouts/
│   └── default.html          # 탭 네비게이션이 포함된 기본 레이아웃
├── assets/
│   └── css/
│       └── tabs.css          # 탭 스타일
├── docs/                     # 상세 문서 (참고용)
│   ├── accommodation.md
│   └── transportation.md
├── index.html                # 루트 페이지 (restaurants로 리다이렉트)
├── restaurants.md            # 🍜 음식점 페이지
├── accommodation.md          # 🏨 숙소 페이지
├── transportation.md         # 🚇 교통 페이지
├── _config.yml               # Jekyll 설정
└── Gemfile                   # Ruby 의존성
```

## 🚀 로컬 실행 방법

### 1. Ruby 환경 설정 (rbenv 사용)

```bash
# rbenv 설치
brew install rbenv ruby-build

# Ruby 3.2.0 설치
rbenv install 3.2.0
rbenv local 3.2.0

# 쉘 초기화
rbenv init
```

### 2. Jekyll 설치 및 실행

```bash
# Bundler와 Jekyll 설치
gem install bundler jekyll

# 프로젝트 의존성 설치
bundle install

# Jekyll 서버 실행
bundle exec jekyll serve
```

### 3. 브라우저에서 확인

```
http://localhost:4000
```

## 🐳 Docker로 실행 (간단)

```bash
docker run --rm -v "$PWD:/srv/jekyll" -p 4000:4000 jekyll/jekyll jekyll serve --force_polling
```

## 📝 정보 추가 규칙

새로운 정보를 추가할 때는 다음 규칙을 따릅니다:

1. **각 페이지별 내용**:
   - `restaurants.md`: 음식점 정보 (위치, 영업시간, 특징, 메뉴 등)
   - `accommodation.md`: 숙박 시설 상세 정보
   - `transportation.md`: 교통 정보 (공항 이동, ICOCA 등)

2. **링크 형식**:
   - 주소는 구글 맵 링크로 연결
   - 음식점/호텔 제목은 일반 텍스트, 위치에 링크
   - 참고 자료(블로그 등)는 별도 항목으로 추가

## 🔧 기술 스택

- **Jekyll 4.3**: 정적 사이트 생성기
- **GitHub Pages**: 호스팅
- **Jekyll Theme Cayman**: 베이스 테마
- **Custom CSS**: 탭 네비게이션

## 📄 라이선스

개인 여행 가이드 용도로 작성되었습니다.
