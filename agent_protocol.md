# 📜 JARVIS Agent Communication Protocol

### Overview
Communication between `server.js` (Node) and `agent.py` (Python) happens over **stdin/stdout** using JSON lines.

### Message Format
Each message is a single-line JSON object.

**Request (Node -> Python):**
```json
{
  "_req_id": 123,
  "action": "system_info",
  "args": {}
}
```

**Response (Python -> Node):**
```json
{
  "_req_id": 123,
  "success": true,
  "data": { ... }
}
```

### Protocol Rules
1. **Serialization**: Single line JSON per command.
2. **Persistence**: The Python agent runs as a persistent background process (`pythonw`).
3. **Timeout**: Node.js waits for 10 seconds before rejecting a request.
4. **Error Handling**: Agent catches exceptions and returns `{ success: false, error: "message" }`.
