# Chatbot Workflows

This document describes the main conversational workflows implemented in the Pronix AI Chatbot using the Kore.ai XO Platform.

## 1. Welcome Workflow

When a user starts the chatbot on Telegram, the bot displays:

- "Hello! Welcome to our Virtual Assistant."
- "Please choose either Login or Register."

The user can select one of two buttons:

- Register
- Login

## 2. User Registration

The registration workflow collects the following information:

1. Username
2. Email address
3. Phone number
4. Password

### Registration process

1. The chatbot asks the user to enter their username.
2. It collects the user's email address.
3. It asks for the phone number.
4. It collects the password.
5. The collected information is sent to the `RegisterUsersAPI` Custom Service.
6. The workflow checks the API response status code.
7. On successful registration, the chatbot displays a registration confirmation and asks whether the user wants to continue.
8. The user can choose Yes or No.
9. The chatbot provides account management options after successful registration.

If registration fails, the chatbot displays an error message and asks the user to try again later.

## 3. User Login

The login workflow uses email-based verification.

### Login process

1. The chatbot asks the user to enter their registered email address.
2. The email is sent to a Custom Service.
3. The workflow checks the API response status code using a Logic node.
4. If the response status code is `200`, the workflow continues to the successful login path.
5. A Script node processes the service response and session information.
6. The chatbot displays account management options.

### If the email is not registered

If the API response does not return status code `200`, the chatbot displays:

"This email is not registered. Would you like to create a new account?"

The user can select:

- Register Now
- Retry
- Cancel

**Note:** This implementation verifies whether the email is registered. It does not request or verify a password during the login process.

## 4. Modify Account

The Modify Account workflow allows users to update their account information.

### Available options

- Modify Username
- Modify Phone Number

### Workflow

1. The chatbot welcomes the user to the account modification service.
2. It asks which information the user wants to modify.
3. The user selects the required field.
4. The chatbot asks for the new username or phone number.
5. The updated information is sent through a Custom Service.
6. The workflow checks the API response.

**Success message:** "Your account has been updated."

**Failure message:** "Something went wrong. Please try again later."

## 5. Delete Account

The Delete Account workflow allows users to delete their account after confirmation.

### Workflow

1. The chatbot asks the user to confirm account deletion.
2. It provides Yes and No options.
3. If the user selects Yes, a Custom Service is called.
4. The workflow checks the API response.

**Successful deletion:** "Your account has been deleted. Goodbye!"

**If deletion fails:** "Something went wrong. Please try again later."

**If the user selects No:** "No problem! Your account was not deleted."

## 6. Company Information Search

The chatbot uses the Search AI feature to handle company-related questions.

### Workflow

1. The user asks a question about Pronix.
2. Kore.ai processes the question through the Search AI node.
3. The Search AI integration generates a response.
4. A Script node processes the response.
5. The final message is displayed to the user.

For the demonstrated question, the chatbot provides the company website:

https://www.pronixinc.com

## 7. Error Handling and Conversation Management

The chatbot includes:

- API response status checking.
- Registration and account-operation failure messages.
- Retry and Cancel options in the login flow.
- Welcome and fallback messages.
- Script-based response and session handling.

## 8. Deployment

The Pronix AI Chatbot is deployed on Telegram using the Kore.ai XO Platform.

Users can interact with the chatbot through Telegram to access registration, email-based login, account management, and company information responses.

## 9. Technologies Used

- Kore.ai XO Platform
- Dialog Tasks
- Intents and Entities
- Search AI
- Custom Services
- REST API integration
- MockAPI
- JavaScript Script Nodes
- Telegram

