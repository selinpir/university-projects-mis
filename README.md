# Yönetim Bilişim Sistemleri | Akademik Projeler

Bu repo, Yönetim Bilişim Sistemleri lisans eğitimim sırasında hazırladığım seçili akademik projeleri bir araya getiriyor.

Projelerde iş süreçleri analizi, veri madenciliği, sistem analizi, simülasyon ve finansal analiz gibi farklı YBS alanlarında çalıştım.

## Projeler

| Proje | Alan | Kullanılan Yöntem / Araçlar |
|---|---|---|
| SAP Destek Süreçlerinin Analizi | İş Süreç Yönetimi | As-Is / To-Be, Ishikawa, SLA, BPMN |
| Kantin Kuyruk Simülasyonu | Simülasyon ve Modelleme | Arena Simulation, Excel |
| Öğrencilerde Depresyon Riskinin Modellenmesi | Veri Madenciliği | Python, pandas, scikit-learn, CRISP-DM |
| PetSAS | Sistem Analizi ve Tasarımı | Use Case, DFD, E-R, Scrum |
| Vestel Firma Değerleme | Finansal Analiz ve Değerleme | Excel, İNA, AOSM, Rasyo Analizi |

---

## SAP Destek Süreçlerinin Analizi ve İyileştirilmesi

SAP destek ticket sürecinin analiz edilerek mevcut sorunların ve iyileştirme alanlarının incelendiği iş süreçleri yönetimi çalışmasıdır.

### Çalışma kapsamında

- Mevcut süreci As-Is olarak modelledim.
- Ticket atama ve çözüm sürecindeki darboğazları inceledim.
- SLA ihlallerinin nedenlerini Ishikawa yöntemiyle analiz ettim.
- Yanlış modül ataması, önceliklendirme ve bildirim süreçlerini değerlendirdim.
- Otomatik ticket sınıflandırma ve danışman eşleştirme içeren To-Be süreç önerisi hazırladım.

**Yöntemler:** As-Is / To-Be · Ishikawa · SLA Analizi · BPMN · Süreç Analizi

---

## Kantin Kuyruk Yönetimi ve Simülasyonu

Bir KYK yurdu kantinindeki müşteri ve sipariş akışını Arena Simulation kullanarak modellediğim simülasyon çalışmasıdır.

### Çalışma kapsamında

- 10 gün ve toplam 1.200 dakikalık sistem simülasyonu oluşturdum.
- Müşteri gelişleri, servis süreleri ve personel kapasitesini modelledim.
- Kuyruk ve sistemde kalma sürelerini analiz ettim.
- 10 tekrar sonucunda ortalama sistemde kalma süresini 19,50 dakika olarak ölçtüm.
- Alternatif personel kapasitesi senaryolarını değerlendirdim.

**Araçlar:** Arena Simulation · Microsoft Excel · Kuyruk Modellemesi

---

## Öğrencilerde Depresyon Riskinin Lojistik Regresyon ile Modellenmesi

27.000'den fazla gözlem ve 18 başlangıç değişkeni içeren bir veri seti üzerinde gerçekleştirdiğim sınıflandırma çalışmasıdır.

### Çalışma kapsamında

- CRISP-DM metodolojisini izledim.
- Eksik değer ve aykırı değer analizi gerçekleştirdim.
- Kategorik değişkenleri modele uygun hale getirdim.
- Verileri standardize ederek eğitim ve test kümelerine ayırdım.
- Python ve scikit-learn ile Logistic Regression modeli oluşturdum.
- Model değişkenlerini Odds Ratio üzerinden yorumladım.

### Model sonuçları

| Metrik | Sonuç |
|---|---:|
| Accuracy | %84,65 |
| ROC-AUC | 0,9185 |
| Precision | 0,86 |
| Recall | 0,89 |
| F1 Score | 0,87 |

**Araçlar:** Python · pandas · scikit-learn · CRISP-DM

> Bu çalışma akademik bir veri madenciliği projesidir ve tıbbi tanı amacı taşımaz.

---

## PetSAS | Sistem Analizi ve Tasarımı

Veterinerlerin ve evcil hayvan sahiplerinin randevu, sağlık kaydı ve ilgili süreçlerini tek sistem altında yönetebilmesi amacıyla tasarlanan bir bilgi sistemi projesidir.

Bu çalışmada uygulama geliştirmeden çok sistemin analiz ve tasarım aşamalarına odaklandık.

### Hazırlanan çalışmalar

- Use Case Diyagramı
- As-Is / To-Be süreç akışları
- Veri Akış Diyagramı (DFD)
- Varlık-İlişki Diyagramı (E-R)
- Veri Sözlüğü
- Veritabanı Tasarımı
- Kullanıcı arayüzü tasarımları
- Fizibilite Analizi
- Scrum tabanlı proje planlaması

Proje 71 günlük bir zaman planı ve 12 Scrum sprinti üzerinden tasarlandı.

**Yöntemler:** Sistem Analizi · Gereksinim Analizi · UML · DFD · E-R Modelleme · Scrum

---

## Vestel Elektronik Firma Değerleme

Vestel Elektronik Sanayi ve Ticaret A.Ş.'nin finansal performansını inceleyerek 31.12.2025 tarihi itibarıyla firma değerini hesapladığım finansal analiz ve değerleme çalışmasıdır.

Çalışmada şirketin kamuya açıklanan finansal tabloları ve faaliyet raporlarından yararlandım.

### Finansal analiz

2018-2025 dönemi için:

- Bilanço yatay analizi
- Bilanço dikey analizi
- Gelir tablosu yatay analizi
- Gelir tablosu dikey analizi
- Likidite oranları
- Faaliyet devir oranları
- Mali yapı oranları
- Karlılık oranları
- Borsa oranları

üzerinden şirketin finansal yapısını ve dönemler arasındaki değişimi inceledim.

### Firma değerleme

Şirket değerini İndirgenmiş Nakit Akımları (İNA) yöntemiyle hesapladım.

Değerleme kapsamında:

- Firmaya Serbest Nakit Akımı hesaplaması
- Ağırlıklı Ortalama Sermaye Maliyeti (AOSM)
- Özkaynak maliyeti
- Borçlanma maliyeti
- Terminal değer
- Finansal projeksiyonlar

üzerinde çalıştım.

### Değerleme sonucu

| Gösterge | Sonuç |
|---|---:|
| AOSM | %28,96 |
| Terminal büyüme oranı | %2 |
| Hesaplanan pay değeri | 31,94 TL |
| 31.12.2025 piyasa fiyatı | 26,94 TL |
| Değerleme farkı | yaklaşık %19 |

İNA modeli, 2025 yılındaki operasyonel daralma sonrasında temkinli bir toparlanma senaryosu üzerinden oluşturuldu.

**Araçlar / Yöntemler:** Microsoft Excel · İndirgenmiş Nakit Akımları (İNA) · AOSM · Finansal Tablo Analizi · Rasyo Analizi · Finansal Modelleme

> Bu çalışma Firma Değerlemesi dersi kapsamında hazırlanmış akademik bir çalışmadır ve yatırım tavsiyesi niteliği taşımaz.

---

## Çalıştığım Alanlar

`Business Process Analysis` · `SAP` · `Data Analysis` · `Machine Learning` · `Financial Analysis` · `Company Valuation` · `Arena Simulation` · `System Analysis` · `UML` · `Scrum`

## Kullanılan Araçlar ve Teknolojiler

`Python` · `pandas` · `scikit-learn` · `Microsoft Excel` · `Arena Simulation` · `BPMN` · `CRISP-DM`
