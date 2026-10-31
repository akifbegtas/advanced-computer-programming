# Advanced Computer Programming — FastAPI, SQLite3 & WebSockets

**Haliç University** — Dr. Mohammed Al-Hubaishi  
4 PDF Sunumu (134 Slayt) temel alınarak hazırlanmış, Türkçe konu anlatımlı, İngilizce teknik terimli ve canlı simülatörlü interaktif çalışma rehberi.

## 🚀 Canlı Görünüm (Live Demo)

👉 **[https://akifbegtas.github.io/advanced-computer-programming/](https://akifbegtas.github.io/advanced-computer-programming/)**

---

## 📚 Ders İçeriği (Course Content)

### 1. Introduction to FastAPI & RESTful API Architecture (PDF 1 • 61 Slides)
- **API & FastAPI Nedir?** Key Features, OpenAPI, JSON Schema, Swagger UI (`/docs`), ReDoc (`/redoc`).
- **Geliştirme Ortamı:** Python 3.10+, `pyenv`, `pip`, `fastapi[standard]`, ASGI Server (`uvicorn`), VS Code & Chrome Extensions.
- **Python Özellikleri:** Type hints, mypy, List comprehensions, generators, Asynchronous I/O.
- **5 Endpoint In-Memory CRUD Lab:** `GET /`, `POST /items`, `GET /items/{id}`, `PUT /items/{id}`, `DELETE /items/{id}` (Index shift uyarısı).
- **İlişkisel Veritabanı:** ER Diagram (Student, Course, Enrollment, 1:N), `cURL` komut satırı aracı.
- **HTTP Response Status Codes:** 1xx (Informational), 2xx (Success), 3xx (Redirection), 4xx (Client Error), 5xx (Server Error).
- **REST Mimarisi & Parametreler:** 6 adımlı iletişim akışı, Path Parameters (`{item_id}`) vs. Query Parameters (`?skip=0&limit=10`).
- **Pydantic Veri Doğrulama:** `BaseModel`, Request Body (`POST`), Form Data (`Form`), File Uploads (`UploadFile`).
- **Gelişmiş Yapılar:** `HTTPException`, Dependency Injection (`Depends`), `BackgroundTasks`, `Middleware`, `CORSMiddleware`, OAuth2 Password Flow (`OAuth2PasswordBearer`), Özel Hata Yakalayıcılar (`@app.exception_handler`).

### 2. Practical FastAPI Examples & Algorithms (PDF 2 • 15 Slides)
- **11 Canlı Endpoint:**
  1. `Hello World` (`GET /`)
  2. `Square of a Number` (`GET /square/{num}`)
  3. `String Length` (`GET /length/?s=...`)
  4. `Sum of Two Numbers` (`GET /sum/?a=&b=`)
  5. `Check Prime Number` (`GET /prime/{num}`) — Parçalı matematiksel tanım, Base Case ($n < 2$), Karekök Optimizasyonu ($\lfloor\sqrt{n}\rfloor$), Bölünebilirlik Testi.
  6. `Concatenate Strings` (`GET /concat/?a=&b=`) — cURL Windows escape notu.
  7. `Check Palindrome` (`GET /palindrome/{word}`) — `word[::-1]` dilimleme.
  8. `Generate a Fibonacci Sequence` (`GET /fibonacci/{count}`)
  9. `Reverse a String` (`GET /reverse/?s=...`)
  10. `Convert Celsius to Fahrenheit` (`GET /convert/?celsius=...`)
  11. `Euclid's Algorithm (GCD)` (`GET /gcd/?a=&b=`) — $(u, v) = (v, u \pmod v)$ adım adım simülasyonu.

### 3. Database Integration: SQLite3 & FastAPI (PDF 3 • 26 Slides)
- **SQLite3 Temelleri:** Disk-based, hafif veritabanı, Python yerleşik desteği, VS Code `SQLite Viewer`.
- **Veritabanı Mimarisi:** `Student(BaseModel)`, `sqlite3.connect('students.db')`, `cursor()`, `CREATE TABLE IF NOT EXISTS students (AUTOINCREMENT)`.
- **Hata Yönetimi & Güvenlik:** `try / except sqlite3.Error`, Parametreli SQL sorguları (`?`) ile SQL Injection engelleme, Index kullanımı.
- **Full CRUD Endpoints:** `SELECT *`, `INSERT INTO`, `UPDATE SET`, `DELETE FROM` ve `conn.commit()`.

### 4. WebSocket Implementation in FastAPI (PDF 4 • 32 Slides)
- **WebSocket vs. HTTP:** HTTP Polling maliyeti vs. Çift yönlü kalıcı tünel (Full-Duplex Persistent Tunnel).
- **Sunucu & İstemci Mimarisi:** Single Server Broadcast vs. Message Broker ile Worker yönetimi.
- **Core Fonksiyonlar:** `accept()`, `receive_text()`, `send_text()`, `receive_json()`, `send_json()`.
- **ConnectionManager Sınıfı:** `active_connections`, `connection_count`, `connect()`, `disconnect()`, `broadcast()`.
- **Frontend & İstemci Geliştirme:** HTML Color Names, `<ul>` / `<ol>` listeleri, CSS Grouping & Universal Selectors, JavaScript DOM & Event Listeners (`ws.onopen`, `ws.onmessage`, `ws.onclose`, `ws.onerror`).
- **Çoklu İstemci Canlı Sohbet Simülatörü:** Slayt 4'teki 3 pencereli chat sisteminin birebir tarayıcı simülasyonu.

### 5. Sınava Hazırlık & Test (Module 5)
- **İnteraktif Flashcard'lar:** Tıklayınca ters dönen 12 teknik terim kartı.
- **12 Soruluk Kapsamlı Test:** Açıklamalı ve anlık puanlamalı sınav hazırlık testi.

---

## 🛠️ Yerel Çalıştırma (Local Setup)

Projeyi bilgisayarınızda yerel olarak çalıştırmak için:

```bash
git clone https://github.com/akifbegtas/advanced-computer-programming.git
cd advanced-computer-programming
python3 -m http.server 8080
```

Tarayıcınızda açın:
```
http://127.0.0.1:8080/
```
