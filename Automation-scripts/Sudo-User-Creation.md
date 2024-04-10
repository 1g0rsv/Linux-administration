# Sudo User Creation Script

This script allows you to quickly create a new user on a Linux system, offering the option to add the user to their own group and/or the sudo group.

## Getting Started

Follow the instructions below to use this script. Ensure you have administrative rights on the target system to execute the script.

### Prerequisites

For the script to work, you will need:

- Access to a Linux system with administrative rights
- `curl` installed to download the script

### Installation

You can download and run the script on your target system by following these steps:

1. Open a terminal on your target system.
2. Execute the following command to download and run the script:

```bash
curl -sL https://raw.githubusercontent.com/1g0rsv/Linux-administration/main/Automation-scripts/Sudo-User-Creation.sh -o Sudo-User-Creation.sh && chmod +x Sudo-User-Creation.sh && ./Sudo-User-Creation.sh
