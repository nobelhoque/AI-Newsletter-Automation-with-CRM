# AI-Powered Newsletter Automation with CRM Integration

A sophisticated n8n workflow designed to streamline newsletter creation and distribution. This automation bridges the gap between AI-driven content generation and personalized CRM-based delivery, allowing users to send tailored newsletters to their audience with minimal effort.

## 🚀 Overview

This project provides an end-to-end solution for businesses to manage their email marketing. Whether you want to write your own newsletter or let a state-of-the-art AI model (Llama 3.3 via Groq) handle the heavy lifting, this workflow automates the entire process from content creation to bulk or personalized delivery.

## ✨ Key Features

- **Hybrid Content Creation**: Choose between manual input or AI-generated content based on a topic and specific instructions.
- **AI-Powered Copywriting**: Leverages Groq's Llama 3.3 model to craft engaging, HTML-formatted newsletters.
- **CRM Integration**: Dynamically fetches subscriber data (Name and Email) from Google Sheets.
- **Intelligent Dispatch Logic**:
  - **Personalized Mode**: Sends individual emails to each subscriber, injecting their name for a personal touch. Includes a **5-second rate limit delay** between emails to ensure high deliverability.
  - **Bulk Mode**: Sends a single broadcast to all subscribers for maximum efficiency.
- **Optimized for Deliverability**: Designed with safe limits in mind (~150 personalized or ~500 bulk emails per day, depending on your provider).
- **Professional Formatting**: Automatically generates clean HTML emails with proper structure (headers, lists, links, and styling).
- **Interactive Triggers**: Controlled via an n8n Form for a user-friendly experience.

## 🛠️ Tech Stack

- **Automation**: [n8n](https://n8n.io/)
- **AI Model**: [Groq](https://groq.com/) (Llama 3.3 70B Versatile)
- **CRM/Database**: Google Sheets
- **Email Service**: SMTP (Gmail, Outlook, or any standard provider)

## 📋 Prerequisites

To get this workflow running, you will need:
1. An **n8n** instance (self-hosted or Cloud).
2. A **Groq API Key** (for AI generation).
3. A **Google Cloud Project** with Google Sheets API enabled and OAuth credentials.
4. An **SMTP Service** account (e.g., Gmail App Password).

## ⚙️ Setup Instructions

1. **Import Workflow**: Download the `AI Newsletter Automation with CRM.json` file and import it into your n8n canvas.
2. **Configure Credentials**:
   - Add your **Groq API** credentials.
   - Connect your **Google Sheets OAuth2** account.
   - Setup your **SMTP** credentials for sending emails.
3. **Prepare Google Sheet**:
   - Create a sheet with a tab named `CRM`.
   - Ensure you have columns titled: `Full Name` and `Email Address`.
4. **Update IDs**: Update the Google Sheet ID in the "Fetch Subscribers" node to match your specific spreadsheet.

## 📈 Workflow Preview

Below is a preview of the automation logic. You can also find a high-resolution version in the project files.

[📄 View High-Res Workflow PDF Preview](./AI%20Newsletter%20Automation%20with%20CRM%20(1).pdf)

*(Note for Upwork/GitHub: It is highly recommended to upload a screenshot of your n8n canvas as `preview.png` and link it here for a better visual impact.)*

## 💡 How to Use

1. Open the **Newsletter Request Form** URL provided by n8n.
2. Enter your **Subject Line** and **Topic**.
3. **Optional**: Enter your own content in the "Newsletter body" or leave it empty to trigger the AI writer.
4. **Select Personalization**:
   - `Yes`: Every recipient gets an email addressed to them.
   - `No`: A single bulk email is sent.
5. Click **Submit** and watch the automation handle the rest!

---
*Professional Automation Solutions | Optimized for Deliverability and Engagement*
