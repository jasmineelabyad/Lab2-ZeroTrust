# ZT-Policy-Profile.md

## 1. ZTA Component Definitions

**Policy Engine (PE)**  
The Policy Engine is the decision making brain of a Zero Trust Architecture. Its main role is to evaluate access requests by analyzing security signals such as who the user is, the condition of their device, and where they are connecting from. Based on predefined policies and real-time context, the Policy Engine decides whether access should be approved or denied. It does not enforce access itself it only makes the decision.

**Policy Administrator (PA)**  
The Policy Administrator acts as the rule setter and coordinator within Zero Trust. It is responsible for translating the Policy Engine’s decision into action by configuring access permissions, issuing authentication tokens, or triggering session setup. The PA ensures that the rules defined by security leadership are properly applied to systems and users.

**Policy Enforcement Point (PEP)**  
The Policy Enforcement Point is the gatekeeper that sits directly in front of the protected resource. Its function is to enforce the decision made by the Policy Engine by either allowing or blocking access. The PEP does not make decisions it simply enforces them in real time by controlling traffic to applications, databases, or services.

---

## 2. Core Principle Application

**Chosen ZT Core Principle: Verify Explicitly**

The principle of *Verify Explicitly* means that trust is never assumed and every access request must be validated using multiple security signals. At the Golden State Water Treatment Facility, the Policy Engine enforces this principle by explicitly verifying contextual information before granting access to the HR Employee PII Database.

For example, when an HR analyst attempts to access employee background check records, the Policy Engine evaluates their verified identity, confirms that their device meets security requirements, and checks that the request originates from an approved corporate network. Only if all required signals meet policy conditions does the Policy Engine issue an approval decision.

---

## 3. Simplified Policy Table

| **Policy Requirement (Signal)** | **Condition to be Met by User** | **Action if Condition is Met** |
|--------------------------------|--------------------------------|-------------------------------|
| User Identity | User is authenticated with corporate credentials and assigned an HR role | Grant Access |
| Device Posture | Device is company-managed and compliant with security updates | Grant Access |
| Network Context | Connection originates from the internal corporate network or approved VPN | Grant Access |

---

## 4. Submission Details

# Git Repository Metadata

**Project:** Lab 2 - Zero Trust Policy  
**Filename:** ZT-Policy-Profile.md  
**Commit Message:** Added Zero Trust policy profile for HR PII database – https://github.com/jasmineelabyad/Lab2-ZeroTrust  
**D**
