# AISOC 2025

#  SoundSentry – Acoustic Event Detection App

A privacy-first mobile/web app that performs real-time detection of critical environmental sounds such as fire alarms, glass breaking, and dog barking — all processed entirely on-device using optimized AI models.

---

##  Team Information

**Team Name:** Sound Sentry

| Name            | Branch | Roll Number | Role                                | Email                    |
|-----------------|--------|-------------|-------------------------------------|--------------------------|
| Monaal          | IT     | UE238056    | Full Stack AI Engineer              | monaalmamen@gmail.com    |
| Sarthak Verma   | ECE    | UE235098    | Backend Engineer / ML Engineer      | iamsarthakverma@gmail.com|
| Tarun           | ECE    | UE235108    | Flutter Developer / Testing         | tarunmehrda@gmail.com    |                 
| Alok Kumar      | ECE    | UE235011    | UI/UX Designer / Embedded Systems   | alokyadav1023@gmail.com  |                     
| Abhinay Tiwari  | ECE    | UE235006    | Full Stack Developer                |abhinaytiwari542@gmail.com|                    

 **GitHub Repo:** https://github.com/Monaal5/Sound_Sentry

---

##  Problem Statement

Current sound recognition systems for safety and accessibility either:
- Rely on cloud streaming, compromising **user privacy**
- Require **expensive hardware** inaccessible to many
- Suffer from **latency** or **false positives**, reducing trust and usability

###  Critical Market Gaps

- **Assistive technologies** for the hearing-impaired depend on costly wearables or cloud-based tools with unacceptable delays.
- **Security systems** often generate false alarms due to inaccurate acoustic event detection.
- **Smart home solutions** stream continuous audio to cloud servers, raising serious **privacy concerns**.
  
These limitations create **accessibility barriers** and **security vulnerabilities**, especially in **bandwidth-constrained environments** such as rural areas, offline institutions, or homes without reliable connectivity.

###  Human-Centric Use Cases

- **Emergency Awareness:** Hearing-impaired users miss smoke alarms and sirens without visual cues.
- **Proactive Pet Management:** Pet owners receive alerts for stress barking or abnormal pet behavior.
- **Intrusion Detection:** Businesses need real-time glass-break alerts to prevent break-ins.

---

**SoundSentry** transforms passive devices into **active environmental interpreters**, bridging sensory gaps using **real-time on-device sound analysis** powered by TensorFlow Lite.  

Our solution focuses on:
-  Empowering **hearing-impaired individuals**  
-  Enhancing **smart home safety**  
-  Improving **surveillance and alerting systems**

All of this, while maintaining:
-  Sub-100ms detection latency  
-  Fully offline AI processing  
-  No cloud storage or audio transmission  
-  AES-encrypted event logs

---

## Motivation

We aim to empower users — especially the hearing-impaired and those in low-connectivity environments — through:

- **Accessibility**: Alerts for critical sounds in real-time  
- **Safety**: Reliable, low-latency sound detection  
- **Privacy**: All analysis is performed **on-device**, no cloud audio transfer  

Our approach:
- Fast sub-100ms inference
- Compact quantized DNNs
- Lightweight signal processing (MFCC + RNNoise)

---

##  Expected Outcomes

-  Fully functional cross-platform app built with **Flutter**
-  Real-time detection of **fire alarms**, **glass breaks**, **dog barks**
-  Live waveform visualization and detection logs
-  **AES-encrypted event storage** with no raw audio retention
-  Open-source codebase + offline presentation

---

##  Timeline & Milestones

| Week     | Milestone                                                                 |
|----------|---------------------------------------------------------------------------|
| Week 1   | Setup DCASE/ESC-50 datasets, audio preprocessing (MFCC) pipeline          |
| Week 2–3 | Train quantized DNN model with RNNoise-enhanced and augmented audio data  |
| Week 4   | Integrate AI model with Flutter frontend using TFLite                     |
| Week 5   | UI & alert system: waveform, haptics, SQLite logging                      |
| Week 6–7 | Optimize (battery, accuracy), test edge cases, finalize demo + pitch      |

---

##  Final Deliverables

-  Hosted working demo (to be linked)
-  GitHub repository with complete code & documentation
-  Offline presentation slides
-  Google Drive folder with final deliverables
-  Issue thread with all logs and updates

---

## Technical Highlights

### Signal Processing
- **Pre-emphasis Filter:** Boosts high frequencies
- **Framing & Windowing:** 25ms Hamming windows
- **MFCC Extraction:** Using Mel-scale log spectrograms
- **Noise Reduction:** RNNoise removes background hum/static

###  Model Architecture
- Quantized DNN with **8-bit integer weights**
- Symmetric quantization with per-channel scaling
- Training using **ESC-50 dataset + synthetic augmentation**
- **Dropout** and **L2 normalization** to prevent overfitting

###  App Features
- Real-time inference using `tflite_flutter`
- Circular 2-second audio buffer
- Custom alerts: vibration + screen flash
- Secure logging with SQLite + SQLCipher
- No raw audio stored or uploaded

---

##  System Architecture

### Mobile App (Flutter)
- `flutter_sound`: Real-time audio input
- `rnnoise-dart`: Background noise suppression
- `tflite_flutter`: Inference engine
- `vibration`, `flutter_local_notifications`: Alerts
- `sqflite`, `SQLCipher`: Secure on-device logging

### ☁ Cloud Backend (Pro Version)
- `firebase_core`, `cloud_firestore`
- OAuth login
- Optional cloud-sync for event logs
- Admin dashboard for multi-location monitoring

---

##  Real-Life Use Cases

- 👵 A deaf grandmother sees a red flash when her grandchild cries
- 🐕 A pet owner receives a notification if their dog barks while they’re away
- 🏪 A shop owner is alerted if someone breaks glass after hours
- 🏡 A smart home system integrates it with automation triggers

---

## Resources & References

-  GitHub: [SoundSentry Repository](https://github.com/Monaal5/Sound_Sentry)
- Dataset: [ESC-50 Dataset](https://github.com/karoldvl/ESC-50)

### References:
1. Davis, S. B. (1980). MFCC Derivation – IEEE Transactions on Acoustics  
2. Valin, J. M. (2018). RNNoise: Learning-Based Noise Reduction – arXiv  
3. Google TensorFlow Lite Optimization Toolkit  
4. World Health Organization – World Report on Hearing  
5. ADA.gov – Digital Accessibility Guidelines

---

##  Get Started

```bash
# Clone the repository
git clone https://github.com/Monaal5/Sound_Sentry.git
cd Sound_Sentry

# Install dependencies
flutter pub get

# Run the app (emulator or device must be connected)
flutter run



---


