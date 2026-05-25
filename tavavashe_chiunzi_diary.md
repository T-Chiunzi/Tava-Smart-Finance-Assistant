# 📓 Developer's Diary – AI Collaboration Guide

This file shows sample entries for your **Developer's Diary**. You must document your AI collaboration throughout the project development. Each entry should have:
- **Artifact**: a screenshot, GIF, or snippet of your AI interaction
- **Context**: one-sentence description of your goal
- **Reflection**: analysis of what happened, what you learned, and how you improved the solution

**Key Principle**: You're directing AI like a junior developer - always review, critique, and improve their suggestions.

---

## Foundation Skills Examples

### Entry 1 – Starting Out
**Artifact:**

<img width="1831" height="639" alt="Screenshot (63)" src="https://github.com/user-attachments/assets/4eec5a3c-5b82-4c95-a791-6e995d4c59d3" />
<img width="1831" height="667" alt="Screenshot (64)" src="https://github.com/user-attachments/assets/e25061ce-d1b4-411a-b1dd-e501425fbe74" />
<img width="1828" height="709" alt="Screenshot (65)" src="https://github.com/user-attachments/assets/d23886a4-75f1-48c7-a780-48a0bbc03b82" />
<img width="1831" height="904" alt="Screenshot (66)" src="https://github.com/user-attachments/assets/b030767d-d057-4b21-b650-c17ce3ac4689" />
<img width="1830" height="913" alt="Screenshot (67)" src="https://github.com/user-attachments/assets/92cac211-5dca-4231-b526-2c2ed87914fb" />
<img width="1829" height="906" alt="Screenshot (68)" src="https://github.com/user-attachments/assets/bced0041-b46b-4cc3-ba1b-155f7e8644b2" />
<img width="1828" height="903" alt="Screenshot (70)" src="https://github.com/user-attachments/assets/a0c1dcb5-0449-45dc-affd-153d654fcdf9" />


**My Initial Prompt:** "Hello, Gemini. May you please help me with this AI-assisted task? My course requires me to design and generate a smart finance assistant using Python. These are the project specifications: 
Your Assistant should help users complete personal finance tasks such as: 
•	Summarising transactions from a CSV file.
•	Tracking a stock/crypto portfolio via API data.
•	Analysing budgets and spending patterns.
•	Offering advice through a chatbot personality.
•	Running a simple custom tool (e.g., currency converter, savings goal calculator). 
May you please give a basic skeleton template that breaks down the overall task into simpler tasks? Remember that it should not be overly complex.
"

**My Improved Prompt:** Currently there is no second prompt, as this was only a test script.

**Context:** Using Gemini to generate a basic skeleton as a foundation for a smart financial tracker that integrates my knowledge from the past 9 weeks of Introduction to Business Programming. 
**Reflection:** My first prompt makes it clear that I want a base foundation with which to base my tracker around. So far the template is satisfactory, however, I feel that it can be improved upon.  

---

### Entry 2 – Understanding the code
**Artifact:** Before/after screenshots of AI-generated spending analysis code.

**Context:** AI gave me complex code that was hard to understand for my transaction analysis.

**AI's First Response:**
```python
df.groupby('Category')['Amount'].agg({'sum','mean','count'}).round(2)
```

**My Critique:** "This code is unclear and doesn't handle dollar signs. Can you make it more readable with business-friendly variable names and add data cleaning?"

**AI's Improved Response:**
```python
# Clean amount data by removing dollar signs
df['Amount_Clean'] = pd.to_numeric(df['Amount'].str.replace('$', ''), errors='coerce')

# Calculate spending metrics by category
spending_summary = df.groupby('Category')['Amount_Clean'].agg({
    'Total_Spent': 'sum',
    'Average_Amount': 'mean', 
    'Transaction_Count': 'count'
}).round(2)
```

**Reflection:** I learned that AI's first response isn't always the best. By asking for clearer variable names and business context, I got much better code. This taught me to always review AI code and ask for improvements rather than accepting the first solution.

