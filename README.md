# Go-Back-N ARQ Protocol Simulator

A C++ simulation of the **Go-Back-N (GBN) Automatic Repeat reQuest** protocol used in reliable data transmission.  
This project demonstrates how frames are sent, acknowledged, lost, or retransmitted using a sliding-window mechanism.

---

## 📌 Features


- Full implementation of **Go-Back-N ARQ**
- User-defined:
  - Window size
  - Number of frames
- Simulates:
  - Frame sending
  - ACK / NAK
  - Frame loss
  - Sequence number corruption (20% probability)
- Displays detailed sender/receiver logs
- Random packet generation (lowercase a–z)
- Sliding window with modulo arithmetic

---

## 🧠 How the Protocol Works

### Sender
- Sends frames up to the window limit.
- Waits for ACKs.
- If one frame fails, **all frames from that point are resent**.

### Receiver
- Accepts only the frame with the correct expected sequence number.
- Sends:
  - ACK if correct
  - NAK if wrong or out-of-order

## 📁 Project_Structure:
  - file: "main.cpp"
    description: "Go-Back-N implementation"
  - file: "README.md"
    description: "Documentation"

## 🧩 Concept_Covered:
  - "Sliding Window Protocols"
  - "Reliable Data Transfer"
  - "Sequence Number Wrapping (modulo arithmetic)"
  - "ACK/NAK handling"
  - "Sender/Receiver synchronization"
  - "Error simulation"

## 🚀 Future_Improvements
  - "Selective Repeat ARQ version"
  - "Timer + timeout support"
  - "GUI visualization"
  - "Bit-level error simulation"
  - "File logging"
