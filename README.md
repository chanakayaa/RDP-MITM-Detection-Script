Here's a complete README for your RDP MITM Detection Script repository:

---

# RDP MITM Detection Script

This repository contains an Nmap script designed to check if an RDP (Remote Desktop Protocol) server is vulnerable to Man-in-the-Middle (MITM) attacks. The script detects weak encryption configurations or the absence of Network Level Authentication (NLA) in RDP servers.

## Description

The RDP MITM Detection Script performs the following tasks:
- Checks if the RDP server is vulnerable to MITM attacks.
- Detects weak encryption configurations or missing NLA by initiating an RDP connection and analyzing the server's response.

## Features

- **Detect Weak Encryption**: Identifies if the RDP server supports weak encryption algorithms.
- **Check NLA Status**: Determines if Network Level Authentication is enabled or missing.
- **Automated Detection**: Integrates with Nmap to automate the detection process.

## Prerequisites

- **Nmap**: The script is designed to be used with Nmap. Ensure Nmap is installed and properly configured on your system.

## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/rdp-mitm-detection.git
   cd rdp-mitm-detection
   ```

2. **Add the Script to Nmap's Script Directory:**

   Copy the script to Nmap's script directory, typically found at `/usr/share/nmap/scripts/` on Linux systems or `C:\Program Files (x86)\Nmap\scripts\` on Windows.

   ```bash
   sudo cp rdp_mitm_detection.nse /usr/share/nmap/scripts/
   ```

3. **Update Nmap Script Database:**

   Update the Nmap script database to include the new script.

   ```bash
   sudo nmap --script-updatedb
   ```

## Usage

To use the script, run Nmap with the `--script` option and specify the target. For example:

```bash
nmap -p 3389 --script rdp_mitm_detection <target_ip>
```

- Replace `<target_ip>` with the IP address of the RDP server you want to scan.

## Script Details

- **Script Name**: `rdp_mitm_detection.nse`
- **Author**: Your Name
- **License**: Same as Nmap - see [Nmap License](https://nmap.org/book/man-legal.html)
- **Categories**: `safe`, `discovery`



## Contributing

Contributions are welcome! If you have any improvements or bug fixes, feel free to submit a pull request or open an issue.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
