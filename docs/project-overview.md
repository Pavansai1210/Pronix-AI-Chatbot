# Project Overview – Pronix AI Chatbot

## 1. Introduction

Pronix AI Chatbot is an AI-powered virtual assistant developed using the Kore.ai XO Platform.

The chatbot is integrated with Telegram to provide users with a conversational interface for account management and company-related information.

The project demonstrates conversational workflow development, API integration, Search AI, and chatbot deployment.

## 2. Project Objectives

The main objectives are:

- Develop an interactive virtual assistant.
- Provide user registration functionality.
- Implement email-based login verification.
- Allow users to modify account information.
- Provide account deletion with confirmation.
- Handle company-related questions using Search AI.
- Integrate external APIs with chatbot workflows.
- Deploy the chatbot on Telegram.

## 3. Main Modules

### Welcome Module
Introduces the chatbot and provides Login and Register buttons.

### User Registration Module
Collects:
- Username
- Email address
- Phone number
- Password

Sends the collected information to the registration Custom Service.

### User Login Module
- Collects the registered email address.
- Sends the email to a Custom Service.
- Checks the API response status code.
- Continues when the response status code is 200.
- Provides Register Now, Retry, and Cancel options when the email is not registered.

Note: The implemented login flow uses email-based verification and does not request password authentication.

### Account Modification Module
Allows users to update:
- Username
- Phone number

### Account Deletion Module
Provides a confirmation step before processing account deletion through a Custom Service.

### Company Information Module
Uses Search AI to process company-related questions and provide responses.

## 4. System Architecture

The chatbot follows this high-level architecture:

1. User interacts with the Telegram chatbot.
2. Kore.ai XO Platform processes the conversational input.
3. Dialog Tasks control the chatbot workflow.
4. Intents and Entities help handle user requests and inputs.
5. Custom Services connect account-related workflows to APIs.
6. MockAPI is used for account-related data operations.
7. Search AI handles company-related questions.
8. JavaScript Script nodes process selected responses and session information.
9. The chatbot sends responses back to the user.

## 5. Technologies and Tools

| Technology | Usage |
|---|---|
| Kore.ai XO Platform | Chatbot development |
| Telegram | User interaction and deployment |
| Dialog Tasks | Workflow management |
| Intents and Entities | Conversational input handling |
| Custom Services | API integration |
| REST APIs | Communication with external services |
| MockAPI | Account data operations |
| Search AI | Company information handling |
| JavaScript | Script node processing |

## 6. Deployment

The chatbot is deployed on Telegram and can be accessed through its public bot link.

Telegram Bot: https://t.me/Pronix_AI_Pavan

## 7. Project Learning Outcomes

This project provided practical experience in:

- Building chatbots using a low-code conversational AI platform.
- Creating dialog tasks and conversational workflows.
- Working with intents and entities.
- Integrating REST APIs through Custom Services.
- Connecting chatbot workflows with MockAPI.
- Processing API responses using JavaScript.
- Implementing Search AI.
- Deploying conversational applications on Telegram.

## 8. Project Author

**Bangaru Pavan Sai**

GitHub: https://github.com/Pavansai1210

Repository: https://github.com/Pavansai1210/Pronix-AI-Chatbot
