# Investigating Netflix Movies and Guest Stars in The Office

<p >
    <a href="https://www.python.org/doc/" alt="Python 3.7">
        <img src="https://img.shields.io/badge/Python-v3.7+-brightgreen.svg" />
    </a>
    <img src="https://img.shields.io/badge/Data Manipulation-Pandas-orange" >
    <img src="https://img.shields.io/badge/Llibrary-Matplotlib-ff69b4" >
</p>  

## What's this?
Apply the foundational Python skills you learned in Introduction to Python and Intermediate Python by manipulating and visualizing movie and TV data.

![cool image](./screencover.jpg)

## Data Visualisation
Many of the films under 60 minutes appear to fit under genres such as "Children", "Stand-Up", and "Documentaries". This is a natural outcome, given that these sorts of films are likely to be shorter than a 90-minute Hollywood blockbuster.

<p align="center">
  <img src="https://github.com/tantikornpoon/Investigating-Netflix-Movies-and-Guest-Stars-in-The-Office/blob/main/screenshot_01.png"/>
</p>

We may remove these rows from our DataFrame and re-plot the values. However, another intriguing technique to investigate the impact of various genres on our data would be to plot them but coloring them differently.

```python
# Define an empty list
colors = []

# Iterate over rows of netflix_movies_col_subset
for gen in data.genre :
    if   gen == "Children":
        colors.append("lightcoral")
    elif gen == "Documentaries" :
        colors.append("skyblue")
    elif gen == "Stand-Up" :
        colors.append("teal")
    else:
        colors.append("black")
        
# Inspect the first 10 values in your list        
colors[:10]
```

As expected, non-traditional genres such as children's movies and documentaries are concentrated in the bottom half of the plot.

<p align="center">
  <img src="https://github.com/tantikornpoon/Investigating-Netflix-Movies-and-Guest-Stars-in-The-Office/blob/main/screenshot_02.png"/>
</p>
