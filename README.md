# 🌾 Smart Farm Management System

![Java](https://img.shields.io/badge/Java-17-orange?style=flat-square&logo=java)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.x-brightgreen?style=flat-square&logo=springboot)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Database-blue?style=flat-square&logo=postgresql)
![Spring Security](https://img.shields.io/badge/Spring%20Security-Authentication-red?style=flat-square&logo=springsecurity)
![License](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)

Smart Farm Management System, modern tarım alanlarında toprak ve çevre verilerinin gerçek zamanlı takibini sağlayan, yapay zeka (AI) destekli bir akıllı tarım yönetim platformudur. 

Sistem, sahadaki IoT cihazlarından gelen telemetri verilerini (Sıcaklık, Toprak Nemi, Rüzgar Hızı, Işık Şiddeti, Toprak EC Besin Değeri) simüle ederek analiz eder ve entegre AI danışmanı sayesinde çiftçilere anlık biyolojik analiz ve verim tavsiyeleri sunar.

---

## 🚀 Öne Çıkan Özellikler

* **📊 Gerçek Zamanlı Telemetri Takibi:** Tarla bazlı sensör verilerinin (Sıcaklık, Nem, Rüzgar, Işık, EC) dinamik olarak izlenmesi.
* 
* **🤖 Yapay Zeka (AI) Danışman Entegrasyonu:** Generative AI servisleri kullanılarak sensör verilerinin bitki türüne göre biyolojik analizinin yapılması ve otomatik uyarı/tavsiye üretilmesi.
* 
* **🔐 Kullanıcı ve Rol Yönetimi:** Spring Security altyapısı ile güvenli oturum açma, yetkilendirme ve kullanıcıya özel tarla/cihaz yönetimi.
* 
* **🌱 Tarla ve Cihaz Mimarisi (CRUD):** Dinamik tarla ekleme, güncelleme, silme ve IoT cihaz eşleştirme mekanizması.
* 
* **🔔 Bildirim Sistemi:** AI analizleri ve eşik değeri aşımlarında kullanıcıya anlık bildirim oluşturulması.

---

## 🛠️ Teknolojik Altyapı

* **Backend:** Java 17, Spring Boot 3, Spring Data JPA, Spring Security
* **Frontend / Template Engine:** Thymeleaf, HTML5, CSS3, JavaScript (Fetch API)
* **Veritabanı:** PostgreSQL
* **Entegrasyonlar:** RESTful APIs, Spring RestTemplate, Jackson JSON Parser
* **Araçlar:** Lombok, Maven, Git, GitHub

---

## 🏗️ Mimari & Çalışma Mantığı

1. **Telemetri Simülasyonu:** `/api/fields/{id}/telemetry` endpoint'i üzerinden tarlaya bağlı cihazların sensör verileri anlık olarak güncellenir.
2. **AI Analiz Motoru:** Toplanan 5 temel sensör verisi (Sıcaklık, Nem, Rüzgar, Işık, EC) bitki türüyle harmanlanarak `AiService` üzerinden AI modeline gönderilir.
3. **Karar Destek:** AI tarafından üretilen 2 cümlelik öz ve teknik tavsiye, `NotificationRepository` üzerinden veritabanına işlenir ve kullanıcı arayüzüne yansıtılır.

---

## 🔧 Kurulum ve Çalıştırma

### Gereksinimler
* Java 17 veya üzeri
* PostgreSQL
* Maven

### Adımlar

1. Repoyu klonlayın:
   ```bash
   git clone [https://github.com/kadirsancar/smart-farm-management-system.git](https://github.com/kadirsancar/smart-farm-management-system.git)
   cd smart-farm-management-system
