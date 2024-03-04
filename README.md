# Ransomware Detection and Prevention Configuration

## Overview

This repository contains configuration files and scripts to enhance ransomware detection and prevention capabilities in the Wazuh security information and event management (SIEM) system. The provided files are organized into two folders:

1. **manager-conf**: This folder includes configuration files (`ossec.conf` and `local_rules.xml`) that should be modified in the Wazuh manager to enable ransomware detection and prevention rules.

2. **win-conf**: This folder contains a Python script (`remove-threat.py`) that verifies file hashes and removes files if they are identified as potential ransomware threats.

## Instructions

### manager-conf

#### ossec.conf

The `ossec.conf` file in this folder contains additional configurations to be added to your Wazuh manager configuration. These configurations include rules and settings specifically designed for ransomware detection. Please merge the content of this file into your existing `ossec.conf` file.

#### local_rules.xml

The `local_rules.xml` file includes custom rules that augment the default Wazuh ruleset to improve ransomware detection. Merge the content of this file into your existing `local_rules.xml` file.

### win-conf

#### remove-threat.py

The `remove-threat.py` script is designed to be run on Windows systems. It uses file hashes to identify potential ransomware threats and removes the files if they match known threat signatures. To use this script:

1. Ensure you have Python installed on your Windows system.

2. Run the script from the command line:

   ```bash
   python remove-threat.py
   ```

   Note: Make sure to run the command with appropriate privileges to access and remove files.

   The script will prompt you to enter the path of the directory to scan for potential ransomware threats.

## Disclaimer

Use these configurations and scripts at your own risk. Make sure to thoroughly test them in a controlled environment before deploying them in a production setting. The provided configurations and scripts are intended to enhance ransomware detection and prevention, but their effectiveness may vary depending on your specific environment and requirements. Always follow best practices for security and regularly review and update your configurations based on the evolving threat landscape.

## Contributions

Contributions are welcome! If you have improvements, bug fixes, or additional features to suggest, feel free to submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
