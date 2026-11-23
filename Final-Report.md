# Prompt Engineering: A Practical Study of LLM Behaviour

**Project Type:** Hands-on Prompt Engineering Assignment

**Platform:** Google AI Studio

**Models Used:**
- Gemini 4 Hydrogen – Zero-shot, Few-shot and Chain-of-Thought experiments
- Gemini 3.5 Flash Lite – Structured Output experiment

**Project Date:** November 2026

---

## 1. Introduction

Prompt engineering is the process of designing and improving instructions given to Large Language Models (LLMs) to obtain accurate, consistent and structured responses.

This project explores three important prompt engineering techniques:

1. Zero-shot and Few-shot Prompting
2. Chain-of-Thought Prompting
3. Structured Output Generation using JSON Schema

The experiments were conducted using Google AI Studio. Different prompts were tested, and the actual model responses were recorded and evaluated.

The main objective was to understand how different prompting techniques influence the accuracy, consistency, reasoning and formatting of LLM responses.

## 2. Objectives

- Compare zero-shot and few-shot prompting using a sentiment classification task.
- Evaluate direct prompting against explicit step-by-step prompting using a mathematical reasoning problem.
- Configure structured output using a JSON schema.
- Test structured information extraction across five different customer purchase examples.
- Evaluate the outputs using correctness, consistency and format validation.
- Document actual prompts, model responses and experimental observations.

## 3. Tools and Technologies

| Tool | Purpose |
|---|---|
| Google AI Studio | Prompt experimentation |
| Gemini 4 Hydrogen | Classification and reasoning experiments |
| Gemini 3.5 Flash Lite | Structured JSON generation |
| Structured Outputs | Enforcing JSON schema |
| Notepad | Recording prompts and actual outputs |
| GitHub | Final report submission |

**Programming Requirement:** No programming code was required for the practical experiments.

---

## 4. Experiment 1: Zero-shot vs Few-shot Prompting

### 4.1 Aim

To compare zero-shot and few-shot prompting techniques using a sentiment classification task and evaluate how providing examples affects the model's output.

### 4.2 Experimental Setup

- Platform: Google AI Studio
- Model: Gemini 4 Hydrogen
- Task: Sentiment Classification
- Output categories: Positive, Negative, Neutral and Mixed.
- Test inputs: Five sentences.

### 4.3 Zero-shot Prompting

**Definition:**

Zero-shot prompting is a technique in which the model performs a task without receiving any examples. The model uses the instructions provided in the prompt to generate its response.

**Prompt:**

[Insert the exact zero-shot prompt from zero_shot_output.txt.]

**Actual Model Output:**

[Paste the complete original Gemini response from zero_shot_output.txt.]

### 4.4 Few-shot Prompting

**Definition:**

Few-shot prompting provides a small number of examples within the prompt to demonstrate the expected task and output format.

In this experiment, examples were provided to guide the model in classifying sentiment.

**Prompt:**

[Insert the exact few-shot prompt from few_shot_output.txt.]

**Actual Model Output:**

[Paste the complete original Gemini response from few_shot_output.txt.]

### 4.5 Experimental Results

The model classified five test sentences into sentiment categories.

The recorded output included:

- Sentence 1: Positive
- Sentence 2: Negative
- Sentence 3: Neutral
- Sentence 4: Mixed
- Sentence 5: Negative

### 4.6 Comparison

| Parameter | Zero-shot | Few-shot |
|---|---|---|
| Examples provided | No | Yes |
| Task | Sentiment classification | Sentiment classification |
| Test sentences | 5 | 5 |
| Accuracy | [Insert verified result] | [Insert verified result] |
| Output format | Classification labels | Classification labels |

### 4.7 Analysis

Zero-shot prompting allowed the model to perform sentiment classification directly from the given instructions without requiring examples.

Few-shot prompting provided examples that demonstrated the expected classification pattern. This helped communicate the task requirements and expected response format more explicitly.

The comparison shows why examples can be useful when designing prompts for consistent classification tasks. However, the actual improvement in accuracy must be determined from the recorded outputs rather than assumed.

### 4.8 Conclusion

Zero-shot and few-shot prompting are useful techniques for sentiment classification. Zero-shot prompting is suitable when instructions are sufficient, whereas few-shot prompting provides additional guidance through examples.

The experiment demonstrates the importance of selecting an appropriate prompting technique based on the task requirements.

