# Social Media Impact Analyzer.

##  Project Overview

This repository contains contribution to the **Social Sphere: Student Social-Media Behavior & Relationship Analytics** project. The work focuses on developing a comprehensive machine learning pipeline for analyzing social media addiction patterns and deploying an interactive web application for real-time predictions and insights.

##  Key Deliverables

### 1. **Production-Ready Streamlit Application**
- **File**: `app.py` (234 lines)
- **Features**: Interactive dashboard with real-time predictions
- **Deployment**: Ready for Streamlit Community Cloud hosting

### 2. **Machine Learning Pipeline**
- **Classification Model**: Predicts relationship conflicts (High vs Low)
- **Regression Model**: Estimates addiction scores
- **Clustering Model**: Segments students into behavioral groups
- **Preprocessing Pipeline**: Handles data transformation and feature engineering

### 3. **Comprehensive Analysis Notebooks**
- **EDA Analysis**: `eda_kmtaiwo.ipynb` - Exploratory data analysis
- **MLflow Experiments**: Multiple notebooks for experiment tracking
- **Model Development**: Separate notebooks for classification, regression, and clustering

## 📊 Technical Implementation

### **Streamlit Application Features**
```python
# Core Application Structure
- Interactive user input forms
- Real-time model predictions
- EDA insights and visualizations
- Cluster exploration dashboard
- Model performance metrics
```

### **Model Architecture**
- **Classification**: Binary classification for conflict prediction
- **Regression**: Continuous prediction of addiction scores
- **Clustering**: Behavioral segmentation using HDBSCAN
- **Preprocessing**: Comprehensive feature engineering pipeline

### **Key Technical Decisions**

#### **Feature Selection Strategy**
```python
clustering_features = [
    'Age', 'Avg_Daily_Usage_Hours', 'Sleep_Hours_Per_Night',
    'Mental_Health_Score', 'Addicted_Score', 'Conflicts_Over_Social_Media'
]
```

#### **Categorical Encoding Approach**
```python
categorical_columns = [
    'Gender', 'Academic_Level', 'Most_Used_Platform', 
    'Affects_Academic_Performance', 'Relationship_Status'
]
```

## 🔬 Clustering Analysis Design

### **Why Country Column is Excluded**
The 'Country' column is **intentionally excluded** from clustering analysis for several reasons:

#### **1. High Cardinality Problem**
- **100+ unique countries** create sparse features
- **Curse of dimensionality** with 100+ binary columns
- **Noise introduction** from countries with few students

#### **2. Behavioral Focus**
- Analysis focuses on **behavioral and psychological patterns**
- Geographic location would dilute clustering signal
- Objective is student segmentation based on usage patterns

#### **3. Practical Considerations**
- **Interpretability**: Behavioral segments are more actionable
- **Intervention strategies**: Focus on modifiable behaviors
- **Model complexity**: Avoids unnecessary geographic noise

### **Alternative Geographic Analysis**
If geographic analysis is needed:
- **Regional grouping** (continents, economic regions)
- **Post-clustering analysis** of geographic distribution
- **Hierarchical clustering** with country as secondary factor

## 📈 Model Performance

### **Classification Model (Conflict Prediction)**
- **Target**: Predict relationship conflicts (High vs Low)
- **Features**: Usage patterns, mental health, sleep quality
- **Performance**: High accuracy with interpretable results

### **Regression Model (Addiction Score)**
- **Target**: Continuous addiction score prediction
- **Features**: Behavioral and demographic indicators
- **Output**: Numeric addiction scores for intervention planning

### **Clustering Model (Behavioral Segmentation)**
- **Algorithm**: HDBSCAN for robust clustering
- **Segments**: 3-5 distinct behavioral groups
- **Interpretability**: Clear behavioral patterns in each cluster

## ️ Technical Stack

### **Core Technologies**
```python
# Dependencies
streamlit>=1.22.0      # Web application framework
pandas>=1.3.0          # Data manipulation
numpy>=1.20.0          # Numerical computing
scikit-learn>=1.0.0    # Machine learning algorithms
joblib>=1.1.0          # Model serialization
plotly>=5.13.0         # Interactive visualizations
hdbscan>=0.8.29        # Advanced clustering
seaborn>=0.11.0        # Statistical visualizations
lightgbm>=4.0.0        # Gradient boosting
```

