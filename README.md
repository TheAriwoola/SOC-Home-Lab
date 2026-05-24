# My SOC Home Lab

## Phase 1: Virtualization & Lab Topology
I have successfully initialized my core virtualization environment using Oracle VirtualBox. This lab will serve as the testing ground for simulating attacks and analyzing security telemetry.

### Running Infrastructure:
* **Ubuntu 22 Server:** Configured to host the centralized SIEM manager.
* **Windows 10 & Ubuntu Desktop:** Serving as production endpoints for log generation.
* **Kali Linux:** Configured as the adversarial attack platform.

### Current Lab Environment Status:
<img width="695" height="327" alt="VM pic" src="https://github.com/user-attachments/assets/b1ada516-5063-4d4c-b179-061cf2d54b72" />


## Phase 2: Target Hardening & Telemetry Preparation

To simulate real world attacks without interference, I began preparing the Windows 10 endpoint. This involved disabling default security controls to ensure adversarial actions are explicitly captured by telemetry agents rather than silently blocked.

### Actions Taken:
* **Disabled Windows Defender:** Used Administrative PowerShell to run `Set-MpPreference` to turn off real time monitoring, scanning network files, and block at first seen behaviors.
* **Registry Modification:** Permanently disabled anti spyware features via a registry injection (`HKLM\SOFTWARE\Policies\Microsoft\Windows Defender`).

### Endpoint Configuration:
<img width="956" height="599" alt="Win10" src="https://github.com/user-attachments/assets/5073e174-7128-4147-9512-539df9bb964a" />
