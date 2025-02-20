## Objective

By the end of this lesson, students will:

- Understand the fundamentals of prompt engineering.
- Learn how to design effective prompts to get accurate and relevant responses from AI models.
- Develop practical skills in structuring prompts for different use cases.
- Experiment with different types of prompts and analyze their outcomes.
- Apply prompt engineering techniques to optimize AI-generated outputs.

---

## What is Prompt Engineering?

Prompt engineering is the practice of designing and refining inputs (prompts) to effectively interact with AI models. The goal is to craft clear, structured, and precise prompts that guide the AI in generating relevant, accurate, and useful responses.

AI models, such as ChatGPT, Gemini etc process natural language inputs and generate text-based outputs based on their training data. The way a prompt is phrased significantly impacts the quality of the response.

---

## Experience with Langflow

To better understand **Prompt Engineering**, we will be using **Langflow**, a no-code tool that allows us to design and experiment with AI prompts interactively.

### **Why Langflow?**
- Provides a **visual interface** to create and test AI prompts.  
- Helps in **understanding how different prompts impact AI responses**.  
- Allows us to **iterate and refine prompts** for better accuracy.  
- Enables **rapid prototyping** of AI-driven applications without coding.  

By using Langflow, you will gain **practical experience** in crafting, testing, and optimizing prompts, reinforcing key concepts in prompt engineering.

#### ***🔗 Want to learn more about Langflow? [Click Here](https://docs.langflow.org)***
---

# **Deep Dive : Prompt Engineering and Best Practices**


## **Building Blocks of a Prompt:**  
Prompts are not created equal and have ways to get different responses. Here are the building blocks that make a prompt:

- **Instruction** - A specific task or instruction you want the model to perform:  
  *"Find the capital of the top 10 countries by GDP?"*
  
- **Context** - Can involve external information or additional context that can steer the model to better responses.  
  *Context (You are a student listing all countries and their capitals as comma-separated files); Instruction (Find the capital of the top 10 countries by GDP?)*
  
- **Input Data** - The input or question that we are interested in finding a response for.  
  *Context (You are a student, preparing a list of countries and capitals in any order); Input (Can you list the capital of the USA in that format?)*
  
- **Output Indicator** - Indicates the type or format of the output.  
  *Context (You are a student, preparing a list of countries and capitals in any order); Input (Can you list the capital of the USA in the given output format?); Output Format: "Paris; France", "New Delhi; India"*

Like Legos, you can pick up all or any combination of these prompts to perform the task at hand.

---

## **Methods Used in Prompts**

There are different types of prompts that you can use to interact with large models based on your task:

### **1) Instructions**  
Here, you simply tell the machine what to do, and it does that for you. For example:

**INPUT:**  
```text
Read the following sales email. Remove any personally identifiable information (PII), and replace it with the appropriate placeholder. For example, replace the name "Mahesh Yadav" with "[NAME]".

Hi John,

I'm writing to you because I noticed you recently purchased a new car. I'm a salesperson at a local dealership (Cheap Dealz), and I wanted to let you know that we have a great deal on a new car. If you're interested, please let me know.

Thanks,
Mahesh Yadav  
Phone: 410-805-2345  
Email: initmahesh@gmail.com  
```

**OUTPUT:**  
```text
Hi [NAME],

I'm writing to you because I noticed you recently purchased a new car. I'm a salesperson at a local dealership, and I wanted to let you know that we have a great deal on a new car. If you're interested, please let me know.

Thanks,
[SALESPERSON]
Phone: [PHONE]
Email: [EMAIL]
```

### **2) Role Prompting**  
Here, you assign a role and then ask questions based on that role.

**INPUT:**  
```text
You are a frontend engineer. Now estimate what it takes to build a stunning website for a startup with 10 pages, with very basic interactions and simple functionality. Just give the estimate in weeks, restrict your answer to 2 lines.
```

**OUTPUT:**  
```text
A stunning website for a startup with 10 pages, basic interactions, and simple functionality could take approximately 4-8 weeks to complete. However, the actual time required may vary depending on project-specific requirements and available resources.
```

