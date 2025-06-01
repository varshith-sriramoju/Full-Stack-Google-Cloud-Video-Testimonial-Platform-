# Full-Stack Video Testimonial Recorder

A full-stack web application that allows users to record video testimonials directly from their browser and upload them securely to a specified Google Drive folder using a Node.js backend and the Google Drive API.

---

## Features

- Record video & audio directly in the browser
- Stream live camera feed via WebRTC
- Upload recorded video to backend via `multipart/form-data`
- Store videos directly in Google Drive using a service account
- Responsive and clean UI with HTML, CSS, and JavaScript

---

## Tech Stack

### Frontend:
- HTML5
- CSS3 (Flexbox, Responsive Design)
- JavaScript (MediaRecorder API, getUserMedia)

### Backend:
- Node.js
- Express.js
- Multer (for file upload handling)
- Google Drive API (via `googleapis` npm package)
- CORS

---

## Folder Structure
├── app.js # Frontend JS logic

├── index.html # UI structure

├── styles.css # UI styling

├── server.js # Node.js + Express backend

├── uploads/ # Temporary video file storage

├── video-testimonial-record-*.json # Google service account credentials

├──ProjectWorkFlow.pdf # Workflow and architecture

├──node_modules,package-lock.json & package.json # node.js Dependencies

## node.js terminal commands
npm init -y   #initalize the node modules

npm install express multer cors googleapis google-auth-library #install all neccesary depemdencies

node server.js # run server

## How It Works
1.User opens the app in a browser and grants camera/microphone access

2.User records a testimonial video

3.Upon stopping, the video is uploaded to the backend

4.The backend saves it temporarily and uploads it to Google Drive

5.The temporary file is deleted from the server