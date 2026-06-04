# OverLang
> 영상 속 정보의 공백을 해소하고, 시청 경험을 학습으로 연결하는 **AI 기반 영상 번역 및 학습** 웹 플랫폼입니다.

![OverLang Service Overview](./images/overlang-service-overview.png)

## 🚀 Key Features
- 🎙️ 영상 속 음성을 자막으로 변환하고 다국어 번역 제공
- 📝 영상 화면의 텍스트(PPT, 간판, 자막 등)를 추출하여 번역 제공
- 🔗 음성 정보와 화면 텍스트를 함께 분석하여 보다 완전한 영상 이해 지원
- 📚 핵심 단어, 주요 표현, 영상 요약 등 학습 콘텐츠 자동 생성
- 💡 문맥 기반 단어 설명 및 표현 학습 기능 제공
- ⚡ Redis Queue 기반 비동기 AI 영상 분석 처리

## 💡 Why OverLang?

### 1. 음성과 화면 텍스트를 함께 분석
기존 영상 번역 서비스는 주로 음성(STT) 기반 자막 생성에 집중하기 때문에, 화면에 등장하는 PPT, 간판, 자막, UI 텍스트 등은 충분히 활용되지 못하는 경우가 있습니다. OverLang은 STT와 OCR을 함께 활용하여 영상 속 음성과 화면 텍스트를 통합적으로 분석합니다.

### 2. 번역을 넘어 학습 콘텐츠로 확장
OverLang은 단순히 번역 결과만 제공하지 않고, 영상 내용을 기반으로 핵심 단어, 주요 표현, 요약 등 학습 콘텐츠를 생성합니다. 이를 통해 사용자는 영상을 시청하는 과정에서 자연스럽게 외국어 학습까지 이어갈 수 있습니다.

### 3. 실제 서비스 흐름을 고려한 구조
영상 분석은 시간이 오래 걸릴 수 있기 때문에 Redis Queue 기반 비동기 처리 구조를 적용했습니다. Frontend, Backend, AI Server를 분리하여 AI 분석 작업을 독립적으로 처리하고, 향후 OCR 품질 개선이나 학습 기능 확장에도 유연하게 대응할 수 있도록 설계했습니다.

## 🖥️ Service Preview
<table>
  <tr>
    <td align="center">
      <img src="./images/main.gif" width="250">
    </td>
    <td align="center">
      <img src="./images/upload.gif" width="250">
    </td>
    <td align="center">
      <img src="./images/dashboard.gif" width="250">
    </td>
  </tr>

  <tr>
    <td align="center"><b>메인 페이지</b></td>
    <td align="center"><b>업로드 페이지</b></td>
    <td align="center"><b>대시보드</b></td>
  </tr>

  <tr>
    <td align="center">
      <img src="./images/translate.gif" width="250">
    </td>
    <td align="center">
      <img src="./images/wordnote.gif" width="250">
    </td>
    <td align="center">
      <img src="./images/mypage.gif" width="250">
    </td>
  </tr>

  <tr>
    <td align="center"><b>번역 & 학습 페이지</b></td>
    <td align="center"><b>학습 노트</b></td>
    <td align="center"><b>마이페이지</b></td>
  </tr>
</table>

## 🏗️ System Architecture
![System Architecture](./images/architecture.png)

## 🛠️ Tech Stack
#### Frontend
![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![Vite](https://img.shields.io/badge/vite-%23646CFF.svg?style=for-the-badge&logo=vite&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white)
![Firebase](https://img.shields.io/badge/firebase-%23039BE5.svg?style=for-the-badge&logo=firebase)

#### Backend
![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![SpringBoot](https://img.shields.io/badge/springboot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![Spring Data JPA](https://img.shields.io/badge/Spring%20Data%20JPA-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
![Redis](https://img.shields.io/badge/redis-%23DD0031.svg?style=for-the-badge&logo=redis&logoColor=white)

#### AI/LLM
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![FastAPI](https://img.shields.io/badge/FastAPI-005571.svg?style=for-the-badge&logo=fastapi)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C.svg?style=for-the-badge&logo=pytorch&logoColor=white)
![WhisperX](https://img.shields.io/badge/WhisperX-000000?style=for-the-badge)
![EasyOCR](https://img.shields.io/badge/EasyOCR-4CAF50?style=for-the-badge)

#### Database
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)

#### Infrastructure & Deployment
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Railway](https://img.shields.io/badge/Railway-0B0D0E?style=for-the-badge&logo=railway&logoColor=white)
![Amazon S3](https://img.shields.io/badge/Amazon_S3-569A31?style=for-the-badge&logo=amazons3&logoColor=white)
![CUDA](https://img.shields.io/badge/CUDA-76B900?style=for-the-badge&logo=nvidia&logoColor=white)

## 👥 Team
<table>
  <tr>
    <td align="center">
      <img src="./images/jiwon.jpeg" width="130">
    </td>
    <td align="center">
      <img src="./images/gukhee.jpeg" width="130">
    </td>
    <td align="center">
      <img src="./images/yujeong.jpeg" width="130">
    </td>
  </tr>

  <tr>
    <td align="center"><b>Frontend</b></td>
    <td align="center"><b>Backend</b></td>
    <td align="center"><b>AI</b></td>
  </tr>

  <tr>
    <td align="center">이지원</td>
    <td align="center">한국희</td>
    <td align="center">서유정</td>
  </tr>
</table>
