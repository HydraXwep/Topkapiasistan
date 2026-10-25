# 🎓 Topkapı Öğrenci Asistanı

Topkapı Üniversitesi öğrencileri için özel olarak geliştirilmiş; ders programından sınav notlarına, yapay zeka destekli ders çalışma asistanından kampüs içi sosyal ağa kadar tüm akademik süreçleri tek bir çatı altında toplayan modern bir masaüstü uygulamasıdır.

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![CustomTkinter](https://img.shields.io/badge/UI-CustomTkinter-indigo)
![Supabase](https://img.shields.io/badge/Backend-Supabase-green)
![Sürüm](https://img.shields.io/badge/Sürüm-v2.2-orange)

---

## ✨ Öne Çıkan Özellikler

* **🏫 Otomatik OİS Entegrasyonu:** Öğrenci Bilgi Sistemi (OİS) ile senkronize çalışır. Ders programınızı, sınav sonuçlarınızı ve OİS mesajlarınızı tek tıkla çeker.
* **🔔 Akıllı Sınav Takibi:** Uygulama açıkken her 15 dakikada bir arka planda notları kontrol eder; yeni bir sınav sonucu açıklandığında bildirim gönderir.
* **🤖 Yapay Zekâ Destekli Çalışma Paneli:**
  * Ders türüne (*Sayısal, Sözel, Karma*) göre uyarlanır.
  * Yüklediğiniz ders PDF'lerini sayfa sayfa analiz eder, otomatik özet çıkarır.
  * Belgedeki önemli formülleri, LaTeX kodlarını ve kavramları derler.
  * PDF içeriğinden çoktan seçmeli deneme soruları üretir.
  * Analiz aynı anda birden fazla parçayı işler, böylece daha hızlıdır.
* **💬 Yapay Zekâ Sohbet:** Derslerinle ilgili sorularını sorabileceğin sohbet sayfası. Günlük kullanım hakkın ana ekranda görünür.
* **📊 GNO & Sınavlar ve Deneme Sınavı:** Ortalama hesaplama ve kendini sınama araçları.
* **💬 Kampüs İçi İletişim:** Genel sohbet odası, bölümünüze özel grup sohbetleri ve birebir özel mesajlaşma. Kişilerin yanında **çevrimiçi / son görülme** durumu görünür; istersen Ayarlar'dan durumunu gizleyebilirsin.
* **🧮 Akademik Araçlar:**
  * **Final Hesaplayıcı:** Vize notunuza ve ağırlığına göre hedeflediğiniz ortalamayı tutturmak için finalden kaç almanız gerektiğini hesaplar.
  * **Devamsızlık Takibi:** Hafta sayısı ve devamsızlık yüzdesi kurallarına göre kalan haklarınızı otomatik takip eder.
* **☁️ Ortak Ders Kataloğu:** Öğrenciler verilerini senkronize ettikçe bölümlere ait ders katalogları Supabase bulut veritabanında birleşir; aynı bölümdeki arkadaşlarınız için güncel bir ders kütüphanesi oluşur.
* **🔑 Beni Hatırla:** Giriş ekranındaki kutucuğu işaretlersen uygulamayı her açtığında şifre yazmana gerek kalmaz. Şifren hiçbir yerde saklanmaz; yalnızca Windows tarafından şifrelenen oturum anahtarı tutulur. Çıkış yapınca silinir.
* **🎨 Kişiselleştirme:** Hazır temalar (Gece, Gündüz, Okyanus, Orman, Sakura, Amoled, Yüksek kontrast...) ya da kendi renklerinle tema oluşturma. Türkçe ve İngilizce arayüz.
* **🛡 Admin Paneli:** Üyeler ve üyelik süreleri, lisans anahtarları, hata bildirimleri, mesaj şikayetleri, duyurular, sürüm yayınlama, ders kataloğu, yapay zekâ sohbet kayıtları ve işlem geçmişi tek yerden yönetilir.
* **🚀 Güvenli Altyapı & Otomatik Güncelleme:** RLS (Row Level Security) tabanlı Supabase güvenliği, lisans anahtarı doğrulama, tek bilgisayar kuralı (cihaz kilidi) ve yeni sürümleri doğrulayarak (SHA256) otomatik indirip kuran güncelleme yöneticisi.

---

## 🛠 Kullanılan Teknolojiler

* **Arayüz (UI):** `CustomTkinter`, `Tkinter`, `PIL (Pillow)`
* **Ağ & Veri İşleme:** `Requests`, `BeautifulSoup4 (bs4)`, `PyMuPDF (fitz)`, `pypdf`, `truststore`
* **Veritabanı & Backend:** `Supabase` (Auth, REST API, Edge Functions, RLS)
* **Paketleme:** `PyInstaller` (tek exe) ve `Inno Setup` (kurulum sihirbazı)
* **Asistan Motoru:** Özel PDF parçalama, Threading ve yapay zekâ entegrasyonu

---

## 🚀 Kullanım

Ekstra hiçbir kurulum veya Python kütüphanesi yüklemeye gerek yoktur.

1. Güncel **`TopkapiAsistan_Kurulum_x.x.exe`** dosyasını indirin ve çift tıklayın.
2. Kurulum sihirbazındaki adımları izleyin (yönetici izni gerekmez). İsterseniz masaüstü kısayolu oluşturun.
3. Uygulamayı açın, kayıt olun (lisans anahtarı gerekir) ve giriş yapın.

Uygulama açılışta yeni sürüm olup olmadığına bakar. Yeni sürüm varsa "Şimdi güncelle"ye basmanız yeterlidir, tekrar indirmeniz gerekmez.

> Kurulum dosyası şimdilik imzasız olduğu için Windows SmartScreen uyarı gösterebilir. "Ek bilgi › Yine de çalıştır" ile devam edebilirsiniz.

---

## 🧰 Geliştirici: Sürüm Çıkarma

1. `app.py` içindeki `APP_VERSION` değerini artırın.
2. `kurulum\build_installer.bat` dosyasını çalıştırın. Bu, `dist\TopkapiAsistan.exe` ve `installer_output\TopkapiAsistan_Kurulum_x.x.exe` dosyalarını üretir; ekrana SHA256 kodunu yazar. (Inno Setup 6 kurulu olmalıdır.)
3. Düz `TopkapiAsistan.exe` dosyasını internete yükleyin.
4. Admin paneli › Sürümler'den sürüm numarasını, indirme bağlantısını, SHA256 kodunu ve notları girip yayınlayın.
5. Yeni kullanıcılara kurulum dosyasını verin; mevcut kullanıcılar uygulamayı açınca güncellemeyi kendileri alır.

Logo ve ikonlar için: `py make_assets.py LOGO.png [ARKAPLAN.jpg]`

---

## 📂 Dosya Yapısı

* `app.py` – Ana uygulama penceresi, yönlendiriciler, giriş/kayıt, admin paneli ve arayüz sayfaları.
* `ois.py` – OİS oturum yönetimi (captcha çözme), ders programı ve sınav sonucu çekme modülü.
* `study.py` – PDF görüntüleyici, yapay zekâ özetleri, formül listesi ve deneme soruları arayüzü.
* `features.py` – Yapay zekâ sohbet, GNO & sınavlar ve deneme sınavı sayfaları.
* `supa.py` – Supabase kimlik doğrulama (Auth), veritabanı ve RPC istemcisi, oturum yenileme.
* `ai.py` – PDF'leri parçalara ayırıp Edge Function üzerinden yapay zekâya gönderen analiz motoru.
* `theme.py` – Tema motoru (hazır temalar ve özel tema paleti üretimi).
* `i18n.py` – Türkçe / İngilizce arayüz çevirileri.
* `data.py` – Fakülte, bölüm ve statik ders listeleri.
* `icon_data.py` – Gömülü uygulama ikonu.
* `make_assets.py` – Logo, ikon ve giriş arka planı hazırlama aracı.
* `kurulum/` – Kurulum dosyası üretimi: `build_installer.bat`, `setup.iss` (Inno Setup tarifi), `get_version.py`.

---

## 🛡️ Lisans & Güvenlik
Bu proje Topkapı Üniversitesi öğrencilerine özel olarak tasarlanmıştır. OİS şifreleriniz hiçbir şekilde veritabanında saklanmaz; yalnızca anlık OİS oturum doğrulaması için kullanılır. Uygulama şifrenizi yerel olarak da saklamaz; "Beni hatırla" açıksa yalnızca Windows tarafından şifrelenmiş bir oturum anahtarı tutulur.
