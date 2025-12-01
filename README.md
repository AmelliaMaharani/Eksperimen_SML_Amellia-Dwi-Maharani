# Eksperimen Machine Learning - Amellia Dwi Maharani

## 📊 Project Overview

Proyek ini merupakan bagian dari submission **Machine Learning System and MLOps** yang menggunakan **Drug Classification dataset** untuk memprediksi jenis obat yang tepat berdasarkan kondisi medis pasien.

## 🎯 Objective

Melakukan eksperimen dan preprocessing data untuk membangun model machine learning yang dapat memprediksi jenis obat yang sesuai untuk pasien berdasarkan fitur-fitur medis seperti usia, jenis kelamin, tekanan darah, dan kadar kolesterol.

## 📁 Repository Structure

```
Eksperimen_MSML_Amellia_Dwi_Maharani/
├── README.md
├── drug200.csv                                      
└── preprocessing/
    ├── Eksperimen_Amellia_Dwi_Maharani_MSML.ipynb
    └── drug_preprocessing/              
        ├── drug200_processed                            
        ├── X_test.csv                                   
        ├── X_train.csv                                  
        ├── y_test.csv                             
        ├── y_test.csv                               
        ├── y_train.csv                            
```

## 📚 Dataset Information

- **Dataset**: Drug Classification
- **Source**: [Kaggle - Pratham Tripathi](https://www.kaggle.com/datasets/prathamtripathi/drug-classification)
- **Total Samples**: 200 rows
- **Features**: 5 columns
- **Target**: 5 drug types (DrugY, drugX, drugA, drugB, drugC)

### Features Description:

| Feature | Type | Description |
|---------|------|-------------|
| `Age` | Numerical | Usia pasien (tahun) |
| `Sex` | Categorical | Jenis kelamin (M/F) |
| `BP` | Categorical | Tekanan darah (HIGH/NORMAL/LOW) |
| `Cholesterol` | Categorical | Kadar kolesterol (HIGH/NORMAL) |
| `Na_to_K` | Numerical | Rasio sodium terhadap potassium dalam darah |
| **`Drug`** | **Target** | **Jenis obat yang diresepkan (5 classes)** |

### Target Distribution:
- **DrugY**: ~90 samples
- **drugX**: ~50 samples  
- **drugA**: ~25 samples
- **drugB**: ~20 samples
- **drugC**: ~15 samples

## 🔬 Experimentation Process

### 1. Data Loading
- ✅ Load dataset menggunakan pandas
- ✅ Explorasi struktur data awal
- ✅ Check data types dan dimensi
- ✅ **Missing values analysis**: Check data yang hilang

### 2. Exploratory Data Analysis (EDA)
- ✅ **Target variable distribution**: Distribusi 5 jenis obat
- ✅ **Numerical features analysis**: Distribusi Age dan Na_to_K
- ✅ **Categorical features analysis**: Distribusi Sex, BP, Cholesterol
- ✅ **Correlation analysis**: Heatmap korelasi antar fitur
- ✅ **Drug distribution by features**: Analisis pola berdasarkan fitur

### 3. Data Preprocessing

#### Feature Engineering:
- ✅ **Encode categorical variables**: 
  - Sex → Label Encoding (M=1, F=0)
  - BP → Label Encoding (LOW=0, NORMAL=1, HIGH=2)
  - Cholesterol → Label Encoding (NORMAL=0, HIGH=1)

#### Data Splitting:
- ✅ **Train**: 60% (120 samples)
- ✅ **Validation**: 20% (40 samples)  
- ✅ **Test**: 20% (40 samples)
- ✅ Stratified split untuk menjaga proporsi target

## 🛠️ Technologies Used

- **Python** 3.12
- **pandas**: Data manipulation and analysis
- **numpy**: Numerical computing
- **matplotlib & seaborn**: Data visualization
- **scikit-learn**: Machine learning & preprocessing

## 📈 Key Findings

### Class Distribution:
- **Imbalanced dataset**: DrugY dominan (~45%), drugC minor (~7.5%)
- **Solution**: Stratified split untuk menjaga proporsi di train/val/test

## 🚀 How to Run

### 1. Clone repository:
```bash
git clone https://github.com/YOUR_USERNAME/Eksperimen_MSML_Amellia_Dwi_Maharani.git
cd Eksperimen_MSML_Amellia_Dwi_Maharani
```

### 2. Install dependencies:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter joblib
```

### 3. Download dataset:
- Download dari [Kaggle](https://www.kaggle.com/datasets/prathamtripathi/drug-classification)
- Place file `drug.csv` sebagai `drug_raw.csv` di root folder

### 4. Run Jupyter Notebook:
```bash
cd preprocessing
jupyter notebook Eksperimen_Amellia.ipynb
```

### 5. Execute all cells:
- Run semua cells secara berurutan
- Output files akan ter-generate otomatis di folder `preprocessing/`

## 📊 Expected Model Performance

### Random Forest Classifier:
- **Expected Accuracy**: 85-95%
- **Expected F1-Score**: 80-90%
- **Training Time**: < 1 minute

### Deep Learning (Neural Network):
- **Expected Accuracy**: 80-90%
- **Expected F1-Score**: 75-85%
- **Training Time**: 2-5 minutes

> **Note**: Dataset kecil (200 samples), Random Forest biasanya perform lebih baik dari Deep Learning untuk ukuran data ini.

## 📝 Next Steps

### Kriteria 2: Membangun Model
- [ ] Build Random Forest model dengan MLflow
- [ ] Manual logging (parameters, metrics, artifacts)
- [ ] Hyperparameter tuning dengan GridSearchCV
- [ ] Compare multiple configurations

### Kriteria 3: Workflow CI
- [ ] Create MLflow Project structure
- [ ] Setup GitHub Actions untuk CI/CD
- [ ] Automated model training on push
- [ ] Save artifacts to repository/Google Drive

### Kriteria 4: Monitoring & Logging
- [ ] Serve model dengan MLflow
- [ ] Setup Prometheus untuk monitoring
- [ ] Create Grafana dashboard (min 3 metrics)
- [ ] Setup alerting rules

## 👤 Author

**Amellia Dwi Maharani**  
Submission: Machine Learning System and MLOps  
Program: Dicoding Machine Learning Developer

## 📄 License

This project is created for educational purposes as part of Dicoding Machine Learning System and MLOps course.

## 🙏 Acknowledgments

- Dataset by [Pratham Tripathi](https://www.kaggle.com/prathamtripathi) on Kaggle
- Dicoding Indonesia for course materials
- Machine Learning community for inspiration

## ⭐ Project Status

| Kriteria | Status | Points |
|----------|--------|--------|
| **Kriteria 1**: Eksperimen Dataset | ✅ **Completed** | **2/4 pts (Basic)** |
| **Kriteria 2**: Membangun Model | 🔄 In Progress | 0/4 pts |
| **Kriteria 3**: Workflow CI | ⏳ Pending | 0/4 pts |
| **Kriteria 4**: Monitoring & Logging | ⏳ Pending | 0/4 pts |

**Total Progress**: 2/16 points (12.5%)

---

### 📧 Contact

For questions or feedback, please reach out via Dicoding forum or create an issue in this repository.

**Happy Learning! 🚀**
