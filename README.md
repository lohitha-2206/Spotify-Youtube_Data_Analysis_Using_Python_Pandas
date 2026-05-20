# 🎵 Spotify & YouTube Big Data Analysis using Python Pandas

## 📌 Project Introduction

This project is based on performing Big Data Analysis on a Spotify & YouTube Dataset using Python and the Pandas library inside Jupyter Notebook. The dataset contains information related to artists, tracks, streams, views, likes, comments, album types, danceability, and YouTube channels.

The main objective of this project is to understand how Python and Pandas are used in real-world music and streaming data analysis for cleaning, filtering, grouping, statistical analysis, correlation analysis, and extracting meaningful insights from large datasets efficiently.

In this project, different data analysis techniques were implemented such as:

- Data Cleaning
- Removing Duplicate Records
- Spotify Stream Analysis
- YouTube Views Analysis
- Album Type Analysis
- Correlation Analysis
- Statistical Analysis
- Exploratory Data Analysis (EDA)
- Data Visualization

This project provides practical exposure to working with large entertainment datasets and understanding how data analysts use Python for extracting insights from streaming platforms like Spotify and YouTube.

---

# 📂 Dataset Information

The dataset contains information related to songs, artists, YouTube statistics, and Spotify streaming performance.

### Dataset Features:

- Artist
- Track
- Album
- Album Type
- Stream
- Views
- Likes
- Comments
- Danceability
- Energy
- Official Video
- YouTube Channel

Each record in the dataset represents a music track with its Spotify and YouTube performance metrics.

---

# 🛠️ Tools & Technologies Used

## 🐍 Python
Python was used as the programming language for performing data analysis and dataframe operations.

## 📊 Pandas
Pandas library was used for:
- Data Cleaning
- Data Manipulation
- Statistical Analysis
- Correlation Analysis
- GroupBy Operations
- Filtering Data

## 📈 Matplotlib
Used for:
- Bar Graphs
- Correlation Heatmaps
- Track & Artist Visualization
- Stream & Views Analysis

## 📓 Jupyter Notebook
Jupyter Notebook was used to execute Python code interactively and visualize outputs step-by-step.

---

# 🔍 Pandas Functions Implemented

## 🔹 info()
Displays complete dataset information.

### Syntax:
```python
data.info()
```

---

## 🔹 drop()
Removes unnecessary columns from dataframe.

### Syntax:
```python
data.drop('Column_Name', axis=1)
```

---

## 🔹 duplicated()
Checks duplicate records.

### Syntax:
```python
data.duplicated()
```

---

## 🔹 drop_duplicates()
Removes duplicate records.

### Syntax:
```python
data.drop_duplicates(inplace=True)
```

---

## 🔹 isnull()
Checks missing values.

### Syntax:
```python
data.isnull().sum()
```

---

## 🔹 fillna()
Fills missing values.

### Syntax:
```python
data.fillna(0)
```

---

## 🔹 groupby()
Groups data based on specific columns.

### Syntax:
```python
data.groupby('Artist')['Views'].sum()
```

---

## 🔹 sort_values()
Sorts values in ascending or descending order.

### Syntax:
```python
data.sort_values(by='Views', ascending=False)
```

---

## 🔹 head()
Displays top records.

### Syntax:
```python
data.head(10)
```

---

## 🔹 value_counts()
Displays unique values with their counts.

### Syntax:
```python
data['Album_type'].value_counts()
```

---

## 🔹 corr()
Calculates correlation between numerical columns.

### Syntax:
```python
data[['Views','Likes','Comments','Stream']].corr()
```

---

## 🔹 plot()
Creates visualizations.

### Syntax:
```python
data.groupby('Artist')['Views'].sum().plot(kind='bar')
```

---

# 📊 Tasks Performed in the Project

## ✅ Q1) Top 10 Artists with Highest YouTube Views

### Task:
Find the top 10 artists having the highest total YouTube views.

