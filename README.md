# AI Chatbot Workflow for Educational Institution

An n8n workflow that creates an intelligent chatbot for handling course inquiries and FAQs.

## Features

- Multilingual support (responds in the same language as user input)
- Course information lookup from Google Sheets
- FAQ answering from Google Sheets
- Automatic logging of unanswered questions with mobile numbers
- Conversation memory for context-aware responses

## Prerequisites

- n8n instance (cloud or self-hosted)
- Google Gemini API key
- Google Sheets with three sheets:
  - Course (course information)
  - FAQ (frequently asked questions)
  - unansweredQueries (logs unanswered questions)

## Setup Instructions

1. Import the workflow JSON file into your n8n instance
2. Configure credentials:
   - Google Gemini API account
   - Google Sheets OAuth2 account
3. Update the Google Sheets document ID in all three Google Sheets Tool nodes
4. Activate the workflow
5. Access the chat interface via the webhook URL

## Workflow Structure

- **Trigger**: Chat Trigger (hosted chat mode)
- **AI Agent**: Orchestrates the conversation
- **Google Gemini Chat Model**: Language model for responses
- **Simple Memory**: Maintains conversation context
- **Get Course Information Tool**: Retrieves course data
- **FAQ Tool**: Answers common questions
- **Question Tool**: Logs unanswered queries

## Usage

Users can:
- Ask about courses in any language
- Get answers to FAQs
- Have their unanswered questions logged with contact information
