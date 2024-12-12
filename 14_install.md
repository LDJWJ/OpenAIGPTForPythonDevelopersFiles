### 14. 인공지능 기반 Alexa 만들기

### 개발 환경
 * OS : Window 11
 * GPU/CPU : CPU
 * Python Version : 3.9.5 (default, May 18 2021, 14:42:02) [MSC v.1916 64 bit (AMD64)]
 * 아나콘다 Version : 22.9.0
 * 라이브러리 버전
```
python                    3.9
openai                    1.5.0
openai-whisper            220231117
click                     8.1.7
torch                     2.1.2
spacy                     3.7.2
speechrecognition         3.10.1
pyaudio                   0.2.14
pydub                     0.25.1
gtts                      2.4.0
```
 
### 작업 절차

#### 01. 가상환경 만들기 
 * 내용 : 가상환경을 만들고, 설치를 위해 권한 문제로 오류가 발생할 수 있습니다. Anaconda Prompt를 관리자 권한으로 실행해 주세요.
 
 * 가상환경 만들기 - 사전 아나콘다 설치 필수. 여기에서 최신 Python 버전을 호환하지 않는 프로그램이 있어, 3.9로 설치를 진행합니다. 23/12월 기준 Python을 3.12를 설치하여 아래 라이브러릴 설치를 진행했을 경우, 정상적으로 설치가 진행되지 않는 부분이 있습니다.
```
conda create --name myenvAI python==3.9
```
 * myenvAI는 가상환경 이름으로 사용자 지정이 가능합니다.

 * 가상환경 활성화 및 pip 설치
```
conda activate myenvAI
conda install pip
```

#### 02. 라이브러리 설치 
 * 일반적으로 버전을 지정하여 설치하지 않고 설치시, 호환이 안되는 패키지 들로 인해 오류가 발생할 수 경우, 다음과 같이 실행 버전을 지정해서 설치 수행해 보기
```
python.exe -m pip install --upgrade pip
pip install openai
pip install click
pip install openai-whisper
```

패키지의 버전을 지정해서 설치할 경우,
```
python.exe -m pip install --upgrade pip
pip install openai==1.5
pip install click==8.1.7
pip install openai-whisper==20231117
```

#### 03. spaCy 모델 설치 및 다운로드
 * spaCy는 자연어 처리(Natural Language Processing, NLP)를 위한 파이썬 라이브러리 중 하나로, 텍스트 데이터를 처리하고 분석하는 데 사용됩니다. spaCy는 빠르고 정확한 토큰화(Tokenization), 형태소 분석(Morphological Analysis), 개체 인식(Named Entity Recognition), 구문 분석(Syntactic Parsing) 등 다양한 NLP 작업을 지원합니다.

 * 최신 버전 설치 진행
```
pip install spacy
python -m spacy download en_core_web_md
```

 * 버전을 지정해서 설치 진행
```
pip install spacy==3.7.2
python -m spacy download en_core_web_md
```

#### 04. speech_recognition 라이브러리 설치
 * 파이썬에서 음성 인식을 수행하기 위한 라이브러리입니다. 이 라이브러리는 다양한 음성 인식 엔진과 상호 작용하고, 오디오 데이터를 텍스트로 변환하는 기능을 제공합니다.
```
pip install SpeechRecognition==3.10.0
```
  
 * 최신 버전 설치 진행
```
pip install SpeechRecognition
```

 * 버전을 지정해서 설치 진행
```
pip install SpeechRecognition==3.10.1
```


#### 05. pyaudio 라이브러리 설치
 * 오디오 데이터를 다루고 처리하기 위한 라이브러리로 오디오 입력(마이크)과 출력(스피커)을 다루는 데 사용되며, 다양한 오디오 응용 프로그램을 개발하는 데 도움

 * 최신 버전 설치 진행
```
pip install pyaudio
```

 * 버전을 지정해서 설치 진행
```
pip install pyaudio==0.2.14
``` 

#### 06. pydub 모듈 설치하기 
 * 오디오 파일 처리 및 변환
  
 * 최신 버전 설치 진행
```
pip install pydub
```

 * 버전을 지정해서 설치 진행
```
pip install pydub==0.25.1
``` 

#### 07. gtts 모듈 설치하기 
 * Google Text-to-Speech의 Python 래퍼로, 텍스트를 음성으로 변환하는 데 사용
 * 최신 버전 설치 진행
```
pip install gtts
```

 * 버전을 지정해서 설치 진행
```
pip install gtts==2.4.0
```