---

## **Parameters You Can Tweak**  
We have seen how we can use the above blocks, tune our model response, or get different responses. Here are some parameters that affect the results:

- **Temperature** - Controls randomness. A lower temperature leads to more predictable responses, while a higher value increases creativity.
- **Top_p** - Controls response diversity. A lower value gives exact answers, while a higher value encourages varied responses.

📌 *Recommendation: Alter only one of these at a time.*

- **Penalty** - Discourages overuse of specific words or patterns in the response.

---

# **How AI Models Process Prompts**  

AI models like GPT work by predicting the most likely next word based on the input prompt. The way you structure the prompt **directly influences** the response quality.

- **A vague prompt** results in **ambiguous** or **generic** responses.  
- **A detailed, structured prompt** provides **precise, high-quality** responses.  

---

## **Poor vs  Good Prompting**  

### **🔴 Poor Prompt:**  
```text
Input 
Extract these Information from the document: Key Term, Description, and Location in Contract. 
```
![Langflow Screenshot](./Images/Screenshot%20(1589).png)

```text
Output
Here are some key terms extracted from the document along with their descriptions and locations in the contract:

1. **Key Term:** Kaseya Master Agreement  
   **Description:** A binding legal contract between Kaseya and the entity making purchases under this Agreement.  
   **Location in Contract:** Introduction (Effective as of April 1, 2024)

2. **Key Term:** Scope  
   **Description:** Governs the interactions between the customer and Kaseya, including access to Kaseya portals and platforms, and the right to purchase Kaseya Products.  
   **Location in Contract:** Section 1(a)

3. **Key Term:** Product Terms of Use  
   **Description:** Terms applicable to the use, marketing, resale, and distribution of Kaseya Products.  
   **Location in Contract:** Section 1(a)

4. **Key Term:** License  
   **Description:** The right to use a Product pursuant to the terms of the Agreement and as defined in the applicable Documentation.  
   **Location in Contract:** Section 2(c)

5. **Key Term:** End User  
   **Description:** The person or entity that purchases a Product for its own use and owns, licenses, or uses Content.  
   **Location in Contract:** Section 16

6. **Key Term:** Confidential Information  
   **Description:** Any business, operational, and/or technical information that is designated as confidential or that a reasonable person would believe to be confidential.  
   **Location in Contract:** Section 7(a)

7. **Key Term:** Termination for Convenience  
   **Description:** Either party may terminate the Agreement at any time without cause upon 30 calendar days written notice.  
   **Location in Contract:** Section 9(b)

8. **Key Term:** Indemnification  
   **Description:** Obligations of Kaseya and the customer to defend and hold harmless against certain claims.  
   **Location in Contract:** Section 11

9. **Key Term:** Governing Law  
   **Description:** The laws of the State of Delaware, USA, govern all disputes arising out of the Agreement.  
   **Location in Contract:** Section 14(a)

10. **Key Term:** Fair Use  
    **Description:** Policies that prohibit excessive use of Products that harms Kaseya's resources or circumvents the intended use of the Product.  
    **Location in Contract:** Section 2(f)

These terms provide a foundational understanding of the Kaseya Master Agreement and its key components.
```

**⚠️ Issue With This Prompt**
Lack of Output Format Specification.The prompt does not specify how the extracted information should be formatted (e.g., table, JSON, bullet points).This can lead to inconsistent or unstructured responses.

---

### **🟢 Improved Prompt:**
```text
Input
 Create a table with the following columns: Key Term, Description, and Location in Contract. Populate it with the extracted details of the service provider name, customer name, and termination clauses.
```
![Langflow Screenshot](./Images/Screenshot%20(1590).png)

