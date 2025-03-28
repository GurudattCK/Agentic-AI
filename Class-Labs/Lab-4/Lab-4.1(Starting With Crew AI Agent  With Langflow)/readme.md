## Project Objective

Develop an AI-driven document processing system where:  

1. Key terms are extracted from the uploaded PDF.  
2. Extracted terms are compared with reference values.  
3. A report is generated highlighting mismatched data.  

---
# CrewAI Overview

CrewAI is a Python framework for orchestrating multiple AI agents to collaborate on complex tasks.

## Key Features  
- **Multi-Agent Collaboration** – Enables AI agents to work together.  
- **Task Automation** – Automates workflows by assigning tasks to specialized agents.  
- **Customizable Roles** – Each agent has distinct responsibilities and behaviors.  
- **Memory & Context Handling** – Agents retain information and share context.  
- **Integration with LLMs** – Supports models like OpenAI’s GPT for decision-making.  

In our project, CrewAI powers agents that extract key terms, compare them with reference values, and generate a mismatch report efficiently. 🚀

---

# **Let's Start Learning with Hands-On Experience!**  

The best way to learn **anything** is by practicing it in real-time.
🚀 **Let's dive in and start experimenting**  


## Setup the Project

- Go to the [LangFlow page](https://www.langflow.org) and click on **"Get Started for Free"**, as shown in the image below.

![Langflow Screenshot](./Images/Screenshot%20(1515).png)

- Create your account on LangFlow.

![Langflow Screenshot](./Images/Screenshot%20(1516).png)

- After creating your account, click on **"New Flow"**.

![Langflow Screenshot](./Images/Screenshot%20(1517).png)

- Now click on **Blank Flow**, as we are building it from scratch.

![Langflow Screenshot](./Images/Screenshot%20(1518).png)

- Now, click on the untitled document above, and in the dropdown, click on the **Import Option** to import the [JSON File](https://drive.google.com/file/d/14qQFiHlZBBfHUV-IdSccLpjsdT9TbUjC/view?usp=drive_link) to view the flow diagram that has been provided to you.

![Langflow Screenshot](./Images/Screenshot%20(1520).png)

- Now, you will see that your project has been successfully imported, and you can view all the components.

**⚠️ Note: Sometimes while uploading your JSON file the links can be disconnected from each other, so make sure all the links are connected to each other as shown in the screenshot provided to you below.**

![Langflow Screenshot](./Images/Screenshot%20(1877).png)

- Now the first step is you have to provide the document in the file component. We are using a reference MSA document, you can upload yours as well. Click on the blue circle icon to upload your document.

Reference MSA Document link: [MSA document link](https://drive.google.com/file/d/142cTmwtzkly2SkAhgwGwAJ-xKo4B4Ogk/view?usp=drive_link)

![Langflow Screenshot](./Images/Screenshot%20(1780).png)

---

⚠️ **Important Note**  
- Provide your **OpenAI API Key** to the agent and the **OpenAI Model** component to enable authentication and access.  
- **[Follow this article](https://github.com/initmahesh/MLAI-community-labs/tree/main/Class-Labs/Lab-0(Pre-requisites))** to generate an OpenAI API key. 🔑  
- Ensure that the **API key is securely stored** and used **only for authorized requests** to prevent misuse.  

![Langflow Screenshot](./Images/Screenshot%20(1776).png)

---

- Now, click on the **Playground Section**.

![Langflow Screenshot](./Images/Screenshot%20(1878).png)

---

- In the **Playground** section, click on **"Run Flow"**.  
![Langflow Screenshot](./Images/Screenshot%20(1778).png)
- The system will fetch and display the output based on the document you have uploaded.  
- It will then extract key terms from the document, compare them with reference values, and generate a report highlighting any mismatched data.  


![Langflow Screenshot](./Images/Screenshot%20(1779).png)

- **⚠️ Note: If no document is found in the upload document, the file uploader component will fail, and the output generation will not proceed**.
---

- You can change the reference value by clicking on the second agent goal section. 
![Langflow Screenshot](./Images/Screenshot%20(1781).png) 
![Langflow Screenshot](./Images/Screenshot%20(1782).png) 

---
# Our Agents and Their Tasks  

## Agents Overview  

### 1. **Researcher Agent**  
- **Role:** PDF Data Extractor  
- **Purpose:** Extract key terms from uploaded PDF documents.  
- **Description:** This agent specializes in scanning and extracting important contract terms with precision.  
  

### 2. **Writer Agent**  
- **Role:** Data Comparison Analyst  
- **Purpose:** Compare extracted terms with reference values to find mismatches.  
- **Description:** This agent ensures that extracted terms align with expected reference data, highlighting discrepancies.  
  

### 3. **Review Agent**  
- **Role:** Compliance Report Generator  
- **Purpose:** Generate a final report detailing mismatches and compliance issues.  
- **Description:** This agent analyzes discrepancies and provides a structured compliance report with insights.  
  

---  

## Task Assignments  

### 1. **PDF Extraction Task**  
- **What it does:** Extracts key terms from the uploaded contract document.  
- **Who performs it:** Researcher Agent  
- **Expected Output:** A structured list of key terms from the document.  

### 2. **Data Comparison Task**  
- **What it does:** Compares extracted terms with reference data to identify mismatches.  
- **Who performs it:** Writer Agent  
- **Expected Output:** A report listing all mismatched data points.  

### 3. **Final Report Generation Task**  
- **What it does:** Creates a detailed compliance report based on mismatches found.  
- **Who performs it:** Review Agent  
- **Expected Output:** A structured compliance report with insights and recommendations.  

---  

## Summary  

This AI-powered system automates contract analysis using three specialized agents:  
1. **Researcher Agent** extracts key terms from PDFs.  
2. **Writer Agent** compares the extracted data with reference values.  
3. **Review Agent** generates a compliance report highlighting mismatches.  

---  



## 📚 Resources  

We have provided you with the **document** and the **JSON file** used in this lab, available in the same repository. You can use them to **explore, experiment, and practice** on your own. 🚀  

🔗 Feel free to **modify and play around** with these resources to deepen your understanding! 🎯  




---

## ⚠️ Challenges You May Face in Langflow
While running Langflow, you might encounter some bugs related to network connectivity and session creation. If you see an error or face issues while creating a new session, don’t worry. Simply refresh the page and try again.

Behind the scenes, everything continues to function properly—this is just a known Langflow bug that you can safely ignore.




