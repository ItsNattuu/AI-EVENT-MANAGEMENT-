 AI-Powered Event Management System
 
An AI-powered event management automation system built using **n8n, Gemini AI, and Google Workspace**. The project automates repetitive event-management tasks such as participant registration, QR-code generation, attendance tracking, reminder emails, event notifications, and feedback analysis.

 Project Overview

Managing an event manually involves several repetitive activities. Organizers have to collect registrations, maintain participant records, send confirmation and reminder emails, manage attendance, communicate event updates, and analyze feedback after the event.

This project was developed to automate these processes using **workflow automation and Generative AI**.

The system consists of **five interconnected n8n workflows**, with Google Sheets acting as the central data layer.

The main goal is to reduce repetitive manual work and allow event organizers to focus more on planning and managing the actual event.

Objectives:
- Automate participant registration
- Generate unique Registration IDs
- Generate QR codes for participants
- Automatically send confirmation emails
- Implement QR-based attendance tracking
- Automate reminder emails
- Automate event notifications
- Analyze participant feedback using Generative AI
- Generate sentiment analysis and feedback summaries
- Reduce manual workload and human errors
- Improve the overall participant experience

 System Architecture

The system follows a workflow-based architecture:

                    ┌─────────────────────┐
                    │       Users         │
                    │ Organizer / Student │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │    Google Forms     │
                    │ Registration /      │
                    │ Feedback Forms      │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │    Google Sheets    │
                    │  Central Data Layer │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │        n8n          │
                    │ Workflow Automation │
                    └──────────┬──────────┘
                               │
             ┌─────────────────┼─────────────────┐
             │                 │                 │
             ▼                 ▼                 ▼
      Registration        Communication      Analytics
        Workflow            Workflows         Workflow
             │                 │                 │
             └─────────────────┼─────────────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │     Gemini AI       │
                    │ Content Generation  │
                    │ & Feedback Analysis │
                    └─────────────────────┘
                               │
              ┌────────────────┼────────────────┐
              ▼                ▼                ▼
           Gmail          Google Drive      Attendance
        Communication      QR Storage        Updates
