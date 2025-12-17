# TMDB Movie Data Analysis using Spark and APIs

A comprehensive data engineering project demonstrating movie analytics using Apache Spark and The Movie Database (TMDB) API. This project showcases modern data processing techniques, API integration, and distributed computing for extracting insights from entertainment industry data.

## 🎯 Project Overview

This project implements a complete ETL pipeline that:
- Fetches movie data from TMDB's REST API
- Processes data using PySpark for scalable analytics
- Performs comprehensive data cleaning and transformation
- Calculates key performance indicators (KPIs)
- Generates insights on movie performance, franchises, and directors

## 🛠️ Technologies Used

- **Apache Spark (PySpark 4.0.1)** - Distributed data processing and analytics
- **TMDB API** - Movie data source with comprehensive film information
- **Python 3.x** - Primary programming language
- **Jupyter Notebooks** - Interactive development and documentation
- **Pandas 2.3.3** - Data manipulation and analysis
- **NumPy 2.2.6** - Numerical computing
- **Matplotlib 3.10.7** - Data visualization
- **Requests 2.32.5** - HTTP API client with robust error handling
- **python-dotenv 1.2.1** - Environment variable management

## 📊 Features

### Data Extraction
- Secure TMDB API integration with environment-based credentials
- Robust error handling for network timeouts and HTTP errors
- Rate limiting compliance
- Progress tracking and failure reporting
- Fetches 18+ blockbuster movies including Avengers, Avatar, Star Wars, etc.

### Data Processing
- Comprehensive data cleaning pipeline
- JSON field extraction and normalization
- Missing value handling and data type conversion
- Duplicate removal and data validation
- Filtering for released movies with sufficient data quality

### Analytics & KPIs
- **Financial Metrics**: Revenue, budget, profit, ROI analysis
- **Performance Rankings**: Best/worst performing movies by multiple criteria
- **Franchise Analysis**: Comparison of franchise vs. standalone movies
- **Director Success**: Top directors by revenue and ratings
- **Advanced Filtering**: Genre-based and cast-specific movie searches
- **Trend Analysis**: Yearly box office performance

### Data Collected
- Movie metadata (title, release date, runtime, budget, revenue)
- Cast and crew information (top actors, directors, team sizes)
- Ratings and popularity metrics (vote average, vote count, popularity score)
- Genre classifications and production details
- Collection/franchise associations
- Production companies and countries

## 🚀 Getting Started

### Prerequisites

- Python 3.8 or higher
- Java 8 or higher (required for PySpark)
- TMDB API key ([Get one here](https://www.themoviedb.org/settings/api))

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd module5.1
   ```

2. **Create virtual environment** (recommended)
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables**
   
   Create a `.env` file in the project root:
   ```env
   TMDB_API_KEY=your_api_key_here
   ```

### Running the Project

1. **Launch Jupyter Notebook**
   ```bash
   jupyter notebook
   ```

2. **Open `module5.1.ipynb`**

3. **Run cells sequentially** to execute the complete pipeline

## 📁 Project Structure

```
module5.1/
├── module5.1.ipynb          # Main analysis notebook
├── requirements.txt         # Python dependencies
├── instructions.md          # Project requirements and specifications
├── .env                     # Environment variables (not in repo)
├── .gitignore              # Git ignore rules
└── README.md               # This file
```

## 📈 Analysis Pipeline

### Step 1: API Setup and Data Extraction
- Initialize Spark session with adaptive query execution
- Configure TMDB API connection
- Fetch movie details and credits for 18 blockbuster films
- Handle errors and track failed requests

### Step 2: Data Cleaning and Preprocessing
- Drop irrelevant columns (adult, imdb_id, video, homepage, etc.)
- Extract and normalize JSON fields (genres, production companies, etc.)
- Convert data types (budget/revenue to millions USD, dates to datetime)
- Handle missing values and unrealistic data (zero budgets/revenues)
- Filter for quality (minimum 10 non-null columns, released status)
- Reorder columns for logical structure

### Step 3: KPI Implementation & Analysis
- **Performance Rankings**: Highest/lowest revenue, profit, ROI, ratings
- **Advanced Filtering**: Genre + cast/director specific searches
- **Franchise Analysis**: Compare franchise vs. standalone performance
- **Success Metrics**: Top franchises and directors by multiple criteria

### Step 4: Data Visualization
- Revenue vs. Budget trends
- ROI distribution by genre
- Popularity vs. Rating correlations
- Yearly box office performance
- Franchise vs. Standalone comparisons

## 🎬 Sample Movies Analyzed

- Avengers: Endgame
- Avatar
- Star Wars: The Force Awakens
- Avengers: Infinity War
- Titanic
- Jurassic World
- The Lion King
- Black Panther
- Frozen series
- And more...

## 🔒 Security Best Practices

- API keys stored in environment variables (`.env` file)
- `.env` file excluded from version control via `.gitignore`
- No hardcoded credentials in source code
- Secure credential management following industry standards

## 📊 Key Insights

The project enables analysis of:
- Which movies generate the highest ROI
- How franchises perform compared to standalone films
- Director success patterns across multiple metrics
- Genre-specific performance trends
- Budget vs. revenue relationships
- Rating vs. popularity correlations

## 🤝 Contributing

This is an individual data engineering upskilling project. However, suggestions and improvements are welcome through issues and pull requests.

## 📝 License

This project is for educational purposes as part of a data engineering upskilling program.

## 🙏 Acknowledgments

- **TMDB** for providing comprehensive movie data API
- **Apache Spark** community for distributed computing framework
- Data Engineering Upskilling Program for project specifications

## 📧 Contact

For questions or feedback about this project, please open an issue in the repository.

---

**Note**: This project demonstrates real-world data engineering practices including ETL pipelines, API integration, distributed computing, and data analytics. Perfect for portfolios, learning Spark, or as a foundation for recommendation systems.
