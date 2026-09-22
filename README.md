# Yönetim Bilişim Sistemleri | Akademik Projeler

Bu repo, Yönetim Bilişim Sistemleri lisans eğitimim sırasında hazırladığım seçili akademik projeleri bir araya getiriyor.

Projelerde iş süreçlerinin analizi, süreç iyileştirme, simülasyon, veri madenciliği ve sistem analizi gibi farklı alanlarda çalıştım.

## Projeler

| Proje | Alan | Kullanılan Yöntem / Araçlar |
|---|---|---|
| SAP Destek Süreçlerinin Analizi | İş Süreç Yönetimi | As-Is / To-Be, Ishikawa, SLA, BPMN |
| Kantin Kuyruk Simülasyonu | Simülasyon ve Modelleme | Arena Simulation, Excel |
| Öğrencilerde Depresyon Riskinin Modellenmesi | Veri Madenciliği | Python, pandas, scikit-learn, CRISP-DM |
| PetSAS | Sistem Analizi ve Tasarımı | Use Case, DFD, E-R, Scrum, Fizibilite Analizi |

---

## 1. SAP Destek Süreçlerinin Analizi ve İyileştirilmesi

**Ders:** İş Süreç Yönetimi  
**Dönem:** 2024–2025 Bahar

NTT DATA SAP destek birimindeki ticket yönetim sürecini analiz ettiğim süreç yönetimi çalışmasıdır.

Mevcut süreç;

`Ticket oluşturma → Atama → Çözüm → Müşteri onayı → Kapama → Faturalandırma`

adımları üzerinden incelendi.

### Çalışmada yaptıklarım

- Mevcut süreci As-Is olarak modelledim.
- Ticket atama ve çözüm sürecindeki darboğazları inceledim.
- SLA ihlallerinin nedenlerini Ishikawa diyagramı ile analiz ettim.
- Yanlış modül ataması, önceliklendirme ve geç bildirim gibi sorunları belirledim.
- Otomatik ticket sınıflandırma ve danışman eşleştirme üzerine To-Be süreç önerileri hazırladım.
- Süreç performansını SLA metrikleri üzerinden karşılaştırdım.

### İyileştirme senaryosu

| Metrik | Mevcut | Hedeflenen |
|---|---:|---:|
| SLA ihlal oranı | %30 | %10 |
| Ortalama yanıt süresi | 6 saat | 2 saat |
| Ortalama çözüm süresi | 48 saat | 30 saat |
| Müşteri memnuniyeti | %60 | %85 |

> Bu değerler gerçek üretim ortamında uygulanmış sonuçlar değil, proje kapsamında oluşturulan To-Be süreç senaryosunun hedef değerleridir.

**Yöntemler:** As-Is / To-Be · Ishikawa · SLA Analizi · BPMN · Süreç Analizi

---

## 2. Kantin Kuyruk Yönetimi ve Simülasyonu

**Ders:** Simülasyon ve Modelleme  
**Dönem:** 2024–2025 Bahar

Bir KYK yurdu kantinindeki tost sipariş sürecini Arena Simulation kullanarak modelledim.

Amaç, müşteri yoğunluğunun, servis sürelerinin ve personel kapasitesinin kuyruk üzerindeki etkisini incelemekti.

### Model

- Günlük çalışma süresi: **120 dakika**
- Simülasyon süresi: **10 gün / 1.200 dakika**
- Ortalama müşteri gelişi: **0,626 dakika**
- Kasa personeli: **1**
- Tost hazırlama personeli: **2**
- Ürün türleri: Karışık, kaşarlı ve özel tost

Modelde `Create`, `Assign`, `Decide`, `Batch`, `Process`, `Separate`, `Record` ve `Dispose` modüllerini kullandım.

### Sonuçlar

10 tekrar üzerinden:

- Ortalama sistemde kalma süresi: **19,50 dakika**
- %95 güven aralığı: **16,39 – 22,61 dakika**
- Sistemden çıkan müşteri sayısı: yaklaşık **79**
- Tost hazırlama süresi: yaklaşık **3–4 dakika**
- Aynı anda sistemde bulunan müşteri sayısı: **22–67**

