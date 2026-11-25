# Cybersecurity Fundamentals: Foundational Concepts, Threat Types and Security Frameworks

> **Portfolio learning resource** · Foundational cybersecurity · NIST
> CSF 2.0 · MITRE ATT&CK

## Overview

Cybersecurity is the practice of managing risks to information, systems,
networks, applications, and the people who use them. It combines
technical safeguards with governance, repeatable processes, and informed
human decisions. A useful foundation therefore goes beyond memorizing
attack names: it means understanding what must be protected, how
adversaries and accidents can cause harm, how risk is evaluated, and how
organizations select, operate, and improve security controls.

This guide introduces core information-security concepts, explains
common attack patterns and their defenses, examines the CIA triad and
related principles, and compares two widely used resources: the **NIST
Cybersecurity Framework (CSF) 2.0** and **MITRE ATT&CK**. A hypothetical
incident ties the concepts together.

The material is educational. It describes concepts and illustrative
practices; it does not claim that the author has deployed the controls,
conducted an assessment, or responded to a real incident.

## Table of Contents

-   [1. Introduction to Cybersecurity](#1-introduction-to-cybersecurity)
-   [2. Core Cybersecurity Concepts](#2-core-cybersecurity-concepts)
-   [3. Common Cyber Threats and
    Attacks](#3-common-cyber-threats-and-attacks)
-   [4. The CIA Triad](#4-the-cia-triad)
-   [5. Additional Security
    Principles](#5-additional-security-principles)
-   [6. Cybersecurity Frameworks](#6-cybersecurity-frameworks)
    -   [6.1 NIST Cybersecurity Framework
        2.0](#61-nist-cybersecurity-framework-20)
    -   [6.2 MITRE ATTCK](#62-mitre-attck)
    -   [6.3 NIST CSF 2.0 and MITRE ATTCK
        Compared](#63-nist-csf-20-and-mitre-attck-compared)
-   [7. Security Controls](#7-security-controls)
-   [8. People, Processes and
    Technology](#8-people-processes-and-technology)
-   [9. Practical Application: Hypothetical
    Incident](#9-practical-application-hypothetical-incident)
-   [10. Key Takeaways and Conclusion](#10-key-takeaways-and-conclusion)
-   [11. Official References and Further
    Reading](#11-official-references-and-further-reading)

------------------------------------------------------------------------

## 1. Introduction to Cybersecurity

### 1.1 Definition and purpose

**Cybersecurity** is the discipline of protecting digital systems,
networks, applications, devices, and information against unauthorized
access, misuse, disruption, modification, or destruction. It includes
the technologies, policies, procedures, skills, and oversight used to
manage those risks.

The purpose is not simply to prevent every possible attack. No
organization can eliminate all risk. The practical goal is to reduce the
likelihood and consequences of harmful events to a level consistent with
the organization's mission, legal obligations, risk appetite, and
available resources. Effective cybersecurity also helps an organization
detect problems quickly, respond in a controlled way, and restore
trustworthy services.

Cybersecurity overlaps with information security. Information security
protects information in any form---digital, paper, spoken, or
otherwise---whereas cybersecurity focuses particularly on risks
involving digital environments. In practice, the disciplines are closely
connected.

### 1.2 Importance in modern organizations

Organizations depend on connected systems for payments, communications,
customer records, logistics, cloud services, industrial operations, and
decision-making. This dependence creates value but also creates
exposure.

A security failure can lead to:

-   **Financial loss:** fraud, ransom demands, recovery costs, business
    interruption, and legal expenses.
-   **Privacy harm:** exposure of personal, financial, health, or
    confidential business information.
-   **Operational disruption:** unavailable applications, damaged
    equipment, interrupted production, or delayed services.
-   **Loss of trust:** customers, employees, partners, and investors may
    lose confidence.
-   **Legal and regulatory consequences:** investigations, contractual
    penalties, reporting obligations, or sanctions.
-   **Strategic harm:** stolen intellectual property, competitive
    disadvantage, or compromise of sensitive plans.

Modern environments are complex. Employees work remotely, organizations
use cloud platforms and third-party providers, mobile devices connect
from many locations, and business systems exchange data through APIs.
Security must account for these relationships rather than treating the
corporate network as a single protected boundary.

### 1.3 Common security objectives

The foundational objectives are confidentiality, integrity, and
availability, commonly called the **CIA triad**. Organizations also
pursue identity assurance, accountability, privacy, resilience, and
compliance.

A sound security program seeks to:

1.  Protect information from unauthorized disclosure.
2.  Prevent or detect unauthorized changes.
3.  Keep systems and information available when needed.
4.  Ensure that users and services are who or what they claim to be.
5.  Limit each identity to the permissions needed for its tasks.
6.  Record relevant actions so activity can be reviewed.
7.  Prepare to contain incidents and restore services safely.

These objectives can conflict. For example, strict access restrictions
may improve confidentiality but make a service harder to use. Security
design is therefore a risk-informed balance, not the maximization of one
property in isolation.

## 2. Core Cybersecurity Concepts

The following terms describe different parts of a security problem. They
are related, but they are not interchangeable.

### 2.1 Assets

An **asset** is anything valuable that an organization needs to protect.
Assets include more than computers.

Examples:

-   Data: customer records, payment details, source code, business
    plans.
-   Technology: laptops, servers, routers, cloud workloads,
    applications, databases.
-   Identities: employee accounts, administrator accounts, service
    accounts, API keys.
-   Business capabilities: payroll, online ordering, manufacturing,
    customer support.
-   People, facilities, reputation, and intellectual property.

Asset identification helps determine what matters most and what level of
protection is justified. A public brochure and a database containing
customer identity documents should not automatically receive identical
protection.

### 2.2 Threats

A **threat** is a potential cause of harm to an asset. Threats may be
deliberate, accidental, or environmental.

Examples include a criminal group attempting to steal credentials, an
employee accidentally deleting a production database, a power failure,
or a fire in a data centre.

A threat describes the possibility or source of harm; it does not prove
that an incident has occurred.

### 2.3 Threat actors

A **threat actor** is an individual or group that performs, sponsors, or
enables actions that may harm an organization.

Common categories include:

-   **Cybercriminals:** commonly motivated by financial gain, such as
    fraud or extortion.
-   **Nation-state or state-sponsored groups:** may pursue espionage,
    strategic advantage, or disruption.
-   **Hacktivists:** may act to promote a political or social cause.
-   **Insiders:** employees, contractors, or trusted users who
    intentionally or unintentionally create risk.
-   **Competitors or industrial spies:** may seek confidential business
    information.
-   **Opportunistic attackers:** exploit exposed systems or widely known
    weaknesses without a specific target.

Attribution is difficult. An observed technique does not, by itself,
establish who performed an attack or why.

### 2.4 Vulnerabilities

A **vulnerability** is a weakness in software, hardware, configuration,
process, or human practice that could be exploited.

Examples:

-   An internet-facing server running software with a known unpatched
    flaw.
-   A storage bucket configured for public access when it should be
    private.
-   A weak password policy or lack of multi-factor authentication.
-   Excessive permissions assigned to a service account.
-   Employees who have not been taught how to report suspicious
    messages.

A vulnerability may exist without being exploited. Its significance
depends on the asset, exposure, threat capability, and available
safeguards.

### 2.5 Exploits

An **exploit** is a method, sequence of actions, or piece of code that
takes advantage of a vulnerability or security weakness.

For example, a vulnerable web application may fail to distinguish
trusted database commands from user-supplied input. An attacker could
use a crafted input sequence to cause an unintended database query. The
vulnerability is the weakness; the exploit is the means of taking
advantage of it.

Not every exploit is malware, and not every vulnerability has a publicly
available exploit.

### 2.6 Risk

**Risk** is the potential for an unwanted outcome, commonly considered
in terms of the likelihood of an event and the severity of its
consequences. A simplified model is:

> **Risk ≈ Likelihood × Impact**

This is a conceptual model, not a universal mathematical formula.
Organizations may use qualitative ratings, quantitative models, or a
combination.

Example: an internet-facing payroll application with a critical
unpatched flaw, weak authentication, and access to sensitive employee
records may present high risk. A similar flaw on an isolated test system
containing no sensitive data may have a different risk profile.

Risk assessment should consider:

-   Asset value and business criticality.
-   Threat sources and their capabilities.
-   Vulnerability severity and exploitability.
-   Exposure and existing safeguards.
-   Potential operational, financial, privacy, and legal impact.

Risk can be treated by avoiding the activity, mitigating the risk,
transferring or sharing some financial consequences, or accepting it
through an authorized decision. Transferring risk (for example, through
insurance) does not transfer all responsibility or eliminate the
underlying threat.

### 2.7 Attack surfaces

An **attack surface** is the set of points where an attacker could
attempt to enter, affect, or extract information from an environment.

Examples include:

-   Internet-facing websites, VPN gateways, and remote-access services.
-   Employee email accounts and endpoints.
-   Cloud consoles, storage services, and APIs.
-   Wireless networks and exposed network services.
-   Third-party connections and software supply chains.
-   Physical access points, removable media, and unattended devices.

Reducing the attack surface means removing unnecessary services,
limiting exposure, securing identities, segmenting networks, and
maintaining accurate asset inventories.

### 2.8 Attack vectors

An **attack vector** is the path or method used to reach a target or
exploit a weakness.

Examples include a phishing email, a stolen VPN credential, a vulnerable
public web form, a malicious attachment, or a compromised supplier
update.

**Attack surface vs. attack vector:** the attack surface is the
collection of possible entry or interaction points; an attack vector is
a particular route used through one or more of those points.

### 2.9 Security incidents

A **security incident** is an event, or series of events, that actually
or imminently jeopardizes the confidentiality, integrity, or
availability of information or systems, or violates security policy.

Examples include confirmed malware execution, unauthorized access to an
account, data exfiltration, ransomware encryption, or a misconfiguration
that exposes confidential records.

A security alert is not automatically an incident. Alerts require triage
and investigation. Conversely, an incident may exist before a monitoring
tool generates an alert.

### 2.10 How the concepts fit together

Consider a fictional online retailer:

1.  Its customer database is an **asset**.
2.  A financially motivated criminal group is a possible **threat
    actor**.
3.  The database server has an unpatched software flaw, a
    **vulnerability**.
4.  The attacker uses a crafted request, an **exploit**.
5.  The public application is part of the **attack surface**; the
    crafted web request is the **attack vector**.
6.  Unauthorized access could expose customer records. The likelihood
    and impact determine the **risk**.
7.  Confirmed unauthorized access becomes a **security incident**.

  -----------------------------------------------------------------------
  Concept                 Key question            Example
  ----------------------- ----------------------- -----------------------
  Asset                   What has value?         Customer database

  Threat                  What could cause harm?  Criminal intrusion

  Threat actor            Who may cause it?       Financially motivated
                                                  group

  Vulnerability           What weakness exists?   Unpatched application

  Exploit                 How is the weakness     Crafted request
                          used?                   

  Attack surface          Where could interaction Public web application
                          occur?                  

  Attack vector           What route was used?    Malicious HTTP request

  Risk                    How likely and harmful  Potential customer-data
                          is it?                  exposure

  Incident                Has security been       Confirmed unauthorized
                          compromised or          database access
                          imminently jeopardized? 
  -----------------------------------------------------------------------

## 3. Common Cyber Threats and Attacks

Threats often overlap. For example, phishing may deliver a Trojan, which
may steal credentials and enable ransomware deployment. The descriptions
below explain the concepts at a defensive level.

### 3.1 Malware

**What it is:** Malware (malicious software) is software or code
designed to perform unauthorized or harmful actions.

**How it works conceptually:** It may arrive through an attachment,
download, compromised website, removable device, software supply chain,
or exploitation of a vulnerability. Depending on its purpose, it may
steal data, disrupt systems, spy on users, or provide remote access.

**Potential impact:** Data theft, system damage, unauthorized control,
service interruption, fraud, and further compromise.

**Defenses:** Endpoint detection and response (EDR), anti-malware
controls, application allowlisting where appropriate, patching, least
privilege, network segmentation, secure backups, email/web filtering,
and user awareness.

### 3.2 Viruses and worms

-   **Virus:** malicious code that attaches to a host file or program
    and typically spreads when the infected host is executed or shared.
-   **Worm:** standalone malware that can self-propagate, often by
    exploiting vulnerable services or using network connections, without
    needing to attach to another file.

**How they work:** A virus relies on infected content being run or
distributed. A worm can scan for other reachable systems and spread
automatically.

**Impact:** Widespread infection, resource consumption, data corruption,
service disruption, and delivery of additional malware.

**Defenses:** Timely patching, endpoint protection, disabling
unnecessary services, network segmentation, secure configuration, email
controls, and monitoring for unusual propagation patterns.

### 3.3 Trojan horses

**What it is:** A Trojan is malware disguised as, or bundled with,
something that appears legitimate. Unlike a worm, a Trojan does not
inherently self-replicate.

**How it works:** A user may install a fake utility, open a
booby-trapped document, or run a compromised installer. The Trojan may
then install a backdoor, steal credentials, or download additional
payloads.

**Impact:** Remote access, credential theft, surveillance, data theft,
and a foothold for more serious attacks.

**Defenses:** Obtain software from trusted sources, verify signatures
where available, restrict software installation, use EDR, apply least
privilege, and monitor unexpected persistence or outbound connections.

### 3.4 Ransomware

**What it is:** Ransomware is malware or an attack operation that denies
access to data or systems, commonly by encrypting them, and demands
payment. Some operations also steal data and threaten disclosure---often
called double extortion.

**How it works conceptually:** Attackers may gain access through
phishing, stolen credentials, exposed remote services, or exploited
vulnerabilities. They may then move laterally, disable defenses,
identify valuable data, exfiltrate information, and encrypt systems.

**Impact:** Operational shutdown, data loss, extortion, regulatory
exposure, recovery expense, and reputational damage. Paying does not
guarantee restoration or deletion of stolen data.

**Defenses:** Offline or immutable backups with tested restoration, MFA,
patching, EDR, segmentation, privileged-access controls, application
control, email security, logging, and rehearsed incident-response plans.

### 3.5 Spyware

**What it is:** Spyware covertly collects information about a user,
device, or organization.

**How it works:** It may record keystrokes, capture screens, monitor
browsing, collect files, or harvest credentials. It may be installed
through malicious software, exploit chains, or unwanted applications.

**Impact:** Privacy violations, account takeover, intellectual-property
theft, and surveillance.

**Defenses:** Endpoint protection, software restriction, patching,
mobile-device management, browser controls, least privilege, and review
of suspicious processes and network traffic.

### 3.6 Phishing

**What it is:** Phishing is a social-engineering technique in which an
attacker uses deceptive electronic communication---often email---to
trick a recipient into revealing information, transferring money, or
executing a harmful action.

**How it works:** A message may imitate a bank, supplier, colleague, or
cloud service and direct the recipient to a fake sign-in page or
malicious attachment.

**Impact:** Credential theft, malware infection, fraudulent payments,
account compromise, and data exposure.

**Defenses:** Email authentication and filtering, MFA (preferably
phishing-resistant methods), safe link and attachment analysis, user
education, independent verification of payment or account-change
requests, and easy reporting channels.

### 3.7 Spear phishing

**What it is:** A targeted form of phishing tailored to a particular
person, role, or organization.

**How it works:** The attacker uses contextual details---such as a
current project, colleague's name, supplier relationship, or job
responsibility---to make the message credible.

**Impact:** Targeted account compromise, sensitive-data theft, fraud, or
access to high-value systems.

**Defenses:** Strong identity controls, phishing-resistant MFA,
verification through a separate trusted channel, role-based awareness
training, and monitoring of unusual sign-ins and mailbox rules.

### 3.8 Whaling

**What it is:** Whaling is spear phishing directed at senior executives
or other high-impact individuals.

**How it works:** Messages may impersonate legal counsel, board members,
finance leaders, or business partners and request urgent wire transfers,
confidential documents, or account access.

**Impact:** Large financial losses, disclosure of strategic information,
and compromise of privileged accounts.

**Defenses:** Dual approval for high-value transactions, out-of-band
verification, executive-focused awareness, strong MFA,
privileged-account separation, and payment-change procedures.

### 3.9 Smishing and vishing

-   **Smishing:** phishing through SMS or other text messaging.
-   **Vishing:** phishing through voice calls or voice messages.

**How they work:** A text may claim that a delivery failed or an account
is locked. A caller may impersonate technical support, a bank, or an
authority and pressure the victim to disclose a code or install
remote-access software.

**Impact:** Credential and one-time-code theft, fraudulent transfers,
identity theft, and device compromise.

**Defenses:** Do not trust caller ID or unexpected links, never disclose
authentication codes, use official contact details to call back, train
staff to recognize urgency tactics, and require independent verification
for sensitive requests.

### 3.10 Social engineering

**What it is:** Social engineering manipulates people into taking
actions or disclosing information that weaken security.

**How it works:** Common techniques include impersonation, urgency,
authority, fear, curiosity, reciprocity, pretexting, baiting, and
tailgating. Phishing is one form of social engineering; social
engineering also occurs in person and by phone.

**Impact:** Unauthorized access, fraud, disclosure, malware execution,
and bypass of otherwise sound technical controls.

**Defenses:** Awareness training, clear verification procedures, visitor
controls, least privilege, reporting mechanisms, and a culture where
employees can pause and verify unusual requests without penalty.

### 3.11 Denial-of-Service (DoS)

**What it is:** A DoS attack attempts to make a system or service
unavailable to legitimate users, often by exhausting bandwidth,
connection capacity, memory, CPU, or application resources.

**How it works:** A single source or a small number of sources sends
excessive or malformed requests, or triggers expensive operations that
overwhelm the target.

**Impact:** Service outage, lost revenue, missed transactions, and
degraded customer trust.

**Defenses:** Rate limiting, traffic filtering, resilient architecture,
capacity planning, web application firewalls, upstream provider
coordination, and monitoring of service health.

### 3.12 Distributed Denial-of-Service (DDoS)

**What it is:** A DDoS attack is a DoS attack generated from many
distributed systems, often compromised devices in a botnet.

**How it works:** Traffic from numerous sources converges on a target,
making simple source blocking ineffective and potentially overwhelming
network or application capacity.

**Impact:** The same availability harms as DoS, often at greater scale
and with more complex mitigation.

**Defenses:** DDoS protection services, content delivery networks,
upstream filtering, traffic scrubbing, rate limiting, resilient DNS and
network design, and a tested response plan with service providers.

### 3.13 Man-in-the-Middle (MitM) attacks

**What it is:** A MitM attack occurs when an adversary positions
themselves between communicating parties and can observe, relay, or
alter communications.

**How it works:** An attacker may exploit an untrusted Wi-Fi network,
compromised router, weak encryption, certificate-validation failure, or
name-resolution manipulation. The attacker may impersonate one endpoint
or transparently relay traffic.

**Impact:** Credential theft, session hijacking, data disclosure, or
modification of transactions.

**Defenses:** Properly configured TLS, certificate validation, secure
Wi-Fi, VPNs on untrusted networks where appropriate, HSTS for websites,
secure DNS practices, and avoidance of certificate-warning bypasses.

### 3.14 SQL injection (SQLi)

**What it is:** SQL injection is an application vulnerability in which
untrusted input is interpreted as part of a SQL statement rather than
strictly as data.

**How it works conceptually:** An application constructs a database
query unsafely using user input. Crafted input may change the query's
intended logic. The exact impact depends on the database permissions and
application design.

**Impact:** Unauthorized data access or modification, authentication
bypass, and in severe cases compromise of the application or database
environment.

**Defenses:** Parameterized queries/prepared statements, safe ORM usage,
input validation as a supporting measure, least-privileged database
accounts, secure error handling, code review, and application security
testing. Input filtering alone is not a reliable substitute for
parameterization.

### 3.15 Brute-force attacks

**What it is:** A brute-force attack repeatedly tries possible passwords
or authentication values until one works.

**How it works:** Attempts may be directed at a live login service or
performed against stolen password hashes offline. Password spraying is a
related technique that tries a small number of common passwords across
many accounts to reduce lockout risk.

**Impact:** Account takeover, access to sensitive systems, and potential
privilege escalation.

**Defenses:** Long unique passwords, password managers, MFA, rate
limiting, progressive delays, breached-password screening, secure
password hashing, and alerting on repeated failures. Lockout policies
should be designed carefully to avoid enabling denial-of-service against
users.

### 3.16 Credential stuffing

**What it is:** Credential stuffing uses username/password pairs exposed
in one breach and tests them against other services, relying on password
reuse.

**How it works:** Automated tools attempt previously leaked combinations
across many login portals.

**Impact:** Account takeover, fraud, privacy exposure, and access to
connected services.

**Defenses:** Unique passwords, password managers, MFA,
breached-credential detection, bot detection, rate limits, risk-based
authentication, and monitoring for unusual login patterns.

**Credential stuffing vs. brute force:** brute force guesses
credentials; credential stuffing reuses credentials already obtained
elsewhere. Both can be automated, but the underlying source of the
attempted passwords differs.

### 3.17 Insider threats

**What it is:** An insider threat is risk arising from someone with
legitimate access, such as an employee, contractor, or business partner.
The behavior may be malicious, negligent, or compromised by an external
attacker.

**How it works:** Examples include an employee deliberately copying
customer data, a user accidentally sending a confidential file to the
wrong recipient, or an attacker using a compromised employee account.

**Impact:** Data leakage, fraud, sabotage, intellectual-property theft,
and disruption. Insiders may bypass perimeter defenses because their
access is legitimate.

**Defenses:** Least privilege, separation of duties, access reviews,
data-loss prevention where appropriate, logging and monitoring, secure
offboarding, staff training, clear policies, and fair investigation
processes. Monitoring should be proportionate and respect applicable
privacy and employment requirements.

### 3.18 Threat comparison summary

  -----------------------------------------------------------------------
  Threat                  Primary objective or    Common defensive
                          effect                  emphasis
  ----------------------- ----------------------- -----------------------
  Malware                 Unauthorized or harmful EDR, patching,
                          code execution          application control

  Virus / worm            Infection and           Endpoint security,
                          propagation             patching, segmentation

  Trojan                  Deceptive installation  Trusted software
                          and payload delivery    sources, least
                                                  privilege

  Ransomware              Denial of access and/or Tested backups, EDR,
                          extortion               segmentation, MFA

  Spyware                 Covert information      Endpoint controls,
                          collection              software restrictions

  Phishing family         Manipulate people and   MFA, filtering,
                          steal access or money   verification, training

  DoS / DDoS              Exhaust resources and   Rate limits, traffic
                          disrupt availability    scrubbing, resilience

  MitM                    Intercept or alter      TLS, certificate
                          communications          validation, secure
                                                  networks

  SQL injection           Manipulate database     Parameterized queries,
                          queries                 least privilege

  Brute force             Guess authentication    MFA, rate limits,
                          secrets                 strong passwords

  Credential stuffing     Reuse breached          Unique passwords, MFA,
                          credentials             bot detection

  Insider threat          Misuse or accidental    Least privilege,
                          misuse of trusted       oversight, access
                          access                  reviews
  -----------------------------------------------------------------------

## 4. The CIA Triad

The **CIA triad** is a foundational model for evaluating information
security. It consists of confidentiality, integrity, and availability. A
security incident may affect one, two, or all three.

### 4.1 Confidentiality

**Confidentiality** means information is accessible only to authorized
people, systems, or processes, and is not disclosed to unauthorized
parties.

**Realistic scenario:** A healthcare provider stores patient records in
a database. Only care teams with a legitimate treatment purpose and
authorized administrative staff should access particular records. A
public cloud-storage misconfiguration that exposes the records violates
confidentiality.

**Common threats:**

-   Phishing and credential theft.
-   Unauthorized access and privilege misuse.
-   Data exfiltration and spyware.
-   Misconfigured storage or excessive permissions.
-   Eavesdropping on inadequately protected communications.
-   Lost devices containing unencrypted information.

**Relevant controls:**

-   Access control and least privilege.
-   MFA and strong identity management.
-   Encryption in transit and at rest, with sound key management.
-   Data classification and handling rules.
-   Network segmentation and secure configuration.
-   Data-loss prevention and monitoring where appropriate.
-   Physical security and secure disposal.

Encryption can reduce the consequences of data exposure, but it does not
prevent an authorized, compromised application from accessing decrypted
data.

### 4.2 Integrity

**Integrity** means information and systems remain accurate, complete,
and protected against unauthorized or unintended modification. Integrity
also includes confidence that data came from an expected source and has
not been improperly altered.

**Realistic scenario:** An online retailer stores order totals and
payment status. If an attacker changes an order's total or alters a
payment record without authorization, the integrity of the data has been
compromised even if the database remains available and private.

**Common threats:**

-   SQL injection and unauthorized database writes.
-   Malware that modifies files or system settings.
-   Insider misuse or accidental changes.
-   Compromised software updates or supply chains.
-   Unauthorized changes to logs or configurations.

**Relevant controls:**

-   Role-based access control and separation of duties.
-   Change management and approval workflows.
-   Cryptographic hashes and digital signatures where appropriate.
-   Database constraints, validation, and transaction controls.
-   Version control and protected backups.
-   Audit logs stored with restricted access and integrity protection.
-   Secure software development and code review.

A hash can help detect changes when the expected hash is protected. A
hash stored beside an attacker-modifiable file, without a trusted
reference, may not provide meaningful assurance.

### 4.3 Availability

**Availability** means authorized users can access information and
services when required, within agreed service levels.

**Realistic scenario:** A bank's mobile banking service must remain
accessible during business hours. A DDoS attack or ransomware incident
that prevents customers from viewing balances or making payments affects
availability.

**Common threats:**

-   DoS and DDoS attacks.
-   Ransomware and destructive malware.
-   Hardware failure, power loss, and natural disasters.
-   Resource exhaustion and software defects.
-   Accidental deletion or failed changes.
-   Cloud or third-party service outages.

**Relevant controls:**

-   Redundancy, failover, and resilient architecture.
-   Capacity management, rate limiting, and DDoS protection.
-   Backups and tested restoration procedures.
-   Disaster recovery and business continuity plans.
-   Monitoring, alerting, and incident response.
-   Patch and configuration management.
-   Power, environmental, and physical protections.

Backups support recovery, but they do not by themselves guarantee
continuous availability. Recovery time objectives (RTOs) and recovery
point objectives (RPOs) help define acceptable downtime and data loss.

### 4.4 CIA triad comparison

  -----------------------------------------------------------------------
  Principle         Core question     Example failure   Typical controls
  ----------------- ----------------- ----------------- -----------------
  Confidentiality   Who can see the   Unauthorized      Access control,
                    information?      disclosure of     encryption, MFA
                                      customer records  

  Integrity         Can information   Unauthorized      Change control,
                    be trusted as     change to payment signatures, audit
                    accurate and      data              logs
                    unaltered?                          

  Availability      Can authorized    DDoS outage or    Resilience,
                    users access it   ransomware        backups, DDoS
                    when needed?      shutdown          mitigation
  -----------------------------------------------------------------------

The principles are interdependent. For example, ransomware may make
records unavailable (availability), while data theft before encryption
violates confidentiality and tampering with records affects integrity.

## 5. Additional Security Principles

### 5.1 Authentication

**Authentication** verifies an identity claim: it establishes that a
user, device, or service is who or what it claims to be.

Common authentication factor categories:

-   **Something you know:** password or PIN.
-   **Something you have:** security key, smart card, or authenticator
    device.
-   **Something you are:** biometric characteristic.

Multi-factor authentication (MFA) combines factors from different
categories. Two passwords are not true MFA because both are knowledge
factors. Phishing-resistant methods, such as appropriately deployed
FIDO2/WebAuthn security keys or passkeys, provide stronger protection
against credential phishing than one-time codes alone.

### 5.2 Authorization

**Authorization** determines what an authenticated identity is permitted
to do. Authentication answers "Who are you?"; authorization answers
"What may you access or perform?"

Example: an employee may successfully authenticate to a finance
application but be authorized only to view invoices, not approve
payments.

Authorization models include role-based access control (RBAC),
attribute-based access control (ABAC), and policy-based approaches.

### 5.3 Accountability

**Accountability** means actions can be attributed to an identity or
process and reviewed. It is supported by unique user identities, audit
logs, time synchronization, monitoring, and procedures for reviewing
events.

Shared accounts weaken accountability because it may be difficult to
determine which individual performed an action.

### 5.4 Non-repudiation

**Non-repudiation** provides evidence that can help prevent a party from
credibly denying an action or communication. Digital signatures, trusted
timestamps, transaction records, and controlled identity processes can
contribute.

It is not an absolute guarantee. Its strength depends on key protection,
identity proofing, system integrity, procedures, and applicable legal
context. A digital signature demonstrates use of a private key; it does
not automatically prove which human controlled that key at the time.

### 5.5 Least privilege

The **principle of least privilege** gives each user, process, or
service only the minimum permissions necessary, for only as long as
needed.

Example: a reporting service account should be able to read the required
reporting tables, not administer the database or create new privileged
accounts.

Implementation practices include role-based permissions, just-in-time
elevation, privileged access management, periodic access reviews, and
removal of unused accounts.

### 5.6 Defense in depth

**Defense in depth** uses multiple, complementary security layers so
that failure of one safeguard does not automatically lead to compromise.

For example, a web application may be protected by secure coding, a WAF,
network segmentation, MFA for administrators, EDR on servers,
centralized logging, and tested backups. Layers should be meaningfully
independent; repeating the same weak control in several places is not
robust defense.

### 5.7 Zero Trust fundamentals

**Zero Trust** is a security approach that avoids granting implicit
trust solely because a user or device is inside a network boundary.
Access decisions are made explicitly and continuously informed by
identity, device posture, resource sensitivity, context, and policy.

Core ideas include:

-   Verify explicitly using available identity and context signals.
-   Apply least-privilege access.
-   Assume breach and design to limit blast radius.
-   Protect resources rather than relying only on network location.
-   Continuously monitor access and reassess trust conditions.

Zero Trust is not a single product, nor does it mean "trust nobody" in a
literal sense. It is an architecture and operating model that requires
identity governance, device management, segmentation, telemetry, and
consistent policy enforcement.

## 6. Cybersecurity Frameworks

Frameworks organize security work and provide shared language. They are
not turnkey products and do not guarantee security. Organizations tailor
them to their size, sector, legal obligations, technology, and risk
profile.

## 6.1 NIST Cybersecurity Framework 2.0

### 6.1.1 Overview and purpose

The **NIST Cybersecurity Framework (CSF) 2.0**, published in February
2024, provides a flexible, outcome-based structure for understanding,
assessing, prioritizing, and communicating cybersecurity risk. It is
designed for organizations of different sizes and sectors, not only
critical infrastructure.

CSF 2.0 is organized around six concurrent and continuous **Functions**:

1.  Govern
2.  Identify
3.  Protect
4.  Detect
5.  Respond
6.  Recover

The Functions are not a rigid sequence or a one-time project checklist.
Governance, identification, protection, and detection activities
continue throughout normal operations; response and recovery
capabilities should be prepared in advance and activated when needed.

The Framework Core organizes outcomes into Functions, Categories, and
Subcategories. It does not prescribe one mandatory implementation
method.

### 6.1.2 Govern

**Purpose:** Establish, communicate, and monitor the organization's
cybersecurity risk-management strategy, expectations, roles, and
oversight.

**Practical applications:**

-   Define risk-management policies and risk appetite.
-   Assign cybersecurity responsibilities and decision authority.
-   Integrate cyber risk into enterprise risk management.
-   Assess legal, regulatory, and contractual obligations.
-   Manage cybersecurity risks from suppliers and other third parties.
-   Review performance and adjust strategy.

**Example:** A retailer's leadership approves a policy requiring MFA for
privileged access, defines who may accept high residual risk, and
establishes security requirements for payment-processing suppliers.

Governance makes cybersecurity a business responsibility rather than an
isolated technical function.

### 6.1.3 Identify

**Purpose:** Understand the organization's current cybersecurity risks,
assets, dependencies, and improvement needs.

**Practical applications:**

-   Maintain inventories of hardware, software, data, services, and
    identities.
-   Classify information and identify business-critical processes.
-   Map dependencies on cloud providers and suppliers.
-   Assess vulnerabilities, threats, and business impact.
-   Establish a current understanding of risk and improvement
    priorities.

**Example:** An organization discovers that an old internet-facing
server still stores customer records. It records the asset owner, data
classification, software version, business dependency, and exposure so
the risk can be assessed.

An organization cannot protect assets consistently if it does not know
they exist.

### 6.1.4 Protect

**Purpose:** Use safeguards to manage cybersecurity risks and reduce the
likelihood or impact of adverse events.

**Practical applications:**

-   Manage identities, authentication, and access permissions.
-   Train employees and contractors.
-   Protect data through encryption and handling controls.
-   Secure endpoints, applications, and infrastructure.
-   Maintain secure configurations and patch systems.
-   Use backups, resilience, and protective technologies.

**Example:** The organization deploys MFA for remote access, restricts
administrator privileges, patches the exposed server, and encrypts
sensitive data.

Protection reduces risk but cannot prevent every incident; detection and
response remain necessary.

### 6.1.5 Detect

**Purpose:** Find and analyze possible cybersecurity attacks,
compromises, and other adverse events in a timely manner.

**Practical applications:**

-   Collect and centralize relevant logs.
-   Monitor endpoint, identity, network, cloud, and application
    activity.
-   Establish baselines and alert on suspicious deviations.
-   Triage alerts and correlate events across systems.
-   Test detection coverage and tune noisy rules.

**Example:** A security operations team receives alerts for repeated
failed logins followed by a successful sign-in from an unusual location
and an unexpected mailbox forwarding rule.

Detection is more than generating alerts: signals must be assessed to
determine whether they indicate a real incident.

### 6.1.6 Respond

**Purpose:** Take action regarding a detected cybersecurity incident to
contain, analyze, communicate, and manage its effects.

**Practical applications:**

-   Validate and classify incidents.
-   Activate incident-response roles and playbooks.
-   Contain affected endpoints or accounts.
-   Preserve evidence and maintain a timeline.
-   Eradicate malicious access and coordinate communications.
-   Meet applicable legal, regulatory, and contractual notification
    requirements.

**Example:** The response team disables a compromised account, revokes
active sessions, isolates an affected laptop, blocks malicious
infrastructure, and investigates whether data was accessed or removed.

Response actions should be coordinated and documented. Poorly planned
containment can destroy evidence or interrupt critical operations
unnecessarily.

### 6.1.7 Recover

**Purpose:** Restore assets and services affected by an incident and
improve resilience based on lessons learned.

**Practical applications:**

-   Prioritize restoration using business impact and recovery
    objectives.
-   Rebuild compromised systems from trusted sources.
-   Restore clean backups and validate their integrity.
-   Monitor restored systems for signs of reinfection.
-   Communicate service status to affected stakeholders.
-   Conduct lessons-learned reviews and update plans.

**Example:** After confirming that a clean backup is available, the
organization rebuilds affected servers, restores validated data, rotates
credentials, tests business workflows, and gradually returns services to
production.

Recovery is not complete merely because a server is online; the
organization must verify that the restored environment is secure and
operational.

### 6.1.8 CSF implementation concepts

Organizations can use several CSF concepts to make the framework
practical:

-   **Organizational Profile:** describes current or target
    cybersecurity outcomes in the context of mission, stakeholders,
    requirements, and risk.
-   **Current Profile:** records outcomes currently being achieved.
-   **Target Profile:** describes desired outcomes based on priorities
    and risk.
-   **Tiers:** characterize the rigor of an organization's cybersecurity
    risk-governance and management practices (Partial, Risk Informed,
    Repeatable, Adaptive). They are not maturity scores for individual
    technologies.
-   **Community Profiles:** reusable, sector- or community-focused
    selections of CSF outcomes.

A common improvement cycle is to understand the current state, define a
target state, analyze gaps, prioritize actions, assign owners and
resources, and measure progress.

## 6.2 MITRE ATT&CK

### 6.2.1 Introduction and purpose

**MITRE ATT&CK** (Adversarial Tactics, Techniques, and Common Knowledge)
is a publicly available knowledge base and taxonomy of observed
adversary behavior. It helps defenders describe what attackers do during
intrusions using a common vocabulary.

ATT&CK is behavior-focused. It is not a compliance framework, a complete
risk-management program, or a guarantee that every attack will appear in
the matrix. Its content evolves as research and observations change.

The **Enterprise ATT&CK Matrix** covers adversary behavior across
enterprise environments and platforms such as Windows, macOS, Linux,
cloud services, identity providers, SaaS, network devices, and
containers. ATT&CK also has other domains, including Mobile and ICS.

### 6.2.2 Tactics, techniques, sub-techniques, and procedures

These terms have distinct meanings:

-   **Tactic:** the adversary's tactical goal---the *why* behind an
    action. Examples include gaining initial access, stealing
    credentials, or exfiltrating data.
-   **Technique:** the general method used to achieve a tactical
    goal---the *how*. For example, phishing is a technique used to gain
    initial access or obtain information, depending on the specific
    behavior.
-   **Sub-technique:** a more specific version of a technique, adding
    detail about how the behavior is carried out. For example, a
    technique may be divided into specific command or protocol variants.
-   **Procedure:** the concrete implementation observed in a particular
    intrusion, such as the exact command, script, tool, or sequence used
    by an adversary.

A tactic is not a technique. A technique may be relevant to more than
one tactic because the same behavior can support different goals in
different contexts.

### 6.2.3 Enterprise ATT&CK Matrix

The Enterprise Matrix arranges techniques under the tactics they
support. Each technique has a unique ATT&CK identifier (for example,
`T1566` for Phishing). Sub-techniques use a dotted identifier (for
example, `T1566.001` for Spearphishing Attachment).

The matrix is useful for exploring adversary behavior, mapping observed
activity, identifying detection opportunities, and communicating
threat-informed defense priorities. It is not a mandatory chronological
attack sequence: adversaries may skip tactics, revisit them, or perform
activities in a different order.

### 6.2.4 The 14-tactic Enterprise model and current taxonomy note

Many established learning materials and older Enterprise Matrix
references describe **14 tactics**, including **Defense Evasion**. The
current live MITRE Enterprise tactics page has evolved and lists **15
tactics**, including **Stealth** and **Defense Impairment** as separate
tactical goals rather than presenting the older single Defense Evasion
column. Because ATT&CK is actively maintained, users should verify
tactic names and identifiers against the live official matrix before
using them in a detection engineering or threat-intelligence
deliverable.

The following section explains the **traditional 14-tactic Enterprise
model** requested in many foundational curricula. It preserves the
established Defense Evasion tactic and does not silently mix it with the
newer live taxonomy.

### 6.2.5 Traditional 14 Enterprise tactics with practical examples

  -------------------------------------------------------------------------
                     \# Tactic           Adversary goal   Illustrative
                                                          example
  --------------------- ---------------- ---------------- -----------------
                      1 Reconnaissance   Gather           Search public
                                         information to   websites and job
                                         plan an          postings to learn
                                         operation.       employee names,
                                                          technologies, and
                                                          suppliers.

                      2 Resource         Establish        Register
                        Development      resources to     look-alike
                                         support an       domains, obtain
                                         operation.       infrastructure,
                                                          or prepare
                                                          malicious
                                                          tooling.

                      3 Initial Access   Get into the     Send a convincing
                                         target           phishing message
                                         environment.     or exploit an
                                                          exposed service.

                      4 Execution        Run malicious    Cause a malicious
                                         code or          script or payload
                                         commands.        to execute on a
                                                          compromised
                                                          endpoint.

                      5 Persistence      Maintain access  Create an
                                         across           unauthorized
                                         interruptions    scheduled task or
                                         such as reboots  modify an account
                                         or credential    configuration.
                                         changes.         

                      6 Privilege        Gain             Exploit a local
                        Escalation       higher-level     weakness or abuse
                                         permissions.     an
                                                          over-privileged
                                                          service to obtain
                                                          administrator
                                                          access.

                      7 Defense Evasion  Avoid detection  Obfuscate
                                         or bypass        malicious
                                         security         activity, abuse
                                         controls.        trusted tools, or
                                                          tamper with
                                                          security
                                                          settings.

                      8 Credential       Steal or obtain  Capture
                        Access           account          credentials
                                         credentials.     through a fake
                                                          sign-in page or
                                                          extract secrets
                                                          from an exposed
                                                          store.

                      9 Discovery        Learn about      Enumerate domain
                                         systems,         users, hosts,
                                         accounts, and    shares, and
                                         the environment. installed
                                                          security tools.

                     10 Lateral Movement Move from one    Use compromised
                                         system or        credentials to
                                         account to       access a file
                                         another.         server from an
                                                          initial endpoint.

                     11 Collection       Gather data of   Stage selected
                                         interest.        finance documents
                                                          or customer
                                                          records for later
                                                          transfer.

                     12 Command and      Communicate with Use outbound web
                        Control          compromised      traffic to
                                         systems to       exchange commands
                                         direct them.     and results with
                                                          attacker
                                                          infrastructure.

                     13 Exfiltration     Steal data from  Transfer
                                         the environment. collected
                                                          documents to an
                                                          external
                                                          destination.

                     14 Impact           Manipulate,      Encrypt files,
                                         interrupt, or    delete data,
                                         destroy systems  disrupt services,
                                         and data.        or alter business
                                                          records.
  -------------------------------------------------------------------------

These examples are conceptual. The same activity may map to different
techniques depending on the evidence and exact behavior. Analysts should
use the ATT&CK technique descriptions and detection guidance rather than
infer a technique from a broad label alone.

### 6.2.6 How the current 15-tactic live Enterprise taxonomy differs

The current official Enterprise tactics page lists:

1.  Reconnaissance
2.  Resource Development
3.  Initial Access
4.  Execution
5.  Persistence
6.  Privilege Escalation
7.  Stealth
8.  Defense Impairment
9.  Credential Access
10. Discovery
11. Lateral Movement
12. Collection
13. Command and Control
14. Exfiltration
15. Impact

This is a taxonomy update, not a reason to assume that older reports
using the traditional 14-tactic model are automatically invalid. When
producing new work, use a stated ATT&CK version and the corresponding
matrix. Avoid mixing technique mappings across versions without checking
for changes.

### 6.2.7 Practical applications in threat detection and SOC operations

A Security Operations Center (SOC) can use ATT&CK to:

-   **Classify observed behavior:** map evidence such as suspicious
    PowerShell execution, credential dumping alerts, or remote-service
    activity to relevant techniques.
-   **Develop detections:** identify telemetry sources and analytics
    that could reveal specific behaviors.
-   **Assess coverage:** compare deployed detections with techniques
    relevant to the organization's threat model.
-   **Threat hunt:** formulate hypotheses such as "an attacker may be
    using valid accounts to move laterally" and search endpoint,
    identity, and network data.
-   **Enrich incident reports:** describe behavior in a consistent,
    analyst-friendly format.
-   **Emulate adversary behavior safely:** plan controlled purple-team
    exercises and validate whether detections work.
-   **Prioritize improvements:** focus on high-risk techniques that are
    plausible in the organization's environment.

**Illustrative SOC workflow:**

1.  An endpoint alert reports an unusual script interpreter launched by
    an office application.
2.  The analyst validates the process tree, command-line details, user,
    host, and timestamp.
3.  The observed behavior is mapped to the most specific applicable
    ATT&CK technique and sub-technique.
4.  The analyst checks related identity, DNS, proxy, and endpoint events
    for follow-on activity.
5.  The team determines whether the event is benign, suspicious, or part
    of a confirmed incident.
6.  A detection gap is documented, tested, and improved.

ATT&CK mapping is an analytical aid, not proof of malicious intent. A
technique can also be used by administrators and legitimate software.

## 6.3 NIST CSF 2.0 and MITRE ATT&CK Compared

  -----------------------------------------------------------------------
  Dimension               NIST CSF 2.0            MITRE ATT&CK
  ----------------------- ----------------------- -----------------------
  Primary purpose         Organize and            Describe adversary
                          communicate             behavior and support
                          cybersecurity           threat-informed defense
                          risk-management         
                          outcomes                

  Main focus              Organizational risk and Tactics, techniques,
                          security capabilities   sub-techniques, and
                                                  procedures

  Structure               Six Functions,          Matrices organized by
                          Categories, and         tactics and techniques
                          Subcategories           

  Typical users           Leadership, risk        SOC analysts, threat
                          owners, security        hunters, detection
                          managers, practitioners engineers, red/purple
                                                  teams

  Main question           What cybersecurity      What behaviors might an
                          outcomes should the     adversary use, and how
                          organization achieve?   can we detect or
                                                  disrupt them?

  Prescriptiveness        Outcome-based and       Descriptive knowledge
                          flexible                base; not a control
                                                  standard

  Typical output          Current/Target          Technique mappings,
                          Profiles, gap analysis, detection coverage,
                          prioritized improvement hunt hypotheses,
                          plan                    adversary emulation
                                                  plans
  -----------------------------------------------------------------------

### How they complement each other

The frameworks work well together because they solve different problems:

-   Use **NIST CSF 2.0** to organize the overall cybersecurity program,
    establish governance, identify risk, and prioritize desired
    outcomes.
-   Use **MITRE ATT&CK** to understand plausible adversary behaviors and
    translate threat knowledge into detection, hunting, and response
    activities.
-   Use **NIST SP 800-53** or another suitable control catalog to select
    and tailor specific safeguards.
-   Use incident-response guidance such as **NIST SP 800-61 Rev. 3** to
    integrate response activities into risk management.

**Example:** A CSF Detect outcome may lead an organization to improve
monitoring of identity activity. ATT&CK can help identify relevant
adversary behaviors---such as credential access, valid-account use, or
lateral movement---and the telemetry needed to detect them. The
organization then selects controls and analytics, tests them, and tracks
improvement through its CSF Profile.

## 7. Security Controls

A **security control** is a safeguard or countermeasure intended to
protect assets, manage risk, or support detection and response. Controls
may be administrative, technical, or physical. A single control can
serve more than one purpose.

### 7.1 Preventive controls

**Purpose:** Stop or reduce the likelihood of an unwanted event before
it occurs.

Examples:

-   MFA and access restrictions.
-   Secure configuration and timely patching.
-   Network segmentation and firewalls.
-   Security awareness training.
-   Application allowlisting.
-   Physical access badges and locked server rooms.

### 7.2 Detective controls

**Purpose:** Discover or alert on events that have occurred or are in
progress.

Examples:

-   SIEM correlation and alerting.
-   EDR behavioral detection.
-   Intrusion detection systems.
-   Audit-log review.
-   File-integrity monitoring.
-   Physical intrusion alarms.

Detection controls do not necessarily stop an attack; they provide
information that enables investigation and response.

### 7.3 Corrective controls

**Purpose:** Reduce the effect of an incident and restore a secure or
acceptable state after a problem is identified.

Examples:

-   Remove malware and rebuild a compromised endpoint.
-   Restore data from a verified backup.
-   Revoke exposed credentials and rotate secrets.
-   Apply a security patch after identifying an exploited vulnerability.
-   Repair a misconfiguration and validate the correction.

Corrective actions often overlap with response and recovery activities.

### 7.4 Deterrent controls

**Purpose:** Discourage attempted violations by making consequences or
detection more apparent.

Examples:

-   Visible security monitoring notices.
-   Warning banners on systems.
-   Physical security patrols and access signage.
-   Enforced disciplinary policies communicated to personnel.

A deterrent may discourage some behavior, but it cannot guarantee
prevention.

### 7.5 Compensating controls

**Purpose:** Provide an alternative safeguard when a preferred control
cannot be implemented or is not currently feasible. The alternative
should address the same risk as effectively as practical and be formally
assessed.

Examples:

-   If a legacy application cannot support MFA, restrict access through
    a hardened gateway that enforces MFA, limit source networks, and
    monitor sessions.
-   If a system cannot be patched immediately because of operational
    constraints, isolate it, restrict access, increase monitoring, and
    establish a time-bound remediation plan.

Compensating controls are not a permanent excuse to ignore remediation.
Their residual risk and expiration or review date should be documented.

### 7.6 Control selection

Controls should be selected based on risk, business context, legal
requirements, architecture, and operational feasibility. Organizations
should consider whether controls are designed correctly, implemented as
intended, and operating effectively. A policy that exists only on paper
does not provide the same protection as a policy consistently followed
and verified.

## 8. People, Processes and Technology

An effective cybersecurity program depends on three mutually reinforcing
elements.

### 8.1 People

People make decisions, operate systems, interpret alerts, approve
access, and respond to incidents. They can strengthen security through
awareness and sound judgment, or introduce risk through mistakes and
unsafe practices.

Important practices include:

-   Role-appropriate security education.
-   Clear ownership and escalation paths.
-   Background checks and personnel processes where lawful and
    appropriate.
-   A culture that encourages prompt reporting.
-   Management support and adequate staffing.
-   Separation of duties for sensitive activities.

Security awareness should be practical and continuous, not limited to a
once-a-year presentation.

### 8.2 Processes

Processes turn intentions into repeatable activities. They define who
does what, when, and how evidence is recorded.

Examples include:

-   Risk assessment and risk acceptance.
-   Asset and vulnerability management.
-   Change and configuration management.
-   Joiner-mover-leaver identity processes.
-   Incident response and business continuity.
-   Supplier risk management.
-   Backup testing and access reviews.
-   Security testing and lessons-learned reviews.

A well-written process must be realistic, assigned to an owner,
communicated, and tested.

### 8.3 Technology

Technology provides mechanisms to enforce policy, collect evidence, and
protect systems.

Examples include:

-   Firewalls, secure gateways, and network segmentation.
-   EDR, anti-malware, and endpoint management.
-   Identity and access management (IAM), MFA, and privileged access
    management.
-   Encryption and key management.
-   SIEM, log management, and security analytics.
-   Vulnerability scanners and configuration assessment tools.
-   Backup, recovery, and resilience platforms.

Technology is not a substitute for people and processes. A SIEM without
useful log sources, trained analysts, and an escalation process may
generate little security value.

### 8.4 Bringing the three together

Consider employee offboarding:

-   **People:** the manager and HR notify IT when an employee leaves.
-   **Process:** a documented workflow requires timely access
    revocation, asset return, and ownership transfer.
-   **Technology:** IAM disables accounts, sessions are revoked, devices
    are recovered or wiped, and relevant actions are logged.

If any one element fails, former access may remain active. Strong
cybersecurity depends on all three working together.

## 9. Practical Application: Hypothetical Incident

### 9.1 Scenario

A fictional mid-sized online retailer, **Northstar Retail**, uses a
cloud-hosted customer portal, a corporate identity provider, employee
laptops, and a finance file server. An employee in the finance
department receives an email that appears to come from a supplier and
opens a link to a fake document-sharing sign-in page. The employee
enters corporate credentials.

The attacker uses the stolen credentials to access the employee's cloud
account. The account has no phishing-resistant MFA. The attacker creates
an inbox rule, accesses shared files, and attempts to reach the finance
file server. A monitoring system later detects an unusual sign-in and
suspicious file-access activity.

This scenario is fictional and is provided to demonstrate analysis, not
to describe a real engagement.

### 9.2 Identify affected assets

  -----------------------------------------------------------------------
  Asset                   Why it matters          Potential impact
  ----------------------- ----------------------- -----------------------
  Employee identity       Provides access to      Unauthorized account
  account                 cloud resources         use

  Employee laptop         May contain sessions,   Malware or session
                          files, and business     compromise
                          data                    

  Corporate email         Contains business       Fraud, impersonation,
                          communications and can  information disclosure
                          enable further phishing 

  Finance file server     Stores sensitive        Confidentiality and
                          invoices and financial  integrity impact
                          records                 

  Customer portal and     Critical business       Wider access or service
  identity provider       services and            disruption
                          authentication          
                          dependencies            

  Audit and security logs Support detection and   Loss of visibility if
                          investigation           altered or unavailable
  -----------------------------------------------------------------------

The team should identify owners, data classifications, dependencies,
system locations, and whether the attacker accessed or changed each
asset.

### 9.3 Recognize threats and vulnerabilities

**Threat actor:** an unknown external actor using stolen credentials.
The actor's identity and motivation should not be assumed without
evidence.

**Threats:**

-   Credential theft through phishing.
-   Unauthorized use of a valid account.
-   Mailbox manipulation and internal impersonation.
-   Access to confidential finance information.
-   Potential lateral movement and data exfiltration.

**Potential vulnerabilities or control weaknesses:**

-   Employee susceptibility to a convincing phishing message.
-   Lack of phishing-resistant MFA on the account.
-   Insufficient restrictions on mailbox-rule creation or external
    forwarding.
-   Excessive access to finance shares.
-   Inadequate alerting for unusual sign-ins or file access.

The phishing message is the delivery method; the stolen credential is
the compromised authentication secret; the absence of stronger
authentication is a control weakness. These should not be conflated.

### 9.4 Assess potential risks

A simple qualitative assessment could look like this:

  Risk                                         Likelihood (illustrative)   Impact (illustrative)   Priority
  -------------------------------------------- --------------------------- ----------------------- --------------
  Unauthorized use of employee cloud account   High                        High                    High
  Disclosure of finance documents              Medium--High                High                    High
  Modification of payment instructions         Medium                      High                    High
  Spread to additional systems                 Medium                      High                    High
  Customer portal disruption                   Low--Medium                 High                    Medium--High

These ratings are hypothetical and should be refined using actual
evidence, asset criticality, threat intelligence, exposure, and existing
controls. The organization should also consider legal, contractual,
privacy, and reporting obligations.

### 9.5 Apply the CIA triad

-   **Confidentiality:** Determine whether the attacker viewed,
    downloaded, or forwarded finance records. Revoke unauthorized
    sessions, restrict access, and assess any disclosure.
-   **Integrity:** Check for changed mailbox rules, modified files,
    altered payment instructions, and suspicious configuration changes.
    Compare records with trusted versions and review audit trails.
-   **Availability:** Determine whether systems or accounts were
    disabled or disrupted. Maintain critical finance operations through
    approved fallback procedures while preserving evidence.

The team should not assume that confidentiality is the only concern
simply because the initial event involved stolen credentials.

### 9.6 Map observed behavior to MITRE ATT&CK

The following mappings are illustrative. Exact technique selection
depends on evidence, platform, ATT&CK version, and the specific behavior
observed.

  -----------------------------------------------------------------------
  Observed or suspected   Traditional tactic      Candidate ATT&CK
  behavior                context                 mapping
  ----------------------- ----------------------- -----------------------
  Deceptive email used to Initial Access /        Phishing (`T1566`) may
  obtain credentials      Credential Access       apply to the delivery
                                                  behavior; credential
                                                  capture may require a
                                                  separate technique
                                                  based on evidence

  Stolen employee account Initial Access /        Valid Accounts
  used to sign in         Persistence or other    (`T1078`)
                          context                 

  Mailbox rule created to Persistence /           Email-specific rule
  hide or redirect        Collection or           technique should be
  messages                defense-related context selected from the
                          depending on behavior   relevant ATT&CK version
                                                  and platform

  Attacker inspects       Discovery               Specific discovery
  accessible files and                            technique based on the
  systems                                         commands and resources
                                                  observed

  Access to finance       Lateral Movement        A technique such as
  server from compromised                         Remote Services
  identity                                        (`T1021`) only if the
                                                  observed access method
                                                  matches

  Files gathered for      Collection              Data from local system
  transfer                                        or network share
                                                  technique, depending on
                                                  evidence

  Data sent outside the   Exfiltration            Exfiltration Over Web
  organization                                    Service (`T1567`) only
                                                  if the transfer method
                                                  supports that mapping
  -----------------------------------------------------------------------

**Analyst caution:** Do not assign a technique merely because it sounds
plausible. Preserve evidence such as sign-in logs, process trees,
mailbox audit records, network telemetry, and file-access events. Use
the official technique pages to validate mappings. Where behavior is
suspected but unconfirmed, label it as a hypothesis.

### 9.7 Apply the NIST CSF 2.0 Functions

  -----------------------------------------------------------------------
  CSF Function                        Application to the scenario
  ----------------------------------- -----------------------------------
  Govern                              Confirm incident authority,
                                      escalation paths, supplier
                                      communication rules, risk
                                      tolerance, and notification
                                      responsibilities.

  Identify                            Determine affected identities,
                                      devices, cloud resources, finance
                                      data, business processes, and
                                      dependencies.

  Protect                             Enforce phishing-resistant MFA,
                                      reduce file permissions, harden
                                      mailbox settings, train staff, and
                                      improve email protections.

  Detect                              Correlate identity, mailbox,
                                      endpoint, and file-server logs;
                                      alert on unusual sign-ins,
                                      suspicious rules, and abnormal data
                                      access.

  Respond                             Validate the incident, disable or
                                      secure the account, revoke
                                      sessions, isolate affected devices
                                      if necessary, preserve evidence,
                                      investigate scope, and communicate
                                      with stakeholders.

  Recover                             Restore trusted configurations,
                                      validate affected records, rotate
                                      credentials and tokens, return
                                      services to normal, and monitor for
                                      recurrence.
  -----------------------------------------------------------------------

All six Functions are relevant. Governance and protection should already
exist before the incident, while response and recovery are activated and
informed by the investigation.

### 9.8 Recommend security controls

**Immediate containment and investigation**

1.  Disable or restrict the compromised identity according to the
    incident-response plan.
2.  Revoke active sessions, refresh tokens, and exposed credentials as
    appropriate.
3.  Remove unauthorized mailbox rules and inspect forwarding settings.
4.  Isolate a device if evidence suggests it is compromised.
5.  Preserve relevant logs and evidence with timestamps and
    chain-of-custody procedures.
6.  Review file access, external sharing, and payment changes.
7.  Determine whether other accounts received or acted on the phishing
    message.

**Short-term risk reduction**

-   Enforce MFA, prioritizing phishing-resistant methods for high-risk
    users.
-   Review privileged and finance access using least privilege.
-   Alert on suspicious mailbox rules, impossible or anomalous sign-ins,
    and unusual downloads.
-   Strengthen email authentication and filtering.
-   Ensure centralized logging covers identity, endpoint, email, and
    file activity.
-   Verify backups and restoration procedures.

**Long-term improvement**

-   Conduct targeted phishing and social-engineering education.
-   Establish a repeatable access-review process.
-   Improve supplier payment-change verification.
-   Test incident-response playbooks with tabletop exercises.
-   Use ATT&CK to evaluate detection coverage for relevant identity and
    cloud behaviors.
-   Use CSF Profiles to track current and target security outcomes.

### 9.9 Lessons learned

A mature review asks not only "Who clicked the link?" but also:

-   Why could a single credential provide access to sensitive resources?
-   Which identity and file-access signals were available, and were they
    monitored?
-   Were permissions broader than the employee's role required?
-   Could the incident have been detected earlier?
-   Were response roles and communication paths clear?
-   Were backups, logs, and evidence protected?
-   Which improvements will be assigned, funded, and tested?

The purpose of lessons learned is to improve the system and its
controls, not simply to assign blame.

## 10. Key Takeaways and Conclusion

Cybersecurity is a continuous, risk-based discipline that protects the
information and services on which organizations depend. Its foundations
can be summarized as follows:

1.  **Know what matters.** Identify information, systems, identities,
    services, and dependencies before deciding how to protect them.
2.  **Understand the risk chain.** Threat actors may exploit
    vulnerabilities through attack vectors; the resulting risk depends
    on likelihood, impact, exposure, and safeguards.
3.  **Protect the CIA triad.** Confidentiality, integrity, and
    availability provide a practical lens for evaluating security
    requirements and incident consequences.
4.  **Use layered principles.** Authentication, authorization,
    accountability, least privilege, defense in depth, and Zero Trust
    help shape secure architecture and operations.
5.  **Choose controls based on risk.** Preventive, detective,
    corrective, deterrent, and compensating controls have different
    purposes and often work together.
6.  **Use frameworks for different jobs.** NIST CSF 2.0 organizes
    organizational cybersecurity risk outcomes; MITRE ATT&CK describes
    adversary behavior and supports threat-informed detection and
    response.
7.  **Integrate people, processes, and technology.** Tools alone cannot
    create a dependable security program.
8.  **Prepare before incidents happen.** Logging, response plans, tested
    backups, defined authority, and practiced communications reduce the
    cost and confusion of an incident.

These fundamentals support progression into several cybersecurity
specialties:

-   **Vulnerability assessment:** understand assets, weaknesses,
    exploitability, risk, and remediation priorities.
-   **Network security:** understand attack surfaces, segmentation,
    secure protocols, traffic monitoring, and availability protections.
-   **SOC operations:** interpret alerts, investigate events, correlate
    telemetry, and map adversary behavior to ATT&CK.
-   **Threat intelligence:** assess threat actors, campaigns,
    indicators, tactics, techniques, and the confidence of attribution.
-   **Incident response:** scope incidents, preserve evidence, contain
    threats, eradicate persistence, recover services, and improve
    controls.

A strong cybersecurity practitioner continually connects technical
observations to business impact and risk. Foundational knowledge
provides the vocabulary and reasoning needed to make those connections.

> **Educational-purpose disclaimer:** This document is an independent
> learning resource. It is not legal, compliance, or incident-response
> advice. Frameworks and ATT&CK content evolve; consult the official
> publications and current knowledge base when applying them to a real
> environment. Examples are hypothetical and do not represent claims of
> practical implementation or professional certification.

## 11. Official References and Further Reading

The following primary sources are useful for deeper study. Prefer the
official publication or live knowledge base when checking definitions,
identifiers, and version changes.

### NIST

1.  [The NIST Cybersecurity Framework (CSF) 2.0 --- official publication
    (CSWP 29)](https://doi.org/10.6028/NIST.CSWP.29)\
    The primary reference for the six Functions, Framework Core,
    Profiles, and implementation concepts.

2.  [NIST Cybersecurity Framework 2.0 --- official landing
    page](https://www.nist.gov/cyberframework)\
    Framework resources, downloads, and supporting material.

3.  [NIST CSF Frequently Asked
    Questions](https://www.nist.gov/cyberframework/faqs)\
    Clarifications on Framework components, use, and implementation.

4.  [NIST SP 800-61 Rev. 3 --- Incident Response Recommendations and
    Considerations for Cybersecurity Risk
    Management](https://doi.org/10.6028/NIST.SP.800-61r3)\
    Guidance integrating incident response with CSF 2.0 risk management.
    Published April 2025; supersedes SP 800-61 Rev. 2.

5.  [NIST SP 800-53 Rev. 5 --- Security and Privacy Controls for
    Information Systems and
    Organizations](https://doi.org/10.6028/NIST.SP.800-53r5)\
    A broad catalog of security and privacy controls that can be
    tailored to organizational context.

6.  [NIST SP 800-30 Rev. 1 --- Guide for Conducting Risk
    Assessments](https://doi.org/10.6028/NIST.SP.800-30r1)\
    Guidance on preparing for, conducting, communicating, and
    maintaining risk assessments.

7.  [NIST SP 800-63B --- Digital Identity Guidelines: Authentication and
    Authenticator
    Management](https://pages.nist.gov/800-63-4/sp800-63b.html)\
    Guidance on digital authentication and authenticator management.
    Consult the current revision and related volumes.

8.  [NIST SP 800-207 --- Zero Trust
    Architecture](https://doi.org/10.6028/NIST.SP.800-207)\
    Foundational NIST publication describing Zero Trust architecture.

### MITRE ATT&CK

9.  [MITRE ATT&CK --- Enterprise
    Matrix](https://attack.mitre.org/matrices/enterprise/)\
    The live Enterprise matrix, platforms, tactics, and techniques.

10. [MITRE ATT&CK --- Enterprise
    Tactics](https://attack.mitre.org/tactics/enterprise/)\
    Official tactic definitions and identifiers. Check this page for
    current taxonomy changes.

11. [MITRE ATT&CK ---
    Techniques](https://attack.mitre.org/techniques/enterprise/)\
    Official Enterprise technique and sub-technique reference pages.

12. [MITRE ATT&CK
    Navigator](https://mitre-attack.github.io/attack-navigator/)\
    A tool for visualizing ATT&CK coverage, creating layers, and
    supporting analysis.

13. [MITRE ATT&CK Getting Started](https://attack.mitre.org/resources/)\
    Official resources for learning and applying ATT&CK.

### Further foundational resources

14. [CISA --- Secure Our World](https://www.cisa.gov/secure-our-world)\
    Practical guidance on phishing, passwords, MFA, and software
    updates.

15. [OWASP Top 10](https://owasp.org/www-project-top-ten/)\
    Awareness resource for major web application security risk
    categories, including injection.

16. [CIS Critical Security
    Controls](https://www.cisecurity.org/controls)\
    Prioritized safeguards that organizations can use to improve cyber
    defense.

------------------------------------------------------------------------

*Document title: Cybersecurity Fundamentals: Foundational Concepts,
Threat Types and Security Frameworks*\
*Suggested repository path: `Cybersecurity-Fundamentals.md`*
