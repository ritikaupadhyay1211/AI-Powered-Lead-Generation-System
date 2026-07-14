<!-- HEADER BANNER -->
<div style="background: linear-gradient(135deg, #0176D3, #0b2240); padding: 30px; border-radius: 8px; border-left: 6px solid #00A1E0; margin-bottom: 30px; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;">
  <span style="background: rgba(0, 161, 224, 0.15); border: 1px solid rgba(0, 161, 224, 0.3); padding: 4px 12px; border-radius: 4px; font-size: 0.75rem; color: #00A1E0; text-transform: uppercase; font-weight: 600; letter-spacing: 1px;">Virtual Internship Project</span>
  <h1 style="color: #FFFFFF; font-size: 2rem; margin: 12px 0 6px 0; font-weight: 700;">AI-Powered Lead Management & Security Infrastructure</h1>
  <p style="color: #A0AEC0; font-size: 1rem; margin: 0 0 16px 0; max-width: 800px;">Developed as part of the Salesforce Certified Administrator with AI Agentforce Specialization Virtual Internship using Salesforce Developer Edition.</p>
  <div style="color: #E2E8F0; font-size: 0.9rem;">
    <span>Author: </span><span style="font-weight: 600; color: #00A1E0;">Ritika Upadhyay</span>
  </div>
</div>

## Project Overview

The objective of this project was to build a secure and AI-powered Lead Management System by customizing the Salesforce Lead object, configuring user access and security, implementing role-based permissions, and integrating Salesforce Prompt Builder to generate AI-powered Lead summaries.

The project demonstrates core Salesforce Administration concepts including object customization, security implementation, user management, AI integration, and Lightning Experience customization.

---

## Project Objectives

* Configure Salesforce Developer Edition for Lead Management.
* Customize the Standard Lead Object.
* Create custom Profiles, Users, and Roles.
* Implement Role-Based Security.
* Configure Prompt Builder for AI-powered Lead Summary generation.
* Customize Lightning Record Pages.
* Understand Salesforce Administration best practices.

---

## Features Implemented

<div style="display: flex; flex-wrap: wrap; gap: 16px; margin: 20px 0; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;">
  <!-- Column 1 -->
  <div style="flex: 1; min-width: 250px; background: #F8FAFC; border: 1px solid #E2E8F0; padding: 20px; border-radius: 6px;">
    <h3 style="color: #0176D3; margin-top: 0; font-size: 1.1rem; border-bottom: 2px solid #E2E8F0; padding-bottom: 8px;">Lead Management</h3>
    <ul style="padding-left: 20px; color: #4A5568; font-size: 0.9rem; line-height: 1.6;">
      <li>Customized the Standard Lead Object.</li>
      <li>Configured custom Lead fields.</li>
      <li>Managed Lead records.</li>
      <li>Customized Lead Page Layout.</li>
    </ul>
  </div>
  <!-- Column 2 -->
  <div style="flex: 1; min-width: 250px; background: #F8FAFC; border: 1px solid #E2E8F0; padding: 20px; border-radius: 6px;">
    <h3 style="color: #0176D3; margin-top: 0; font-size: 1.1rem; border-bottom: 2px solid #E2E8F0; padding-bottom: 8px;">User & Security Management</h3>
    <ul style="padding-left: 20px; color: #4A5568; font-size: 0.9rem; line-height: 1.6;">
      <li>Created Lead Manager Profile.</li>
      <li>Created Sales Agent Profile.</li>
      <li>Configured Object-Level Permissions.</li>
      <li>Configured Field-Level Security.</li>
      <li>Created Lead Manager User.</li>
      <li>Created Sales Agent User.</li>
      <li>Assigned Profiles and Roles.</li>
      <li>Configured Role Hierarchy.</li>
      <li>Assigned Permission Sets.</li>
    </ul>
  </div>
  <!-- Column 3 -->
  <div style="flex: 1; min-width: 250px; background: #F8FAFC; border: 1px solid #E2E8F0; padding: 20px; border-radius: 6px;">
    <h3 style="color: #0176D3; margin-top: 0; font-size: 1.1rem; border-bottom: 2px solid #E2E8F0; padding-bottom: 8px;">AI & Automation</h3>
    <ul style="padding-left: 20px; color: #4A5568; font-size: 0.9rem; line-height: 1.6;">
      <li>Enabled Salesforce Einstein.</li>
      <li>Created AI_Summary__c custom field.</li>
      <li>Created a Field Generation Prompt Template.</li>
      <li>Configured Prompt Builder resources.</li>
      <li>Activated Prompt Template.</li>
      <li>Integrated Template with Lightning App Builder.</li>
      <li>Generated AI Lead summaries into fields.</li>
    </ul>
  </div>
