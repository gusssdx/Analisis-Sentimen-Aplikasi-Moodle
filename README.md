# ANALISIS SENTIMEN TERHADAP REVIEW APLIKASI MOODLE DI GOOGLE PLAY STORE MENGGUNAKAN KLASIFIKASI NAIVE BAYES
Moodle merupakan aplikasi LMS yang populer di google play store, Projek ini melakukan analisis sentiment terhadap review atau ulasan di aplikasi
Moodle menggunakan algoritma multinomial naive bayes, tujuan penelitian ini untuk mengklasifikasi komentar positif dan negatif dari review pengguna Moodle.

## Tahapan Projek
- Scrapping data : untuk Scrapping data review aplikasi Moodle menggunakan library google_play_scraper, jumlah data yang diambil berjumlah 2500.
- Case folding : mengubah seluruh huruf yang ada pada dokumen menjadi lower case semua ataupun upper case semua.
- Pembersihan karakter : Pembersihan karakter pada dokumen ini mencangkup penghapusan angka, tanda baca, emoji, menghapus karakter dan simbol simbol yang tidak diperlukan dalam pemrosesan nantinya
- Word Normalization : proses mengubah kata tidak baku atau non standar menjadi kata baku dari kumpulan slangwords yang tersedia.
- Tokenization : membagi teks menjadi token-token atau bagian-bagian untuk memecah kalimat menjadi kepingan kata, contoh kalimat “aplikasinya bagus sekali”, menjadi “aplikasinya”,”bagus”,”sekali”.
- Stop-word removal : penghapusan kata yang tidak bermakna, seperti kata penghubung dan, yang, bisa, dalam , dan lain-lain.
- Stemming : proses yang digunakan dalam text mining untuk mengubah kata-kata dalam dokumen menjadi bentuk dasarnya. Seperti menghapus imbuhan yang ada dalam sebuah kata.
- Labeling : membuat variabel baru untuk menjadi variable pengawas, parameter dalam pemberian label adalah dari jumlah rating, apabila ratingnya 1 - 3 maka diberi label negatif dan jika ratingnya 4 - 5 maka diberi label positif.
- Pembobotan TF-IDF : TF-IDF (Term Frequency-Inverse Document Frequency) adalah suatu metode yang digunakan dalam pemrosesan teks dan pengelompokan dokumen. Fungsi utamanya adalah untuk memberikan bobot (weight) pada setiap kata dalam suatu dokumen, yang mencerminkan seberapa penting kata tersebut
- EDA : melihat gambaran awal data review seperti apa
- Split data : splitting data menggunakan library train_test_split dengan perbandingan 80% untuk data training dan 20% untuk data testing dan random_state = 40.
- Membuat model Naive bayes : Membuat model klasifikasi dengan algoritma Multinominal Naive Bayes, dan membuat model untuk data training dan data testing. Dimana training model dengan variabel X_train dan y_train disimpan pada variable clf.  Lalu data training digunakan untuk memprediksi label pada data testing.
- Evaluasi model : Hasil dari evaluasi model yang di dapatkan dari algoritma Multinominal naive bayes adalah 406 untuk hasil prediksi benar dan 94 untuk hasil prediksi  yang salah, total data prediksi yaitu 500.
  
  