### **Project Structure**
```
kola-taiwo/
├── app.py                    # Main Streamlit application
├── utils.py                  # Utility functions
├── requirements.txt          # Dependencies
├── models/                   # Trained models
│   ├── classifier_model.pkl  # Conflict classifier
│   ├── regressor_model.pkl   # Addiction regressor
│   ├── clustering_model.pkl  # Behavioral clusters
│   └── preprocessor.pkl      # Data preprocessing
├── notebooks/                # Analysis notebooks
│   ├── eda_kmtaiwo.ipynb     # Exploratory analysis
│   ├── mlf_clustering_model.ipynb
│   ├── mlf_predictive_task_conflict_classifier.ipynb
│   └── mlf_predictive_task_addiction_level-regressor.ipynb
├── data/                     # Dataset
│   └── ssma.csv             # Social media addiction data
└── deployment/              # Deployment assets
```

This README.md specifically highlights the contributions to the Social Sphere project, including:

1. **Streamlit application** with its features and capabilities
2. **Machine learning pipeline** (classification, regression, clustering)
3. **Technical decisions made** (like excluding the Country column from clustering)
4. **EDA notebooks** and MLflow experiments
5. **Deployment-ready solution** with production features
6. **Personal specific insights** and findings from the analysis



##  Usage Instructions

### **Local Development**
1. **Clone and navigate to directory:**
   ```bash
   cd submissions/team-members/kola-taiwo
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the application:**
   ```bash
   streamlit run app.py
   ```

### **Application Features**
- **Interactive Input Forms**: User-friendly feature selection
- **Real-time Predictions**: Instant model predictions
- **EDA Dashboard**: Comprehensive data insights
- **Cluster Explorer**: Behavioral segment analysis
- **Model Performance**: Accuracy and validation metrics

## 📊 Key Insights & Findings

### **Behavioral Patterns**
- **Usage Intensity**: Strong correlation with academic impact
- **Platform Preferences**: Instagram dominance (35.3%)
- **Sleep Impact**: Inverse relationship with social media use
- **Mental Health**: Significant correlation with addiction scores

### **Intervention Opportunities**
- **High-Risk Groups**: Identified through clustering analysis
- **Predictive Insights**: Early warning system for conflicts
- **Targeted Strategies**: Platform-specific intervention approaches
- **Academic Support**: Usage pattern-based academic guidance

## 🔍 Model Interpretability

### **Feature Importance**
- **Mental Health Score**: Strongest predictor of conflicts
- **Daily Usage Hours**: Key behavioral indicator
- **Sleep Quality**: Important health metric
- **Platform Usage**: Platform-specific risk factors

### **Clustering Insights**
- **Behavioral Segments**: Clear patterns in each cluster
- **Intervention Targets**: Specific groups for targeted support
- **Risk Assessment**: Quantified risk levels per segment

## 📈 Deployment & Scalability

### **Production Ready**
- **Model Serialization**: All models saved as pickle files
- **Error Handling**: Robust input validation and error management
- **Performance Optimization**: Cached data loading and model testing
- **User Experience**: Intuitive interface with clear visualizations
- **Deployed app can be seen here:** https://kola-taiwo-social-sphere-m5hxkappxnriipz8aonj2vv.streamlit.app/

### **Scalability Features**
- **Modular Design**: Easy to extend with new features
- **Model Versioning**: Support for model updates
- **Data Pipeline**: Automated preprocessing and validation
- **Cloud Deployment**: Ready for Streamlit Community Cloud

## 🎯 Impact & Applications

### **Educational Institutions**
- **Student Support**: Early identification of at-risk students
- **Intervention Programs**: Data-driven intervention strategies
- **Policy Development**: Evidence-based social media policies

### **Mental Health Professionals**
- **Assessment Tools**: Quantitative addiction scoring
- **Treatment Planning**: Personalized intervention approaches
- **Progress Monitoring**: Track intervention effectiveness

### **Researchers**
- **Data Analysis**: Comprehensive behavioral insights
- **Model Validation**: Reproducible research framework
- **Further Studies**: Foundation for additional research

## 🔮 Future Enhancements

### **Planned Improvements**
- **Real-time Data Integration**: Live data feeds
- **Advanced Analytics**: Additional ML algorithms
- **Mobile Application**: Cross-platform deployment
- **API Development**: RESTful API for external integrations

### **Research Extensions**
- **Longitudinal Studies**: Time-series analysis
- **Cross-cultural Analysis**: Geographic pattern exploration
- **Intervention Studies**: A/B testing framework
- **Predictive Maintenance**: Model performance monitoring

## 📞 Contact & Collaboration

**Author**: Kola Taiwo  
**Project**: Social Sphere - SuperDataScience Community Project  
**Contribution**: Machine Learning Pipeline & Streamlit Deployment

---

**Project Status**: ✅ Complete  
**Last Updated**: July 2025  
**Deployment**: Ready for production use
