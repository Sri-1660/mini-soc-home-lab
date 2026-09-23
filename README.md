# Mini SOC Home Lab

A hands-on Security Operations Center (SOC) home lab built to practice
security monitoring, endpoint telemetry, alert investigation,
MITRE ATT&CK mapping, and AI-assisted SOC analysis.

## Overview

This project simulates a small SOC environment using Wazuh as the
SIEM/XDR platform.

The lab monitors both Linux and Windows endpoint activity and
investigates security events using a structured SOC investigation
workflow.

A Python + Groq AI layer was also developed to assist with analysis
of Wazuh security alerts.

🎥 Project Demo: https://drive.google.com/file/d/1P9itA-LQEAFvkKZn3QgQNmvsnMPRfV9_/view?usp=drive_link

## Architecture

```text
                    SOC Analyst
                        │
                        ▼
                Wazuh Dashboard
                        │
                        ▼
                 Wazuh Manager
                  /          \
                 /            \
                ▼              ▼
        Linux Lab Host     Windows 11
                              │
                              ▼
                           Sysmon
                              │
                              ▼
                        Wazuh Agent
                              │
                              ▼
                       Security Events
                              │
                              ▼
                       Python AI Layer
                              │
                              ▼
                         Groq LLM
                              │
                              ▼
                      SOC Investigation
                           Report