---

### Entry 3 – Improving the code


<img width="1919" height="907" alt="Screenshot 2026-05-25 151142" src="https://github.com/user-attachments/assets/75493f92-f2b5-45c9-9b6a-855af7493dde" />
<img width="1919" height="908" alt="Screenshot 2026-05-25 151203" src="https://github.com/user-attachments/assets/8833cb45-0384-41fa-a244-d27dd1f98f84" />
<img width="1917" height="909" alt="Screenshot 2026-05-25 151220" src="https://github.com/user-attachments/assets/b1d4f1b2-8d32-4b0f-a77b-fa5b75fa1608" />
<img width="1919" height="916" alt="Screenshot 2026-05-25 151242" src="https://github.com/user-attachments/assets/39bf4139-54e7-4122-bd3e-d2529e93cca7" />
<img width="1919" height="908" alt="Screenshot 2026-05-25 151257" src="https://github.com/user-attachments/assets/491e4050-7139-4508-92a3-186147946996" />
<img width="1916" height="910" alt="Screenshot 2026-05-25 151313" src="https://github.com/user-attachments/assets/d1ce8aff-34e8-42a4-b2d0-9f31640f54a2" />
<img width="1916" height="903" alt="Screenshot 2026-05-25 151331" src="https://github.com/user-attachments/assets/c88e3e37-69dc-466f-8a6d-71a1753bdbf6" />
<img width="1919" height="900" alt="Screenshot 2026-05-25 151347" src="https://github.com/user-attachments/assets/60bf6fa9-0b04-4c85-8734-1e905ab3edd4" />
<img width="1919" height="903" alt="Screenshot 2026-05-25 151405" src="https://github.com/user-attachments/assets/b767398e-cf6a-431b-8516-eae0b25b1142" />
<img width="1916" height="913" alt="Screenshot 2026-05-25 151444" src="https://github.com/user-attachments/assets/68e42f1c-ea3c-41fd-b816-7f15ea596591" />


**Context:** I wanted AI to help improve the code I had already written. 
This was my code:

<img width="1915" height="796" alt="Screenshot 2026-05-25 153249" src="https://github.com/user-attachments/assets/052dc207-a97a-4dbc-9902-a698f8b17fba" />
<img width="1919" height="909" alt="Screenshot 2026-05-25 153307" src="https://github.com/user-attachments/assets/6cca941d-e37f-402d-bc1d-e54cde49e7c2" />


This is what my code was outputting:

<img width="1919" height="903" alt="Screenshot 2026-05-25 153330" src="https://github.com/user-attachments/assets/de608ac3-6fe9-452b-a152-18c9e3253192" />


**My Prompt:** "Hi Gemini. I wanted to first test my understanding and write my own code before asking for assistance. I've finished some of the coding. Can we build from what I have?"

**AI Response:** That is an incredible approach! Writing your own code first is exactly how you transition from an amateur to a confident programmer, and your lecturers will love to see that initiative reflected in your repository.

I would be absolutely delighted to build directly from your code.

Please paste what you have written so far. It doesn't matter if it's just a single function, an unfinished loop, a rough draft of your math logic, or some basic Gradio components.

Once you share it, we can:

1. Review how it works and ensure it aligns with your "Savings Buddy" requirements.
2. Polish or expand it to include the category breakdowns, timeline calculations, or savings boosts you want.
3. Help you structure it perfectly into the **Six-Step Methodology** for your Colab notebook.

Whenever you're ready, drop your code below!."

This was the output after Gemini's corrections:

<img width="1918" height="910" alt="Screenshot 2026-05-25 154026" src="https://github.com/user-attachments/assets/9c799815-4510-4dfe-a75e-b2921a37e52c" />


**Reflection:** 

---

### Entry 4 – Data Quality and Edge Cases
**Artifact:** Screenshot of debugging session with Claude about handling messy CSV data.

