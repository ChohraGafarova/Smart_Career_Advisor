# AI-Based Smart Career Advisor

## Project Overview
The **AI-Based Smart Career Advisor** is a web-based platform designed to recommend optimal career paths and skill-building roadmaps for users based on their input skills. The system combines classical machine learning models with a responsive Flask-based web interface to deliver personalized recommendations.

## Key Features
- **User Management:** Registration, login, and secure authentication.  
- **Skill Input:** Users can enter their skills in text form.  
- **Career Recommendations:** Uses multiple ML models (Random Forest, Naive Bayes, KNN) to predict suitable career paths.  
- **Roadmaps & Resources:** Suggests courses and skill-building roadmaps tailored to selected careers.  
- **Motivation Tracking:** Optional feature to track learning progress and goals.  
- **Responsive Web UI:** Accessible on desktops and mobile devices.

## Technical Stack

### Backend
- **Framework:** Python Flask  
- **ML Libraries:**
  - scikit-learn (Random Forest, Naive Bayes, KNN)  
  - pandas & numpy (data manipulation)  
- **Data Preprocessing:**
  - TF-IDF Vectorizer for text-based skill representation  
  - One-Hot Encoding for categorical features  
  - MinMaxScaler for numeric normalization  
- **Authentication & Security:**
  - Flask-Login for session management  
  - Werkzeug for password hashing  
  - Input validation & sanitization  
- **Database:** Self-made data frames  
- **APIs:** REST endpoints for ML predictions  

### Frontend
- **Technologies:** HTML5, CSS3, JavaScript, Bootstrap 5, Jinja2 templating engine  
- **Pages:** Home, Register/Login, Skill Input & Career Recommendations, About/Motivation Tracker  

### Machine Learning Models
- **Random Forest Classifier:** Ensemble model for career classification  
- **Multinomial Naive Bayes:** Works with TF-IDF skill inputs for probabilistic predictions  
- **K-Nearest Neighbors (KNN):** Optional model for similarity-based career matching  
- **Evaluation Metrics:** Accuracy, Confusion Matrix, Cross-Validation (optional)  

### Development Tools
- Python 3.11  
- Jupyter Notebook (ML experimentation)  
- Git & GitHub (version control)  
- VS Code / PyCharm (development)  
- Postman (API testing)  

### Deployment
- **Server:** Gunicorn + Nginx (production)  
- **Containerization:** Docker (optional)  
- **Hosting:** Heroku / AWS EC2 / DigitalOcean  
- **CI/CD Pipeline:** GitHub Actions for automated deployment (optional)  
- **Monitoring & Logging:** Flask logging module, AWS CloudWatch (if hosted on AWS)  

## Data Flow & Architecture
1. **User Interaction:** User inputs skills → Submit  
2. **Backend Processing:** Clean and preprocess input, convert skills into TF-IDF vector  
3. **Prediction Layer:** ML models generate career recommendations with confidence scores  
4. **Output Layer:** Recommended careers displayed with related roadmap and courses  
5. **Optional Tracking:** User progress saved, recommendations updated based on skill acquisition  

**Architecture Diagram:**  
![Architecture Diagram](https://github.com/user-attachments/assets/5753c2cb-b450-418c-81bf-8336d41346c5)  

```
[User Interface] → [Flask Backend] → [ML Models: RF, NB, KNN] → [Database] → [Recommendations]
```

## Future Enhancements
- NLP-based skill extraction from CVs and LinkedIn profiles  
- Integration of country-specific job market data  
- Deep learning recommendation models (e.g., transformers)  
- Personalized notifications and email-based insights  
- Mobile app integration (Flutter or React Native)  

## References & Resources
- [scikit-learn documentation](https://scikit-learn.org/)  
- [Flask documentation](https://flask.palletsprojects.com/)  
- [Bootstrap](https://getbootstrap.com/)  
- Career data: Self-made dataset  
- [TF-IDF & NLP resources](https://www.nltk.org/)
