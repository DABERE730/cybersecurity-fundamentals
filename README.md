# Cybersecurity Fundamentals
### Foundational Concepts, Threat Types and Security Frameworks

## 1. Project Overview

Cybersecurity is the practice of protecting computer systems, networks, applications, and digital information against unauthorised access, attacks, damage, and disruption.

As individuals and organisations become increasingly dependent on digital technologies, protecting information and maintaining secure systems have become essential. Cybersecurity is therefore not limited to installing security software or responding to attacks. It involves understanding potential risks, identifying weaknesses, implementing appropriate safeguards, and maintaining the confidentiality, integrity, and availability of information.

This project explores the foundational principles of cybersecurity, common cyber threats, essential security practices, and recognised frameworks used to understand and manage cybersecurity risks.

It is intended to establish a solid theoretical foundation for further learning and practical development in cybersecurity.

## 2. Core Cybersecurity Concepts

Understanding cybersecurity begins with becoming familiar with the terminology used to describe security environments, potential attacks, and organisational risks.

Some of the most important concepts include:

| Concept | Explanation |
|---|---|
| Asset | Anything valuable that requires protection, including information, hardware, software, and network resources. |
| Threat | A potential event, action, or circumstance capable of causing harm to a system or organisation. |
| Vulnerability | A weakness in a system, application, process, or configuration that could be exploited. |
| Exploit | A method or technique used to take advantage of a vulnerability. |
| Risk | The potential for a threat to exploit a vulnerability and cause harm. |
| Attack Surface | The collection of points through which an attacker could potentially interact with or compromise a system. |
| Attack Vector | The method or pathway through which an attacker attempts to gain access or carry out an attack. |

These concepts are closely connected. For example, an organisation may have an exposed system containing a vulnerability. A threat actor could use an attack vector to exploit that weakness, potentially resulting in data exposure or service disruption.

Understanding these relationships helps security professionals identify risks and determine appropriate protective measures.

## 3. Common Cybersecurity Threats

Cyber threats vary in their methods, objectives, and potential impact. Some target technical weaknesses, while others exploit human behaviour.

Common examples include:

| Threat | Description |
|---|---|
| Malware | Malicious software designed to damage systems, disrupt operations, steal information, or gain unauthorised access. |
| Ransomware | A type of malware that prevents access to data or systems, commonly through encryption, and demands payment for restoration. |
| Phishing | Fraudulent communication designed to trick individuals into revealing sensitive information or performing harmful actions. |
| Social Engineering | The manipulation of individuals into disclosing information or taking actions that compromise security. |
| Denial-of-Service (DoS) | An attack intended to make a system or service unavailable to legitimate users. |
| Distributed Denial-of-Service (DDoS) | A denial-of-service attack originating from multiple systems or sources. |
| Man-in-the-Middle (MitM) | An attack in which communication between parties is intercepted and may be monitored or altered. |
| SQL Injection | An attack that manipulates database queries through improperly handled application input. |
| Brute-Force Attack | Repeatedly attempting possible passwords or credentials to gain unauthorised access. |
| Insider Threat | A security risk originating from someone with legitimate access to an organisation's systems or information. |

Recognising these threats is important because effective cybersecurity requires both prevention and the ability to detect and respond to malicious activity.

## 4. The CIA Triad

The CIA Triad is a fundamental model in information security. It describes three essential principles that guide the protection of information and systems.

### Confidentiality

Confidentiality ensures that information is accessible only to authorised individuals, systems, or processes.

Examples of measures that support confidentiality include:
- Encryption.
- Access controls.
- Multi-factor authentication.
- Appropriate user permissions.

### Integrity

Integrity ensures that information remains accurate, complete, and protected against unauthorised modification.

Examples of measures that support integrity include:
- File integrity monitoring.
- Hashing.
- Digital signatures.
- Change management controls.

### Availability

Availability ensures that systems, services, and information remain accessible to authorised users when required.

Examples of measures that support availability include:
- Regular backups.
- Redundancy.
- Disaster recovery planning.
- System maintenance and monitoring.

The three principles work together. A security measure that protects confidentiality but makes essential information permanently inaccessible, for example, would not provide a complete security solution.

## 5. Additional Security Principles

