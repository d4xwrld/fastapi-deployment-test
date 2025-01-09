# Sistem Manajemen Data Mahasiswa dengan FastAPI dan MongoDB

Aplikasi REST API untuk manajemen data mahasiswa menggunakan FastAPI dan MongoDB.

## Teknologi yang Digunakan

- [FastAPI](https://fastapi.tiangolo.com/) - Framework web Python yang modern dan cepat
- [MongoDB](https://www.mongodb.com/) - Database NoSQL
- [Motor](https://motor.readthedocs.io/) - Driver MongoDB async untuk Python
- [Pydantic](https://pydantic-docs.helpmanual.io/) - Data validation menggunakan Python type annotations

## Struktur Project

```
app/
├── server/
│   ├── models/
│   │   └── student.py    # Schema dan model data
│   ├── routes/
│   │   └── student.py    # API endpoints
│   ├── app.py           # Aplikasi FastAPI
│   └── database.py      # Konfigurasi dan operasi database
└── main.py             # Entry point aplikasi
```

## Fitur

- Create, Read, Update, Delete (CRUD) data mahasiswa
- Validasi data otomatis menggunakan Pydantic
- API dokumentasi interaktif dengan Swagger UI
- Async database operations dengan Motor

## Instalasi & Menjalankan Aplikasi

1. Clone repository:
```bash
git clone https://github.com/d4xwrld/fastapi-deployment-test.git
cd fastapi-deployment-test.git
```

2. Buat virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
.\venv\Scripts\activate   # Windows
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Jalankan MongoDB:
```bash
# Pastikan MongoDB sudah running di localhost:27017
```

5. Jalankan aplikasi:
```bash
python -m app.main
```

Aplikasi akan berjalan di `http://localhost:8000`

## API Endpoints

### Mahasiswa

- `POST /student/` - Tambah data mahasiswa baru
- `GET /student/` - Ambil semua data mahasiswa
- `GET /student/{id}` - Ambil data mahasiswa berdasarkan ID
- `DELETE /student/{id}` - Hapus data mahasiswa

## Model Data

```python
class StudentSchema(BaseModel):
    fullname: str
    email: EmailStr
    course_of_study: str
    year: int        # 1-8
    gpa: float      # 0-4.0
```

## Dokumentasi API

Akses dokumentasi interaktif di:
- Swagger UI: `http://localhost:8000/docs`
- ReDoc: `http://localhost:8000/redoc`

## Requirements

Lihat 

requirements.txt

 untuk daftar lengkap dependencies:

```txt
fastapi==0.73.0
uvicorn==0.17.4
pydantic[email]
motor==2.5.1
```

---
Dibuat dengan ❤️ menggunakan FastAPI dan MongoDB
