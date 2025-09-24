 📹 CamAlive – AI for Your CCTV Cameras  

CamAlive is a software solution that transforms regular CCTV cameras into AI-powered security systems.  
It adds real-time detection, analysis, reporting, and escalation capabilities to any IP camera without replacing existing hardware.  

---

## ✨ Features
- 🔒 **Intrusion Detection** – detect unauthorized entries or perimeter breaches  
- 👥 **Chaos & Incident Detection** – detect fights, unrest, or abnormal crowd behavior  
- 🔥 **Fire, Smoke & Flood Detection** – prevent disasters before escalation  
- 🧑‍🤝‍🧑 **Face & License Plate Recognition** (optional add-on)  
- 📢 **Smart Escalation System** – alerts security, supervisors, and authorities in order  
- 📊 **Dashboard & Logs** – track alerts, generate reports, and analyze incidents  

---

## 🏗️ System Architecture
```text
Camera Snapshot → WordPress Plugin → n8n Webhook → Python AI → n8n → User Alerts
                                                 ↓
                                          WordPress Alert Log


WordPress Plugin: Admin dashboard, camera registration, snapshot fetching

Python AI Engine: Analyzes snapshots for intrusion, fire, chaos, license plates

n8n: Automation layer — routes alerts to WhatsApp, Telegram, Email, or IoT devices

📸 Example Alert
{
  "event": "chaos_detected",
  "confidence": 0.88,
  "camera": "gate-entrance",
  "timestamp": "2025-10-10T11:25:00Z"
}


📲 WhatsApp message:

🚨 CamAlive Alert
Camera: Gate Entrance
Event: Chaos / Crowd Incident
Confidence: 88%
Time: 11:25 AM

🚀 Getting Started
1. Clone the Repo
git clone https://github.com/<your-org>/camalive.git
cd camalive

2. WordPress Plugin

Copy wordpress-plugin/ into wp-content/plugins/

Activate CamAlive in WP Admin → Plugins

Add camera details (Name, Snapshot URL, n8n Webhook)

3. Python AI Service
cd python-service
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
uvicorn app:app --reload --port 8001

4. n8n Workflow

Import n8n-flows/alerts.json into n8n

Configure WhatsApp/Twilio API credentials

Ensure webhook URL matches WordPress settings

🖥️ Tech Stack

WordPress (PHP/MySQL) → Dashboard & Camera Management

Python (FastAPI, OpenCV, PyTorch) → AI Analysis Engine

n8n (Node.js) → Automation & Alerting

Optional: Docker for containerized deployment

📂 Repository Structure
camalive/
├── wordpress-plugin/ # WordPress plugin for dashboard
├── python-service/ # AI detection microservice
├── n8n-flows/ # Exported n8n automation workflows
├── INSTALLATION.md # Detailed installation instructions
├── USAGE.md # How to use the system
└── ARCHITECTURE.md # System design and diagrams

🎯 Use Cases

🏢 Corporate Offices – detect intrusions or workplace incidents

🏫 Schools & Campuses – monitor fights, chaos, or unauthorized entries

🏥 Hospitals – detect emergencies or fire/flood hazards

🏘️ Residential Estates – protect perimeters and escalate to security teams

🛒 Retail & Malls – track theft, chaos, or overcrowding

🤝 Contributing

Contributions are welcome!

Fork the repo

Create your feature branch (git checkout -b feature/amazing-feature)

Commit your changes (git commit -m 'Add amazing feature')

Push to the branch (git push origin feature/amazing-feature)

Open a Pull Request

📜 License

MIT License © 2025 Engr Julius Raphael Ochai | Codemi Technologies LLC

🌍 Vision

CamAlive aims to democratize AI surveillance by making advanced security accessible with any regular CCTV system.
We believe in smarter, safer, and more connected communities — powered by AI.
