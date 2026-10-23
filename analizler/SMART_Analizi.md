# SMART Analizi: MiR250 CE ve Siber Güvenlik Projesi

**Hazırlayan:** Betül Altunyuva · Gece-B
**Güncelleme tarihi:** 23.10.2026
**Planlama ufku:** LAB 1'den akademik CE teknik dosya taslağına kadar, haftada bir laboratuvar

## Ana SMART hedef

MiR250 otonom mobil robotu için, kamuya açık üretici ve CISA dokümanlarına dayanarak, **LAB 1–7 çıktılarını ve bunları birleştiren akademik bir CE teknik dosya taslağını** haftalık ders takvimiyle uyumlu biçimde tamamlamak. Taslak, doğrulanmış bilgi, bilinmeyenler ve akademik önerileri birbirinden ayırarak sunacaktır.

## SMART kriterleri

| Harf | Kriter | Bu projede |
| --- | --- | --- |
| **S** | Specific (Belirli) | Tek makine (MiR250), tek konu (siber güvenlik ve emniyet kesişimi), tanımlı çıktılar (Safety Function Map, Zone/Conduit, Risk Register, Secure Architecture, …) |
| **M** | Measurable (Ölçülebilir) | Tamamlanan laboratuvar sayısı, Risk Register'daki senaryo sayısı ve S3 bayrakları, kaynaklarda doğrulama etiketi taşıyan kayıt oranı |
| **A** | Achievable (Ulaşılabilir) | Fiziksel test veya robota erişim gerekmez; tüm çalışma kamuya açık dokümanlarla yapılır |
| **R** | Relevant (İlgili) | CRA ve Makine Tüzüğü (AB) 2023/1230 kapsamında üreticinin siber risk değerlendirmesini teknik dosyaya koyma yükümlülüğüne hazırlık |
| **T** | Time-bound (Zamanlı) | Her laboratuvar ilgili haftada teslim edilir; teknik dosya taslağı LAB 7'den sonraki hafta için önerilmiştir |

## İş paketleri ve başarı ölçütleri

| Paket | Önerilen zaman | Ölçülebilir çıktı | Başarı ölçütü |
| --- | --- | --- | --- |
| **H1** Makine tanımı ve kaynak envanteri | Hafta 1 | Teknik özellik tablosu, bileşen listesi, `kaynaklar/Kaynaklar.md` | Her kaynakta doğrulama durumu yazılı |
| **H2** LAB 1–2 | Hafta 1–2 | Safety Function Map, envanter, Zone/Conduit | Safety PLC için ayrı bölge gerekçelendirilmiş |
| **H3** LAB 3–4 | Hafta 3–4 | Risk Register, güvenli uzak erişim mimarisi | En az 3 senaryo, S3 bayrağı, her puana gerekçe |
| **H4** LAB 5 | Hafta 5 | SBOM ve CVE karar kaydı | Her CVE için "uygulanabilirlik" ve "gerekli kanıt" alanı dolu |
| **H5** LAB 6–7 | Hafta 6–7 | Olay müdahale akışı, yapay zekâ başarısızlık kararı | 24 saat / 72 saat / 14 gün çizelgesi ve güvenli davranış tablosu |
| **H6** Teknik dosya taslağı | Hafta 8 | `PROJE_KAPSAMI.md`'deki 10 bölümün doldurulması | Üç veri sınıfı (doğrulanmış / bilinmeyen / öneri) ayrı gösterilmiş |

## İzleme göstergeleri

| Gösterge | Hedef | Durum (23.10.2026) |
| --- | --- | --- |
| Tamamlanan laboratuvar | 7 | 4 |
| Risk Register senaryosu | En az 3 | 3 föyde, 5 raporda |
| S3 bayrağı taşıyan senaryo | Hepsi işaretli | Evet |
| Doğrulanmayan kabul | 0 açık madde | 1 açık: PL d üretici beyanı |
| Kaynak kaydında durum etiketi | %100 | Evet |

## Kapsam dışı

- Fiziksel robot üzerinde test, tarama veya yapılandırma değişikliği
- Bilinen açıkların istismar edilmesi
- Resmî CE belgelendirmesi veya uygunluk beyanı
- Üreticiye ait gizli dokümanların kullanılması

> Zamanlar **önerilen hedef tarihlerdir**; dersin resmî teslim tarihleri değildir ve ders takvimine göre güncellenir.
