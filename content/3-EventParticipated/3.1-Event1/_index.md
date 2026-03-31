---
title: "Event 1"
date: 2026-03-31
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

{{% notice warning %}}
⚠️ **Note:** The information below is for reference purposes only. Please **do not copy it verbatim** into your report, including this warning.
{{% /notice %}}

# Summary Report: “GenAI-powered Cloud-Mastery 2026 workshop”

#### Some event photos
* Some photos from the workshop:

![Workshop photo 1](/images/3-EventParticipated/3.1-Event1/photo-1.jpg)
![Workshop photo 2](/images/3-EventParticipated/3.1-Event1/photo-2.jpg)
![Workshop photo 3](/images/3-EventParticipated/3.1-Event1/photo-3.jpg)

> Overall, the event not only provided technical knowledge but also helped me reshape my thinking about application design, system modernization, and cross-team collaboration.

---

## 1. Building AI Agent with Strands (Banh Cam Vinh)

### Event Objectives

- Introduce foundational **LLM** concepts and limitations of **standalone LLMs**.
- Explain why **AI Agents** are needed (**multi-step reasoning**, **tool integration**, **autonomous behavior**).
- Present **Strands Agents**: workflow, tool types, open standards, and how **Strands** reduces glue code.

### Speaker

- Banh Cam Vinh — "Building AI Agent with Strands".

### Key Highlights

- Limitations of **standalone LLMs**: chat-only behavior, no long-term state, no API/DB connections, difficulty with multi-step processes.
- Connecting **LLMs** to the real world via **tools** (APIs, databases, external services) to enable actionable agents.
- **AI Agent** definition: **LLM** as the "brain" plus **planning**, **tool-calling**, result interpretation, and iterative execution.
- **Strands Agents** provide standardized workflows, toolkits, and open-provider standards that speed up building **agentic loops**.

### Key Takeaways

- To make **LLMs** truly productive, design **agents** rather than relying on prompts alone.
- **Tool-calling** and the **agentic loop** are core: plan → select tool → call tool → read result → repeat.
- **Strands** significantly reduces engineering effort for agent-based systems.

### Applying to Work

- For internal chatbots (FAQ, IT support, CS), design **agents** that can call company APIs (tickets, HR, CRM).
- For multi-step workflows (onboarding, service registration), use **agents** to orchestrate actions automatically.
- Map internal APIs/services to tools and let **agents** orchestrate instead of hard-coding workflows.

### Event Experience

- Conceptual content but highly practical for engineers familiar with **LLM** basics and ready to deploy **agent** systems.

---

## 2. Automated Prompt Engineering: Enhancing LLM Output Quality (Nguyen Tuan Thinh)

### Event Objectives

- Explain why **prompt engineering** matters: generic prompts produce generic outputs and higher token costs.
- Systematize components of a strong prompt and introduce advanced techniques (**CoT**, **RAG**, **ToT**, etc.).
- Demo **Proptimizer** — a browser extension that optimizes prompts and an overview of its **AWS** architecture.

### Speaker

- Nguyen Tuan Thinh — DevOps Engineer, First Cloud AI Journey.

### Key Highlights

- "Generic prompts → Generic outputs": a strong prompt includes **Role**, **Instruction**, **Context**, **Input Data**, **Output Format**, **Examples**, **Constraints**.
- Concrete examples show how precise prompts produce clearer, cheaper outputs.
- Advanced techniques: **Chain-of-Thought (CoT)**, **Self-Consistency**, **Tree-of-Thoughts (ToT)**, **Retrieval-Augmented Generation (RAG)**, **Role Prompting**.
- **Proptimizer** demo and its architecture using **CloudFront**, **S3**, **Cognito**, **API Gateway**, and **Lambda**.

### Key Takeaways

- **Prompt engineering** is a core skill: treat prompts as specifications (role, task, context, format, examples, constraints).
- Optimizing prompts reduces token costs and increases result stability and accuracy.
- Techniques like **CoT/RAG/ToT** improve reasoning beyond single-shot answers.

### Applying to Work

- Use a standard prompt template for tasks (code, summary, analysis) to ensure reliable outputs.
- Standardize prompt templates and logging in production to iteratively improve performance.
- Consider **Proptimizer**-style tooling and **AWS** patterns if building prompt-optimization products.

### Event Experience

- Practical slides and clear examples — useful for both beginners and advanced users focusing on cost and quality.

---

## 3. AIoT Project: Locker Management (Aiden Dinh)

### Event Objectives

- Present a real **AIoT** project: an automated locker management system using sensors, **RFID**, and **AI**.
- Share hardware + cloud architecture (**AWS**), data flow, costs, and a working demo.

### Speaker

- Aiden Dinh — Katalon Operation Engineer, "AI-Powered Projects – AIoT Project: Locker Management".

### Key Highlights

- Problem: automate locker borrowing to reduce manual manager dependency.
- Architecture: **Arduino** (edge) + **Raspberry Pi** (controller, **MQTT**) + sensors (reed switch, **RFID**) + camera.
- Cloud: **AWS IoT Core (MQTT)**, **S3** (images), **DynamoDB** (members/transactions), **Lambda** (**Rekognition**), **Amplify** (monitoring UI).
- Flow: **RFID**/sensor events trigger photo capture → **Lambda** runs **Rekognition** → match against collection → record transaction in **DB**.

### Key Takeaways

- Combining sensing, connectivity, and **AI** solves physical asset-management problems effectively.
- **Rekognition** + **RFID** enable auditable borrow/return logs (who, when, which item).
- **AWS IoT Core** and serverless services allow scaling to multiple lockers and locations.

### Applying to Work

- Apply this design to lab equipment inventory, smart cabinets, or automated lending systems.
- Use the project as an IoT/Cloud case study for coursework or portfolio.

### Event Experience

- A showcase-style talk: problem → mission → architecture → cost → demo — great inspiration for projects.
