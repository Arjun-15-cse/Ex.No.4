# Ex.No.4 – Evaluation of Advanced Prompt Engineering Patterns

### DATE:
08-08-2026

### REGISTER NUMBER:
212224040028

---

# AIM

To implement and evaluate different prompt engineering patterns — Zero-shot Prompting, Few-shot Prompting, Chain-of-Thought, Persona Pattern, Reverse Prompting, Graph Prompting, and Active Prompting — using an engineering case study and compare their performance based on reasoning, correctness, and token usage.

---

# CASE STUDY

## Smart Irrigation System

A smart irrigation system uses IoT sensors and AI to monitor soil and environmental conditions and automatically control water supply to crops.

The system collects:

- Soil moisture
- Temperature
- Humidity
- Rainfall
- Water availability

The AI system analyzes the sensor data and determines whether irrigation is required.

### Objective

The main goal is to provide the required amount of water to crops while reducing water wastage and improving irrigation efficiency.

---

# 1. ZERO-SHOT PROMPTING

## Definition

Zero-shot prompting gives the AI a direct instruction without providing examples.

### Prompt

> Analyze the following smart irrigation sensor data and determine whether irrigation is required: Soil moisture = 25%, Temperature = 34°C, Humidity = 45%, Rainfall = 0 mm. Give the recommended action and explain why.

### Expected Output

> Irrigation is required because the soil moisture is low and there is no rainfall. The system should provide a suitable amount of water to maintain healthy crop growth.

### Evaluation

- **Reasoning:** Good
- **Correctness:** High
- **Token Usage:** Low

### Observation

Zero-shot prompting provides a quick response with minimal instructions, making it suitable for simple irrigation decisions.

---

# 2. FEW-SHOT PROMPTING

## Definition

Few-shot prompting provides examples to guide the AI before presenting the actual problem.

### Prompt

> Example 1:  
> Soil moisture = 20%, Rainfall = 0 mm → Irrigation Required.
>
> Example 2:  
> Soil moisture = 70%, Rainfall = 5 mm → Irrigation Not Required.
>
> Example 3:  
> Soil moisture = 40%, Rainfall = 0 mm → Moderate Irrigation.
>
> Now analyze:
>
> Soil moisture = 25%, Rainfall = 0 mm.
>
> Determine the irrigation requirement and recommended action.

### Expected Output

> Irrigation is required because the soil moisture is 25% and there has been no rainfall. Based on the examples, the system should initiate irrigation.

### Evaluation

- **Reasoning:** Very Good
- **Correctness:** Very High
- **Token Usage:** Medium

### Observation

Few-shot prompting improves consistency because the AI learns the expected decision pattern from the examples.

---

# 3. CHAIN-OF-THOUGHT PROMPTING

## Definition

Chain-of-Thought prompting encourages the AI to analyze a problem through multiple reasoning steps before reaching a conclusion.

### Prompt

> Analyze this smart irrigation situation systematically. Consider soil moisture, temperature, humidity, and rainfall. Determine the crop's irrigation requirement, identify the main factors affecting the decision, and recommend an appropriate action.
>
> Sensor Data:
> - Soil moisture: 25%
> - Temperature: 34°C
> - Humidity: 45%
> - Rainfall: 0 mm

### Expected Output

> The soil moisture level is low, the temperature is relatively high, and there has been no rainfall. These conditions indicate that the crop may require additional water. The irrigation controller should activate irrigation while considering crop type and soil characteristics.

### Evaluation

- **Reasoning:** Excellent
- **Correctness:** Very High
- **Token Usage:** High

### Observation

Chain-of-Thought prompting is useful for engineering problems involving multiple variables, although it generally requires more output tokens.

---

# 4. PERSONA PATTERN

## Definition

Persona prompting assigns a professional role to the AI so that it responds from a specific expert perspective.

### Prompt

> Act as an agricultural IoT engineer specializing in smart irrigation systems. Analyze the following sensor readings and recommend an irrigation decision:
>
> Soil moisture = 25%, Temperature = 34°C, Humidity = 45%, Rainfall = 0 mm.
>
> Consider water conservation and crop health while providing your recommendation.

### Expected Output

> As an agricultural IoT engineer, I would recommend initiating irrigation because the soil moisture is relatively low and no rainfall has occurred. However, the irrigation duration should also consider crop type, soil type, weather forecasts, and water availability to prevent over-irrigation.

### Evaluation

- **Reasoning:** Excellent
- **Correctness:** Excellent
- **Token Usage:** Medium

### Observation

The Persona Pattern provides domain-specific recommendations and considers practical engineering factors.

---

# 5. REVERSE PROMPTING

## Definition

Reverse prompting starts with the desired output and asks the AI to create an effective prompt for generating that output.

### Prompt

> I want an AI system to produce a smart irrigation decision containing:
>
> - Sensor condition
> - Irrigation requirement
> - Reason
> - Water conservation recommendation
> - Final action
>
> Create an effective prompt that can be used with smart irrigation sensor data to generate this output.

### Expected Output

