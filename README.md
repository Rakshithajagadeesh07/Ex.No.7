# Ex.No.7 – Develop a Prompt-Based Application Tailored to Personal Needs

## Date: 05-09-2026
## Register No.: 212223240135

# Aim

To develop a prompt-based application using ChatGPT that demonstrates how Large Language Models can be used to assist with explainable AI-driven multi-crop farm monitoring and management, with prompts progressing from simple to advanced designs and producing increasingly useful, personalized, and explainable outputs.

# AI Tools Required

- ChatGPT
- Python
- FastAPI
- React.js
- PostgreSQL / TimescaleDB (time-series sensor data)
- IoT sensors (soil moisture, temperature, pH)
- Drone / satellite imagery APIs (NDVI, canopy health)
- TensorFlow / PyTorch (CNN for disease detection, LSTM for growth & yield prediction)
- SHAP / LIME (Explainable AI)
- MQTT (sensor data ingestion)
- Pandas
- Large Language Model (LLM)
- Web Browser
- Visual Studio Code

# Project Used

**AgriTwin – A Unified Multi-Crop Digital Twin for Explainable AI-Driven Crop Monitoring and Intelligent Farm Management**

AgriTwin is a full-stack precision-agriculture platform that builds a continuously updated **virtual replica (digital twin)** of a farm, capable of monitoring **multiple crop types simultaneously** on the same land. It integrates IoT soil sensors, drone/satellite imagery, and weather data with AI models to predict irrigation needs, pest/disease outbreaks, and expected yield per crop zone.

The system uses a **React.js** frontend, **FastAPI** backend, Python-based AI/ML pipelines, **PostgreSQL/TimescaleDB** for sensor and twin-state persistence, and **Pandas** for feature engineering and zone-level analysis. A key differentiator of AgriTwin is its **Explainable AI (XAI) layer**, which translates model outputs (e.g., SHAP feature-importance values) into plain-language justifications so that farmers can understand *why* a recommendation was made, not just *what* it is.

The prompt-based application developed for this experiment acts as an **AI Farm Advisory Assistant** for AgriTwin's Decision-Support Layer.

<img width="878" height="436" alt="image" src="https://github.com/user-attachments/assets/bcc9cc85-1ada-45d4-80c0-7cdf8ad042c7" />


# Explanation

A prompt-based application uses carefully designed natural-language instructions to communicate with a Large Language Model and generate useful responses according to user requirements.

In AgriTwin, a prompt-based AI assistant can be used to:

- Analyze real-time digital twin data for a specific crop zone
- Interpret sensor readings (soil moisture, pH, NPK) alongside satellite-derived NDVI
- Suggest irrigation schedules tailored to crop type and growth stage
- Recommend pest/disease management actions based on CNN model confidence scores
- Explain AI recommendations in plain, farmer-friendly language (XAI translation)
- Forecast yield risk for a given zone
- Generate safety-conscious, non-extreme agronomic guidance
- Consider multiple crops growing simultaneously on adjacent zones of the same farm
- Produce dashboard-ready, structured recommendations for the decision-support layer

The experiment demonstrates how progressively improving a prompt can produce more relevant, structured, explainable, and multi-crop-aware AI-generated recommendations.

**Note:** AI-generated agronomic recommendations are intended for general decision-support guidance and should be verified by a qualified agronomist or extension officer, especially before large-scale application of pesticides, fertilizers, or irrigation changes.

# Problem Statement

Develop a prompt-based AI Farm Advisory Assistant for the AgriTwin project that accepts a specific crop zone's digital twin data (sensor readings, imagery-derived indices, and AI model outputs) and generates personalized, **explainable** crop management recommendations.

The assistant should understand the zone's condition and generate an appropriate response using a Large Language Model while considering factors such as crop type, growth stage, soil condition, NDVI trend, pest-model confidence, weather forecast, and historical yield — and must explain the reasoning behind each recommendation, consistent with AgriTwin's explainable-AI design goal.

# Prompt-Based Application

The application is designed as an **AI Farm Advisory Assistant** operating within AgriTwin's Decision-Support Layer.

## Input

The system provides:

