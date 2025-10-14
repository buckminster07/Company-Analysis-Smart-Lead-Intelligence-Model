# 🚀 AI-Powered Lead Generation & Company Analysis System

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://python.org)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org)

This project is a data-driven lead generation engine designed to analyze and rank companies for B2B sales or investment purposes. It moves beyond traditional, lagging financial indicators by integrating a rich set of alternative data sources to build a forward-looking, holistic company profile.A key innovation of this tool is its multi-faceted scoring system, which synthesizes these diverse metrics into three key strategic factors:

Stability Factor: Uses Principal Component Analysis (PCA) on core financial data to create an objective, data-driven measure of a company's market strength and scale.

Growth Factor: Combines a technographics score (derived from a Zero-Shot NLP model) with brand momentum data (from Google Trends) to signal a company's innovation and future trajectory.

Perception Factor: Utilizes sentiment analysis on real-time news articles to provide a gauge of public opinion and brand health.

These factors are then combined to generate a final "Overall Score," allowing users to perform targeted, industry-specific analysis. The result is a clear and objective list of prioritized leads, empowering teams to focus their efforts on the most promising opportunities.

## 📊 Dataset

This project uses the **Forbes 2000** companies dataset, which includes comprehensive financial and operational data for the world's largest public companies. The dataset contains:

- **Financial Metrics**: Revenue, profits, assets, market value, and employee count
- **Company Information**: Organization names, industries, and countries
- **Industry Classifications**: Standardized industry categories for analysis

## 🌟 Features

### 📊 Multi-Dimensional Company Analysis
- **Financial Metrics Analysis**: Revenue, profits, assets, market value, and employee count analysis
- **Technology Stack Assessment**: AI-powered technographic analysis using zero-shot classification
- **News Sentiment Analysis**: Real-time sentiment analysis of company news and media coverage
- **Brand Interest Tracking**: Google Trends analysis for brand awareness and market interest
- **PCA Scoring**: Principal Component Analysis for comprehensive company ranking

### 🔍 Advanced Analytics
- **TOPSIS Multi-Criteria Decision Making**: Industry-specific ranking and investment recommendations
- **Industry-Specific Analysis**: Tailored analysis for Banking, Healthcare, IT, Retail, and more
- **Competitive Intelligence**: Peer group analysis and market positioning
- **Lead Scoring**: Automated scoring system for investment opportunities

### 🛠️ Technical Capabilities
- **API Integration**: NewsAPI, Google Custom Search, Google Trends
- **Machine Learning**: Transformers-based sentiment analysis and zero-shot classification
- **Data Processing**: Pandas-based data manipulation and analysis
- **Visualization**: Matplotlib-based charts and heatmaps
- **Caching**: Request caching for improved performance

## 🚀 Quick Start

### Prerequisites
- Python 3.8 or higher
- Google Colab (recommended) or Jupyter Notebook
- API keys for:
  - NewsAPI
  - Google Custom Search API
  - Google Trends (optional)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/lead-generation.git
   cd lead-generation
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up API keys**
   ```bash
   # Copy the example environment file
   cp env.example .env
   
   # Edit .env with your actual API keys:
   # NEWS_API_KEY=your_actual_news_api_key
   # GOOGLE_API_KEY=your_actual_google_api_key
   # GOOGLE_CSE_ID=your_actual_cse_id
   ```

4. **Run the analysis**
   ```bash
   # For Google Colab
   # Upload the notebook and run all cells
   
   # For local execution
   jupyter notebook notebooks/company_analysis.ipynb
   ```

## 📋 Usage

### Running the Analysis

1. **Open the Jupyter Notebook**
   ```bash
   jupyter notebook notebooks/company_analysis.ipynb
   ```

2. **Configure API Keys**
   - Ensure your .env file contains all required API keys
   - The notebook will automatically load API keys from the .env file
   - For Google Colab, use the secrets manager

