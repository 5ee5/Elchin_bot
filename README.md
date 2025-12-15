# Elchin Discord Bot

A Python Discord bot for personal or server use. This repository includes the bot code, dependency setup, and an optional systemd service file for running it automatically.


## Requirements

- Python 3.10+
- [pip](https://pip.pypa.io/en/stable/installation/)
- Optional: Linux systemd for service management

---

## Installation

1. Clone the repository:

```bash
git clone https://github.com/5ee5/Elchin_bot.git
cd Elchin_bot
```

2. Create a virtual environment:
```bash
python3 -m venv .venv
source .venv/bin/activate
```

3. Create `.env` file with this content:
```bash
DISCORD_TOKEN=YOUR_TOKEN
GEMINI_API_KEY=YOUR_API_KEY
```

4. Install dependencies:
```bash
pip install -r requirements.txt
```

5. Run the bot:
```bash
python3 Elchin_bot.py
```

---

## Running bot automatically in the background


1. Copy the service file to systemd:
```bash
sudo cp systemd/elchin_bot.service /etc/systemd/system/
```

2. Reload systemd daemon:
```bash
sudo systemctl daemon-reload
```

3. Enable and start the service:
```bash
sudo systemctl enable --now elchin_bot
```
