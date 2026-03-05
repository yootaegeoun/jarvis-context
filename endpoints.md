# 📡 JARVIS API Endpoints

### 1. AI Chat Proxy
- **POST `/api/ai/chat`**
  - **Description**: Standard Gemini chat proxy.
  - **Body**: `{ model, contents, systemInstruction, tools }`

- **POST `/api/conversation/:sessionId/message`**
  - **Description**: Context-aware chat. Saves to SQLite and manages sliding window.
  - **Body**: `{ role, parts, systemInstruction, tools }`

### 2. PC Agent Operations
- **POST `/api/pc/execute`**
  - **Description**: Executes a command on the local machine via the Python agent.
  - **Body**: `{ command: { action, args } }`

- **GET `/api/pc/sysinfo`**
  - **Description**: Retrieves system stats (CPU, RAM, Disk).

### 3. History Management
- **GET `/api/chats/:sessionId`**: Retrieve conversation history.
- **POST `/api/chats/save`**: Legacy/Mirror message saving.
