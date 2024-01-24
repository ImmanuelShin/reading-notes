# Class 14

## Data Visualization

Matplotlib, Seaborn, and Bokeh are three popular Python libraries used for data visualization, each with its unique features and use cases.

### Matplotlib

**Features:**
- **Versatility:** Matplotlib is the most established Python plotting library and is considered a building block for many other visualization libraries. It offers great flexibility and allows for the customization of almost every element of a plot.
- **Output Formats:** It supports many output formats like PNG, PDF, SVG, and EPS.
- **Integration:** Easily integrates with Pandas and NumPy, which are commonly used in data science.

**Use Cases:**
- Ideal for creating static, interactive, and animated visualizations.
- Often used in scientific computing and publication-quality plots.

**Example Visualization:**
- A line chart showing the change in a stock's price over time. This is a straightforward plot but can be customized extensively with Matplotlib.

### Seaborn

**Features:**
- **Statistical Plotting:** Seaborn is built on top of Matplotlib and is particularly good at making complex statistical plots more accessible.
- **Attractive Default Styles:** It provides more attractive and informative statistical plots as compared to Matplotlib.
- **Integration:** Works well with Pandas data structures.

**Use Cases:**
- Best used for making statistical graphics in Python. It simplifies the process of creating complex visualizations like heat maps or violin plots.
- Often used in exploratory data analysis.

**Example Visualization:**
- A heatmap showing correlation between different variables. Seaborn makes it easy to create informative and attractive heatmaps.

### Bokeh

**Features:**
- **Interactive Plots:** Bokeh is designed to generate interactive plots that can be manipulated in the browser.
- **High-Performance:** Handles streaming and real-time data smoothly, making it suitable for large or streaming datasets.
- **Output Formats:** Generates HTML files or interactive web applications.

**Use Cases:**
- Ideal for creating interactive visualizations and dashboards for the web.
- Often used in web-based data applications.

**Example Visualization:**
- An interactive dashboard showing real-time data, like stock market trends. Users can zoom in/out, pan, or select specific data points.

## Seaborn

### Relational Plots

**Main Function:** `relplot()`

**Purpose:** Relational plots are used for visualizing the relationship between two quantitative variables. They can reveal trends and patterns in the data.

- **Example Use Case:** Plotting the relationship between `time` and `distance` for a moving object can help understand its speed patterns over time.

### Categorical Plots

**Main Functions:** `catplot()`, `barplot()`, `boxplot()`, `violinplot()`, `stripplot()`, `swarmplot()`

**Purpose:** Categorical plots are used to show the distribution of a variable or the relationships between multiple variables, often involving categorical data.

- **Example Use Case:** Using a `barplot()` to display the average daily temperature per month. This helps in comparing temperatures across months.

### Distribution Plots

**Main Functions:** `distplot()`, `kdeplot()`, `histplot()`

**Purpose:** Distribution plots are used for visualizing the distribution of a dataset. These plots can show the underlying frequency distribution (like histograms) or a smooth estimate of the distribution (like kernel density estimation).

- **Example Use Case:** Using `histplot()` to visualize the distribution of cholesterol levels in a group of people, helping in identifying common health trends.

Checkout the [Seaborn cheat sheet](https://s3.amazonaws.com/assets.datacamp.com/blog_assets/Python_Seaborn_Cheat_Sheet.pdf) for more context. The **Plotting with Seaborn** section is particularly helpful for simply remembering what tools are available for use.

## Things I want to know more about
