# Ex.No.4 – Advanced Prompt Patterns for AI-Powered Manufacturing

### DATE:
08-08-2026

### REGISTER NUMBER:
212224040028

---

# AIM

To design and evaluate prompts using different advanced prompt engineering patterns such as Zero-shot Prompting, Few-shot Prompting, Chain-of-Thought, Persona Pattern, Reverse Prompting, Graph Prompting, and Active Prompting, and compare their effectiveness using a rubric-based evaluation method.

---

# USE CASE

## AI-Powered Smart Manufacturing and Predictive Maintenance

The manufacturing industry wants to reduce manual monitoring and improve production efficiency using IoT devices and embedded controllers.

The proposed system monitors:

- Machine temperature
- Vibration
- Energy consumption
- Production rate
- Machine operating hours
- Equipment status

The system uses sensor data to identify abnormal machine behavior and predict possible equipment failures.

## Main Objectives

- Improve production efficiency by **30%**.
- Minimize machinery downtime using predictive maintenance.
- Enable real-time monitoring and remote control.
- Reduce energy consumption through process optimization.
- Detect machine faults at an early stage.

---

# PROCEDURE

1. Define the manufacturing use case.
2. Select the AI task for prompt generation.
3. Apply different prompt engineering patterns.
4. Generate responses using AI tools.
5. Compare the generated outputs.
6. Evaluate the outputs using a rubric.
7. Identify the most effective prompting technique.

---

# 1. ZERO-SHOT PROMPTING

## Definition

Zero-shot prompting provides the AI with a direct instruction without giving examples.

## Prompt

> Explain how an IoT-based predictive maintenance system can monitor manufacturing machines, detect possible failures, and reduce machine downtime. Explain it in simple terms with a practical example.

## Expected Output

The AI should explain how sensors collect machine data, how abnormal conditions are detected, and how maintenance can be scheduled before a machine fails.

## Evaluation

- Simple and direct.
- Requires no examples.
- Fast to generate.
- Suitable for general explanations.
- May provide less specialized information.

---

# 2. FEW-SHOT PROMPTING

## Definition

Few-shot prompting provides the AI with a few examples before asking it to perform a similar task.

## Prompt

> Example 1:  
> **Sensor:** Temperature sensor  
> **Abnormal Reading:** Temperature continuously increases  
> **Possible Problem:** Machine overheating  
> **Action:** Inspect cooling system.
>
> Example 2:  
> **Sensor:** Vibration sensor  
> **Abnormal Reading:** High vibration level  
> **Possible Problem:** Bearing damage  
> **Action:** Schedule machine inspection.
>
> Now analyze the following manufacturing condition:
>
> **Sensor:** Energy sensor  
> **Abnormal Reading:** Energy consumption suddenly increases  
>
> Identify the possible problem and recommended action.

## Expected Output

> **Possible Problem:** Motor or equipment may be operating inefficiently or experiencing a mechanical fault.  
> **Recommended Action:** Inspect the motor, bearings, and power system and compare the current energy consumption with historical values.

## Evaluation

- Provides consistent responses.
- Examples guide the AI.
- Useful for repeated industrial tasks.
- More reliable for structured outputs than a basic prompt.

---

# 3. CHAIN-OF-THOUGHT PROMPTING

## Definition

Chain-of-Thought prompting encourages the AI to approach a complex problem through a sequence of reasoning steps.

## Prompt

> A manufacturing machine has shown increasing vibration, increasing temperature, and higher energy consumption during the last three operating cycles. Analyze the situation systematically. Identify the possible cause, supporting indicators, risk level, recommended maintenance action, and expected benefit of taking action before failure.

## Expected Output Structure

1. Identify abnormal sensor readings.
2. Determine possible relationships between the readings.
3. Identify the most likely equipment problem.
4. Estimate the potential risk.
5. Recommend a maintenance action.
6. Explain how early maintenance can reduce downtime.

## Evaluation

- Suitable for complex problems.
- Produces systematic analysis.
- Helps identify relationships between multiple sensor readings.
- Useful for predictive maintenance decisions.

---

# 4. PERSONA PATTERN

## Definition

Persona prompting assigns a specific professional role to the AI so that it responds from that perspective.

## Prompt

> Act as an experienced industrial IoT and predictive maintenance engineer. Analyze a manufacturing machine that shows abnormal vibration, increasing temperature, and rising energy consumption. Explain the possible causes, recommended maintenance actions, and methods to prevent future failures. Present the explanation so that a factory maintenance manager can understand it easily.

## Expected Output

The AI should respond like an industrial maintenance expert and focus on:

- Machine health
- Sensor readings
- Failure prediction
- Maintenance planning
- Production downtime
- Energy efficiency

## Evaluation

- Provides domain-focused responses.
- Uses appropriate technical terminology.
- Improves relevance.
- Useful for professional decision-making.

---

# 5. REVERSE PROMPTING

## Definition

Reverse prompting starts with the desired output and asks the AI to create or improve the prompt required to generate that output.

## Prompt

> I need an AI-generated predictive maintenance report containing:
>
> - Machine status
> - Sensor abnormalities
> - Possible failure
> - Risk level
> - Recommended maintenance
> - Estimated downtime
> - Preventive action
>
> Create an effective prompt that I can give to an AI system to generate this report from IoT sensor data.

