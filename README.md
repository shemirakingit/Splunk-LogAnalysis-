# Splunk-LogAnalysis-
Hands-on SIEM lab on GCP — Splunk deployment, log forwarding via Universal Forwarder, custom SPL searches, security dashboards, and automated brute-force detection alerting.
# Splunk SIEM Lab — GCP Deployment

A hands-on SIEM lab built on Google Cloud Platform, focused on log ingestion, search processing, dashboarding, and automated threat detection using Splunk.

## Overview

This project simulates a small-scale enterprise security monitoring setup. It covers provisioning cloud infrastructure, deploying Splunk components, forwarding logs from a monitored host, building custom searches and dashboards, and configuring an automated alert for brute-force login attempts.

## Architecture

- **Cloud Platform:** Google Cloud Platform (GCP)
- **VM Instance:** Ubuntu Server (Compute Engine)
- **SIEM Platform:** Splunk Enterprise
- **Log Forwarding:** Splunk Universal Forwarder
- **Detection Logic:** Scheduled SPL search with alerting

```
[Ubuntu VM] --(Universal Forwarder)--> [Splunk Indexer/Search Head]
                                              |
                                   [Dashboards + Alerts]
```

## What This Lab Covers

### 1. Infrastructure Provisioning
- Deployed an Ubuntu VM on GCP Compute Engine
- Configured networking, firewall rules, and SSH access

### 2. Splunk Deployment
- Installed and configured Splunk Enterprise (indexer/search head)
- Installed and configured the Splunk Universal Forwarder on the Ubuntu VM
- Established data forwarding from the VM to the Splunk instance

### 3. Search Processing Language (SPL)
- Wrote custom SPL queries to parse and filter incoming log data
- Built searches to identify authentication events, failed logins, and system activity patterns

### 4. Dashboards
- Created visual dashboards summarizing key security metrics
- Included panels for login activity, event trends, and system health indicators

### 5. Automated Alerting
- Configured a scheduled search to detect brute-force login attempts
- Set alert thresholds and actions to trigger notifications when suspicious patterns are detected

## Skills Demonstrated

- Cloud infrastructure provisioning (GCP)
- Linux system administration (Ubuntu)
- SIEM deployment and configuration
- Log forwarding and data ingestion pipelines
- SPL (Search Processing Language) query writing
- Security dashboard design
- Threat detection and alert automation

## Lessons Learned

- Configuring the Universal Forwarder correctly is critical — misconfigured inputs.conf files are a common source of "missing data" issues in Splunk deployments.
- SPL searches benefit significantly from field extraction planning up front, rather than adjusting after dashboards are built.
- Alert thresholds require tuning to balance sensitivity (catching real brute-force attempts) against noise (false positives from normal failed logins).

## Next Steps / Future Improvements

- Expand log sources beyond the single Ubuntu VM (e.g., additional hosts, firewall logs, cloud audit logs)
- Integrate with a ticketing/notification system (e.g., Slack, email) for real-time alert delivery
- Explore Splunk's Enterprise Security app for more advanced correlation searches


<img width="4480" height="1297" alt="245E74DF-98A9-4515-A4C3-3FC2BB1B53DF_1_201_a" src="https://github.com/user-attachments/assets/db280383-96e5-49e3-ad92-ba636868773a" />

## Author

Shemira — IT Systems Administrator | Cloud & Security Enthusiast

---

*This lab was built as part of an ongoing hands-on portfolio project focused on cloud security, SIEM tooling, and infrastructure automation.*
