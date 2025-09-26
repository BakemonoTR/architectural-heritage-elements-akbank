# architectural-heritage-elements-akbank
Akbank Derin Öğrenme Bootcamp'i için CNN ile architectural-heritage-elements veri seti

<br/>
<div align="center">
  <h1 align="center">Akbank Derin Öğrenme Bootcamp - Mimari Miras Öğeleri Sınıflandırma</h1>
</div>

<p align="center">
  Bu proje, Akbank Derin Öğrenme Bootcamp'i kapsamında geliştirilmiş olup, mimari yapı elemanlarını derin öğrenme teknikleri kullanarak sınıflandırmayı amaçlamaktadır.
</p>

<div align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white" alt="TensorFlow">
  <img src="https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white" alt="Kaggle">
  <img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License">
</div>

<br>

<div align="center">
  <strong><a href="[https://www.kaggle.com/code/envercanbickin/akbank-derin-renme-bootcamp]">» Kaggle Notebook'u Görüntüle «</a></strong>
</div>

<br>

<details>
  <summary>İçindekiler</summary>
  <ol>
    <li><a href="#proje-hakkında">Proje Hakkında</a></li>
    <li><a href="#veri-seti">Veri Seti</a></li>
    <li><a href="#kullanılan-yöntemler-ve-teknolojiler">Kullanılan Yöntemler ve Teknolojiler</a></li>
    <li><a href="#elde-edilen-sonuçlar">Elde Edilen Sonuçlar</a></li>
    <li><a href="#kurulum-ve-kullanım">Kurulum ve Kullanım</a></li>
    <li><a href="#lisans">Lisans</a></li>
    <li><a href="#iletişim">İletişim</a></li>
  </ol>
</details>

---

## Proje Hakkında

Bu proje, **Akbank Derin Öğrenme Bootcamp: Yeni Nesil Proje Kampı**'nın bir parçası olarak gerçekleştirilmiştir. Projenin temel amacı, verilen bir mimari yapı elemanının görselinden yola çıkarak bu elemanın hangi sınıfa (örneğin kubbe, sütun, kemer vb.) ait olduğunu tespit eden bir Evrişimli Sinir Ağı (CNN) modeli geliştirmektir.


## Veri Seti

Projede, Kaggle üzerinde halka açık olarak yayınlanan **"Architectural Heritage Elements"** veri seti kullanılmıştır.

* **Veri Seti Linki:** [https://www.kaggle.com/datasets/xhlulu/archi-heritage-elements](https://www.kaggle.com/datasets/xhlulu/archi-heritage-elements)
* **İçerik:** Veri seti, 10 farklı mimari eleman sınıfından oluşmaktadır.
* **Boyut:** Toplamda yaklaşık 15,000 adet renkli görsel içermektedir.
* **Sınıflar:** `Altar`, `Apse`, `Bell Tower`, `Column`, `Dome`, `Gargoyle`, `Stained Glass`, `Vault`, `Flying Buttress`, `Tympanum`.

## Kullanılan Yöntemler ve Teknolojiler

Proje, baştan sona Kaggle Notebooks ortamında geliştirilmiştir. Süreç boyunca kullanılan ana kütüphaneler ve yöntemler aşağıda listelenmiştir.

**Teknolojiler:**
* Python 3
* TensorFlow & Keras
* Scikit-learn
* NumPy
* Pandas
* Matplotlib & Seaborn

**Metodoloji:**
1.  **Veri Ön İşleme:** Görüntüler, `150x150` piksel boyutuna getirildi. Veri seti, `ImageDataGenerator` kullanılarak eğitim, doğrulama ve test setlerine ayrıldı.
2.  **Veri Çoğaltma (Data Augmentation):** Modelin genelleme yeteneğini artırmak amacıyla eğitim verilerine rastgele döndürme, yakınlaştırma, kaydırma ve yatay çevirme gibi işlemler uygulandı.
3.  **Model Eğitimi:** Model, `Adam` optimizer ve düşük bir öğrenme oranı ile derlendi. Aşırı öğrenmeyi engellemek için `EarlyStopping` tekniği kullanıldı.
4.  **Model Değerlendirme:** Modelin performansı; doğruluk/kayıp grafikleri, sınıflandırma raporu ve karmaşıklık matrisi gibi metriklerle analiz edildi.
5.  **Yorumlanabilirlik (Interpretability):** Modelin bir tahminde bulunurken görüntünün hangi bölgelerine odaklandığını anlamak için **Eigen-CAM** ile ısı haritaları oluşturuldu.

## Elde Edilen Sonuçlar

Transfer öğrenme yaklaşımı sayesinde, model test seti üzerinde **~%75** gibi bir doğruluk oranına ulaşmıştır.

Eigen-CAM ile yapılan analizler, modelin doğru sınıflandırma yaparken ilgili mimari öğenin kendisine odaklandığını görsel olarak kanıtlamaktadır.

<br>

## Kurulum ve Kullanım

Bu projenin tamamı bir Kaggle Notebook'u üzerinde çalışmaktadır. Modeli çalıştırmak veya sonuçları yeniden üretmek için aşağıdaki adımları izleyebilirsiniz:

1.  Yukarıda verilen **[Kaggle Notebook linkine]([https://www.kaggle.com/code/envercanbickin/akbank-derin-renme-bootcamp])** gidin.
2.  Notebook'u kendi Kaggle hesabınıza kopyalamak için sağ üstteki "Copy and Edit" butonuna tıklayın.
3.  Eğitim sürecini hızlandırmak için sağdaki menüden "Settings > Accelerator > GPU" seçeneğini aktif ettiğinizden emin olun.
4.  "Run All" komutu ile tüm hücreleri çalıştırarak projenin baştan sona çalışmasını izleyebilirsiniz.


## İletişim

**[Enver Can Biçkin]** - [https://www.linkedin.com/in/envercanbickin/]


