# Water Quality Classification

Project ini bertujuan untuk mengklasifikasikan kualitas air menjadi dua kategori, yaitu **Good** dan **Not Good**, berdasarkan parameter fisik dan kimia air seperti pH, Dissolved Oxygen (DO), Turbidity, dan Conductivity.

Dataset yang digunakan berasal dari Kaggle (Water Quality Testing). Karena dataset tidak memiliki label kualitas air secara langsung, label dibuat menggunakan aturan (rule-based labeling) berdasarkan standar umum kualitas air.

## Methods
Beberapa tahapan yang dilakukan dalam project ini meliputi:
- Data cleaning dan preprocessing (rename kolom, menghapus kolom yang tidak digunakan, dan menghapus data duplikat).
- Exploratory Data Analysis (EDA) menggunakan histogram, heatmap korelasi, dan boxplot.
- Pembuatan label kualitas air (Good/Not Good) berdasarkan threshold tertentu.
- Pembagian data menjadi data latih (80%) dan data uji (20%).
- Pelatihan model menggunakan Logistic Regression dan Random Forest.

## Model Evaluation
Evaluasi model dilakukan menggunakan metrik **F1-score**, karena distribusi kelas pada dataset tidak seimbang (jumlah data Good dan Not Good berbeda).  
Hasil evaluasi menunjukkan bahwa **Random Forest** memberikan performa yang lebih baik dibandingkan **Logistic Regression** dalam mengklasifikasikan kualitas air.

## Feature Importance
Berdasarkan analisis feature importance dari model Random Forest, fitur yang paling berpengaruh terhadap prediksi kualitas air adalah **Turbidity**, **pH**, dan **Dissolved Oxygen (DO)**.

## Conclusion
Project ini menunjukkan bahwa parameter fisik dan kimia air dapat digunakan untuk memprediksi kualitas air menggunakan metode machine learning sederhana.  
Meskipun hasilnya cukup baik, project ini masih memiliki keterbatasan karena jumlah data terbatas dan belum dilakukan optimasi hyperparameter secara mendalam.

## Future Work
Project ini masih dapat dikembangkan lebih lanjut dengan:
- Melakukan hyperparameter tuning pada model.
- Menambahkan algoritma lain seperti SVM atau XGBoost.
- Menggunakan dataset yang lebih besar dan beragam.
- Mengimplementasikan model ke dalam aplikasi sederhana (web atau desktop).
