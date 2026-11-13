# Chatbot, Messaging & Conversational UI Blueprint
Source Attribution: WebUI Dataset & Modern Conversational Interface Standards

## 1. Domain Concept: "WHAT IS A CHAT / MESSAGING VIEW?"
An interactive real-time conversational thread with message bubbles, avatar indicators, status chips, code snippet blocks, and an anchored bottom input toolbar.

## 2. Standard Parts & DOM Anatomy:
1. `.chat-container`: Flex column with `height: 100svh; overflow: hidden;`.
2. `.chat-messages`: Scrollable central container (`flex: 1; overflow-y: auto;`).
3. `.message-bubble.user`: Right-aligned bubble with accent background (`#ff5500`) and white text.
4. `.message-bubble.assistant`: Left-aligned bubble with dark surface (`#181b24`), subtle border (`#272a38`), and rich markdown styling.
5. `.chat-input-bar`: Sticky bottom container with text input, send button, and attachment triggers.

## 3. Scoped Pure CSS:
```css
.chat-container {
  display: flex;
  flex-direction: column;
  height: 100svh;
  max-width: 900px;
  margin: 0 auto;
}

.chat-messages {
  flex: 1;
  overflow-y: auto;
  padding: 1.5rem;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.message-bubble {
  max-width: 80%;
  padding: 1rem 1.25rem;
  border-radius: 14px;
  line-height: 1.5;
}

.message-bubble.user {
  align-self: flex-end;
  background-color: #ff5500;
  color: #ffffff;
  border-bottom-right-radius: 4px;
}

.message-bubble.assistant {
  align-self: flex-start;
  background-color: #181b24;
  border: 1px solid #272a38;
  color: #f8fafc;
  border-bottom-left-radius: 4px;
}

.chat-input-bar {
  padding: 1rem 1.5rem;
  background-color: #12141a;
  border-top: 1px solid #272a38;
  display: flex;
  gap: 0.75rem;
}
```
