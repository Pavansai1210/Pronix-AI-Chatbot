
# API Integration — Pronix AI Chatbot

## 1. Overview

Pronix uses MockAPI to connect chatbot account-management workflows with an external API.

## 2. Account Operations

The chatbot includes the following account-related operations:

- Register Account
- Login
- Modify Account
- Delete Account

## 3. Integration Workflow

1. The user selects an account-related option in Telegram.
2. The chatbot collects the required information.
3. The corresponding dialog workflow processes the request.
4. The workflow connects to MockAPI.
5. The chatbot handles the API response and displays an appropriate message.

## 4. Technologies

- Kore.ai XO Platform
- REST API
- MockAPI
- JavaScript
- Telegram

## 5. Security Note

Do not publish API keys, access tokens, passwords, or private user information in this repository.
