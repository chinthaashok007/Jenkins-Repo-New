## Jenkins Pipeline for Java based application using Maven, SonarQube, Argo CD, Helm and Kubernetes

---

<img width="930" height="460" alt="image" src="https://github.com/user-attachments/assets/5abf5b9a-64b8-4aa8-9ab0-ccb026f86342" />

Here are the step-by-step details to set up an end-to-end Jenkins pipeline for a Java application using SonarQube, Argo CD, Helm, and Kubernetes:

# 🚀 End-to-End Jenkins CI/CD Pipeline for Java Application

## 🧾 Prerequisites

- ☕ **Java application code** hosted on a Git repository  
- ⚙️ **Jenkins server**  
- ☸️ **Kubernetes cluster**  
- ⛵ **Helm package manager**  
- 🚀 **Argo CD**

---

## 🧩 Steps

### 🧱 1. Install the necessary Jenkins plugins

1.1 🧠 Git plugin  
1.2 ⚙️ Maven Integration plugin  
1.3 🧱 Pipeline plugin  
1.4 ☸️ Kubernetes Continuous Deploy plugin  

---

### ⚙️ 2. Create a new Jenkins pipeline

2.1 In Jenkins, create a new pipeline job and configure it with the Git repository URL for the Java application.  
2.2 Add a **Jenkinsfile** to the Git repository to define the pipeline stages.  

---

### 🏗️ 3. Define the pipeline stages

- **Stage 1:** Checkout the source code from Git.  
- **Stage 2:** Build the Java application using Maven.  
- **Stage 3:** Run unit tests using JUnit and Mockito.  
- **Stage 4:** Run SonarQube analysis to check the code quality.  
- **Stage 5:** Package the application into a JAR file.  
- **Stage 6:** Deploy the application to a test environment using Helm.  
- **Stage 7:** Run user acceptance tests on the deployed application.  
- **Stage 8:** Promote the application to a production environment using Argo CD.  

---

### 🔧 4. Configure Jenkins pipeline stages

- **Stage 1:** Use the **Git plugin** to check out the source code from the Git repository.  
- **Stage 2:** Use the **Maven Integration plugin** to build the Java application.  
- **Stage 3:** Use the **JUnit and Mockito plugins** to run unit tests.  
- **Stage 4:** Use the **SonarQube plugin** to analyze the code quality of the Java application.  
- **Stage 5:** Use the **Maven Integration plugin** to package the application into a JAR file.  
- **Stage 6:** Use the **Kubernetes Continuous Deploy plugin** to deploy the application to a test environment using Helm.  
- **Stage 7:** Use a testing framework like **Selenium** to run user acceptance tests on the deployed application.  
- **Stage 8:** Use **Argo CD** to promote the application to a production environment.  

---

### ☸️ 5. Set up Argo CD

- 🛠️ Install **Argo CD** on the Kubernetes cluster.  
- 📁 Set up a Git repository for Argo CD to track changes in Helm charts and Kubernetes manifests.  
- ⚙️ Create a **Helm chart** for the Java application that includes Kubernetes manifests and Helm values.  
- 🔗 Add the Helm chart to the Git repository that Argo CD is tracking.  

---

### 🔐 6. Configure Jenkins pipeline to integrate with Argo CD

6.1 Add the **Argo CD API token** to Jenkins credentials.  
6.2 Update the **Jenkins pipeline** to include the Argo CD deployment stage.  

---

### ▶️ 7. Run the Jenkins pipeline

7.1 Trigger the Jenkins pipeline to start the CI/CD process for the Java application.  
7.2 Monitor the pipeline stages and fix any issues that arise.  

---

## ✅ Summary

This end-to-end **Jenkins pipeline** automates the entire CI/CD process for a **Java application**, from **code checkout to production deployment**, using popular tools like:

- 🧠 **SonarQube**  
- 🚀 **Argo CD**  
- ⛵ **Helm**  
- ☸️ **Kubernetes**
