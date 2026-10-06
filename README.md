# 🎬 IMDb Web Scraping & Movie Data Analysis

A complete **Web Scraping and Exploratory Data Analysis project** using Python to collect and analyze movie information from the **IMDb Top 250** list.

The project demonstrates how raw web data can be collected using Selenium, cleaned and transformed with Pandas, and analyzed using statistical and visualization techniques.

---

## 📌 Project Overview

This project focuses on extracting movie information from IMDb's Top 250 Movies page and performing an end-to-end data analysis.

The analysis explores:

- ⭐ IMDb ratings
- 🗳️ Number of votes
- 🎬 Movie runtime
- 📅 Release year
- 🔞 Movie certificates
- 📊 Decade-wise movie distribution
- 📈 Relationship between ratings and votes
- ⏱️ Relationship between movie runtime and ratings

The project follows a complete data workflow:

**Website Selection → Data Collection → Data Understanding → Data Cleaning → Exploratory Data Analysis → Data Visualization → Insights & Recommendations**

---

## 🎯 Objectives

The main objectives of this project are to:

1. Scrape movie information from IMDb Top 250.
2. Store the collected information in a structured dataset.
3. Clean and transform the scraped data.
4. Analyze movie ratings and audience engagement.
5. Study movie distribution across years and decades.
6. Analyze certificate patterns.
7. Explore movie runtime patterns.
8. Identify relationships between ratings, votes, and runtime.
9. Generate meaningful insights from the collected data.

---

## 🌐 Data Source

**Website:** IMDb

**Source:** IMDb Top 250 Movies

**URL:** https://www.imdb.com/chart/top/

The following movie attributes were collected:

| Column | Description |
|---|---|
| Rank | IMDb ranking of the movie |
| Movie_Name | Name of the movie |
| Year | Movie release year |
| Runtime | Original runtime information |
| Runtime_Minutes | Runtime converted into minutes |
| Certificate | Movie certification |
| Rating | IMDb rating |
| Votes | Number of IMDb votes |
| Decade | Decade derived from release year |

---

## 🛠️ Technologies & Libraries

### Programming Language
- Python

### Web Scraping
- Selenium
- BeautifulSoup
- Requests
- Regular Expressions

### Data Manipulation
- Pandas
- NumPy

### Data Visualization
- Matplotlib
- Seaborn

### Development Environment
- Jupyter Notebook

---

## 🔄 Project Workflow

### 1. Website Selection

IMDb Top 250 was selected as the data source because it provides useful movie information such as:

- Ranking
- Movie name
- Release year
- Runtime
- Certificate
- IMDb rating
- Number of votes

---

### 2. Data Collection

Selenium was used to open the IMDb Top 250 page and collect the page content.

The scraped information was extracted from the page text and organized into a Pandas DataFrame.

The raw data was saved as:

```text
imdb_raw_data.csv
```

---

### 3. Data Understanding

The dataset was examined using:

- Dataset shape
- Column names
- Data types
- First few records
- Missing-value analysis
- Duplicate-value analysis

This helped understand the structure and quality of the scraped dataset before cleaning.

---

### 4. Data Cleaning

Several preprocessing operations were performed:

- Converted Rank into numeric format.
- Converted Year into numeric format.
- Converted Rating into numeric format.
- Converted vote counts such as `3.2M` into numerical values.
- Converted movie runtime into minutes.
- Cleaned certificate values.
- Replaced empty certificates with `Unknown`.
- Created a `Decade` column.
- Checked missing values and duplicate records.

The cleaned dataset was saved as:

```text
imdb_cleaned_data.csv
```

---

# 📊 Exploratory Data Analysis

The project performs several analyses to understand patterns in the IMDb Top 250 dataset.

## ⭐ IMDb Rating Distribution

The distribution of IMDb ratings was analyzed to understand how ratings are spread across the Top 250 movies.

## 📅 Movies by Release Year

The release years were analyzed to identify how movies are distributed across different periods.

## 🔞 Certificate Distribution

Movie certificates were analyzed to identify the most common certification categories.

## 🗳️ Rating vs Number of Votes