### Code Used:
```python
data.groupby('Artist')['Views'].sum().sort_values(ascending=False).head(10)
```

### Explanation:
- Groups data artist-wise
- Calculates total views
- Displays top 10 artists

---

# 📊 Q2) Top 10 Tracks with Highest Spotify Streams

### Task:
Find the top 10 tracks having the highest Spotify streams.

### Code Used:
```python
data.groupby('Track')['Stream'].sum().sort_values(ascending=False).head(10)
```

### Explanation:
- Groups tracks by stream count
- Sorts stream values
- Displays top streamed tracks

---

# 📊 Q3) Most Common Album Types on Spotify

### Task:
Find the most common album types and count their tracks.

### Code Used:
```python
data['Album_type'].value_counts()
```

### Explanation:
- Counts album types
- Displays frequency of each album type

---

# 📊 Q4) Average Views, Likes & Comments by Album Type

### Task:
Compare average views, likes, and comments between album types.

### Code Used:
```python
data.groupby('Album_type')[['Views','Likes','Comments']].mean()
```

### Explanation:
- Groups data by album type
- Calculates average engagement metrics

---

# 📊 Q5) Top 5 YouTube Channels Based on Views

### Task:
Find top YouTube channels with highest views.

### Code Used:
```python
data.groupby('Channel')['Views'].sum().sort_values(ascending=False).head(5)
```

### Explanation:
- Groups data channel-wise
- Calculates total views
- Displays top 5 channels

---

# 📊 Q6) Most Viewed Track on YouTube

### Task:
Find the track with maximum YouTube views.

### Code Used:
```python
data.groupby('Track')['Views'].sum().sort_values(ascending=False).head(1)
```

### Explanation:
- Calculates track-wise views
- Displays highest viewed track

---

# 📊 Q7) Top 7 Tracks with Highest Like-to-View Ratio

### Task:
Find tracks with highest audience engagement ratio.

### Code Used:
```python
data['LV_Ratio'] = data['Likes'] / data['Views']

data.groupby('Track')['LV_Ratio'].mean().sort_values(ascending=False).head(7)
```

### Explanation:
- Creates Like-to-View ratio column
- Finds tracks with highest engagement

---

# 📊 Q8) Albums with Maximum Danceability

### Task:
Find albums containing highly danceable tracks.

### Code Used:
```python
data.groupby('Album')['Danceability'].max().sort_values(ascending=False)
```

### Explanation:
- Groups tracks album-wise
- Finds maximum danceability score

---

# 📊 Q9) Correlation between Views, Likes, Comments & Streams

### Task:
Analyze correlation between engagement metrics.

### Code Used:
```python
data[['Views','Likes','Comments','Stream']].corr()
```

### Explanation:
- Calculates correlation matrix
- Helps identify relationships between metrics

---

# 📌 Important Insights

✔️ Python and Pandas make large-scale music data analysis efficient.

✔️ GroupBy operations help analyze artist and track performance.

✔️ Correlation analysis helps understand relationships between streams and engagement.

✔️ YouTube Views and Likes are highly related.

✔️ Album type analysis helps understand audience preferences.

✔️ Real-world Spotify and YouTube datasets can be analyzed effectively using Python.

---

# 📁 Project Structure

```text
├── Spotify_YouTube_Analysis.ipynb
├── README.md
```

---

# 🎯 Final Conclusion

This project demonstrates how Python and Pandas can be used for real-world music and streaming platform data analysis tasks. Different operations such as data cleaning, removing duplicate records, grouping data, correlation analysis, statistical analysis, visualization, and extracting meaningful insights were successfully implemented.

Through this project, practical understanding was gained in:

- Data Cleaning
- Exploratory Data Analysis (EDA)
- Data Manipulation using Pandas
- Correlation Analysis
- Statistical Analysis
- GroupBy Operations
- Spotify Stream Analysis
- YouTube Engagement Analysis
- Data Visualization

Overall, this project serves as a strong beginner-friendly foundation for learning Data Analysis and Data Science using Python.
