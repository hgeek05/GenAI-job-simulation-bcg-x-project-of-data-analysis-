# Task 2: Developing an AI-powered Financial Chatbot

## Financial Chatbot Prototype

This project is a simplified prototype of an AI-powered financial chatbot designed to answer predefined queries using manually extracted and analyzed financial data from Microsoft, Tesla, and Apple. While basic in its current form, this chatbot lays the groundwork for future development using advanced AI and machine learning techniques.

---

## Project Overview

The chatbot responds to frequently asked financial questions using rule-based logic. It is built with Python and structured to demonstrate how conversational interfaces can enhance access to complex financial insights.

This project was completed as part of a larger initiative to explore how AI can improve financial decision-making and data interaction for GFC (Global Finance Corporation).

---

## Task Objectives and Deliverables

- Extract key financial data from 10-K filings for Microsoft, Tesla, and Apple (completed in Task 1).
- Build a prototype chatbot responding to a small set of predefined financial queries.
- Implement rule-based logic.
- Document the chatbot’s functionality, limitations, and future enhancements.

---

## My Chatbot Prototype

I developed a command-line chatbot using Python that answers five predefined financial queries based on the analyzed data, using simple conditional statements.

### Supported Queries

- What is the total revenue?
- How has net income changed over the last year?
- What is the total assets value?
- What are the total liabilities?
- What is the cash flow from operating activities?

### Sample Code Snippet

```python
def simple_chatbot(user_query):
    if user_query == "What is the total revenue?":
        return "The total revenue for the last reported year was $394.3 billion (Apple, 2023)."
    elif user_query == "How has net income changed over the last year?":
        return "Apple's net income decreased by 2.8% from 2022 to 2023."
    elif user_query == "What is the total assets value?":
        return "Apple's total assets for 2023 were $352.583 billion."
    elif user_query == "What are the total liabilities?":
        return "Apple's total liabilities for 2023 were $290.437 billion."
    elif user_query == "What is the cash flow from operating activities?":
        return "Apple's cash flow from operating activities in 2023 was $110.543 billion."
    else:
        return "Sorry, I can only provide information on predefined queries."
```

---

## Example Answer Provided by the Project

Great work! Below is the example answer given by the project to illustrate how a professional might approach the task. It serves as a foundation and inspiration for further innovation.

---

### Chatbot Example: Basic Financial Inquiry Bot

**Objective:** Develop a chatbot that responds to predefined queries about a company's financial performance, focusing on net income and revenue growth.

---

### 1. Rule-based Logic Implementation

```python
def financial_chatbot(query):
    responses = {
        "net income": "The net income for the fiscal year 2021 was $5 billion, a 10% increase from 2020.",
        "revenue growth": "The revenue grew by 8% from 2020 to 2021, reaching $22 billion."
    }
    return responses.get(query.lower(), "I'm not sure how to answer that. Can you try a different question?")
```

**Explanation:**
This simple Python function uses a dictionary to map user queries to predefined responses. It demonstrates the principle of rule-based logic and error handling by providing a default response when the query does not match.

---

### 2. Data Structuring and Retrieval

* **Data Structuring:** Assume there is a CSV file named `financial_data.csv` storing the company’s financial data.
* **Retrieval Method:** Although the example uses hardcoded responses, in practice, you could load the CSV with pandas and query it dynamically based on user input.

---

### 3. Communicating Financial Insights

* The chatbot’s responses summarize complex financial data clearly and concisely.
* To improve user engagement, you might expand this by suggesting related queries or follow-ups.

---

### Example Interaction with the Chatbot

| User Query                      | Chatbot Response                                                                     |
| ------------------------------- | ------------------------------------------------------------------------------------ |
| "What was the net income?"      | "The net income for the fiscal year 2021 was \$5 billion, a 10% increase from 2020." |
| "Tell me about revenue growth." | "Revenue grew by 8% from 2020 to 2021, reaching \$22 billion."                       |

---

### Conclusion and Variations

This example demonstrates the core principles of developing a financial chatbot using rule-based logic. Depending on your skills and needs, you can:

* Integrate more advanced NLP for flexible query handling.
* Connect to real-time financial databases for dynamic responses.
* Implement machine learning for more nuanced interactions.

**Key Takeaway:**
Rule-based logic, data integration, and clear communication are fundamental, regardless of chatbot complexity. This example provides a solid foundation, encouraging you to innovate beyond it.

---

## Project Structure

```
financial_chatbot_prototype/
│
├── chatbot.py              # Python script implementing the rule-based chatbot
├── documentation.md        # Documentation on chatbot design and functionality
├── README_Task2.md         # This file: explanation and example answer
```

---

## How to Use

1. Clone or download this repository.

2. Open a terminal and navigate to the project directory.

3. Run the chatbot:

   ```bash
   python chatbot.py
   ```

4. Enter one of the predefined queries.

5. Type `exit` or `quit` to end the session.

---

## Limitations & Future Improvements

* Supports only exact, predefined queries.
* No natural language understanding or fuzzy matching.
* Uses static financial data, requiring manual updates.
* Command-line interface only — a web UI could improve accessibility.

Future enhancements may include NLP integration, real-time data connectivity, and machine learning for smarter interactions.

---

Thank you for reviewing this chatbot prototype. Feedback and collaboration are welcome!
