# Kaynaklar ve Doğrulama Durumu

**Derleme tarihi:** 23.10.2026

| Kaynak | Kapsam | Durum |
| --- | --- | --- |
| [CISA ICSA-21-280-02](https://www.cisa.gov/ics/advisories/icsa-21-280-02) | MiR100/200/250/500/1000 ve MiR Fleet açıkları, yazılım 2.10.2.1 öncesi | Resmî danışma notu; **MiR250 kapsamda**; bu çalışmada açılıp okundu |
| [MiR250 Specifications (2023-06-28)](https://www.hartfiel.com/wp-content/uploads/2024/04/MiR250-Specs.pdf) | Boyut, yük, hız, batarya, sensörler, bağlantılar | Üretici belgesinin üçüncü taraf kopyası; güncel sürüm MiR destek portalında; bu çalışmada okundu |
| [MiR250 ürün dokümanları](https://mobile-industrial-robots.com/product-documents/mir250-hw-20-sw-2-v1) | Üretici belge sayfası | Üretici kaynağı; **kullanım kılavuzundaki PL/kategori beyanı henüz okunmadı** |
| [CVE-2020-10269](https://db.gcve.eu/vuln/CVE-2020-10269) | Robotun Wi-Fi erişim noktası, tahmin edilebilir ad, parola dokümanlarda | Gerçek CVE; MiR100/MiR200'de doğrulanmış, **MiR250 için etki doğrulanmadı** |
| [CVE-2020-10270](https://vulnerability.circl.lu/vuln/CVE-2020-10270) | Kontrol paneli sabit adreste, varsayılan giriş bilgileri dokümanlarda | Gerçek CVE; **MiR250 için etki doğrulanmadı** |
| Safety 4.0 Readiness Bootcamp föyleri ve sunumları (INSPECCO × Kriptarium) | Yöntem: L × S × E, zone/conduit, Evidence Pack | Ders materyali; mevzuat takvimleri bu kaynaktan alındı |

---

## CVE değerlendirme kaydı: CVE-2020-10276

- **Tanım:** Emniyet kontrolcüsünde varsayılan parola; acil durdurmanın devre dışı bırakılmasına izin verebilir.
- **Etkilenen ürün / sürüm:** CISA'ya göre Haziran 2020 öncesi sevk edilen robotlar (MiR100/200/250/500/1000, yazılım 2.10.2.1 öncesi).
- **CVSS v3:** 8,8 (CISA ICSA-21-280-02 tablosu).
- **Uygulanabilirlik:** **Bilinmiyor.** Robotun üretim tarihi ve yazılım sürümü bu çalışmada elde yok.
- **Gerekli kanıt:** Seri numarası ve sevk tarihi, yazılım sürümü, emniyet kontrolcüsü parolasının değiştirilip değiştirilmediğine dair kayıt.

## Diğer CISA kayıtları (özet)

| CVE | Konu | CVSS v3 |
| --- | --- | --- |
| CVE-2020-10271 | ROS API'leri kablolu ve kablosuz arayüzden erişilebilir | 9,8 |
| CVE-2020-10272 | ROS varsayılan paketleri kimlik doğrulamasız | 8,8 |
| CVE-2020-10277 | Varsayılan olarak USB'den açılış açık | 6,4 |
| CVE-2020-10278 | BIOS parolası yok | 4,6 |
| CVE-2020-10280 | Port 80 web sunucusu yarım HTTP başlıklarıyla yanıtsız bırakılabilir | 7,5 |

---

Bu belge, incelenen robotun savunmasız olduğunu iddia etmez; yalnızca yayımlanmış kayıtların **ürün ailesi için** ne söylediğini ve neyin doğrulanması gerektiğini gösterir.
