# Görev Talimatı — Referans Kopyası

> Bu dosya, zamanlayıcıda tanımlı görevin talimatının kopyasıdır. Görev bu dosyayı OKUMAZ; asıl talimat zamanlayıcıdadır. Talimat değiştiğinde ikisini birlikte güncelle.
>
> Zamanlama ayarı: **Daily, 09:00** (İstanbul). 3 günlük ritmi ADIM 0'daki kapı sağlıyor.
> Son güncelleme: 2026-10-16

---

```
Kerem için AI/LLM gelişmeleri özeti hazırla. Bu oturumun önceki konuşmalardan HİÇBİR hafızası yok; adımları sırayla uygula. Kerem bu oturumu okumaz (zamanlanmış görev) — rapor ona ADIM 7'deki bildirim/dosya ile ulaşır.

ZAMANLAMA: Görev HER GÜN tetiklenir ama rapor 3 GÜNDE BİR üretilir. Hangi günün rapor günü olduğuna ADIM 0'daki kapı karar verir. Tarihler İstanbul saatine (UTC+3) göredir.

MİMARİ: İki ayrı şey var, karıştırma.
• DURUM (takip listesi) → GitHub: `irgan/ai-llm-takip` deposunda `takip-listesi.md`. Her çalışmada okunur, güncellenir, AYNI YOLA yazılır. Kalıcı, birikimli. Dosyanın "Çalışma Ritmi" ve "Kurallar" bölümleri bağlayıcıdır; bu talimatla çelişirse DOSYADAKİ kural geçerlidir.
• RAPOR (çalışma çıktısı) → aynı depoda `raporlar/YYYY-AA-GG.md` (çalışma tarihi). Bir kez yazılır, sonra dokunulmaz (istisna: aynı gün ikinci çalışma, bkz. 7.2).

════ TEMEL KURALLAR ════

K1. SAYI DİSİPLİNİ: Sayısal iddiaları (yıldız, parametre, benchmark, fiyat) ikincil kaynağın özetinden ALMA. GitHub yıldızları YALNIZCA API'nin `stargazers_count` alanından. Trendshift/blog'daki "+235 stars" ARTIŞTIR, toplam değil. WebFetch'in sayfa özetleyicisi yıldız rozetlerini yanlış okuyabiliyor — ona güvenme. Doğrulayamadığın sayıyı YAZMA, "doğrulanamadı" de.

K2. ARAÇ ŞEFFAFLIĞI: Bir araç bağlı değilse sessizce eksik veriyle devam etme; hangi kaynağı kullanamadığını raporda yaz.

K3. UYDURMA YOK: Bulamadığın bölüme "bu dönemde kayda değer bir şey yok" yaz; boşluğu zayıf maddeyle doldurma. 3 günlük pencerede boş bölüm normaldir.

K4. VERİMLİLİK: Bağımsız aramaları TEK mesajda paralel yap. Bir konuda 3 aramada sonuç yoksa "gelişme yok" kabul edip geç. Rapor günlerinde ~15-25 arama yeterli. `list_triggers` ve `update_trigger` ÇAĞIRMA — bu göreve gerekmez (list_triggers devasa çıktı döndürüp bağlamı doldurur).

════ ADIM 0 — KAPI: Bugün rapor günü mü? ════

1. ToolSearch ile mcp__GG__get_file_contents'i yükle.
2. owner=irgan, repo=ai-llm-takip, path=raporlar ile klasörü listele. `YYYY-AA-GG.md` adlı dosyalardan EN YENİ tarihi bul (= SON_RAPOR).
3. GÜN_FARKI = bugün − SON_RAPOR (gün olarak).
   • GÜN_FARKI < 3 → ÇALIŞMAYI BİTİR. Hiçbir dosya yazma, bildirim ve dosya GÖNDERME. Oturum yanıtı olarak yalnızca tek satır yaz: "Kapı: son rapor SON_RAPOR, GÜN_FARKI gün önce — bugün rapor günü değil."
   • GÜN_FARKI ≥ 3 → Devam et (ADIM 1). PENCERE = (SON_RAPOR + 1 gün) → bugün, ikisi de dahil. GÜN_FARKI > 3 ise bir çalışma kaçmış demektir; pencere kendiliğinden geniştir, raporun kısıt notunda belirt.
4. GitHub'a erişilemiyorsa (ToolSearch'le bir kez yeniden yüklemeyi dene): Kapıyı tarihle uygula. 2026-10-17'den bugüne geçen gün sayısı 3'e tam bölünüyorsa DEGRADE MOD ile devam et, bölünmüyorsa tek satır "Kapı: GitHub erişilemedi, bugün tarih-kapısına göre rapor günü değil" yazıp bitir. Böylece GitHub çökük kaldığı sürece her gün bildirim gitmez.

════ ADIM 1 — Araç envanteri ════

ToolSearch ile yükle ve mevcut olduklarını doğrula: mcp__GG__get_file_contents, mcp__GG__create_or_update_file, mcp__GG__search_repositories, WebSearch, WebFetch.
GG bağlı değilse: bir kez ToolSearch ile yeniden yüklemeyi dene. Yine yoksa DEGRADE MOD'a geç.

════ ADIM 2 — Durumu oku ════

mcp__GG__get_file_contents ile path=takip-listesi.md oku.
⚠️ Dönen `sha` değerini NOT AL — ADIM 7'de yazmak için zorunlu.
Dosyada "Çalışma Ritmi", "Kurallar", "Aktif Takip Listesi", "Arşivlenmiş Konular", "Değişiklik Geçmişi" bölümleri ve 15+ aktif konu olmalı. Çok daha azı varsa bozuk okuma olabilir; devam etmeden depoyu kontrol et.
"BEKLEYEN NOT" satırlarını listele — bu çalışmada işlenecekler.

════ ADIM 3 — PENCERE'yi araştır ════

a) HABERLER: Büyük laboratuvarlar (OpenAI, Anthropic, Google DeepMind, Meta, Mistral, xAI, DeepSeek, Alibaba/Qwen, Moonshot, Z.ai) — model/ürün duyuruları, önemli araştırma, regülasyon. Yalnızca yayın tarihi PENCERE içinde olanlar.
b) GITHUB: mcp__GG__search_repositories ile gerçek API'den ara: `created:[PENCERE başı]..[bugün] stars:>100 agent OR llm OR ai OR claude OR gpt` (sort: stars, order: desc). Yıldızlar API'den (K1).
c) YENİ ARAÇLAR: yeni çıkan AI araçları/ajanları.
d) ÇALIŞMA YÖNTEMLERİ: yeni prompting teknikleri, agent workflow yaklaşımları, verimlilik ipuçları.
e) BEKLEYEN NOTLAR: her birini birincil kaynaktan doğrula.

════ ADIM 4 — Çapraz kontrol ════

Aktif ve Arşivlenmiş listedeki HER konuyu tek tek gözden geçir — araç/repo/yöntem tipi olanlar dahil (en çok atlanan kısım burası).
Takip edilen GitHub repolarının yıldızlarını API'den tazele. Tek sorguda birden çok `repo:owner/name` kullanabilirsin.
Kaynağı belirsiz sayısal iddia varsa doğrula; doğrulayamıyorsan rakamı çıkar ve günlüğe "doğrulanamadı, kaldırıldı" yaz.

════ ADIM 5 — Raporu yaz (Türkçe) ════

Başlık: `# AI/LLM Özeti — GG Ay YYYY (pencere: GG–GG Ay)`
Bölümler:
1) Haberler (0-5, kaynak linkli)
2) Yeni Araçlar (0-5, linkli)
3) Dikkat Çekici GitHub Repoları (0-5, linkli; takip edilen repoların yıldız değişimi önceki rapora göre, aralık belirtilerek, örn. "3 günde +%2,1")
4) AI ile Çalışma Yöntemleri (varsa 1-3)
5) Önceki Konularda Gelişmeler — her eşleşen konu için: konu adı, gelişme, derece (🟢 Büyük / 🟡 Orta / ⚪ Küçük). Gelişmesi olmayan konuyu gösterme. Arşivden dönen varsa "X yeniden gündemde" diye vurgula.
Riskli/şüpheli repo ve araçları ⚠️ ile işaretle ve nedenini tek cümleyle yaz.
Okuma süresi 2 dakikayı geçmesin. Kısıt yaşandıysa (araç yok, kaçırılmış çalışma vb.) raporun başına tek satır not düş.

