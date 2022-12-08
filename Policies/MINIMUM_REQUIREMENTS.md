# Minimum Requirements for an OPI Project Capable Device

- Contains a general purpose processor
- Has the ability to boot a general purpose Operating System
- Has domain-specific acceleration capabilities which can be accessed via an open API approach
- Has strict security isolation from the hosting system on the hardware-level
- Has a high performance network interface as its primary external data path
- Possesses a unique network identity on its primary network interface
- Has out-of-band management capabilities where the device is managed separately from its hosting system
- When the device takes the form of a PCIe add-on card inserted into a server as the hosting system, the following additional requirements also exist
  - PCIe device functions presented to the host are programmatically controlled by the device itself
  - PCIe device function changes must be presented via hot plug mechanisms
- Capable of hosting entire software subsystems, such as the Networking or Storage stack, including their control and data planes
