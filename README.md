# 🎓 Topkapı Öğrenci Asistanı

Topkapı Üniversitesi öğrencileri için özel olarak geliştirilmiş; ders programından sınav notlarına, yapay zeka destekli ders çalışma asistanından kampüs içi sosyal ağa kadar tüm akademik süreçleri tek bir çatı altında toplayan modern bir masaüstü uygulamasıdır[cite: 7].

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![CustomTkinter](https://img.shields.io/badge/UI-CustomTkinter-indigo)
![Supabase](https://img.shields.io/badge/Backend-Supabase-green)
![Sürüm](https://img.shields.io/badge/Sürüm-v1.2-orange)

---

## ✨ Öne Çıkan Özellikler

* **🏫 Otomatik OİS Entegrasyonu:** Öğrenci Bilgi Sistemi (OİS) ile tam senkronize çalışır[cite: 3]. Ders programınızı, sınav sonuçlarınızı ve OİS mesajlarınızı tek tıkla çeker[cite: 3, 7].
* **🔔 Akıllı Sınav Takibi:** Uygulama açıkken her 15 dakikada bir arka planda notları kontrol eder; yeni bir sınav sonucu açıklandığında sesli ve pencereli bildirim gönderir[cite: 7].
* **🤖 Yapay Zeka Destekli Çalışma Paneli (AI Study Buddy):** 
  * Ders türüne (*Sayısal, Sözel, Karma*) göre özel olarak uyarlanır[cite: 4, 6].
  * Yüklediğiniz ders PDF'lerini sayfa sayfa analiz eder, otomatik özet çıkarır[cite: 6].
  * Belgedeki önemli formülleri, LaTeX kodlarını ve kavramları derler[cite: 6].
  * PDF içerisinden anında geri bildirim veren çoktan seçmeli deneme sınavları (quiz) üretir[cite: 4, 6].
* **💬 Kampüs İçi İletişim & Sosyal Ağ:** Genel sohbet odası, bölümünüze özel grup sohbetleri ve öğrenciler arası birebir özel mesajlaşma (DM) altyapısı barındırır[cite: 5, 7].
* **🧮 Akademik Araçlar:** 
  * **Final Hesaplayıcı:** Vize notunuza ve ağırlığına göre hedeflediğiniz ortalamayı tutturmak için finalden kaç almanız gerektiğini hesaplar[cite: 7].
  * **Devamsızlık Takibi:** Okulun hafta sayısı ve devamsızlık yüzdesi kurallarına göre kalan haklarınızı otomatik takip eder[cite: 7].
* **☁️ Ortak Ders Kataloğu (Bulut Mimari):** Öğrenciler verilerini senkronize ettikçe bölümlere ait ders katalogları Supabase bulut veritabanında birleşir; aynı bölümdeki diğer arkadaşlarınız için güncel bir ders kütüphanesi oluşur[cite: 5, 7].
* **🚀 Güvenli Altyapı & Otomatik Güncelleme:** RLS (Row Level Security) tabanlı Supabase güvenliği[cite: 5], lisans anahtarı doğrulama sistemi[cite: 5] ve yeni sürümleri otomatik indirip kurabilen akıllı güncelleme yöneticisi[cite: 7] içerir.

---

## 🛠 Kullanılan Teknolojiler

* **Arayüz (UI):** `CustomTkinter`, `Tkinter`, `PIL (Pillow)`[cite: 7]
* **Ağ & Veri İşleme:** `Requests`, `BeautifulSoup4 (bs4)`, `PyMuPDF (fitz)`[cite: 3, 4]
* **Veritabanı & Backend:** `Supabase` (Auth, REST API, Edge Functions, RLS)[cite: 5, 6]
* **Asistan Motoru:** Özel PDF Parçalama, Threading ve Yapay Zeka Entegrasyonları[cite: 6]

---

## 🚀 Kullanım (Çalıştırma)

Ekstra hiçbir kurulum veya Python kütüphanesi yüklemeye gerek yoktur. 

1. **Releases** kısmından güncel `TopkapiAsistan.exe` dosyasını indirin.
2. Dosyaya çift tıklayarak doğrudan çalıştırın.
3. İlk açılışta Supabase bağlantı bilgileriniz otomatik tanınır veya ilk kurulum ekranından yapılandırılır[cite: 7].

---

## 📂 Dosya Yapısı

* `app.py` – Ana uygulama penceresi, yönlendiriciler, state yönetimi ve arayüz sayfaları[cite: 7].
* `ois.py` – OİS oturum yönetimi (Kelime Captcha çözme), ders programı ve sınav sonucu scraper modülü[cite: 3].
* `study.py` – PDF görüntüleyici, AI özetleri, formül listesi ve interaktif Quiz arayüzü[cite: 4].
* `supa.py` – Supabase veritabanı, kimlik doğrulama (Auth) ve RPC fonksiyon istemcisi[cite: 5].
* `ai.py` – PDF dosyalarını parçalara ayırarak Edge Function üzerinden yapay zekaya gönderme ve analiz motoru[cite: 6].
* `data.py` – Fakülte, bölüm ve statik ders listeleri[cite: 8].

---

## 🛡️ Lisans & Güvenlik
Bu proje Topkapı Üniversitesi öğrencilerine özel olarak tasarlanmıştır[cite: 7]. OİS şifreleriniz hiçbir şekilde veritabanında saklanmaz; yalnızca anlık OİS oturum doğrulaması için kullanılır[cite: 7].