A scatter plot was used to compare IMDb ratings with the number of votes received by movies.

This helps understand the relationship between audience engagement and movie ratings.

## 🏆 Top 10 Highest-Rated Movies

The movies were sorted according to IMDb rating to identify the highest-rated movies in the collected dataset.

**The Shawshank Redemption** was identified as the highest-rated movie with a rating of **9.3** in the collected dataset.

## 🗳️ Top 10 Most-Voted Movies

Movies were sorted according to the number of votes to identify movies with the strongest audience engagement.

## 🎞️ Average Rating by Certificate

The average IMDb rating was calculated for each certificate category.

## 📆 Movies by Decade

A `Decade` column was created from the release year to analyze the distribution of movies across different decades.

## ⭐ Average Rating by Decade

Average IMDb ratings were calculated for each decade to compare rating patterns across different periods.

## ⏱️ Movie Runtime Analysis

Movie runtime was converted into minutes and analyzed using:

- Runtime distribution
- Longest movie
- Average runtime
- Runtime vs rating relationship

A correlation analysis was also performed between runtime and IMDb rating.

---

# 🔍 Key Insights

Based on the analysis:

- ⭐ IMDb Top 250 movies generally have high ratings because the dataset represents highly rated movies.
- 🏆 **The Shawshank Redemption** has the highest IMDb rating of **9.3** in the collected dataset.
- 🗳️ Several highly ranked movies have received millions of votes, showing strong audience engagement.
- 🔞 **R** is the most common certificate in the collected dataset.
- 📅 Movies from multiple decades are represented in the IMDb Top 250.
- 🎬 The **2000s** have strong representation in the collected dataset.
- ⏱️ Movie runtimes vary considerably, from shorter films to very long movies.
- 📈 The project analyzes the relationship between movie ratings and number of votes.
- 📊 The relationship between movie runtime and rating is also examined using correlation.

---

# 💡 Recommendations

Based on the analysis, movie platforms can:

- Combine **ratings and number of votes** to understand both quality and popularity.
- Use **rating, popularity, certificate and runtime** when creating movie recommendations.
- Analyze decade-wise trends to identify periods with strong representation of highly rated movies.
- Consider runtime when recommending movies based on users' available viewing time.

---

# 📁 Project Structure

```text
IMDb_Web_Scraping_Project/
│
├── IMDb_Web_Scraping_Project.ipynb
├── imdb_raw_data.csv
├── imdb_cleaned_data.csv
├── README.md
└── .gitignore
```

> The CSV files are generated during the execution of the notebook.

---

# ▶️ How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/SamikshyaJoshi/IMDb-Web-Scraping-Project_Data_Analysis.git
```

### 2. Navigate to the project folder

```bash
cd IMDb-Web-Scraping-Project_Data_Analysis
```

### 3. Install the required libraries

```bash
pip install pandas numpy matplotlib seaborn requests beautifulsoup4 selenium jupyter
```

### 4. Open Jupyter Notebook

```bash
jupyter notebook
```

### 5. Open

```text
IMDb_Web_Scraping_Project.ipynb
```

Run the notebook cells sequentially.

---

# ⚠️ Notes

- The project uses Selenium with Chrome WebDriver.
- IMDb's website structure may change over time, which can affect scraping selectors and extraction logic.
- Scraping should be performed responsibly and in accordance with the website's terms and applicable policies.

---

# 🚀 Future Improvements

Possible improvements include:

- Add movie genres.
- Extract directors and cast information.
- Add more detailed NLP analysis of movie descriptions.
- Build an interactive dashboard using Power BI or Streamlit.
- Develop a movie recommendation system.
- Automate periodic data collection.
- Store the scraped data in a SQL database.
- Perform advanced statistical analysis.

---

# 👩‍💻 Author

**Samikshya Joshi**

B.Tech CSE | Data Analytics & Python

---

## ⭐ Project Highlights

**Web Scraping • Data Cleaning • Exploratory Data Analysis • Data Visualization • Python • Selenium • Pandas • NumPy • Matplotlib • Seaborn**