## Expected Output

The AI may generate a prompt such as:

> "Analyze the provided IoT sensor data from a manufacturing machine. Identify abnormal readings, determine the likely equipment fault, classify the risk level, recommend maintenance actions, estimate possible downtime, and suggest preventive measures. Present the results in a structured predictive maintenance report."

## Evaluation

- Useful for creating reusable prompts.
- Helps users who do not know how to formulate complex prompts.
- Produces task-specific prompts.
- Useful for developing AI-based industrial applications.

---

# 6. GRAPH PROMPTING

## Definition

Graph prompting represents information as connected entities and relationships. It is useful when multiple components have dependencies or relationships.

## Prompt

> Represent the smart manufacturing predictive maintenance system as a relationship graph using the following components:
>
> Sensors → IoT Gateway → Data Processing → AI Model → Fault Detection → Maintenance Alert → Maintenance Team.
>
> Show the relationship between each component and explain how information flows through the system.

## Expected Output

```text
Temperature Sensor ──┐
Vibration Sensor ────┤
Energy Sensor ───────┤
                     ↓
                IoT Gateway
                     ↓
              Data Processing
                     ↓
                AI Model
                     ↓
              Fault Detection
                     ↓
             Maintenance Alert
                     ↓
             Maintenance Team
                     ↓
              Machine Service
```

## Evaluation

- Clearly represents relationships.
- Makes complex systems easier to understand.
- Useful for architecture and workflow analysis.
- Helps visualize dependencies between components.

---

# 7. ACTIVE PROMPTING

## Definition

Active prompting allows the AI to identify missing information and ask the user relevant questions before producing the final response.

## Prompt

> You are designing a predictive maintenance system for a manufacturing plant. Before recommending the AI solution, ask me the most important questions about the machines, available sensors, production environment, historical data, failure records, and required response time. After receiving my answers, design the predictive maintenance solution.

## Example AI Questions

1. What type of machines are being monitored?
2. Which sensors are currently available?
3. How frequently is sensor data collected?
4. Is historical machine failure data available?
5. How quickly should maintenance alerts be generated?

## Evaluation

- Improves personalization.
- Reduces assumptions.
- Collects missing information.
- Produces more relevant solutions.
- Useful for real-world project requirements.

---

# COMPARISON OF PROMPT PATTERNS

| Prompt Pattern | Main Purpose | Strength | Limitation |
|---|---|---|---|
| Zero-shot | Direct task | Simple and fast | Less context |
| Few-shot | Learn from examples | Consistent output | Requires examples |
| Chain-of-Thought | Complex reasoning | Detailed analysis | Can be lengthy |
| Persona | Expert perspective | Domain-focused output | Depends on role definition |
| Reverse | Create better prompts | Reusable prompts | Requires clear desired output |
| Graph | Show relationships | Excellent visualization | More suitable for structured systems |
| Active | Gather missing information | Highly personalized | Requires interaction |

---

# RUBRIC-BASED EVALUATION

Each prompting technique is evaluated on a scale of **1 to 5**.

### Evaluation Criteria

| Score | Meaning |
|---|---|
| 5 | Excellent |
| 4 | Very Good |
| 3 | Good |
| 2 | Average |
| 1 | Poor |

---

# EVALUATION TABLE

| Prompt Pattern | Accuracy | Relevance | Clarity | Structure | Usefulness | Total / 25 |
|---|---:|---:|---:|---:|---:|---:|
| Zero-shot | 4 | 4 | 5 | 4 | 4 | **21** |
| Few-shot | 5 | 5 | 4 | 5 | 5 | **24** |
| Chain-of-Thought | 5 | 5 | 4 | 5 | 5 | **24** |
| Persona | 5 | 5 | 5 | 4 | 5 | **24** |
| Reverse | 4 | 5 | 4 | 5 | 5 | **23** |
| Graph | 5 | 5 | 5 | 5 | 5 | **25** |
| Active | 5 | 5 | 5 | 4 | 5 | **24** |

---

# OBSERVATION

- **Zero-shot prompting** was the simplest and fastest technique for general explanations.
- **Few-shot prompting** improved consistency by providing examples to the AI.
- **Chain-of-Thought prompting** was useful for analyzing complex machine-failure scenarios.
- **Persona prompting** generated domain-specific responses suitable for industrial professionals.
- **Reverse prompting** was useful for designing reusable prompts.
- **Graph prompting** provided the clearest representation of relationships between IoT components.
- **Active prompting** produced personalized solutions by collecting missing information first.

---

# RESULT

The different prompt engineering patterns were successfully designed and evaluated for the smart manufacturing predictive maintenance use case. Each technique produced different benefits depending on the task, with **Graph Prompting** achieving the highest rubric score for representing the relationships and workflow of the IoT-based manufacturing system.

---

# CONCLUSION

Advanced prompt engineering techniques significantly improve the quality and usefulness of AI-generated responses. Simple techniques such as Zero-shot prompting are suitable for direct questions, while Few-shot and Chain-of-Thought prompting are useful for complex tasks. Persona, Reverse, Graph, and Active prompting provide additional control, specialization, visualization, and personalization. Therefore, selecting the appropriate prompt pattern according to the task is essential for developing effective AI-powered manufacturing applications.
