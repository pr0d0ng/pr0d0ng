# 💫 최영동 | Yeongdong Choi
> **Data & Quality Engineer | AI & Cloud Data Engineering**  
> *"데이터 파이프라인의 안정성부터 AI 모델의 현장 최적화까지, 엔드투엔드로 문제를 해결합니다."*

[![GitHub](https://img.shields.io/badge/GitHub-pr0d0ng-181717?style=flat-square&logo=github)](https://github.com/pr0d0ng)
[![Email](https://img.shields.io/badge/Email-cyd0303%40g.skku.edu-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:cyd0303@g.skku.edu)
[![Blog/Portfolio](https://img.shields.io/badge/Portfolio-Live_Demo-38BDF8?style=flat-square&logo=googlechrome&logoColor=white)](https://pr0d0ng.github.io)
[![Location](https://img.shields.io/badge/Location-Suwon%2C%20Korea-blue?style=flat-square&logo=googlemaps&logoColor=white)](#)

---

## 👨‍💻 About Me

- 🎓 **시스템경영공학(산업공학)** 학사 전공을 바탕으로 통계적 공정 관리(QC), 실험계획법(DOE), 정량적 최적화 감각을 체화했습니다.
- ☁️ **Microsoft Data School 2기**를 수료하며 Azure 기반 클라우드 데이터 파이프라인 및 지식 그래프(Knowledge Graph) RAG 시스템을 구축하여 **최우수상**을 수상했습니다.
- 🚀 현재 **삼성 청년 SW·AI 아카데미(SSAFY) 16기**에서 풀스택 SW 및 최신 멀티모달 VLM 파인튜닝/최적화 기법을 집중 탐구하고 있습니다.
- 💡 단순 모델 스케일업보다 **도메인 문제에 적합한 데이터 전처리, 아키텍처 재설계, 엄밀한 통계 검증**을 통해 실질적인 엔지니어링 임팩트를 창출하는 데 몰입합니다.

---

## 🛠 Tech Stack

### Cloud & Data Engineering
![Azure](https://img.shields.io/badge/Microsoft_Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)
![Databricks](https://img.shields.io/badge/Azure_Databricks-FF3621?style=flat-square&logo=databricks&logoColor=white)
![Event Hubs](https://img.shields.io/badge/Event_Hubs-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)
![Stream Analytics](https://img.shields.io/badge/Stream_Analytics-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)

### AI & Machine Learning
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![HuggingFace](https://img.shields.io/badge/Hugging_Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![XGBoost](https://img.shields.io/badge/XGBoost-EB5424?style=flat-square)
![OpenAI](https://img.shields.io/badge/GPT--4o-412991?style=flat-square&logo=openai&logoColor=white)

### Languages & Frameworks
![Python](https://img.shields.io/badge/Python_3.10+-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=sqlite&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)

---

## 📌 Featured Projects

### 1. [Qwen3-VL 기반 한국어 Scene-Text 객관식 VQA 성능 개선](https://github.com/pr0d0ng)
> **SSAFY 16기 AI Challenge (2026.09) | Kaggle Public Score 0.96127 달성**

- **Key Problem**: 베이스라인 모델(0.70점대) 및 단순 모델 스케일업(30B MoE: 0.95233) 시 미세 텍스트 판독 오인식 및 생성 형식 파싱 에러 발생.
- **Engineering Solution**:
  - **Direct Choice Logit Scoring & Answer-only Loss**: 불안정한 텍스트 생성 대신 선택지 로짓 직접 비교로 생성 오류 0% 제거 및 추론 가속화.
  - **Question-Aware OCR Localization**: EasyOCR을 텍스트 입력기가 아닌 관심 영역 탐색기로 재정의, 질문 관련 BBox 크롭 이미지를 원본과 병렬 입력(`Multi-Image V3: 0.95918`).
  - **Cyclic TTA & Vote-Switch**: 선택지 순환 추론으로 위치 편향을 제거하고, 2/3 합의 및 확신도 격차(≥0.08)를 충족하는 35개 난제만 정밀 보정.
- **Tech**: `Qwen3-VL-8B`, `PyTorch`, `BF16 LoRA`, `EasyOCR`, `Direct Logit Scoring`, `Cyclic TTA`

---

### 2. [Gitjabi: 지능형 IT 거버넌스 및 코드 인텔리전스 플랫폼](https://github.com/pr0d0ng)
> **Microsoft Data School 2기 최종 프로젝트 (2026.01 - 2026.02) | 🏆 최우수상 수상**

- **Key Problem**: 기술 의사결정 문서(PDF 370p+)와 실제 구현 코드 간 괴리로 인한 개발 리소스 및 컴플라이언스 검증 비용 낭비.
- **Engineering Solution**:
  - **Azure Databricks Auto Loader**: 비정형 지침 문서를 실시간 수집하여 지식 그래프 및 벡터 DB와 동기화하는 엔터프라이즈 파이프라인 구축.
  - **Knowledge Graph RAG**: GPT-4o 기반 슬라이딩 윈도우 청킹 기법으로 정책 노드를 정형화하고 검색 노이즈 사전 필터링 적용.
  - **트러블슈팅**: 분산 스트리밍 환경의 노드 ID 중복 충돌을 중앙 식별자 할당 로직으로 리팩토링하여 PostgreSQL과 AI Search 간 데이터 정합성 100% 확보.
- **Tech**: `Azure Databricks`, `Auto Loader`, `GPT-4o`, `FastAPI`, `React`, `PostgreSQL`, `Azure AI Search/Language`

---

### 3. [FacFLEXity: Azure 기반 AI FEMS 및 LLM 스케줄링 최적화](https://github.com/pr0d0ng)
> **Microsoft Data School (2025.12) | 실시간 전력 예측 & AGV 예지보전 & 공정 스케줄링**

- **Key Problem**: 공장 내 피크 전력 부하로 인한 요금 급증 및 설비 돌발 정지(Down-time) 리스크 대응.
- **Engineering Solution**:
  - **XGBoost 전력 소비 예측**: 전력 소비 패턴 예측 모델 구현 ($R^2: 0.9259$, 추론 지연시간 0.2903s).
  - **ViT+MLP 멀티모달 PdM**: AGV 장비 상태 진단 멀티모달 예지보전 모델 구축.
  - **LangChain & Databricks Serving LLM**: 실시간 예측 결과와 요금제를 연동하여 공정 가동 스케줄 자동 수립.
  - **트러블슈팅**: FastAPI 비차단 비동기 병렬 추론 파이프라인 구성 및 PyTorch 대용량 텐서 메모리 청킹으로 GPU OOM 방지.
- **Tech**: `Azure Databricks`, `LangChain`, `XGBoost`, `PyTorch (ViT+MLP)`, `FastAPI`, `Asyncio`

---

### 4. [Azure 기반 실시간 반도체 결함 탐지 플랫폼](https://github.com/pr0d0ng)
> **클라우드 센서 데이터 파이프라인 & 실시간 품질 관리 (2025.11)**

- **Key Pipeline**: Azure Event Hubs ➔ Stream Analytics ➔ AKS 배포 XGBoost ➔ Logic Apps 무서버 Teams 실시간 경보.
- **트러블슈팅**: 센서 시계열 데이터 분할 시 발생하는 데이터 누수(Data Leakage)를 방지하기 위해 `GroupShuffleSplit` 기법을 엄격 적용하여 과적합 없는 일반화 신뢰도 확보.
- **Tech**: `Event Hubs`, `Stream Analytics`, `AKS`, `XGBoost`, `Logic Apps`, `Power BI`

---

### 5. [SBW 전자식 변속 버튼의 인간공학적 레이아웃 최적화](https://github.com/pr0d0ng)
> **성균관대학교 시스템경영공학과 전공 연구 (2024.11 - 2024.12)**

- **Engineering Solution**: JavaScript & Web Speech API 기반 밀리초(ms) 단위 조작 반응 시간 및 오류율 로깅 웹 툴 자체 개발.
- **통계적 검증**: Two-way ANOVA (RCBD) 및 Tukey's HSD 사후 검증을 통해 수직형 레이아웃의 반응 시간 단축 효과 입증 ($p = 0.0569 < 0.1$).
- **Tech**: `JavaScript`, `Web Speech API`, `Python`, `Two-way ANOVA`, `Tukey HSD`

---

## 📜 Education & Certifications

### Education & Training
- **삼성 청년 SW·AI 아카데미(SSAFY) 16기** | Python 트랙 *(2026.07 - 2027.06 진행 중)*
- **Microsoft Data School 2기** | 클라우드 데이터 엔지니어링 집중 과정 *(2025.09 - 2026.02 수료)*
- **성균관대학교 자연과학캠퍼스** | 시스템경영공학과 학사 졸업 *(2021.03 - 2026.08, 학점: 3.37/4.5)*

### Honors & Awards
- 🏆 **최우수상** - Microsoft Data School 2기 최종 프로젝트 *(Microsoft, 2026.02)*
- 🥇 **Kaggle Public Score 0.96127 달성** - SSAFY 16기 AI Challenge *(2026.09)*

### Certifications
- **Microsoft Certified: Azure Data Fundamentals** *(Microsoft, 2026.01)*
- **SQLD (SQL 개발자)** *(한국데이터산업진흥원, 2025.04)*
- **ADsP (데이터분석 준전문가)** *(한국데이터산업진흥원, 2024.06)*
- **TOEIC Speaking IH (150점)** *(ETS, 2026.03)*

---

## 📊 GitHub Analytics

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=pr0d0ng&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" height="150"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=pr0d0ng&layout=compact&theme=tokyonight&hide_border=true" height="150"/>
</div>

<div align="center">
  <sub>Last updated: September 2026</sub>
</div>

<!--
**pr0d0ng/pr0d0ng** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
