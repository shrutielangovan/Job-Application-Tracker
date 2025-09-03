# Job Application Tracker

## Overview

An intelligent email processing system that automatically monitors Gmail for job application-related emails and maintains a comprehensive tracking database of all job applications and their current status.

## Problem Statement

Job seekers often struggle to keep track of multiple applications across different companies and platforms. Important updates like interview invitations, rejections, or status changes can get lost in busy email inboxes, leading to missed opportunities and poor follow-up management.
Solution
This automated system continuously monitors your Gmail inbox, intelligently identifies job-related emails, extracts key information using AI and Natural Language Processing, and maintains an up-to-date record of all your job applications in a structured format.

## Core Features

### Automated Email Processing
- Scheduled Monitoring: Automatically checks Gmail every 12 hours for new emails
- Smart Filtering: Uses Gmail API to efficiently retrieve and process recent emails
- Intelligent Classification: Leverages OpenAI's language models to determine if emails are job application-related
### AI-Powered Information Extraction
- Company Identification: Uses Named Entity Recognition (NER) to accurately extract company names from email content
- Role & Status Detection: OpenAI integration identifies job titles and application status from email text
- Contextual Understanding: Distinguishes between application confirmations, interview invitations, rejections, and status updates
### Structured Data Management
- Comprehensive Tracking: Maintains records with Applied Date, Company Name, Role, Status, and Last Updated timestamp
- CSV Database: Stores all information in an easily accessible CSV format for analysis and backup
- Status Updates: Automatically updates existing records when new information is received about the same application

## Technical Architecture

### Data Flow
- Email Retrieval: Gmail API fetches emails from the last 12 hours
- Content Processing: Email body and subject are extracted and preprocessed
- Company Extraction: NER model identifies company names from email signatures and content
- AI Classification: OpenAI model determines if email is job-related and extracts role/status
- Data Storage: Information is structured and saved to CSV with appropriate timestamps

## Key Components

- Gmail API Integration: Secure OAuth2 authentication and email retrieval
- NER Processing: spaCy or similar library for entity recognition
- OpenAI Integration: GPT model for intelligent text classification and extraction
- Data Management: CSV handling with proper data validation and duplicate prevention

## Use Cases

### For Job Seekers
- Automatic Tracking: Never manually log another job application
- Status Monitoring: Stay updated on all application statuses in one place
- Follow-up Management: Know which applications need follow-up attention
- Progress Analysis: Track application success rates and response times
### For Career Coaches
- Client Monitoring: Track multiple clients' job search progress
- Performance Analytics: Analyze application patterns and success rates
- Progress Reporting: Generate comprehensive job search reports


## Future Enhancements
- Web dashboard for visual application management
- Email notifications for important status changes
- Integration with job boards and ATS systems
- Analytics and reporting features

## Technology Stack

Backend: Python
Email Processing: Gmail API
NLP: spaCy for NER
AI: OpenAI GPT models
Data Storage: CSV (with potential database upgrade)
Scheduling: Cron jobs 

## Getting Started

1. Set up Gmail API credentials and OAuth2 authentication
2. Configure OpenAI API access
3. Install required Python dependencies (spaCy, openai, google-api-python-client)
4. Set up automated scheduling (every 12 hours)
5. Run initial email processing and verification

This system transforms the tedious task of job application tracking into a fully automated, intelligent process that ensures no opportunity is missed and all applications are properly monitored throughout the job search journey.
