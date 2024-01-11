# Security Risk Analysis

## Table of Contents

1. [Executive Summary](#executive-summary)  
2. [Introduction](#introduction)  
   2.1 [Purpose](#purpose)  
   2.2 [Scope of this Risk Assessment](#scope-of-this-risk-assessment)  
3. [Risk Assessment Approach](#risk-assessment-approach)  
   3.1 [Participants](#participants)  
   3.2 [Techniques Used](#techniques-used)  
   3.3 [Risk Model](#risk-model)  
4. [System Characterization](#system-characterization)  
   4.1 [Technology Components – The Protection Lab Company (TPL)](#technology-components--the-protection-lab-company-tpl)  
   4.2 [Physical Location(s)](#physical-locations)  
   4.3 [Data Used by System](#data-used-by-system)  
   4.4 [Users – Rank Based](#users--rank-based)  
   4.5 [Flow Diagram – Risk Assessment Activities](#flow-diagram--risk-assessment-activities)  
5. [Risk Assessment Results](#risk-assessment-results)

## Executive Summary

Factors such as size, growth rate, resources, and asset portfolio affect the depth of risk assessment models. Organizations can carry out generalized assessments when experiencing budget or time constraints. However, generalized assessments don’t necessarily provide detailed mappings between assets, associated threats, identified risks, impact, and mitigating controls. To highlight high-risk findings, there are six simple steps in the risk management process: identify your risks; analyze the risks; control the risks; monitor those risks; improve your risk management, and report progress.

## 1. Introduction

### 1.1 Purpose

IT enterprise security risk assessments are performed to allow organizations to assess, identify and modify their overall security posture and to enable security, operations, organizational management, and other personnel to collaborate and view the entire organization from an attacker's perspective.

### 1.2 Scope of this Risk Assessment

The scope of risk assessment identifies the various information assets that could be affected by a cyber-attack (such as hardware, systems, laptops, customer data, and intellectual property), and then identifies the various risks that could affect those assets. Also, a risk assessment is intended to estimate potential human health and environmental risks posed by current and potential future conditions assuming no further remediation of the Facility.

## 2. Risk Assessment Approach

### 2.1 Participants

**Role** | **Participant**
--- | ---
System Owner | The Protection Lab
System Custodian | The Protection Lab
Security Administrator | 
Database Administrator | 
Network Administrator | 
Risk Assessment Administrator | 

### 2.2 Techniques Used

**Technique** | **Description**
--- | ---
Risk Assessment | Assessing risk from Tiers: 1. the Organization 2. Mission/ Business 3. Information Systems. Risk Assessment Process: The four steps for assessing risk: 1. Prepare for Assessment 2. Conduct Assessment 3. Communicate Results 4. Maintain Assessment

### 2.3 Risk Model

The Risk Model defines the risk factors to be assessed and the relationship among those factors. Risk factors are characteristics used in risk models as inputs to determine levels of risk in risk assessments.
- Threats
- Vulnerabilities and Predisposing Conditions
- Likelihood
- Impact

## 3. System Characterization

System characterization is the process of defining the information assets that require a risk analysis. Information assets that require protection – that includes infrastructure, workflows, key assets, and resources. System characterization requires an inventory of major applications and general support systems.

The following are some examples of major applications and their probable owners:

- Syxsense
- Netsparker
- Wireshark

General support systems are the systems used throughout the organization to support one or more. The following are some examples of general support systems:

- Laptops, tablets, smartphones, and other mobile devices
- Computer workstations
- Network (wired and wireless)

In assessing risks for an IT system, the first step is to define the scope of the effort. In this step, the components of the IT system are identified, along with the resources and the information that constitute the system. Characterizing an IT system establishes the scope of the risk assessment effort, defines the operational authorization, and provides information like hardware, software, system connectivity, and responsible division or support personnel –essential to defining the risk.

### 3.1 Technology components – The Protection Lab Company (TPL)

**Component** | **Description**
--- | ---
IT system Description and Components | TPL is a distributed server application hosting multiple applications for our clients. Here are some of the major components: - 4 x Dell R740’s with Xeon 3.5 20 Core sockets, 768 GB of redundant memory and 200TB of raw magnetic and flash storage. - The base OS on the Servers is VMware vSphere 7.0 with vSAN. - Redundant 10GB multimode SFPs to our core switch. IT System Interfaces and Protocols - An interface between TPL and the Budget Consolidation System (TPL). This interface allows only the ABC to securely transit data using the Secure Copy Protocol (SCP) on port 22 into the TPL. - A VPN for emergency remote support to diagnostics, secured via the use of a one-time password authentication mechanism.

**Networks and Application** | - Our network consists of two ISPs both providing copper and fiber hand-offs to help reduce the chances of loss of one type or service provider. Our firewall aggregates these connections and is constantly checking the statuses via heartbeat so that in the event of a service loss, there won't be an induration. - TPL provides virtual hosting and managed services.

### 3.2 Physical Location(s)

**Location** | **Description**
--- | ---
TPL Data Center | 342 Elm Street, San Diego, California

### 3.3 Data Used by System

**Data** | **Description**
--- | ---
Data Elements | - Client software is located within our Windows Server Active Directory Domain to manage access to TPL. Our software utilizes encrypted communications between the client and the server and connects using SSL encryption. - Only users with the appropriate user rights within the TPL domain can access the client software, although a separate client login and password are required to gain elevated permissions to TPL.

### 3.4 Users – Rank Based

**Rank Based on Risk** | **Description**
--- | ---
Number of users | Starting with the application with the greatest number of users
Type of information | The more sensitive the information, the higher the risk Example: bank account numbers, social security numbers
Use of the information | Determine whether it is research, business intelligence
Availability of information | Hosted in our datacenter / cloud, or a standalone system
Mobility of the information | The more mobile, the greater the risk

### 3.5 Flow Diagram – Risk Assessment Activities

[Flow Diagram Image Link](#)

## 4. Risk Assessment Results

| Item Number | Perceived Threat | Threat-Source/ Vulnerability | Existing controls | Likelihood | Impact | Risk Rating | Recommended controls |
| ----------- | ----------------- | ----------------------------- | ------------------ | ---------- | ------ | ------------ | --------------------- |
| 01 (BD#4) | User system passwords can be guessed or cracked | Previous employee | Password Policy | High | High | High | Reevaluate Password Policy |
| 02 (BD#14) | Not having appropriate security measures heightens the risk of an attack | Attacks are indiscriminate, falling victim to “one size fits all” mentality | Regulations, policies | Low | High | High | Implement relevant security measures for the company or organization |
| 03 (BD#1) | Maintaining the continuity of TPL | Natural Disasters or cyber-attacks that force a shutdown business. | Disaster Recovery Plan | Low | High | Low | Maintain backups and cold site for continuity of business |
| 04 (BD#7) | Accidental human interference – Accidental disclosure of information | Employee being duped into releasing sensitive information, sending data to the wrong email address | Backups are taken regularly | Medium | High | Medium | Continue monitoring permissions changes, privileged users and backups. |
| 05 (BD#2) | Information accuracy is compromised | Software vulnerabilities like zero-day attacks. Or hardware malfunctions. | Firewall/ IPS. Backups are taken regularly | High | High | High | Patch vulnerabilities and keep programs up to date. Back up data. |
| 06 (BD#9) | Permissions, Privileges, and access control | Improper user permissions and access controls | Usernames and Passwords | Low | High | High | PINS or Biometric Scans |
| 07 (BD#15) | Using Granular Security | Prevent the spread of malware | Role Based Access control (RBAC) | Low | High | High | Using Security applied Schema allows specific users |
| 08 (BD #3) | Detecting attempted financial fraud in our point-of-sale system. | A set of activities taken money from being obtained through false pretenses | Check the name, phone number, and personal address of the customers | High | High | High | Using a fraud detection model with machine learning (ML) |
| 09 (BD#12) | Helps prevent violations of rules and protects organizations from fines and lawsuits | The loss of customer loyalty and trust. Business reputation | Policies and procedures | Medium | High | Medium | Monitoring regulatory changes, consistently applying policies and procedures |
| 10 (BD#13) | Restrict account access to unauthorized persons. | Non-permanent employees, third parties | Create / Add policies to the GPO | Medium | High | High | Set up guest user, administrator user, remote user |
