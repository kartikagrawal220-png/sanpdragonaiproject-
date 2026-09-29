# sanpdragonaiproject-
Snapdragon® AI Smart Vision & Productivity Assistant
An all-in-one, privacy-focused, on-device AI workspace designed and optimized for Snapdragon-powered PCs (Copilot+ PCs with Qualcomm Hexagon NPU).
This application leverages Qualcomm's NPU acceleration via the Qualcomm AI Hub and ONNX Runtime (QNN Execution Provider) to process documents, audio streams, and screen context locally with zero cloud latency and minimal power consumption.
🚀 Key Features
 * 📄 On-Device Document Summarizer: Local processing of PDFs and markdown files using quantized LLMs (Llama 3 / Phi-3) running directly on the Hexagon NPU.
 * 🎙️ Offline Audio Transcription: Real-time meeting and speech notes generation using Qualcomm AI Hub's optimized Whisper model.
 * 🖼️ Smart Screen & Vision Assistant: Live contextual support powered by lightweight vision models optimized for ARM64 architecture.
 * 🔋 Battery Efficient Acceleration: Offloads computational work from the CPU/GPU to the dedicated NPU for extended laptop battery life.
🛠️ Tech Stack & Architecture
 * Target OS: Windows 11 on Snapdragon (ARM64)
 * Acceleration SDK: Qualcomm Neural Processing SDK / ONNX Runtime (QNN Execution Provider)
 * Model Hub: Qualcomm AI Hub
 * Frontend / Interface: React / Electron (ARM64 Build)
 * Quantization Format: INT8 / FP16 optimized for Hexagon NPU
🏛️ System Pipeline
[ User Input / Files / Audio Stream ]
                 │
                 ▼
     [ Native ARM64 Host UI ]
                 │
                 ▼
  [ ONNX Runtime + QNN Execution Provider ]
                 │
                 ▼
    [ Snapdragon Hexagon NPU ] ──► [ Instant Local Output ]

⚙️ Getting Started
Prerequisites
 * Windows 11 PC (Qualcomm Snapdragon X Series or compatible Snapdragon processor).
 * Qualcomm Neural Processing SDK / QNN Runtime installed.
 * Node.js (v18+) and Python 3.10+ (ARM64 native builds recommended).
Installation & Setup
 * Clone the repository:
   git clone https://github.com/your-username/snapdragon-ai-assistant.git
cd snapdragon-ai-assistant

 * Install Dependencies:
   npm install

 * Download Model Artifacts from Qualcomm AI Hub:
   Follow the Qualcomm AI Hub instructions to export models for ONNX Runtime (QNN):
   python -m pip install qai-hub
qai-hub configure

 * Run the Application:
   npm start

📊 Qualcomm AI Hub Integration
This repository utilizes models compiled and optimized directly from Qualcomm AI Hub:
 * Text Models: Llama-3-8B-Instruct (Quantized INT8)
 * Audio Models: Whisper-Base
 * Vision Models: MobileNetV4 / Segment Anything
📄 License
This project is submitted under the Snapdragon® AI Lab Build & Present Challenge. MIT License.
