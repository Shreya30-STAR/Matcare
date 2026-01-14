# 🤱 MatCare - Maternal & Fetal Health Prediction Platform

An advanced AI-powered platform for maternal and fetal health predictions using machine learning algorithms. MatCare provides accurate risk assessments through comprehensive analysis of maternal health parameters and CTG (Cardiotocography) data.

## 🌟 Features

### 🤰 Pregnancy Risk Prediction
- **Real-time risk assessment** using maternal health parameters
- **ML-powered predictions** with 3-tier risk classification (Low/Medium/High)
- **Comprehensive analysis** of age, blood pressure, glucose, temperature, and heart rate
- **Color-coded risk levels** for easy interpretation
- **Professional PDF reports** with clinical recommendations

### 👶 Fetal Health Prediction
- **Advanced CTG analysis** using 21 medical parameters
- **Clinical classification** (Normal/Suspect/Pathological)
- **Heart rate variability analysis** with accelerations and decelerations
- **Histogram analysis** for fetal heart rate distribution patterns
- **Detailed health reports** with research-backed evidence

### 📊 Additional Features
- **Research-based reasoning** with medical citations
- **Professional PDF generation** for medical use
- **Responsive design** optimized for all devices
- **Mock model fallback** for reliable local development
- **Comprehensive validation** of input parameters

## 🚀 Quick Start

### Prerequisites
- Python 3.11 or higher
- pip package manager

### Installation

1. **Clone or download the project**
   ```bash
   git clone <repository-url>
   cd StreamlitCare
   ```

2. **Create a virtual environment**
   ```bash
   # Windows
   py -3.11 -m venv .venv
   .\.venv\Scripts\Activate.ps1
   
   # macOS/Linux
   python3 -m venv .venv
   source .venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the application**
   ```bash
   streamlit run app.py
   ```

5. **Open your browser**
   - Navigate to `http://localhost:8501`
   - The app will automatically open in your default browser

## 📁 Project Structure

```
StreamlitCare/
├── app.py                 # Main Streamlit application
├── models.py              # Mock ML models for fallback
├── utils.py               # Utility functions and PDF generation
├── requirements.txt       # Python dependencies
└── README.md             # This file
```

## 🔧 Dependencies

- **streamlit** (>=1.49.1) - Web application framework
- **streamlit-option-menu** (>=0.4.0) - Navigation menu component
- **pandas** (>=2.3.2) - Data manipulation
- **numpy** (>=2.3.3) - Numerical computing
- **scikit-learn** (>=1.7.2) - Machine learning utilities
- **plotly** (>=6.3.0) - Interactive visualizations
- **reportlab** (>=4.4.4) - PDF generation
- **requests** (>=2.32.5) - HTTP requests

## 📖 Usage Guide

### Pregnancy Risk Prediction

1. **Navigate** to "Pregnancy Risk Prediction" tab
2. **Enter patient information:**
   - Maternal Age (15-50 years)
   - Diastolic Blood Pressure (40-120 mmHg)
   - Blood Glucose Level (3.0-25.0 mmol/L)
   - Body Temperature (35.0-42.0 °C)
   - Heart Rate (50-120 bpm)
3. **Click** "Predict Pregnancy Risk"
4. **Review** the risk assessment and recommendations
5. **Download** PDF report if needed

### Fetal Health Prediction

1. **Navigate** to "Fetal Health Prediction" tab
2. **Enter CTG parameters** across 4 organized tabs:
   - **Basic Parameters:** FHR, Accelerations, Fetal Movement, Uterine Contractions
   - **Variability:** Short-term and long-term variability parameters
   - **Decelerations:** Light, Severe, and Prolonged decelerations
   - **Histogram:** Statistical analysis parameters
3. **Click** "Predict Fetal Health"
4. **Review** the health assessment and clinical analysis
5. **Download** CTG report if needed

## 🔬 Research Foundation

MatCare is built on evidence-based research from leading medical institutions:

- **[WHO Maternal Health Guidelines](https://www.who.int/publications/i/item/9789240080591)** - World Health Organization standards
- **[Scientific Reports: ML for High-Risk Pregnancy](https://pmc.ncbi.nlm.nih.gov/articles/PMC12049423/)** - Machine learning applications
- **[PMC Research Articles](https://pmc.ncbi.nlm.nih.gov/articles/PMC11128252/)** - AI in healthcare
- **[Nature Scientific Reports](https://www.nature.com/articles/s41598-025-89905-1)** - Effective prediction models

## 🛠️ Technical Details

### Model Architecture
- **Pregnancy Risk Model:** 5-input neural network (age, BP, glucose, temp, HR)
- **Fetal Health Model:** 21-parameter CTG analysis system
- **Fallback System:** Mock models ensure app reliability

### Risk Classifications
- **Pregnancy Risk:** Low (0), Medium (1), High (2)
- **Fetal Health:** Normal (0), Suspect (1), Pathological (2)

### PDF Report Features
- Professional medical formatting
- Clinical analysis and recommendations
- Research citations and evidence
- Parameter summaries and risk assessments
- Medical disclaimer for professional use

## 🔧 Troubleshooting

### Common Issues

1. **Port already in use**
   ```bash
   streamlit run app.py --server.port 8502
   ```

2. **Dependencies not found**
   ```bash
   pip install --upgrade pip
   pip install -r requirements.txt
   ```

3. **Mock models warning**
   - This is normal when no `.pkl` files are present
   - The app automatically uses mock models for demonstration

4. **PDF generation fails**
   - Ensure reportlab is installed: `pip install reportlab`
   - Check write permissions in temp directory

### Performance Tips

- **First run** may be slower due to model loading
- **PDF generation** takes 2-3 seconds per report
- **Large datasets** may require more memory

## 📊 Sample Data

### Pregnancy Risk Input Ranges
- **Age:** 18-35 years (optimal), 15-50 years (acceptable)
- **Blood Pressure:** 60-90 mmHg (normal), 40-120 mmHg (range)
- **Glucose:** 4.0-7.8 mmol/L (normal), 3.0-25.0 mmol/L (range)
- **Temperature:** 36.1-37.2°C (normal), 35.0-42.0°C (range)
- **Heart Rate:** 60-100 bpm (normal), 50-120 bpm (range)

### CTG Parameter Ranges
- **Baseline FHR:** 110-160 bpm (normal)
- **Accelerations:** >0.001/sec (present)
- **Decelerations:** 0-0.02/sec (various types)
- **Variability:** 0-100% (abnormal percentage)

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📄 License

This project is for educational and research purposes. Please ensure compliance with medical software regulations in your jurisdiction.

## ⚠️ Medical Disclaimer

**Important:** This application is for educational and research purposes only. It should not replace professional medical judgment or direct patient care. All predictions should be validated by qualified healthcare professionals. The recommendations provided are based on current medical literature but may not apply to all individual cases.

---

**MatCare** - Advancing maternal and fetal healthcare through AI-powered predictions 🤱
