# 🚀 Dockerized Flask Application with Trivy Security Scan

This repository contains a simple **Flask web application**, containerized using **Docker** and secured with **Trivy** vulnerability scanning integrated through **GitHub Actions**.

---

## 📌 Features

- ✅ Minimal Flask application
- 🐳 Dockerized using Python 3.10 slim image
- 🔐 Automated Docker image vulnerability scanning with Trivy
- 🤖 CI/CD workflow with GitHub Actions
- 🔔 Slack notification on scan failure (HIGH/CRITICAL vulnerabilities)

---

## 🧾 Project Structure

```
.
├── app.py                     # Flask application
├── requirements.txt           # Python dependencies
├── Dockerfile                 # Dockerfile for image build
├── .github
│   └── workflows
│       └── trivy-scan.yml     # GitHub Actions workflow for Trivy scan
└── README.md                  # Project documentation
```

---

## ⚙️ Setup Instructions

### 🔧 Prerequisites

- Docker installed
- Python 3.10+ (if testing locally without Docker)
- GitHub repository (for CI/CD pipeline)

---

## 🐳 Running Locally with Docker

1. Clone the repository:

```bash
git clone https://github.com/your-username/flask-docker-app.git
cd flask-docker-app
```

2. Build the Docker image:

```bash
docker build -t flask-docker-app .
```

3. Run the container:

```bash
docker run -p 5000:5000 flask-docker-app
```

4. Visit in browser:

```
http://localhost:5000
```

---

## 🤖 GitHub Actions - Trivy Security Scan

The GitHub Actions workflow `.github/workflows/trivy-scan.yml` performs the following:

- 📦 Builds the Docker image
- 🕵️ Runs Trivy to scan for HIGH/CRITICAL vulnerabilities
- 📄 Uploads scan report as artifact
- 🚨 Sends Slack alert if vulnerabilities found

### 🔐 Add Secret for Slack Notification

Go to your GitHub repo → **Settings** → **Secrets and variables** → **Actions** → **New repository secret**:

| Name               | Value                          |
|--------------------|--------------------------------|
| `SLACK_WEBHOOK_URL`| Your Slack Incoming Webhook URL|

---

## 🧪 Sample Output

On successful run, you'll see:

```
Hello from Dockerized Flask App!
```

And on GitHub Actions:
- ✅ Green check for no critical issues
- 🚨 Slack alert if any found

---

## 📋 Technologies Used

- [Flask 2.3.3](https://flask.palletsprojects.com/)
- [Docker](https://www.docker.com/)
- [GitHub Actions](https://github.com/features/actions)
- [Trivy](https://github.com/aquasecurity/trivy)

---

## 📝 License

This project is licensed under the [MIT License](LICENSE) — feel free to use and modify.

---

## 🙌 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

---