</div>

---

## Security Configuration

The project implements Salesforce security using Profiles, Roles, Permission Sets, and Object-Level Security.

### Profile Permissions

<table style="width: 100%; border-collapse: collapse; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif; margin-bottom: 20px;">
  <thead>
    <tr style="background-color: #0176D3; color: white;">
      <th style="padding: 10px; text-align: left; font-size: 0.95rem;">Profile</th>
      <th style="padding: 10px; text-align: left; font-size: 0.95rem;">Permissions Granted</th>
    </tr>
  </thead>
  <tbody>
    <tr style="border-bottom: 1px solid #E2E8F0;">
      <td style="padding: 10px; font-weight: bold; color: #2D3748; font-size: 0.9rem;">Lead Manager Profile</td>
      <td style="padding: 10px; color: #4A5568; font-size: 0.9rem;">Read, Create, Edit, Delete. Full access to Lead, Task, Event, and Contact.</td>
    </tr>
    <tr style="border-bottom: 1px solid #E2E8F0;">
      <td style="padding: 10px; font-weight: bold; color: #2D3748; font-size: 0.9rem;">Sales Agent Profile</td>
      <td style="padding: 10px; color: #4A5568; font-size: 0.9rem;">Read, Create, Edit. Restricted Delete Permission. Access to Task and Event.</td>
    </tr>
  </tbody>
</table>

### Role Hierarchy

<div style="background: #F8FAFC; border: 1px solid #E2E8F0; border-radius: 6px; padding: 20px; font-family: monospace; font-size: 0.9rem; color: #2D3748; margin-bottom: 20px;">
VP of Sales<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└── Lead Manager<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└── Sales Agent
</div>

This hierarchy controls record visibility and ensures secure data sharing within the organization.

---

## Einstein Generative AI Integration

The project incorporates Salesforce Prompt Builder to improve Lead management through AI-assisted content generation.

Implemented features include:
* AI Summary Custom Field
* Prompt Builder Configuration
* Field Generation Prompt Template
* Lightning App Builder Integration
* AI-generated Lead Summary
* One-click generation and storage of Lead summaries within Salesforce

---

## Project Implementation

The repository includes screenshots demonstrating every major configuration step.

* **Salesforce Setup:** Home Page | App Launcher
* **Profiles:** Profiles List | Lead Manager Profile | Sales Agent Profile
* **Users:** Users List | Lead Manager User | Sales Agent User
* **Roles:** Role Hierarchy | Lead Manager Role | Sales Agent Role
* **Lead Configuration:** Object Manager | Lead Object | Fields & Relationships | Lead Page Layout | Lead Record
* **AI Configuration:** Prompt Builder | AI Summary Field
* **Security:** Permission Set Configuration
* **Final Project:** Completed Salesforce Environment

---

## Business Value

This project demonstrates how Salesforce Administration can improve organizational efficiency by:
* Securing customer data using Profiles and Roles.
* Controlling user access through Permission Sets.
* Organizing Lead information efficiently.
* Automating Lead Summary generation using Salesforce AI.
* Improving productivity through Lightning Experience customization.
* Applying Salesforce Administration best practices.

---

## Tools & Technologies Used

<div style="display: flex; flex-wrap: wrap; gap: 6px; margin: 15px 0; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;">
  <span style="background: #EDF2F7; color: #2D3748; padding: 4px 10px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">Salesforce Developer Edition</span>
  <span style="background: #EDF2F7; color: #2D3748; padding: 4px 10px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">Salesforce Lightning Experience</span>
  <span style="background: #EDF2F7; color: #2D3748; padding: 4px 10px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">Salesforce Prompt Builder</span>
  <span style="background: #EDF2F7; color: #2D3748; padding: 4px 10px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">Salesforce Einstein AI</span>
  <span style="background: #EDF2F7; color: #2D3748; padding: 4px 10px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">Lightning App Builder</span>
  <span style="background: #EDF2F7; color: #2D3748; padding: 4px 10px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">GitHub</span>
  <span style="background: #EDF2F7; color: #2D3748; padding: 4px 10px; border-radius: 4px; font-size: 0.85rem; font-weight: 500;">Microsoft Word</span>
</div>

---

## 📂 Repository Structure

```bash
AI-Powered-Lead-Management-System
│
├── README.md
├── Documentation.pdf
├── Screenshots
│     ├── Home Page
│     ├── Profiles
│     ├── Users
│     ├── Roles
│     ├── Lead Object
│     ├── Prompt Builder
│     ├── AI Summary
│     └── Final Project
│
└── Demo Video Link
