## The Learning Ripple Effect of Chatbots

For this project, we designed and built an interactive data visualization to explore how students’ use of AI tools like ChatGPT spreads and evolves over time, drawing inspiration from the ripple effect.

The visualization is built with **React**, **D3.js**, **Python3**, and **SQLite**, combining full-stack data processing with an interactive frontend. The ripple pattern visually represents how students’ engagement with AI grows and changes across different learning contexts.

***

### Behind the Scenes

#### 1. Dataset
Survey data from 131 students on their use of generative AI in learning.
<br>
<br>
<img src="images/form.png?raw=true"/>

#### 2. ETL Pipeline
Raw text data was processed into hierarchical JSON with Python & SQLite, mapping agreement and frequency levels numerically.
<br>
**Step 1:** <br>
Mapping responses — Survey answers were converted from text to numeric values for visualization and analysis.
<br>
- Agreement Mapping: “Strongly Disagree” → 1, ..., “Strongly Agree” → 5
- Frequency Mapping: “Never” → 1, ..., “Very Often” → 5
<br>
**Step 2:** <br>
  Data Structuring — Mapped data was stored in a hierarchical JSON format, including values such as agreement level, usage frequency, student ID, degree, major, and gender.
<br>
<br>
```
"name": "Q5.1",
          "children": [{
                  "name": "Data Point 1", "value": 4, "distance": 4.0,
                  "studentID": "0",  "degree": "Master",
                  "major": "International_Economic_Relations",
                  "gender": "Female" }, ...
```

#### 3. Visualization
D3.js was used to draw the concentric circles, animate nodes, and handle interactions.
<br>
<br>
<img src="images/d3-intro-1.png?raw=true"/>

***

### How It Works

- Ripple Design: Concentric circles represent levels of agreement (from “Strongly Disagree” to “Strongly Agree”)
- Red Dots: Each dot = a student response
- Glow Effects: The glow size = how frequently the student uses AI tools (“Never” → “Very Often”)
- Interactions: Hovering reveals student details (degree, major, gender), and creates a ripple animation
<br>
<br>
<img src="images/note.png?raw=true"/>

***

### Wrap-up
This project brings together data engineering, interaction design, and visualization to tell a story of how generative AI is reshaping student learning behaviors.
<br>
<br>
<img src="images/ripple-g.gif?raw=true"/>

