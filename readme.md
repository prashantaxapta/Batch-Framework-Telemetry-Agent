# 🚀 Batch Telemetry Agent

## 📚 Table of Contents
- [Overview](#-overview)
- [Key-Capabilities](#-key-capabilities)
- [Architecture](#-architecture)
- [Prerequisites](#-prerequisites)
-   [Step-1---Telemetry-Configuration](#-step-1---telemetry-configuration)
-   [Step-2---Agent-Deployment](#-step-2---agent-deployment)
-   [Step-3---Knowledge-Source-Integration](#-step-3---knowledge-source-integration)
- [Usage](#-usage)
- [Resources](#-resources)
- [Contributors](#-contributors)

## 🧠 Overview

The Batch Telemetry Agent is an AI-powered monitoring and diagnostic solution designed to optimize batch job execution within Dynamics 365 SCM & Finance. It leverages telemetry streamed into Azure Application Insights and integrates with **Copilot Studio** to provide actionable insights, alerts, and automation capabilities.

## 🔧 Key Capabilities

- **Telemetry Collection**: Captures signals such as job start/end times, thread usage, throttling metrics, queue sizes, failures, and Infolog errors.
- **Prompt-Based Analysis**: Uses GPT-4o and GPT-5 models to interpret telemetry data via natural language prompts.
- **Anomaly Detection**: Applies Kusto (KQL) queries and AI models to detect performance degradation and scheduling inefficiencies.
- **Self-Healing Options**: Supports guided or autonomous remediation actions like restarting failed jobs.
- **Visualization & Reporting**: Offers dashboards for workload distribution, priority spread, throttling trends, and batch exceptions.

## 🏗️ Architecture

<p align="center">
  <img src="./Images/Architecture.png" alt="Batch Framework Telemetry Agent Architecture" width="1500"/>
</p>

- **Telemetry Flow**: Batch Telemetry events from D365 F&O are streamed to Application Insights.
- **Agent Logic**: Queries telemetry periodically or on-demand, evaluates rules, and stores results in Dataverse.
- **User Interaction**: Users engage via Copilot chat, M365 chat, or Teams channels.
- **Remediation Execution**: Actions are triggered via MCP Server and verified through telemetry feedback loops.

## ✅ Prerequisites

- Dynamics 365 Finance & Supply Chain version 10.0.45(7.0.7690.21 PU69 or later
- Azure Application Insights configured for batch telemetry
- Access to Copilot Studio and Power Automate

## 🛠️ Step 1 - Telemetry Configuration

- Ensure batch telemetry is enabled in D365 F&O and connected to Application Insights  
  [Monitoring Telemetry](https://learn.microsoft.com/en-us/dynamics365/fin-ops-core/dev-itpro/monitoring-telemetry/)  
  [Getting Started](https://learn.microsoft.com/en-us/dynamics365/fin-ops-core/dev-itpro/monitoring-telemetry/monitoring-getting-started)

## 🛠️ Step 2 - Agent Deployment

- Import the agent canvas app into Copilot Studio.
- Configure prompts and remediation rules.
- Set up Power Automate flows for notifications.

## 🛠️ Step 3 - Knowledge Source Integration

- Connect Microsoft Learn Docs MCP Server for contextual guidance.


## 🧪 Usage

### 💬 Prompt Examples

- "Show me batch jobs throttled in the last 7 days."
- "What are the top 3 batch jobs causing latency spikes?"
- "Suggest optimal scheduling time for job P-0001."

### ⚙️ Automation Scenarios

- Restart failed jobs based on error codes.
- Adjust job priorities based on historical performance.
- Notify admins via Teams when anomalies are detected.

## 📎 Resources

- [📦 Batch Telemetry Dashboard Release](https://github.com/microsoft/Dynamics-365-FastTrack-FSCM-Telemetry-Samples/releases/tag/Batch-1.0.0.0)
- [📘 Application Insights Documentation](https://learn.microsoft.com/en-us/dynamics365/fin-ops-core/dev-itpro/analytics/application-insights)

## 👥 Contributors

- Prashant Verma
- Hemanth Kumar

---

📬 For questions or support, contact the AI Business Solutions team or refer to the internal documentation shared via Teams and email.
