# Solar Wind Speed Prediction with WindNet

This project replicates and extends the deep learning pipeline described in the paper:
**"Solar Wind Prediction Using Deep Learning"** by Upendran et al. (2020), developed during a research project at IUCAA, Pune.

We implement a simplified version of the WindNet model, which uses:
- **AIA EUV images (193 Å)** from NASA's Solar Dynamics Observatory (SDO)
- **Solar wind speed data** from the OMNIWeb database
- A **GoogLeNet CNN feature extractor** + **LSTM regressor** to forecast solar wind speed at Lagrangian Point L1

---

## 📊 Project Goal
Predict daily solar wind speed (in km/s) using deep learning on EUV images of the Sun, focusing on coronal holes and active regions.

---

## 🛰 Dataset
### 1. AIA EUV Images
- Source: SDO/AIA (Atmospheric Imaging Assembly)
- Channel: 193 Å
- Format: `.fits` or `.npy`

### 2. Solar Wind Speed
- Source: NASA OMNIWeb (https://omniweb.gsfc.nasa.gov/)
- Parameter: Daily average solar wind flow speed (km/s)

---

## 📚 Paper Reference
> Upendran, V., Cheung, M. C. M., Hanasoge, S., & Krishnamurthi, G. (2020). Solar wind prediction using deep learning. *Space Weather, 18*, e2020SW002478. https://doi.org/10.1029/2020SW002478

---

## 📆 Timeline
- **Phase 1**: Data collection & cleaning (OMNIWeb + SDO AIA)
- **Phase 2**: Reproduce WindNet architecture
- **Phase 3**: Preprocessing pipeline
- **Phase 4**: Modeling & evaluation
- **Phase 5**: Activation visualization (Grad-CAM)

---

## 💡 Model: WindNet
- **Feature Extractor**: Pretrained GoogLeNet (fixed weights)
- **Temporal Model**: Single-cell LSTM
- **Regression Output**: Daily wind speed in km/s
- **Loss Function**: Combined MSE + Reduced MSE
- **Evaluation Metrics**:
  - Pearson Correlation (r)
  - RMSE
  - Reduced Chi-squared (X2_red)
  - Threat Score (TS) for High-Speed Events

---

## 🚀 Getting Started
```bash
# Clone the repo
https://github.com/your-username/solar-windnet-ml

# Create a virtual environment
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows

# Install requirements
pip install -r requirements.txt

# Run preprocessing and training
python src/train_model.py
```

---

## 📈 Example Output (coming soon)
- Wind speed prediction vs. observation plot
- Grad-CAM activation maps showing CH and AR regions

---

## 🙏 Acknowledgements
This work is inspired by and builds on:
- Vishal Upendran et al.'s WindNet model
- NASA/GSFC OMNIWeb and AIA instruments
- Stanford SDOML Dataset

---

## 👤 Contact
**Khushi Verma**  
Data-Intensive Astrophysics Master's | IIT Madras '25  
[LinkedIn](https://www.linkedin.com/in/khushi-verma-1a44a722b/) | [Email](mailto:khushi@example.com)

---

## ⚖️ License
This project is licensed under the MIT License.
