# NL2SQL Chatbot Agent 
 Membangun sistem berbasis Python yang memungkinkan siapa saja mengakses data secara demokratis hanya dengan menggunakan percakapan sehari-hari.
# Anggota Tim
-Ikram Rahmani
-Ribka Putri Sutanto
-Najwa Nabila Firdaus
# Rumusan Masalah & Solusi
## Tantangan Akses Data
1. Pengguna non-teknis tidak memahami SQL.
2. Query database kompleks dan rawan error.
3. Proses akses data memakan waktu.
4. Ketergantungan pada tim teknis (IT/Data Engineer).
## Solusi
1. NL2SQL Chatbot Agent berbasis AI.
2. Mengubah bahasa alami menjadi query SQL.
3. Interaksi seperti chatting (user-friendly).
4. Akses data lebih cepat dan mudah.
# Apa Itu SQL?
SQL (Structured Query Language) adalah bahasa standar yang digunakan untuk mengakses dan mengelola database. Dengan SQL, pengguna dapat mengambil, menambah, mengubah, dan menghapus data dalam sistem database.
# Apa Itu NL2SQL?
Natural Language to SQL (NL2SQL) adalah teknologi yang mengubah pertanyaan dalam bahasa manusia (Natural Language) menjadi query SQL yang valid secara sintaksis dan semantik.
# Arsitektur Alur Kerja
1. Python
Bertindak sebagai “otak” yang mengatur lalu lintas data.
2. Ollama & Qwen 2.5
Qwen 2.5 digunakan untuk memahami instruksi logika. Model menerima pertanyaan dalam bahasa alami dan metadata tabel, lalu menghasilkan sintaks SQL.
3. MySQL (Data Source)
Tempat penyimpanan data. Query SQL yang dihasilkan model akan dieksekusi melalui Python.
# Tantangan Akses Data Tradisional
## Hambatan Query
Pengguna non-teknis sering kesulitan mengakses data karena harus memahami sintaks SQL yang kompleks dan struktur database yang kaku.
## Solusi AI Chatbot
Chatbot berbasis NL2SQL memungkinkan siapa saja bertanya menggunakan bahasa alami dan mendapatkan hasil instan dalam bentuk tabel.
# Kekuatan Ollama & Qwen 2.5
## Kelebihan Ollama
1. Mudah digunakan
2. Privasi dan keamanan lebih terjaga
3. Mendukung kuantisasi model secara efisien
## Kelebihan Qwen 2.5
1. Unggul dalam coding dan matematika
2. Pemahaman Bahasa Indonesia sangat baik
3. Mendukung context window panjang
# Alur Kerja Percakapan ke SQL
1. Input User
Pengguna mengajukan pertanyaan dalam bahasa alami melalui Streamlit.
2. AI Processing
Qwen 2.5 mengubah natural language menjadi query SQL.
3. DB Execution
Query dijalankan pada database SQLite/MySQL.
4. Hasil Ditampilkan
Output ditampilkan dalam bentuk tabel yang mudah dipahami.
# Implementasi Engine LangChain
## Prompt Engineering
Menggunakan prompt template untuk memastikan AI menghasilkan query SQL murni tanpa tambahan penjelasan teks.
## SQLDatabase Chain
Menggunakan fitur use_query_checker=True untuk memastikan sintaks SQL valid sebelum dieksekusi.
# ANTARMUKA CHAT STREAMLIT MODERN
## USER-CENTRIC DESIGN
Dibangun menggunakan Streamilt untuk aksesibilitas web yang cepat Fitur utama termasuk riwayat percakapan yang persisten (Session State) dan tampilan tabel responsif

Integrasi st.chat message memberikan pengalaman layaknya ChatGPT namun dengan akses data perusahaan yang aman
# Fitur Cerdas: Deteksi Tabel Otomatis
## Detection
Sistem secara otomatis mendeteksi apakah respons AI berupa list data atau teks biasa.
## Auto-Formatting
Data mentah dari database langsung dikonversi menjadi Pandas DataFrame.
## Visualisasi
Hasil query kompleks ditampilkan dalam format tabel yang mudah dibaca pengguna.
# Contoh Query & Hasil Pencarian
## Input User
> “Siapa saja siswa yang mendapatkan nilai A di kelas 108?”
## SQL Generated

```sql
SELECT nama
FROM siswa
WHERE nilai = 'A'
AND kelas = '108
```
# Tabel Hasil


| Nama	| Hasil Data |
| :--- | :---: | 
| Ribka |	Data ditemukan |
| Jennyka | Data ditemukan |

# Efisiensi & Dampak Operasional
Sistem ini meningkatkan efisiensi pengambilan data dan mengurangi ketergantungan pada tim teknis. Pengguna dapat mengakses data dengan lebih cepat, mudah, dan intuitif.


# Sesi Tanya Jawab
Terima kasih atas perhatiannya.
Silakan sampaikan pertanyaan mengenai arsitektur, keamanan, maupun implementasi sistem NL2SQL ini.


