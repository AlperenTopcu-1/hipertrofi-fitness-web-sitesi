# 💪 Hipertrofi — Antrenman Takip Uygulaması

![Python](https://img.shields.io/badge/Python-3.10-blue) ![Flask](https://img.shields.io/badge/Flask-green) ![SQLite](https://img.shields.io/badge/SQLite-amber) ![Platform](https://img.shields.io/badge/PythonAnywhere-deployed-success)

Kas grubu bazlı egzersiz rehberi, kişisel program oluşturma ve ilerleme takibi için Flask web uygulaması.

---

## ✨ Özellikler

- 🫀 **Kas Grubu Haritası** — Vücut üzerinde tıklanabilir kas grupları (ön/arka görünüm)
- 📋 **Egzersiz Rehberi** — Her kas grubu için 5 farklı egzersiz, set/tekrar bilgisi ve açıklamalar
- ❤️ **Favoriler** — Beğenilen egzersizleri kaydet ve listele
- 👤 **Kullanıcı Sistemi** — Kayıt, giriş ve oturum yönetimi
- 🌐 **REST API** — JSON tabanlı endpoint'ler

---

## 🛠️ Teknolojiler

| Katman | Teknoloji |
|--------|-----------|
| Backend | Python 3.10 / Flask |
| Veritabanı | SQLite (sqlite3) |
| Frontend | HTML / CSS / JavaScript |
| Deployment | PythonAnywhere |
| Güvenlik | Werkzeug (password hashing) |

---

## 📁 Proje Yapısı

```
Hipertrofi/
├── app.py                  ← Ana uygulama ve API endpoint'leri
├── requirements.txt        ← Bağımlılıklar
├── update_db.py            ← Veritabanı güncelleme scripti
├── templates/
│   └── index.html          ← Ana sayfa şablonu
└── static/
    ├── css/style.css
    ├── js/script.js
    └── images/
        ├── body_front.png
        ├── body_back.png
        └── exercises/      ← Kas grubu başına 5 egzersiz görseli
```

---

## 🚀 Kurulum

```bash
# 1. Repoyu klonla
git clone https://github.com/AlperenTopcu-1/hipertrofi.git
cd hipertrofi

# 2. Bağımlılıkları kur
pip install -r requirements.txt

# 3. Uygulamayı başlat
python app.py

# 4. Tarayıcıda aç → http://localhost:5000
```

---

## 🗃️ Veritabanı Şeması

| Tablo | Alanlar |
|-------|---------|
| `users` | id, username, email, password |
| `muscle_groups` | id, name, turkish_name, coordinates, side |
| `exercises` | id, muscle_id, name, turkish_name, description, difficulty, equipment, sets, reps |
| `favorites` | id, user_id, exercise_id, created_at |

---

## 🌐 API Endpoint'leri

| Method | Endpoint | Açıklama |
|--------|----------|----------|
| GET | `/api/muscles` | Tüm kas gruplarını listeler |
| GET | `/api/exercises/<muscle_id>` | Kas grubuna ait egzersizler |
| POST | `/api/register` | Kullanıcı kaydı |
| POST | `/api/login` | Giriş |
| POST | `/api/logout` | Çıkış |
| GET/POST/DELETE | `/api/favorites` | Favori egzersiz yönetimi |

---

## 🔗 Canlı Demo

👉 [kullanici.pythonanywhere.com](https://kullanici.pythonanywhere.com)

---

## 👤 Geliştirici

**Alperen Topcu** — [@AlperenTopcu-1](https://github.com/AlperenTopcu-1)