Sonuçlar üzerinden mevcut iki kişilik hazırlama kapasitesinin yoğun saatlerde darboğaz oluşturabileceğini analiz ettim ve personel kapasitesinin artırıldığı alternatif senaryoyu değerlendirdim.

**Araçlar:** Arena Simulation · Microsoft Excel · Kuyruk Modellemesi

---

## 3. Öğrencilerde Depresyon Riskinin Lojistik Regresyon ile Modellenmesi

**Ders:** Veri Madenciliği Teknikleri  
**Dönem:** 2025–2026 Güz

Kaggle üzerinde yayınlanan Student Depression Dataset kullanılarak hazırladığım veri madenciliği ve sınıflandırma çalışmasıdır.

Çalışmada yaklaşık **27.000+ gözlem ve 18 başlangıç değişkeni** kullanıldı.

### Veri hazırlama

CRISP-DM metodolojisini izleyerek:

- Veri tipi dönüşümleri
- Eksik değer analizi ve medyan ile doldurma
- Aykırı değer analizi
- Binary encoding
- One-Hot Encoding
- Standardizasyon
- Eğitim / test ayrımı

işlemlerini gerçekleştirdim.

Kategorik değişkenlerin dönüştürülmesinin ardından model yaklaşık **100+ sayısal özellik** ile eğitildi.

### Model

**Algoritma:** Logistic Regression  
**Kütüphane:** scikit-learn

| Metrik | Sonuç |
|---|---:|
| Accuracy | %84,65 |
| ROC-AUC | 0,9185 |
| Precision - Hedef Sınıf | 0,86 |
| Recall - Hedef Sınıf | 0,89 |
| F1 Score - Hedef Sınıf | 0,87 |

Model katsayılarını Odds Ratio üzerinden inceleyerek değişkenlerin tahmin üzerindeki etkilerini de analiz ettim.

**Araçlar:** Python · pandas · scikit-learn · matplotlib · seaborn · CRISP-DM

> Bu çalışma akademik bir veri madenciliği projesidir ve tıbbi tanı amacı taşımaz.

---

## 4. PetSAS | Sistem Analizi ve Tasarımı

**Ders:** Sistem Analizi ve Tasarımı  
**Dönem:** 2024–2025 Güz  
**Proje Türü:** Takım çalışması

PetSAS, veterinerlerin ve evcil hayvan sahiplerinin randevu, sağlık kaydı ve stok yönetimi gibi süreçlerini tek sistem altında toplamak amacıyla tasarlanan bir bilgi sistemi projesidir.

Bu projede uygulamanın geliştirilmesinden çok sistemin analiz ve tasarım aşamalarına odaklandık.

### Hazırlanan analiz çıktıları

- Use Case Diyagramı
- As-Is / To-Be süreç akışları
- Veri Akış Diyagramı (DFD)
- Varlık-İlişki Diyagramı (E-R)
- Karar Ağacı
- HIPO Diyagramı
- Veri Sözlüğü
- Veritabanı Tasarımı
- Kullanıcı ve veteriner arayüz tasarımları
- Finansal fizibilite analizi

### Proje planı

- Başlangıç: **21.10.2024**
- Bitiş: **24.12.2024**
- Proje süresi: **71 gün**
- Planlanan sprint sayısı: **12**

Proje kapsamında sistem gereksinimleri, kullanıcı rolleri, süreçler, veri yapıları ve sistem mimarisi üzerine çalıştık.

**Yöntemler:** Sistem Analizi · Gereksinim Analizi · UML · DFD · E-R Modelleme · Scrum · Fizibilite Analizi

---

## Repo İçeriği

```text
university-projects-mis/
│
├── 25-bahar-is_surec_yonetimi/
│   └── SAP destek süreç analizi çalışması
│
├── 25-bahar-simulasyon_ve_modelleme/
│   └── Arena kuyruk simülasyonu
│
├── 25-guz-veri_madenciligi_teknikleri.pdf
│   └── Veri madenciliği proje raporu
│
├── 24-guz-sistem_analizi_ve_tasarimi.pdf
│   └── Sistem analizi ve tasarımı proje raporu
│
└── README.md
