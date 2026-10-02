# 📊 YouTube Analytics Dashboard

An interactive **YouTube Analytics Dashboard** built with **Python, Pandas, Plotly, and Streamlit** to analyze channel performance and explore the performance of individual videos.

The dashboard provides both **aggregate channel-level insights** and **individual video analysis**, including views, engagement, subscribers, audience distribution, and first-30-day performance.

---

## 🚀 Features

### 📈 Aggregate Metrics

* View overall channel performance metrics
* Compare the latest **6 months** with the previous **12-month period**
* Track:

  * Views
  * Likes
  * Subscribers
  * Shares
  * Comments
  * RPM
  * Average percentage viewed
  * Average video duration
  * Engagement ratio
  * Views per subscriber gained
* Display performance changes using percentage-based metrics
* View a formatted table of video-level performance

### 🎥 Individual Video Analysis

Select any video from the dropdown to analyze its performance.

#### Audience Analysis

* Compare views by subscriber status
* Analyze audience distribution by country
* Countries are grouped into:

  * 🇺🇸 USA
  * 🇮🇳 India
  * 🌎 Other

#### 📊 First 30-Day Performance

The dashboard compares the selected video's first 30 days against overall channel performance.

It displays:

* 20th percentile performance
* Median (50th percentile) performance
* 80th percentile performance
* Selected video's cumulative views

This helps visualize how a video's early performance compares with other videos published during the analyzed period.

---

## 🛠️ Tech Stack

* **Python**
* **Pandas** – Data manipulation and analysis
* **NumPy** – Numerical computations
* **Plotly** – Interactive visualizations
* **Streamlit** – Dashboard and web application

---

## 📂 Project Structure

```text
youtube-analytics-dashboard/
│
├── app.py
│
├── Aggregated_Metrics_By_Video.csv
├── Aggregated_Metrics_By_Country_And_Subscriber_Status.csv
├── All_Comments_Final.csv
├── Video_Performance_Over_Time.csv
│
├── requirements.txt
└── README.md
```

> File names may vary depending on the dataset version being used.

---

## 📊 Dataset

The project uses YouTube Analytics data containing information about:

* Video performance
* Views and engagement
* Subscriber activity
* Audience country
* Subscriber status
* Daily video performance over time

The data is processed using Pandas before being displayed through the Streamlit dashboard.

---

## ⚙️ How It Works

### 1. Load Data

The application loads multiple CSV files containing aggregated video metrics, audience information, comments, and video performance over time.

### 2. Data Preprocessing

The data is cleaned and transformed by:

* Converting publication dates into datetime format
* Converting video duration into seconds
* Calculating engagement ratio
* Calculating views per subscriber gained
* Calculating days since publication
* Filtering data to the relevant 12-month period

### 3. Performance Analysis

For the first 30 days after publication, the dashboard calculates:

* Mean views
* Median views
* 20th percentile views
* 80th percentile views

These values are converted into cumulative views for comparison.

### 4. Interactive Dashboard

Streamlit provides two main dashboard views:

```text
Aggregate Metrics
        │
        ├── Channel-level metrics
        ├── 6-month vs 12-month comparison
        └── Video performance table

Individual Video Analysis
        │
        ├── Select a video
        ├── Subscriber/country analysis
        └── First 30-day performance comparison
```

---

## ▶️ Running the Project Locally

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
cd YOUR-REPOSITORY
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the Streamlit application

```bash
streamlit run app.py
```

The dashboard will open in your browser.

---

## 📦 Requirements

The main dependencies are:

```text
pandas
numpy
plotly
streamlit
```

You can install them using:

```bash
pip install -r requirements.txt
```

---

## 💡 Key Concepts Demonstrated

This project demonstrates practical use of:

* Data cleaning and preprocessing
* Feature engineering
* Exploratory data analysis
* Statistical analysis
* Percentile-based performance comparison
* Cumulative metrics
* Interactive data visualization
* Dashboard development
* Streamlit application development

---

## 🎯 Project Goal

The goal of this project is to transform raw YouTube Analytics data into an **interactive dashboard** that makes channel and video performance easier to explore and understand.

Rather than relying only on individual metrics, the dashboard provides comparisons between videos and historical performance to give more context to early video growth.

---

## 👩‍💻 Author

**Vaishnavi**

Built as a data analytics and Streamlit dashboard project.

---

## ⭐ Future Improvements

Potential improvements include:

* Add more interactive filters
* Add video thumbnail previews
* Add additional engagement visualizations
* Add comment sentiment analysis
* Add video category analysis
* Add automated data updates using the YouTube Analytics API
* Deploy the dashboard publicly using Streamlit Community Cloud
