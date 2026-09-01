# Marcus Fleet: Terminal Control Guide

This guide describes how an external assistant or bot can control the Marcus Fleet via the terminal.

## 🚀 1. Triggering New Tasks
You can trigger a task by sending a POST request to the local API.

### Command:
```bash
curl -X POST http://127.0.0.1:8000/trigger \
     -H "Content-Type: application/json" \
     -d '{"raw_text": "YOUR_PROJECT_DESCRIPTION_HERE"}'
```

```

### 🔄 1.2 Iterating on Existing Projects (Refinement)
To update an existing project rather than starting from scratch, simply include the original **`TASK-ID`** anywhere in your `raw_text` payload.

**Command Example:**
```bash
curl -X POST http://127.0.0.1:8000/trigger \
     -H "Content-Type: application/json" \
     -d '{"raw_text": "Add a Google Login feature to the mobile specific dashboard in TASK-1773084446"}'
```

**How it works under the hood:**
1. **Marcus** detects the `TASK-ID` and switches the pipeline to **Update Mode**.
2. **Librarian** loads the existing PRD, SDD, Design Docs, and Source Code into the agents' context.
3. The agents (Sophia, David, Maya, Alan) will **refine** the existing documents and codebase instead of overwriting them.
4. **Eve** (QA) will audit the new changes against the existing context to ensure nothing was broken.

---
The fleet provides multiple ways to monitor the active pipeline.

### Dashboard (HTTP)
- **Local**: `http://localhost:8000`
- **Mobile/Remote**: Check the Telegram notification for the generated **Ngrok** URL (Port 8000).

### MVP Deployment (HTTP)
- **Local**: `http://localhost:5000` (Default port for Alan's MVPs)
- **Mobile/Remote**: Check the Telegram notification for the second **Ngrok** URL (Port 5000). You can now view the generated product directly on your phone!

### Logs
- **System Logs**: View stdout/stderr of the `start_fleet.py` process.
- **Project Context**: Each task stores its current state in:
  `marcus-fleet/projects/{TASK_ID}/context.json`
---

## 🛠️ 3. Process Control
The fleet runs as a collection of sub-processes managed by `start_fleet.py`.

### Force Kill Everything
```bash
pkill -9 -f "uvicorn" || true; pkill -9 -f "start_fleet.py" || true; pkill -9 -f "ngrok" || true
```

### Restart Fleet
```bash
python3 start_fleet.py
```

---

## 📁 4. Output Locations
- **Research/PRD/SDD**: Generated in the project folder:
  `marcus-fleet/projects/{TASK_ID}/`
- **Source Code**: Generated in subfolders under the task directory:
  `marcus-fleet/projects/{TASK_ID}/src/`
---

## 🤖 5. Integration Tips for Bots
- **Polling**: A bot can poll the `projects/` directory to detect new files.
- **Telegram Bridge**: All critical phase completions and files are sent via `notifier.py` to the linked Telegram bot.
