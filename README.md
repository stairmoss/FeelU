# FeelU
A stress relief robot assistant
# 🤖 Feel U – AI-Powered Stress-Relief Robot

**Feel U** is an integrated hardware-software system that detects human stress through EEG and emotion sensing, interacts empathetically, and provides personalized calming responses.  
Built around the **Raspberry Pi 5**, the robot combines bio-signal analysis, computer vision, and a mobile companion app to promote mental wellness.

---Feel U is an AI-powered robot that understands human emotions and helps people reduce stress.
It moves around the room, detects when someone is feeling tense using a brain-sensing EEG headset and emotion camera, and then gives calming responses — like soft voice guidance, relaxing lights, or soothing music.

It’s like having a personal emotional assistant that can see, feel, and care about your mental health.

🧩 Technical Explanation (for project reports & presentations):

The Feel U Robot is an integrated AI + Robotics + Bio-sensing system designed to monitor and manage stress levels in real-time.

It uses:

EEG BioAmp sensors to measure electrical activity in the brain.

Facial emotion recognition (via Pi Camera) to analyze user mood visually.

Raspberry Pi 5 for local data processing and AI inference.

Mobile App (Firebase/Flutter) for live stress monitoring and suggestions.

Voice + Light output to provide emotional feedback and therapy.

⚙️ Core Functions
Function	Description
🧠 Stress Detection	EEG headset measures alpha, beta, theta waves → calculates stress score.
😊 Emotion Analysis	Pi camera + MediaPipe detect facial emotion (happy, sad, tired, angry).
🤖 Robot Movement	Moves around, greets user, and approaches them when stress is detected.
🎧 Therapy Response	Plays relaxing sounds, guides breathing, and changes LED color (mood light).
📱 App Dashboard	Displays stress level, emotion trend, and AI suggestions in real-time.
☁️ Cloud Sync	Logs stress data and sessions to Firebase/Supabase for analysis.
🔁 How It Works (Step-by-Step)

The robot patrols the room and detects the user using PIR & camera sensors.

It asks the user to wear the EEG headset.

EEG signals are read via Arduino + BioAmp and sent to Raspberry Pi 5.

Pi 5 processes data using an AI model to estimate stress % and emotion type.

The robot then reacts based on the stress level:

< 30% → Green light, cheerful tone.

30–60% → Blue light, gentle relaxation voice.

60% → Red light, breathing exercise & calm music.

The app shows real-time data, history graphs, and suggestions.

The robot logs data and returns to charging dock when idle.

💡 In Short:

“Feel U” senses how you feel — through your brainwaves, face, and actions — and responds like a caring companion to calm your mind.

🧾 Example Use Case:

A student studying for exams feels stressed.

The robot detects high stress from EEG signals and facial tension.

It moves near the student and softly says:
“You seem tense. Let’s take a short break — breathe with me for 2 minutes.”

The lights turn soft blue, music plays, and stress levels drop — all shown in the app.

## 🧩 System Overview
EEG BioAmp → Arduino Nano → Raspberry Pi 5 → Cloud/App
│ │
Sensors & Motors Camera + AI Model



- **Input:** EEG brain-wave data + emotion recognition + environment sensors  
- **Processing:** On-device AI (TensorFlow Lite / MediaPipe) on Pi 5  
- **Output:** Movement, light color, speech, and app notifications  
- **Connectivity:** Wi-Fi 6 / Bluetooth 5.0 / MQTT or Firebase Realtime DB  

---

## ⚙️ Hardware Components

| Module | Model / Example | Function |
|---------|-----------------|-----------|
| **Main SBC** | Raspberry Pi 5 (8 GB) | AI processing, communication |
| **EEG Interface** | BioAmp EXG Pill + Arduino Nano | Brain-wave acquisition |
| **Motor Driver** | L298N / TB6612FNG | Wheel control |
| **Motors & Chassis** | 12 V DC x4 + Caster | Robot movement |
| **Sensors** | PIR + Ultrasonic + DHT11 | Presence & environment detection |
| **Camera** | Raspberry Pi Camera Module 3 | Facial emotion analysis |
| **Audio System** | ReSpeaker 2-Mic Hat + Mini Speaker | Voice interaction |
| **Lighting** | NeoPixel RGB Ring | Mood indicator |
| **Power** | 12 V Li-ion Battery + Buck Converter (5 V) | Energy supply |
| **App Backend** | Firebase / Supabase | Data sync & user storage |

