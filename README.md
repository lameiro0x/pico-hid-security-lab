# Raspberry Pi Pico HID Payload Lab

This repository contains example payloads used to study **USB HID-based attack techniques**
in a **controlled and educational context**. These payloads are intended exclusively for
use in **isolated lab environments** or on **systems owned by the user**.

The project is based on the concept of emulating a **Human Interface Device (HID)** (e.g. a keyboard)
using a **Raspberry Pi Pico**, allowing scripted keystroke injection for learning, testing,
and security awareness purposes.

---

## Purpose of the Repository

The main goals of this repository are:

- To understand how **USB HID devices** work at a low level.
- To study **keystroke injection techniques** in a safe, ethical, and controlled environment.
- To experiment with payload execution logic on microcontrollers.
- To gain hands-on experience with **offensive security concepts** relevant to real-world attacks,
  while maintaining a responsible and educational approach.

This repository is intended for **cybersecurity learning**, **lab experimentation**, and
**defensive awareness**, not for real-world misuse.

---

## Important Safety Notice

⚠️ **Use responsibly**

- Do **NOT** connect this device to systems you do not own or have explicit permission to test.
- Do **NOT** deploy payloads in production environments.
- All testing should be performed in **isolated virtual machines** or **owned hardware**.

---

## Setup Mode (Important)

To modify payloads or configuration files, the Raspberry Pi Pico must be started in **setup mode**:

1. Connect **pin 1 (GP0)** to **pin 3 (GND)**.
2. Plug the Pico into the computer while the pins are connected.
3. The device will boot in setup/configuration mode, allowing file access.

---

## Payload Modification Workflow

If the payload is **not malicious** (as is currently the case):

1. Connect the Pico and allow the payload to execute.
2. Rename the `.dd` payload file to `.txt`.
3. Edit the payload content as needed.
4. Rename the file back to `.dd`.
5. Copy it back to the Pico filesystem.

This workflow allows safe iteration and testing of payload logic.

Detailed instructions for modifying payloads are provided in  
[`Instalar/change_payload.txt`](Instalar/change_payload.txt), including how to boot the
device in setup mode and safely edit `.dd` payload files.

---

## Repository Structure


```bash
.
└── Instalar
├── INSTALL.txt
├── adafruit-circuitpython-raspberry_pi_pico-en_US-8.0.0.uf2
├── adafruit-circuitpython-raspberry_pi_pico_w-en_US-8.0.0.uf2
├── boot.py
├── code.py
├── duckyinpython.py
├── lib/
│   └── (Adafruit HID and CircuitPython libraries)
├── payload.dd
├── payload2.dd
├── payload3.dd
├── payload4.dd
├── pico-ducky-v2.0-win_es.zip
├── secrets.py
├── webapp.py
└── wsgiserver.py
```

---

## Credits

This project is based on and inspired by:

- https://github.com/dbisu/pico-ducky

All credit for the original concept and tooling goes to the original author.
This repository adapts and extends the idea for **educational and learning purposes**.

---

## Disclaimer

This repository is provided **for educational purposes only**.
The author is not responsible for any misuse of the information or tools contained herein.