```text
Output
Here's a table with the requested details extracted from the Kaseya Master Agreement:

| Key Term                     | Description                                                                                     | Location in Contract                       |
|------------------------------|-------------------------------------------------------------------------------------------------|-------------------------------------------|
| Service Provider Name         | Kaseya US, LLC (for customers in the United States)                                           | Exhibit A                                 |
| Customer Name                 | The entity making purchases under this Agreement (referred to as "you")                       | Introduction (first paragraph)            |
| Termination for Convenience    | Either party may terminate the Agreement at any time, without cause, upon 30 days written notice. | Section 9(b)                             |
| Termination for Material Breach | Each party may terminate the Agreement upon notice if the other party materially breaches and fails to cure within 30 days. | Section 9(c)                             |
| Effect of Termination         | Upon termination, the customer may not order or sell additional Products without consent, and all rights and licenses will terminate. | Section 9(d)                             |

This table summarizes the key terms related to the service provider name, customer name, and termination clauses as specified in the Kaseya Master Agreement.
```

✅ Why This Works:
- The response is in a table format, which enhances readability and organization.
- Each key term is properly categorized under three columns:
   - Key Term (What is being defined)
   - Description (Brief explanation)
   - Location in Contract (Where it is found in the document)

---

# **Let's Start Learning Prompt Engineering with Hands-On Experience!**  

The best way to learn **Prompt Engineering** is by practicing it in real-time.
🚀 **Let's dive in and start experimenting with prompts!**  


## Setup the Project

