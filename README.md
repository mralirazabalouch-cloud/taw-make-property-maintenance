## 🎥 Project Demo Video

[Watch My Property Maintenance Automation Demo]((https://www.loom.com/share/fbbb95eee9b7463bad78e55eabcd63ca))

# AI-Powered Property Maintenance Automation

An AI-powered property maintenance workflow built with Make.com to automate tenant maintenance requests, classify issues, assign suitable contractors, and send email notifications.

## 🎥 Project Demo

[Watch the Live Workflow Demo](https://www.loom.com/share/fbbb95eee9b7463bad78e55eabcd63ca)

## 📌 Problem Statement

Property managers often handle maintenance requests manually, which can delay issue classification, contractor assignment, and communication with tenants.

This automation helps streamline the process and reduce repetitive administrative work.

## ✨ Key Features

- Tenant maintenance request collection through Google Forms
- Automatic request capture in Google Sheets
- AI-powered issue classification using Google Gemini
- Category detection: Plumbing, Electrical, HVAC, and General
- Priority classification: High, Medium, and Low
- Airtable maintenance request tracking
- Contractor matching based on specialty, availability, and active status
- Automatic assignment status updates
- Gmail notifications for tenants and a test contractor email
- Automatic retry handling for temporary Gemini AI errors

## 🛠️ Technology Stack

| Tool | Purpose |
|---|---|
| Make.com | Workflow automation |
| Google Forms | Tenant request submission |
| Google Sheets | Request collection |
| Google Gemini 2.5 Flash | AI classification |
| JSON Parser | Structured AI output |
| Airtable | Request and contractor management |
| Gmail | Email notifications |

## 🔄 Workflow Architecture

Google Forms → Google Sheets → Gemini AI → JSON Parser → Airtable Create Record → Airtable Search Contractors → Airtable Update Record → Gmail Notifications

A retry error handler is attached to the Gemini AI module.

## ⚙️ Setup Instructions

1. Import `property-maintenance-blueprint-public.json` into Make.com.
2. Connect Google Sheets, Airtable, and Gmail accounts.
3. Configure the Google Sheets spreadsheet and response worksheet.
4. Set up the Airtable `Maintenance Requests` and `Contractors` tables.
5. Reconfigure the Airtable base, table, and field mappings as needed.
6. Configure the Gemini AI module and JSON Parser data structure.
7. Set the contractor notification recipient for your environment.
8. Test the scenario using a new Google Form submission.
9. Enable scenario scheduling for automatic processing.

## 🧪 Testing

The workflow was tested using sample tenant maintenance requests.

Verified results include:

- Successful Google Sheets request capture
- Gemini AI category and priority classification
- Airtable record creation
- Matching a plumbing request to an available plumbing contractor
- Updating request status to `Assigned`
- Sending test notification emails
- Configuring automatic Gemini retries

## ⚠️ Current Limitations

- Contractor notification currently uses a fixed test email address rather than the dynamically selected contractor's email.
- When no matching contractor is available, the workflow does not yet provide a dedicated fallback route.
- Follow-up notifications for `In Progress` and `Completed` statuses are not yet automated.
- The public blueprint uses placeholders for private connection and resource identifiers, so configuration is required after import.

## 📁 Repository Files

- `README.md` — Project documentation
- `property-maintenance-blueprint-public.json` — Sanitized Make.com scenario blueprint

## 👨‍💻 Project Information

**Project:** Property Maintenance Automation

**Internship:** Think AI Works

**Role:** AI Automation Engineer Intern

**Platform:** Make.com
