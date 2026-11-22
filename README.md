# Prediksi Kategori Sleep Debt

Notebook ini mengklasifikasikan `sleep_debt_category` menggunakan Ordinal Logistic Regression dan Decision Tree Classification. Notebook menggunakan file dataset yang disertakan dalam folder ini.

## Isi folder

1. `main.ipynb` - notebook pemeriksaan, preprocessing, pelatihan, dan evaluasi model.
2. `bedtime_screentime_sleep_debt.csv` - dataset kebiasaan penggunaan smartphone malam hari dan kondisi tidur.

## Menjalankan notebook

1. Buka `main.ipynb` menggunakan Jupyter Notebook, JupyterLab, atau Google Colab.
2. Pastikan pustaka `pandas`, `numpy`, `scikit-learn`, `statsmodels`, dan `matplotlib` tersedia.
3. Jalankan seluruh cell secara berurutan.

Notebook membagi data dengan `random_state=42` dan stratifikasi target. Imputasi, scaling, serta encoding di-fit hanya pada data training. Evaluasi memakai Accuracy, Precision Macro, Recall Macro, Macro-F1, dan Confusion Matrix.

## Target dan fitur

Target adalah `sleep_debt_category` dengan urutan `Optimal Recovery`, `Mild Deficit`, `Moderate Debt`, dan `Severe Sleep Debt`. Kolom `user_id` dan fitur yang berpotensi membocorkan target, seperti `total_sleep_hours`, sleep latency, persentase tidur, snooze alarm, dan kelelahan hari berikutnya, tidak digunakan sebagai prediktor.

Analisis ini bersifat prediktif dan tidak membuktikan hubungan sebab-akibat. Ablation Study belum termasuk dalam notebook ini.
