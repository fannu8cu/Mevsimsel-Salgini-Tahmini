# Mevsimsel Hastaliklar Icin Erken Uyari Sistemi Prototipi

Bu proje, halka acik Google Trends arama verileri ve gecmis hava durumu verilerini kullanarak Turkiye'deki mevsimsel hastalik salginlari icin bir erken uyari sistemi prototipi gelistirmeyi amaclamaktadir. Proje, bir veri bilimi projesinin veri toplama, temizleme, kesifsel analiz, ozellik muhendisligi ve makine ogrenmesi modellemesi gibi tum adimlarini kapsamaktadir.

---

### Onemli Bulgular

Projenin en dikkat cekici bulgusu, haftalik ortalama sicaklik ile 'oksuruk' aramalari arasindaki guclu negatif korelasyondur (-0.50). Bu, hava sogudukca insanlarin hastalik belirtilerini aratma egiliminin belirgin sekilde arttigini gorsel ve istatistiksel olarak kanitlamaktadir.


<img width="1690" height="690" alt="öksürük_grafik" src="https://github.com/user-attachments/assets/0c2a0441-946d-4131-a10c-bc9b164263c9" />

---

### Kullanilan Teknolojiler (Technologies Used)

- **Programlama Dili:** Python 3
- **Kutuphaneler:** Pandas, Seaborn, Matplotlib, Scikit-learn
- **Veri Kaynaklari:** Google Trends (Manuel Indirme), Open-Meteo API

---

### Proje Akisi ve Metodoloji

Proje, asagidaki adimlar izlenerek tamamlanmistir:
1.  **Veri Toplama:** Google Trends'ten `.csv` dosyasi ve Open-Meteo API'sinden hava durumu verileri cekildi.
2.  **Veri Temizleme:** Iki veri seti birlestirildi, eksik veriler temizlendi ve zamanla hizalama saglandi.
3.  **Kesifsel Veri Analizi:** Degiskenler arasi iliskileri anlamak icin korelasyon matrisi ve zaman serisi grafikleri olusturuldu.
4.  **Ozellik Muhendisligi:** Problem, "salgin" donemlerini istatistiksel olarak etiketleyerek bir siniflandirma problemine donusturuldu.
5.  **Modelleme:** Gelecek haftanin salgin riskini tahmin etmek icin bir Lojistik Regresyon modeli kuruldu.

---

### Model Performansi

Kurulan modelin test verisi uzerindeki performansi oldukca basarilidir:
- **Duyarlilik (Recall):** Model, gercek salgin haftalarinin **%86'sini** basariyla tespit edebilmektedir.
- **Kesinlik (Precision):** Modelin verdigi "Salgin Var" alarmlarinin **%67'si** isabetlidir.

<img width="530" height="455" alt="karmasiklik_matrisi" src="https://github.com/user-attachments/assets/20a658e0-0231-488b-b76b-eb093c8e1d93" />


---

### Kurulum ve Calistirma (Installation & Usage)

Projeyi kendi bilgisayarinizda calistirmak icin:
1.  Bu repository'yi klonlayin.
2.  Gerekli kutuphaneleri `pip install pandas seaborn matplotlib scikit-learn` komutu ile yukleyin.
3.  `Hava_Durumu_ve_Mevsimsel_Salgin_Analizi.ipynb` dosyasini bir Jupyter ortaminda acin ve hucreleri sirayla calistirin.

---

### Gelecek Gelistirmeler (Future Improvements)

- Daha karmasik siniflandirma modelleri (Random Forest, XGBoost) denenerek performans artisi hedeflenebilir.
- Modele daha fazla ozellik eklenebilir.
- Farkli sehirlerin hava durumu verileriyle bolgesel modeller olusturulabilir.
