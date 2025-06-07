# Proyek Akhir: Menyelesaikan Permasalahan Perusahaan Edutech

## Business Understanding

### Latar Belakang Bisnis

Jaya Jaya Institut adalah institusi pendidikan tinggi yang telah beroperasi sejak tahun 2000 dan telah menghasilkan banyak lulusan berkualitas. Meskipun institusi ini memiliki reputasi yang baik, mereka menghadapi masalah serius berupa tingginya tingkat *dropout* (siswa yang tidak menyelesaikan pendidikan).

Fenomena ini tidak hanya berdampak buruk pada citra institusi, tetapi juga pada efektivitas sistem pembelajaran serta kepercayaan calon mahasiswa dan orang tua. Oleh karena itu, penting bagi pihak manajemen untuk memahami dan mendeteksi lebih awal siswa-siswa yang berisiko tinggi mengalami *dropout*, sehingga dapat dilakukan intervensi tepat waktu untuk mencegahnya.

## Permasalahan Bisnis

Permasalahan utama yang ingin diselesaikan oleh Jaya Jaya Institut adalah:

1. **Tingginya tingkat dropout siswa** yang berdampak pada reputasi dan performa institusi.
2. **Kurangnya sistem deteksi dini** untuk mengidentifikasi siswa yang berisiko mengalami dropout.
3. **Keterbatasan informasi visual dan real-time** untuk memonitor performa siswa dan mengambil keputusan cepat.
4. **Minimnya alat bantu bagi pihak manajemen dan staf akademik** untuk memahami faktor-faktor yang mempengaruhi dropout.

## Cakupan Proyek

Proyek ini memiliki beberapa ruang lingkup utama yang akan dikerjakan, yaitu:

1. **Eksplorasi dan Analisis Data**

   * Menganalisis dataset performa siswa yang telah disediakan oleh Jaya Jaya Institut.
   * Mengidentifikasi pola dan faktor-faktor penting yang berkontribusi terhadap risiko dropout.

2. **Pembuatan Model Prediktif**

   * Mengembangkan model machine learning untuk memprediksi kemungkinan seorang siswa akan dropout.
   * Menggunakan teknik klasifikasi dan evaluasi performa model untuk memilih model terbaik.

3. **Pembuatan Dashboard Interaktif**

   * Merancang dashboard interaktif yang memvisualisasikan performa siswa dan prediksi risiko dropout.
   * Memberikan insight yang mudah dipahami bagi staf dan manajemen kampus.

4. **Dokumentasi dan Rekomendasi**

   * Menyusun laporan akhir yang berisi hasil analisis, performa model, serta rekomendasi intervensi yang bisa dilakukan berdasarkan hasil prediksi.

## Persiapan

### Sumber Data
Dataset yang digunakan dalam proyek ini adalah **Students' Performance** yang tersedia secara publik melalui repositori GitHub Dicoding:

