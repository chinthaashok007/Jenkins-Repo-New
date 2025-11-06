🧱 Jenkins Interview Preparation Notes

💡 NOTE:
While I have prepared all the questions, the answers below are based on my personal knowledge and references from Medium, Stack Overflow, and ChatGPT for better clarity and completeness.

🚀 Q1: Can you explain the CI/CD process in your current project?

In my project, we use Jenkins as the core CI/CD orchestrator along with the following tools:

🧰 Tools Used:
Maven, SonarQube, AppScan, ArgoCD, Kubernetes

🧩 Implementation Flow (8 Steps)

Code Commit: Developers push code to GitHub.

Build: Jenkins triggers a Maven build and runs unit tests.

Code Analysis: SonarQube scans for bugs and vulnerabilities.

Security Scan: AppScan performs deep security analysis.

Deploy to Dev: Jenkins deploys the app to Kubernetes (Dev).

Continuous Deployment: ArgoCD auto-deploys changes from Git.

Promote to Prod: Manual promotion using ArgoCD.

Monitoring: Continuous performance monitoring via Kubernetes tools.

⚙️ Q2: What are different ways to trigger Jenkins pipelines?

There are multiple trigger mechanisms available:

🕒 Poll SCM: Jenkins periodically checks for code changes.

🧩 Build Triggers: Automatically build when changes are pushed to Git.

🌐 Webhooks: GitHub notifies Jenkins instantly upon new commits.

💾 Q3: How to backup Jenkins?

You can backup Jenkins by saving essential directories and configurations.

🧱 Components to Backup:

Configuration: ~/.jenkins folder

Plugins: JENKINS_HOME/plugins

Jobs: JENKINS_HOME/jobs

User Content: Custom scripts and artifacts

Database: Use tools like mysqldump if DB is used

🕑 Tip: Automate backups using cron or Task Scheduler for daily/weekly runs.

🔐 Q4: How do you store or handle secrets in Jenkins?

Several secure methods are available for handling secrets:

🔑 Credentials Plugin: Safely store passwords, API keys, tokens.

⚙️ Environment Variables: Easy but less secure.

🏦 HashiCorp Vault: Integrate for secure, centralized secrets.

☁️ Cloud Secret Managers: Use AWS Secrets Manager, Azure Key Vault, etc.

🧮 Q5: What is the latest version of Jenkins?

📘 Always check the official Jenkins Website
 before interviews — version numbers change frequently.
This question checks your hands-on familiarity.

📦 Q6: What are shared modules in Jenkins?

Shared modules allow reusability and consistency across pipelines.

🧰 Libraries: Reusable scripts and functions

🧾 Shared Jenkinsfile: One file used for multiple pipelines

🔌 Plugins: Common plugin setups

🌍 Global Variables: Manage versions, URLs, and constants globally

🧠 Q7: Can Jenkins build multi-language applications using different agents?

✅ Yes!
Jenkins supports multiple agents, each configured for different languages and environments.

Example:

One agent builds Java apps

Another builds Node.js apps

🔄 This ensures proper dependencies and tools for each language.

☁️ Q8: How to setup Auto Scaling Group for Jenkins in AWS?

Here’s a high-level setup flow:

🚀 Launch EC2 Instance: Install Jenkins on a base AMI.

⚙️ Create Launch Configuration: Define instance type, security groups, and key pairs.

🧩 Create Auto Scaling Group: Set min, max, and desired capacity.

📈 Configure Scaling Policy: Scale based on CPU or request count.

🌐 Load Balancer: Forward traffic using ELB.

🔗 Connect to Jenkins: Use ELB DNS or instance IP.

📊 Monitor: Track with Amazon CloudWatch.

🧩 Q9: How to add a new worker node in Jenkins?

Steps:

Navigate to Manage Jenkins → Manage Nodes → New Node

Enter name → select Permanent Agent

Configure SSH details → click Launch

🧰 Q10: How to add a new plugin in Jenkins?

Using CLI:

java -jar jenkins-cli.jar install-plugin <PLUGIN_NAME>


Using Jenkins UI:

Go to Manage Jenkins → Manage Plugins

Search and install the required plugin.

🌐 Q11: What is JNLP and why is it used in Jenkins?

JNLP (Java Network Launch Protocol) enables remote Jenkins agents to connect securely with the master node.
It helps distribute builds across multiple agents → better scalability and parallelism.

🔌 Q12: What are some common Jenkins plugins you use?

Always mention at least 3–4 plugins you use frequently:

🔹 Git Plugin

🔹 Pipeline Plugin

🔹 Credentials Binding Plugin

🔹 SonarQube Plugin

🔹 Docker Plugin

✨ Pro Tip

Keep your Jenkins setup modular, secure, and version-controlled.
Adopt GitOps practices for automation and scalability.
