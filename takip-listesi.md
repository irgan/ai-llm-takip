# AI/LLM Takip Listesi

Bu dosya AI/LLM özeti otomasyonunun KALICI DURUM dosyasıdır. Her rapor çalışmasında okunur, güncellenir ve AYNI YOLA (`takip-listesi.md`) yazılır. Git commit geçmişi sayesinde her çalışmanın değişimi diff olarak görülebilir.

Raporlar ayrı dosyalardır: `raporlar/YYYY-AA-GG.md`. Bu dosya rapor değil, takip durumudur. Görev talimatının referans kopyası: `gorev-talimati.md`. Talimatla bu dosya çelişirse BU DOSYADAKİ kural geçerlidir.

## Çalışma Ritmi

- **Tetikleme:** Zamanlayıcı HER GÜN 09:00'da (İstanbul) tetiklenir. Rapor 3 günde bir üretilir. Geçerlilik başlangıcı 2026-10-17; öncesi haftalıktı (2026-08-17 – 2026-10-12).
- **Kapı (görev ADIM 0):** `raporlar/` klasöründeki en son tarihli dosyadan bu yana 3 gün geçmediyse çalışma hiçbir şey yazmadan biter. Bu dosya kapı günlerinde DEĞİŞMEZ; "Son kontrol" de güncellenmez.
- **`raporlar/` klasöründe yalnızca `YYYY-AA-GG.md` dosyaları bulunur.** Başka dosya (taslak, not, alt klasör) konulmaz; kapı en son tarihi bu dosya adlarından okur.
- **GitHub erişilemezse:** Kapı tarihle çalışır. 2026-10-17'den bu yana geçen gün sayısı 3'e tam bölünen günlerde degrade rapor üretilir, bu dosya güncellenmez.
- **Tarama penceresi:** en son rapor dosyasının tarihinden sonraki gün → çalışma günü (dahil). Normalde 3 gün. Çalışma kaçarsa ya da yarıda kalırsa pencere son rapora kadar genişler, arada boşluk bırakılmaz; bu durum raporun kısıt notunda belirtilir.
- **Rapor dosyası:** `raporlar/YYYY-AA-GG.md`, ad çalışma tarihidir. Aynı gün o adla bir rapor zaten varsa (yalnızca elle tetiklemede olur) üzerine YAZILMAZ: mevcut rapor yeni bulgularla güncellenir ve kısıt notuna "aynı gün ikinci çalışma" eklenir.
- **Başlık formatı:** `# AI/LLM Özeti — GG Ay YYYY (pencere: GG–GG Ay)`. Bölüm yapısı değişmez: 1. Haberler · 2. Yeni Araçlar · 3. Dikkat Çekici GitHub Repoları · 4. AI ile Çalışma Yöntemleri · 5. Önceki Konularda Gelişmeler. (2026-10-12 ve öncesi raporların başlığı "Haftalık Özet"tir; değiştirilmez.)
- **Kısa pencere:** Bölümlerin boş kalması normaldir. Boşluk doldurmak için zayıf haber eklenmez; "Bu dönemde kayda değer gelişme yok" yazılır.
- **GitHub repo taraması (#24):** `created:` filtresi rapor penceresiyle aynıdır.
- **Bekleyen notlar:** Bir konuda "BEKLEYEN NOT" varsa, sonraki rapor çalışması onu birincil kaynaktan doğrulayıp normal kayıt olarak işler ve notu siler. Doğrulanamazsa "doğrulanamadı, kaldırıldı" diye kapatılır.

## Kurallar

- Yeni bahsedilen her önemli konu buraya bir madde olarak eklenir (ilk görülme = son güncelleme = son kontrol = bugün). Bir çalışmada 0-3 yeni konu makuldür; fazlası mevcut konularla eşleştirilir.
- Gerçek bir gelişme olduğunda "Son güncelleme" değişir ve günlüğe tarihli not eklenir.
- ⚠️ Gelişme yoksa günlüğe satır EKLENMEZ. Yalnızca konu başlığındaki "Son kontrol" tarihi güncellenir. "Son güncelleme" DEĞİŞMEZ; arşivleme buna bağlıdır.
- **Yalnızca yıldız büyümesi gerçek gelişme sayılmaz** ve "Son güncelleme"yi değiştirmez. Yıldızlar raporda her çalışmada verilir. Takip listesine son yıldız kaydından bu yana ≥7 gün geçtiyse, tek satır olarak (`(yıldız, tarih)` etiketiyle) yazılır. Önceki kayda göre ±%25'i aşan değişim anomali sayılır ve hemen yazılır.
- Yıldız yüzdeleri bir önceki rapordaki değere göre hesaplanır ve karşılaştırma aralığı belirtilir (ör. "3 günde +%2,1").
- "Son güncelleme"si 21+ gün eskiyen konu "Arşivlenmiş Konular"a taşınır (her rapor çalışmasında kontrol edilir). Arşivdeki konu yeniden gündeme gelirse Aktif'e döner. Arşivdeki konulara gelişme yoksa satır eklenmez.
- Sayısal iddialar (yıldız, parametre, benchmark, fiyat) yalnızca birincil kaynaktan/API'den alınır. GitHub yıldızları yalnızca `stargazers_count`'tan alınır.
- **Sıkıştırma:** YALNIZCA dosya 25 KB'ı aştığında yapılır. Her konuda son 3 günlük kayıt bırakılır, öncesi konunun "Özet" satırına eklenir; #24'te tarama başına en fazla 5 repo tutulur (tam liste raporda); "Değişiklik Geçmişi"nde son 10 satır bırakılır, öncesi tek bir "bkz. git geçmişi" satırına indirilir. Hedef: sıkıştırma sonrası ≤20 KB (her çalışmada tekrar sıkıştırmayı önler).
- Kısaltmalar: K1 = doğrulanamadı/alınmadı, K2 = kaynağa erişilemedi, K3 = geriye dönük fark edildi.
- Geriye dönük üretilen raporlarda geçmiş tarihli yıldız verisi alınamaz. Yıldızlar üretim günü itibarıyla verilir ve bu kayıtta belirtilir.

## Aktif Takip Listesi

### 2. Anthropic modelleri, ürünleri ve kurumsal/güvenlik gelişmeleri (Claude 5.5 ailesi; Fable/Mythos 5.2; Duet; Chat+Cowork; S-1/IPO; Max/Ultra; FlashProve)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-10 | Son kontrol: 2026-11-10 | Durum: Aktif
- Özet (07-27/11-04): Fable 5, Opus 5, Sonnet 5; Cowork; Commerce Agents. 5.5 ailesi: Opus ($4/$20), Sonnet ($2/$10), Haiku ($0,10/$0,50). Claude Duet (21 Eki; #33); Enterprise Chat+Cowork birleşimi (16 Kasım). S-1 / S-1/A (Nasdaq "ANT"); Max ($100) / Ultra ($200); FlashProve; message threads beta.
  - 2026-11-07 (🟡): AP ile seçim verisi lisans anlaşması; Claude Personal Finance beta (ABD, Plaid, salt okunur); Cat Wu OpenAI'ye geçti. Hepsi ikincil. METR → #34.
  - 2026-11-10 (🟢): Claude Fable 5.2 + Mythos 5.2 (9 Kasım; anthropic.com/claude-fable-and-mythos-5-2) — aynı temel model; Fable herkese (siber/bio korumalarıyla), Mythos doğrulanmış kuruluşlara (Cyber / Life Sciences Verification Program; Enterprise'da Claude Security). $8/$40 (hızlı mod $16/$80). FrontierCode 2.0 Xhigh %49,1 (Opus 5.5 %45,5), OSWorld 2.1 %89,3, HLE (araçlı) %74,2. FLT formalizasyonu → #39; CVE Rediscovery → #37. İkincil: IPO fiyat aralığı/halka arz takvimi bildirildi (rakamlar K1); jeneratör anlaşması → #42; Claude Code sır sızıntısı → #12.

### 3. Gemini ailesi ve Google DeepMind (Gemini 4 Argon, Genie 4, Omni, TPU 8)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-10 | Son kontrol: 2026-11-10 | Durum: Aktif (09-28 arşivlendi, 10-05 geri döndü)
- Özet (07-27/10-29): Gemini 4 Argon GA 13 Ekim — $2/$10 tanıtım fiyatı 30 Kasım'a kadar, sonra $4/$20. Genie 4 (27 Ekim; erken erişim).
  - 2026-11-07 (🟡): Gemini Omni 1.2 Flash GA (5 Kasım; Gemini API + Google Cloud) — video üretim/çok turlu düzenleme, klip 3–15 sn (önce 10), fiyat %30 düşüşle 720p $0,07/sn; SynthID filigranı. Kaynak: blog.google.
  - 2026-11-10 (⚪): TPU 8tx (gizli/güvenli çıkarım, 5. nesil AMD EPYC host; TPU 8t'ye göre "2 kata kadar daha düşük gecikme") ve TPU 8i Max (iki 8i çipi tek pakette; işlem/SRAM/HBM bant genişliği 2 kat) duyuruldu (9 Kasım; blog.google). Çıkış tarihi belirtilmemiş.

### 6. Qwen serisi (Alibaba: 3.8 ailesi, QwenWork, Qwen 4; Apple Intelligence Çin)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-07 | Son kontrol: 2026-11-10 | Durum: Aktif (10-20 arşivlendi, 11-01 geri döndü)
- Özet (07-27/11-01): 3.8 ailesi, QwenWork; Qwen 4 duyurusu (22 Eyl). Apple–Alibaba (31 Ekim): Qwen Çin'de Apple Intelligence'ı çalıştıracak (ikincil).
  - 2026-11-04 (⚪): Qwen 4 yayınlanmadı; "gelecek hafta" aktarımı, 16/18 Kasım söylentileri. Apple Çin betası teyit edilmedi (K1).
  - 2026-11-07 (⚪): Qwen 4 hâlâ yok. Qwen ekibi Qwen 4 ve 5'in açık ağırlık kalacağını söyledi (MindStudio, 3 Kasım; ikincil). Microsoft Foundry Local, Qwen3.8-27B'yi Copilot BYOK ile yerel kodlama ajanı olarak çalıştırıyor (6 Kasım; benchmark K1).

### 12. AI ajan güvenlik açıkları (sandbox kaçışları, framework RCE, anahtar/veri sızıntıları, tedarik zinciri, AI ile otonom saldırılar) ve savunma araçları
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-11-10 | Son kontrol: 2026-11-10 | Durum: Aktif
- Özet (08-07/11-01): CISA 12 framework RCE; Cursor CVE'leri; CVE-2026-82533 (dsh); Archon CVE-2026-111322 (9.8, yama yok); OpenCode ihlali; sahte AGENTS.md npm; kurcalanmış Claude Code eklentisi 2.1.313 (Cursor marketplace, 29 Ekim).
  - 2026-11-04 (🟡): K3: Postman Desktop 12.33.4 Claude Code/Codex'e sormadan eklenti/hook kuruyor (issue #14370). OpenAI–Cathedral; Apple 10-K ajan riski.
  - 2026-11-10 (🟢): K3 (7 Kasım; The Hacker News / Apiiro): Claude Code "Yes, and don't ask again" onayı komutu sırlarıyla birlikte `.claude/settings.local.json`'a yazıyor; 103.617 açık repoda 104.185 kopya, 1.122'sinde sır (1.379 farklı sır; 379 DB parolası, 23 AWS anahtarı); ilgili 4 hata kaydı bot tarafından kapatılmış, Anthropic yanıtı yok. İkincil (aiweekly; rakamlar K1): DeepSeek Flash tabanlı otonom saldırı aracı "Operation Snowball" (Avrupa telekom, CVE-2026-20320) ve DeepSeek V4.1 Flash/Kimi K3.1 Pro ile yürütülen ARTEX kampanyası (Check Point); Fireworks AI ikinci ihlal (24 Ekim saldırısı; müşteri sırları/veri).

### 13. DeepSeek V4-Pro / V4.1-Flash + DeepSeek Harness (dsh) + superagent prototipi
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-11-01 | Son kontrol: 2026-11-10 | Durum: Aktif
- Özet (08-07/11-01): V4-Pro GA; dsh; V4.1-Flash-1017 açık ağırlık (MIT, 763B, 1M bağlam); Search/Fetch API'leri. dsh-superagent-prototype (31 Ekim, MIT; Router + Worker proaktif kodlama ajanı). Yıldız (1 Kasım): harness 267.639.
  - 2026-11-04 (yıldız, 4 Kasım — anomali): dsh-superagent-prototype 17.449 (3 günde +%360,9).
  - 2026-11-10 (yıldız, 10 Kasım): harness 277.594 (1 Kasım'a göre 9 günde +%3,7); superagent 21.878 (4 Kasım'a göre 6 günde +%25,4 — anomali eşiği).

### 24. Yeni GitHub AI/agent repoları (her rapor çalışmasında tarama)
- İlk görülme: 2026-08-10 | Son güncelleme: 2026-11-10 | Son kontrol: 2026-11-10 | Durum: Aktif
- Özet (08-10/11-04): taramalar raporlarda. Öne çıkanlar: anatomy (23.444, 1 Kasım), huashu-motion, dsh-superagent, pixelfx, teardown, agent-autoloop (3 Kasım). ⚠️ Tekrarlayan desenler: sahte "free model"/sürüm, korsan installer, jailbreak/hile repoları.
  - 2026-11-07 (🟡, pencere 5-7 Kasım): pixel-gif-sticker-pack (572), vork (480), hermes-voice (459), ⚠️ poki (437), turkish-anti-ai-skill (234). Yıldız anomalisi (7 Kasım): agent-autoloop 3.755 (+%224,0), teardown 2.456, pixelfx 5.660, huashu-motion 2.462; shim/verdict/EXZA-Remote −%54–61.
  - 2026-11-10 (🟡, pencere 8-10 Kasım; 7 sonuç): gokayfem/image-to-sculpt (212), danyuchn/claude-work-mode (175), Dodaios/ste80-humanizer (162), stevenmichaelthomas/numbrone (110), Leonxlnx/escapement (104). ⚠️ roblox-studio-mcp (283; 6 KB, fork≈yıldız) ve valorant-ai-clip-editor (179) spam deseni.

### 25. AI imza/watermark temizleme araçları ve filigran tartışması
- İlk görülme: 2026-08-17 | Son güncelleme: 2026-11-04 | Son kontrol: 2026-11-10 | Durum: Aktif
- Özet (08-17/10-23): guillaumemeyer/watermarks-remover 12.177 → 24.680 (23 Eki); rakip ShadowAqueduct silindi.
  - 2026-11-01 (yıldız, 1 Kasım): 25.799 (9 günde +%4,5).
  - 2026-11-04 (🟡): Anthropic sürüm notu (3 Kasım): Mythos 5, Opus 4.7, Sonnet 4.6 metinleri Anthropic metin filigranı taşıyor; Sonnet 4.6'da varsayılan dışı örnekleme ayarlarıyla olmayabilir.
  - 2026-11-10 (yıldız, 10 Kasım): 26.908 (1 Kasım'a göre 9 günde +%4,3).

### 26. OpenAI GPT-6 ailesi ve ürünleri (Astra / Sol / Luna / 6.1 Sol / 6.1 Terra / Rosalind / Cyber, Dots, ChatGPT Space)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-07 | Son kontrol: 2026-11-10 | Durum: Aktif
- Özet (07-27/11-01): GPT-6 Astra ($10/$50), Sol ($2/$10), Luna ($0,10/$0,50); 6.1 Astra iptal; DevDay: Dots, 6.1 Sol, Space, Agents API. GPT-6.1 Terra ($1/$5). GPT-6 Rosalind Research (30 Ekim).
  - 2026-11-04 (⚪): Codex dökümlerinde "GPT-6.2-Astra" kimliği (söylenti).
  - 2026-11-07 (🟢): GPT-6 Cyber (5 Kasım; deploymentsafety.openai.com) — Astra'nın yetkili güvenlik varyantı; yalnızca onaylı Daybreak Red kuruluşları; siber "Critical", bio/kimya "High". İkincil: ChatGPT Images 2.6 (4 Kasım; K3); Community Compact → #42.

### 28. Meta Muse ailesi (Muse Spark, Muse Code, Muse ajan uygulaması, Muse Wonder, Muse Spark Open, Muse Ember)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-10 | Son kontrol: 2026-11-10 | Durum: Aktif
- Özet (07-27/10-29): Muse Spark 1.3; Muse ajan uygulaması (8 Eyl); Muse Wonder (12 Eki; API $4/$20); Muse Spark Open (#35); 10 milyon+ Muse hesabı.
  - 2026-11-07 (⚪): Muse asistanında ABD'de gerçek zamanlı ifadeli avatarlar (mobil/web/Mac). Meta Business kullanıcılarının sitelerini kazımaya izin veren 20 Kasım şart güncellemesini süresiz askıya aldı (Norveç/Brezilya tepkisi). İkisi de ikincil.
  - 2026-11-10 (🟡): Muse Ember (9 Kasım; research.meta.ai/blog/muse-ember) — ailenin ucuz/yüksek hacim katmanı; `muse-ember-1.0`, Muse Code + Meta Model API; $0,10/$0,50 (200K üstü $0,30/$1,50); 1M bağlam, 512K çıktı. Meta'nın ölçümü: AutomationBench-AA %37,8 (Haiku 5.5 %13,9), Terminal-Bench 4.0 %40,9 (Haiku 5.5 %39,2), FrontierCode 2.0-AA %27,2 (Haiku 5.5 %34,9).

### 29. Mistral AI (Series D, Mistral Large 4, CERN Flare, Studio)
- İlk görülme: 2026-09-14 | Son güncelleme: 2026-11-07 | Son kontrol: 2026-11-10 | Durum: Aktif (10-05 arşivlendi, 10-12 geri döndü)
- Özet (09-14/10-29): 3 milyar € Series D (8 Eyl); Large 4 public preview (6 Ekim); CERN "Flare".
  - 2026-11-01 (🟢): K3 (29 Ekim): Large 4 açık ağırlık — `mistralai/Mistral-Large-4-1T-A52B` (1T/52B aktif), "Mistral Ecosystem Open-Weight license"; API $0,70/$2,10; Terminal-Bench 4.0 %41 (Mistral).
  - 2026-11-07 (🟡): Mistral Studio genişletmesi (5 Kasım; mistral.ai/news/build-with-studio) — managed agents (skills, kod sandbox'ı, alt ajanlar, hook'lar), iş akışları, gözlemlenebilirlik, değerlendirme; Mistral MCP sunucusuyla tek komutla deploy; bulut/VPC/on-prem. Fiyat belirtilmemiş.

### 31. TypeSafe AI — Jev / "System One Models"
- İlk görülme: 2026-09-21 | Son güncelleme: 2026-10-26 | Son kontrol: 2026-11-10 | Durum: Aktif
- Özet (09-21/10-05): Jev (15 Eylül) — tipli/kalibre kararlar; Jev 1.13 OpenRouter'da.
  - 2026-10-17 (⚪): Jev 1.14.0 (14 Ekim).
  - 2026-10-26 (🟡): Veri sızıntısı (24 Ekim) — tüm müşterilerin Jev çıktıları sızdı. Postmortem yok.

### 33. Always-on kişisel/iş ajanları (OpenAI Dots, Meta Muse, ChatGPT Space, Claude Duet, Perplexity Teammates; açık kaynak: OpenDots, nanoMuse)
- İlk görülme: 2026-10-05 | Son güncelleme: 2026-11-07 | Son kontrol: 2026-11-10 | Durum: Aktif
  - 2026-10-05 (🟢) — İLK TAKİP: OpenAI Dots (29 Eylül) ile kategori ana akım oldu.
  - 2026-10-23 (🟢): Claude Duet (21 Ekim; #2) — üç büyük laboratuvarda da always-on ajan var.
  - 2026-11-07 (🟡): Perplexity Teammates — Max abonelerine web'de always-on iş ajanları; Rerun açık kaynak self-host seçeneği ekledi (The Neuron; ikincil).

### 34. Frontier güvenlik olayları, duraklatmalar ve düzenleyici yanıt (OpenAI eğitim durdurma/dönüş, rogue-model olayları, SI Force, FTC, RSI eşiği, METR)
- İlk görülme: 2026-09-28 | Son güncelleme: 2026-11-10 | Son kontrol: 2026-11-10 | Durum: Aktif
- Özet (09-28/11-04): OpenAI eğitim duraklaması ve dönüşü (23 Ekim); SI Force, FTC CID'leri; Newsom kararnamesi (rehber ~18 Kasım). Anthropic S-1/A: RSP "dramatik hızlanma" eşiğine "may imminently meet".
  - 2026-11-07 (🟢): METR bağımsız değerlendirmesi (5 Kasım; erişim 12 Ağu–29 Eki): Anthropic AECI ilerlemesi Ekim 2025'ten beri 1,9 kat (%95 GA 1,5–2,8); hızlanmanın ≈%80'i AI kaynaklı; kanıtların çoğu karartıldı. ABD DOJ Super Intelligence Task Force (6 Kasım; ikincil).
  - 2026-11-10 (⚪): Trump AI risklerinin "yönetilebilir" olduğunu söyleyip Demokratlarla koruma önlemlerine açık olduğunu işaret etti (Reuters, 9 Kasım; ikincil). Senato savunma yasası taslağında Çin'e giden AI çiplerine Kongre denetimi ve yurtdışı çip takibi (ikincil).

### 35. ABD açık/lisanslı ağırlık yarışı (Muse Spark Open, Reflection Beam, MAI-Base-2, Inkling 2)
- İlk görülme: 2026-10-17 | Son güncelleme: 2026-11-07 | Son kontrol: 2026-11-10 | Durum: Aktif
  - 2026-10-17 (🟢) — İLK TAKİP: Reflection AI Beam (16 Ekim; 501B/23B aktif, Apache 2.0), Microsoft MAI-Base-2 (15 Ekim; Foundry lisanslı), Meta Muse Spark Open (#28).
  - 2026-11-07 (🟡): Thinking Machines Inkling 2 Small (5 Kasım; thinkingmachines.ai) — 594B toplam / 17B aktif MoE, görsel girdi; şimdilik Tinker'da kapalı ağırlık, dış güvenlik testlerinden sonra "gelecek hafta" Apache 2.0 tam ağırlık niyeti. Sonraki çalışmada teyit edilecek. (10 Kasım: ağırlık yayımına dair kanıt bulunamadı; HF sayfası açılamadı, K2.)

### 37. AI destekli zafiyet keşfi (PHP2Shell, Node2Shell, Codex Security, Wiz Atlas, GPT-6 Cyber, Mythos 5.2)
- İlk görülme: 2026-10-23 | Son güncelleme: 2026-11-10 | Son kontrol: 2026-11-10 | Durum: Aktif
- Özet (10-23/10-29): PHP2Shell (CVE-2026-109618/109619) — Calif, Codex Security, Wiz bağımsız buldu; OpenAI php2shell-checker (yıldız 4 Kasım: 1.460); CISA KEV (26 Ekim). K3: Node2Shell (CVE-2026-111497, CVSS 9,2).
  - 2026-11-07 (🟡): GPT-6 Cyber (#26) — exploit geliştirmeye izinli, Daybreak Red ile sınırlı. OpenAI siber modelinin çok sayıda Linux yerel yetki yükseltme hatası bulduğu bildirildi (aiweekly; K1).
  - 2026-11-10 (🟡): Claude Mythos 5.2 (9 Kasım; #2) — CVE Rediscovery %89,6; Opus 5.5'ten "%10,2 daha fazla zafiyet" (Anthropic). Yalnızca Cyber Verification Program / Claude Security üzerinden.

### 38. Kimi (Moonshot) — K3 → K3.1 Pro
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-07 | Son kontrol: 2026-11-10 | Durum: Aktif (08-31 arşivlendi, 10-26 geri döndü)
- Özet (07-27/11-04): K3.1 Pro + Highspeed (23 Ekim), API `kimi-k3.1-pro`, 1M bağlam. K2 serisi emeklilik Aralık sonu.
  - 2026-11-07 (🟢): Ağırlıklar yayımlandı — `moonshotai/Kimi-K3.1-Pro` (HF model sayfası): 2,8T toplam / 104B aktif, 93 katman, 896 uzman (token başına 16), 1.048.576 bağlam, MoonViT-V2 görsel kodlayıcı, MXFP4 ağırlık; lisans "Kimi K3.1 Pro License" (özel). Yayın 4 Kasım (ikincil).

### 39. AI ile matematik/bilim keşif iddiaları ve doğrulama (OpenAI ETH/Kakeya/Yang–Mills, Axiom CFSG, Fable 5.2 FLT)
- İlk görülme: 2026-10-29 | Son güncelleme: 2026-11-10 | Son kontrol: 2026-11-10 | Durum: Aktif
  - 2026-10-29 (🟢) — İLK TAKİP: K3 (26 Ekim): OpenAI ETH çürütme, local smoothing ve 4B Yang–Mills/QCD varlık sonuçları (Lean açık; Millennium çözülmedi). Axiom CFSG Lean formalizasyonu (133 ⭐). Bağımsız teyit bekleniyor.
  - 2026-11-07 (yıldız, 7 Kasım): AxiomMath/CFSG 163 (29 Ekim'e göre 9 günde +%22,6).
  - 2026-11-10 (🟢): Anthropic (9 Kasım): 1.000 Fable 5.2 ajanı Fermat'nın Son Teoremi ispatını "minimal insan müdahalesiyle" 30 saatte formalize etti; ilk formalizasyon yayımlanmamış bir araştırma sürümüyle 11 gün sürmüş; Opus 5.5 aynı düzende 18 saatte %26. Tek koşu, şirket iddiası; bağımsız teyit yok. İkincil: iki açık teorik fizik problemi çözüldü iddiası (K1).

### 40. AI eğitim tercihi sinyali / yayıncı opt-out standardı (robots.txt token, IETF taslağı)
- İlk görülme: 2026-11-01 | Son güncelleme: 2026-11-01 | Son kontrol: 2026-11-10 | Durum: Aktif
  - 2026-11-01 (🟡) — İLK TAKİP: OpenAI, Google, Microsoft, Anthropic (30 Ekim) ortak eğitim tercihi sinyalini destekliyor; IETF taslağı `draft-kelley-aipref-training-preference-signal` (onaysız, gönüllü). Microsoft'ta 1 Şubat 2027'de yürürlükte.

### 41. Meituan LongCat model ailesi
- İlk görülme: 2026-11-04 | Son güncelleme: 2026-11-04 | Son kontrol: 2026-11-10 | Durum: Aktif
  - 2026-11-04 (🟡) — İLK TAKİP: LongCat-2.5 Preview (2 Kasım; TechNode) — ajan kodlama için çok modlu; 1,6T / ~48B aktif; sohbet ve API'de, açık ağırlık henüz yok.

### 42. AI veri merkezi altyapısına yerel tepki, enerji ve piyasa etkisi
- İlk görülme: 2026-11-07 | Son güncelleme: 2026-11-10 | Son kontrol: 2026-11-10 | Durum: Aktif
  - 2026-11-07 (🟡) — İLK TAKİP: ABD seçimlerinde (3 Kasım) yerel oylamaların çoğu veri merkezi kısıtlamasını destekledi. OpenAI "National Community Compact" (5 Kasım): veri merkezlerinde elektrik/altyapı maliyetini üstlenme, kamu görevlileriyle NDA yok. Çip hisselerinde sert satış. aiweekly aktarımı (CNBC/FT); rakamlar K1.
  - 2026-11-10 (🟡): Anthropic'in OnePWR'ın 1,7 GW gaz jeneratörü siparişlerini devraldığı bildirildi (FT/CNBC, 8 Kasım; tutar K1, şirketler teyit etmedi). SpaceX, Starbase'de gaz santralli süper bilgisayar tesisi için vergi indirimi başvurusu (xAI; ikincil).

## Arşivlenmiş Konular

(Geri dönüş olmadıkça satır eklenmez. Tam geçmiş git commit'lerinde.)

- **Vercel fx / libfx / fx0 [#27]** — İlk 08-24 | Son güncelleme 10-20 | Arşiv 11-10. Zig ile minimal kodlama ajanı; fx0 tasarım ajanı (19 Ekim). Son yıldızlar (10 Kasım): fx 3.801 (1 Kasım'a göre 9 günde +%2,8), fx0 431 (+%3,1).
- **AB AI Act uygulama takvimi ve standartları [#36]** — İlk 08-07 | Son güncelleme 10-20 | Arşiv 11-10. Madde 50/yüksek riskli hükümler Ağustos'ta yürürlükte; ilk uyumlaştırılmış standart EN 18286:2026 (19 Ekim).
- **Prime Agent (Prime Intellect) [#17]** — İlk 08-08 | Son güncelleme 10-12 | Arşiv 11-04. ARC-AGI-3 %95,5, MIT. Son yıldız (4 Kasım): prime-agent 22.557.
- **AI ajan mimarisi/hafıza yaklaşımları [#20]** — İlk 08-08 | Son güncelleme 10-12 | Arşiv 11-04. Son yıldızlar (4 Kasım): tigerless-labs/agent-memory 4.303, okf-agent-memory 851, AgentMemoryRepo 847, elstongun/leviathan 881.
- **Z.ai (Zhipu) ZCode ve GLM dikey modelleri [#32]** — İlk 09-21 | Son güncelleme 10-12 | Arşiv 11-04. ZCode açık kaynak (20 Eylül), GLM-Legal (12 Ekim). Son yıldız (4 Kasım): 8.461.
- **Yerel/açık kaynak Cowork ve kişisel ajan alternatifleri (Goose, Eigent, ZCode, OpenDots, nanoMuse) [#22]** — İlk 08-10 | Son güncelleme 10-05 | Arşiv 10-26. Son yıldızlar (26 Ekim): eigent 15.662, OpenDots 6.013, nanoMuse 2.600. Eğilim #33'te.
- **Grok 4.6 → 4.7 (xAI) [#30]** — İlk 07-27 | Son güncelleme 09-28 | Arşiv 10-20. Grok 4.7 (21 Eylül). Grok 5 çıkarsa geri döner.
- **Eski arşiv (tek satır):** Anthropic Cowork (arşiv 09-21; #2), Salesforce Slackbot/Claudeforce (09-21), ChatGPT for Work & GPT-Live (08-17; #26/#33), OptMem (08-17), Sakana Fugu-Cyber (08-17), x402 ödeme altyapısı (08-31), Mistral Shieldstral (08-31; #29), DiffusionGemma/MiniMax H3 (08-31), Gemini liderlik değişikliği (09-07; #3).
- **OpenAI Astra (matematik modeli — GPT-6 Astra ile KARIŞTIRILMASIN)** — İlk 08-07 | Son 08-10 | Arşiv 08-31. Yeni matematik iddiaları #39'da.

## Değişiklik Geçmişi

- 2026-08-10 – 2026-10-26: bkz. git geçmişi (08-10'da bu repoya taşındı; 10-16'da 3 günlük ritim, kapı, "Son kontrol"/yıldız/BEKLEYEN NOT kuralları, `gorev-talimati.md`).
- 2026-10-29 (pencere 27-29 Ekim): +1 konu (#39); 9 güncelleme; 0 arşiv; 5 K3; sıkıştırma → ~24,8 KB.
- 2026-11-01 (pencere 30 Ekim–1 Kasım): +1 konu (#40); #6 arşivden döndü; 9 güncelleme; 0 arşiv; 2 K3; yıldız satırları (9 gün); sıkıştırma → ~24,2 KB.
- 2026-11-04 (pencere 2-4 Kasım): +1 konu (#41); 8 güncelleme; 3 arşiv (#17, #20, #32); yıldız anomalileri (dsh-superagent, teardown, pixelfx); 1 K3; sıkıştırma → ~24,7 KB.
- 2026-11-07 (pencere 5-7 Kasım): +1 konu (#42); 12 güncelleme; 0 arşiv; #27/#36 arşiv adayı. Yıldız anomalileri: agent-autoloop +%224,0; shim/verdict/EXZA-Remote −%54–61. K2: WebFetch yok (alt ajan). Sıkıştırma.
- 2026-11-10 (pencere 8-10 Kasım): 0 yeni konu; 9 güncelleme (#2 Fable/Mythos 5.2, #3 TPU 8, #12 Claude Code sır sızıntısı (K3), #24, #28 Muse Ember, #34, #37, #39 FLT, #42); 2 arşiv (#27, #36). Yıldız satırları: #13 (superagent +%25,4 anomali), #25. Inkling 2 ağırlıkları teyit edilemedi (HF K2). google/elephant-goldfish-model: WebFetch 13,4k dedi, API 16.642 (K1 uyarısı doğrulandı). WebFetch alt ajan üzerinden. Sıkıştırma ~26,9 → ~24,5 KB (≤20 KB hedefine kurallar ve arşiv bölümü yüzünden ulaşılamadı). BEKLEYEN NOT yoktu.
