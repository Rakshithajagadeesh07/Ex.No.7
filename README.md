# Ex.No.7 – Develop a Prompt-Based Application Tailored to Personal Needs

## Date: 02-09-2026

## Register No.: 212223230143

# Aim

To develop a prompt-based application using ChatGPT that demonstrates how Large Language Models can be used to assist with personalized health and wellness planning, with prompts progressing from simple to advanced designs and producing increasingly useful outputs.

---

# AI Tools Required

* ChatGPT
* Python
* FastAPI
* React.js
* PostgreSQL
* Pandas
* Large Language Model (LLM)
* Web Browser
* Visual Studio Code

---

# Project Used

## CHARMCare – Health & AI-based Regimen Manager

CHARMCare is a full-stack health and AI recommendation platform designed to provide personalized diet, nutrition, and fitness recommendations based on an individual's health profile.

The system uses a React.js frontend, FastAPI backend, Python-based recommendation logic, PostgreSQL for data persistence, and Pandas for nutrient analysis and recipe ranking.

The prompt-based application developed for this experiment acts as an **AI Health & Regimen Assistant** for CHARMCare.

---

# Explanation

A prompt-based application uses carefully designed natural-language instructions to communicate with a Large Language Model and generate useful responses according to user requirements.

In CHARMCare, a prompt-based AI assistant can be used to:

* Analyze user health profiles
* Suggest personalized meal plans
* Recommend suitable workout routines
* Explain nutrition requirements
* Suggest balanced recipes
* Provide calorie and nutrient guidance
* Consider dietary preferences
* Consider activity levels and fitness goals
* Generate grocery lists
* Explain health recommendations in simple language

The experiment demonstrates how progressively improving a prompt can produce more relevant, structured and personalized AI-generated recommendations.

> **Note:** AI-generated health recommendations are intended for general wellness guidance and should not replace advice from a qualified healthcare professional.

---

# Problem Statement

Develop a prompt-based AI Health & Regimen Assistant for the CHARMCare project that accepts a user's health and lifestyle information and generates personalized diet, nutrition and fitness recommendations.

The assistant should understand the user's requirements and generate an appropriate response using a Large Language Model while considering factors such as age, BMI, activity level, dietary preferences and fitness goals.

---

# Prompt-Based Application

The application is designed as an **AI Health & Regimen Assistant**.

### Input

The user provides:

* Age
* Height
* Weight
* BMI
* Activity level
* Fitness goal
* Dietary preference
* Health or nutritional considerations
* Cuisine preference

### Processing

```text
User Health Profile
        ↓
Prompt Construction
        ↓
Large Language Model
        ↓
Health & Nutrition Analysis
        ↓
Personalized Recommendations
        ↓
Diet / Workout / Nutrition Plan
        ↓
User
```

### Output

The application generates:

* Daily calorie guidance
* Meal recommendations
* Nutritional suggestions
* Workout recommendations
* Healthy recipe suggestions
* Grocery list
* General wellness recommendations

---

# Procedure

1. Identify a practical requirement from the CHARMCare project.
2. Define the user health profile and expected recommendation.
3. Create a simple prompt for the selected task.
4. Execute the prompt using ChatGPT.
5. Observe and record the generated response.
6. Improve the prompt by adding user context.
7. Introduce a specific AI role for better recommendations.
8. Create an advanced structured prompt with detailed requirements.
9. Compare the outputs obtained from the four prompting techniques.
10. Develop a final refined prompt suitable for integration into CHARMCare.
11. Evaluate the usefulness and consistency of the final AI-generated response.

---

# Selected Engineering Scenario

The selected scenario is **personalized diet and fitness recommendation**.

A sample user profile is provided to the AI assistant:

```text
Age: 22
Height: 170 cm
Weight: 72 kg
BMI: 24.9
Activity Level: Moderately Active
Goal: Healthy Weight Management
Dietary Preference: Vegetarian
Cuisine Preference: Indian
```

The objective is to generate a personalized one-day meal and fitness recommendation while considering the user's lifestyle and dietary preference.

---

# Prompt 1 – Simple Prompt

## Prompt

> Create a healthy diet and workout plan for this user:
>
> Age: 22
> Height: 170 cm
> Weight: 72 kg
> Activity Level: Moderately Active
> Goal: Healthy Weight Management
> Diet: Vegetarian
> Cuisine: Indian