- Go to the [LangFlow page](https://www.langflow.org) and click on **"Get Started for Free"**, as shown in the image below.

![Langflow Screenshot](./Images/Screenshot%20(1515).png)

- Create your account on LangFlow.

![Langflow Screenshot](./Images/Screenshot%20(1516).png)

- After creating your account, click on **"New Flow"**.

![Langflow Screenshot](./Images/Screenshot%20(1517).png)

- Now click on **Blank Flow**, as we are building it from scratch.

![Langflow Screenshot](./Images/Screenshot%20(1518).png)

- Now, click on the untitled document above, and in the dropdown, click on the **Import Option** to import the JSON file that has been provided to you.

![Langflow Screenshot](./Images/Screenshot%20(1520).png)

- Now, you will see that your project has been successfully imported, and you can view all the componets.

#### **LangFlow Components and Inputs**
   - **Chat Input (`ChatInput`)**
**Role:** Captures user input for processing.  
**Inputs:**
      - `input_value` – User's text message.
      - `session_id` – Tracks chat sessions.
      - `should_store_message` – Saves conversation history.

---
- **OpenAI Model (`OpenAIModel`)**
**Role:** Processes input using an OpenAI language model.  
**Inputs:**
   - `model_name` – Defines the AI model (e.g., GPT-4).
   - `max_tokens` – Sets the word limit.
   - `temperature` – Controls randomness.
   - `api_key` – OpenAI authentication.

---

- **Prompt (`PromptComponent`)**
**Role:** Structures user input into a formatted query.  
**Inputs:**
   - `template` – Defines how the prompt is structured.
   - `tool_placeholder` – Placeholder for tool-specific input.

---

- **Parse Data (`ParseData`)**
**Role:** Converts structured data into plain text.  
**Inputs:**
   - `data` – Raw data input.
   - `template` – Defines text formatting.
   - `sep` – Sets text separators.

---

- **Chat Output (`ChatOutput`)**
**Role:** Displays AI-generated responses to the user.  
**Inputs:**
   - `input_value` – AI response message.
   - `sender` – Identifies if the response is from "AI" or "User".
   - `sender_name` – Name of the sender.
   - `session_id` – Maintains conversation context.
   - `should_store_message` – Saves response history.


![Langflow Screenshot](./Images/Screenshot%20(1571).png)

⚠️ **Important Note**  
- Provide your **OpenAI API Key** to the agent and the **OpenAI Model** component to enable authentication and access.  
- Ensure that the **API key is securely stored** and used **only for authorized requests** to prevent misuse.  

---
- To tweak parameters in Langflow, go to your **OpenAI Component**, click on **Controls**, and adjust the parameters as needed to refine the AI's response. This allows for better customization and optimization of the model's behavior.

![Langflow Screenshot](./Images/Screenshot%20(1593).png)

---

- Now, click on the **Playground Section**.

![Langflow Screenshot](./Images/Screenshot%20(1588).png)

---
- In the **Playground section**, enter a query such as: 'Please provide the input particular user.' The system will fetch and display the output based on the document that you have uploaded.

![Langflow Screenshot](./Images/Screenshot%20(1556).png)

  **Example:**
   ```text
  Input: "Create a table with the following columns: Key Term, Description, and Location in Contract. Populate it with the extracted details of the service provider name, customer name, and termination clauses."
  ```
  ```text 
  Output:
  Fetched the answer from the document uploaded by you.
  ```
  
![Langflow Screenshot](./Images/Screenshot%20(1573).png)

- **⚠️ Note: If no document is found in the upload document, the file uploader component will fail, and the output generation will not proceed**.



## **Top 10 Best Practices Walkthrough**  
Using our *Contract Summarization App*, we will apply ten best practices for prompt engineering:

1. **Be Specific with Information Requests**  
   📌 *Example:* Extract the service provider name, start and end date of the contract, and the total deal value.

2. **Supply Examples for Context**  
   📌 *Example:* Given the format "Service Provider Name: [Name], Start Date: [Date], End Date: [Date], Deal Value: [Amount]", summarize accordingly.

3. **Include Relevant Data**  
   📌 *Example:* Referencing Section 1.5, summarize the deal value and billing frequency terms.

4. **Specify Desired Output Format**  
   📌 *Example:* Create a table with "Key Term", "Description", and "Location in Contract" columns.

5. **Use Positive Instructions**  
   📌 *Example:* Extract key terms including 'termination for breach' and 'limitations of liability' in JSON format.

6. **Assign a Persona or Frame of Reference**  
   📌 *Example:* Imagine you are a legal analyst. Summarize auto-renewal terms, notice periods, and liabilities.

7. **Implement Chain of Thought Prompting**  
   📌 *Example:* Identify 'termination without cause' clauses → Summarize → Explain implications.

8. **Break Down Complex Tasks**  
   📌 *Example:* Identify and summarize indemnification terms. Then extract coverage for attorney fees.

9. **Acknowledge the Model's Limitations**  
   📌 *Example:* Extract governing law and indemnification terms. Flag unclear sections for expert review.

10. **Take an Experimental Approach**  
    📌 *Example:* Extract 'termination for cause' using a bullet list, then as a paragraph. Compare clarity.

---

## **Example Prompt for Contract GPT**  

```xml
<Role>
You are an in-house general counsel trained to find liabilities and other clauses from contracts.
</Role>

<Instruction>
Use your legal expertise to review the provided contract document. Your primary goal is to extract and summarize specific terms accurately, following the structured format specified.
</Instruction>

<Task>
1. Extract key terms including 'Service Provider Name', 'Start Date', 'End Date', and 'Deal Value'. Present these in a list format.
2. Review and identify clauses related to 'termination for breach', 'data breach notice', and 'limitations of liability'. Provide a summary in JSON format.
3. Analyze 'auto-renewal' terms and specify the required notice period.
4. Summarize 'indemnification' and 'attorney fees' coverage terms separately.
5. Highlight any ambiguous or unclear language, suggesting further review if necessary.
</Task>

<Guardrails>
1. Be specific and concise in term extraction.
2. Provide summaries in the specified format (JSON, table, or bullet points as directed).
3. Emulate a legal analyst persona.
4. Use positive instructions: focus on terms to include, rather than avoid.
5. Acknowledge model limitations: flag uncertain sections for professional review.
</Guardrails>
```

---

## **Conclusion**
Prompt engineering is a crucial skill in working with AI models effectively. By understanding the different prompt structures, applying best practices, and fine-tuning parameters, users can achieve highly specific and accurate responses. As AI continues to evolve, mastering these techniques will be essential for optimizing AI interactions and improving task outcomes.

---

© **All rights reserved Mahesh Yadav Institute**. No part of this course can be reproduced, distributed, or transmitted in any form without permission.