════ ADIM 6 — SON KONTROL (göndermeden önce, atlanamaz) ════

Bir madde başarısızsa önce düzelt, sonra devam et:
1. Her sayısal iddia birincil kaynaktan mı? (K1) Yıldızlar API'den mi?
2. Rapordaki her link gerçekten açıp gördüğün bir sayfa mı? Uydurma URL var mı?
3. Aktif listedeki HER konunun "Son kontrol" tarihi bugün mü? (Gelişme yoksa günlüğe SATIR EKLEME — yalnızca "Son kontrol" güncellenir.)
4. "Son güncelleme"yi yalnızca GERÇEK gelişme olan konularda mı değiştirdin? Yalnızca yıldız artışı ve "gelişme yok" durumu "Son güncelleme"yi DEĞİŞTİRMEZ. Yanlışlıkla değiştirdiysen geri al — bu kural bozulursa hiçbir konu arşivlenmez.
5. Arşivleme: (bugün − "Son güncelleme") ≥ 21 gün olan Aktif konu kaldı mı? Kaldıysa arşivle.
6. Yıldız satırları: takip listesine son yıldız kaydından bu yana ≥7 gün geçtiyse ya da değişim ±%25'i aştıysa mı yazdın? (Aksi halde yalnızca raporda kalır.)
7. Tüm BEKLEYEN NOT'lar işlenip silindi mi? (Doğrulanamayan not "doğrulanamadı, kaldırıldı" diye kapatılır.)
8. Raporda yazdığın her gelişme takip listesine de işlendi mi?
9. Yeni konu sayısı makul mu (0-3)? Fazlaysa mevcut konuyla eşleştir.
10. Dosya boyutu: güncel takip listesi 25 KB'ı aşıyor mu? Aşıyorsa dosyadaki sıkıştırma kuralını uygula (konu başına son 3 kayıt, #24'te tarama başına en fazla 5 repo, hedef ≤20 KB). Aşmıyorsa SIKIŞTIRMA YAPMA.

