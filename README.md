# Big Five Personality Assessment Using KNN Method with RoBERTA
Kepribadian dipahami sebagai keadaan pikiran individu yang bergantung pada perilaku, emosi, dan sikap seperti perbedaan karakteristik setiap orang. Kepribadian juga sering diartikan sebagai kualitas yang membedakan individu. Kepribadian Big Five dianggap sebagai cara yang efektif untuk mengetahui kepribadian seseorang karena lebih informatif. Big Five sering disingkat dengan model “OCEAN”, Openness, Conscientiousness, Extraversion, Agreeableness, dan Neuroticism. Secara umum seseorang merespons dan berinteraksi dengan orang lain juga dapat dilihat dari kepribadiannya. Pada media sosial yang telah diciptakan untuk membantu masyarakat berkomunikasi jarak jauh dan mudah.  Fokus penelitian ini menyajikan analisis perilaku pengguna Twitter yang dapat digunakan untuk memprediksi kepribadian Big Five Personality dengan menggunakan metode KNN. Aspek penting yang perlu diperhatikan dalam menggunakan metode ini yaitu keakuratan dalam mengklasifikasikan Lima Besar Kepribadian. Penggunaan K-Nearest Neighbor (KNN) merupakan metode pengklasifikasian objek berdasarkan data latih terdekatnya. Untuk mengatasi ketidakseimbangan data pada data pelatihan, kami menggunakan K-Means SMOTE (Synthetic Minority Oversampling Technique). Fitur lain seperti LIWC (Linguistic Inquiry Word Count), Information Gain, Robustly Optimized BERT Approach (RoBERTa), dan hyperparameter tuning dapat meningkatkan performa sistem yang kami bangun. 

## K-Nearest Neighbor (KNN)
 K-Nearest Neighbor (KNN) merupakan algoritma yang mengklasifikasikannya berdasarkan jarak terdekat [3], [10]. Pengklasifikasi K- Nearest Neighbor biasanya didasarkan pada jarak Euclidean antara sampel uji dan sampel pelatihan yang ditentukan. Tetangga terdekat k ditentukan di bawah ini,

<img width="214" alt="KNN" src="https://github.com/athirahrifdha/Big-Five-Personality-Assessment-Using-KNN-Method-with-RoBERTA/assets/139842516/cd91c811-8745-4b78-88d8-b3a174e51d15">

Pada rumus yang ada di atas, 𝑞𝑖 adalah data yang atributnya telah dinormalisasi dan 𝑃 adalah data uji baru di atas data latih.

## Robustly Optimized BERT Approach (RoBERTA)
RoBERTA mengandalkan strategi penyembunyian bahasa BERT, untuk memprediksi bagian teks yang sengaja disembunyikan dalam sampel Bahasa yang tidak diklasifikasikan. RoBERTa mendapatkan peningkatan kinerja yang signifikan dengan menggunakan arsitektur BERT dan proses pelatihan. RoBERTa memiliki tujuan untuk meningkatkan model pelatihan BERT. RoBERTa memeiliki kinerja yang sebanding dengan kinerja semua metode BERT sebelumnya.

## Information Gain (IG) 
Information Gain (IG) adalah metodologi analisis kepraktisan berbasis entropi asosiasi yang banyak digunakan dalam pembelajaran mesin. Hasil perolehan data digunakan dalam pemilihan fitur, hal ini ditentukan karena banyaknya data yang disediakan oleh fitur untuk kategori teks. Pengumpulan data dihitung berdasarkan jumlah istilah yang akan digunakan untuk mengklasifikasikan pengetahuan, untuk mengukur pentingnya bagian leksikal untuk klasifikasi. Persamaan perolehan informasi disajikan di bawah ini,

<img width="271" alt="InformationGain" src="https://github.com/athirahrifdha/Big-Five-Personality-Assessment-Using-KNN-Method-with-RoBERTA/assets/139842516/d06e9f32-3e7e-46e2-aea8-e2a3ccd2597c">

Di Rumus di atas, C adalah kumpulan dokumen yang tidak memiliki fungsi t. S(c) adalah entropi seluruh fungsi c (sebelum pemisahan), S (cj) adalah entropi fungsi c untuk kelas t = j (pasca pemisahan), nilai (t) adalah himpunan nilai yang mungkin untuk kelas t, n adalah banyaknya nilai potensial untuk kelas t, yaitu. Paling bermanfaat untuk klasifikasi C. |cj| adalah banyaknya kelas sampel yang nilainya = j, |c| adalah jumlah sampel untuk setiap kelas. Kasus S(c) dirumuskan sebagai berikut,

<img width="215" alt="InformationGain2" src="https://github.com/athirahrifdha/Big-Five-Personality-Assessment-Using-KNN-Method-with-RoBERTA/assets/139842516/50331999-a79c-4fb4-b461-adb75cebc3c2">

Dalam Rumus di atas, p(ci) adalah probabilitas karakteristik i dan m adalah jumlah maksimum karakteristik.

