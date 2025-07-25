# Social Sphere: Student Social-Media Behavior & Relationship Analytics

## 🎯 Project Overview

**Social Sphere** is a collaborative data science project that explores the relationship between social media usage patterns and students' academic performance, mental health, sleep patterns, and relationship dynamics. The project analyzes anonymized data from over 700 students across 100+ countries, aged 16-25, to provide insights into social media addiction and its impacts.

**Dataset Source:** [Kaggle - Social Media Addiction vs Relationships](https://www.kaggle.com/datasets/adilshamim8/social-media-addiction-vs-relationships)

## 📊 Project Objectives

### Primary Goals
- **Exploratory Data Analysis**: Profile demographics and social media metrics
- **Predictive Modeling**: Predict relationship conflicts and addiction levels
- **Clustering Analysis**: Segment students into behavior-based groups
- **Interactive Dashboard**: Deploy insights via Streamlit web application

### Key Research Questions
- How do social media usage patterns correlate with mental health and academic performance?
- Can we predict relationship conflicts based on usage patterns and addiction scores?
- What are the distinct behavioral segments among students?
- How do platform preferences vary across demographics and regions?

## 🏗️ Project Structure

```
SDS-CP029-social-sphere/
├── submissions/
│   ├── team-members/           # Core team contributions
│   │   ├── aditi-phadnis/      # EDA & Streamlit app
│   │   ├── blake-lawall/       # Comprehensive analysis pipeline
│   │   ├── bob-hosseini/       # MLflow experiments & classification
│   │   ├── galyna-boiko/       # Classification & regression models
│   │   ├── kola-taiwo/         # Deployment & clustering
│   │   ├── Patrick-Edosoma/    # Feature engineering & classification
│   │   └── shaheer-airaj/      # Community contribution
│   └── community-contributions/
├── requirements.txt            # Project dependencies
├── CONTRIBUTING.md            # Contribution guidelines
└── README.md                  # This file
```

## 👥 Team Contributions & Results

### 1. **Aditi Phadnis** - EDA & Streamlit Application
**Key Deliverables:**
- Comprehensive EDA notebooks with detailed visualizations
- Interactive Streamlit application (`social_media_app.py`)
- Data cleaning and preprocessing pipeline

**Technical Stack:**
- Jupyter notebooks for analysis
- Streamlit for web application
- Pandas, Matplotlib, Seaborn for visualization

**Key Findings:**
- Platform usage patterns across demographics
- Correlation between usage hours and academic performance
- Mental health score distributions by platform

### 2. **Blake Lawall** - Comprehensive Analysis Pipeline
**Key Deliverables:**
- Modular Python pipeline with 5 core modules
- Advanced clustering analysis with PCA/UMAP
- Feature engineering and encoding strategies
- Extensive visualization outputs

**Technical Implementation:**
```python
# Core modules
- data_preprocessing.py    # Data cleaning and preparation
- data_visualization.py    # Comprehensive visualizations
- clustering_analysis.py   # PCA, UMAP, clustering
- target_analysis.py       # Addiction score analysis
- feature_encoding.py      # Multiple encoding strategies
```

**Key Results:**
- **PCA Analysis**: 57.18% variance explained with 2 components
- **Platform Dominance**: Instagram leads with 35.3% preference
- **Academic Impact**: 64.3% report negative academic effects
- **Sleep Correlation**: Strong inverse relationship with social media use

### 3. **Bob Hosseini** - MLflow Experiments & Classification
**Key Deliverables:**
- MLflow experiment tracking and model versioning
- Advanced classification models with SHAP analysis
- Binary and multiclass conflict prediction

**Model Performance:**
| Model | Precision | Recall | F1-Score |
|-------|-----------|--------|----------|
| Logistic Regression | 0.98 | 0.98 | 0.98 |
| XGBoost | 0.99 | 0.99 | 0.99 |
| CatBoost | 0.99 | 1.00 | 0.99 |

**Key Insights:**
- **Mental Health** is the strongest predictor of conflicts
- **Daily Usage** and **Sleep Hours** are key behavioral indicators
- Models maintain high performance even without mental health features
- **SHAP Analysis** reveals interpretable feature importance

**MLflow Dashboard:** [View Experiments](https://dagshub.com/bab-git/SDS-social-sphere.mlflow/#/experiments/2)

### 4. **Galyna Boiko** - Classification & Regression Models
**Key Deliverables:**
- Comprehensive classification pipeline
- Regression models for addiction score prediction
- Feature engineering and model comparison

**Technical Approach:**
- Multiple preprocessing strategies
- Model ensemble techniques
- Cross-validation and hyperparameter tuning
- Performance comparison across algorithms

### 5. **Kola Taiwo** - Deployment & Clustering
**Key Deliverables:**
- Production-ready Streamlit application
- Clustering analysis with behavioral segmentation
- Model deployment pipeline

**Application Features:**
- Interactive EDA dashboards
- Real-time prediction capabilities
- Cluster exploration and visualization
- User-friendly interface for researchers and educators

**Clustering Strategy:**
- **Feature Selection**: Focused on behavioral patterns (Age, Usage Hours, Sleep, Mental Health, Addiction Score, Conflicts)
- **Geographic Exclusion**: Intentionally excluded Country due to high cardinality (100+ countries)
- **Behavioral Segmentation**: Identified distinct student groups based on usage patterns

### 6. **Patrick Edosoma** - Feature Engineering & Classification
**Key Deliverables:**
- Advanced feature engineering techniques
- Classification model training pipeline
- Data preprocessing and validation

**Technical Implementation:**
- Custom feature engineering pipeline
- Classification trainer module
- Processed datasets for training/testing

### 7. **Shaheer Airaj** - Community Contribution
**Key Deliverables:**
- Community contribution to the project
- Additional analysis perspectives

## 🔬 Key Findings & Insights

### Usage Patterns
- **Platform Preferences**: Instagram dominates (35.3%), followed by TikTok and WhatsApp
- **Daily Usage**: Average varies significantly by platform and demographic
- **Peak Hours**: Correlate with academic schedules and time zones

### Academic Impact
- **Performance Effects**: 64.3% report negative academic impact
- **Usage Correlation**: Strong relationship between daily hours and academic performance
- **Platform Variations**: Different platforms show varying academic impact levels

### Mental Health Correlations
- **Sleep Impact**: Significant inverse relationship between social media use and sleep quality
- **Addiction Patterns**: Higher addiction scores correlate with increased relationship conflicts
- **Platform Effects**: Platform-specific variations in mental health impact

### Demographic Insights
- **Regional Patterns**: Clear preferences across different countries and regions
- **Academic Level**: Influences usage patterns and platform preferences
- **Cultural Variations**: Different social media impact across cultures

## 🛠️ Technical Stack

### Core Technologies
- **Python 3.9+** - Primary programming language
- **Pandas & NumPy** - Data manipulation and analysis
- **Scikit-learn** - Machine learning algorithms
- **Matplotlib & Seaborn** - Data visualization
- **Plotly** - Interactive visualizations
- **Streamlit** - Web application deployment

### Advanced Tools
- **MLflow** - Experiment tracking and model versioning
- **XGBoost & CatBoost** - Gradient boosting algorithms
- **SHAP** - Model interpretability
- **PCA & UMAP** - Dimensionality reduction
- **HDBSCAN** - Advanced clustering

### Deployment
- **Streamlit Community Cloud** - Web application hosting
- **GitHub** - Version control and collaboration
- **Dagshub** - MLflow experiment hosting

## 📈 Model Performance Summary

### Classification Models (Conflict Prediction)
- **Best Performance**: CatBoost (F1: 0.99, Precision: 0.99, Recall: 1.00)
- **Feature Importance**: Mental Health Score, Daily Usage Hours, Sleep Hours
- **Generalization**: Models perform well across different demographic groups

### Regression Models (Addiction Score Prediction)
- **High Accuracy**: R² scores above 0.85 for most models
- **Key Predictors**: Usage patterns, sleep quality, academic performance
- **Cross-validation**: Consistent performance across folds

### Clustering Results
- **Behavioral Segments**: 3-5 distinct student groups identified
- **Interpretability**: Clear behavioral patterns in each cluster
- **Actionability**: Segments provide basis for targeted interventions

## 🚀 Deployment & Accessibility

### Streamlit Applications
- **Kola Taiwo's App**: Production-ready social media impact analyzer
- **Aditi Phadnis's App**: Interactive EDA and insights dashboard
- **Features**: Real-time predictions, cluster exploration, data visualization

### Model Accessibility
- **Pre-trained Models**: Available for immediate use
- **API Endpoints**: Ready for integration
- **Documentation**: Comprehensive usage guides

## 📚 Usage Instructions

### Getting Started
1. **Clone the repository:**
   ```bash
   git clone [repository-url]
   cd SDS-CP029-social-sphere
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run Streamlit applications:**
   ```bash
   # Kola's app
   cd submissions/team-members/kola-taiwo
   streamlit run app.py
   
   # Aditi's app
   cd submissions/team-members/aditi-phadnis
   streamlit run social_media_app.py
   ```

### Running Analysis
- **EDA**: Use notebooks in respective team member directories
- **MLflow**: Access experiment tracking via Dagshub dashboard
- **Clustering**: Run clustering analysis scripts in blake-lawall/src/

## 🤝 Contributing

This project follows the guidelines outlined in [CONTRIBUTING.md](CONTRIBUTING.md). We welcome contributions from the community!

### Contribution Areas
- Additional analysis perspectives
- Model improvements
- Visualization enhancements
- Documentation updates
- Bug fixes and optimizations

## 📄 License

This project is part of the SuperDataScience community initiative. Please refer to individual team member directories for specific licensing information.

## 🙏 Acknowledgments

Special thanks to:
- **SuperDataScience** community for organizing this collaborative project
- **All team members** for their valuable contributions
- **Kaggle** for providing the dataset
- **Open-source community** for the tools and libraries used

## 📞 Contact

For questions or contributions, please reach out to individual team members or create an issue in the repository.

---

**Project Status**: ✅ Complete  
**Last Updated**: December 2024  
**Contributors**: 7 team members + community contributions

