# CodeAlpha_Network_Intrusion_Detection_System

This repository contains the implementation of a Network Intrusion Detection System (NIDS) developed as part of an internship task at CodeAlpha. The NIDS is built using Suricata, an open-source Intrusion Detection and Prevention System (IDPS) engine, to monitor network traffic and detect suspicious activities.

## Installation

1.  Clone the repository:
    
    ```bash
    git clone https://github.com/ahmedelgendy3/CodeAlpha_Network_Intrusion_Detection_System
    ```
    
2.  Navigate to the project directory:
    
    ```bash
    cd CodeAlpha_Network_Intrusion_Detection_System
    ```
    
3.  Configure Suricata:
    
    Follow the installation instructions provided in the Suricata documentation to install and configure Suricata on your system.
    
4.  Customize Rules:
    
    Create or modify the Suricata rules file (`custom.rules`) to define custom intrusion detection rules tailored to your network environment and security requirements.
    
## Configuration

- **Suricata Configuration**: Modify the Suricata configuration file (`/etc/suricata/suricata.yaml`) to customize various settings such as interface configuration, logging options, and performance tuning. Ensure to update the `$HOME_NET` variable in the configuration file to reflect your actual internal network subnet.


## Usage

```bash
sudo suricata -c /etc/suricata/suricata.yaml -S custom.rules -i <interface>
```

- **-c /etc/suricata/suricata.yaml**: Specifies the path to the main configuration file for Suricata. By default, Suricata looks for its configuration in this file. In this command, it points to the Suricata configuration file located at `/etc/suricata/suricata.yaml`.
- **-S custom.rules**: Loads a custom rules file exclusively. This option instructs Suricata to use the specified file (`custom.rules`) for intrusion detection rules. These rules define the criteria for identifying suspicious network traffic and potential security threats.
- **-i**: Specifies the network interface on which Suricata will listen for network traffic. This interface is where Suricata will capture packets and analyze them for suspicious activity. Replace `<interface>` with the name of the network interface you want Suricata to monitor, such as `eth0` or `ens33`.

The NIDS monitors network traffic on the specified interface using Suricata's rule-based detection engine. Detected events are logged and can be analyzed for potential security threats.

## Features

- **Rule-Based Detection**: Utilizes Suricata's rule-based detection engine to detect various network-based attacks and anomalies.
- **Customizable Rules**: Allows users to define custom intrusion detection rules to match specific network traffic patterns and security policies.
- **Event Logging**: Logs detected events to facilitate post-analysis and investigation of security incidents.
- **Testing**: Includes testing methodologies to verify the effectiveness of custom rules and analyze live network traffic.

## Testing

1.  **Test Custom Rules**: Use test scenarios to verify the effectiveness of custom intrusion detection rules in detecting predefined attack patterns and anomalies.
    
2.  **Live Traffic Analysis**: Monitor live network traffic on the specified interface and analyze the Suricata logs (`/var/log/suricata`) to identify and investigate potential security threats.
    
3.  **Test with Metasploitable 2**: Deploy a vulnerable virtual machine (e.g., Metasploitable 2) on the same network and conduct targeted attacks (e.g., FTP, Telnet, SSH) to validate the NIDS's ability to detect and mitigate security risks.
    

## Resources

- [Suricata Documentation](https://suricata.readthedocs.io/)
- [Suricata Rule Management](https://suricata.readthedocs.io/en/suricata-6.0.0/rule-management/adding-your-own-rules.html)
- [Google's Detection and Response Course](https://www.coursera.org/learn/detection-and-response)
