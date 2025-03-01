# Perbandingan-Model-Transformer-Dalam-Analisis-Sentimen-Bahasa-Indonesia

link dataset [link](https://drive.google.com/drive/folders/1VBZaX9FTjxIJccktBXgd_H2xg9VShPbO?usp=sharing)

# Training History Indobert
<img width="180" alt="image" src="https://github.com/user-attachments/assets/7ff75b9c-4bcb-42fe-a1ae-cbf71ffd1c56" />

Hasil pelatihan model IndoBERT menunjukkan peningkatan kinerja seiring bertambahnya epoch. Pada epoch pertama, akurasi validasi mencapai 87%, dengan F1-score 82%, menandakan model sudah cukup baik dalam membedakan sentimen. Seiring pelatihan, train loss terus menurun dari 0.4404 ke 0.1771, sementara akurasi pelatihan meningkat hingga 94%, menunjukkan model semakin memahami pola dalam data. Namun, valid loss stagnan di sekitar 0.31–0.32, dengan akurasi validasi berkisar 88–89%, yang mengindikasikan bahwa model mungkin mulai mengalami overfitting setelah beberapa epoch terakhir. Meskipun begitu, dengan F1-score validasi mencapai 86%, model tetap menunjukkan performa yang kuat untuk tugas analisis sentimen. 
<img width="229" alt="image" src="https://github.com/user-attachments/assets/9eaee4c1-1379-42f7-915d-df74d3ab9689" />
<img width="267" alt="image" src="https://github.com/user-attachments/assets/213eccb5-65ce-4941-9618-7871d368f990" />

Evaluasi model IndoBERT menunjukkan kinerja yang baik dengan akurasi 89%, mencerminkan kemampuan model dalam mengklasifikasikan teks secara efektif. Label "neutral" memiliki performa terbaik dengan F1-score 0.93, menunjukkan keseimbangan antara precision (0.92) dan recall (0.94). Label "positive" dan "negative" memiliki F1-score 0.83 dan 0.81, dengan recall label "positive" (0.79) lebih rendah dibanding precision-nya (0.86), yang bisa mengindikasikan model cenderung melewatkan beberapa sampel positif. Macro average F1-score 0.86 menunjukkan keseimbangan antar kelas, sementara weighted average 0.89 mengonfirmasi bahwa model bekerja baik secara keseluruhan. Untuk peningkatan, dapat dilakukan penyesuaian data balancing atau fine-tuning pada kelas yang memiliki recall lebih rendah.![image](https://github.com/user-attachments/assets/8f5c6d33-33c7-4ed6-b4c1-d8a051a2f877)




# Training History RoBERTa
<img width="194" alt="image" src="https://github.com/user-attachments/assets/d78e3178-b21e-42f2-ad6c-20095089f8dc" />

Model RoBERTa menunjukkan tren peningkatan performa selama lima epoch pelatihan, dengan penurunan bertahap dalam train loss dari 0.3535 ke 0.2055, yang mencerminkan perbaikan dalam pemahaman data. Akurasi meningkat secara konsisten dari 89% pada epoch pertama menjadi 93% pada epoch kelima, sementara skor F1 juga meningkat dari 0.84 ke 0.91, menunjukkan keseimbangan antara presisi dan recall yang baik. Meskipun valid loss cenderung stagnan sekitar 0.26-0.27, akurasi validasi tetap stabil di 91%, menunjukkan bahwa model berhasil menggeneralisasi dengan baik tanpa tanda-tanda overfitting yang signifikan.
<img width="213" alt="image" src="https://github.com/user-attachments/assets/a393532d-0b35-4c8e-bfd2-25c42e5c3b70" />
<img width="274" alt="image" src="https://github.com/user-attachments/assets/1ee045d2-3a39-43f8-b98e-07fd21e89984" />

Evaluasi model RoBERTa menunjukkan akurasi 91%, yang sedikit lebih tinggi dibandingkan model IndoBERT sebelumnya. Label "neutral" memiliki performa terbaik dengan F1-score 0.94, berkat precision (0.92) dan recall (0.97) yang tinggi, menunjukkan bahwa model sangat baik dalam mengenali teks netral. Label "positive" dan "negative" memiliki F1-score masing-masing 0.83 dan 0.86, dengan recall untuk "positive" masih lebih rendah (0.79), yang mengindikasikan potensi underfitting pada kelas ini. Macro average F1-score 0.88 menunjukkan distribusi performa yang relatif merata di semua kelas, sedangkan weighted average 0.91 menegaskan kinerja model yang solid secara keseluruhan. Model ini lebih seimbang dibanding IndoBERT, tetapi perbaikan bisa difokuskan pada meningkatkan recall kelas "positive" agar lebih selaras dengan precision-nya.![image](https://github.com/user-attachments/assets/7bf1d4f4-9ae5-496c-8aeb-91d54f0c3e0b)




# Training History XLM RoBERTa

<img width="178" alt="image" src="https://github.com/user-attachments/assets/b61a9c5f-2a95-44e5-b925-0cbf80ff170b" />

Model XLM-RoBERTa menunjukkan peningkatan performa yang signifikan selama 5 epoch pelatihan. Train Loss berkurang dari 0.6451 di Epoch 1 menjadi 0.2263 di Epoch 5, sementara akurasi meningkat dari 75% menjadi 92%, dengan skor F1 yang juga meningkat dari 0.66 menjadi 0.90. Hal ini menunjukkan bahwa model semakin mampu memahami dan membedakan pola dalam data pelatihan. Di sisi validasi, meskipun Valid Loss sedikit fluktuatif, akurasi tetap stabil di sekitar 89-90%, dan skor F1 tetap di angka 0.86-0.87, menunjukkan bahwa model sudah mencapai performa yang sangat baik setelah beberapa epoch. Namun, stabilitas ini bisa mengindikasikan potensi overfitting, di mana model sudah mencapai puncaknya pada data validasi dan tidak menunjukkan peningkatan lebih lanjut.
Untuk menghindari overfitting, sebaiknya dilakukan early stopping setelah Epoch 3 atau 4, karena performa validasi sudah cukup stabil. Selain itu, eksperimen dengan learning rate decay bisa dicoba untuk meningkatkan generalisasi model, mengingat learning rate tetap konstan pada 3e-6 sepanjang pelatihan. Penambahan data melalui data augmentation atau teknik lain juga bisa membantu model dalam mempertahankan performa yang optimal pada data yang belum pernah dilihat sebelumnya. Secara keseluruhan, model XLM-RoBERTa telah menunjukkan hasil yang sangat baik, namun perlu beberapa penyesuaian untuk menjaga kinerjanya pada data validasi.

<img width="226" alt="image" src="https://github.com/user-attachments/assets/a7373f16-5954-4d56-be20-46e50dce839d" />
<img width="280" alt="image" src="https://github.com/user-attachments/assets/b9e93a06-89fb-4513-adc6-171fdf472ef3" />

Evaluasi model XLM-RoBERTa menunjukkan akurasi 90%, yang cukup kompetitif dengan model sebelumnya. Label "neutral" memiliki performa terbaik dengan F1-score 0.94, didukung oleh precision (0.94) dan recall (0.93) yang seimbang, menunjukkan kemampuan model dalam mengklasifikasikan teks netral dengan baik. Label "positive" memiliki F1-score 0.84 dengan recall (0.85) yang lebih tinggi dibanding precision (0.83), mengindikasikan model sedikit lebih baik dalam menangkap teks positif meskipun ada kemungkinan beberapa false positives. Label "negative" memiliki F1-score 0.81, dengan precision dan recall yang seimbang, menunjukkan performa yang stabil namun masih lebih rendah dibanding kelas lain. Macro average F1-score 0.86 mengindikasikan performa merata di semua kelas, sedangkan weighted average 0.90 menegaskan kestabilan model secara keseluruhan. Model ini menunjukkan keseimbangan antara precision dan recall, tetapi bisa ditingkatkan dengan memperbaiki deteksi kelas "negative" agar lebih akurat.





