### **Football Analytics Platform**

![WhatsApp Image 2024-12-04 at 13 18 22](https://github.com/user-attachments/assets/d9558154-ef29-4c28-b3b1-7495b449c019)



This project is a comprehensive **football analytics platform** that integrates **machine learning models** and **interactive dashboards** to provide actionable insights into player valuations and replacements. Built for clubs, managers, and analysts, it empowers data-driven decision-making in scouting, transfers, and team management.

---

### **Project Overview**

The platform has two primary functionalities:
1. **Market Value Prediction**:
   - Predicts player market values based on attributes like age, goals, assists, passing accuracy, and contract duration using advanced machine learning models.
2. **Player Replacement Recommendation**:
   - Identifies suitable replacements for players using cosine similarity and machine learning classification models.

Additionally, **interactive dashboards** in Power BI and Tableau provide visual insights into player statistics, team performance, and market trends.

---

### **Features**

#### **Market Value Prediction**
- Utilizes **Gradient Boosting Regressor** for accurate market value prediction with ~90% R² score.
- Key features: Age, positional data, passing metrics, goal contributions, and contract details.

#### **Player Replacement Recommendation**
- Employs **cosine similarity** to identify players with similar performance profiles.
- Uses **Random Forest Classifier** and **Gradient Boosting Classifier** to predict player suitability for a team.
- Addresses class imbalance using **SMOTE** for fair and reliable predictions.

#### **Interactive Dashboards**
- **Power BI**: Visualizes player performance trends, market values, and league comparisons.
- **Tableau**: Provides in-depth analysis of player attributes by age, height, and position.

---

### **Project Structure**

```plaintext
├── code/
│   ├── main.py                     # Main Streamlit application
│   ├── market_value_model.py       # Code for market value prediction
│   ├── player_replacement_model.py # Code for player replacement recommendation
├── data/
│   ├── player_stats.csv            # Player statistics dataset
│   ├── market_values.csv           # Market valuations dataset
├── model/
│   ├── gbr_model.pkl               # Trained Gradient Boosting Regressor
│   ├── similarity_model.pkl        # Cosine similarity model
├── dashboards/
│   ├── power_bi_dashboard.pbix     # Power BI dashboard file
│   ├── tableau_dashboard.twbx      # Tableau dashboard file
├── requirements.txt                # Python dependencies
├── README.md                       # Project documentation (this file)
```

---

### **Setup Instructions**

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/vineeth917/football-analytics.git
   cd football-analytics
   ```

2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Application**:
   ```bash
   streamlit run code/main.py
   ```

4. **View Dashboards**:
   - Open hosted dashboards via the app:
     - [Power BI Dashboard]([https://public.powerbi.com](https://app.powerbi.com/groups/me/reports/018b1e0d-080e-481e-9f8e-1fc94f0b468b/192daea5bdfd502dc7b8?experience=power-bi))
     - [Tableau Dashboard]([https://public.tableau.com](https://public.tableau.com/app/profile/vineeth.rayadurgam/viz/FootballAnalyticsDashboard-DATA230/Dashboard1))

---

### **Data and Models**

1. **Datasets**:
   - Player stats from **Transfermarkt**.
   - Enriched with features like age, height, performance metrics, and positional data.

2. **Machine Learning Models**:
   - **Market Value Prediction**: Gradient Boosting Regressor (final model).
   - **Player Replacement**:
     - Cosine Similarity for similarity scoring.
     - Random Forest and Gradient Boosting Classifiers for suitability prediction.

3. **Evaluation Metrics**:
   - R² score for regression (~90% for Gradient Boosting).
   - Accuracy (~85%) and precision/recall for classification models.

---

### **Key Insights**
- **Market Value Prediction**:
  - Younger players (21-27 years) and taller players (180-190 cm) tend to have higher market values.
  - Progressive passing metrics and goal contributions are key predictors.
  
- **Player Replacement**:
  - Top 3 recommended players are ranked by cosine similarity scores.
  - Models accurately predict player suitability with balanced class performance.

---

### **Future Enhancements**
- Include **historical player statistics** for better long-term predictions.
- Integrate **live APIs** for real-time data updates.
- Expand models to include advanced metrics like **expected goals (xG)** and injury analysis.

---

### **Contributors**
- **Vimalanandhan Sivanandham** - Project Lead, ML and Power BI Developer 
- **Shashidhar Babu P V D** - ETL
- **Vineeth R** - Tableau Developer
- **Nakshatra Desai** - Documentation
