# 🚀 AI-Powered Lead Management & Security Infrastructure

<p align="center">
  <img src="https://img.shields.io/badge/Salesforce-Developer%20Edition-0176D3?style=for-the-badge&logo=salesforce&logoColor=white" alt="Salesforce">
  <img src="https://img.shields.io/badge/Einstein%20AI-Agentforce-00A1E0?style=for-the-badge" alt="Einstein AI">
  <img src="https://img.shields.io/badge/Security-Role%20Based-2E7D32?style=for-the-badge" alt="Security">
</p>

---

## 📋 Project Overview

This project was developed as part of the Salesforce Certified Administrator with AI Agentforce Specialization Virtual Internship using a *Salesforce Developer Edition* environment.

The objective was to architect a highly secure, automated, and AI-powered Lead Management System. This was achieved by heavily customizing the standard Salesforce Lead object, enforcing stringent role-based data visibility sharing rules, and using Salesforce Prompt Builder to dynamically inject Einstein AI-generated context summaries straight into the agent UI.

---

## 🎯 Project Objectives

- [x] Configure Salesforce Developer Edition optimized for Lead pipelines.
- [x] Deeply customize fields and schemas on the Standard Lead Object.
- [x] Establish secure operational Profiles, Users, and Roles.
- [x] Enforce rigid Role-Based Security configurations.
- [x] Integrate Prompt Builder for generative AI Lead Summary generation.
- [x] Design user-centric Lightning Record Pages.
- [x] Practice enterprise-level Salesforce Administration best practices.

---

## 🛠 Implemented Features

### 👤 User & Security Management
* Profile Layer: Built custom Lead Manager (Full CRUD) and Sales Agent (Restricted Deletion) profiles.
* Access Control: Deployed advanced Object-Level Permissions & granular Field-Level Security.
* Data Privacy: Programmed explicit Role Hierarchies and targeted Permission Sets to ensure zero data leakage.

### 💼 Lead Operations Customization
* Expanded the standard schema with custom tracking fields (AI_Summary__c).
* Redesigned clutter-free Lead Page Layouts to accelerate agent workflows.
* Tailored customized Lightning Experience records for optimal viewing.

### 🤖 Generative AI Infrastructure
* Enabled baseline Salesforce Einstein capabilities.
* Programmed an active Field Generation Prompt Template inside Salesforce Prompt Builder.
* Orchestrated a 1-click execution engine via Lightning App Builder to generate, update, and lock AI summaries natively.

---

## 🔒 Security Configuration Matrix

### Profile Access Clearances

| Profile | Object Permissions (Lead, Task, Event, Contact) | Operational Intent |
| :--- | :--- | :--- |
| Lead Manager | Read | Create | Edit | Delete | Oversees pipeline, monitors audits, handles exceptions. |
| Sales Agent | Read | Create | Edit (No Delete) | Daily prospecting, lead conversion, event scheduling. |

### Role Hierarchy Architecture
```text
  [VP of Sales]
        │
        └── [Lead Manager]
                 │
                 └── [Sales Agent]