# MockAPI Integration

## 1. Introduction

Pronix AI Chatbot uses MockAPI to handle account-related data operations.

Kore.ai XO Platform Custom Services are used to connect chatbot workflows with MockAPI.

## 2. Registration Integration

The registration workflow collects:

- Username
- Email address
- Phone number
- Password

The collected information is sent to `RegisterUsersAPI` through a Custom Service.

The chatbot checks the service response status code to determine whether registration was successful.

## 3. Login Integration

The login workflow uses email-based verification.

1. The user enters an email address.
2. The chatbot sends the email through a Custom Service.
3. The workflow checks the service response status code.
4. If the status code is `200`, the workflow continues.
5. If the status code is not `200`, the chatbot informs the user that the email is not registered.

The chatbot provides Register Now, Retry, and Cancel options.

**Note:** The implemented login workflow does not request or verify a password.

## 4. Modify Account Integration

The Modify Account workflow allows users to update:

- Username
- Phone number

The updated information is submitted through a Custom Service.

The chatbot checks the response and displays a success or failure message.

## 5. Delete Account Integration

The Delete Account workflow:

1. Requests confirmation from the user.
2. Provides Yes and No options.
3. Calls a Custom Service when the user confirms deletion.
4. Checks the service response.
5. Displays the appropriate success or failure message.

## 6. Technologies Used

- Kore.ai XO Platform
- MockAPI
- Custom Services
- JavaScript Script Nodes

## 7. Integration Workflow

```text
User
  |
  v
Kore.ai Chatbot
  |
  v
Dialog Task
  |
  v
Custom Service
  |
  v
MockAPI
  |
  v
Service Response
  |
  v
Kore.ai Logic Node
  |
  v
Chatbot Response
```

## 8. Important Note

MockAPI is used for account-related data operations in this project. Custom Services connect the chatbot workflows to MockAPI and process the returned responses.