════ ADIM 7 — Kaydet ve gönder ════

7.1 DURUM: mcp__GG__create_or_update_file ile path=takip-listesi.md, branch=main, sha=[ADIM 2'deki sha], message="Güncelleme YYYY-AA-GG: N yeni konu, M güncelleme, K arşiv". sha olmadan yazma BAŞARISIZ olur; sürüm çakışması dönerse dosyayı yeniden oku, değişikliklerini birleştir ve tekrar yaz.
   Kurallar: yeni konuları ekle (ilk görülme = son güncelleme = son kontrol = bugün); gelişme olanların "Son güncelleme"sini bugüne çek ve günlüğe tarihli not ekle (eski notları silme); tüm aktif konuların "Son kontrol"ünü bugüne çek; 21+ gün eskiyeni arşivle; arşivden döneni Aktif'e al; "Değişiklik Geçmişi"ne bugünün tek satır özetini ekle.

7.2 RAPOR: path=raporlar/YYYY-AA-GG.md (bugün), branch=main, message="Rapor YYYY-AA-GG". Yeni dosya, sha GEREKMEZ. AYNI ADLA dosya zaten varsa (aynı gün ikinci çalışma) üzerine yazma: önce get_file_contents ile oku, sha'sını al, yeni bulguları ekleyerek güncelle ve kısıt notuna "aynı gün ikinci çalışma" yaz.

7.3 Raporu yerel .md olarak da kaydedip SendUserFile ile gönder (status: proactive).

7.4 PushNotification (status: proactive) gönder; mesajı <routine_summary> etiketleri içine koy. İlk cümle dönemin EN ÖNEMLİ tek gelişmesi olsun (telefon bildiriminde sadece o görünür), sonra 2-3 kritik madde ve "N konu güncellendi, M yeni konu, K arşivlendi" özeti. Sorun yaşandıysa (GitHub'a yazılamadı, konektör yok, çalışma kaçmış) bildirimde MUTLAKA belirt.

7.5 Özeti oturum yanıtı olarak da yaz.

════ DEGRADE MOD (GitHub erişilemiyorsa) ════

Yalnızca ADIM 0.4'teki tarih kapısı geçildiyse uygulanır. Takip listesi olmadan raporun 1-4. bölümlerini üret (5. bölümü atla, sebebini yaz). PENCERE = son 3 gün. Raporu ADIM 7.3 ve 7.4 ile Kerem'e ULAŞTIR. Durum güncellemesini ATLA — Drive'a veya başka bir yere alternatif kopya YAZMA (iki ayrı durum dosyası oluşması en kötü sonuçtur). Bildirimde "GitHub erişilemedi, takip listesi güncellenmedi" de. GitHub geri geldiğinde bir sonraki çalışma, son rapordan bu yana geçen tüm dönemi kendiliğinden kapsar.
```
