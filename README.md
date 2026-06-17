# VocaStudy 📖

> **AI OCR 기술과 Gemini API를 활용한 맞춤형 영단어 단어장 & 학습 메이트**

VocaStudy는 사용자가 업로드한 이미지나 텍스트 속 영단어를 인공지능(OCR 및 LLM)으로 분석하여 자동으로 영단어장을 구성하고, 다양한 모드로 복습할 수 있도록 돕는 클라이언트 사이드 웹 애플리케이션입니다.

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/lsmsonic/voca-study)

---

## ✨ 주요 기능

1. **AI OCR 및 단어 추출**
   - **Tesseract.js**를 이용한 이미지 텍스트 인식(OCR)으로 이미지 속 영어 단어를 추출합니다.
   - **Gemini API** 연동을 통해 추출된 단어의 정확한 한글 뜻, 품사(POS), 쉬운 영영 정의(English definition), 실생활 예문(Example sentences)을 실시간 생성합니다.

2. **3D 플래시 카드 학습 모드**
   - 한 화면에 한 단어씩 집중해서 학습하는 반응형 3D 카드 디자인을 제공합니다.
   - 클릭 시 카드가 3D 회전하며 단어 뜻과 예문을 보여줍니다.
   - Web Speech API(TTS) 기반의 즉각적인 발음 듣기(🔊) 기능을 지원합니다.
   - Oxford Learner's Dictionaries 및 Google 발음 검색 바로가기 링킹(🔗)이 제공됩니다.

3. **인터랙티브 퀴즈 모드**
   - 사지선다(객관식) 모드 및 스펠링 타이핑(주관식) 모드를 제공합니다.
   - 퀴즈 결과를 맞히면 축하 효과(Confetti)와 사운드가 울리며 오답 시 알림 진동/경고를 제공합니다.

4. **학습 기록 보관함 (History)**
   - 한번 분석한 단어장 목록은 `localStorage`에 자동 저장되어 언제든지 다시 복습하거나 삭제할 수 있습니다.
   - 서버 없이 100% 브라우저 내에서 안전하게 작동합니다.

5. **모바일 최적화 및 편의 기능**
   - iOS/Android Safari 및 Chrome 모바일 화면에 최적화된 글래스모피즘(Glassmorphism) UI.
   - 모바일 키보드 자동 철자교정(Autocorrect) 및 자동 대문자 변환(Autocapitalize) 방지.

---

## 🚀 시작하기

이 프로젝트는 별도의 서버 구성이 필요 없는 **Pure Static HTML/JS** 애플리케이션입니다.

### 로컬에서 실행하기

1. 본 저장소를 클론합니다.
   ```bash
   git clone https://github.com/lsmsonic/voca-study.git
   cd voca-study
   ```

2. 임의의 웹 서버(예: Live Server, http-server 등)를 이용하여 `index.html`을 엽니다.
   ```bash
   # 예: Python 간이 서버 실행
   python -m http.server 8000
   ```
   이후 브라우저에서 `http://localhost:8000`으로 접속합니다.

---

## ☁️ Vercel로 배포하기

본 저장소는 Vercel에 단 1초 만에 배포할 수 있습니다.

1. [Vercel New Project](https://vercel.com/new)에 접속합니다.
2. 본인의 GitHub 계정을 연동한 후 `voca-study` 저장소를 Import 합니다.
3. 별도의 빌드 커맨드 설정 없이 **Deploy** 버튼을 누르면 즉시 배포가 완료됩니다!

---

## 🛠️ 기술 스택

- **Frontend**: HTML5, CSS3 (Vanilla Custom Properties & Keyframes), JavaScript (ES6+)
- **OCR Engine**: Tesseract.js (CDN)
- **AI Model**: Google Gemini API (`gemini-1.5-flash`)
- **Animation & Effects**: Canvas Confetti (CDN)
- **Design System**: Glassmorphism, CSS Custom Properties, Google Fonts (Fredoka & Quicksand)
