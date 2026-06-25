# Raspberry Pi Pico 2W BadUSB

A USB Rubber Ducky–style HID injection tool built on the Raspberry Pi Pico 2W. This project emulates a USB keyboard to automate keystroke injection for security testing, penetration testing labs, and educational purposes.

![Raspberry Pi Pico 2W BadUSB](images/pico-photo.jpg)

## ⚠️ Disclaimer

This project is intended **strictly for educational purposes, authorized penetration testing, and security research** on systems you own or have explicit permission to test. Unauthorized use against systems you do not own or lack permission to test is illegal. The author assumes no liability for misuse.

## Features

- Emulates a USB HID keyboard via the Pico 2W
- Executes pre-written keystroke injection scripts (DuckyScript-style or custom)
- Wireless (2W) control option for triggering payloads
- Lightweight, low-cost (~$6 hardware), easy to reproduce

## Hardware Requirements

- Raspberry Pi Pico 2W
- Micro-USB / USB-C cable (depending on board revision)
- (Optional) Case / enclosure

## Software Requirements

- [CircuitPython](https://circuitpython.org/board/raspberry_pi_pico2_w/) or MicroPython firmware
- Thonny IDE or any serial IDE (for uploading code)

## Installation

1. Flash CircuitPython/MicroPython onto your Pico 2W.
2. Clone this repository:
```bash
   git clone https://github.com/yourusername/pico-badusb.git
```
3. Copy the contents of `src/` onto the Pico's `CIRCUITPY` drive.
4. Edit `payloads/example_payload.txt` with your desired keystroke sequence.
5. Reset the Pico — it will enumerate as a USB HID device and execute the payload.

## Usage

Plug the Pico 2W into a target machine's USB port. On boot, it will identify as a standard keyboard and execute the configured payload automatically.

## Project Photo

![Project Setup](images/pico-photo.jpg)

## Folder Structure

```
pico-badusb/
├── src/            # Main firmware/code
├── payloads/        # Example keystroke scripts
├── images/          # Project photos
└── README.md
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.
