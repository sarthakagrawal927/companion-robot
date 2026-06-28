# new-things — study queue

Short stubs for non-standard tech in this repo. 3–5 lines each. Fill `Why here:`
yourself after learning; never invent rationale.

> **Note:** This project is in the planning/early prototype phase. Topics below
> are anticipated from the architecture described in `PROJECT_STATUS.md` and
> `docs/protocol.md`. Update gotchas with real file:line refs once code lands.

## ESP32 firmware — motor control + sensor integration
- What: C++ firmware on ESP32 controlling wheeled base motors and reading sensors over I2C/SPI
- Why here: TBD
- Gotcha (from code): TBD — no firmware code yet; planned to use ESP-IDF or Arduino framework
- Source: https://docs.espressif.com/projects/esp-idf/

## iOS Vision framework — on-device object detection
- What: Using Apple's Vision framework for real-time object detection on the iPhone that serves as the robot's "head"
- Why here: TBD
- Gotcha (from code): TBD — planned to run Vision requests on-device; camera frame → Vision pipeline → structured response over Wi-Fi to the Mac "brain"
- Source: https://developer.apple.com/documentation/vision

## Hardware-software protocol design (ESP32 ↔ iPhone ↔ Mac)
- What: Three-device protocol where iPhone is the head (camera/mic/speaker), ESP32 is the body (motors/sensors), Mac running Pace is the brain
- Why here: TBD
- Gotcha (from code): TBD — protocol described in `docs/protocol.md`; the tricky part is latency budget across 2 Wi-Fi hops (iPhone→Mac→ESP32)
- Source: https://developer.apple.com/documentation/network

## On-device speech recognition + TTS pipeline
- What: Voice conversation flow — speech-to-text on device, LLM inference on Mac (Pace), text-to-speech back on iPhone
- Why here: TBD
- Gotcha (from code): TBD — planned to use Apple Speech framework for STT and AVSpeechSynthesizer for TTS; Pace handles LLM inference
- Source: https://developer.apple.com/documentation/speech

## Robotics — person following with computer vision
- What: Using object detection + depth estimation to follow a person around a space
- Why here: TBD
- Gotcha (from code): TBD — planned to use Vision person detection → bounding box center → motor commands; the control loop bandwidth is the hard part
- Source: https://developer.apple.com/documentation/vision/detecting_human_body_poses_in_images
