# 🚀 NextUp Launcher
![Kotlin](https://img.shields.io/badge/Kotlin-1.9-blue)
![Jetpack Compose](https://img.shields.io/badge/Jetpack%20Compose-UI%20Toolkit-orange)
![License: MIT](https://img.shields.io/badge/License-MIT-green)
NextUp Launcher is a fully custom Android launcher built with Jetpack Compose and Kotlin. It combines a modern homescreen experience with advanced drag-and-drop features, folder management, and a right-swipe content feed powered by Reddit. Designed with clean architecture, responsiveness, and modularity at its core.


---

## 📱 Check Out the Website

👉 [View the NextUp Launcher Demo Website](https://glacira-ltd.com/nextup-presentation.html)


## ✨ Features

- 🧲 **Real-Time Drag & Drop** — Smooth icon repositioning with dynamic grid snapping, hover detection, and cross-page movement.
- 🗃️ **Folders** — Create, rename, and organize apps into folders inline, with intuitive merging and removal behavior
- 🔍 **Expandable App Drawer** — Swipe-up gesture to reveal a full app list with search and drag support
- 🎥 **Content Feed** — Right-swipe reveals a customizable feed (currently Reddit videos with ExoPlayer)  
- 🎨 **Jetpack Compose UI** — Built fully in Compose with a modern Material3 theme  
- 🔁 **Persistent Layout** — App placements saved with DataStore + Protobuf  
- 📦 **MVVM + Event-Driven Architecture** — Clean separation of concerns for state and effect handling

- ## 📊 Analytics & Monetization

- Firebase Analytics: Tracks user engagement, dwell time, and feature usage
- AdMob integration: (Planned/In Progress) – Pre-roll video ads on content feed

- ## 💡 Engineering Highlights

- Custom gesture detectors using raw `pointerInput` and `VelocityTracker`
- Dynamic page creation and removal based on drag context
- Full-screen ExoPlayer with custom IMA ad integration and rotation handling
- Centralized `DragManager` and `MeasurementManager` to coordinate layout and input state
- Scalable backend with Cloud Functions + Firestore + Cloud Run (`ffmpeg`)
- Clean architecture with MVVM, event-driven reducers, and sealed intent/effect state modeling

### 🎥 TikTok-Style Vertical Feed

- Fully custom vertical video feed powered by Reddit and ExoPlayer
- Single active player model with dynamic start/stop logic tied to scroll position
- Fullscreen transitions and aspect-ratio-aware resize behavior
- Serverless backend (Cloud Functions + Firestore) fetches and stores Reddit videos
- Thumbnail generation via `ffmpeg` on Cloud Run for improved load performance
- Pre-roll ad support (Google IMA SDK) and Firebase Analytics for engagement tracking


---

## 📸 Previews

<p float="left">
  <img src="screenshots/homescreen.png" width="200"/>
  <img src="screenshots/feed.png" width="200"/>
</p>

---
## 🎬 Demos

### Drag & Drop
![App Drawer Demo](screenshots/app_drawer_preview.gif)

### Folder Creation
![Drag and Homescreen Demo](screenshots/drag_and_homescreen_preview.gif)

### Video Feed Navigation
![Feed And Video Demo](screenshots/feed_and_video_preview.gif)

---
## 🧰 Tech Stack

- **Language**: Kotlin (100%)  
- **UI**: Jetpack Compose + Material 3  
- **DI**: Hilt  
- **State**: StateFlow / SharedFlow  
- **Persistence**: DataStore (Protobuf)  
- **Media**: ExoPlayer  
- **Backend**: Firebase (Firestore + Functions)  
- **Architecture**: MVVM + Event-Driven State Management  
- **Build**: Gradle + KSP

---

## 🧪 Highlights of Implementation

### 🔁 Drag-and-Drop Architecture
- Uses `Modifier.pointerInput` with `detectDragGesturesAfterLongPress`
- Position tracking via `Offset` + dynamic highlight overlays
- Real-time folder merging and removal with visual cues

### 📁 Folder System
- Drop an icon onto another to create a folder
- Inline folder renaming
- App repositioning with duplicate prevention logic

### 🎬 Reddit Video Feed
- Cloud Function fetches top Reddit videos to Firestore
- Thumbnails generated via `ffmpeg` on Cloud Run
- Videos displayed using `ExoPlayer` in Compose UI

---

## 🚧 Roadmap

- [ ] Custom themes and icon packs  
- [ ] Additional content sources (YouTube, TikTok, etc.)  
- [ ] Long-press actions & widgets  
- [ ] Backup/export layouts  
- [ ] Animations polish (spring-based drag easing)

---

## 👨‍💻 Author

**Alec Dipasquale**  
Android Developer • 2+ years experience  
Open to roles or collaboration — [LinkedIn](https://www.linkedin.com/in/alecdipasquale/)
