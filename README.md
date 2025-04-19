# Reppy

## Table of Contents

1. [Overview](#Overview)  
2. [Product Spec](#Product-spec)  
3. [Wireframes](#Wireframes)  
4. [Schema](#Schema)  

---

## Overview

### Description

Reppy is a visually-driven mobile fitness app that helps users track workouts, measure heart rate using just their phone's flashlight, and stay connected with coaching updates. Designed to be functional, fast, and visually engaging, Reppy empowers users to stay consistent through an organized dashboard, guided workouts, and real-time heart rate detection.

### App Evaluation

- **Category:** Health & Fitness  
- **Mobile:** Yes – built specifically for mobile  
- **Story:** Users can follow their training regimen, check their heart rate using the camera, and stay on track with visual stats and updates from their coach.  
- **Market:** Designed for beginner-to-intermediate users who want a no-wearable-required tracking app.  
- **Habit:** Encourages quick daily check-ins for workouts, updates, and motivation.  
- **Scope:** Focused on core features that offer strong user value with a clean UI and efficient dev timeline.

---

## Product Spec

### 1. User Stories

**Required Must-have Stories**  
* User can view a training regimen with exercise name, sets, reps, and rest  
* User can measure their heart rate using the phone flashlight  
* User can navigate between screens using a bottom navigation bar  
* User can view upcoming workouts and a coach message on the home screen  

**Optional Nice-to-have Stories**  
* User can mark exercises as complete using checkboxes  
* User can start a guided workout session with timers  
* User can view and send messages in a static trainer chat  
* User can view demo video thumbnails under exercises  
* User can view timestamps on chat messages  
* User sees animated pulse effect during heart rate scan  

---

### 2. Screen Archetypes

- [ ] **Home Dashboard**  
  * View personalized greeting  
  * See workout streak, weekly goal, and earned points  
  * View today's workout  
  * See upcoming workouts (time, type, duration)  
  * Read static coach update  
  * Navigate via bottom tab bar  

- [ ] **Training Regimen**  
  * View assigned exercises with sets, reps, rest  
  * [Optional] Check off exercises  
  * Tap “Start Workout”  

- [ ] **Heart Rate Detection**  
  * Instructions for placing finger on flashlight  
  * Begin scan, see animated pulse  
  * Display BPM  

- [ ] **Guided Workout**  
  * Show current exercise, set count  
  * Rest timer or rep counter  
  * “Next” or “Complete Set”  

- [ ] **Trainer Chat (Static)**  
  * Read 1–2 hardcoded messages  
  * Optional input bar for reply  

---

### 3. Navigation

**Tab Navigation** (Tab to Screen)

* 🏠 Home → Dashboard  
* ❤️ Heart → Heart Rate Detection  
* 🏋️ Workout → Guided Workout / Regimen  
* 💬 Chat → Trainer Chat  

**Flow Navigation** (Screen to Screen)

- [ ] Home → Workout Regimen  
  * Tap “Today's Workout”  
- [ ] Workout Regimen → Guided Workout  
  * Tap “Start Workout”  
- [ ] Home → Trainer Chat  
  * [Optional] Tap on coach message  

---

## Wireframes

[Add picture of your hand sketched wireframes in this section]  
<img src="YOUR_WIREFRAME_IMAGE_URL" width=600>

### [BONUS] Digital Wireframes & Mockups  
- Designed in Figma using modern dark UI and orange highlight accents  

### [BONUS] Interactive Prototype  
- [Link your Figma prototype if created]

---

## Schema 

_To be completed in Unit 9_

### Models  
*Workout, User, TrainerMessage*

| Model | Property | Type     | Description                      |
|-------|----------|----------|----------------------------------|
| Workout | name | String | Name of the workout (e.g. “Pushups”) |
| Workout | sets | Number | Number of sets |
| Workout | reps | Number | Number of reps |
| Workout | rest | Number | Rest time in seconds |
| TrainerMessage | sender | String | Trainer or User |
| TrainerMessage | content | String | Message text |
| TrainerMessage | timestamp | Date | Message time |

---

### Networking

- **Home Dashboard**
  - [Optional] GET: Fetch today's streak, goals, and coach message  

- **Training Regimen Screen**
  - GET: Fetch assigned exercises  
  - [Optional] POST: Mark exercise as complete  

- **Heart Rate**
  - Local flashlight & camera – no network  

- **Trainer Chat**
  - [Optional] GET: Fetch trainer messages  
