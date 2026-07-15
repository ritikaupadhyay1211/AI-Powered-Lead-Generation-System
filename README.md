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
<!-- TOOLS & TECHNOLOGIES -->
<div style="margin-top: 30px; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;">
  <h2 style="color: #0176D3; border-bottom: 2px solid #E2E8F0; padding-bottom: 8px; font-size: 1.5rem;">🛠 Tools & Technologies</h2>
  <div style="display: flex; flex-direction: column; gap: 12px; margin-bottom: 30px;">
    <div>
      <span style="font-weight: bold; color: #2D3748;">Platform:</span> 
      <span style="background: #F1F5F9; color: #334155; padding: 3px 8px; border-radius: 4px; font-size: 0.9rem;">Salesforce Developer Edition (Lightning Experience)</span>
    </div>
    <div>
      <span style="font-weight: bold; color: #2D3748;">Automation & Intelligence:</span> 
      <span style="background: #F1F5F9; color: #334155; padding: 3px 8px; border-radius: 4px; font-size: 0.9rem;">Salesforce Prompt Builder</span>
      <span style="background: #F1F5F9; color: #334155; padding: 3px 8px; border-radius: 4px; font-size: 0.9rem;">Einstein AI</span>
      <span style="background: #F1F5F9; color: #334155; padding: 3px 8px; border-radius: 4px; font-size: 0.9rem;">Lightning App Builder</span>
    </div>
    <div>
      <span style="font-weight: bold; color: #2D3748;">Documentation & Storage:</span> 
      <span style="background: #F1F5F9; color: #334155; padding: 3px 8px; border-radius: 4px; font-size: 0.9rem;">GitHub</span>
      <span style="background: #F1F5F9; color: #334155; padding: 3px 8px; border-radius: 4px; font-size: 0.9rem;">Microsoft Word</span>
    </div>
  </div>
</div>

<!-- REPOSITORY TREE STRUCTURE -->
<div style="margin-top: 30px; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;">
  <h2 style="color: #0176D3; border-bottom: 2px solid #E2E8F0; padding-bottom: 8px; font-size: 1.5rem;">📂 Repository Tree Structure</h2>
  <pre style="background-color: #0F172A; color: #38BDF8; padding: 20px; border-radius: 8px; font-family: 'Fira Code', Consolas, Monaco, 'Andale Mono', 'Ubuntu Mono', monospace; font-size: 0.9rem; overflow-x: auto; margin-bottom: 30px; line-height: 1.5;">
AI-Powered-Lead-Management-System
├── README.md                # Project Presentation
├── Documentation.pdf        # Complete Technical Runbook
├── Screenshots/             # Verification Images
│   ├── Home_Page/
│   ├── Profiles_&_Users/
│   ├── Roles/
│   ├── Lead_Object_Config/
│   ├── Prompt_Builder/
│   └── Final_System_View/
└── Demo_Video_Link.txt      # Walkthrough Links
  </pre>
</div>

<!-- AUTHOR INFO -->
<div style="background-color: #F8FAFC; border: 1px solid #E2E8F0; padding: 20px; border-radius: 8px; text-align: center; margin-top: 40px; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;">
  <p style="margin: 0; font-size: 0.95rem; color: #4A5568;">
    👩‍💻 <strong>Author:</strong> 
    <span style="color: #0176D3; font-weight: bold;">Ritika Upadhyay</span>
  </p>
  <p style="margin: 5px 0 0 0; font-size: 0.85rem; color: #718096; font-style: italic;">
    Salesforce Certified Administrator with AI Agentforce Specialization – Virtual Internship Project Submission
  </p>
</div>
