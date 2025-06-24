## The Learning Ripple Effect of Chatbots

An interactive ripple-inspired data visualization exploring how students’ use of AI tools spreads and evolves over time. The visualization draws on survey data about generative AI usage in learning contexts and uses concentric circles to represent levels of engagement and agreement. The ripple design metaphor offers an intuitive and dynamic way to explore student behaviors and evolving patterns of AI adoption in education.

***

### 1. Dataset

This dataset was collected through an online survey conducted in Bulgaria between May 14 and May 31, 2023. The survey received 131 valid responses, focusing on how students perceive and use generative AI technologies like ChatGPT in learning. 
<br>
<br>
<img src="images/form.png?raw=true"/>

### 2. Inspiraation
This study illustrates how the use of conversational chatbots creates a continuous and expanding impact on learning, much like ripples in water. 
So, we got inspirations from ripple and designed a ripple-like pattern to visualize data, showing this dynamic and transformative process. Below is our sketch. 
<br>
<br>
<img src="images/note.png?raw=true"/>

The concentric circles represent the increasing levels of agreement with students' statements, ranging from “Strongly Disagree” to “Strongly Agree.” T

### 3. Graph Symbolization

It symbolizes the spreading influence of generative AI in learning, much like ripples expanding outward when a drop hits water.
 Data Representation:
• Red Dots: Each red dot represents an individual student’s response.
• Glow Around the Dots: The size of the glowing circle around each dot represents the frequency of generative AI usage, ranging from “Never” to “Very Often.” Larger glows indicate higher usage frequency.

When the mouse hovers over a data point, a box appears at the bottom of the visualization. This box displays detailed information linked to that specific data point, such as the student’s ID, degree, major, and gender.
<br>
<br>
<img src="images/ripple-g.gif?raw=true"/>

### 4. Data Processing

Step 1: Agreement & Frequency Mapping
 
The first  involves converting survey responses from text into numerical values. This process mapping helps make the data easier to analyze. There are two types of mappings here:
<br>
- **Agreement Mapping:**
<br>
This is for questions about levels of agreement. For example:
- “Strongly Disagree”is mapped to 1
- “Disagree”is mapped to 2
- “Neutral”is mapped to 3
- “Agree”is mapped to 4
- “Strongly Agree”is mapped to 5

- **Frequency Mapping:**
<br>
This is for questions about usage frequency. For example:
- “Never”is mapped to 1
- “Rarely”is mapped to 2
- “Sometimes”is mapped to 3
- “Often”is mapped to 4
- “Very Often”is mapped to 5
<br>
Mapping simplifies data by converting text responses into numeric values, making it easier to calculate averages, visualize trends, and run statistical analysis.
<br>
```
agreement_mapping = {
    'Strongly Disagree': 1,
    'Disagree': 2,
    'Neutral': 3,
    'Agree': 4,
    'Strongly Agree': 5
}
```
```{json}
"name": "Q5.1",
            "children": [{
                    "name": "Data Point 1", "value": 4, "distance": 4.0,
                    "studentID": "0",  "degree": "Master",
                    "major": "International_Economic_Relations",
                    "gender": "Female" }, ...
```


### 5. D3.js

We primarily used D3.js for data visualization. Since there’s a lot to cover, let’s take an example of how we created five concentric circles as the framework and added nodes with their glowing effects.

First, we declared an SVG canvas and set its height and width.

Next, we used a for loop to draw five circles, adding attributes such as the circle’s center coordinates, radius, and styling.

Then, we defined the glow and nodes, setting their center coordinates and radius as well. The glow’s radius was determined using the distance attribute from the data points, specifically based on the Q4 data.

For the nodes, we implemented transition animations. Initially, the node radius was set to 0. Then, we added an animation with a specified duration and defined the final size we wanted the nodes to reach.

After setting up the basic attributes for each node and its glow, we used a forEach loop to go through the entire dataset, enabling us to visualize the data and complete the chart.

<img src="images/d3-intro-1.png?raw=true"/>

