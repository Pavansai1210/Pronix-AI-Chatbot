# Search AI – Company Information

## 1. Introduction

Pronix AI Chatbot uses the Search AI feature available in the Kore.ai XO Platform to handle company-related user questions.

It allows users to ask questions about Pronix through a conversational interface.

## 2. How It Works

The Search AI workflow follows these steps:

1. The user asks a company-related question.
2. The question is processed through the Search AI node.
3. Search AI generates a response.
4. The response is passed to a JavaScript Script node.
5. The Script node processes the response and stores the final answer in `context.finalAnswer`.
6. A Message node displays the final answer to the user.

## 3. Response Handling

The chatbot uses JavaScript logic to handle Search AI responses.

- When a suitable short answer is available, the chatbot displays that answer.
- When the answer is long or unavailable, the chatbot provides the Pronix website link.

Website: https://www.pronixinc.com

## 4. Example Interaction

**User:**

What does Pronix do?

**Chatbot:**

The chatbot provides the Pronix company website link so the user can find more information.

https://www.pronixinc.com

## 5. Technologies Used

- Kore.ai XO Platform
- Search AI
- JavaScript Script Node
- Message Node

## 6. Benefits

- Allows users to ask company-related questions naturally.
- Provides automated responses.
- Directs users to the official company website when needed.
- Improves the chatbot's ability to handle information requests.

## 7. Summary

The Search AI feature adds company-information handling to Pronix AI Chatbot. It works with a JavaScript Script node to process responses before displaying them to users.