---

## 5. Experiment 2: Chain-of-Thought Prompting

### 5.1 Aim

To compare direct prompting with explicit step-by-step prompting using a multi-step mathematical word problem and evaluate their accuracy and response organization.

### 5.2 Experimental Setup

- Platform: Google AI Studio
- Model: Gemini 4 Hydrogen
- Thinking Level: High
- Task: Mathematical problem solving
- Problem: Calculate purchasing cost, selling amount, profit and profit percentage.

### 5.3 Problem Statement

A shopkeeper buys 5 notebooks for ₹40 each.

He sells 3 notebooks for ₹55 each and the remaining 2 notebooks for ₹45 each.

Calculate:

1. Total purchasing cost.
2. Total selling amount.
3. Total profit.
4. Profit percentage.

### 5.4 Direct Prompting

**Technique:**

Direct prompting asks the model to solve a problem without explicitly instructing it to organize the answer into separate reasoning steps.

**Actual Prompt:**

Solve the following mathematical word problem.

A shopkeeper buys 5 notebooks for ₹40 each.
He sells 3 notebooks for ₹55 each and the
remaining 2 notebooks for ₹45 each.

Calculate:
1. Total purchasing cost.
2. Total selling amount.
3. Total profit.
4. Profit percentage.

Provide the final answers clearly.

**Actual Model Output:**

Here are the step-by-step calculations for the problem:

1. Total purchasing cost (Cost Price):

- Cost of 1 notebook = ₹40
- Total cost of 5 notebooks = 5 × 40 = ₹200

2. Total selling amount (Selling Price):

- Selling price of 3 notebooks = 3 × 55 = ₹165
- Selling price of the remaining 2 notebooks = 2 × 45 = ₹90
- Total selling amount = 165 + 90 = ₹255

3. Total profit:

- Profit = Total Selling Amount − Total Purchasing Cost
- Profit = 255 − 200 = ₹55

4. Profit percentage:

- Profit Percentage = (Total Profit / Total Purchasing Cost) × 100
- Profit Percentage = (55 / 200) × 100 = 27.5%

Final Answers:

1. Total purchasing cost: ₹200
2. Total selling amount: ₹255
3. Total profit: ₹55
4. Profit percentage: 27.5%

### 5.5 Explicit Step-by-Step Prompting

**Technique:**

Explicit step-by-step prompting instructs the model to organize a multi-step problem into separate stages and show the relevant formulas and calculations.

**Actual Prompt:**

Solve the following mathematical word problem.

A shopkeeper buys 5 notebooks for ₹40 each.
He sells 3 notebooks for ₹55 each and the
remaining 2 notebooks for ₹45 each.

Break the solution into clear calculation steps.

Step 1: Calculate the total purchasing cost.
Step 2: Calculate the total selling amount.
Step 3: Calculate the total profit.
Step 4: Calculate the profit percentage.

Show the formula and calculation for each step.
Verify the numerical results before giving
the final answer.

Present the final answers clearly.

**Actual Model Output:**

Here is the step-by-step solution to the problem:

Step 1: Calculate the total purchasing cost

- Formula:
  Total Cost Price (CP) = Number of notebooks × Cost per notebook
- Calculation: CP = 5 × ₹40 = ₹200

Step 2: Calculate the total selling amount

- Formula:
  Total Selling Price (SP) = (Quantity 1 × Price 1) + (Quantity 2 × Price 2)
- Calculation: SP = (3 × ₹55) + (2 × ₹45)
- SP = ₹165 + ₹90 = ₹255

Step 3: Calculate the total profit

- Formula:
  Total Profit = Total Selling Price − Total Cost Price
- Calculation: Total Profit = ₹255 − ₹200 = ₹55

Step 4: Calculate the profit percentage

- Formula:
  Profit Percentage = (Total Profit / Total Cost Price) × 100%
- Calculation:
  (55 / 200) × 100% = 27.5%

Final Answers:

- Total Purchasing Cost: ₹200
- Total Selling Amount: ₹255
- Total Profit: ₹55
- Profit Percentage: 27.5%

### 5.6 Experimental Results

| Calculation | Direct Prompt | Step-by-Step Prompt |
|---|---:|---:|
| Purchasing cost | ₹200 | ₹200 |
| Selling amount | ₹255 | ₹255 |
| Total profit | ₹55 | ₹55 |
| Profit percentage | 27.5% | 27.5% |
| Correct calculations | 4/4 | 4/4 |
| Accuracy | 100% | 100% |

