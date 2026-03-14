# Ex.No.6 Development of Python Code Compatible with Multiple AI Tools

# 🤖 Framing Prompts for AI-Assisted Project Coding
## Comparative Analysis: Perplexity AI vs. ChatGPT

> **Course Exercise** | AI Tools in Software Development  
> **Task:** Sum of All Odd Numbers in a Given Range  
> **Tools Evaluated:** Perplexity AI · ChatGPT (GPT-4)

---

## 📋 Table of Contents

- [Aim](#aim)
- [Procedure](#procedure)
- [Stage 1 — Prompt Design](#stage-1--prompt-design)
- [Stage 2 — AI-Generated Responses](#stage-2--ai-generated-responses)
- [Stage 3 — Output Comparison](#stage-3--output-comparison)
- [Comparison Table](#comparison-table)
- [Insights & Next Steps](#insights--next-steps)
- [Reflection Note](#reflection-note)

---

## Aim

The aim of this exercise is to learn how to design effective prompts for AI tools to assist in coding tasks related to project development. By submitting the same Python programming task to two different AI tools — **Perplexity AI** and **ChatGPT** — this report evaluates how each tool responds, compares the quality and approach of their generated code, and reflects on how prompt design influences output quality.

Specifically, this exercise aims to:
- Understand how different AI tools interpret the same prompt
- Analyse differences in code structure, explanation style, and output quality
- Develop skills in prompt refinement for more accurate and useful AI responses
- Generate actionable insights on choosing the right AI tool for coding assistance

---

## Procedure

The exercise was carried out in the following stages:

### Stage 1 — Designing the Prompt
A common Python programming task was selected and a prompt was carefully worded to be clear and unambiguous. The same prompt was submitted to both AI tools without any modification to ensure a fair comparison.

### Stage 2 — Submitting the Prompt
The designed prompt was submitted to:
- **Perplexity AI** (via [perplexity.ai](https://www.perplexity.ai))
- **ChatGPT** (GPT-4, via [chat.openai.com](https://chat.openai.com))

# chatgpt 

      start = int(input("Enter start of range: "))
      end = int(input("Enter end of range: "))
    
      sum = 0
    
      for i in range(start, end + 1):
          if i % 2 != 0:
              sum += i
    
      print("Sum of odd numbers:", sum)


# perplixity
def sum_odd_numbers(start, end):
    """
    Returns the sum of all odd numbers from start to end inclusive.
    
    Args:
    start (int): Starting number of the range.
    end (int): Ending number of the range.
    
    Examples:
    >>> sum_odd_numbers(1, 10)
    25  # 1+3+5+7+9
    >>> sum_odd_numbers(4, 15)
    45  # 5+7+9+11+13+15
    """
    # Adjust start to first odd >= start
    if start % 2 == 0:
        first_odd = start + 1
    else:
        first_odd = start
    
    # Last odd <= end
    last_odd = end if end % 2 == 1 else end - 1
    
    if first_odd > last_odd:
        return 0
    
    # Number of odds: (last - first)/2 + 1
    n = ((last_odd - first_odd) // 2) + 1
    
    # Sum = n * (first + last) / 2
    return n * (first_odd + last_odd) // 2

# Test it
print(sum_odd_numbers(1, 10))  # Output: 25
print(sum_odd_numbers(4, 15))  # Output: 45


### Stage 3 — Recording the Outputs
The complete responses from both tools were recorded, including the generated code, inline explanations, and any additional commentary provided by each tool.

### Stage 4 — Comparing the Outputs
The two outputs were compared across multiple dimensions: code correctness, approach/logic, explanation quality, code style, and extra features offered.

### Stage 5 — Reflection
A short reflection was written on the effectiveness of the prompt and suggestions for how it could be refined further.

---

## Stage 1 — Prompt Design

### 🔵 Basic Prompt (Unrefined)
```
Write python code to add odd numbers in a range.
```
> **Limitation:** Vague — does not specify whether the range is user-inputted or hardcoded, what the expected output format is, or whether edge cases should be handled.

---

### 🟡 Zero-Shot Prompt (Refined, No Examples)
```
Write a Python program to find the sum of all odd numbers in a given range.
The program should:
- Accept the start and end of the range from the user
- Identify all odd numbers within that range (inclusive)
- Calculate and display their sum
```
> **Improvement:** Clearly states the task, input method, and expected output — no examples needed.

---

### 🟠 Final Prompt Used (Submitted to Both Tools)
```
Write a Python program to find the sum of all odd numbers in a given range.
The range should be provided by the user as input (start and end values).
Include comments in the code to explain each step.
Also briefly explain how the program works after the code.
```
> **Why this prompt?** It is specific, requests user interaction, asks for inline comments (which tests explanation quality), and requests a post-code explanation — making it easy to compare how each AI communicates.

---

## Stage 2 — AI-Generated Responses

### 🔷 Perplexity AI Response

**Code Generated:**
```python
# ---- PASTE YOUR PERPLEXITY AI CODE HERE ----
# (Copy and paste the exact code Perplexity AI gave you)
```

**Explanation Provided by Perplexity AI:**
> *(Paste or summarise Perplexity AI's explanation of the code here)*

**Notable Characteristics:**
- *(e.g., "Used a for loop with an if condition")*
- *(e.g., "Provided source citations alongside the answer")*
- *(e.g., "Did not handle invalid input")*

---

### 🔶 ChatGPT Response

**Code Generated:**
```python
# ---- PASTE YOUR CHATGPT CODE HERE ----
# (Copy and paste the exact code ChatGPT gave you)
```

**Explanation Provided by ChatGPT:**
> *(Paste or summarise ChatGPT's explanation of the code here)*

**Notable Characteristics:**
- *(e.g., "Used Python's built-in sum() and range() functions")*
- *(e.g., "Offered an alternative approach using list comprehension")*
- *(e.g., "Included input validation with a try-except block")*

---

## Stage 3 — Output Comparison

### Approach to Solving the Problem

| Aspect | Perplexity AI | ChatGPT |
|---|---|---|
| **Core Logic Used** | *(e.g., for loop + if condition)* | *(e.g., sum() + range() with step 2)* |
| **Input Handling** | *(e.g., basic input())* | *(e.g., input() with try-except)* |
| **Alternative Approach Offered** | *(Yes / No)* | *(Yes / No)* |
| **Edge Cases Covered** | *(e.g., None mentioned)* | *(e.g., Invalid input handled)* |

### Code Style Comparison

| Style Element | Perplexity AI | ChatGPT |
|---|---|---|
| **Inline Comments** | *(Present / Absent / Partial)* | *(Present / Absent / Partial)* |
| **Variable Naming** | *(e.g., descriptive / short)* | *(e.g., descriptive / short)* |
| **Code Length (approx. lines)** | *(e.g., ~12 lines)* | *(e.g., ~9 lines)* |
| **Use of Built-in Functions** | *(e.g., Minimal)* | *(e.g., Extensive — sum(), range())* |
| **Pythonic Style** | *(e.g., Moderate)* | *(e.g., High — uses list comprehension)* |

### Explanation Quality Comparison

| Explanation Factor | Perplexity AI | ChatGPT |
|---|---|---|
| **Clarity of Explanation** | *(e.g., Clear but brief)* | *(e.g., Detailed with step breakdown)* |
| **Cited Sources / References** | *(e.g., Yes — links provided)* | *(e.g., No external citations)* |
| **Suggested Follow-ups** | *(e.g., None)* | *(e.g., Offered optimised version)* |
| **Beginner-Friendliness** | *(e.g., Moderate)* | *(e.g., High — explained logic intuitively)* |

---

## Comparison Table

> **Master Evaluation — Perplexity AI vs. ChatGPT**  
> Scores are rated on a scale of **1 (Poor) to 5 (Excellent)**

| Evaluation Criteria | Perplexity AI | ChatGPT | Winner |
|---|:---:|:---:|:---:|
| **Code Correctness** | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | 🤝 Tie |
| **Code Efficiency** | *(score /5)* | *(score /5)* | *(tool)* |
| **Inline Comments Quality** | *(score /5)* | *(score /5)* | *(tool)* |
| **Code Readability** | *(score /5)* | *(score /5)* | *(tool)* |
| **Explanation Depth** | *(score /5)* | *(score /5)* | *(tool)* |
| **Beginner Friendliness** | *(score /5)* | *(score /5)* | *(tool)* |
| **Edge Case Handling** | *(score /5)* | *(score /5)* | *(tool)* |
| **Response Speed** | *(score /5)* | *(score /5)* | *(tool)* |
| **Extra Features Offered** | *(score /5)* | *(score /5)* | *(tool)* |
| **Source Citations** | *(score /5)* | *(score /5)* | *(tool)* |
| **TOTAL SCORE** | **/50** | **/50** | *(overall winner)* |

> 💡 **How to fill this table:** Go through each criterion and honestly rate each tool based on what you observed in their outputs. Use the sub-tables in Stage 3 to inform your scores.

---

### 📊 Quick Feature Snapshot

| Feature | Perplexity AI | ChatGPT |
|---|:---:|:---:|
| Provided Working Code | ✅ | ✅ |
| Code had Inline Comments | *(✅ / ❌)* | *(✅ / ❌)* |
| Post-Code Explanation Included | *(✅ / ❌)* | *(✅ / ❌)* |
| Alternative Approach Offered | *(✅ / ❌)* | *(✅ / ❌)* |
| Input Validation / Error Handling | *(✅ / ❌)* | *(✅ / ❌)* |
| External Source Citations | *(✅ / ❌)* | *(✅ / ❌)* |
| Suggested Next Steps | *(✅ / ❌)* | *(✅ / ❌)* |
| Beginner-Friendly Tone | *(✅ / ❌)* | *(✅ / ❌)* |

---

## Insights & Next Steps

Based on comparing the two AI-generated outputs, the following insights were identified:

### 🔍 Key Observations

1. **Both tools solved the core problem correctly** — The fundamental logic for finding the sum of odd numbers in a range was accurate in both outputs, confirming that well-framed prompts lead to correct results regardless of the tool.

2. **Approach differed significantly** — *(Fill in: e.g., "Perplexity AI used a traditional loop-based approach, while ChatGPT used Python's built-in `sum()` and `range()` with a step of 2, resulting in a more concise solution.")*

3. **Perplexity AI's citation advantage** — Perplexity AI provided source links alongside its response, which is useful for verifying the logic or exploring documentation. ChatGPT did not cite external sources but delivered a more conversational explanation.

4. **ChatGPT offered more depth** — *(Fill in based on your observation: e.g., "ChatGPT proactively provided an alternative list comprehension approach and explained edge cases, showing more initiative in anticipating follow-up needs.")*

5. **Prompt specificity mattered** — The addition of "Include comments in the code" and "briefly explain how the program works" in the final prompt directly improved the quality of both outputs compared to what a basic prompt would have produced.

### 🚀 Suggested Next Steps

- **Refine the prompt further** to request a specific number of alternative approaches (e.g., *"Provide two different solutions — one using a loop and one using a built-in function"*)
- **Add an input validation requirement** explicitly in the prompt to check whether both tools handle invalid inputs gracefully
- **Test with a harder problem** (e.g., API integration, file handling) to reveal deeper differences in how each tool handles complexity
- **Compare token efficiency** — submit longer tasks and observe which tool gives more concise responses without losing quality

---

## Reflection Note

### Was the Prompt Effective?

The final prompt used — asking for user input, inline comments, and a post-code explanation — was **effective** in producing structured, comparable outputs from both tools. The specificity of the prompt ensured that both Perplexity AI and ChatGPT addressed the same dimensions, making comparison straightforward.

### What Worked Well?

- Asking for **inline comments** forced both tools to explain their logic as part of the code itself, which made it easy to evaluate understanding
- Requesting a **post-code explanation** revealed differences in how each tool communicates technical concepts to learners
- Keeping the prompt **task-focused** (not open-ended) prevented the tools from drifting into unrelated content

### What Could Be Improved?

| Limitation in Current Prompt | How to Fix It |
|---|---|
| Did not specify input type (integer only) | Add: *"Ensure the input is validated as a positive integer"* |
| Did not request multiple approaches | Add: *"Provide two solutions — one using a loop, one using built-in functions"* |
| Did not set complexity expectations | Add: *"Write this for a beginner audience"* or *"Write this for an intermediate Python developer"* |
| Did not ask for sample output | Add: *"Show a sample run with example inputs and expected output"* |

### Which Tool Would You Recommend for Coding Tasks?

> *(Write 2–3 sentences based on your experience. Example structure below — replace with your own opinion.)*
>
> *"For straightforward coding tasks, **ChatGPT** offered a more complete response with deeper explanation and alternative approaches. However, **Perplexity AI** is valuable when source verification matters, as it cited external references. For project coding assistance where iteration and explanation are important, ChatGPT proved slightly more useful — though both tools are capable when the prompt is well-designed."*

---

<div align="center">

**Report prepared as part of the AI-Assisted Project Coding Exercise**

*Prompt Design · API Comparison · Output Evaluation · Reflection*

*Tools Used: Perplexity AI · ChatGPT (GPT-4)*

</div>
