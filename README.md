# 🧠 Brain Tumor MRI Detection with CNN

## 📌 Giriş
Bu projede **Brain Tumor MRI Detection** veri seti ([Kaggle - arwabasal](https://www.kaggle.com/datasets/arwabasal/brain-tumor-mri-detection)) kullanılmıştır.  
Amaç, MRI görüntülerinden **beyin tümörü var mı yok mu** sorusuna yanıt verebilen bir **Convolutional Neural Network (CNN)** modeli geliştirmektir.  

Proje kapsamında:
- Veri önişleme & Data Augmentation (Horizontal Flip, Rotation)  
- Custom CNN modeli (PyTorch)  
- Eğitim süreci & Accuracy/Loss analizi  
- Confusion Matrix & Classification Report  
- Grad-CAM görselleştirme  
- Hiperparametre optimizasyonu  

---

## 📊 Metrikler
Model 15 epoch boyunca eğitilmiştir.  

- **Validation Accuracy:** %78  
- **Classification Report:**  
  - No: Precision=0.63, Recall=0.75, F1=0.69  
  - Yes: Precision=0.87, Recall=0.79, F1=0.83  
- **Genel Accuracy:** 0.78  

### 🔹 Confusion Matrix
Model çoğunlukla “Yes” sınıfında daha başarılı tahminler yapmıştır.  


### 🔹 Accuracy & Loss Grafikleri
Modelde kısmi dalgalanmalar olsa da ciddi bir overfitting gözlemlenmemektedir.  


### 🔹 Grad-CAM Görselleştirmeleri
Modelin karar verirken odaklandığı bölgeler, MRI üzerindeki tümör bölgeleriyle örtüşmektedir.  


---

## 🔧 Ekler
- Farklı hiperparametreler denenmiştir:  
  - Learning Rate: 0.001, 0.0005  
  - Batch Size: 32, 64  
  - Dropout: 0.3 – 0.5  
- En iyi sonuç: `lr=0.001, batch_size=32, dropout=0.5`  
- Proje PyTorch ile GPU/CPU üzerinde çalıştırılabilmektedir.  

---

## 🚀 Sonuç ve Gelecek Çalışmalar
- Model %78 doğruluk ile beyin tümörü tespitinde başarılı sonuçlar vermektedir.  

Gelecekte yapılabilecek geliştirmeler:  
- Daha derin CNN mimarileri veya **transfer learning** (ResNet, EfficientNet)  
- Veri setinin büyütülmesi, farklı MR görüntüler ile desteklenmesi  
- Modelin **Streamlit/Gradio** ile deploy edilerek kullanıcı arayüzü eklenmesi  
- Gerçek zamanlı tahmin için medikal sistemlere entegre edilmesi  

---

## 🔗 Linkler
- 📓 [Kaggle Notebook]([https://www.kaggle.com/](https://www.kaggle.com/code/senanurztrk/braintumordetection)) 
- 📂 [Dataset - Kaggle](https://www.kaggle.com/datasets/arwabasal/brain-tumor-mri-detection)  