---

# Output

### Sample One-Day Plan

**Breakfast**

* Vegetable upma
* One serving of curd
* Seasonal fruit

**Lunch**

* Brown rice or chapati
* Dal
* Mixed vegetable curry
* Salad

**Evening Snack**

* Fruit
* Handful of nuts

**Dinner**

* Vegetable chapati roll
* Paneer or tofu
* Salad

### Workout

* 10 minutes warm-up
* 25 minutes brisk walking
* 15 minutes bodyweight exercises
* 5–10 minutes stretching

### Observation

The simple prompt generates a basic recommendation but provides limited personalization and does not clearly explain why each recommendation was selected.

---

# Prompt 2 – Context-Based Prompt

## Prompt

> You are assisting CHARMCare, a health and AI-based regimen management platform. Based on the following user profile, create a personalized vegetarian Indian diet and fitness plan for healthy weight management.
>
> User Profile:
>
> Age: 22
> Height: 170 cm
> Weight: 72 kg
> BMI: 24.9
> Activity Level: Moderately Active
> Goal: Healthy Weight Management
> Dietary Preference: Vegetarian
> Cuisine Preference: Indian
>
> Include breakfast, lunch, evening snack, dinner and a simple daily workout. Prefer balanced meals containing protein, carbohydrates, healthy fats, vegetables and fruits.

---

# Output

### Personalized Diet Plan

| Meal          | Recommendation                           |
| ------------- | ---------------------------------------- |
| Breakfast     | Vegetable oats/upma with curd and fruit  |
| Mid-Morning   | Seasonal fruit                           |
| Lunch         | Chapati, dal, mixed vegetables and salad |
| Evening Snack | Roasted chana and fruit                  |
| Dinner        | Paneer/tofu with chapati and vegetables  |

### Workout Plan

* 10 minutes warm-up
* 20–30 minutes brisk walking
* Squats – 3 sets
* Modified push-ups – 3 sets
* Lunges – 2 sets
* Plank – 2 sets
* Stretching

### Observation

The context-based prompt produces a more personalized response because it provides information about the CHARMCare application and the user's dietary preferences, activity level and goal.

---

# Prompt 3 – Role-Based Prompt

## Prompt

> Act as a professional nutrition and fitness planning assistant working for CHARMCare. Analyze the following user profile and prepare a practical one-day wellness plan.
>
> User Profile:
>
> Age: 22
> Height: 170 cm
> Weight: 72 kg
> BMI: 24.9
> Activity Level: Moderately Active
> Goal: Healthy Weight Management
> Dietary Preference: Vegetarian
> Cuisine Preference: Indian
>
> Your response should:
>
> 1. Recommend balanced meals.
> 2. Include vegetarian protein sources.
> 3. Include vegetables and fruits.
> 4. Consider the user's activity level.
> 5. Suggest a practical workout routine.
> 6. Explain the purpose of the major recommendations.
> 7. Avoid extreme dieting or unsafe recommendations.
>
> Present the result in a clear table.

---

# Output

### CHARMCare Personalized Wellness Plan

| Meal          | Suggested Food                             | Purpose                                                  |
| ------------- | ------------------------------------------ | -------------------------------------------------------- |
| Breakfast     | Vegetable oats/upma + curd + fruit         | Provides carbohydrates, protein and micronutrients       |
| Mid-Morning   | Apple/guava/orange                         | Provides fiber and vitamins                              |
| Lunch         | 2 chapatis + dal + vegetable curry + salad | Balanced combination of protein, carbohydrates and fiber |
| Evening Snack | Roasted chana + fruit                      | Provides protein and sustained energy                    |
| Dinner        | Paneer/tofu + vegetables + chapati         | Provides protein and a balanced dinner                   |

### Workout

**Warm-up**

* 10 minutes

**Cardio**

* 25 minutes brisk walking

**Strength**

* Squats – 3 × 10
* Lunges – 2 × 10
* Push-ups – 2 × 8
* Plank – 3 × 20 seconds

**Cool-down**

* 5–10 minutes stretching

### Observation

The role-based prompt produces a more professional response by instructing the AI to act as a nutrition and fitness planning assistant and by specifying safety and personalization requirements.

---

# Prompt 4 – Advanced Structured Prompt