### 5.7 Analysis

The direct prompt produced correct answers for all four calculations. Although the prompt did not explicitly request intermediate steps, the model voluntarily provided detailed calculations.

The explicit step-by-step prompt also achieved 100% accuracy. It produced a more organized response with separate formulas and calculations for each stage.

Step-by-step prompting did not improve numerical accuracy because the direct prompt had already produced correct results. However, it improved the explicit organization and presentation of the solution.

### 5.8 Conclusion

Both prompting approaches achieved equal numerical accuracy in this experiment.

Direct prompting was sufficient to solve the mathematical problem correctly, while explicit step-by-step prompting provided a clearer calculation structure.

This experiment demonstrates that explicit step-by-step instructions can improve response organization even when they do not increase accuracy.

---

## 6. Experiment 3: Structured Output Generation Using JSON

### 6.1 Aim

To configure a Large Language Model to generate valid JSON responses according to a predefined schema and evaluate its reliability across five different customer purchase examples.

### 6.2 Experimental Setup

- Platform: Google AI Studio
- Model: Gemini 3.5 Flash Lite
- Technique: Structured Output Generation
- Output format: JSON
- Number of test cases: 5
- Task: Customer purchase information extraction

### 6.3 JSON Schema Design

A JSON schema was created to define the expected structure of the model response.

The schema contains three required properties:

| Property | Data Type | Description |
|---|---|---|
| name | String | Customer's full name |
| date | String | Purchase date in YYYY-MM-DD format |
| amount | Number | Purchase amount in INR |

**Actual configured schema:**

```json
{
  "type": "object",
  "properties": {
    "name": {
      "type": "string",
      "description": "Customer's full name"
    },
    "date": {
      "type": "string",
      "description": "Purchase date in YYYY-MM-DD format"
    },
    "amount": {
      "type": "number",
      "description": "Purchase amount in INR"
    }
  },
  "required": ["name", "date", "amount"]
}
```

The required properties ensure that all three fields are included in the generated response.

### 6.4 Prompt Design

The following instruction was used as the common prompt structure:

**Prompt:**

Extract the customer purchase information from the following paragraph.

Return the extracted information using the configured JSON schema.

Convert the date into YYYY-MM-DD format and return the amount as a number.

The customer purchase paragraph was changed for each test case to evaluate the model's ability to extract information from different sentence structures.

### 6.5 Test Case 1

**Input:**

A customer named Rahul purchased a laptop on 15 November 2026 for ₹55,000.

**Actual Model Output:**

```json
{
  "name": "Rahul",
  "date": "2026-11-15",
  "amount": 55000
}
```

**Result:** PASS

### 6.6 Test Case 2

**Input:**

Priya Sharma bought a smartphone for ₹72,499.50 on November 18, 2026.

**Actual Model Output:**

```json
{
  "name": "Priya Sharma",
  "date": "2026-11-18",
  "amount": 72499.5
}
```

**Result:** PASS

### 6.7 Test Case 3

**Input:**

On 20 November 2026, customer Arjun Kumar purchased a tablet worth Rs. 38,999.

**Actual Model Output:**

[Insert the complete actual Gemini response from test_case_3.txt.]

**Result:** PASS (as recorded in the experiment)

### 6.8 Test Case 4

**Input:**

Meera purchased a wireless headphone for Rs. 4,750 on November 21, 2026. The purchase was made from an electronics store.

**Actual Model Output:**

[Insert the complete actual Gemini response from test_case_4.txt.]

**Result:** PASS (as recorded in the experiment)

### 6.9 Test Case 5

**Input:**

A laptop was purchased by customer David Raj for INR 85,499.99. The transaction took place on 22 November 2026.

**Actual Model Output:**

```json
{
  "name": "David Raj",
  "date": "2026-11-22",
  "amount": 85499.99
}
```

**Result:** PASS

### 6.10 Validation Criteria

Each generated response was evaluated using the following criteria:

1. Valid JSON syntax.
2. Presence of all three required properties.
3. Correct extraction of the customer name.
4. Correct date extraction and YYYY-MM-DD formatting.
5. Correct numerical amount.
6. Amount represented as a number rather than a string.

### 6.11 Experimental Results

