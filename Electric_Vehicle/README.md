## README - Electric Vehicle Population Data Analysis

## 1. About the Dataset
This dataset provides fundamental information about electric vehicles (EVs), including details such as vehicle identification number (VIN), location, model year, manufacturer, and more. The dataset is sourced from [Electric Vehicle Population Data](https://catalog.data.gov/dataset/electric-vehicle-population-data) and has been analyzed from the uploaded PDF file.

## 2. File Structure and Column Descriptions
The dataset consists of multiple attributes related to electric vehicles. Below are key columns:

- **VIN (1-10):** The first 10 characters of the unique vehicle identification number.
- **County, City, State, Postal Code:** The geographical registration details of the vehicle.
- **Model Year:** Year of manufacture.
- **Make & Model:** Manufacturer and model name (e.g., Tesla Model 3).
- **Electric Vehicle Type:** Indicates whether the vehicle is a **Battery Electric Vehicle (BEV)** or **Plug-in Hybrid Electric Vehicle (PHEV)**.
- **Clean Alternative Fuel Vehicle (CAFV) Eligibility:** Specifies eligibility for incentives such as tax credits.
- **Electric Range:** The estimated distance (in miles) the vehicle can travel using only battery power.
- **Base MSRP:** The Manufacturer's Suggested Retail Price (MSRP).
- **Legislative District & Electric Utility:** Details about the area where the vehicle is registered and the electric utility provider.

## 3. Analysis Steps
The data analysis was performed in the following steps:

1. **Data Loading & Initial Overview**  
   - Imported dataset and checked structure using `df.head()` and `df.info()`.

2. **Data Cleaning (Handling Missing Values & Inconsistencies)**  
   - Missing values in **"Electric Range"** and **"Base MSRP"** were filled using the group means of Make/Model.
   - Categorical fields like **"County"** and **"Electric Utility"** were filled with "Unknown".
   - Columns **"Postal Code", "Vehicle Location", "Census Tract"** were dropped to streamline the dataset.

3. **Basic Statistical Analysis**  
   - Summary statistics on **Model Year**, **Electric Range**, and **Base MSRP**.
   - Distribution of **EV brands and models**.

4. **Visualization & Insights**
   - **EV Market Trends:** Growth in EV adoption over the years.
   - **Geographical Distribution:** Interactive maps showing EV density.
   - **Top Manufacturers & Models:** Tesla, Chevrolet, Nissan, and Ford lead the market.
   - **Electric Range Analysis:** Most EVs have a range below 250 miles.
   - **Base MSRP Trends:** EVs' pricing distribution over model years.
   - **Sankey Diagram:** Relationship between Manufacturers, Clean Fuel Eligibility, and Electric Utility Providers.

## 4. Usage Notes
- Ensure compliance with licensing agreements when using this dataset.
- Missing or incorrect data points should be handled with appropriate imputation techniques.
- Use **Python (Pandas, Matplotlib, Seaborn, Plotly)** for further analysis and visualization.

## 5.Findings

### 1. Most Common EV Model Years
- The most common EV model years in descending order: **2023 > 2024 > 2022 > 2021 > 2018 > 2020 > 2019 > 2017**

### 2. EV Distribution by State
- The majority of EVs in the dataset are located in **Washington (WA)**, comprising **98%** of the total.
- The top 4 counties in WA with the most EVs:
  1. **King County**
  2. **Snohomish County**
  3. **Pierce County**
  4. **Clark County**

### 3. Most Popular EV Models
- The most common EV models in terms of count:
  1. **Tesla Model Y**
  2. **Tesla Model 3**
  3. **Nissan Leaf**
  4. **Tesla Model S**

### 4. Average Electric Range
- The EV with the highest average electric range:
  - **Porsche Macan (305 miles)**
  - Followed by **Tesla Model Y (291 miles)**

### 5. Top Electric Utility Providers
- The top 3 electric utility providers serving EVs:
  1. **Puget Sound Energy Inc || City of Tacoma - (WA)**
  2. **Puget Sound Energy Inc**
  3. **City of Seattle - (WA) || City of Tacoma - (WA)**

---



## README - Elektrikli Araç Popülasyonu Veri Analizi

## 1. Veri Kümesi Hakkında
Bu veri kümesi, elektrikli araçlar hakkında temel bilgileri içerir. **Araç Kimlik Numarası (VIN)**, **konum**, **model yılı**, **üretici firma** gibi çeşitli özellikleri barındırır. Veri kümesi, [Electric Vehicle Population Data](https://catalog.data.gov/dataset/electric-vehicle-population-data) kaynağından alınmış ve yüklenen PDF dosyasından analiz edilmiştir.

## 2. Dosya Yapısı ve Sütun Açıklamaları
Veri kümesi, elektrikli araçlarla ilgili çeşitli sütunlardan oluşmaktadır. Önemli sütunlar aşağıdaki gibidir:

- **VIN (1-10):** Araçların benzersiz kimlik numarasının ilk 10 karakteri.
- **County, City, State, Postal Code:** Aracın tescilli olduğu bölge bilgileri.
- **Model Year:** Üretim yılı.
- **Make & Model:** Araç üreticisi ve modeli (ör. Tesla Model 3).
- **Electric Vehicle Type:** Aracın tamamen elektrikli mi (BEV) yoksa hibrit mi (PHEV) olduğunu belirtir.
- **Clean Alternative Fuel Vehicle (CAFV) Eligibility:** Araçların vergi teşvikleri gibi avantajlara uygunluğunu gösterir.
- **Electric Range:** Aracın yalnızca batarya gücüyle ne kadar yol gidebileceği (mil cinsinden).
- **Base MSRP:** Üreticinin önerdiği perakende satış fiyatı.
- **Legislative District & Electric Utility:** Aracın kayıtlı olduğu bölge ve elektrik sağlayıcısı.

## 3. Analiz Aşamaları
Veri analizi şu adımlarla gerçekleştirilmiştir:

1. **Veri Yükleme ve İlk Genel Bakış**  
   - Veri kümesi içe aktarıldı ve **df.head()**, **df.info()** fonksiyonlarıyla genel yapısı incelendi.

2. **Veri Temizleme (Eksik ve Tutarsız Değerlerin Düzeltilmesi)**  
   - **"Electric Range"** ve **"Base MSRP"** sütunlarında eksik değerler, ilgili marka/modelin ortalama değeri ile dolduruldu.
   - **"County"**, **"Electric Utility"** gibi kategorik sütunlardaki eksik değerler "Unknown" olarak belirlendi.
   - **"Postal Code", "Vehicle Location", "Census Tract"** gibi sütunlar, analiz açısından gereksiz oldukları için çıkarıldı.

3. **Temel İstatistiksel Analiz**  
   - **Model Yılı, Elektrik Menzili ve MSRP** gibi anahtar sütunlar için istatistiksel özetler oluşturuldu.
   - **Elektrikli araç markaları ve modelleri** analiz edildi.

4. **Veri Görselleştirme & Çıkarımlar**
   - **EV Pazarı Büyüme Trendi:** Yıllara göre EV benimsenme oranları incelendi.
   - **Coğrafi Dağılım:** Elektrikli araç yoğunluğunu gösteren interaktif haritalar oluşturuldu.
   - **En Popüler Üreticiler & Modeller:** Tesla, Chevrolet, Nissan ve Ford öne çıkmaktadır.
   - **Elektrik Menzili Analizi:** Çoğu elektrikli araç, 250 milin altında bir menzile sahiptir.
   - **Base MSRP Eğilimleri:** Model yıllarına göre EV fiyatlarının dağılımı incelendi.
   - **Sankey Diagramı:** Üreticiler, Temiz Yakıt Uygunluğu ve Elektrik Sağlayıcıları arasındaki ilişki analiz edildi.

## 4. Kullanım Notları
- Veri kümesinin kullanımında lisans ve telif hakkı kurallarına dikkat edilmelidir.
- Eksik veya yanlış veri noktaları uygun doldurma (imputation) teknikleriyle düzeltilmelidir.
- **Python (Pandas, Matplotlib, Seaborn, Plotly)** kullanılarak daha derin analizler ve görselleştirmeler yapılabilir.

## 5. Bulgular 

### 1. En Yaygın EV Model Yılları
- En çok bulunan EV model yılları sırasıyla: **2023 > 2024 > 2022 > 2021 > 2018 > 2020 > 2019 > 2017**

### 2. Eyaletlere Göre EV Dağılımı
- Dataset'te bulunan EV'lerin **%98'i** **Washington (WA)** eyaletinde bulunmaktadır.
- WA eyaletinde en fazla EV bulunan ilk 4 ilçe:
  1. **King County**
  2. **Snohomish County**
  3. **Pierce County**
  4. **Clark County**

### 3. En Popüler EV Modelleri
- En çok bulunan EV modelleri:
  1. **Tesla Model Y**
  2. **Tesla Model 3**
  3. **Nissan Leaf**
  4. **Tesla Model S**

### 4. Ortalama Elektrik Menzili
- En yüksek ortalama elektrik menziline sahip EV modelleri:
  - **Porsche Macan (305 mil)**
  - Ardından **Tesla Model Y (291 mil)**

### 5. En Büyük Elektrik Hizmet Sağlayıcıları
- En fazla hizmet veren 3 elektrik şirketi:
  1. **Puget Sound Energy Inc || City of Tacoma - (WA)**
  2. **Puget Sound Energy Inc**
  3. **City of Seattle - (WA) || City of Tacoma - (WA)**

