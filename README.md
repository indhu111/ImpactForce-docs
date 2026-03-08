# ImpactForce - Nonprofit Donor Management Platform

[![Salesforce](https://img.shields.io/badge/Salesforce-Nonprofit%20Cloud-00A1E0?logo=salesforce)](https://www.salesforce.com/nonprofit/)
[![Agentforce](https://img.shields.io/badge/Agentforce-Service%20Agent-00D4FF)](https://www.salesforce.com/agentforce/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> An AI-powered Salesforce solution built on Nonprofit Cloud to streamline donation management, automate donor engagement, and provide 24/7 intelligent support for nonprofit organizations.

---

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Architecture](#architecture)
- [Technical Stack](#technical-stack)
- [Setup & Installation](#setup--installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Documentation](#documentation)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

---

## 🎯 Overview

**ImpactForce** is a comprehensive Salesforce-based platform designed to help nonprofit organizations efficiently manage donations, engage with donors, and automate fundraising operations. The solution leverages **Salesforce Nonprofit Cloud** and **Agentforce** to provide intelligent, 24/7 donor support while ensuring secure payment processing and data management.

### Problem Statement

Nonprofits face challenges in:
- Manual donation tracking and donor record management
- Limited 24/7 donor support capabilities
- Lack of secure online payment infrastructure
- Time-consuming donor verification and authentication processes
- Fragmented communication and engagement workflows

### Solution

ImpactForce addresses these challenges through:
- **Automated Donation Management**: Custom Salesforce objects for tracking donations, campaigns, and donor relationships
- **AI-Powered Support**: Agentforce Service Agent with custom prompt templates for intelligent, empathetic donor interactions
- **Secure Authentication**: Multi-factor verification flows for donor identity validation
- **Online Payment Integration**: Razorpay gateway integration for seamless donation processing
- **Self-Service Portal**: Experience Cloud site for donors to manage their contributions and access information

---

## ✨ Features

### 🤖 Agentforce Service Agent
- **24/7 Automated Support**: AI-powered agent handles donor inquiries about donations, policies, and campaigns
- **Custom Prompt Templates**: Tailored responses ensuring polite, empathetic, and policy-compliant communication
- **Natural Language Understanding**: Processes donor questions in plain English and provides accurate answers
- **Knowledge Base Integration**: Accesses FAQ and Policy PDFs to answer donor questions
- **Contextual Conversations**: Maintains conversation history for personalized interactions

### 🔐 Donor Authentication & Security
- **Email Verification Flow**: Sends verification codes to registered donor emails
- **Code Validation**: Secure 6-digit code verification with expiry (10 minutes)
- **Session Management**: Authenticated sessions for secure data access
- **Data Masking**: PII/GDPR compliance with sensitive data protection
- **Permission-Based Access**: Role-based security with permission sets

### 💳 Payment Processing
- **Razorpay Integration**: Secure online donation processing
- **Multiple Payment Methods**: Credit/debit cards, UPI, wallets, net banking
- **Automated Receipts**: Instant tax receipt generation and email delivery
- **Recurring Donations**: Support for monthly/annual recurring contributions
- **Transaction Tracking**: Real-time payment status and history

### 📊 Donation Management
- **Custom Data Model**: Donation, Campaign, Contact, and Account objects
- **Automated Workflows**: Flow-based automation for donor communications
- **Dashboard & Reports**: Real-time fundraising metrics and donor analytics
- **Campaign Tracking**: Monitor campaign performance and ROI
- **Donor Segmentation**: Categorize donors by contribution levels and engagement

### 🌐 Experience Cloud Portal
- **Donor Self-Service**: View donation history and manage recurring gifts
- **Profile Management**: Update contact information and preferences
- **Online Donations**: Make secure contributions through integrated payment gateway
- **Receipt Downloads**: Access and download tax receipts
- **Communication Preferences**: Manage email subscriptions and notifications

---

## 🏗️ Architecture
```
┌─────────────────────────────────────────────────────────┐
│                   Donor Interface                        │
│            (Experience Cloud Portal / Chat)              │
└────────────────────┬────────────────────────────────────┘
                     │
                     ▼
┌─────────────────────────────────────────────────────────┐
│              Agentforce Service Agent                    │
│        (AI-Powered 24/7 Donor Support)                   │
└────────┬────────────────────────────────┬───────────────┘
         │                                │
         ▼                                ▼
┌──────────────────┐            ┌──────────────────────┐
│  Knowledge Base  │            │  Action Framework    │
│  - FAQ PDF       │            │  - Verification Flow │
│  - Policy PDF    │            │  - Donation Flow     │
└──────────────────┘            │  - Prompt Templates  │
                                └──────────┬───────────┘
                                           │
                                           ▼
                                  ┌─────────────────────┐
                                  │  Salesforce Data    │
                                  │  - Contact          │
                                  │  - Account          │
                                  │  - Donation         │
                                  │  - Campaign         │
                                  └─────────────────────┘
                                           │
                                           ▼
                                  ┌─────────────────────┐
                                  │  Payment Gateway    │
                                  │     (Razorpay)      │
                                  └─────────────────────┘
```

---

## 🛠️ Technical Stack

### Salesforce Platform
- **Salesforce Nonprofit Cloud**: Core platform for nonprofit data management
- **Agentforce**: AI-powered service agent for automated support
- **Experience Cloud**: Public-facing donor portal
- **Einstein AI**: Natural language processing and intent recognition
- **Flow Builder**: Automated workflows and business logic
- **Apex**: Custom server-side logic and API integrations
- **Lightning Web Components (LWC)**: Custom UI components

### Integrations
- **Razorpay Payment Gateway**: REST API integration for payment processing
- **Email Service**: Org-wide email for verification codes and receipts
- **PDF Libraries**: Knowledge base for FAQ and policy documents

### Security & Compliance
- **Data Masking**: PII protection for GDPR compliance
- **Permission Sets**: Role-based access control
- **Field-Level Security**: Granular data access controls
- **Sharing Rules**: Record-level access management
- **AI Safety**: Toxicity detection and prompt injection prevention

---

## 🚀 Setup & Installation

### Prerequisites
- Salesforce Developer/Nonprofit Edition org
- Agentforce Service Agent license
- Razorpay merchant account (for payment integration)
- Einstein AI enabled in org
