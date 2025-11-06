🧱 Jenkins Interview Preparation Notes

💡 NOTE: While I have prepared all the questions, the answers below are based on my personal knowledge and references from Medium, Stack Overflow, and ChatGPT for better clarity and completeness.

---

🚀 Q1: Can you explain the CI/CD process in your current project?

In my project, we use Jenkins as the core CI/CD orchestrator, integrated with the following tools:

🧰 Tools Used: Maven · SonarQube · AppScan · ArgoCD · Kubernetes

🧩 Implementation Flow (8 Steps)

Code Commit: Developers push code to GitHub.

Build: Jenkins triggers a Maven build and runs unit tests.

Code Analysis: SonarQube scans for bugs and vulnerabilities.

Security Scan: AppScan performs deep security analysis.

Deploy to Dev: Jenkins deploys the app to Kubernetes (Dev).

Continuous Deployment: ArgoCD automatically deploys new commits.

Promote to Prod: Manual promotion using ArgoCD.

Monitoring: Continuous performance monitoring via Kubernetes tools.

---

⚙️ Q2: What are different ways to trigger Jenkins pipelines?

Jenkins supports multiple pipeline triggers:

🕒 Poll SCM: Periodically checks for code changes.

🧩 Build Triggers: Automatically runs builds when new commits are pushed.

🌐 Webhooks: GitHub instantly notifies Jenkins about new commits or PRs.

---

💾 Q3: How to backup Jenkins?

To ensure data safety, regularly back up key Jenkins directories.

🧱 Components to Backup

🧩 Configuration: ~/.jenkins folder

🔌 Plugins: JENKINS_HOME/plugins

📁 Jobs: JENKINS_HOME/jobs

📜 User Content: Custom scripts and artifacts

🗃️ Database: Use mysqldump if Jenkins data is stored in a database

🕑 Pro Tip: Automate backups with cron jobs or Task Scheduler (daily/weekly).

---

🔐 Q4: How do you store or handle secrets in Jenkins?

There are several secure ways to handle credentials in Jenkins:

🔑 Credentials Plugin: Safely store passwords, tokens, and API keys.

⚙️ Environment Variables: Simple but less secure option.

🏦 HashiCorp Vault: External and centralized secret management.

☁️ Cloud Secret Managers: AWS Secrets Manager · Azure Key Vault · GCP Secret Manager

---

🧮 Q5: What is the latest version of Jenkins?

📘 Always check the official Jenkins website
 before interviews — version numbers change frequently.
🧩 Interviewers ask this to verify if you’re actively using Jenkins.

---

📦 Q6: What are shared modules in Jenkins?

Shared modules help improve reusability and consistency across pipelines.

🧰 Libraries: Reusable Groovy scripts or shared functions

🧾 Shared Jenkinsfile: Single Jenkinsfile for multiple jobs

🔌 Plugins: Centralized common plugin usage

🌍 Global Variables: Shared constants like versions or URLs

---

🧠 Q7: Can Jenkins build multi-language applications using different agents?

✅ Yes! Jenkins supports multiple agents for different languages or platforms.

Example:

☕ One agent builds Java apps

🟩 Another builds Node.js apps

This ensures that proper dependencies and tools are available per language.

---

☁️ Q8: How to set up an Auto Scaling Group for Jenkins in AWS?
🚀 Setup Overview

Launch EC2 Instance: Install Jenkins and create a base AMI.

Create Launch Configuration: Define instance type, storage, and security groups.

Create Auto Scaling Group: Set minimum, maximum, and desired instances.

Configure Scaling Policy: Scale up/down based on CPU utilization.

Load Balancer: Use ELB to distribute incoming traffic.

Connect to Jenkins: Access via ELB DNS or instance IP.

Monitor: Use CloudWatch for metrics and health checks.

---

🧩 Q9: How to add a new worker node in Jenkins?

Steps:

Go to Manage Jenkins → Manage Nodes → New Node

Enter a node name → choose Permanent Agent

Configure SSH details → click Launch

---

🧰 Q10: How to add a new plugin in Jenkins?

Using CLI:

java -jar jenkins-cli.jar install-plugin <PLUGIN_NAME>


Using UI:
Manage Jenkins → Manage Plugins → Available → Search → Install

---

🌐 Q11: What is JNLP and why is it used in Jenkins?

JNLP (Java Network Launch Protocol) allows remote Jenkins agents to connect securely to the master.
It enables distributed builds for better scalability and performance.

---

🔌 Q12: What are some common Jenkins plugins you use?

Always mention at least 3–4 frequently used plugins:

🔹 Git Plugin – Source code management

🔹 Pipeline Plugin – For declarative and scripted pipelines

🔹 Credentials Binding Plugin – Secure secrets injection

🔹 SonarQube Plugin – Code quality analysis

🔹 Docker Plugin – Build and deploy using containers

---

✨ Pro Tip

Keep your Jenkins setup modular, secure, and version-controlled.
Adopt GitOps practices for maximum automation and scalability.
