# 📹 Generate AI Viral Videos with Seedance and Upload to TikTok, YouTube & Instagram

> **Automate the entire process of ideating, generating, editing, and uploading viral ASMR-style short videos using cutting-edge AI tools.**

---

## 🚀 Overview

This **n8n agent** automates the full creative and publishing pipeline for short-form viral video content. It uses GPT-4, Wavespeed AI, Fal.ai, and Blotato to:

1. **Generate viral video ideas daily**
2. **Draft cinematic prompt-based scenes**
3. **Create AI-generated video clips**
4. **Synthesize ASMR audio**
5. **Merge clips into a final video**
6. **Upload the video across all major platforms: TikTok, Instagram, YouTube, Threads, Facebook, Twitter, Pinterest, LinkedIn, and Bluesky**

---

## 🧠 Features

- ✅ **Automated Content Ideation** (GPT-4)
- ✅ **Creative Scene Prompt Generation** (LangChain agents)
- ✅ **Macro-Cinematic Scene Scripting**
- ✅ **AI Video Generation with Wavespeed**
- ✅ **ASMR Soundtrack with Fal AI**
- ✅ **Final Stitching and Editing via FFMPEG (Fal)**
- ✅ **Metadata management via Google Sheets**
- ✅ **1-Click Upload to 10+ Social Platforms via Blotato**

---

## 🛠️ Tech Stack

| Tool         | Purpose                              |
|--------------|---------------------------------------|
| **n8n**      | Workflow Orchestration                |
| **GPT-4.1**  | Idea & Prompt Generation              |
| **LangChain**| Prompt Parsing and Agent Tools        |
| **Wavespeed AI** | AI Video Clip Generator         |
| **Fal AI**   | ASMR Sound & Video Merging            |
| **Google Sheets** | Idea Tracking and Metadata       |
| **Blotato API** | Social Media Posting Automation   |

---

## 🔄 Workflow Structure

### 1. **Daily Trigger**
- Starts the pipeline automatically each day.

### 2. **Video Idea Generation**
- Uses GPT-4 to create one original, immersive video idea.
- Follows strict formatting: Idea, Caption (w/ 12 hashtags), Environment, Sound.

### 3. **Prompt Scripting (13 Scenes)**
- Converts the idea into 13 cinematic, high-detail video prompts.
- Each scene is designed with camera terminology and visual logic.

### 4. **AI Clip Generation**
- Each scene is turned into a 10-second video using Wavespeed’s `seedance-v1-pro-t2v-480p`.

### 5. **ASMR Soundtrack Creation**
- Uses Fal's `mmaudio-v2` to synthesize clean, soothing ASMR audio based on the Sound prompt.

### 6. **Video Merging**
- All generated clips are stitched using Fal’s FFMPEG API for seamless delivery.

### 7. **Publishing**
- Final videos are uploaded via Blotato to:
  - TikTok
  - Instagram
  - YouTube
  - Threads
  - Facebook
  - Twitter
  - LinkedIn
  - Bluesky
  - Pinterest

### 8. **Status Update**
- Google Sheets is updated with `final_output` URL and `production: done` status.

---

## 📁 Google Sheets Structure

| Column Name          | Description                                  |
|----------------------|----------------------------------------------|
| `id`                 | Auto-generated row identifier                |
| `idea`               | Short, unique video idea                     |
| `caption`            | Hashtag-rich social caption                  |
| `environment_prompt` | Scene setting and description                |
| `sound_prompt`       | ASMR audio reference                         |
| `production`         | Workflow status (`for production` or `done`) |
| `final_output`       | Final video URL after merge                  |

---

## 🔑 Requirements

### ✅ External Accounts & APIs
- [ ] **OpenAI GPT-4 API key**
- [ ] **Wavespeed.ai API key**
- [ ] **Fal.ai API key**
- [ ] **Google Sheets credentials (OAuth2)**
- [ ] **Blotato API key for each social media account**

### ✅ Environment Variables / Secrets
```env
OPENAI_API_KEY=your-openai-key
WAVESPEED_API_KEY=your-wavespeed-key
FAL_API_KEY=your-fal-key
BLOTATO_API_KEY=your-blotato-key
GOOGLE_SHEETS_CREDENTIALS=path/to/credentials.json
```

---

## 🧪 Testing Instructions

1. Set up the workflow in [n8n](https://n8n.io/)
2. Input your API credentials under relevant HTTP Request nodes.
3. Link your Google Sheet and map appropriate columns.
4. Trigger the workflow manually or schedule it via the trigger node.
5. Observe video generation, audio creation, merging, and social uploads.

---

## 📌 Tags

`#AIContent` `#ShortVideos` `#ViralMarketing` `#ContentAutomation` `#ASMR` `#TikTokAI` `#Blotato` `#Wavespeed` `#FalAI`

---

## 👨‍💻 Author

**AI Automation Designer:**  
_Hassan Rauf_  
Feel free to fork, customize, or extend the pipeline!