📂 [Students' Performance Dataset - Dicoding](https://github.com/dicodingacademy/dicoding_dataset/blob/main/students_performance/data.csv)

### Setup Environment

Untuk menjalankan notebook dan aplikasi dashboard, ikuti langkah-langkah berikut:

1. **Clone repositori ini** (jika belum):
    ```bash
    git clone https://github.com/username/repo-anda.git
    cd repo-anda
    ```

2. **Buat dan aktifkan virtual environment** menggunakan pipenv:
    ```bash
    pip install pipenv
    pipenv install
    pipenv shell
    ```

    > Atau jika menggunakan `requirements.txt`, jalankan:
    ```bash
    python -m venv venv
    
    source venv/bin/activate  # untuk Linux/macOS
    
    venv\\Scripts\\activate   # untuk Windows

    pip install -r requirements.txt
    ```

3. **Dengan Conda**
      - Buat environment baru dengan Conda
      
      Jalankan perintah berikut untuk membuat environment baru bernama dropout-prediction menggunakan Python 3.9.15 <br>
      ```
      conda create -n dropout-prediction python=3.9.15
      ```
      
      - Aktifkan environment yang telah dibuat
      
      Setelah environment berhasil dibuat, aktifkan environment tersebut dengan perintah berikut<br>
      
      ```
      conda activate dropout-prediction
      ```
      
      - Install dependencies
      
      Setelah environment aktif, install semua dependensi yang diperlukan untuk menjalankan aplikasi dan model prediksi dropout. Anda dapat menggunakan file `requirements.txt` yang sudah disediakan dalam proyek        ini <br>
      
      ```
      pip install -r requirements.txt
      ```

5. **Jalankan Jupyter Notebook**:
    ```bash
    jupyter notebook
    ```

6. **(Opsional) Jalankan Streamlit dashboard**:
    ```bash
    cd streamlit_dashboard
    streamlit run app.py
    ```

---


## Business Dashboard - Education Overview

### 📘 Deskripsi
Dashboard ini dibuat menggunakan **Metabase** (versi lokal) untuk memvisualisasikan data mahasiswa secara menyeluruh. Fokus utama dashboard adalah memberikan wawasan terkait status pendidikan, demografi, status sosial ekonomi, dan distribusi mahasiswa.
![image](https://github.com/user-attachments/assets/02c8d28e-dce9-41cd-a05c-120dc553b8b1)

![image](https://github.com/user-attachments/assets/d7acf156-208d-4dc1-ab6b-59fe8a7cbb0e)

---

### 📊 Ringkasan Utama

| Keterangan           | Nilai     |
|----------------------|-----------|
| Total Mahasiswa      | 4.424     |
| Total Drop Out       | 1.421     |
| Rate Drop Out        | 32.12%    |
| Graduated Student    | 2.209     |
| Student Active       | 794       |

---

### 📌 Statistik Dasar Mahasiswa

- **Jumlah Pria**: 1.556
- **Jumlah Wanita**: 2.868
- **Rata-rata Usia Masuk**: 23.27 tahun
- **Rata-rata Nilai Masuk**: 126.98
- **Jumlah Penerima Beasiswa**: 1.099

---

### 🧩 Status Pendidikan Mahasiswa (Grouped by Status)

- **Graduate**: 49.9%
- **Dropout**: 32.1%
- **Enrolled (Aktif)**: 17.9%

---

### 💍 Distribusi Status Pernikahan Mahasiswa

- **Single**: mayoritas
- **Married, Divorced, Widowed**: minoritas

---

### 💰 Analisis Status Ekonomi (Debtor)

#### Status Hutang vs Jumlah Mahasiswa:
- **Tidak Memiliki Hutang**: 3.921 (88.6%)
- **Memiliki Hutang**: 503 (11.4%)

#### Rata-rata Nilai Masuk:
- **Tanpa Hutang**: 127.05
- **Dengan Hutang**: 126.4

#### Status Hutang vs Penerima Beasiswa:
- Mayoritas penerima beasiswa berasal dari mahasiswa **tanpa hutang**.

---

### 🌍 Mahasiswa Internasional

- **Mahasiswa Lokal**: 97.51%
- **Mahasiswa Internasional**: 2.49%

---

### 🎂 Distribusi Umur Mahasiswa

- **< 20 tahun**: paling banyak
- **20–25 tahun**: signifikan
- **26–35+ tahun**: relatif sedikit

---

### 🛠 Teknologi yang Digunakan

- **Metabase (Localhost)**
- **Visualisasi Pie Chart, Bar Chart, Donut Chart, dan Summary Cards**

---


## Menjalankan Sistem Machine Learning

Prototype sistem machine learning telah dikembangkan menggunakan **Streamlit** dan dapat dijalankan secara **online** maupun **lokal**.

### 🔗 Akses Online (Prototype)
Klik link berikut untuk mencoba prototype yang telah dideploy:

🌐 [Akses Prototype di Streamlit Cloud](https://data-science-2-nkw2bgsiiank6wtotz6odp.streamlit.app/)

---
Langkah menjalankan di lokal:
```
streamlit streamlit_dashboard.py
```

File penting:

1. `streamlit_dashboard.py`: untuk input prediksi.
2. `best_model.pkl`: Model machine learning terlatih.
3. `class_names.pkl`: Urutan fitur untuk input model.
4. `scaler.pkl`: Skaler fitur untuk preprocessing data.

## Conclusion

Proyek ini menunjukkan bagaimana pendekatan machine learning dapat diterapkan secara efektif untuk menyelesaikan masalah klasifikasi berbasis data nyata. Melalui tahapan data preprocessing, eksplorasi data (EDA), pemilihan fitur, hingga pemodelan dengan beberapa algoritma pembelajaran mesin, sistem ini berhasil membandingkan dan mengevaluasi beberapa model populer.

Dalam proyek ini, digunakan tiga algoritma utama yaitu **Logistic Regression**, **Random Forest**, dan **Gradient Boosting**. Ketiganya dipilih karena merepresentasikan pendekatan yang berbeda: model linier, model ensambel berbasis pohon, dan boosting. Evaluasi dilakukan secara menyeluruh menggunakan teknik cross-validation dan pengujian data aktual untuk memastikan bahwa model yang dipilih tidak hanya unggul dalam pelatihan, tetapi juga dapat melakukan generalisasi dengan baik terhadap data yang belum pernah dilihat sebelumnya.

Salah satu pelajaran penting dari eksperimen ini adalah pentingnya keseimbangan antara **kompleksitas model** dan **kemampuan generalisasi**. Meskipun model-model kompleks seperti Random Forest dan Gradient Boosting menawarkan performa yang sangat kompetitif, model yang lebih sederhana seperti Logistic Regression mampu memberikan hasil yang sangat baik dengan interpretabilitas yang jauh lebih tinggi. Dalam banyak kasus di dunia nyata, kemampuan untuk menjelaskan keputusan model merupakan aspek penting, terutama di bidang-bidang seperti keuangan, kesehatan, dan kebijakan publik.

Proyek ini juga menegaskan nilai dari proses evaluasi sistematis menggunakan metrik seperti akurasi, AUC, dan standar deviasi. Tanpa evaluasi kuantitatif, pemilihan model berpotensi bias dan subyektif. Dengan pendekatan ini, keputusan yang diambil menjadi lebih objektif dan berbasis data.

Secara keseluruhan, proyek ini tidak hanya menghasilkan model prediktif yang siap digunakan, tetapi juga memperlihatkan alur kerja yang dapat direplikasi untuk berbagai kasus klasifikasi lainnya. Ke depan, sistem ini masih dapat ditingkatkan melalui optimasi hyperparameter, penggunaan teknik feature engineering lanjutan, serta integrasi dengan sistem visualisasi dashboard yang dapat membantu pengguna non-teknis memahami output model dengan lebih mudah.

Dengan hasil ini, proyek menjadi fondasi yang kuat untuk pengembangan solusi berbasis machine learning yang akurat, efisien, dan mudah diakses.


## ✅ Rekomendasi Action Items

Berdasarkan analisis data serta insight dari dashboard *Jaya Jaya Institut Student Dropout Monitoring*, berikut adalah sejumlah rekomendasi strategis yang dapat diterapkan untuk menurunkan tingkat mahasiswa dropout dan meningkatkan retensi pendidikan:

1. **Penguatan Program Beasiswa dan Dukungan Finansial**  
   - Perluasan akses beasiswa bagi mahasiswa dari latar belakang ekonomi rendah.  
   - Fokus bantuan kepada mahasiswa yang terdeteksi memiliki risiko tinggi untuk dropout, khususnya yang tidak memperoleh beasiswa dan berasal dari keluarga dengan kondisi ekonomi lemah (misalnya orang tua tidak bekerja).

2. **Penerapan Intervensi Akademik Sejak Awal**  
   - Lakukan pemantauan akademik intensif pada semester awal (semester 1 dan 2).  
   - Mahasiswa dengan nilai akademik awal yang rendah perlu diarahkan ke program bimbingan, mentoring, atau kelas remedial secara proaktif.

3. **Perbaikan Proses Seleksi Masuk**  
   - Tinjau ulang kriteria penerimaan mahasiswa baru berdasarkan korelasi dengan keberhasilan studi.  
   - Implementasikan sistem prediksi risiko dropout sebagai salah satu indikator dalam proses seleksi.

4. **Peningkatan Peran Orang Tua dan Dukungan Sosial**  
   - Bangun komunikasi yang intensif dengan orang tua, terutama bagi mahasiswa dari keluarga yang kurang stabil secara ekonomi.  
   - Sediakan layanan konseling sosial dan psikologis untuk mahasiswa yang mengalami tekanan dari faktor lingkungan atau personal.

5. **Fleksibilitas dalam Skema Pembayaran Kuliah**  
   - Kembangkan sistem pembayaran uang kuliah yang lebih fleksibel dan bersahabat.  
   - Siapkan dana bantuan darurat bagi mahasiswa yang mengalami kesulitan finansial mendadak agar tetap dapat melanjutkan studi.

6. **Pemantauan Keterlibatan dan Kesejahteraan Mahasiswa**  
   - Terapkan sistem pelaporan berkala (mingguan/bulanan) melalui platform digital untuk memantau aktivitas dan keterlibatan mahasiswa.  
   - Gunakan sistem peringatan dini (early warning system) berbasis data untuk mendeteksi potensi dropout dan melakukan intervensi tepat waktu.

Dengan melaksanakan langkah-langkah di atas secara terstruktur dan berbasis data, institusi dapat secara aktif mencegah dropout dan menciptakan ekosistem pendidikan yang lebih inklusif dan suportif.
