# MyTone — Personal Color Analysis Web Application

MyTone is a web-based personal color analysis platform that helps users discover their seasonal color profile through image-based analysis. The system provides a modern interactive experience with personalized results, curated color palettes, fashion recommendations, and seasonal insights.

---

# Features

* Upload portrait image for analysis
* Image preview before submission
* Simulated loading progress during analysis
* Seasonal result generation:
  - Spring
  - Summer
  - Autumn
  - Winter
* Personalized color palettes
* Fashion recommendations
* Gender-specific styling pages
* Season detail pages
* Responsive modern interface
* Dynamic Flask routing

---

# Project Structure

```bash
mytone/
│
├── venv/
│
├── app.py
│   # Main Flask routing
│   # Handles page navigation and analysis process
│
├── check.py
│   # Testing and debugging model prediction
│
├── model/
│   │
│   ├── pipeline.py
│   │   # Model prediction pipeline
│   │
│   ├── notebook/
│   │   ├── face_isolator.ipynb
│   │   └── mytone_classifier.ipynb
│   │
│   └── weights/
│       └── best_farl64_classifier.pt
│
├── data/
│   ├── __init__.py
│   └── analysis_results.py
│
├── templates/
│   │
│   ├── layouts/
│   │   └── base.html
│   │
│   ├── partials/
│   │   ├── navbar.html
│   │   └── footer.html
│   │
│   └── pages/
│       ├── discover.html
│       ├── analysis.html
│       ├── result.html
│       ├── seasons.html
│       ├── spring.html
│       ├── summer.html
│       ├── autumn.html
│       ├── winter.html
│       ├── fashion.html
│       ├── gender.html
│       └── shop.html
│
├── static/
│   │
│   ├── css/
│   │   │
│   │   ├── pages/
│   │   │   ├── analysis.css
│   │   │   ├── discover.css
│   │   │   ├── fashion.css
│   │   │   ├── gender.css
│   │   │   ├── result.css
│   │   │   ├── season-detail.css
│   │   │   ├── seasons.css
│   │   │   └── shop.css
│   │   │
│   │   ├── components.css
│   │   ├── global.css
│   │   ├── layout.css
│   │   ├── responsive.css
│   │   └── variables.css
│   │
│   ├── js/
│   │   ├── main.js
│   │   └── analysis.js
│   │
│   └── images/
│
└── README.md
```

---

# Technologies Used

## Frontend
* HTML5
* CSS3
* JavaScript

## Backend
* Flask
* Jinja2 Template Engine

## Machine Learning
* PyTorch
* CNN-based Image Classification

## Programming Language
* Python

---

# Installation

Clone repository:

```bash
git clone https://github.com/your-username/mytone.git
```

Go into project directory:

```bash
cd mytone
```

Create virtual environment:

```bash
python -m venv venv
```

Activate virtual environment:

### Windows
```bash
venv\Scripts\activate
```

### Mac/Linux
```bash
source venv/bin/activate
```

Install dependencies:

```bash
pip install flask torch torchvision pillow
```

---

# Run Application

Run Flask application:

```bash
python app.py
```

or:

```bash
flask run
```

Open browser:

```bash
http://127.0.0.1:5000
```

---

# Application Flow

1. User visits Discover page  
2. User navigates to Analysis page  
3. User uploads portrait image  
4. System previews uploaded image  
5. User starts analysis  
6. Loading animation appears  
7. Image sent to prediction pipeline  
8. Model predicts seasonal color type  
9. User redirected to Result page  
10. Personalized palette and recommendations displayed  

---

# Machine Learning Integration

The application integrates a CNN-based image classification model for personal color prediction.

Prediction flow:

```python
predicted_season = predict_image(image)
```

The prediction pipeline is located inside:

```bash
model/pipeline.py
```

Model weights:

```bash
model/weights/best_farl64_classifier.pt
```

Notebook experiments and preprocessing:

```bash
model/notebook/
```

---

# Current Seasonal Categories

The model currently predicts four seasonal color types:

* Spring
* Summer
* Autumn
* Winter

Each result provides:
* Recommended color palette
* Fashion styling suggestions
* Seasonal characteristics
* Personalized outfit inspiration

---

# Future Improvements

* Advanced Deep Learning integration
* Automatic facial landmark detection
* Skin undertone extraction
* Real-time webcam analysis
* User authentication system
* Save analysis history
* Database integration
* Outfit recommendation engine
* E-commerce integration
* Dark mode support
* Mobile optimization

---

# Contributors

Developed for Human Computer Interaction (HCI) Project.

| Name | Student ID | Role |
|---|---|---|
| Annabelle Frederica Suryana | 2802412351 | Backend Developer & Frontend Support |
| Chelsy Wandellice | 2802412534 | Frontend Developer & Backend Support |
| Jennifer Liyanto | 2802392122 | UI/UX Designer (Figma) |
| Jocellyn Jonathan | 2802392085 | UI/UX Designer (Figma) |
| Sherly Davina Winarlie | 2802419963 | UI/UX Designer (Figma) |
| Muhammad Shidiq Hidayatullah | 2602199645 | - |
| Reyhan Habibi | 2802434573 | Machine Learning Engineer |

---

# Additional Resources

Some files are not included in this GitHub repository due to GitHub file size limitations and security protection policies.

Excluded files:
- Model weights (`.pt`)
- Jupyter notebooks (`.ipynb`)

The complete project files can be accessed through Google Drive:

"AKAN SEGERA DIISI"

---

# License

This project is developed for educational purposes only.
