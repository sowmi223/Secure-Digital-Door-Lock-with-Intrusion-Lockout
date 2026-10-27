# Secure-Digital-Door-Lock-with-Intrusion-Lockout
Secure Digital Door Lock with Intrusion Lockout


## 📌 Project Overview

The **Secure Digital Door Lock with Intrusion Lockout** is a VLSI mini project developed using Verilog HDL. It implements password-based access control and improves security by limiting the number of incorrect password attempts.

When the maximum number of consecutive incorrect attempts is reached, the system enters a temporary lockout state and activates an alarm indication. Normal operation is restored after the lockout period expires.

The project demonstrates the application of Finite State Machines (FSMs) in digital security systems using FPGA technology.

## 🎯 Objectives

- Implement password-based access control using Verilog HDL.
- Interface a PS/2 keyboard with the FPGA for password input.
- Detect incorrect password attempts.
- Count consecutive failed attempts.
- Activate an alarm after the maximum permitted attempts.
- Implement a temporary lockout mechanism.
- Prevent password-based bypass of the lockout sequence.
- Demonstrate FSM-based digital hardware design and simulation.

## ❗ Problem Statement

Traditional password-based door-lock systems may be vulnerable to repeated unauthorized password attempts. This project addresses the problem by restricting the number of incorrect attempts and temporarily disabling access after repeated failures.

The system provides an alarm indication during lockout and restores normal operation only after the lockout period expires.

## 💡 Proposed Solution

A secure digital door-lock controller is designed using Verilog HDL and implemented for an FPGA platform.

The controller verifies the entered password, tracks failed attempts, and manages access through an FSM. After three consecutive incorrect password attempts, the controller activates the lockout and alarm indications.

The design is intended to improve access security and demonstrate hardware-based intrusion prevention.

## ⚙️ Working Principle

1. **Password Input:** The user enters a password using the PS/2 keyboard interface.
2. **Password Verification:** The controller checks the entered password.
3. **Access Granted:** If the password is correct, access is permitted.
4. **Error Detection:** If the password is incorrect, an error indication is generated.
5. **Attempt Counting:** The controller counts consecutive failed attempts.
6. **Lockout Activation:** After three consecutive incorrect attempts, the system enters lockout.
7. **Alarm Indication:** The alarm output is activated during lockout.
8. **Access Restoration:** Normal operation resumes after the lockout period expires.

## 🔄 Finite State Machine (FSM)

The controller uses the following states:

| State | Description |
|---|---|
| LOCKED | Waits for password input. |
| VERIFY | Checks the entered password. |
| ACCESS GRANTED | Permits valid access. |
| ERROR | Indicates an incorrect password. |
| ATTEMPT COUNT | Tracks failed attempts. |
| LOCKOUT | Blocks access after the attempt limit is reached. |
| RESET / UNLOCK | Restores operation after lockout expires. |

The FSM coordinates password verification, access control, failed-attempt counting, alarm activation, and lockout recovery.

## 🛠️ Hardware Requirements

- FPGA development board
- FPGA device: Cyclone II EP2C8T144C8
- PS/2 keyboard interface
- Clock and reset inputs
- Access, error, locked, and alarm indicators

**Note:** The actual availability and connection of each peripheral depend on the hardware implementation.

## 💻 Software Requirements

- **HDL:** Verilog
- **Design software:** Quartus II 13.0
- **Simulation:** Waveform Editor
- **Target device:** Cyclone II EP2C8T144C8

## 📊 Input and Output Signals

### Inputs
- `clk` – Clock signal for circuit operation.
- `password` – Password input data.
- Control and reset signals.

### Outputs
- `ACCESS` – Indicates access status.
- `ERROR` – Indicates an incorrect password condition.
- `LOCKED` – Indicates the lock status.
- `ALARM` – Indicates the alarm condition.

*The signal names are based on the project presentation; the exact Verilog port declarations should be checked against the source code.*

## 🧪 Simulation and Verification

The design uses waveform simulation to observe the controller's signal transitions and evaluate password verification and access-control behaviour.

The simulation focuses on:

- Clock signal operation.
- Password input and verification.
- Access-granted and error conditions.
- Failed-attempt counting.
- Lockout and alarm behaviour after repeated incorrect attempts.

The waveform helps analyse the expected behaviour of the digital controller.

## 🔒 Security Features

- Password-based access control.
- Consecutive failed-attempt monitoring.
- Three-attempt lockout threshold.
- Alarm indication during lockout.
- Timed restoration of normal operation.
- FSM-based access-control logic.

## 🚀 Future Enhancements

- Integrate a physical electronic door-lock mechanism.
- Add a buzzer for audible intrusion alerts.
- Include an LCD display for system status messages.
- Introduce multiple authentication methods.
- Implement mobile notifications for repeated failed attempts.
- Enhance password storage and verification security.

## 📚 Applications

- Laboratory access-control systems.
- Restricted-access rooms.
- Educational FPGA security demonstrations.
- Digital door-lock prototypes.
- Hardware-based intrusion prevention systems.

## 🏁 Conclusion

The Secure Digital Door Lock with Intrusion Lockout demonstrates password-based access control using Verilog HDL and an FSM-based architecture. By counting incorrect password attempts and activating a temporary lockout with an alarm indication after three consecutive failures, the design provides a foundation for FPGA-based digital security applications.

Waveform simulation supports the analysis of the controller's signal behaviour and its intended access-control operation.

## 👨‍💻 Project Information

- **Project Type:** VLSI Mini Project
- **Subject:** VLSI and Chip Design (EC3552)
- **Department:** Electronics and Communication Engineering
- **Institution:** University College of Engineering, Kanchipuram

### Team Members

- Anusree K
- Sowmiya S
- Yogeshwaran GP

### Mentor

Dr. K. Arunkumar

---

**Secure Access Through FPGA-Based Digital Design** 🔐