- Zone ID and crop type
- Growth stage
- Soil moisture (%) and soil pH
- NPK (nutrient) levels
- NDVI value (current and previous reading, from satellite/drone imagery)
- Pest/disease detection confidence (from CNN model)
- Short-term weather forecast
- Historical yield for the zone
- Farmer's preferred language/simplicity level

## Processing

```
Digital Twin Zone Data (sensors + imagery + models)
        ↓
Prompt Construction
        ↓
Large Language Model
        ↓
Agronomic & Explainability Analysis
        ↓
Personalized, Explainable Recommendations
        ↓
Irrigation / Pest / Nutrient / Yield-Risk Guidance
        ↓
Farmer / Agronomist (via Dashboard or Mobile App)
```

## Output

The application generates:

- Irrigation recommendation (amount and timing)
- Pest/disease alert and recommended action
- Fertilizer/nutrient guidance
- Yield-risk forecast for the zone
- Plain-language explanation of *why* each recommendation was made (XAI translation)
- Safety and escalation considerations

# Procedure

1. Identify a practical requirement from the AgriTwin project.
2. Define the crop zone's digital twin profile and expected recommendation.
3. Create a simple prompt for the selected task.
4. Execute the prompt using ChatGPT.
5. Observe and record the generated response.
6. Improve the prompt by adding platform/zone context.
7. Introduce a specific AI role for more professional, explainable recommendations.
8. Create an advanced structured prompt with detailed requirements and an explainability report.
9. Compare the outputs obtained from the four prompting techniques.
10. Develop a final refined prompt suitable for integration into AgriTwin's Decision-Support Layer.
11. Evaluate the usefulness, explainability, and consistency of the final AI-generated response.

# Selected Engineering Scenario

The selected scenario is **explainable irrigation and pest-management recommendation for a single crop zone within a multi-crop farm.**

A sample zone profile is provided to the AI assistant:

- Zone ID: Zone 3
- Crop: Maize
- Growth Stage: Tasseling
- Soil Moisture: 18% (target range 25–30%)
- Soil pH: 6.2
- NDVI: 0.52 (declining from 0.61 the previous week)
- Pest Model Confidence: 78% likelihood of Fall Armyworm
- Weather Forecast: No rainfall expected for the next 5 days
- Historical Average Yield (Zone 3): 4.2 tons/acre
- Adjacent Zones: Zone 1 (Wheat), Zone 2 (Vegetables)

The objective is to generate a personalized, explainable irrigation and pest-management recommendation for Zone 3, considering its role within the unified multi-crop digital twin.

# Prompt 1 – Simple Prompt

**Prompt**
```
Analyze this farm zone data and tell me what to do:

Crop: Maize
Growth Stage: Tasseling
Soil Moisture: 18%
Soil pH: 6.2
NDVI: 0.52 (declining from 0.61)
Pest Detection Confidence: 78% Fall Armyworm
Weather: No rain for 5 days
```

**Output**

- Irrigate the field soon since soil moisture is low.
- Declining NDVI may indicate stress; monitor closely.
- 78% pest detection confidence is high — apply a suitable pesticide for Fall Armyworm.
- Recheck soil and canopy conditions in a few days.

**Observation**
The simple prompt generates a basic recommendation but provides limited personalization, no explanation of *why* each action matters, and does not consider the multi-crop digital twin context or other zones on the farm.

# Prompt 2 – Context-Based Prompt

**Prompt**
```
You are assisting AgriTwin, a unified multi-crop digital twin platform for explainable AI-driven crop monitoring. Based on the following zone data from a farm that also grows wheat and vegetables in adjacent zones, generate an irrigation and pest-management recommendation for this maize zone.

Zone Data:
Crop: Maize | Growth Stage: Tasseling
Soil Moisture: 18% (target 25-30%) | Soil pH: 6.2
NDVI: 0.52, down from 0.61 last week
Pest Detection Confidence: 78% Fall Armyworm
Weather Forecast: No rain expected for 5 days
Historical Yield: 4.2 tons/acre

Include irrigation guidance, pest management options, and a brief note on nutrient status.
```

**Output**

