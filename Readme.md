# 📊 COVID-19 Metadata Analysis Dashboard 🦠

Welcome to the **CORD-19 Metadata Analysis Dashboard**! This Streamlit app lets you explore the COVID-19 Open Research Dataset metadata interactively. Dive into publication trends, top journals, and visualize key insights from the research papers. 📚🔍

---

## 🚀 Features

- **Data Loading & Cleaning** 🧹  
  Efficiently loads the `metadata.csv` file, drops columns with excessive missing data, fills missing key fields, and extracts important features like publication year and abstract word count.

- **Interactive Filters** 🎛️  
  Filter data dynamically by publication year range and select specific journals to narrow your investigation.

- **Visual Insights** 📈  
  - Publications Over Time: Line chart showing yearly publication counts.  
  - Top Journals: Bar chart highlighting most prolific publishers.  
  - Word Cloud: Highlights trending words in paper titles.  
  - Source Distribution: Bar chart showing paper counts by source.

- **Data Preview** 👀  
  Display a scrollable table featuring a sample of the filtered research metadata.

---

## 🛠️ How It Works

1. **Load and Clean Data**  
   Uses Pandas to load the CSV dataset, drops columns with over 50% missing values, fills important missing fields, converts publication dates to years, and counts abstract words.

2. **Filter Data**  
   The sidebar lets users select the publication year range and pick a journal from the dataset to filter the results.

3. **Display & Visualize**  
   Shows a sample of the filtered data and updates visualizations accordingly in real-time.

4. **Efficient Caching** ⏱️  
   Data loading is cached for 1 hour to speed up performance and reduce repetitive computation.

---

## 📋 Requirements

- Python 3.7+  
- Streamlit  
- Pandas  
- Matplotlib  
- Seaborn  
- WordCloud  

Install dependencies via:

```
pip install streamlit pandas matplotlib seaborn wordcloud

```


---

## 🏃 Running the App

1. Place your `metadata.csv` file in the same directory as this app script.  
2. Run the app with:

```
streamlit run your_script_name.py
```


3. Open the provided URL in your browser and explore! 🌐

---

## 🧐 Code Highlights

- **`@st.cache_data` decorator** to cache data loading and cleaning.  
- Robust data preprocessing including dropping mostly empty columns and imputing missing values.  
- Multiple visualizations built with Matplotlib and Seaborn.  
- Intuitive Streamlit widgets for dynamic filtering.

---

## ⚠️ Notes

- The CSV file should include columns like `title`, `publish_time`, `journal`, `abstract`, and optionally `source_x`.  
- The app gracefully handles missing columns by notifying the user.  
- Performance may vary based on dataset size; caching helps improve responsiveness.

---

## ❤️ Contributions & Feedback

Feel free to open issues or submit pull requests. Your feedback helps make this dashboard better!

---

Thank you for exploring the CORD-19 research metadata with this dashboard! 🙌📊🧪
