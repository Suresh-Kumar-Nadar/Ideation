# 🎓 AR Graduation Booth — “Where Memories Come Alive”

An **AR based interactive booth** that transforms printed graduation photos into living memories.  
When visitors scan a graduate’s photo using their phone, a **personal video message** plays right on top of the image in **Augmented Reality (AR)** — making the photo *come alive*.

---

## 🌟 Overview

**AR Graduation Booth** is a physical installation displaying graduates' printed photos arranged in a grid.  
Each photo has an **AR marker** (QR code or image marker).  
Scanning it through a **WebAR link or AR-enabled app** triggers the graduate’s **personal video message** to play directly on their printed photo.

---

## 🗂️ 1. Data Collection Phase

### 🎓 Students Submit:
- 📸 **Profile Photo:** Clear, well-lit headshot  
- 🎥 **Short Video Message:** 10–30 seconds (MP4/MOV)  
- 📝 **Metadata (optional):**
  - Full Name  
  - Department  
  - Batch / Year  
  - Personal Quote or Message

### 📦 Data Storage:
| Type | Tools |
|------|----------------|
| File Storage | AWS S3 |
| Metadata | Firebase Firestore, MongoDB Atlas |

---

## 🧱 2. Photo Grid Generation (Physical Display)


### 🖼️ Process
1. Align photos into a **grid layout** for wall or canvas display.  
2. Generate a **unique AR marker** for each student.  
3. Optionally print:
   - Student’s name & batch
   - Their corresponding QR code (For web version) 
4. Print the final layout (matte finish preferred for better tracking).

Example  :

![Alt Text](Assets/idea.png)

### 🧰 Tools
- **Canva / Photoshop** – manual grid design  
- **Python (Pillow, OpenCV)** – automated grid generation  
- **`qrcode` library (Python)** – QR code creation  

---

## 🌐 3. AR Integration

### 📱 How It Works
1. A visitor scans the **photo or QR code**.  
2. The AR app link or WebAR site opens.  
3. The system recognizes the image marker using **image tracking**.  
4. A **personalized video** plays directly over the printed photo in AR.  
5. As the camera moves, the video stays *anchored* to the image surface.

---

### 🧠 4. MindAR.js Marker Tracking — Accuracy & Stability (For Open Source) 


## 🖋️ Marker Design Best Practices

| ✅ Do’s | ❌ Don’ts |
|--------|-----------|
| Use non-repetitive patterns | Avoid flat color logos |
| Ensure high contrast and textured details | Avoid symmetry |
| Maintain ≥ 300×300 px resolution | Avoid glossy print material |
| Use faces or detailed textures | Avoid low-resolution prints |

---

## 🔧 5. Supported AR Platforms 

| Tool | Image Marker Support | Notes |
|------|----------------------|-------|
| **8thWall** | ✅ | Most robust, WebAR-ready, commercial license |
| **MindAR.js** | ✅ | Open-source, lightweight, runs in browser |
| **Unity + Vuforia** | ✅ | High stability, app-based AR |

---

## 🚀 6. Implementation Blueprint

| Phase | Description | Tools |
|-------|--------------|-------|
| **Data Collection** | Students upload photos & videos | Google Forms → Firebase |
| **Grid Generation** | Create wall collage with QR codes | Python |
| **AR Experience** | Image tracking & video overlay | 8thWall / MindAR.js / Unity|
| **Hosting** | WebAR + video hosting | AWS / Firebase  |
| **Interaction** | Scan photo → AR video playback | Mobile browser |

---

## 💻 7. Tech Stack

- **Frontend:** HTML, CSS, JavaScript  
- **AR Engine:** 8thWall or MindAR.js or Vuforia
- **Backend:** Node.js / Flask (optional for data upload)  
- **Database:** Firebase Firestore / MongoDB Atlas  
- **Storage:** AWS S3 / Firebase Storage  
- **Deployment:** Netlify / Vercel / AWS Amplify  

---

## ⚙️ 8. Project Setup (Coming Soon)

The full source code and setup instructions will be pushed shortly.  
This will include:
- 🗂️ Folder structure and file organization  
- ⚙️ Installation steps   
- 🌐 Deployment guide for WebAR hosting  / App Deploying 
- 🧩 Example JSON schema for graduate data 
 

 > ⏳ **Codebase will be pushed soon. Stay tuned for updates!**

---

## ✨ Future Enhancements

- Add 3D confetti or animation around the video  
- Include subtitles or name labels in AR  
- Admin dashboard for media moderation  
- Kiosk display with preloaded AR viewer  
- Multi-photo or faculty message integration  


---



> *“Turning every graduate’s memory into an unforgettable AR moment.”




