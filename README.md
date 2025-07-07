
# 🎬 Netflix Titles Data Analysis Dashboard

This is an advanced, interactive dashboard built with **Streamlit** and **Docker** to explore the Netflix titles dataset. It includes powerful visualizations, real-time filters, and sentiment analysis using **TextBlob**.

---

## 📊 Dataset

We use the [`netflix_titles.csv`](https://www.kaggle.com/datasets/shivamb/netflix-shows) dataset, which includes the following fields:

- **Title**
- **Type** (Movie / TV Show)
- **Director / Cast**
- **Country**
- **Release Year**
- **Rating**
- **Duration**
- **Listed In**
- **Description**

> Ensure `netflix_titles.csv` is placed in the same directory as `app.py`.

---

## 🚀 Features

| Feature                      | Description                                                                 |
|-----------------------------|-----------------------------------------------------------------------------|
| 🎚️ Sidebar Filters           | Filter content by `Type` and `Country`                                      |
| 📊 Ratings Pie Chart         | See distribution of content ratings (TV-MA, PG, etc.)                      |
| 📅 Release Year Histogram    | View trends in content production over the years                           |
| 🧠 Sentiment Analysis        | Analyze the polarity of Netflix descriptions using NLP                     |
| 📈 Sentiment Distribution    | Histogram from -1 (very negative) to +1 (very positive)                    |
| 🧾 Interactive Data Table    | Explore the top 20 filtered entries dynamically                             |

---

## 🧪 How to Run (Locally Without Docker)

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/netflix-dashboard
cd netflix-dashboard
```

### 2. Add Dataset

Download `netflix_titles.csv` from Kaggle and place it in the root folder.

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the App

```bash
streamlit run app.py
```

Then open [http://localhost:8501](http://localhost:8501) in your browser.

---

## 🐳 Run With Docker

### 1. Build the Docker Image

```bash
docker build -t netflix-app .
```

### 2. Run the Docker Container

```bash
docker run -p 8501:8501 netflix-app
```

### 3. Open in Browser

Visit: [http://localhost:8501](http://localhost:8501)

---

## 📂 Project Structure

```
netflix-dashboard/
├── app.py                 # Streamlit app logic
├── Dockerfile             # Docker configuration
├── requirements.txt       # Required Python libraries
├── netflix_titles.csv     # Dataset (user must supply)
└── README.md              # Project documentation
```

---

## 📦 Requirements

- Python 3.8+
- Streamlit
- pandas
- plotly
- textblob

Install all dependencies with:

```bash
pip install -r requirements.txt
```

---

## 🧠 NLP Notes

We use [TextBlob](https://textblob.readthedocs.io/en/dev/) to analyze sentiment polarity of descriptions:

- `+1` → very positive
- ` 0` → neutral
- `-1` → very negative

---

## 📝 License

This project is licensed under the MIT License — feel free to use and adapt it for your own learning or portfolio.