| Category | Recommendation |
|---|---|
| Irrigation | Apply approximately 25–30 mm of irrigation within the next 24–48 hours, since soil moisture (18%) is well below the target range and no rain is forecast. |
| Pest Management | High-confidence Fall Armyworm detection (78%) during tasseling — recommend field scouting confirmation followed by a targeted biological or chemical treatment. |
| Nutrient Status | Soil pH of 6.2 is acceptable for maize; monitor nitrogen levels given the tasseling stage's high nutrient demand. |
| NDVI Trend | Declining NDVI (0.61 → 0.52) suggests early stress — irrigation and pest control should help stabilize canopy health. |

**Observation**
The context-based prompt produces a more personalized response because it provides information about the AgriTwin platform, the multi-crop farm setting, and the zone's specific growth stage and trend data.

# Prompt 3 – Role-Based Prompt

**Prompt**
```
Act as a professional agronomy AI advisor working within AgriTwin's Explainable AI Decision-Support Layer. Analyze the following maize zone data and prepare a practical, explainable recommendation.

Zone Data:
Crop: Maize | Growth Stage: Tasseling
Soil Moisture: 18% (target 25-30%) | Soil pH: 6.2
NDVI: 0.52, down from 0.61 last week
Pest Detection Confidence: 78% Fall Armyworm
Weather Forecast: No rain expected for 5 days
Historical Yield: 4.2 tons/acre

Your response should:
- Recommend irrigation timing and approximate amount.
- Recommend pest management action appropriate to the confidence level.
- Explain the reasoning behind each recommendation (which factor influenced it most).
- Avoid recommending unsafe or excessive pesticide/fertilizer use.
- Present the result in a clear table.
```

**Output**

**AgriTwin Zone 3 Explainable Advisory**

| Recommendation | Action | Reasoning (Explainability) |
|---|---|---|
| Irrigation | Irrigate with ~25–30 mm within 24–48 hours | Soil moisture (18%) is the strongest contributing factor — it is 7–12 points below the optimal range, and no rain is forecast for 5 days |
| Pest Management | Confirm via field scouting, then apply a targeted biological control agent (e.g., Bt-based) before considering chemical pesticide | Pest model confidence of 78% is high but not certain — recommending confirmation first avoids unnecessary chemical use |
| Nutrient Monitoring | Track nitrogen levels over the next week | Tasseling stage has high nitrogen demand; current pH (6.2) supports normal nutrient uptake |
| Yield-Risk Flag | Moderate risk | Declining NDVI combined with low soil moisture and pest pressure together push this zone's risk score above the average for its historical yield baseline |

**Observation**
The role-based prompt produces a more professional and explainable response by instructing the AI to act as an agronomy advisor and to justify each recommendation using the most influential factor, mirroring AgriTwin's XAI design goal.

# Prompt 4 – Advanced Structured Prompt

**Prompt**
```
You are the Explainable AI Decision-Support Layer of AgriTwin – A Unified Multi-Crop Digital Twin for Explainable AI-Driven Crop Monitoring and Intelligent Farm Management.

Analyze the following zone's digital twin data and generate a personalized, explainable farm management recommendation.

Zone Data
Zone ID: Zone 3
Crop: Maize
Growth Stage: Tasseling
Soil Moisture: 18% (target 25-30%)
Soil pH: 6.2
NDVI: 0.52 (down from 0.61 last week)
Pest Detection Confidence: 78% Fall Armyworm
Weather Forecast: No rain expected for 5 days
Historical Yield: 4.2 tons/acre
Adjacent Zones: Zone 1 (Wheat), Zone 2 (Vegetables)

Instructions
Step 1: Understand the zone's crop, growth stage, and current digital twin readings.
Step 2: Identify which factors deviate most from optimal conditions.
Step 3: Recommend an irrigation schedule with approximate amount and timing.
Step 4: Recommend a pest/disease management action appropriate to the model's confidence level, prioritizing non-extreme, safe interventions.
Step 5: Provide nutrient/fertilizer guidance based on growth stage and soil pH.
Step 6: Provide a short-term yield-risk forecast for this zone.
Step 7: Generate an Explainability Report that ranks the factors (soil moisture, NDVI trend, pest confidence, etc.) by how much each influenced the recommendations, similar to a SHAP-style feature-importance summary.
Step 8: Translate the technical explanation into a short, farmer-friendly explanation in plain language.
Step 9: Note any considerations relevant to the adjacent crop zones (e.g., shared irrigation lines, pest spread risk).
Step 10: Clearly state that recommendations should be confirmed with an agronomist before large-scale pesticide, fertilizer, or irrigation changes.

Required Output Format
1. Zone Profile Summary
2. Irrigation Recommendation
3. Pest / Disease Management
4. Fertilizer / Nutrient Guidance
5. Yield-Risk Forecast
6. Explainability Report (Ranked Feature Importance)
7. Farmer-Friendly Explanation
8. Safety & Escalation Considerations

Keep the response practical, concise, personalized, and easy to understand.
```