Beyond the CIA Triad, several other principles contribute to effective information security.

- **Authentication:** Verifying the identity of a user, device, or system.
- **Authorisation:** Determining what an authenticated user or system is permitted to access or perform.
- **Least Privilege:** Providing users and processes with only the permissions necessary to perform their responsibilities.
- **Non-repudiation:** Providing evidence that supports the verification of an action or transaction so that its origin or occurrence cannot reasonably be denied.
- **Defence in Depth:** Applying multiple layers of security controls so that the failure of one safeguard does not automatically compromise the entire environment.

These principles help establish stronger access management, accountability, and protection across digital environments.

## 6. Cybersecurity Frameworks

Cybersecurity frameworks provide structured guidance for identifying risks, implementing safeguards, monitoring security activities, and improving an organisation's overall security posture.

Two important frameworks explored in this project are NIST Cybersecurity Framework 2.0 and MITRE ATT&CK.

### 6.1 NIST Cybersecurity Framework 2.0

The National Institute of Standards and Technology (NIST) Cybersecurity Framework 2.0 provides guidance for organisations to understand, assess, prioritise, and manage cybersecurity risks.

It is organised around six core functions:

| Function | Purpose |
|---|---|
| Govern | Establishes cybersecurity strategy, policies, responsibilities, and oversight. |
| Identify | Helps organisations understand their assets, risks, and cybersecurity environment. |
| Protect | Establishes safeguards to reduce the likelihood and impact of cybersecurity incidents. |
| Detect | Focuses on identifying potential cybersecurity incidents and suspicious activities. |
| Respond | Provides guidance for taking action when a cybersecurity incident occurs. |
| Recover | Supports the restoration of affected systems, services, and operations. |

Together, these functions provide an organised approach to managing cybersecurity risks throughout an organisation.

### 6.2 MITRE ATT&CK Framework

MITRE ATT&CK is a globally recognised knowledge base that documents real-world adversary tactics and techniques.

It helps security professionals understand how attackers operate, from gaining initial access to carrying out activities such as privilege escalation, credential theft, lateral movement, and data exfiltration.

The framework organises adversary behaviour into:

- **Tactics:** The objectives an attacker is trying to achieve.
- **Techniques:** The methods used to accomplish those objectives.
- **Sub-techniques:** More specific variations of techniques.
- **Procedures:** Examples of how particular techniques are implemented in real-world activity.

MITRE ATT&CK is useful for threat intelligence, security monitoring, detection engineering, incident investigation, and evaluating defensive capabilities.

### 6.3 Understanding the Difference

Although both frameworks support cybersecurity, they serve different purposes.

| NIST CSF 2.0 | MITRE ATT&CK |
|---|---|
| Provides a structure for managing cybersecurity risk. | Documents adversary behaviour. |
| Helps organisations establish and improve security programmes. | Helps security teams understand attacker tactics and techniques. |
| Covers governance, identification, protection, detection, response, and recovery. | Focuses on how attackers operate and achieve their objectives. |
| Supports organisational cybersecurity planning. | Supports threat detection, analysis, and defensive improvements. |

They can complement each other: NIST provides a broader approach to cybersecurity risk management, while MITRE ATT&CK offers detailed insight into adversary behaviour.

## 7. Security Controls

Security controls are safeguards, measures, or mechanisms implemented to reduce risks and protect organisational assets.

They can be classified according to their purpose:

| Control Type | Purpose | Example |
|---|---|---|
| Preventive | Prevents or reduces the likelihood of an incident. | Firewalls and access restrictions. |
| Detective | Identifies suspicious activity or security incidents. | Intrusion detection systems and security monitoring. |
| Corrective | Addresses identified problems and helps restore normal operations. | Removing malware and applying security patches. |
| Deterrent | Discourages individuals from carrying out prohibited activities. | Warning notices and security policies. |
| Compensating | Provides an alternative safeguard when a primary control cannot be implemented. | Additional monitoring where a preferred security mechanism is unavailable. |

Effective security programmes use multiple types of controls rather than relying on a single protective measure.

## 8. People, Processes, and Technology

Cybersecurity is not achieved through technology alone. An effective security programme depends on three interconnected components.

**People**

