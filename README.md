# Yetgim-Proje-




🎬 Film / Dizi Arşiv Sistemi (OOP Projesi)

↘️Proje Amacı

Bu proje, Python’da nesne yönelimli programlama (OOP) prensiplerini kullanarak bir Film/Dizi Arşiv Uygulaması geliştirmeyi amaçlar.
Kullanıcı, kendi film ve dizi arşivini oluşturabilir, arama yapabilir, medya öğelerine puan verebilir ve tüm verileri json formatında kalıcı olarak kaydedebilir . 

Kavram	Uygulamadaki Kullanımı
Sınıf (Class)	Film, Dizi, Yonetmen, Kullanici, Arsiv sınıfları oluşturuldu.
Kalıtım (Inheritance)	Film ve Dizi sınıfları, soyut sınıf Medya’dan türetildi.
Soyutlama (Abstraction)	Medya sınıfı bir abstract base class (ABC) olarak tasarlandı.
Kapsülleme (Encapsulation)	Puanlar _puanlar listesiyle korundu, erişim kontrollü yapıldı.
Polimorfizm (Polymorphism)	bilgileri_goster() metodu Film ve Dizi sınıflarında farklı şekilde çalışıyor.

↘️IMDb Tarzı Puanlama Sistemi Ekledik

Kullanıcılar her film ya da diziye 0 ile 10 arasında puan verebiliyor.
Bir medya nesnesine birden fazla puan verilebiliyor, sistem otomatik olarak ortalama puanı hesaplıyor.

📌def puan_ver(self, puan):
    if 0 <= puan <= 10:
        self._puanlar.append(puan)📌

↘️Ayrıca menüde en yüksek puanlı 5 medya görüntülenebiliyor:

🏆 En yüksek puanlı 5 medya:
1. Breaking Bad (2008) | Tür: Dram | Puan: 9.7/10
2. Inception (2010) | Tür: Bilim Kurgu | Puan: 9.5/10

↘️Veri Kaydı ve Kalıcılık Sağladık (JSON)

Projede arşivdeki tüm filmler/diziler bir dosyaya kaydediliyor.
Python’un json modülünü kullanarak nesneleri JSON formatına dönüştürdük ve sonradan tekrar nesnelere yükledik.

📌with open("arsiv.json", "w", encoding="utf-8") as f:
    json.dump(veri, f, ensure_ascii=False, indent=4)📌

🧚🏻‍♀️Bu sayede program kapanıp açılsa bile, tüm arşiv kayıtlı kalıyor.

↘️Kullanıcı Etkileşimi ve Menü Sistemi

↘️Konsol üzerinden basit ama işlevsel bir menü oluşturduk:

🎬 Film/Dizi Arşiv Sistemi
1. Yeni film ekle
2. Yeni dizi ekle
3. Arşivi listele
4. Başlığa göre ara
5. Medyaya puan ver
6. En yüksek puanlı 5 medya
7. Arşivi kaydet
8. Çıkış
Proje yapısı 

📌film_arsiv_projesi/
│
├── film_arsiv.py      # Ana Python kodu
├── arsiv.json          # Otomatik oluşturulan veri dosyası
└── README.md           # Proje açıklaması📌

↘️↘️Neler Kullandık ? 
Teknoloji	Kullanım Amacı
Python 3	Ana geliştirme dili
JSON	Veri saklama ve yükleme
ABC (abstract base class)	Soyutlama yapısı için
Colab / VS Code	Geliştirme ortamı

🧚🏻‍♀️Öğrenilen OOP Kavramları
	•	Sınıf ve nesne oluşturma
	•	Kalıtım ve soyut sınıflar
	•	Metot geçersiz kılma (override)
	•	Özel nitelikler ve kapsülleme
	•	JSON ile nesne-serileştirme (serialization)
	•	Kullanıcı etkileşimi ile dinamik veri yönetimi

🧚🏻‍♀️🧚🏻‍♀️Bu proje, OOP prensiplerini gerçek bir senaryo üzerinden öğretmek için ideal bir örnektir.
Kullanıcı dostu, modüler, geliştirilebilir bir yapı sunar.
Python’un soyut sınıf, kalıtım, kapsülleme gibi kavramlarını hem teorik hem de pratik olarak pekiştirmemizi sağlar.



