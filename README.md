# n8n-automations

# 🌦️ Weather Automation Workflow using n8n

## 📌 Overview
This automation workflow is built using [n8n](https://n8n.io/), designed to fetch and log daily weather data (high & low temperatures) for selected Indian cities: **Roorkee, Dehradun, New Delhi and Mumbai**.  
It helps in maintaining a daily weather record in Airtable, which can later be used for reporting, dashboards, or sending daily alerts.

## ⚙️ How it works – step by step
1. **Form Trigger**  
   - User submits a form selecting a city from a dropdown list.
2. **Switch Node**  
   - Based on user selection, workflow chooses the correct latitude & longitude.
3. **Set Nodes**  
   - For each city, there’s a set node to add the city’s latitude and longitude dynamically.
4. **HTTP Request to Open-Meteo API**  
   - Makes an API call to fetch hourly temperature data for the selected city.
   - Example API: `https://api.open-meteo.com/v1/forecast?...`
5. **Code Node (JavaScript)**  
   - Processes the hourly temperature data.
   - Extracts today's **highest and lowest temperatures** by comparing each hour.
6. **Airtable Integration**  
   - Logs the city, date, high and low temperatures into an Airtable table.
   - Data stored can later be visualized, analyzed, or shared.

## 🛠 Technologies & APIs used
- **n8n:** Open-source workflow automation tool to visually build and connect APIs.
- **Open-Meteo API:** Provides free, real-time and forecasted weather data.
- **Airtable API:** Used to store daily weather data in a structured table format.
- **JavaScript Code Node:** For custom data transformation and temperature calculations.

## 📊 Why I built this
- To practice real-world API integration & automation.
- Learn how to process data dynamically using code nodes.
- Understand how to store and visualize data in tools like Airtable.

## 📍 Author
Built by [Mehran Mehdi](https://www.linkedin.com/in/mehran-mehdi)

⭐NOTE:- This is part of my personal automation & AI projects to learn and showcase real-world use cases with n8n.
