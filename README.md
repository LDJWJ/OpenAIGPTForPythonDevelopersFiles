## 제대로 시작하는 챗GPT와 AI활용



## 🚀 Book 
책 제목 : 제대로 시작하는 챗GPT와 AI활용

<figure>
    <img src="https://ldjwj.github.io/OpenAIGPTForPythonDevelopersFiles/image/bookcover_01.png" alt="ChatGPT" width=300 height=300>
</figure>

## 🎥 YouTube 가이드 영상
### 게시 완료된 영상
| 챕터 | 내용 | 영상 내용 |YouTube 링크 |
|------|------|-------------|------------- |
| 준비 | 구글 코랩 시작하기(준비중) | 구글 코랩 시작 <br> 구글 코랩 GPU 사용 <br> 구글 코랩 파일 생성 및 올리기 | [![YouTube](https://img.shields.io/badge/Watch-YouTube-red?logo=youtube)](https://www.youtube.com/watch?v=Tgxtc1UcUyI) |


## Install openai
```bash
pip install openai
```

### chatgpt.env 환경파일 준비
 * 일반적으로 환경 변수는 .env 파일에 저장되지만, 구글 코랩 사용자의 편의를 위해 이 책에서는 chatgpt.env를 사용합니다.
 * 실제 개발 환경에서는 보통 .env를 사용하니, 이 점을 기억해 두세요.


 ### 사전 준비
 * 구글 코랩 환경은 일정 시간이후에 초기화가 되기 때문에 두가지 작업을 매번 수행해야 함.
   * chatgpt.env 파일 생성이 필요.
     * 준비된 chatgpt.env를 내용을 변경하여 업로드 하거나 또는 API_KEY와 ORG_ID를 확인하여 생성한다.
   * pip install openai 설치
    * 라이브러리 불일치로 인한 에러 발생시, 추가 라이브러리 설치 필요.
    * 에러 : TypeError: Client.__init__() got an unexpected keyword argument 'proxies'
    * 해결 방법 : 안정된 버전 설치
    ```
    !pip install httpx==0.27.2
    ```

## 실습 코드
 * 아래 코드는 Google colab 환경을 기본으로 합니다.

##  PART 1 오픈AI와 챗GPT 제대로 이해하기

### 2장 오픈AI와 챗GPT
 * 실습 코드 - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LDJWJ/OpenAIGPTForPythonDevelopersFiles/blob/main/ch02_OpenAI_ChatGPT_V10_2412.ipynb)

### 3장 개발 사전 준비
 * 실습 코드 - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LDJWJ/OpenAIGPTForPythonDevelopersFiles/blob/main/ch03_UsingGPTChatComp_V10_2412.ipynb)

### 4장 오픈AI API 활용 첫걸음
### 5장 오픈AI API 모델 탐색하기
 * 실습 코드 - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LDJWJ/OpenAIGPTForPythonDevelopersFiles/blob/main/ch04_ch5_OpenAIStart_V10_2412.ipynb)


## PART 02 오픈AI GPT 대화 생성 실전 가이드
### 6장 대화 생성의 고급 기술
### 7장 GPT 모델의 성능을 극대화하는 프롬프트 엔지니어링 기법
 * 실습 코드 - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LDJWJ/OpenAIGPTForPythonDevelopersFiles/blob/main/ch06_ch07_chatUpgrade_V10.ipynb)

## PART 3 음성 및 이미지 인식: 위스퍼와 CLIP의 실전 활용
### 8장 위스퍼 음성 인식 기초
### 9장 위스퍼 텍스트 변환 최적화 기법
 * 실습 코드 - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LDJWJ/OpenAIGPTForPythonDevelopersFiles/blob/main/ch08_ch09_whisper_V10_2502.ipynb)

### 10장 오픈AI TTS를 활용한 음성 변환
 * 실습 코드 - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LDJWJ/OpenAIGPTForPythonDevelopersFiles/blob/main/ch10_TTS_V10_2412.ipynb)  

### 11장 오픈AI CLIP을 사용한 이미지 분류
 * 실습 코드 - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LDJWJ/OpenAIGPTForPythonDevelopersFiles/blob/main/ch11_CLIP_V10.ipynb)   

## PART 4 생성형 AI를 활용한 이미지 제작과 편집 기술
### 12장 DALL·E로 이미지 생성하기
### 13장 DALL·E로 이미지 편집하기
### 14장 다른 이미지에서 영감 얻기
 * 실습 코드 - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LDJWJ/OpenAIGPTForPythonDevelopersFiles/blob/main/ch12_ch14_DALLE3.ipynb) 

