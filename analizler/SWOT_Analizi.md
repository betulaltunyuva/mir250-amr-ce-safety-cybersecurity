# SWOT Analizi: MiR250 CE ve Siber Güvenlik Projesi

**Tarih:** 23.10.2026
**Analiz konusu:** MiR250 otonom mobil robotun siber güvenlik ve emniyet durumu
**Not:** Bu tablo bir makine test raporu değildir; kamuya açık dokümanlardan ve LAB 1–4 bulgularından çıkarılmıştır. Tasarlanan PDF sürümü: [SWOT_Analizi_MiR250_BetulAltunyuva.pdf](SWOT_Analizi_MiR250_BetulAltunyuva.pdf)

## Güçlü yönler (S)

| # | Güçlü yön | Projeye etkisi |
| --- | --- | --- |
| S1 | 2 × SICK nanoScan3 lazer tarayıcı ve emniyet kontrolcüsü, robot bilgisayarından ayrı bir emniyet zinciri oluşturur | LAB 1'de "ayrı safety yolu" doğrudan gösterilebilir |
| S2 | İnsan algılama, acil durdurma ve aşırı hız önleme fonksiyonları üretici belgesinde tanımlı | Safety Function Map için kaynak hazır |
| S3 | Teknik özellik sayfası ve CISA danışma notu (ICSA-21-280-02) kamuya açık | Doğrulanmış bilgi sınıfı geniş tutulabilir |
| S4 | Bilinen açıklar için yazılım sürümü eşiği belli (2.10.2.1) | LAB 5'te yama kararı gerçek veriye dayanır |

## Zayıf yönler (W)

| # | Zayıf yön | Azaltma yaklaşımı |
| --- | --- | --- |
| W1 | Varsayılan Wi-Fi ve panel parolaları ile emniyet kontrolcüsü parolasına ilişkin açıklar (CVE-2020-10269/10270 araştırmacı bildirimi; CVE-2020-10276 CISA kaydı) | Parolaları ilk kurulumda değiştirmek, kişisel hesap kullanmak |
| W2 | ROS arayüzünde kimlik doğrulama eksikliği (CVE-2020-10271, CVE-2020-10272) | Arayüzü ayrı ve filtreli bir ağda tutmak |
| W3 | USB'den açılış açık, BIOS parolası yok (CVE-2020-10277, CVE-2020-10278) | USB boot kapatmak, BIOS parolası vermek, fiziksel kapak |
| W4 | Bu çalışmanın analizine göre emniyet ayarlarına ağ üzerinden ulaşılabiliyor | Emniyet ayarlarını yalnızca yerinde değiştirilebilir yapmak (LAB 4 gereksinimi) |

## Fırsatlar (O)

| # | Fırsat | Nasıl değerlendirilecek? |
| --- | --- | --- |
| O1 | Yazılımı 2.10.2.1 ve sonrasına yükseltmek | Güncelleme ve sonrasında emniyet fonksiyonu doğrulaması |
| O2 | Jump server, VPN, MFA, kişisel hesap ve oturum kaydı | R-01 riskini 27'den 6'ya indirir |
| O3 | Emniyet ayarlarını ağdan bağımsız tutmak | R-01 riskini 6'dan 2'ye indirir ve S3 bayrağını kaldırır |
| O4 | CRA bildirimi (11 Eylül 2026) ve Makine Tüzüğü (20 Ocak 2027) takvimi | Kanıt dosyasını (Evidence Pack) erken ve düzenli üretmek |

## Tehditler (T)

| # | Tehdit | Önlem |
| --- | --- | --- |
| T1 | Fırsatçı dış saldırgan: parolalar kılavuzda, Wi-Fi sürekli yayında (R-01) | Parola değişikliği, robotun kendi erişim noktasını kapatmak |
| T2 | Meraklı içeriden: paylaşılan hesapla susturma bölgesi eklenebilir (R-02) | Kişisel hesap, değişiklik kaydı, susturma için onay |
| T3 | Tedarik zinciri: servis erişimi veya güncelleme yoluyla hatalı harita/yazılım (R-03) | Varsayılan kapalı erişim, onaylı sürüm, güncelleme sonrası test |
| T4 | Hukuki ve fiziksel sonuç: CRA cezası tavanı 15 M€ veya cironun %2,5'i; 350 kg'a kadar hareketli kütle | Risk Register'da S3 senaryolarını ayrı takip etmek |

## SWOT'tan türetilen strateji

- **SO (güçlü yön + fırsat):** Ayrı emniyet zincirini (S1) koruyup emniyet ayarlarını ağdan ayırarak (O3) en yüksek riski en çok düşüren çözümü uygulamak.
- **WO (zayıf yön + fırsat):** Varsayılan parola ve açık erişim sorunlarını (W1, W2) yazılım güncellemesi ve erişim önlemleriyle (O1, O2) kapatmak.
- **ST (güçlü yön + tehdit):** Açık dokümantasyonu (S3) kullanarak fırsatçı ve içeriden tehditlere (T1, T2) karşı kontrol listesi üretmek.
- **WT (zayıf yön + tehdit):** Güncellenmemiş robot kalırsa açıkların süreceğini (W1–W3, T1) varsayıp eski sürümleri filodan ayrı izlemek.

## Kısa sonuç

MiR250'nin emniyet donanımı güçlüdür; asıl risk **varsayılan parolalar ve ağ üzerinden değişebilen emniyet ayarlarıdır**. Bu proje, akademik bir CE teknik dosya taslağı için uygun bir konudur. Ana kısıt, belirli bir robotun gerçek yapılandırmasının ve üretici emniyet beyanının (PL değeri) doğrulanmamış olmasıdır.
