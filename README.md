# University Course Scheduling System 🎓⏰

**Otomatik Ders Programı Oluşturma ve Yönetim Sistemi**  
_Bölüm bazlı çakışmasız ders planlama, Excel entegrasyonu ve akıllı optimizasyon_

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

<img src="https://i.imgur.com/7VJ0W7f.png" width="600" alt="System Overview">

## 🌟 Öne Çıkan Özellikler
- **Akıllı Zamanlama Algoritması** (Çakışma kontrolü ile)
- **Bölüm/Derslik/Yönetici Yönetimi**
- **Öğretim Üyesi Müsaitlik Takvimi**
- **Excel ve PDF Rapor Üretimi**
- **Ortak Ders Mantığı** (Çapraz bölümler için)
- **CLI Tabanlı Kullanıcı Arayüzü**

## 🛠 Kurulum
```bash
# 1. Repoyu klonla
git clone https://github.com/sizin-repo-linkiniz.git
cd course-scheduler

# 2. Gereksinimleri yükle
pip install -r requirements.txt

# 3. Veritabanını başlat
python main.py init-db

# 4. Sistemi çalıştır
python main.py

# Örnek Verilerle Başlatma
python main.py init-db --sample

# Yeni Bölüm Ekleme
python main.py add-department

# Ders Programı Oluşturma
python main.py generate-schedule --departments 1,2 --year 2024 --semester Güz

# Excel'e Aktarma
python main.py export-excel --output schedule.xlsx

@startuml
component "CLI Interface" as CLI
component "Scheduler Core" as Core
component "Database Module" as DB
component "Export Engine" as Export

CLI --> Core : Triggers
Core --> DB : Reads/Writes
Core --> Export : Generates Reports
@enduml

