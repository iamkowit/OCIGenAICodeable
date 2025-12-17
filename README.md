# 🚀 OCI GenAI Codable - Powered by OCI Generative AI

**OCI GenAI Codable** empowers developers with an enterprise-grade AI assistant directly within the IDE, securing your intellectual property while leveraging the power of Oracle Cloud Infrastructure (OCI) Generative AI Service.

## ✨ Key Product Features

### 🤖 Intelligent AI Agent
Connects securely to OCI-hosted LLMs to provide context-aware coding assistance without data leaving your compliance boundary.

### 🌟 Three Specialized Modes
1. **Agent Mode** 👨‍💻
   - **Smart Coding Partner:** Expert pair programmer that writes, refactors, and debugs code.
   - **Two-Phase Workflow:** Always presents a **Preview** of changes for your approval before writing any code.
   - **Context Verification:** Eliminates hallucinations by verifying file existence and structure.

2. **Plan Mode** 🧠
   - **Strategic Architect:** Analyzes high-level requirements to generate comprehensive implementation plans.
   - **Structured Execution:** Breaks projects into phases and tasks with defined dependencies.
   - **Risk Analysis:** Proactively identifies architectural risks and edge cases.

3. **Canvas Mode** 🎨
   - **Instant Visual Generation:** Creates Presentations, Landing Pages, Dashboards, and Diagrams from text.
   - **Live Editing:** Tweak generated designs in real-time with an interactive preview.
   - **Exportable Formats:** Save your designs as React components, HTML, or images.
   - **Example Prompts:**
     - 📊 **Analytics View:** "Create a dashboard showing quarterly revenue growth."
     - 📽️ **Presentation:** "Generate a slide deck for a project kickoff meeting."
     - 🌐 **Landing Page:** "Design a landing page for a new coffee shop."
     - 🆚 **Versus Layout:** "Compare React vs Vue in a side-by-side layout."
     - 📅 **Visual Timeline:** "Show the history of oracle company on a timeline."
     - 📈 **Infographic:** "Visualize the benefits of cloud migration."
     - 📄 **Research Paper**: "Generate a research paper on the impact of AI on climate change."
     - 🔄 **Interactive Diagram:** "Create an interactive diagram for a presentation."
     - 🎴 **Bento Grid:** "Create a bento grid for a presentation."
     - 📋 **Document Layout:** "Create a document layout for a presentation."
     - 📝 **Document:** "Create a document for a presentation."



### 💼 Enterprise Capabilities
- **🔒 Private & Secure:** Direct connection to your OCI Tenancy. No third-party API brokers.
- **📝 Document Export:** Export technical plans and chat logs to **Microsoft Word (.docx)** for documentation.
- **🏗️ Multi-Language:** Native support for Java, Python, TypeScript, Go, and PL/SQL.

---

## 🛠️ Setup Guide

Follow these steps to configure your environment for OCI GenAI Agent.

### 1️⃣ Prerequisites
- An active **Oracle Cloud Infrastructure (OCI)** Account.
- A user account with permissions to manage API keys.
- Access to **OCI Generative AI Service** (Check region availability).

### 2️⃣ Installation
1. Install **OCI GenAI Codable** editor (or the `oci-genai` extension).
2. Open the IDE and look for the **OCI GenAI** icon in the activity bar.

### 3️⃣ OCI Configuration & API Key
The agent uses the standard OCI SDK authentication method. You need to create a config file at `~/.oci/config` (Linux/Mac) or `%USERPROFILE%\.oci\config` (Windows).

**Step 3.1: Generate API Key**
1. Log in to OCI Console.
2. Go to **Identity & Security** > **Users** > Select your user.
3. Click **API Keys** > **Add API Key**.
4. Download the **Private Key** and save it securely (e.g., `~/.oci/oci_api_key.pem`).
5. Copy the **Configuration File Preview** snippet shown in the console.

**Step 3.2: Create Config File**
Create `~/.oci/config` and paste the snippet. It should look like this:

```ini
[DEFAULT]
user=ocid1.user.oc1..aaaaaaaaxxxxxxxxxx
fingerprint=xx:xx:xx...
key_file=~/.oci/oci_api_key.pem
tenancy=ocid1.tenancy.oc1..aaaaaaaaxxxxxxxxxx
region=us-chicago-1
# IMPORTANT: Add your Compartment ID for GenAI requests
compartment_id=ocid1.compartment.oc1..aaaaaaaaxxxxxxxxxx
```

> **Note:** You MUST add the `compartment_id` field to your profile. This tells the agent where to run the GenAI workload. Currently, OCI GenAI Codeable supported only in `us-chicago-1`. You need to set this region as your home region or subscribe to it.

### 4️⃣ OCI IAM Policies
Ensure your user group has permission to use the Generative AI service.

**Policy Statement:**
```hcl
Allow group <Your-Group-Name> to manage generative-ai-family in compartment <Your-Compartment-Name>
```

*Or for broader access:*
```hcl
Allow group <Your-Group-Name> to use generative-ai-family in tenancy
```

### 5️⃣ Verify Connection
1. Restart **OCI GenAI Codable**.
2. Open the **OCI GenAI** chat panel.
3. If configured correctly, you will see "Powered by Oracle Cloud Infrastructure Generative AI".
4. Type "Hello" to test the connection.

---

## ❓ Known Issues
- **Issue 1**: Slow Tailwind CDN loading; implement local caching.
- **Issue 2**: Canvas Mode: Enhance Visualizer.
```