**Context:** My CSV had negative amounts (refunds) and missing values that broke my calculations.

**My Problem:** "My spending analysis is giving wrong totals because some amounts are negative (refunds) and some cells are empty."

**AI Solution:** Helped me add data validation:
```python
# Handle refunds and missing data appropriately
df_clean = df.dropna(subset=['Amount_Clean'])
positive_spending = df_clean[df_clean['Amount_Clean'] > 0]
refunds = df_clean[df_clean['Amount_Clean'] < 0]
```

**Reflection:** AI helped me think about real-world data issues I hadn't considered. I learned that business data is always messy and I need to ask AI specifically about edge cases like refunds, missing values, and invalid entries. This makes my finance assistant more robust for actual use.

---

## Advanced Integration Examples

### Entry 5 – Combining Multiple AI Tools
**Artifact:** Screenshot showing integration of hands-on-ai chat with pandas analysis.

**Context:** I wanted to create a chatbot that could answer questions about spending data.

**My Approach:** Used AI to help me combine CSV analysis with hands-on-ai chat functionality.

**Key Learning:** AI helped me structure the integration, but I had to understand the business logic to make it useful. The chatbot needed to understand financial concepts, not just execute code.

**Reflection:** Integrating multiple technologies requires understanding how each piece serves the business purpose. AI can generate technical integration code, but I need to guide it toward business value.

---

### Entry 6 – Professional Error Handling
**Artifact:** Code snippet showing error handling for file uploads.

**Context:** I needed my Gradio interface to handle bad CSV files gracefully.

**AI Suggestion:** Generated try/catch blocks with business-appropriate error messages:
```python
try:
    df = pd.read_csv(file.name)
    # Analysis code...
except FileNotFoundError:
    return "Please upload a valid CSV file."
except pd.errors.EmptyDataError:
    return "The uploaded file appears to be empty. Please check your data."
```

**Reflection:** AI helped me think about user experience, not just technical functionality. Good error messages help users understand what went wrong and how to fix it. This is crucial for business applications.

---

## AI Collaboration Best Practices I've Learned

### 🎯 Effective Prompting Strategies
1. **Always provide business context**: "I'm building a finance assistant for..."
2. **Specify data structure**: "My CSV has columns X, Y, Z with these data types..."  
3. **Request professional formatting**: "Format output for business presentation"
4. **Ask for comments**: "Include clear comments explaining the business logic"

### 🤔 Critique Questions I Always Ask
- "Does this handle edge cases like negative amounts or missing data?"
- "Are the variable names clear for a business context?"
- "How would I explain this code to a non-technical manager?"
- "What assumptions is this code making about my data?"

### 🔄 Iterative Improvement Process
1. **Get basic working code** from AI
2. **Test with real data** and find issues  
3. **Ask AI to fix specific problems** with context
4. **Simplify complex solutions** for maintainability
5. **Add business-appropriate formatting** and error handling

### 📊 Business Value Focus
- Always connect code back to business decisions
- Format outputs for non-technical users
- Include actionable insights, not just data summaries
- Consider the end user's needs and context

---

## 📝 Documentation Template for Your Entries

Use this format for consistent diary entries:

```markdown
### Entry [Number] – [Descriptive Title]
**Artifact:** [Screenshot/code snippet/GIF of AI interaction]

**Context:** [One sentence: what you were trying to achieve]

**My Prompt:** "[Your exact prompt to AI]"

**AI Response Summary:** [Brief description of what AI provided]

**My Critique/Improvement:** [How you modified or improved the AI's suggestion]

**Result:** [What you ended up with and why it's better]

**Reflection:** [What you learned about AI collaboration, business programming, or problem-solving]
```

---

✅ **Remember**: Document your AI collaboration throughout your project development. Each entry should show learning and improvement, not just successful interactions. Show how you direct AI like a junior developer to create business-appropriate solutions.