## KMeans SMOTE
Teknik lain dalam kelas teknik aksentuasi wilayah kategori tertentu menggunakan k-means untuk mengelompokkan kelas minoritas sebelum menerapkan SMOTE di antara cluster yang ditemukan. Tujuan yang diungkapkan dari teknik ini adalah untuk meningkatkan wilayah kategori dengan mengambil sampel di antara kelompok-kelompok kategori minoritas yang ada. Metode pengambilan sampel K-Means SMOTE digunakan untuk menyeimbangkan kasus kelas positif dan negatif. Sebagai perbandingan, metode pengambilan sampel awal, SMOTE dan K-Means SMOTE diterapkan pada langkah pra-pemrosesan.

## Linguistic Inquiry Word Count
Linguistic Inquiry Word Count (LIWC) merupakan salah satu metode untuk menganalisia kata sesuai dengan kelasnya. Pennebaker telah dikembangkan ke dalam LIWC sejak tahun 2007. LIWC memiliki dua karakteristik, yaitu kosa kata terbuka dan tertutup. Pertunjukan kosakata tertutup siap untuk meneliti korelasi antara bahasa dan variabel psikologis. Tabel 2 menunjukkan skor korelasi antara kelas LIWC dan Big Five Personality yang dikembangkan pada analisis sebelumnya. Kinerja kosakata tertutup ditentukan oleh kelas kumpulan kata menggunakan LIWC yang memiliki nilai korelasi signifikan. Kosakata tersebut dikumpulkan di situs resmi LIWC dengan cara menerjemahkan kosakata tersebut ke dalam bahasa Indonesia yang baik.

## Hyperparameter
Cara tradisional untuk melakukan optimasi hyperparameter adalah pencarian grid. Ini hanya mengeksplorasi secara mendalam subset tertentu dari ruang hyperparameter Λ dari algoritma pembelajaran A. Algoritme pencarian teralis biasanya perlu dipandu oleh metrik kinerja yang diukur dengan validasi timbal balik dari set pelatihan.

## Evalution Score
Pada proses terakhir ini skor ini terdiri dari akurasi, skor F1, presisi, dan recall. Akurasi digunakan untuk mengukur rasio positif palsu terhadap nilai akurasi dan digunakan untuk mengukur rasio koreksi model secara keseluruhan. Skor F1 adalah kombinasi presisi dan perolehan untuk ukuran akurasi model secara keseluruhan. Presisi digunakan untuk mengukur rasio positif palsu terhadap nilai akurasi. Penarikan kembali digunakan untuk mengukur rasio positif sebenarnya terhadap nilai presisi. Evaluasi kinerja dilakukan oleh metrik evaluasi rekanan yang menggunakan Confusion Matrix. True Positive (TP), True Negative  (TN), False Positive (FP), dan False Negative (FN) merupakan unit area dari empat kelas Confusion Matrix

## Kesimpulan
Dalam penelitian ini, kami menggabungkan K-Means SMOTE, LIWC, dan RoBERTa sebagai pendekatan semantik untuk memprediksi kepribadian Big Five pengguna Twitter menggunakan metode K-nearest neighbour. Hasil kinerja sistem sesuai untuk dataset pengguna Twitter sebanyak 328 data dan data tweet sebanyak 672.866 data. Menerapkan pendekatan semantik adalah kunci untuk meningkatkan kinerja sistem.
Data tersebut dapat dikatakan tidak seimbang karena terdapat label yang dominan sehingga harus dilakukan penyeimbangan data. Untuk mengatasi ketidakseimbangan data, kami menerapkan metode K-Means SMOTE. Selain itu, kami juga menyertakan LIWC sebagai fitur bahasa, RoBERTa sebagai pendekatan semantik, dan menggunakan penyetelan hyperparameter untuk meningkatkan akurasi model. Hasil dari penelitian ini, nilai akurasi yang diperoleh sebesar 72,82% dengan peningkatan sebesar 95,28% dari Baseline Accuracy.
Pada skenario pertama dan kedua menggunakan fitur linguistik LIWC, dan K-Means SMOTE untuk mengolah data yang tidak seimbang, namun perlu diketahui bahwa keakuratan metode ini sangat rendah. Namun pada skenario ketiga, model Roberts merupakan improvisasi dari model BERT miliknya, sehingga pendekatan semantik tampaknya memiliki dampak yang lebih besar terhadap kinerja. Jadi, hasilnya lebih kuat, dan performa sistemnya lebih baik. Penyetelan hyperparameter juga meningkatkan akurasi, karena akurasi dapat ditingkatkan dengan menyediakan parameter optimal untuk diterapkan dalam metode. Kumpulan data yang kami kumpulkan mencakup 320 pengguna Twitter. Dengan jumlah pengguna sebanyak ini, ukuran dataset cukup kecil untuk membuat prediksi, hal ini menjadi keterbatasan penelitian ini.