3. **Load Your Data**
   - The notebook uses the Forbes 2000 companies dataset included in `data/forbes_companies.csv`
   - No additional data upload required

4. **Run Analysis**
   - Execute all cells in sequence
   - The system will perform comprehensive analysis
   - Results will be displayed with investment recommendations

## 📊 Analysis Components

### 1. Financial Analysis (PCA)
- Standardizes financial metrics
- Applies Principal Component Analysis
- Ranks companies within industry
- Provides normalized scores

### 2. Technology Assessment
- Fetches company information from Wikipedia
- Uses zero-shot classification for technology detection
- Industry-specific technology mapping
- Technology adoption scoring

### 3. News Sentiment Analysis
- Fetches recent news articles
- Performs sentiment analysis using DistilBERT
- Calculates news volume and sentiment scores
- Determines share of voice in industry

### 4. Brand Interest Analysis
- Google Trends integration
- 12-month interest tracking
- Industry-normalized scoring
- Brand awareness assessment

### 5. TOPSIS Multi-Criteria Decision Making
- Combines all metrics into single score
- Industry-specific weighting
- Investment recommendation generation
- Competitive positioning analysis

## 🔧 Configuration

### API Keys Setup

1. **Copy the example file:**
   ```bash
   cp env.example .env
   ```

2. **Edit the .env file with your actual API keys:**
   ```bash
   # NewsAPI Configuration
   NEWS_API_KEY=your_actual_news_api_key
   
   # Google Custom Search Configuration
   GOOGLE_API_KEY=your_actual_google_api_key
   GOOGLE_CSE_ID=your_actual_cse_id
   
   # Optional: Google Trends (no key required)
   ENABLE_TRENDS=True
   ```

**⚠️ Important:** Never commit the `.env` file to version control! It contains your private API keys.

## 📈 Sample Results

### Investment Recommendations
| Company | TOPSIS Score | Industry Rank | Recommendation |
|---------|-------------|---------------|----------------|
| Bank of America | 0.847 | 1 | ★🏆 Best to invest in |
| ICBC | 0.723 | 2 | Strong candidate |
| China Construction Bank | 0.689 | 3 | Consider |

### Technology Analysis
| Company | Tech Score | Detected Technologies |
|---------|------------|----------------------|
| Bank of America | 0.192 | FinTech, Digital Banking |
| ICBC | 0.267 | Core Banking, Risk Management |

## 📁 Project Structure

```
lead-generation/
├── notebooks/              # Jupyter notebooks
│   └── company_analysis.ipynb   # Main analysis notebook
├── data/                   # Data files
│   └── forbes_companies.csv    # Forbes 2000 companies dataset
├── requirements.txt        # Python dependencies
├── env.example            # Environment variables template
├── .gitignore             # Git ignore file
├── LICENSE                # MIT License
└── README.md              # This file
```

## 🤝 Contributing

We welcome contributions! Please feel free to submit issues and pull requests.

### Development Setup

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test your changes
5. Submit a pull request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [NewsAPI](https://newsapi.org/) for news data
- [Google Custom Search API](https://developers.google.com/custom-search) for website discovery
- [Hugging Face Transformers](https://huggingface.co/transformers/) for AI models
- [scikit-learn](https://scikit-learn.org/) for machine learning algorithms

## 📞 Support

- 📧 Email: porasdhore@gmail.com
- 🐛 Issues: [GitHub Issues](https://github.com/buckminster07/Machine-Learning-for-Lead-Generation-Company-Analysis-Tool/issues)
- 💬 Discussions: [GitHub Discussions](https://github.com/buckminster07/Machine-Learning-for-Lead-Generation-Company-Analysis-Tool/discussions)

## 🔮 Roadmap

- [ ] Real-time data streaming
- [ ] Advanced visualization dashboard
- [ ] Multi-language support
- [ ] API endpoint development
- [ ] Mobile application
- [ ] Integration with CRM systems

---


**⭐ If you find this project helpful, please give it a star!**

