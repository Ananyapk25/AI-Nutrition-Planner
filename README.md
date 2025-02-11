# AI Meal Planner App

This project is a meal planning app that generates personalized meal plans based on a user's caloric needs and food
preferences.
It uses Meta-Llama-3-70B to generate creative meal ideas using ingredients selected by the algorithm.


## Demo

![image](https://imgur.com/5CqseP5.png)
![image](https://imgur.com/Ma6aJ8f.png)
![image](https://imgur.com/8MFw6lB.png)

## Features

- Calculation of daily calorie needs based on user inputs like age, height, weight, and gender
- Selection of user food preferences and allergies/restrictions
- Generation of meal plans for breakfast, lunch, and dinner within the target calorie ranges with food items from
  different categories
- Creative naming and description of meals using Meta-Llama-3-70B

## Technology

- Python
- Streamlit for app UI
- Pandas for data manipulation
- `Meta-Llama-3-70B` for AI text generation

Add your API key to `.streamlit/secrets.toml`:

```bash
openai_apikey="YOUR_API_KEY"
```

## Random greedy algorithm

- Calculating the target calories for breakfast, lunch, and dinner based on the user's BMR.
- Randomly selecting a food group (e.g., fruits, proteins, etc.)
- Randomly selecting a food item from that group.
- Checking if adding that item would exceed the calorie target.
- If not, add the item to the selected ingredients list.
- Repeating steps 2 – 5 until the calories are within 10 of the target or all items are selected.

### The goal is to select a set of food items that maximize calories, while not exceeding the target calories. This is similar to the knapsack problem.

---

The app calculates the user's basal metabolic rate to determine their daily calorie needs. It then randomly selects
ingredients from categorized food items to meet the calorie targets for each meal. The selected ingredients are passed
to the Meta-Llama-3-70B to generate creative names and descriptions for the meals.

The project demonstrates an application of AI for personalized meal planning.
It could be extended by adding user accounts, more food options, recipe instructions, etc.