> Analyze the provided smart irrigation sensor readings and determine whether irrigation is required. Consider soil moisture, temperature, humidity, rainfall, and water availability. Provide the sensor condition, reasoning, irrigation recommendation, water conservation suggestion, and final action in a structured format.

### Evaluation

- **Reasoning:** Good
- **Correctness:** Very Good
- **Token Usage:** Medium
- **Reusability:** Excellent

### Observation

Reverse prompting is useful for creating reusable prompts for an AI-powered irrigation application.

---

# 6. GRAPH PROMPTING

## Definition

Graph prompting represents a system using entities and relationships. It is useful for understanding how different components interact.

### Prompt

> Represent a smart irrigation system as a graph showing the relationship between sensors, IoT gateway, AI analysis, irrigation controller, water pump, and crops. Explain the direction of information flow.

### Expected Output

```text
Soil Moisture Sensor ──┐
Temperature Sensor ───┤
Humidity Sensor ──────┤
Rain Sensor ──────────┤
                      ↓
                 IoT Gateway
                      ↓
                AI Analysis
                      ↓
             Irrigation Decision
                      ↓
             Irrigation Controller
                      ↓
                  Water Pump
                      ↓
                    Crops
```

### Evaluation

- **Reasoning:** Excellent
- **Correctness:** Excellent
- **Token Usage:** Medium
- **Clarity:** Excellent

### Observation

Graph prompting clearly represents the relationships between components and is useful for understanding system architecture.

---

# 7. ACTIVE PROMPTING

## Definition

Active prompting allows the AI to ask for additional information before making a final decision.

### Prompt

> You are designing a smart irrigation system. Before deciding whether irrigation should be activated, ask the most important questions about the crop, soil, weather conditions, sensor readings, and water availability. After receiving the information, provide the irrigation recommendation.

### Expected Output

The AI may ask:

1. What type of crop is being grown?
2. What is the soil type?
3. What is the current soil moisture?
4. Is rainfall expected?
5. How much water is available?
6. When was the last irrigation cycle?

After receiving the answers, the AI can provide a more reliable irrigation recommendation.

### Evaluation

- **Reasoning:** Excellent
- **Correctness:** Excellent
- **Token Usage:** High
- **Personalization:** Excellent

### Observation

Active prompting reduces assumptions by collecting missing information before making an engineering decision.

---

# COMPARISON OF PROMPTING PATTERNS

| Prompt Pattern | Reasoning | Correctness | Token Usage |
|---|---|---|---|
| Zero-shot | Good | High | Low |
| Few-shot | Very Good | Very High | Medium |
| Chain-of-Thought | Excellent | Very High | High |
| Persona Pattern | Excellent | Excellent | Medium |
| Reverse Prompting | Good | Very Good | Medium |
| Graph Prompting | Excellent | Excellent | Medium |
| Active Prompting | Excellent | Excellent | High |

---

# RUBRIC

The AI outputs are evaluated using a 5-point scale.

| Score | Evaluation |
|---|---|
| 5 | Excellent |
| 4 | Very Good |
| 3 | Good |
| 2 | Average |
| 1 | Poor |

### Evaluation Criteria

**Reasoning:** How effectively the prompt helps the AI analyze the engineering problem.

**Correctness:** How accurately the AI produces the expected technical result.

**Token Usage:** The approximate amount of text/tokens required to produce the response. Lower usage is preferred when the quality remains high.

---

# FINAL EVALUATION

| Prompt Pattern | Reasoning /5 | Correctness /5 | Token Efficiency /5 | Total /15 |
|---|---:|---:|---:|---:|
| Zero-shot | 4 | 4 | 5 | **13** |
| Few-shot | 4 | 5 | 4 | **13** |
| Chain-of-Thought | 5 | 5 | 3 | **13** |
| Persona Pattern | 5 | 5 | 4 | **14** |
| Reverse Prompting | 4 | 4 | 4 | **12** |
| Graph Prompting | 5 | 5 | 4 | **14** |
| Active Prompting | 5 | 5 | 3 | **13** |

---

# OBSERVATION

- **Zero-shot prompting** used the fewest tokens and was effective for simple decisions.
- **Few-shot prompting** improved correctness by providing examples.
- **Chain-of-Thought** produced strong reasoning but required more tokens.
- **Persona Pattern** improved domain-specific reasoning and practical recommendations.
- **Reverse Prompting** was useful for creating reusable prompts.
- **Graph Prompting** was highly effective for representing relationships between system components.
- **Active Prompting** produced highly contextual decisions but required additional interaction and tokens.

---

# RESULT

The seven prompt engineering patterns were successfully implemented for the **Smart Irrigation** engineering case study. The experiment showed that different prompting techniques provide different advantages in reasoning, correctness, and token efficiency.

---

# CONCLUSION

Advanced prompt engineering techniques can significantly improve AI performance in engineering applications. **Persona and Graph Prompting** provided a strong balance of reasoning and correctness, while **Zero-shot Prompting** was the most token-efficient. **Chain-of-Thought and Active Prompting** were effective for complex problems but required more tokens. Therefore, the best prompting technique depends on the complexity and requirements of the engineering task.
