# Audio Transcription Application

## Project Overview

Audio Transcription Application is a full-stack web application built using Spring Boot, Spring AI, OpenAI Whisper API, and React.js.

The application allows users to upload audio files through a React-based user interface. The uploaded audio is sent to the Spring Boot backend, where OpenAI Whisper converts speech into text. The transcribed text is then returned to the frontend and displayed to the user.

---

## Features

* Upload audio files
* Convert speech to text
* OpenAI Whisper integration
* Spring AI integration
* REST API communication
* Responsive user interface
* Real-time transcription results

---

## Tech Stack

### Backend

* Java
* Spring Boot
* Spring AI
* OpenAI Whisper API
* Maven
* REST APIs
* CORS Configuration

### Frontend

* React.js
* Vite
* Axios
* HTML5
* CSS3
* JavaScript (ES6)

---

## Project Architecture

Frontend (React.js)
│
▼
REST API Request
│
▼
Backend (Spring Boot)
│
▼
Spring AI
│
▼
OpenAI Whisper API
│
▼
Transcribed Text
│
▼
Frontend UI

---

## Application Flow

1. User selects an audio file from the frontend.
2. React sends the file to the Spring Boot backend using Axios.
3. Backend receives the file through a REST API endpoint.
4. Spring AI communicates with OpenAI Whisper API.
5. Whisper converts speech into text.
6. Backend receives the transcription result.
7. The result is returned to the frontend.
8. React displays the transcribed text to the user.

---

## API Endpoint

### Transcribe Audio

POST /api/transcribe

Request Type:
multipart/form-data

Request Parameter:

file : Audio File

Response:

Plain Text Transcription

Example:

POST http://localhost:8083/api/transcribe

---

## Project Structure

audio-transcribe
│
├── src
│   ├── main
│   │   ├── java
│   │   └── resources
│   │
│   └── test
│
├── audio-transcribe-frontend
│   ├── public
│   ├── src
│   └── package.json
│
├── pom.xml
└── README.md

---

## Local Development Setup

### Backend Setup

Clone the repository:

git clone https://github.com/mohdsaif84/audio-transcribe.git

Move to project directory:

cd audio-transcribe

Configure OpenAI API Key:

spring.ai.openai.api-key=${OPENAI_API_KEY}

Run Spring Boot Application:

mvn spring-boot:run

Backend runs on:

http://localhost:8083

---

### Frontend Setup

Move to frontend directory:

cd audio-transcribe-frontend

Install dependencies:

npm install

Run React Application:

npm run dev

Frontend runs on:

http://localhost:5173

---

## Configuration

application.properties

spring.application.name=audio-transcribe
spring.ai.openai.api-key=${OPENAI_API_KEY}
spring.ai.openai.audio.transcription.base-url=https://api.openai.com
spring.ai.openai.audio.transcription.options.model=whisper-1
spring.ai.openai.audio.transcription.options.response-format=json
server.port=8083

---

# Future Enhancements

* Store transcription history
* User authentication and authorization
* Download transcription as PDF or TXT
* Multi-language transcription support
* Cloud deployment
* Audio transcription analytics dashboard

<img width="1290" height="720" alt="Image" src="https://github.com/user-attachments/assets/c4c4dc39-2784-4469-9957-66ef5cd7f1c5" />

---

## Author

Mohd Saif Nawaj

Java Backend Developer

GitHub:
https://github.com/mohdsaif84