People include employees, system administrators, users, and cybersecurity professionals. Their awareness, decisions, and actions can strengthen or weaken an organisation's security.

**Processes**

Processes include security policies, procedures, incident response plans, access management practices, and other established methods for maintaining security.

**Technology**

Technology includes hardware, software, networks, and security tools used to protect digital environments. Examples include firewalls, endpoint protection, encryption, and monitoring systems.

A weakness in any one of these areas can create security gaps. Effective cybersecurity requires all three to work together.

## 9. Practical Application: A Phishing Incident

Consider a hypothetical organisation in which an employee receives an email impersonating a trusted service provider.

The email contains a malicious attachment. The employee opens it, potentially allowing malicious software to execute on the workstation.

Depending on the organisation's security environment, the attacker may attempt to steal credentials, access sensitive information, or move to other systems.

This scenario demonstrates how several cybersecurity concepts apply in practice:

1. **Threat:** The phishing email and malicious attachment represent the initial threat.
2. **Attack Vector:** Email is used as the delivery method.
3. **Vulnerability:** Weak security configurations, inadequate controls, or unpatched software may increase the opportunity for compromise.
4. **Impact:** Confidential information may be exposed, data may be modified, or services may become unavailable.
5. **Prevention:** Email filtering, endpoint protection, access restrictions, and security awareness training can reduce the likelihood of compromise.
6. **Detection:** Security monitoring and endpoint detection tools can help identify suspicious activity.
7. **Response:** Incident response procedures guide investigation, containment, and remediation.
8. **Recovery:** Backups and recovery procedures help restore affected systems and operations.

The CIA Triad can be used to assess the potential impact, while MITRE ATT&CK can help security teams classify the adversary's behaviour.

This example illustrates how foundational cybersecurity concepts and frameworks can be applied to a realistic security situation.

## 10. Key Takeaways

The concepts explored in this project highlight several important lessons:

- Cybersecurity involves protecting information, systems, networks, and digital resources against potential threats.
- Understanding the relationship between assets, threats, vulnerabilities, exploits, and risks is essential for identifying security weaknesses.
- Cyber threats can target both technical systems and human behaviour.
- The CIA Triad provides a foundation for maintaining confidentiality, integrity, and availability.
- Security principles such as least privilege and defence in depth contribute to stronger protection.
- NIST CSF 2.0 provides a structured approach to cybersecurity risk management.
- MITRE ATT&CK helps security professionals understand and analyse adversary behaviour.
- Effective security requires appropriate controls, processes, technology, and informed people.

## 11. Conclusion

Cybersecurity begins with understanding the systems and information that require protection, the threats that may affect them, and the weaknesses that could be exploited.

The principles, threats, controls, and frameworks discussed in this project provide a foundation for understanding how organisations approach information security and manage cybersecurity risks.

Developing this knowledge is an important step towards more advanced areas of cybersecurity, including vulnerability assessment, security operations, threat detection, and incident response.

## 12. Detailed Documentation

This README provides an overview of the concepts covered in this project.

For more comprehensive explanations, expanded examples, detailed breakdowns of cybersecurity frameworks, additional security concepts, and further references, see the complete documentation:

### [Read the Complete Cybersecurity Fundamentals Documentation](Cybersecurity-Fundamentals.md)

The accompanying document expands on the topics introduced here and serves as the main reference material for this project.

## 13. References and Further Reading

The following official resources provide additional information on the concepts and frameworks discussed in this project.

1. **National Institute of Standards and Technology (NIST)**  
   [NIST Cybersecurity Framework 2.0](https://www.nist.gov/cyberframework)

2. **MITRE**  
   [MITRE ATT&CK Knowledge Base](https://attack.mitre.org/)

3. **NIST Computer Security Resource Center**  
   [NIST Cybersecurity Publications and Resources](https://csrc.nist.gov/)

4. **Cybersecurity and Infrastructure Security Agency (CISA)**  
   [CISA Cybersecurity Resources](https://www.cisa.gov/)

---

**Project Category:** Cybersecurity Fundamentals  
**Focus Areas:** Information Security, Threat Awareness, Security Principles, and Cybersecurity Frameworks  
**Documentation Format:** Markdown, PDF
**Purpose:** Foundational cybersecurity learning and knowledge development
