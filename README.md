# Admiral AI in Engineering Hackathon 2024: Cloud Workstations Setup Guide

Welcome to the Admiral Hackathon! This guide will walk you through setting up your Google Cloud Workstation, which comes pre-configured with essential tools like Claude Code, MongoDB, and PostgreSQL, to get you started quickly on your projects.

---

### What are Cloud Workstations?

**Cloud Workstations** is a fully managed development environment service in Google Cloud that provides secure, scalable, and customizable development workstations hosted in the cloud. Instead of developing directly on your local machine, your IDE and all your development tools run on a powerful virtual machine in Google Cloud.

**Key Benefits:**
* **Security:** Your code and development environment remain secure within Google Cloud's infrastructure, reducing risks associated with local development.
* **Performance:** Access powerful, scalable computing resources in the cloud, allowing for faster builds, tests, and overall development workflows, without impacting your local machine's performance.
* **Consistency:** Every developer gets a standardized, pre-configured environment, eliminating "it works on my machine" issues and speeding up team onboarding.
* **Flexibility:** You can access your consistent development environment from any device with a browser, or integrate with your local VS Code or Cursor AI editor for a familiar experience with a cloud backend.
* **Centralized Management:** Simplify the management of dependencies, security patches, and tool updates across all developer environments.

Your Cloud Workstation comes pre-configured with essential tools like Claude Code, MongoDB, and PostgreSQL, to get you started quickly on your projects.

---

### 1. Login to GCP & Set Your Project

Your first step is to log in to the Google Cloud Console and select your assigned project.

* Go to `https://console.cloud.google.com`.
* Use the login details (email and password) that were shared with you via email.
* Accept the Terms of Service if prompted.
* Once logged in, click on the **"Select a project"** dropdown at the top of the page.
* Choose the specific hackathon project assigned to your team from the list.

<img src="assets/01-login-and-set-project.gif" alt="Login to GCP and Set Project">

---

### 2. Create and Start Your Workstation

Now you'll create and start your personal Cloud Workstation.

* Use the **search bar** at the top of the Google Cloud Console page and type `/workstations`.
* Select the **"Workstations"** service from the search results.
* On the Workstations page, click the **"Create Workstation"** button.
* For the **Display Name**, simply enter your name (e.g., "JaneDoe-workstation").
* Under **Configuration**, select `'admiral-hackathon-config'`. This is our custom image pre-installed with tools like Claude Code, MongoDB, and PostgreSQL to streamline your development.
* Once created, you will see your workstation listed. Click the **"Start"** button next to your workstation's name.
* Please note: The workstation may take approximately one minute to start up.

<img src="assets/02-start-workstation.gif" alt="Create and Start Workstation">

---

### 3. Launch Your Workstation & Initial Setup

After your workstation has started, you can launch your IDE and proceed with initial setup steps.

* Once the workstation is ready, the "Start" button will change to **"Launch"**.
* Click **"Launch"** to open your IDE in a new browser window.
* **First-Time Setup:** Upon starting a workstation for the first time, a number of background scripts will run to pre-install VS Code extensions and apply basic settings. You will know this process is complete when the theme of the IDE automatically changes to dark mode.

#### Sign in to Cloud Code

**Cloud Code** is a set of powerful tools and extensions for popular IDEs (like VS Code) that helps you write, deploy, and debug cloud-native applications directly from your development environment. It provides integrated support for Google Cloud services, Kubernetes, Cloud Run, and more, significantly streamlining your workflow for Google Cloud development.

* Once your IDE is open, click the **Cloud Code button** (usually a Google Cloud icon) located in the **bottom status bar** of the IDE.
* This will prompt you to authenticate your Google Cloud account. Follow the on-screen instructions to complete the authentication process.
* Once authenticated, click the Cloud Code button again and select the hackathon project assigned to you.

#### Optional: Sign in to Gemini Code Assist

* Click the **Gemini Symbol** from the **Extensions view** (usually the square icon on the left sidebar in VS Code).
* Click **"Select a Google Cloud project"** and select the hackathon project assigned to you.
* **Please Note:** Gemini Code Assist's full coding agent functionality is scheduled for release next month. While you can sign in and explore current features, its primary use as a robust coding agent for this hackathon might be limited. Therefore, signing into Gemini Code Assist is optional for the purposes of this hackathon, which is focused on exploring coding agents.

<img src="assets/03-launch-workstation-cloud-code-sign-in.gif" alt="Launch Workstation and Cloud Code Sign-in">

---

### 4. Launching Claude Code

Your custom image has Claude Code pre-installed. To use it, you'll need an API key from Anthropic which has been shared with you separately. Speak to Himanshu/Andy for details.

* **Launch Claude Code:**
    * Open a **new terminal window** within your VS Code IDE (Terminal > New Terminal).
    * Type `claude` and follow the on-screen instructions to authenticate with Claude.

<img src="assets/04-launch-claude.gif" alt="Launch Claude Code">

---

### 5. Advanced Setup: Remote Development with Local VS Code or Cursor AI

For experienced users who prefer their local development environment but want to leverage the powerful backend of the Cloud Workstation, you can use remote development.

**This is applicable for both VS Code and Cursor AI editors.**

**Benefits:**
* **Install Any Software:** You can install specific software or tools directly on your Cloud Workstation that you might not have permissions to install on your local laptop.
* **Powerful Backend:** Utilize the workstation's robust compute resources (CPU, RAM, GPU if configured) for heavy tasks, while still using your familiar local IDE interface.

**Instructions:**
Detailed instructions on how to set this up can be found in the official Google Cloud Workstations documentation:
[Develop code using a local VS Code editor](https://cloud.google.com/workstations/docs/develop-code-using-local-vscode-editor)

---

### 6. Known Issues

#### "Unable to forward your request to a backend" Error

Occasionally, upon starting your workstation, you might encounter an error message in your browser stating: "Unable to forward your request to a backend" with details about not being able to connect to port 80.

<img src="assets/99-unable-to-forward-request-to-backend.png" alt="Unable to forward request to backend">

**Solution:**
This is typically a transient issue. If you see this message, simply **retry launching the IDE** by clicking the "Launch" button again in the Cloud Workstations console. It should work fine on the second attempt.

#### Claude Code Authentication "Not Found" Error

When authenticating with Claude Code, Code OSS may try to redirect to an external website, leading to a "Not Found" error in the browser.

**Solution:**
Instead of clicking "Open" on the Code OSS prompt, **use the URL printed in the terminal** (which typically starts with `https://console.anthropic.com/oauth...`). Copy this URL and paste it directly into your browser to complete the authentication.

---

We hope you have a productive and exciting hackathon! Good luck!