## Prompt

> You are the AI Health Recommendation Engine of CHARMCare – Health & AI-based Regimen Manager.
>
> Analyze the following user profile and generate a personalized general wellness plan.
>
> ### User Profile
>
> * Age: 22
> * Height: 170 cm
> * Weight: 72 kg
> * BMI: 24.9
> * Activity Level: Moderately Active
> * Goal: Healthy Weight Management
> * Dietary Preference: Vegetarian
> * Cuisine Preference: Indian
>
> ### Instructions
>
> Step 1: Understand the user's health and lifestyle profile.
>
> Step 2: Consider the user's activity level and wellness goal.
>
> Step 3: Recommend balanced meals suitable for a vegetarian Indian diet.
>
> Step 4: Include practical protein sources, vegetables, fruits and healthy fats.
>
> Step 5: Provide breakfast, lunch, evening snack and dinner.
>
> Step 6: Suggest a realistic workout routine containing warm-up, cardio, strength training and cool-down.
>
> Step 7: Provide general calorie and nutrition guidance without presenting it as a medical diagnosis.
>
> Step 8: Provide a grocery list containing the main ingredients.
>
> Step 9: Explain the purpose of the major recommendations.
>
> Step 10: Clearly mention that recommendations should be adjusted with professional advice when medical conditions or special dietary requirements are involved.
>
> ### Required Output Format
>
> **1. User Profile Summary**
>
> **2. Daily Nutrition Plan**
>
> **3. Workout Plan**
>
> **4. Key Nutritional Recommendations**
>
> **5. Grocery List**
>
> **6. Reasoning Behind Recommendations**
>
> **7. Safety Considerations**
>
> Keep the response practical, concise, personalized and easy to understand.

---

# Advanced Prompt Output

## 1. User Profile Summary

The user is a 22-year-old moderately active vegetarian who prefers Indian cuisine and wants to maintain a healthy approach to weight management.

---

## 2. Daily Nutrition Plan

| Meal          | Recommendation                                   |
| ------------- | ------------------------------------------------ |
| Breakfast     | Vegetable oats/upma, curd and one seasonal fruit |
| Mid-Morning   | Guava/apple/orange                               |
| Lunch         | 2 chapatis, dal, mixed vegetables and salad      |
| Evening Snack | Roasted chana with fruit                         |
| Dinner        | Paneer/tofu, vegetables and chapati              |
| Hydration     | Water regularly throughout the day               |

The meals emphasize vegetables, fiber and vegetarian protein sources while avoiding excessive reliance on highly processed foods.

---

## 3. Workout Plan

### Warm-up

10 minutes of light mobility and walking.

### Cardio

20–30 minutes of brisk walking or another enjoyable moderate-intensity activity.

### Strength Training

* Squats – 3 sets
* Lunges – 2 sets
* Push-ups – 2 sets
* Plank – 3 sets

### Cool-down

5–10 minutes of stretching.

---

## 4. Key Nutritional Recommendations

* Include a protein source in major meals.
* Prefer whole grains and minimally processed foods.
* Include a variety of vegetables.
* Include seasonal fruits.
* Choose nuts and seeds in appropriate portions.
* Maintain adequate hydration.
* Avoid extreme calorie restriction.

---

## 5. Grocery List

### Grains

* Oats
* Whole-wheat flour
* Brown rice

### Protein Sources

* Dal
* Chickpeas
* Roasted chana
* Paneer
* Tofu
* Curd

### Vegetables

* Carrot
* Beans
* Spinach
* Tomato
* Cucumber
* Other seasonal vegetables

### Fruits

* Apple
* Guava
* Orange
* Other seasonal fruits

### Healthy Fats

* Almonds
* Peanuts
* Seeds

---

## 6. Reasoning Behind Recommendations

The meal plan combines carbohydrates, vegetarian protein, fiber and micronutrient-rich foods to support daily energy requirements.

The workout combines aerobic activity and strength exercises to support general fitness and healthy weight management.

The recommendations can be further personalized by CHARMCare using user-specific BMR, TDEE, nutrient scores, dietary restrictions and recipe-ranking information.

---

## 7. Safety Considerations

The generated plan is intended for general wellness guidance. Users with medical conditions, allergies, nutritional deficiencies, pregnancy-related requirements or other specialized health needs should consult an appropriate healthcare professional before making significant dietary or exercise changes.

