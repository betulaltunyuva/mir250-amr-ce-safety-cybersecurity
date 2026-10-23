# Proje Kapsamı ve CE Teknik Dosya Hazırlık Notları

## Seçilen nesne

**Mobile Industrial Robots (MiR) / MiR250 Otonom Mobil Robot (AMR – Fabrika İçi Malzeme Taşıma).**

İnceleme, belirli bir fiziksel robot üzerinde değil, üreticinin ve CISA'nın yayımladığı **kamuya açık dokümanlar** üzerinden yapılmaktadır. Robotun gerçek yazılım sürümü, ağ yapılandırması ve parola durumu bu çalışmada bilinmemektedir.

Kullanım senaryosu (depodan montaj hattına parça kasası taşıma, ortak koridor, fabrika Wi-Fi'ı, üretici servisinin uzaktan bağlantısı) **akademik bir varsayımdır**; gerçek bir tesisi temsil etmez.

## Veri sınıflandırması

Bu depodaki bilgiler üç gruba ayrılır:

| Sınıf | Anlamı | Örnek |
| --- | --- | --- |
| **Doğrulanmış** | Üretici veya CISA belgesinde yazılı | 97 kg, 250 kg yük, 2,0 m/s; 2 × SICK nanoScan3; CISA ICSA-21-280-02'deki CVE listesi |
| **Bilinmeyen** | Kaynaklarda bulunamadı veya okunmadı | Emniyet fonksiyonlarının üretici beyanı olan PL/kategori değeri; robotun gerçek yazılım sürümü |
| **Akademik öneri** | Bu çalışmada üretilen tasarım ve değerlendirme | Zone/conduit bölümleri, R-01…R-05 risk puanları, jump server + VPN + MFA tasarımı |

> LAB 1'deki **PL d** değeri ISO 3691-4'ün tipik gerekliliğidir; **MiR'in kendi beyanı değildir** ve kılavuzdan doğrulanana kadar *bilinmeyen* sınıfındadır.

## Akademik CE teknik dosya taslağı bölümleri

1. Makine tanımı ve amaçlanan kullanım
2. Varlık envanteri (donanım, yazılım, hesaplar, anahtarlar, dış bağlantılar, veri akışları)
3. Emniyet fonksiyonları (Safety Function Map)
4. Tehlike ve risk değerlendirmesi
5. Siber risk değerlendirmesi (Risk Register, S3 bayrağı)
6. Zone / conduit ve uzak erişim tasarımı
7. SBOM, bilinen açıklar ve yama kararları
8. Olay müdahale akışı
9. Doğrulama ve test planı
10. Kaynaklar ve revizyon geçmişi

## Kritik sınır

Bu depo **resmî bir CE uygunluk dosyasının yerine geçmez**. Gerçek bir uygunluk dosyası; üreticinin veya yetkili tarafın kanıtlarını, test sonuçlarını ve imzalı beyanlarını gerektirir. Buradaki çalışma, bir CE teknik dosyasının siber güvenlik bölümünün **eğitim amaçlı taslağıdır**.

## Laboratuvar föyleriyle ilişki

- `docs/` altındaki PDF'ler laboratuvar föyleridir. Şu an **LAB 1–4** vardır; sonraki laboratuvarlar her hafta aynı klasörlere eklenecektir.
- Föyler **şişeleme** ve **paketleme** sürümleri olarak ayrı tutulur; her laboratuvar ayrı PDF'tir.
- Föyler ve CE teknik dosya taslağı **ayrı çıktılardır**: föyler dersin haftalık görevidir, teknik dosya taslağı ise bu görevlerin bulgularını birleştiren son çalışmadır.
