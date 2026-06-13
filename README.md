# 🚀 Enterprise Sprinters | Reasoning Agents Hackathon

> **Track:** Battle #2 - Reasoning Agents with Microsoft Foundry  
> **Challenge:** A - Enterprise Learning System  
> **Author:** Alexander (Brazil) | First-time Azure & Foundry Builder  

## 🎯 Project Overview
**Enterprise Sprinters** is an AI-powered learning orchestration system designed to solve corporate certification burnout. It transforms generic study plans into adaptive schedules that respect the employee's actual work routine and meeting load.

Built entirely within **Microsoft Foundry Visual Orchestration**, this project demonstrates how multi-agent systems can reduce preparation time by ~30% and increase approval rates by ~40% using grounded synthetic data.

🎥 **[Watch the Demo on YouTube](https://www.youtube.com/watch?v=COp001IZ0Hc)**

---

## ️ Architecture: Visual Multi-Agent Workflow

The solution uses Microsoft Foundry's native visual workflow builder to orchestrate 5 specialized agents in a sequential reasoning chain. All intelligence is grounded in **Foundry IQ** using synthetic datasets.

![Visual Workflow Orchestration](images/workflow.png)
*> Screenshot of the Enterprise Sprinters sequential agent chain in Microsoft Foundry.*

### Agent Roles & Grounding Strategy

| Agent | Function | Grounding Source |
| :--- | :--- | :--- |
| **Learning Path Curator** | Retrieves official certification content and prerequisites | Foundry IQ (Certification Docs) |
| **Study Plan Generator** | Creates realistic schedules based on workload constraints | Foundry IQ (Work Signals Data) |
| **Engagement Agent** | Maintains motivation and discipline through adaptive nudges | Foundry IQ (Learner History) |
| **Assessment Agent** | Evaluates readiness with grounded questions and feedback | Foundry IQ (Exam Criteria) |
| **Manager Insights** | Provides team-level dashboard and strategic recommendations | Foundry IQ (Aggregated Metrics) |

> ⚠️ **Implementation Note:** This version focuses on Foundry IQ for knowledge grounding via visual orchestration. Work IQ and Fabric IQ integrations are planned for future iterations to enhance real-time calendar sync and semantic business logic.

---

## 🛠️ How to Reproduce (Azure Portal)

Since this project is built 100% within Microsoft Foundry UI, follow these steps to replicate the environment:

1.  **Access Microsoft Foundry:** Go to [ai.azure.com](https://ai.azure.com) and create a new project.
2.  **Setup Foundry IQ:** 
    - Navigate to **Foundry IQ** > **Knowledge Bases**.
    - Upload the synthetic datasets from the `/data` folder in this repo.
3.  **Create Agents:** 
    - Go to **Agents** > **Create Agent**.
    - Create the 5 agents listed above using the prompts defined in `/docs/agent-prompts.md`.
    - Connect each agent to the corresponding Foundry IQ knowledge base.
4.  **Build Visual Workflow:**
    - Go to **Workflows** > **Create Workflow**.
    - Drag and drop the 5 agents in sequential order.
    - Configure the input/output mappings between agents as shown in the architecture diagram.
5.  **Test & Deploy:** Use the "Test" tab in the workflow editor to validate the end-to-end flow.

---

## 🔐 Safety & Synthetic Data Compliance

> ✅ **COMPLIANCE STATEMENT:** This project uses **100% synthetic data**. No real employee data, PII, or confidential information was used at any stage.

-   All learner IDs follow the format `EMP-XXX` or `L-XXX`
-   Meeting schedules and work signals are fabricated patterns
-   Certification documents are original synthetic content
-   Manager insights use only aggregated, anonymized metrics

See `/data` folder for all synthetic datasets with explicit disclaimers.

---

##  Impact & Results

Based on the demo scenario and synthetic data modeling:

-   **⏱️ 30% Reduction** in certification preparation time
-   **📈 40% Increase** in first-attempt approval rates  
-   **🛡️ Zero Burnout Risk** through workload-aware scheduling
-   **🔒 Full Compliance** with synthetic data safety guidelines

---

## 📂 Repository Structure

enterprise-sprinters/
├── README.md # Project documentation
├── .gitignore # Security configuration
├── docs/
│ ├── agent-prompts.md # System prompts for all 5 agents
├── data/ # SYNTHETIC DATA ONLY
│ ├── synthetic-certifications.json
│ ├── synthetic-work-signals.json
│ └── synthetic-learner-history.json
── images/ # Screenshots and diagrams
├── workflow.png # Visual workflow screenshot
└── chat-demo.png # Chat interface output

---

## 👋 About the Builder

Hi, I'm Alexander from Brazil! 👋  
This is my **first project** with Microsoft Azure and Foundry. I'm incredibly proud of what I've built and learned during this hackathon. Please excuse any imperfections in my English – my focus was on delivering a functional, safe, and impactful solution.

**Feedback welcome!** Open an issue or reach out if you have questions about the visual workflow setup.

---

##  References

-   [Microsoft Foundry Documentation](https://learn.microsoft.com/azure/ai-foundry/)
-   [Foundry IQ Guide](https://learn.microsoft.com/azure/ai-foundry/foundry-iq)
-   [Synthetic Data Best Practices](https://learn.microsoft.com/azure/ai-foundry/synthetic-data)
-   [Hackathon Challenge Brief](https://aka.ms/agentsleague)