## Advanced Prompt Output

### 1. Zone Profile Summary
Zone 3 is growing maize at the tasseling stage — a period of high water and nutrient demand. Current readings show low soil moisture, a declining NDVI trend, and a high-confidence pest detection, placing this zone at elevated short-term risk within the farm's multi-crop digital twin.

### 2. Irrigation Recommendation

| Parameter | Recommendation |
|---|---|
| Amount | Approximately 25–30 mm |
| Timing | Within the next 24–48 hours |
| Method | Preferably drip or furrow irrigation to avoid excess canopy wetting during pest pressure |

### 3. Pest / Disease Management

| Step | Action |
|---|---|
| Confirmation | Conduct field scouting to visually confirm Fall Armyworm presence |
| First-Line Treatment | Apply a biological control agent (e.g., Bt-based formulation) targeted at larval stages |
| Escalation | If infestation is confirmed above threshold after scouting, consider an approved chemical pesticide at label-recommended dosage only |
| Cross-Zone Note | Monitor Zone 2 (Vegetables) for early signs of spread, as Fall Armyworm can migrate across adjacent plots |

### 4. Fertilizer / Nutrient Guidance
Soil pH (6.2) is within the acceptable range for maize nutrient uptake. Given the tasseling stage's high nitrogen requirement, a moderate top-dress nitrogen application is advisable, timed after irrigation to support uptake without leaching losses.

### 5. Yield-Risk Forecast
**Moderate risk** to the current season's yield in Zone 3 relative to its historical average of 4.2 tons/acre. The combination of low soil moisture, declining NDVI, and pest pressure — if unaddressed within the next few days — could reduce yield by an estimated 8–15%. Prompt irrigation and pest confirmation should mitigate most of this risk.

### 6. Explainability Report (Ranked Feature Importance)

| Rank | Factor | Contribution to Recommendation |
|---|---|---|
| 1 | Soil Moisture (18%, target 25–30%) | Largest driver of the irrigation urgency score |
| 2 | Pest Detection Confidence (78%) | Second-largest driver, triggering the pest-management recommendation |
| 3 | NDVI Trend (0.61 → 0.52) | Supports the yield-risk flag and reinforces the irrigation urgency |
| 4 | Weather Forecast (no rain, 5 days) | Reinforces irrigation timing rather than waiting for natural rainfall |
| 5 | Soil pH (6.2) | Minor factor; only affects nutrient-uptake guidance, not urgency |

### 7. Farmer-Friendly Explanation
"Your maize in Zone 3 needs water soon — the soil is drier than it should be, and it won't rain for several days. Our cameras also picked up signs that may be a pest called Fall Armyworm, so please check the field. Watering and treating for the pest quickly should protect your harvest."

### 8. Safety & Escalation Considerations
This recommendation is a general decision-support guide generated from digital twin data. Farmers or agronomists should confirm pest presence through physical field inspection before applying any pesticide, follow all label safety instructions, and consult a certified agronomist before making large-scale changes to irrigation, fertilizer, or pest-control practices — especially if conditions differ from what the sensors report.

**Observation**
The advanced structured prompt produces the most comprehensive result because it specifies the zone's digital twin data, the AI's role, a step-by-step analysis process, an explicit **Explainability Report**, a farmer-friendly translation, and safety/escalation considerations — directly reflecting AgriTwin's explainable-AI design principle.

# Comparison of Prompt Outputs

