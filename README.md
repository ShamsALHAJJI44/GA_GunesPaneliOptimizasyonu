# GA_GunesPaneliOptimizasyonu

## 📘 Proje Tanımı
Bu proje, **Genetik Algoritma (GA)** kullanılarak güneş panellerinin **eğim (x₁)** ve **yön (x₂)** açılarını optimize etmeyi amaçlar.  
Amaç, maksimum enerji üretimini sağlayacak açıları bulmaktır.

### Amaç Fonksiyonu:
\[
y = 6x₁ + 4x₂ - 0.1x₁²
\]

### Kısıtlar:
- \( x₁ + 0.5x₂ ≤ 60 \)
- \( x₂ ≥ 15 \)
- \( 10 ≤ x₁ ≤ 45 \)
- \( 0 ≤ x₂ ≤ 90 \)

---

## ⚙️ Parametreler
| Parametre | Değer | Açıklama |
|------------|--------|----------|
| Popülasyon Boyutu | 60 | Başlangıç birey sayısı |
| Jenerasyon | 120 | Evrim süresi |
| Mutasyon Oranı | 0.2 | Genetik çeşitliliği artırır |
| Crossover Oranı | 0.9 | Ebeveyn kombinasyonu oranı |
| Elitizm | 2 | En iyi bireylerin korunması |

---

## 🧪 Deneyler ve Analiz

| Koşul                 | POP | GEN | MUT | En iyi y | Stabilizasyon |
|-----------------------|-----|-----|-----|----------|----------------|
| Temel (Baseline)      | 60  | 120 | 0.2 | 427.5    | ~70 jenerasyon |
| Deney A (mut=0.4)     | 60  | 120 | 0.4 | 426.8    | ~75 jenerasyon |
| Deney B (pop=80)      | 80  | 120 | 0.2 | 427.2    | ~72 jenerasyon |

- **Sonuçlar:** Algoritma parametre değişikliklerine karşı kararlıdır.  
- **Grafik:** En iyi fitness değeri jenerasyonlarla artarak sabitlenmiştir.  
- **Yakınsama:** Ortalama olarak 70. jenerasyonda stabil hale gelmiştir.

---

## 🎯 Sonuç ve Değerlendirme
- **En iyi çözüm:** x₁=15°, x₂=90°, yₘₐₓ=427.5  
- **Kısıt kontrolü:** Uygun (x₁ + 0.5x₂ = 60 ≤ 60)  
- **Parametre Seçimi:** Popülasyon=60 ve jenerasyon=120 çözüm kalitesi ve süre dengesi açısından uygundur.  
  Mutasyon=0.2, erken yakınsamayı önleyerek yeterli çeşitlilik sağlar.

Bu çalışma, Genetik Algoritmaların mühendislik optimizasyon problemlerinde etkin ve uygulanabilir olduğunu göstermektedir.

---

## 🚀 Çalıştırma Talimatı
1. `GA_Senaryo1_SolarPanels_Final.ipynb` dosyasını **Google Colab** veya **Jupyter Notebook** ile açın.  
2. Menüden **Runtime → Run all** seçeneğini çalıştırın.  
3. Çıktılarda en iyi sonuç, grafik ve analiz tabloları görüntülenecektir.
