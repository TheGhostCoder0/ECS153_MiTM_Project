# Man-in-the-Middle (MiTM) Attack Demonstration for UC Davis ECS 153 Fall 2024

## Project Overview
This repository demonstrates a **Man-in-the-Middle (MiTM)** attack using Bettercap to perform ARP and DNS spoofing, as well as packet sniffing, to illustrate the security risks of unencrypted traffic. The project includes a **fake server** that the attacker can use to simulate a phishing page.

## Repository Structure
- **fake_server/**: Contains the `index.html` file for the fake website the attacker uses to redirect the target.
- **instructions.md**: Detailed instructions for setting up and executing the MiTM attack on the attacker device, using Bettercap.

## Prerequisites
- [Bettercap](https://www.bettercap.org/) (Download and install based on your operating system)
- Python 3.x (for running the fake server)

## Quick Start
### 1. Running the Fake Server
1. Open a terminal.
2. Navigate to the `fake_server` directory:
   ```bash
   cd fake_server
   ```
3. Start the Python HTTP server on port 80:
   ```bash
   sudo python3 -m http.server 80
   ```
### 2. Running the MiTM Attack
See `instructions.md` for a full guide on setting up and executing the MiTM attack with Bettercap.