| Feature | Simple Prompt | Context-Based | Role-Based | Advanced Structured |
|---|---|---|---|---|
| Zone/Crop Context | Basic | Detailed | Detailed | Detailed |
| Personalization | Basic | Good | Very Good | Excellent |
| Irrigation Recommendation | Yes | Yes | Yes | Yes |
| Pest Management | Yes | Yes | Yes | Yes |
| Explainability (Why?) | No | Basic | Good | Excellent (ranked factors) |
| Multi-Crop / Adjacent Zone Awareness | No | Partial | Partial | Yes |
| Yield-Risk Forecast | No | No | Partial | Yes |
| Farmer-Friendly Translation | No | No | No | Yes |
| Safety Guidance | No | No | Yes | Yes |
| Structured Output | Basic | Good | Very Good | Excellent |
| Overall Usefulness | Good | Very Good | Very Good | Excellent |

# Analysis

The experiment demonstrates that prompt quality has a significant impact on the usefulness and explainability of AI-generated crop management recommendations.

The **Simple Prompt** generated a basic irrigation and pest recommendation but provided limited personalization and no explanation of reasoning.

The **Context-Based Prompt** improved the response by providing information about the AgriTwin platform, the multi-crop farm setting, and the zone's growth stage and trend data.

The **Role-Based Prompt** produced a more professional, explainable response because the AI was instructed to behave as an agronomy advisor and justify each recommendation using the most influential factor.

The **Advanced Structured Prompt** generated the most comprehensive output. It defined the zone profile, the AI's role within the Decision-Support Layer, a step-by-step analysis process, a ranked **Explainability Report**, a farmer-friendly plain-language translation, and safety/escalation considerations.

Therefore, the advanced structured prompt is the most suitable approach for integrating an explainable AI recommendation assistant into the AgriTwin platform's Decision-Support Layer.

# Final Refined Prompt

```
You are the Explainable AI Decision-Support Layer of AgriTwin – A Unified Multi-Crop Digital Twin for Explainable AI-Driven Crop Monitoring and Intelligent Farm Management.

Analyze the zone's digital twin data and generate a personalized, explainable farm management recommendation.

Consider:
- Crop type and growth stage
- Soil moisture, pH, and NPK levels
- NDVI value and its recent trend
- Pest/disease detection confidence
- Short-term weather forecast
- Historical yield for the zone
- Conditions in adjacent crop zones on the same farm

Perform the following:
1. Summarize the zone's current profile.
2. Provide an irrigation recommendation with amount and timing.
3. Provide a pest/disease management recommendation appropriate to the model's confidence level, prioritizing safe, non-extreme interventions.
4. Provide fertilizer/nutrient guidance based on growth stage and soil condition.
5. Provide a short-term yield-risk forecast for the zone.
6. Generate a ranked Explainability Report showing which factors most influenced each recommendation.
7. Translate the technical explanation into a short, farmer-friendly summary in plain language.
8. Note any relevant considerations for adjacent crop zones (e.g., shared irrigation, pest-spread risk).
9. Identify safety and escalation considerations.

Return the response in the following structure:

Zone Profile Summary
Irrigation Recommendation
Pest / Disease Management
Fertilizer / Nutrient Guidance
Yield-Risk Forecast
Explainability Report
Farmer-Friendly Explanation
Safety & Escalation Considerations

Use practical, safe, and easy-to-follow recommendations. Do not recommend unsafe or excessive pesticide/fertilizer application. When conditions suggest a serious or uncertain risk, recommend confirmation by a qualified agronomist before acting.
```

# Result

The prompt-based AI Farm Advisory Assistant for **AgriTwin – A Unified Multi-Crop Digital Twin for Explainable AI-Driven Crop Monitoring and Intelligent Farm Management** was successfully developed and demonstrated using ChatGPT.

The experiment showed that progressively improving the prompt from a simple instruction to a structured engineering prompt resulted in better personalization, clearer and more explainable recommendations, multi-crop zone awareness, ranked feature-importance reporting, farmer-friendly translation, and improved safety considerations.

The final refined prompt provides a suitable foundation for integrating Large Language Model capabilities into AgriTwin's Explainable AI Decision-Support Layer for real-world intelligent farm management.

Thus, the experiment demonstrates how effective prompt engineering can improve the quality, structure, explainability, and practical usefulness of AI-generated crop monitoring and farm management recommendations.
