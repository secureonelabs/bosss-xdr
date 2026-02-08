<p align="center">
    <img width="640px" src="logo.png" alt="BOSSS XDR"/>
</p>

# BOSSS XDR

> Based on [Wazuh](https://wazuh.com), an open source security platform.

BOSSS XDR is a free and open source platform used for threat prevention, detection, and response. It is capable of protecting workloads across on-premises, virtualized, containerized, and cloud-based environments.

The BOSSS XDR solution consists of an endpoint security agent, deployed to the monitored systems, and a management server, which collects and analyzes data gathered by the agents. It integrates with OpenSearch, providing a search engine and data visualization tool that allows users to navigate through their security alerts.

## Capabilities

A brief presentation of some of the more common use cases of the BOSSS XDR solution.

**Intrusion detection**

BOSSS XDR agents scan the monitored systems looking for malware, rootkits and suspicious anomalies. They can detect hidden files, cloaked processes or unregistered network listeners, as well as inconsistencies in system call responses.

In addition to agent capabilities, the server component uses a signature-based approach to intrusion detection, using its regular expression engine to analyze collected log data and look for indicators of compromise.

**Log data analysis**

BOSSS XDR agents read operating system and application logs, and securely forward them to a central manager for rule-based analysis and storage. When no agent is deployed, the server can also receive data via syslog from network devices or applications.

The rules help make you aware of application or system errors, misconfigurations, attempted and/or successful malicious activities, policy violations and a variety of other security and operational issues.

**File integrity monitoring**

BOSSS XDR monitors the file system, identifying changes in content, permissions, ownership, and attributes of files that you need to keep an eye on. In addition, it natively identifies users and applications used to create or modify files.

File integrity monitoring capabilities can be used in combination with threat intelligence to identify threats or compromised hosts. In addition, several regulatory compliance standards, such as PCI DSS, require it.

**Vulnerability detection**

BOSSS XDR agents pull software inventory data and send this information to the server, where it is correlated with continuously updated CVE (Common Vulnerabilities and Exposure) databases, in order to identify well-known vulnerable software.

Automated vulnerability assessment helps you find the weak spots in your critical assets and take corrective action before attackers exploit them to sabotage your business or steal confidential data.

**Configuration assessment**

BOSSS XDR monitors system and application configuration settings to ensure they are compliant with your security policies, standards and/or hardening guides. Agents perform periodic scans to detect applications that are known to be vulnerable, unpatched, or insecurely configured.

**Incident response**

BOSSS XDR provides out-of-the-box active responses to perform various countermeasures to address active threats, such as blocking access to a system from the threat source when certain criteria are met.

**Regulatory compliance**

BOSSS XDR provides some of the necessary security controls to become compliant with industry standards and regulations. These features, combined with its scalability and multi-platform support help organizations meet technical compliance requirements.

**Cloud security**

BOSSS XDR helps monitoring cloud infrastructure at an API level, using integration modules that are able to pull security data from well known cloud providers, such as Amazon AWS, Azure or Google Cloud.

In addition, BOSSS XDR provides rules to assess the configuration of your cloud environment, easily spotting weaknesses.

**Containers security**

BOSSS XDR provides security visibility into your Docker hosts and containers, monitoring their behavior and detecting threats, vulnerabilities and anomalies. The agent has native integration with the Docker engine allowing users to monitor images, volumes, network settings, and running containers.

## Documentation

* [Full documentation](https://documentation.wazuh.com)
* [Installation guide](https://documentation.wazuh.com/current/installation-guide/index.html)

## Security

If you discover a security vulnerability, please send an email to security@secureonelabs.com. Please do not open a public issue.

## License

This project is licensed under the [GNU General Public License v2.0](LICENSE).

## Attribution

This project is based on [Wazuh](https://github.com/wazuh/wazuh), which is licensed under GPLv2. See [ATTRIBUTION.md](ATTRIBUTION.md) for details.

Copyright (C) 2015, Wazuh Inc.
Copyright (C) 2024, SecureOneLabs
