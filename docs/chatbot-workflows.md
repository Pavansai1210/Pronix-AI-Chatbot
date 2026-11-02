
# Chatbot Workflows — Pronix AI Chatbot

## 1. Welcome Workflow

- Displays a welcome message when the user starts the chatbot.
- Provides Login and Register buttons.
- Allows users to select the required operation.

## 2. User Registration Workflow

1. User selects Register.
2. Chatbot asks for the required registration details.
3. User enters the information.
4. Chatbot sends the details to MockAPI through API integration.
5. MockAPI stores the registered user information.

## 3. User Login Workflow

1. User selects Login.
2. Chatbot asks for login credentials.
3. User provides the required details.
4. Chatbot checks the credentials against the user data stored in MockAPI.
5. Chatbot displays the appropriate login response.

## 4. Modify Account Workflow

- Allows users to request account modification.
- Uses MockAPI integration to update account information.

## 5. Delete Account Workflow

- Allows users to request account deletion.
- Uses MockAPI integration for the account operation.

## 6. Search AI Workflow

- Accepts company-related questions.
- Uses Kore.ai Search AI to retrieve relevant company information.
- Displays the response to the user.

## 7. Process Question Handling

The chatbot can handle questions such as:

- How can I register?
- How can I log in?
- How can I modify my account?
- How can I delete my account?

It provides relevant guidance for these processes.

## 8. Fallback Workflow

- Handles questions that the chatbot cannot understand.
- Displays an appropriate fallback message.
- Guides users to choose Login or Register when needed.

## 9. Deployment

The chatbot is deployed through Telegram.

Telegram Bot: https://t.me/Pronix_AI_Pavan
