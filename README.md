# StegoCore

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Security Tool](https://img.shields.io/badge/type-steganography--tool-red)
![Platform](https://img.shields.io/badge/platform-cross--platform-lightgrey)
![Status](https://img.shields.io/badge/status-active-success)

Python steganography framework designed to **hide and extract data inside images** using the **LSB (Least Significant Bit)** technique.

This project is part of a **technical cybersecurity portfolio focused on steganography, data hiding techniques, and security tool development**.

---

# What does StegoCore do?

The application allows:

- Hide **text messages** inside images
- Extract **hidden messages**
- Hide **entire files** inside images
- Extract **hidden files**
- Display **progress bars for large payloads**
- Use a **modular CLI interface**

The goal of this project is to demonstrate **real-world steganography techniques applied to information security**.

---

# Project Architecture

The project is structured modularly to separate **steganography logic from the user interface**.

StegoCore/
│
├── core/
│ ├── encoder.py
│ ├── decoder.py
│ ├── file_encoder.py
│ ├── file_decoder.py
│ └── progress.py
│
├── ui/
│ ├── menu.py
│ ├── ui_central.py
│ ├── extractor.py
│ └── image_selector.py
│
├── images/
├── output/
├── screenshots/
│
├── main.py
└── requirements.txt


### core/

Contains the **steganography engine**.

- `encoder.py` → hide messages
- `decoder.py` → extract messages
- `file_encoder.py` → hide files
- `file_decoder.py` → extract files
- `progress.py` → progress bar system

### ui/

Handles the **console interface**.

- `menu.py` → main menu
- `ui_central.py` → banner / interface
- `extractor.py` → extraction flow
- `image_selector.py` → image selection

### images/

Test images used as containers.

### output/

Generated images containing hidden payloads.

---

# Steganography Technique

StegoCore uses **LSB (Least Significant Bit)** steganography.

This technique modifies the **least significant bits of pixel values** to hide information while keeping the visual appearance of the image unchanged.

---

# Supported File Types

Because the tool works at **binary level**, it can hide almost any file type:

txt        mp4
pdf        zip
docx       rar
xlsx       7z
csv        exe
png        bin
bmp        py
gif        js
mp3        html
wav


As long as the **payload size fits within the image capacity**.

---

# Important Note about JPG / JPEG

JPEG images **must NOT be used as containers**.

Reason:

- JPG uses **lossy compression**
- Compression modifies least significant bits
- Hidden data becomes corrupted

For this reason **PNG images are recommended**.

---

# Installation

## Clone the repository

git clone https://github.com/Diblock/StegoCore.git

cd StegoCore

## Install dependencies

pip install -r requirements.txt

## Run the application

python main.py


Security Disclaimer

This tool is intended for educational and research purposes only.

Do not use this software to hide malicious content or perform illegal activities.

Author

Francisco Javier

Cybersecurity • Software Development • Steganography Research

GitHub:
https://github.com/Diblock
