# 📁 1 — İŞ SÜREÇ YÖNETİMİ
## NTT DATA SAP Destek Süreçlerinin İncelenmesi ve İyileştirme Önerileri
> **Ders:** İş Süreç Yönetimi(CENG 466) | **Dönem:** 2024-2025 Bahar |
## 📌 Proje Özeti

Bu çalışma, NTT Data şirketinin SAP destek süreçlerini (ticket yönetim süreci) incelemekte; gecikmelere, SLA ihlallerine ve müşteri memnuniyetsizliğine neden olan sorunları analiz ederek süreç iyileştirme önerileri sunmaktadır.

## 🎯 Amaç

- SAP ticket yönetim sürecindeki darboğazları tespit etmek  
- SLA ihlallerinin kök nedenlerini Balık Kılçığı (Ishikawa) diyagramı ile analiz etmek  
- Yeniden tasarlanmış süreç ile iyileştirilmiş performans metriklerini karşılaştırmak

## 🏢 Kapsam

Analiz edilen şirket: **NTT Data** – SAP Destek Birimi  
Süreç: Müşteri ticket oluşturma → Atama → Çözüm → Kapama → Faturalandırma

## 🔍 Süreç Adımları

1. Müşteri tarafından SolMan üzerinden ticket oluşturulması  
2. Service Desk Manager tarafından kontrol ve danışmana atama  
3. Danışman tarafından ticket aktif edilerek çözüm üretilmesi  
4. Müşteriye çözüm iletilmesi ve onay alınması  
5. Ticket kapatılması ve faturalandırma  
6. Kalite kontrolü ve geri bildirim

## ⚠️ Tespit Edilen Problemler

| Problem | Neden |
|---|---|
| Atama gecikmeleri | Müşteri eksik bilgi girişi, yanlış modül ataması |
| SLA ihlalleri | Danışmanın yanlış priority belirleme, eskalasyon yapmama |
| Geç bildirim | Uzak masaüstü kaynaklı e-posta gecikmeleri |

## ✅ İyileştirme Önerileri

- **AI destekli ticket analizi:** Geçmiş ticketlara göre otomatik yönlendirme ve priority önerisi  
- **Çok kanallı bildirim:** E-posta yanı sıra Teams, mobil uygulama ve pop-up uyarıları  
- **Otomatik danışman eşleştirme:** Uzmanlık ve iş yüküne göre akıllı atama; yedek danışman tanımlama

## 📊 Performans Karşılaştırması (Öncesi / Sonrası)

| Metrik | Öncesi | Sonrası |
|---|---|---|
| SLA İhlal Oranı | %30 | %10 |
| Ortalama Yanıt Süresi | 6 saat | 2 saat |
| Ortalama Çözüm Süresi | 48 saat | 30 saat |
| Müşteri Memnuniyeti | %60 | %85 |

## 🛠️ Kullanılan Araçlar & Metodoloji

- Süreç haritalama (As-Is / To-Be akış şemaları)  
- Balık Kılçığı (Ishikawa) – Sebep-Sonuç Diyagramı  
- SLA tabanlı performans ölçümü  
- BPMN akış şeması (Microsoft Visio / benzeri araç)


# 📁 2 — 	SİMÜLASYON VE MODELLEME
# Kantin Kuyruk Yönetimi – Tost Simülasyonu

> **Ders:** Simülasyon ve Modelleme(CENG 428) | **Dönem:** 2024–2025 Bahar | 

## 📌 Proje Özeti

Bu proje, KYK yurdu kantinindeki tost hizmetini Arena simülasyon yazılımı ile modelleyerek müşteri bekleme sürelerini, kuyruk yapısını ve personel yeterliğini analiz etmektedir. Simülasyon; personel sayısı ve tost hazırlama sürelerinin sistem performansı üzerindeki etkisini ölçmek amacıyla tasarlanmıştır.

## 🎯 Senaryo

- **Hizmet saatleri:** 11:00 – 13:00 (120 dk/gün)  
- **Simülasyon süresi:** 10 gün × 120 dk = **1200 dakika**  
- **Müşteri gelişi:** EXPO(0.626) dk — ortalama her ~37 saniyede 1 müşteri

## 🍞 Tost Türleri ve Hazırlama Süreleri

| Tost Türü | Seçilme Oranı | Hazırlama Süresi (TRIA) |
|---|---|---|
| Karışık tost | %60 | TRIA(2.5, 3, 3.5) dk |
| Kaşarlı tost | %30 | TRIA(1.5, 2, 2.5) dk |
| Özel tost | %10 | TRIA(3.5, 4, 4.5) dk |

## ⚙️ Model Bileşenleri (Arena Modülleri)

| Modül | İşlev |
|---|---|
| `Create` | Müşteri girişleri – EXPO(0.626) dağılımı |
| `Assign` | Sipariş türü ve zaman damgası atama |
| `Decide` | %60/%30/%10 olasılıklı tost türü seçimi |
| `Batch` | Karışık ve kaşarlı tostları ikişerli gruplama |
| `Process` | Kasa (1 personel, FIFO) + Tost hazırlama (2 personel) |
| `Separate` | Gruplandırılmış müşterileri tekrar ayırma |
| `Record` | İstatistik kaydı |
| `Dispose` | Müşteri çıkışı |

