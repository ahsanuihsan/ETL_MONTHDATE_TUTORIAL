# Tutorial Setup Lingkungan Data Science/AI dengan Anaconda, Conda, dan UV

## Oleh Ihsan Ahsanu Amala
### No Absen 9.044.DB2025





Selamat datang di tutorial ini! Di sini, kamu akan belajar cara menyiapkan lingkungan Data Science dan AI yang rapi dan terisolasi menggunakan **Anaconda**, **Conda**, dan **UV**. Tutorial ini dirancang untuk pemula hingga profesional, dengan gaya penulisan kreatif dan analogi yang memudahkan pemahaman. Yuk, mulai!

## Apa dan Mengapa?

Bayangkan lingkungan Data Science seperti dapur profesional. Tanpa organisasi yang baik, bahan-bahan (pustaka) bisa bercampur dan merusak resep (proyek). Alat-alat ini membantu:

- **Anaconda**: Dapur lengkap dengan Python, pustaka penting (NumPy, pandas, scikit-learn), dan Conda untuk manajemen lingkungan.
- **Conda**: Asisten yang menjaga dependensi tetap rapi dan menciptakan lingkungan terisolasi, sehingga TensorFlow dan PyTorch tidak bertabrakan.
- **UV**: Alternatif super cepat untuk pip, seperti kurir ekspres untuk mengambil paket Python dengan efisien.

**Mengapa penting?** Lingkungan terisolasi mencegah konflik dependensi, memastikan proyekmu berjalan lancar, dan memudahkan reproduktibilitas.

## Cara Setup Lingkungan

### Prasyarat
- Komputer dengan sistem operasi Windows, macOS, atau Linux.
- Koneksi internet untuk mengunduh Anaconda dan paket.
- Terminal (atau Anaconda Prompt di Windows).

### Langkah 1: Instal Anaconda
1. **Unduh Anaconda**: Buka [anaconda.com](https://www.anaconda.com/products/distribution) dan pilih installer untuk OS kamu (Python 3.x).
2. **Instal**: Jalankan installer. Di Windows, centang “Add Anaconda to my PATH” (opsional). Ikuti petunjuk untuk macOS/Linux.
3. **Verifikasi**: Buka terminal dan ketik:
   ```bash
   conda --version
   ```
   Pastikan versi Conda muncul (contoh: `conda 23.7.4`).


---

### Langkah 2: Buat Lingkungan Conda
1. **Buat Lingkungan**:
   ```bash
   conda create --name ds_env python=3.9
   ```
   Ganti `3.9` dengan versi Python yang diinginkan.
2. **Aktifkan**:
   ```bash
   conda activate ds_env
   ```
   Prompt terminal akan berubah ke `(ds_env)`.
3. **Instal Paket**:
   ```bash
   conda install numpy pandas scikit-learn jupyter
   ```


---

### Langkah 3: Gunakan UV untuk Manajemen Paket Cepat
1. **Instal UV**:
   ```bash
   pip install uv
   ```
2. **Instal Paket dengan UV**:
   ```bash
   uv pip install tensorflow
   ```
3. **Verifikasi**:
   ```bash
   python -c "import tensorflow as tf; print(tf.__version__)"
   ```

---

### Langkah 4: Uji Lingkungan
1. Jalankan Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
2. Buat notebook baru dan uji:
   ```python
   import numpy as np
   import pandas as pd
   import tensorflow as tf
   print("NumPy:", np.__version__)
   print("Pandas:", pd.__version__)
   print("TensorFlow:", tf.__version__)
   ```

---

## Lakukan dan Jangan Lakukan

### Lakukan:
- Buat lingkungan Conda baru untuk setiap proyek.
- Gunakan UV untuk instalasi paket cepat (misalnya, PyTorch, Hugging Face).
- Perbarui Conda secara rutin:
  ```bash
  conda update conda
  conda update --all
  ```
- Simpan lingkungan:
  ```bash
  conda env export > environment.yml
  ```

### Jangan Lakukan:
- Jangan instal paket secara global di luar lingkungan Conda.
- Jangan campur Conda dan pip/UV sembarangan; prioritaskan Conda, lalu UV/pip.
- Jangan lewati pengujian lingkungan.

---

## Analogi: Mengapa Isolasi Penting?
Proyek Data Science seperti hidangan di restoran. Jika kamu memasak cabai pedas dan sup krim di panci yang sama tanpa mencuci, rasanya akan kacau. Conda adalah panci terpisah untuk setiap proyek, UV adalah kurir cepat untuk bahan, dan Anaconda adalah dapur modernnya. Bersama, mereka menjaga alur kerjamu rapi dan efisien.





