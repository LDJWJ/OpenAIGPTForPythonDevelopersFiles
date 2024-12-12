### 14. 인공지능 기반 Alexa 만들기

### 개발 환경
 * OS : Window 11
 * GPU/CPU : CPU
 * Python Version : 3.9.5 (default, May 18 2021, 14:42:02) [MSC v.1916 64 bit (AMD64)]
 * 아나콘다 Version : 22.9.0
 * 라이브러리 버전
```
torch                     2.0.1
speechrecognition         3.10.0
spacy                     3.6.1
pydub                     0.25.1
openai                    0.27.8
openai-whisper            20230314
gtts                      2.3.2
```
 
### 작업 절차

#### 01. 가상환경 만들기 
 * 내용 : 가상환경을 만들고, 설치를 위해 권한 문제로 오류가 발생할 수 있습니다. Command Prompt를 관리자 권한으로 실행해 주세요.
 
 * 가상환경 만들기 - 사전 아나콘다 설치 필수
```
conda create --name myenvAI
```
 * myenvAI는 가상환경 이름으로 사용자 지정이 가능합니다.
 
#### 02. 라이브러리 설치 
 * 일반적으로 버전을 지정하여 설치하지 않아도 되지만, 호환이 안되는 패키지 들로 인해 오류가 발생할 수 있어, 실행된 버전을 지정하여 설치 수행.
```
python.exe -m pip install --upgrade pip
pip install openai==0.27.8
pip install click==8.1.3
pip install openai-whisper==20230314
```

#### 03. spaCy 모델 설치 및 다운로드
 * spaCy는 자연어 처리(Natural Language Processing, NLP)를 위한 파이썬 라이브러리 중 하나로, 텍스트 데이터를 처리하고 분석하는 데 사용됩니다. spaCy는 빠르고 정확한 토큰화(Tokenization), 형태소 분석(Morphological Analysis), 개체 인식(Named Entity Recognition), 구문 분석(Syntactic Parsing) 등 다양한 NLP 작업을 지원합니다.
```
pip install spacy==3.6.1
python -m spacy download en_core_web_md
```
  
#### 04. speech_recognition 라이브러리 설치
 * 파이썬에서 음성 인식을 수행하기 위한 라이브러리입니다. 이 라이브러리는 다양한 음성 인식 엔진과 상호 작용하고, 오디오 데이터를 텍스트로 변환하는 기능을 제공합니다.
```
pip install SpeechRecognition==3.10.0
```
  
#### 05. pyaudio 라이브러리 설치
 * 오디오 데이터를 다루고 처리하기 위한 라이브러리로 오디오 입력(마이크)과 출력(스피커)을 다루는 데 사용되며, 다양한 오디오 응용 프로그램을 개발하는 데 도움
```
pip install pyaudio==0.2.13
```
  
#### 06. pydub 모듈 설치하기 
 * 오디오 파일 처리 및 변환
```
pip install pydub==0.25.1
```
  
#### 07. gtts 모듈 설치하기 
 * Google Text-to-Speech의 Python 래퍼로, 텍스트를 음성으로 변환하는 데 사용
```
pip install gtts==2.3.2
```
  
#### 08. app.py 파일 생성
```

```

#### 07. server 폴더에 .env 파일 생성
```
API_KEY=sk-xxxx
ORG_ID=org-xxx #optional
```

#### 08. 프론트엔드 폴더에 index.js 파일 생성
* frontend 폴더에서  chatbot/client/src/router/index.js 파일을 열고 아래 코드 작성
```
import { createRouter, createWebHistory } from 'vue-router'
import HomeView from '../views/HomeView.vue'

const routes = [
    {
        path: '/',
        name: 'home',
        component: HomeView
    },
    {
        path: '/about',
        name: 'about',
        // route level code-splitting
        // this generates a separate chunk (about.[hash].js) for this route
        // which is lazy-loaded when the route is visited.
        component: () => import(/* webpackChunkName: "about" */ '../views/AboutView.vue')
    }
]

const router = createRouter({
    history: createWebHistory(process.env.BASE_URL),
    routes
})

export default router

```

#### 09. HomeView.vue 파일 생성
* client/src/views에서 HomeView.vue 파일을 만들고 아래 코드를 추가
```
<template>
    <div>
        <h2>DrugBot</h2>
        <div v-if="messages.length">
            <div v-for="message in messages" :key="message.id">
                <strong>{{ message.author }}:</strong> {{ message.text }}
            </div>
        </div>
        <form @submit.prevent="sendMessage">
            <input type="text" v-model="newMessage" placeholder="Type your message">
            <button type="submit">Send</button>
        </form>
    </div>
</template>

<script>
import axios from 'axios';

export default {
    data() {
        return {
            messages: [
                {
                    id: 1,
                    author: "AI",
                    text: "Hi, how can I help you?"
                },
            ],
            newMessage: "",
        };
    },
    methods: {
        sendMessage() {
            if (this.newMessage.trim() === "") {
                return;
            }
            this.messages.push({
                id: this.messages.length + 1,
                author: "Human",
                text: this.newMessage.trim(),
            });

            const messageText = this.newMessage.trim();
            axios.get(`http://127.0.0.1:5000/?m=${encodeURI(messageText)}`)
                .then(response => {
                    const message = {
                        id: this.messages.length + 1,
                        author: "AI",
                        text: response.data.m
                    };
                    this.messages.push(message);
                })
                .catch(error => {
                    console.error(error);
                    this.messages.push({
                        id: this.messages.length + 1,
                        author: "AI",
                        text: "I'm sorry, I don't understand.",
                    });
                });
            this.newMessage = "";
        },
    },
};
</script>
```

#### 10. AboutView.vue 파일 생성

* 리눅스 환경 - 파일 생성 후, 
```
touch client/src/views/AboutView.vue
```
* 파일 내용 작성
```
<template> 
    <div class= "about" > 
        <h1> This is an about page </h1> 
    </div> 
</template>
```

* 원도우 환경 - 아래 내용으로 파일 작성
* 경로 - client/src/views/AboutView.vue
```
<template> 
    <div class= "about" > 
        <h1> This is an about page </h1> 
    </div> 
</template>
```

#### 11. 챗봇 실행하기
* 챗봇 실행 
```
cd server
python app.py

cd client
npm run serve
```

* 브라우저를 열고 주소를 이동해 챗봇 확인해 보기
```
http://localhost:<PORT>/
```