## PART 5 임베딩: 복잡한 데이터를 쉽게 이해하는 방법
### 15장 임베딩 소개
### 16장 텍스트 임베딩 활용 방법
### 17장 고급 임베딩 예제
 * 실습 코드 - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LDJWJ/OpenAIGPTForPythonDevelopersFiles/blob/main/ch15_17_Embedding_V10_2412.ipynb) 

## PART 6 파인 튜닝과 모델의 실전 활용
### 18장 퓨샷 학습 이해하기
### 19장 파인 튜닝의 이해 및 구현
### 20장 파인 튜닝 고급 예제: 정신 건강 코치
 * 실습 코드 - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LDJWJ/OpenAIGPTForPythonDevelopersFiles/blob/main/ch19_ch20_FineTuning_V10_2412.ipynb) 

### 21장 기억력 및 문맥 문제와 해결책
 * 실습 코드 - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LDJWJ/OpenAIGPTForPythonDevelopersFiles/blob/main/ch21_ContextMemory_V10_2412.ipynb) 
 

## PART 7 부록
### 부록 A 챗GPT 및 클로드 실습
### 부록 B 오픈AI 플레이그라운드 실습
### 부록 C 건강 상담 챗봇 구현하기
### 부록 D 작가 스타일 이미지 생성 앱
### 부록 E RAG로 노트북 추천받기
### 부록 F 오토젠을 활용한 AI 에이전트 이해하기

## 🎥 YouTube 가이드 영상
### 추후 제작 예정 영상
| 챕터 | 내용 | 영상 내용 |YouTube 링크 |
|------|------|-------------|------------- |
| 부록 A | 챗GPT 및 클로드 실습(준비중) | -- | [![YouTube](https://img.shields.io/badge/Watch-YouTube-red?logo=youtube)](https://www.youtube.com/watch?v=YOUR_VIDEO_LINK) |
| 부록 B | 오픈AI 플레이그라운드 실습(준비중)  | -- | [![YouTube](https://img.shields.io/badge/Watch-YouTube-red?logo=youtube)](https://www.youtube.com/watch?v=YOUR_VIDEO_LINK) |
| 부록 C | 건강 상담 챗봇 구현하기(준비중)  | -- | [![YouTube](https://img.shields.io/badge/Watch-YouTube-red?logo=youtube)](https://www.youtube.com/watch?v=YOUR_VIDEO_LINK) |
| 부록 D | 작가 스타일 이미지 생성 앱(준비중)  | -- | [![YouTube](https://img.shields.io/badge/Watch-YouTube-red?logo=youtube)](https://www.youtube.com/watch?v=YOUR_VIDEO_LINK) |
| 부록 E | RAG로 노트북 추천받기(준비중)  | -- | [![YouTube](https://img.shields.io/badge/Watch-YouTube-red?logo=youtube)](https://www.youtube.com/watch?v=YOUR_VIDEO_LINK) |
| 부록 F | 오토젠을 활용한 AI 에이전트 이해하기(준비중) | --  | [![YouTube](https://img.shields.io/badge/Watch-YouTube-red?logo=youtube)](https://www.youtube.com/watch?v=YOUR_VIDEO_LINK) |
| 2장 | 오픈AI와 챗GPT 이해하기(준비중)  | -- | [![YouTube](https://img.shields.io/badge/Watch-YouTube-red?logo=youtube)](https://www.youtube.com/watch?v=YOUR_VIDEO_LINK) |
| 3장 | 개발 사전 준비(준비중)  | -- | [![YouTube](https://img.shields.io/badge/Watch-YouTube-red?logo=youtube)](https://www.youtube.com/watch?v=YOUR_VIDEO_LINK) |
| 14장 | DALL·E를 활용한 이미지 변형(준비중) | --  | [![YouTube](https://img.shields.io/badge/Watch-YouTube-red?logo=youtube)](https://www.youtube.com/watch?v=YOUR_VIDEO_LINK) |
| 20장 | 파인 튜닝 고급 예제(준비중)  | -- | [![YouTube](https://img.shields.io/badge/Watch-YouTube-red?logo=youtube)](https://www.youtube.com/watch?v=YOUR_VIDEO_LINK) |



## 📚 Learn More


### 퓨샷 학습
  - PyTorch - 토치메타(Torchmeta) - https://tristandeleu.github.io/pytorch-meta/ (PyTorch에서 few-shot learning과 메타-러닝을 위한 확장 및 데이터로더들을 모아둔 컬렉션)
  - 퓨 샷(few-shot) : https://github.com/oscarknagg/few-shot (깨끗하고 명확하며 검증된 코드로 few-shot learning 연구를 재현하기 위한 저장소)
  - 메타 전이 학습 : https://github.com/yaoyao-liu/meta-transfer-learning