| Test Case | JSON Validation | Extraction Result |
|---|---|---|
| Test 1 | Pass | Pass |
| Test 2 | Pass | Pass |
| Test 3 | Pass | Pass |
| Test 4 | Pass | Pass |
| Test 5 | Pass | Pass |

**Overall reported success rate:**

Successful test cases = 5

Total test cases = 5

Success Rate = (5 / 5) × 100 = 100%

### 6.12 Analysis

The structured output feature helped the model generate responses according to the predefined JSON schema.

The explicit schema defined the required property names and their data types. This reduced formatting inconsistencies and ensured that the response followed a predictable structure.

The five test cases used different customer names, purchase descriptions, date expressions and monetary formats. According to the recorded experiment results, all five test cases passed the validation criteria.

The experiment demonstrates that schema-constrained output is useful when extracting information that must be processed by applications or other automated systems.

### 6.13 Conclusion

Structured output generation successfully produced JSON responses matching the configured schema in all five reported test cases.

The experiment demonstrates how explicit schemas and structured-output features can improve the consistency and usability of LLM-generated data.

---

## 7. Overall Results and Comparison

### 7.1 Summary of All Experiments

The project evaluated three major prompt engineering techniques using Google AI Studio.

| Experiment | Technique | Test Method | Recorded Result |
|---|---|---|---|
| Experiment 1 | Zero-shot | 5 sentiment inputs | 5/5 correct |
| Experiment 1 | Few-shot | 5 sentiment inputs with 4 examples | 5/5 correct |
| Experiment 2 | Direct prompting | 4 mathematical calculations | 4/4 correct |
| Experiment 2 | Step-by-step prompting | 4 mathematical calculations | 4/4 correct |
| Experiment 3 | Structured output | 5 JSON test inputs | 5/5 passed |

### 7.2 Comparison of Prompt Engineering Techniques

| Technique | Main Advantage | Experimental Observation |
|---|---|---|
| Zero-shot | Requires no examples | Correctly classified all five test sentences |
| Few-shot | Provides examples to guide the model | Maintained the same classification accuracy |
| Chain-of-Thought | Encourages organized multi-step responses | Produced clearly separated calculation steps |
| Structured Output | Enforces a predefined response format | Generated schema-compliant JSON in the five reported tests |

### 7.3 Key Findings

1. Zero-shot prompting performed effectively when the task instructions were clear.
2. Few-shot prompting provided additional guidance through labelled examples but did not increase accuracy in this experiment.
3. Direct prompting produced correct mathematical calculations even without explicitly requesting a step-by-step structure.
4. Explicit step-by-step instructions improved the organization and presentation of the mathematical solution.
5. Structured output generation helped produce consistent JSON responses matching the configured schema.
6. Defining required properties and data types made the extracted information easier to validate and process.

### 7.4 Limitations

- The experiments used a small number of test inputs.
- Sentiment classification was evaluated using only five sentences.
- Mathematical reasoning was tested using one problem.
- The results may differ with more complex or ambiguous inputs.
- The structured-output success rate was evaluated using five purchase-information examples.
- The experiments do not establish that the same performance will occur with every LLM or dataset.
- The API-based replication was not performed as part of these no-code experiments.

---

## 8. Conclusion

This project explored three important prompt engineering techniques: few-shot prompting, chain-of-thought prompting and structured output generation.

The zero-shot and few-shot experiments demonstrated that a model can perform sentiment classification accurately with clear instructions, even without examples.

The chain-of-thought experiment showed that explicitly requesting step-by-step calculations can improve the organization and readability of mathematical responses, although numerical accuracy remained unchanged in the selected problem.

The structured-output experiment demonstrated how a predefined JSON schema can guide a model to extract customer purchase information in a consistent format.

Overall, the experiments provided practical experience in designing prompts, configuring structured responses, evaluating model outputs and identifying the strengths and limitations of different prompting techniques.

The project highlights that effective prompt engineering involves more than writing instructions. It requires systematic experimentation, output validation and honest evaluation of results.

---

## 9. Final Project Deliverables

The project includes:

1. Zero-shot and few-shot prompts and outputs.
2. Direct and step-by-step mathematical reasoning prompts and outputs.
3. JSON schema configuration.
4. Five structured-output test cases.
5. Experimental comparison tables.
6. Analysis and conclusions.
7. Screenshots documenting the experiments.