---

## 🧠 EEG BioAmp Flow

1. Electrodes placed on FP1/FP2 (frontal lobe).  
2. BioAmp Kit → Arduino filters & amplifies signals.  
3. Serial transfer to Pi 5.  
4. Python script computes α β θ δ bands → Stress Score (%).  
5. Result sent to mobile app and robot AI module.

---

## 🚀 Robot Operation Cycle

| Phase | Action |
|-------|--------|
| **Idle/Patrol** | Moves slowly, scans room, detects user presence. |
| **Engagement** | Greets user, requests EEG headset. |
| **Measurement** | Reads EEG + emotion, calculates stress index. |
| **Response** | Adjusts LED color & plays relaxing audio. |
| **App Sync** | Uploads data → Firebase for dashboard view. |
| **Recharge** | Returns to dock when battery < 20%. |

---

## 📲 Mobile App Features

- Real-time Stress Dashboard (EEG + Emotion Graph)  
- Voice Assistant for relaxation guidance  
- Historical Data and Trends  
- Robot Control Panel (Movement / Light Mode)  
- Notifications for High Stress Events  

---

## 🧰 Software Stack

| Layer | Tools |
|-------|-------|
| OS | Raspberry Pi OS (Bookworm 64-bit) |
| Programming | Python 3.11 / C++ (Arduino) |
| AI | TensorFlow Lite / MediaPipe / OpenCV |
| Messaging | MQTT / Firebase Realtime DB |
| App | Flutter / React Native |
| Cloud Storage | Supabase / Firebase |
| Optional LLM | Ollama / Gemini Nano for chat responses |

---

## 🌈 Stress Level Indicators

| Stress Score | Robot Reaction |
|--------------|----------------|
| 0-30 % | Green light – calm state |
| 31-60 % | Blue light – moderate stress + music cue |
| 61-80 % | Red light – breathing guide + voice therapy |
| 81-100 % | Robot approaches user + soothing speech |

---

## 🔬 Data Processing Pipeline
1. EEG Signal Acquisition  
2. Digital Filtering & Feature Extraction  
3. Stress Level Inference (ML Model)  
4. Sensor Fusion with Facial Emotion Data  
5. Real-time Dashboard Display + Therapeutic Feedback  

---

## 💡 Future Upgrades
- Full ROS 2 navigation (SLAM)  
- Personalized ML model per user  
- Doctor dashboard for remote monitoring  
- Integration with smart home IoT devices  
- Offline voice assistant (Llama 3 via Ollama)  

---

## 🔋 Power Management
- Auto dock charging station  
- Battery status telemetry to app  
- Low-power mode during idle  

---

## 📦 Estimated Cost (₹ INR)

| Item | Range |
|------|--------|
| Raspberry Pi 5 (8 GB) | 7 500 – 8 000 |
| BioAmp EEG Kit + Arduino | 3 000 |
| Camera Module 3 | 1 800 |
| Motors + Driver + Chassis | 1 200 |
| Sensors Pack | 600 |
| Power System | 1 000 |
| Audio Modules + LED | 800 |
| **Total** | **≈ 16 000 – 18 000 INR** |

---

## 🧭 Repository Structure
feel-u/
├── hardware/
│ ├── schematics/
│ ├── pcb/
│ └── wiring_diagram.png
├── firmware/
│ ├── arduino_eeg/
│ └── motor_control/
├── raspberry/
│ ├── eeg_reader.py
│ ├── stress_ai_model.tflite
│ └── mqtt_publisher.py
├── app/
│ └── flutter_source/
├── docs/
│ └── README.md ← you are here

