# Gerçek Zamanlı İnsan Davranışlarına Dayalı Tehlikeli Durum Tespit Sistemi

<div align="center">

![SecurityVision](https://img.shields.io/badge/SecurityVision-AI%20Güvenlik-blue?style=for-the-badge&logo=shield&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.8+-blue?style=for-the-badge&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-3.0.0-green?style=for-the-badge&logo=flask&logoColor=white)
![AI](https://img.shields.io/badge/AI-DeepFace%20%2B%20Norfair-red?style=for-the-badge&logo=tensorflow&logoColor=white)
![LLM](https://img.shields.io/badge/LLM-Ollama%20Llama3.2-orange?style=for-the-badge&logo=meta&logoColor=white)

**Gerçek zamanlı tehlike tespiti, LLM destekli raporlama ve kapsamlı web paneli ile gelişmiş yapay zeka güvenlik analiz sistemi.**


</div>

---
##  Sistem Görselleri

<div align="center">
  <img src="1771486502941.jpg" width="800"/>
  <br><br>
  <img src="1771486479802.jpg" width="800"/>
</div>

##  Genel Bakış

SecurityVision, son teknoloji bilgisayar görme, makine öğrenmesi ve doğal dil işleme teknolojilerini birleştirerek kapsamlı video güvenlik çözümleri sunan kurumsal düzeyde, yapay zeka destekli bir güvenlik analiz platformudur. Sistem gerçek zamanlı tehlike tespiti, otomatik raporlama ve sezgisel web tabanlı yönetim sunar.

###  Ana Özellikler

- ** Gelişmiş AI Pipeline**: DeepFace + Norfair + Özel Tehlike Tespit Algoritması
- ** Gerçek Zamanlı Analiz**: IP kameralar, telefon kameraları (IP Webcam/iVCam) ve video dosyaları
- ** LLM Entegrasyonu**: Ollama destekli Türkçe güvenlik raporları (Llama 3.2:3B)
- ** Modern Web Arayüzü**: Bootstrap 5 dark tema ile gerçek zamanlı güncellemeler
- ** Admin Paneli**: Kullanıcı yönetimi, analitik ve sistem izleme
- ** Email Sistemi**: Doğrulama kodları ve otomatik ZIP rapor teslimatı
- ** Arka Plan İşleme**: İlerleme takibi ile çok threaded analiz

---

##  Özellikler

###  Analiz Motoru
- **Çoklu Format Desteği**: MP4, AVI, MOV, MKV, WMV, FLV, WEBM (500MB'a kadar)
- **Yüz Tespiti & Takibi**: RetinaFace + Norfair nesne takibi
- **Duygu Analizi**: Gerçek zamanlı duygu tanıma (korku, öfke, üzüntü, vb.)
- **Hareket Tespiti**: Hız hesaplama ve yörünge analizi
- **Yakınlık İzleme**: Kişiler arası mesafe ölçümü

###  Akıllı Tehlike Tespiti
- **Tehlike Seviyesi Skorlama**: 0-10 ölçeğinde tehdit değerlendirme algoritması
- **Çok Faktörlü Analiz**: Duygu + Hız + Yakınlık + Kritik kombinasyonlar
- **Otomatik Alarmlar**: Eşik tabanlı uyarı sistemi (seviye ≥ 7)
- **Gerçek Zamanlı Uyarılar**: Anlık tehlike bildirimleri

###  LLM Raporlama Sistemi
- **Ollama Entegrasyonu**: Llama 3.2:3B model ile Türkçe rapor üretimi
- **Kritik Alarm Analizi**: Seviye 7+ alarmların detaylı analizi
- **Otomatik Özetleme**: Kısa ve net güvenlik özetleri
- **Email Teslimatı**: ZIP formatında kapsamlı rapor gönderimi

###  Web Arayüzü
- **Modern Dashboard**: Bootstrap 5 ile responsive dark tema
- **Gerçek Zamanlı Güncellemeler**: AJAX polling ile canlı durum takibi
- **Drag & Drop Upload**: Sezgisel dosya yükleme arayüzü
- **İlerleme İzleme**: Detaylı analiz ilerlemesi ve durum bilgileri

###  Admin & Kullanıcı Yönetimi
- **Email Doğrulama**: 6 haneli kod ile güvenli giriş sistemi
- **Admin Paneli**: Kullanıcı listesi, doğrulama kodları, istatistikler
- **Oturum Yönetimi**: Flask session tabanlı güvenli authentication
- **CSV Export**: Kullanıcı verilerini dışa aktarma

###  Telefon Kamerası Desteği
- **IP Webcam (Android)**: `http://ip:8080/video` stream desteği
- **iVCam (iOS)**: iPhone kamerası entegrasyonu
- **Bağlantı Testi**: Otomatik IP/port kontrolü
- **Gerçek Zamanlı Stream**: Canlı kamera analizi

---

##  Teknoloji Stack'i

###  AI/ML Kütüphaneleri
```
deepface==0.0.79          # Yüz tespiti ve duygu analizi
tensorflow==2.13.0        # Derin öğrenme framework
norfair==2.2.0            # Nesne takibi ve tracking
opencv-python==4.8.1.78   # Bilgisayar görme
numpy==1.24.3             # Bilimsel hesaplama
scikit-learn==1.3.0       # Makine öğrenmesi
```

###  Backend & Web
```
flask==3.0.0              # Web framework
werkzeug==3.0.1           # WSGI utilities
```

###  Veri İşleme & Görselleştirme
```
pandas==2.0.3             # Veri manipülasyonu
matplotlib==3.7.2         # Grafik ve görselleştirme
Pillow==10.0.1            # Görüntü işleme
```

###  LLM Entegrasyonu
- **Ollama**: Yerel LLM sunucu (llama3.2:3b)
- **Custom Utils**: Prompt engineering ve veri çıkarma




### 2️ Kurulum

```bash
# Repo'yu klonlayın
git clone https://github.com/username/SecurityVision.git
cd SecurityVision

# Virtual environment oluşturun
python -m venv .venv

# Virtual environment'ı aktifleştirin
# Windows:
.venv\Scripts\activate
# Linux/Mac:
source .venv/bin/activate

# Bağımlılıkları yükleyin
pip install -r requirements.txt
```

### 3️⃣ LLM Kurulumu (Ollama)

```bash
# Ollama'yı indirin ve kurun
# https://ollama.ai/download

# Ollama servisini başlatın
ollama serve

# Llama 3.2:3B modelini indirin
ollama pull llama3.2:3b
```

### 4️⃣ Konfigürasyon

`.env` dosyası oluşturun:

```env
# Flask Konfigürasyonu
SECRET_KEY=your-super-secret-key-here

# SMTP Email Ayarları (Gmail örneği)
SMTP_SERVER=smtp.gmail.com
SMTP_PORT=587
EMAIL_ADDRESS=your-email@gmail.com
EMAIL_PASSWORD=your-app-password

# Admin Kullanıcıları (virgül ile ayrılmış)
ADMIN_EMAILS=admin1@gmail.com,admin2@gmail.com
```

> **Not**: Gmail için App Password oluşturmanız gerekir (2FA etkin olmalı)

### 5️⃣ Uygulamayı Başlatın

```bash
python app.py
```

 **Tarayıcıda açın**: http://localhost:5000

---


#### Android (IP Webcam):
```bash
1. Google Play'den "IP Webcam" uygulamasını indirin
2. Uygulamayı açın → "Start server" basın  
3. Gösterilen IP adresini not edin (örn: 192.168.1.105)
4. SecurityVision'da IP'yi girin → "Bağlantı Test Et"
5. Başarılı olursa "📱 Telefon Analizi Başlat"
```

#### iOS (iVCam):
```bash
1. App Store'dan "iVCam" uygulamasını indirin
2. PC'de iVCam Client kurduğunuzdan emin olun
3. Aynı WiFi ağında olduğunuzu kontrol edin
4. iOS uygulamasındaki IP'yi SecurityVision'da kullanın
```

###  LLM Rapor Üretimi

```bash
1. Video analizi tamamlandıktan sonra "LLM Rapor" butonuna basın
2. Sistem kritik alarmları (seviye 7+) otomatik analiz eder
3. Ollama ile Türkçe özet rapor üretilir (1-2 dakika)
4. Rapor otomatik olarak .txt dosyası şeklinde indirilir
5. " Email ile Gönder" ile ZIP paketi email'e gönderilir
```

###  Admin Paneli

Admin kullanıcıları için özel özellikler:

- **Kullanıcı Yönetimi**: Tüm kayıtlı kullanıcıları görüntüleme
- **Doğrulama Kodları**: Son gönderilen kodları izleme
- **Sistem İstatistikleri**: Günlük aktivite ve kullanım metrikleri
- **Temizlik İşlemleri**: Eski kodları silme
- **CSV Export**: Kullanıcı verilerini dışa aktarma

---