### Observation

The advanced structured prompt produces the most comprehensive result because it specifies the user's profile, AI role, analysis process, expected sections, personalization requirements and safety considerations.

---

# Comparison of Prompt Outputs

| Feature                | Simple Prompt | Context-Based | Role-Based | Advanced Structured |
| ---------------------- | ------------- | ------------- | ---------- | ------------------- |
| User Profile           | Basic         | Detailed      | Detailed   | Detailed            |
| Personalization        | Basic         | Good          | Very Good  | Excellent           |
| Diet Recommendation    | Yes           | Yes           | Yes        | Yes                 |
| Workout Recommendation | Yes           | Yes           | Yes        | Yes                 |
| Dietary Preference     | Yes           | Yes           | Yes        | Yes                 |
| Explanation            | Basic         | Good          | Detailed   | Detailed            |
| Grocery List           | No            | No            | No         | Yes                 |
| Safety Guidance        | No            | No            | Yes        | Yes                 |
| Structured Output      | Basic         | Good          | Very Good  | Excellent           |
| Reasoning              | Limited       | Moderate      | Detailed   | Detailed            |
| Overall Usefulness     | Good          | Very Good     | Very Good  | Excellent           |

---

# Analysis

The experiment demonstrates that prompt quality has a significant impact on the usefulness of AI-generated health and wellness recommendations.

The **Simple Prompt** generated a basic meal and workout plan but provided limited personalization.

The **Context-Based Prompt** improved the response by providing additional information about CHARMCare and the user's lifestyle, dietary preference and wellness goal.

The **Role-Based Prompt** produced a more professional response because the AI was instructed to behave as a health and fitness planning assistant and follow specific recommendation guidelines.

The **Advanced Structured Prompt** generated the most comprehensive output. It defined the user profile, AI role, analysis steps, required output format, grocery list, reasoning and safety considerations.

Therefore, the advanced structured prompt is the most suitable approach for integrating an AI recommendation assistant into the CHARMCare platform.

---

# Final Refined Prompt

> You are the AI Health Recommendation Engine of CHARMCare – Health & AI-based Regimen Manager.
>
> Analyze the user's health and lifestyle information and generate a personalized general wellness plan.
>
> Consider:
>
> * Age
> * Height
> * Weight
> * BMI
> * Activity level
> * Fitness or wellness goal
> * Dietary preferences
> * Cuisine preferences
> * Relevant health or nutritional considerations
>
> Perform the following:
>
> 1. Summarize the user's profile.
> 2. Provide a personalized daily meal plan.
> 3. Include appropriate vegetarian/non-vegetarian protein sources based on the user's preference.
> 4. Consider balanced carbohydrates, protein, healthy fats, fiber and micronutrient-rich foods.
> 5. Provide practical breakfast, lunch, snacks and dinner suggestions.
> 6. Suggest a suitable workout routine based on the user's activity level and goal.
> 7. Provide general calorie and nutrition guidance where appropriate.
> 8. Generate a practical grocery list.
> 9. Explain the reasoning behind the major recommendations.
> 10. Identify important safety considerations.
>
> Return the response in the following structure:
>
> **User Profile Summary**
> **Personalized Diet Plan**
> **Workout Plan**
> **Nutritional Recommendations**
> **Grocery List**
> **Reasoning**
> **Safety Considerations**
>
> Use practical, culturally appropriate and easy-to-follow recommendations.
>
> Do not provide medical diagnoses or unsafe/extreme diet recommendations. When the user has a medical condition or specialized dietary requirement, recommend consultation with a qualified healthcare professional.

---

# Result

The prompt-based AI Health & Regimen Assistant for the **CHARMCare – Health & AI-based Regimen Manager** was successfully developed and demonstrated using ChatGPT.

The experiment showed that progressively improving the prompt from a simple instruction to a structured engineering prompt resulted in better personalization, clearer nutrition recommendations, more relevant workout suggestions, grocery-list generation and improved safety considerations.

The final refined prompt provides a suitable foundation for integrating Large Language Model capabilities into CHARMCare's personalized health recommendation workflow.

Thus, the experiment demonstrates how effective prompt engineering can improve the quality, structure and practical usefulness of AI-generated health and wellness recommendations.
