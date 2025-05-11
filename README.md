# Remote PS2 Control with PS4 Controller (Without Streaming)

This repository provides a step-by-step guide for setting up remote control of a PlayStation 2 (PS2) located in one country using a PS4 controller connected to a laptop in another country. The setup involves:
- Relaying PS4 controller inputs over the internet to the PS2.
- Using a hardware and software relay system to enable remote control.

---

## Features
- Use a modern PS4 controller to control a PS2 remotely.
- Open-source tools and hardware adapters for affordable implementation.

---

## Prerequisites

### Hardware:
- **PlayStation 2 console** (PS2 Fat or Slim).
- **8BitDo Retro Receiver** (for connecting the PS4 controller to the PS2).
- **Computer in America** (to act as the server for relaying inputs).
- **Laptop in Japan** (to send controller inputs).

### Software:
- **GIMX**: For relaying controller inputs over the network.
- **Parsec** or **Moonlight**: For low-latency input relay (optional).
- **Dynamic DNS (DDNS)**: To provide a fixed address for the server.

### Network:
- Stable internet connections on both ends.
- Ability to configure **port forwarding** on the American router.

---

## Repository Contents
This repository includes:
- `setup/`: Configuration files for GIMX.
- `scripts/`: Scripts for automating input relay.
- `docs/`: Step-by-step guides and troubleshooting tips.

---

## How to Use This Repository

### 1. Set Up the PS2
1. **Connect the Hardware**:
   - Plug the **8BitDo Retro Receiver** into the PS2 controller port.
2. **Test the Controller Setup**:
   - Pair the PS4 controller with the Retro Receiver using Bluetooth (as described in the 8BitDo manual).
   - Ensure the PS2 responds to the PS4 controller inputs locally.

---

### 2. Configure the Computer in America
1. **Install GIMX**:
   - Download and install **GIMX** on the computer.
   - Connect a **PS2-to-USB adapter** or use the Retro Receiver as a passthrough.
   - Configure GIMX to accept controller inputs over a network socket and relay them to the PS2.

2. **Run the GIMX Input Server**:
   - Start GIMX in server mode to listen for inputs from the laptop in Japan.
   - Ensure that the PS2 responds to the relayed inputs locally.

---

### 3. Configure the Laptop in Japan
1. **Connect the PS4 Controller**:
   - Pair the PS4 controller to the laptop via Bluetooth or USB.
2. **Send Controller Inputs**:
   - Use software like **Parsec** or **Moonlight** to connect to the American server and send controller inputs over the network.

---

### 4. Test the Remote Setup
- Use the PS4 controller on your laptop in Japan to control the PS2 in America.
- Verify that all inputs are being correctly relayed to the PS2.

---

## Troubleshooting
- **Latency Issues**: Use wired internet connections and a low-latency input relay protocol.
- **Controller Not Responding**: Ensure GIMX is running, and the Retro Receiver is paired correctly.
- **Input Relay Fails**: Check port forwarding and firewall settings on the American router.

---

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

---

## Contributing
Contributions are welcome! Please feel free to submit issues or pull requests.
