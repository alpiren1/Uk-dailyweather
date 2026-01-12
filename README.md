# UK Climate Analysis & Temperature Prediction (1961-2024)

Bu proje, Birleşik Krallık'ın 63 yıllık meteorolojik verilerini analiz ederek iklim değişikliği trendlerini incelemek ve Makine Öğrenmesi algoritmaları ile sıcaklık tahmini yapmak amacıyla geliştirilmiştir.

##  Veri Seti Hakkında
* **Kaynak:** [Kaggle](https://www.kaggle.com/datasets/robjbutlermei/uk-daily-weather-1961-2024)
* **Kapsam:** 1961 - 2024 yılları arası günlük hava durumu verileri.
* **Özellikler:** Tarih, Sıcaklık, Çiy Noktası, Rüzgar Hızı, Yağış, Yüzey Akışı.
* **Problem Tipi:** Regresyon (Regression)

## ⚙️ Proje Adımları
1. **Veri Ön İşleme (EDA):**
   * Tarih verilerinin `datetime` formatına çevrilmesi.
   * Günlük verilerin `resample` yöntemi ile aylık ortalamalara dönüştürülmesi.
   * Eksik veri kontrolü ve temizliği.
2. **Görselleştirme:**
   * Yıllara göre sıcaklık artış trendinin (Küresel Isınma) grafiğe dökülmesi.
   * Korelasyon matrisi (Heatmap) ile değişken ilişkilerinin incelenmesi.
3. **Modelleme:**
   * **Linear Regression** ve **Random Forest Regressor** algoritmalarının kurulumu.
   * Modellerin eğitimi ve test edilmesi.

##  Sonuçlar
Modellerin performans metrikleri (R2 Score ve MSE) aşağıda karşılaştırılmıştır:

| Model | MSE (Hata Oranı) | R2 Score (Başarı) |
|-------|------------------|-------------------|
| Linear Regression | 0.1797 | 0.9907 |
| **Random Forest** | **0.1546** | **0.9920** |

**Temel Bulgular:**
* **Random Forest**, en düşük hata oranıyla en iyi performansı göstermiştir.
* Analizler, 1990 yılından sonra Birleşik Krallık'ta belirgin bir sıcaklık artışı olduğunu kanıtlamaktadır.
* Sıcaklık tahmininde en belirleyici faktörün "Çiy Noktası Sıcaklığı" olduğu tespit edilmiştir.