## 📊 Çıktı Analizi (10 Tekrar Ortalaması)

| Metrik | Sonuç |
|---|---|
| Ortalama sistemde kalma süresi | **19.50 dk** |
| %95 güven aralığı | 16.39 – 22.61 dk |
| Sistemden çıkan müşteri sayısı | ~79 müşteri |
| VA Time (tost hazırlama) | ~3–4 dk |
| WIP (aynı anda sistemdeki müşteri) | 22–67 kişi |

## 💡 Sonuç ve Öneriler

Simülasyon sonuçları, tostucuların iş yükünün yüksek olduğunu ortaya koymuştur. Mevcut 2 kişilik tost ekibinin **3 kişiye çıkarılması**, ortalama bekleme süresini ve WIP değerini anlamlı ölçüde azaltabilir.

## 🛠️ Kullanılan Araçlar

- **Arena Simulation Software**  
- **Microsoft Excel** (çıktı analizi ve güven aralığı hesabı)

## 📂 Dosyalar

| Dosya | Açıklama |
|---|---|
| `sPir_tostSimulasyonu_projeRaporu.docx` | Proje raporu (tam) |
| `tost-simulasyonu.doe` | Arena model dosyası |


# 📁 3 — VERİ MADENCİLİĞİ TEKNİKLERİ
# Öğrencilerde Depresyon Riskinin Lojistik Regresyon ile Modellenmesi

> **Ders:** Veri Madenciliği Teknikleri (YBS 441) | **Dönem:** 2025–2026 Güz | 

## 📌 Proje Özeti

Üniversite öğrencilerinin demografik, akademik, finansal ve psikososyal verilerinden yola çıkarak depresyon riskini tahmin eden bir sınıflandırma modeli geliştirilmiştir. Model, rehberlik ve psikolojik destek birimlerine yönelik bir **erken uyarı sistemi** olarak tasarlanmıştır.

## 🎯 Problem Tanımı

> *"Elimizdeki verilerden yola çıkarak, hangi öğrencilerin depresyonda olma ihtimali daha yüksektir?"*

Hedef değişken: `depresyon` (0 = yok, 1 = var)  
Öncelikli metrik: **Recall (Duyarlılık)** – riskli öğrencileri mümkün olduğunca az kaçırmak

## 📦 Veri Seti

- **Kaynak:** Kaggle – [Student Depression Dataset](https://www.kaggle.com/)  
- **Boyut:** ~27.000+ gözlem, 18 özellik  
- **Kategoriler:** Demografik (cinsiyet, yaş, şehir), akademik (not ortalaması, akademik baskı), finansal (finansal stres), psikososyal (uyku süresi, beslenme, intihar düşünceleri, aile ruh sağlığı öyküsü)

## 🔄 Metodoloji: CRISP-DM

### Veri Hazırlama
- Türkçe sütun yeniden adlandırması  
- Sayısal tip dönüşümleri (`finansalstres`, `notortalamasicgpa` vb.)  
- Aykırı değer analizi (IQR yöntemi; yaş için 15–40 aralığı dışındakiler çıkarıldı)  
- Eksik değer doldurma: `finansalstres` → medyan imputation  
- Kategorik kodlama: binary (0/1) + One-Hot Encoding (şehir, meslek, eğitim durumu)  
- Standardizasyon: yalnızca eğitim seti üzerinde fit; test setine uygulandı

### Model
- **Algoritma:** Lojistik Regresyon (scikit-learn)  
- Eğitim / Test ayrımı uygulandı  
- ~100+ özellikten oluşan sayısal X matrisi

## 📊 Model Performansı

| Metrik | Depresyon Yok (0) | Depresyon Var (1) | Genel |
|---|---|---|---|
| Accuracy | — | — | **%84.65** |
| Precision | 0.83 | 0.86 | — |
| Recall | 0.79 | **0.89** | — |
| F1 Score | 0.81 | 0.87 | — |
| ROC-AUC | — | — | **0.9185** |

## 🔑 Öne Çıkan Özellikler (Odds Ratio)

| Değişken | Odds Ratio | Etki Yönü |
|---|---|---|
| İntihar düşünceleri | 3.38 | Risk artırıcı ⬆️ |
| Akademik baskı | 3.20 | Risk artırıcı ⬆️ |
| Finansal stres | 2.25 | Risk artırıcı ⬆️ |
| Günlük çalışma saatleri | 1.53 | Risk artırıcı ⬆️ |
| Sağlıklı beslenme | 0.65 | Koruyucu ⬇️ |
| Uyku süresi | 0.81 | Koruyucu ⬇️ |

## 🛠️ Kullanılan Araçlar & Kütüphaneler

![Python](https://img.shields.io/badge/Python-3.x-blue) ![scikit-learn](https://img.shields.io/badge/scikit--learn-1.x-orange) ![Pandas](https://img.shields.io/badge/Pandas-2.x-green)

- Python, pandas, scikit-learn, matplotlib, seaborn  
- CRISP-DM metodolojisi

## 📂 Dosyalar

| Dosya | Açıklama |
|---|---|
| `25-guz-veri_madenciligi_teknikleri.pdf` | Proje raporu (CRISP-DM) |
| `notebook.ipynb` | Python analiz notebook'u |
| `student_depression.csv` | Kullanılan veri seti |

