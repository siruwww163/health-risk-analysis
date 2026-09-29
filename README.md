# **Health Risk Analysis Using Machine Learning**  
### **A Data-Driven Exploration of Health Indicators and Risk Prediction**  

---

## **Project Overview**  
This project explores health-related data to uncover patterns, identify key risk factors, and predict health status using machine learning techniques. By leveraging both **supervised** and **unsupervised learning**, we analyze health indicators such as **BMI**, **Diabetes Crude Rate**, and **Hypertension Control** to derive actionable insights.  

The analysis integrates clustering methods (K-Means, DBSCAN, Hierarchical Clustering) and predictive models (Random Forest, Gradient Boosting) while comparing dimensionality reduction techniques like **PCA** and **t-SNE**. The findings can help improve public health strategies and early intervention programs.  

---

## **Research Questions**  
1. **Clustering Patterns in Health Data**:  
   - What patterns can unsupervised learning methods (K-Means, DBSCAN, Hierarchical Clustering) reveal in health-related data?  

2. **Feature Importance and Health Risk Prediction**:  
   - Which features contribute most significantly to predicting health risk levels?  

3. **Model Robustness and Performance**:  
   - How do machine learning models perform when noise is introduced into the data?  

4. **Dimensionality Reduction and Visualization**:  
   - How do PCA and t-SNE impact the clustering and visualization of health status?  

5. **Supervised vs. Unsupervised Learning**:  
   - How well do supervised models compare to clustering methods in identifying health risk patterns?  

6. **Impact of Feature Engineering**:  
   - Does adding new features (e.g., Gender, Hypertension Prevalence) improve prediction accuracy?  

7. **Model Generalization**:  
   - Can the models maintain accuracy across various subsets, such as gender-specific data?  

---

## **Methods**  
### **Data Preprocessing**  
- Scaled features using **StandardScaler**.  
- Encoded categorical variables (Gender, Health Status).  

### **Unsupervised Learning**  
- **K-Means Clustering**: Elbow Method and Silhouette Score for optimal K.  
- **DBSCAN**: Epsilon optimization based on clustering performance.  
- **Hierarchical Clustering**: Ward's linkage with PCA-reduced data for visualization.  

### **Dimensionality Reduction**  
- **PCA**: Used for both variance analysis and visualization.  
- **t-SNE**: Applied to visualize data clustering with varying perplexity values (5, 30, 50).  

### **Supervised Learning**  
- **Random Forest Classifier**: Hyperparameter tuning using GridSearchCV.  
- **Gradient Boosting**: Compared for accuracy and overfitting analysis.  

### **Robustness Testing**  
- Introduced **random noise** to test model stability and generalization.

---

## **Results**  
### **Key Findings**  
- **K-Means Clustering** revealed clear patterns in health data but showed moderate overlap between clusters.  
- **Random Forest** achieved perfect accuracy with feature importance showing **BMI** as the dominant predictor.  
- Models remained robust to noise, achieving ~97% accuracy after perturbation.  
- **t-SNE** provided visually distinct clusters, whereas **PCA** served well for Hierarchical Clustering.  

### **Visualizations**  
- Clustering results from K-Means, DBSCAN, and Hierarchical Clustering.  
- Feature importance chart for Random Forest.  
- Dimensionality reduction scatter plots using PCA and t-SNE.

---

## **Technologies Used**  
- **Languages**: Python  
- **Libraries**:  
   - Data Processing: `Pandas`, `NumPy`, `Scikit-learn`  
   - Visualization: `Matplotlib`, `Seaborn`, `Plotly`  
   - Models: `RandomForestClassifier`, `GradientBoostingClassifier`  
   - Dimensionality Reduction: `PCA`, `t-SNE`  
- **Version Control**: Git  

---

## **File Structure**  
```plaintext
.
├── README.md                # Project documentation  
├── README.html              # Rendered HTML version of README  
├── _quarto.yml              # Quarto configuration file  
├── assets/                  # Static assets (e.g., images, stylesheets, references)  
│   ├── gu-logo.png          # Project logo  
│   ├── nature.csl           # Citation style  
│   ├── plotly.js            # Plotly visualization library  
│   └── references.bib       # Bibliography file for citations  
├── build.sh                 # Script to automate site building  
├── data/                    # Data directory  
│   ├── raw-data/            # Raw data files  
│   │   ├── cdc_heart_diabetes_data.csv  
│   │   ├── who_bmi_data.csv  
│   │   ├── who_diabetes_prevalence_crude.csv  
│   │   ├── who_diabetes_prevalence_age_std.csv  
│   │   ├── who_blood_glucose_crude.csv  
│   │   ├── who_blood_glucose_age_std.csv  
│   │   ├── who_hypertension_control.csv  
│   │   ├── who_hypertension_prevalence.csv  
│   │   ├── who_hypertension_treatment.csv  
│   │   └── who_indicators_list.csv  
│   └── processed-data/      # Processed/cleaned data files  
│       ├── who_cleaned_data.csv  
│       └── who_pivoted_data_with_classes.csv  
├── index.qmd                # Landing page for the project  
├── instructions/            # Guidelines and instructions for the project  
│   ├── expectations.qmd  
│   ├── github-usage.qmd  
│   ├── llm-usage.qmd  
│   ├── overview.qmd  
│   ├── quarto-tips.qmd  
│   ├── topic-selection.qmd  
│   └── website-structure.qmd  
├── report/                  # Final project report  
│   └── report.qmd  
├── technical-details/       # Detailed technical analysis files  
│   ├── data-cleaning/  
│   │   ├── instructions.qmd  
│   │   └── main.ipynb  
│   ├── data-collection/  
│   │   ├── closing.qmd  
│   │   ├── methods.qmd  
│   │   ├── overview.qmd  
│   │   └── main.ipynb  
│   ├── eda/  
│   │   ├── instructions.qmd  
│   │   └── main.ipynb  
│   ├── llm-usage-log.qmd  
│   ├── progress-log.qmd  
│   ├── supervised-learning/  
│   │   ├── instructions.qmd  
│   │   └── main.ipynb  
│   └── unsupervised-learning/  
│       ├── instructions.qmd  
│       └── main.ipynb  
└── xtra/                    # Additional portfolio website files  
    └── multiclass-portfolio-website/  
        ├── _quarto.yml  
        ├── build.sh  
        ├── index.qmd  
        ├── images/  
        │   ├── gu-logo.png  
        │   └── photo.jpg  
        └── _site/           # Rendered portfolio website  
            ├── index.html  
            ├── search.json  
            ├── assets/  
            │   └── gu-logo.png  
            ├── technical-details/  
            │   └── data-collection/  
            │       ├── introduction.html  
            │       ├── main.html  
            │       └── methods.html  
            └── site_libs/   # Supporting libraries for the website  

```

