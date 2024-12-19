## openAI GPT For Python Developers(Korean)



## 🚀 Book 
책 제목 : 개발자를 위한 openAI GPT - 추후 책 표지 추가 예정

<figure>
    <img src="https://github.com/LDJWJ/openAIGPT_kor/blob/main/bookcover.png" alt="kaggle" width=300 height=300>
</figure>

### my web site
 * 아직 확정 안됨.

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

## 시작하기 PART 01

### 01 챗GPT, GPT, GPT-3, DALL-E, Codex 
 * GPT 모델 생성 코드 예제 - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LDJWJ/openAIGPT_kor/blob/main/01_GPT_Example_V2.ipynb)

### 2장 OpenAI와 ChatGPT 기본 이해
 * 실습 코드 - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LDJWJ/openAIGPT_kor/blob/main/ch02_OpenAI_ChatGPT_V10_2412.ipynb)

### 3장 개발을 위한 사전 준비
 * Using GPT Chat Completions
 * 실습 코드 - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LDJWJ/openAIGPT_kor/blob/main/ch03_UsingGPTChatComp_V10_2412.ipynb)

### 4장 OpenAI API 활용 첫걸음
### 5장 OpenAI API 모델 탐색하기
 * 실습 코드 - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LDJWJ/openAIGPT_kor/blob/main/ch04_ch5_OpenAIStart_V10_2412.ipynb)

## PART 02 OpenAI GPT 대화 생성 실전 가이드 – 실전 모델 활용법
### 6장 대화 생성의 고급 기술 – temperature, 샘플링, 반복성 제어
### 7장 GPT 모델의 성능을 극대화하는 프롬프트 엔지니어링 기법
 * 실습 코드 - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LDJWJ/openAIGPT_kor/blob/main/ch06_ch07_chatUpgrade_V10_2412.ipynb)

## PART 03 음성 및 이미지 인식: Whisper와 CLIP의 실전 활용
### 05. GPT 모델로 텍스트 편집하기
 * 실습 코드 - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LDJWJ/openAIGPT_kor/blob/main/05_TEXT_EDIT_WITH_GPT_V2.ipynb)

### 06. 텍스트 조작 예제: 고급편
 * 실습 코드 - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LDJWJ/openAIGPT_kor/blob/main/06_Text_Manipulation_Example_V1.ipynb)

### 07. 임베딩
 * 실습 코드 - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LDJWJ/openAIGPT_kor/blob/main/07_Embedding_V1.ipynb)

### 08. 임베딩:고급편
 * 실습 코드 - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LDJWJ/openAIGPT_kor/blob/main/08_Embedding_Advanced_V10.ipynb)  

### 09. 미세 튜닝과 모범 사례
 * 실습 코드 - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LDJWJ/openAIGPT_kor/blob/main/09_fine_tune_V10.ipynb)   

### 10. 고급 미세 튜닝 - 약품 분류하기
 * 실습 코드 - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LDJWJ/openAIGPT_kor/blob/main/10_Advanced_FineTuning_V10.ipynb) 

### 11. 고급 미세 튜닝 - 챗봇 어시스턴트 만들기 
 * 실습 코드 - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LDJWJ/openAIGPT_kor/blob/main/11_fineTuning_chatbot_V10.ipynb)
 
 * 대화식 웹 앱 만들기 - [작업절차](./webApp.md)
 
### 12. OpenAI Whisper를 사용한 지능형 음성 인식
 * 실습 코드 - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LDJWJ/openAIGPT_kor/blob/main/12_openAI_Whisper_V10.ipynb)
 
### 13. 문맥과 기억: AI를 더 현실적으로 만들기
 * 실습 코드 - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LDJWJ/openAIGPT_kor/blob/main/13_Context_Memory_V10.ipynb) 
 
### 14. 인공지능 기반 Alexa 만들기 
 * 해당 작업은 로컬 컴퓨터에서 실행합니다.
 * 사전 설치하기 [Doc](./14_install.md)

### 15. OpenAI CLIP으로 이미지 분류하기
 * 실습 코드 - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LDJWJ/openAIGPT_kor/blob/main/15_OpenAI_CLIP_V10.ipynb)
 
### 16-17 DALL-E을 활용한 이미지 생성하기, DALL-E을 활용한 이미지 편집하기
 * 실습 코드 - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LDJWJ/openAIGPT_kor/blob/main/16_17_DALL_E_V10.ipynb) 
 
### 18. 다른 이미지에서 영감 얻기
 * 실습 코드 - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LDJWJ/openAIGPT_kor/blob/main/18_Image_Make_Variation_V10.ipynb) 

## 📚 Learn More
 - [01] ----
 - [OpenAI 개발자 플랫폼](https://platform.openai.com/)
 - [OpenAI Playground](https://platform.openai.com/playground)

### 퓨샷 학습
  - PyTorch - 토치메타(Torchmeta) - https://tristandeleu.github.io/pytorch-meta/ (PyTorch에서 few-shot learning과 메타-러닝을 위한 확장 및 데이터로더들을 모아둔 컬렉션)
  - 퓨 샷(few-shot) : https://github.com/oscarknagg/few-shot (깨끗하고 명확하며 검증된 코드로 few-shot learning 연구를 재현하기 위한 저장소)
  - 메타 전이 학습 : https://github.com/yaoyao-liu/meta-transfer-learning

