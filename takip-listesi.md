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

### 2. Anthropic modelleri, ürünleri ve kurumsal/güvenlik gelişmeleri (Claude 5.5 ailesi; Fable/Mythos 5.2; Duet; Sheets/Whiteboards/Data; IPO; Max/Ultra)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-13 | Son kontrol: 2026-11-13 | Durum: Aktif
- Özet (07-27/11-04): Fable 5, Opus 5, Sonnet 5; Cowork; 5.5 ailesi: Opus ($4/$20), Sonnet ($2/$10), Haiku ($0,10/$0,50). Claude Duet (21 Eki; #33); Enterprise Chat+Cowork (16 Kasım). S-1/S-1/A; Max ($100)/Ultra ($200); FlashProve.
  - 2026-11-07 (🟡): AP seçim verisi anlaşması; Claude Personal Finance beta; Cat Wu OpenAI'ye geçti (ikincil). METR → #34.
  - 2026-11-10 (🟢): Claude Fable 5.2 + Mythos 5.2 (9 Kasım) — $8/$40; FrontierCode 2.0 Xhigh %49,1, OSWorld 2.1 %89,3, HLE (araçlı) %74,2; Mythos yalnızca doğrulanmış kuruluşlara. FLT → #39; CVE Rediscovery → #37; jeneratör → #42; sır sızıntısı → #12.
  - 2026-11-13 (🟢): K3 (10 Kasım; anthropic.com/news/roadshow-launch): IPO roadshow — 825.000.000 Class A hisse (801.351.354 Anthropic, 23.648.646 mevcut ortaklar), +123.750.000 opsiyon, $70–78, Nasdaq "ANT", liste tarihi yok. K3 (10 Kasım; claude.com): Claude Sheets, Whiteboards, Claude Data (eski Dashboards), etkileşimli connector'lar (Adobe, Atlassian); Meetings "yakında". "Worse Together" (11 Kasım; alignment.anthropic.com): tek koordinatör ajan kişi başı ajanlardan ort. 10–45 puan iyi; MAMUBench. İkincil: kullanım sıfırlama (10 Aralık'a kadar); TSMC yatırımı (K1); Claude Meetings beta.

### 3. Gemini ailesi ve Google DeepMind (Gemini 4 Argon/Carbon, Decisions API, Genie 4, Omni, TPU 8, AlphaGenome 2)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-13 | Son kontrol: 2026-11-13 | Durum: Aktif (09-28 arşivlendi, 10-05 geri döndü)
- Özet (07-27/10-29): Gemini 4 Argon GA 13 Ekim — $2/$10 tanıtım 30 Kasım'a kadar, sonra $4/$20. Genie 4 (27 Ekim).
  - 2026-11-07 (🟡): Gemini Omni 1.2 Flash GA (5 Kasım) — klip 3–15 sn, 720p $0,07/sn; SynthID.
  - 2026-11-10 (⚪): TPU 8tx (gizli çıkarım) ve TPU 8i Max duyuruldu (9 Kasım); çıkış tarihi yok.
  - 2026-11-13 (🟢): K3 (10 Kasım; blog.google): Gemini 4 Carbon — ücretli API + AI Ultra (Antigravity, Gemini app, AI Mode); tanıtım $2/$10, 30 Kasım sonrası $4/$20; CursorBench 4.0, WANDR, AutomationBench'te "#1" (skor yok); /swarm önizleme. Gemini Decisions API (11 Kasım): `gemini-decision-1`, $0,10/1M girdi, çıktı $0; istek başına 1.000 soru, 256K girdi. AlphaGenome 2 (11 Kasım): TenK10K nedensel varyant %30 (önceki %16), ticari olmayan araştırma API'si. AlphaProof Code → #39.

### 6. Qwen serisi (Alibaba: 3.8 ailesi, QwenWork, Qwen 4; Apple Intelligence Çin)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-13 | Son kontrol: 2026-11-13 | Durum: Aktif (10-20 arşivlendi, 11-01 geri döndü)
- Özet (07-27/11-01): 3.8 ailesi, QwenWork; Qwen 4 duyurusu (22 Eyl). Apple–Alibaba (31 Ekim; ikincil).
  - 2026-11-04 (⚪): Qwen 4 yayınlanmadı; 16/18 Kasım söylentileri.
  - 2026-11-07 (⚪): Qwen ekibi Qwen 4/5'in açık ağırlık kalacağını söyledi (ikincil). Foundry Local Qwen3.8-27B.
  - 2026-11-13 (🟢): Qwen4-Max-Preview (11 Kasım 10:00 UTC+8; docs.qwencloud.com) — 1M bağlam, 393.216 maks. çıktı, görsel/video anlama, araçlar, OpenAI/Anthropic API uyumlu; yalnızca Token Plan, 25 Kasım'a kadar, sonra kaldırılacak. Fiyat ve açık ağırlık belirtilmemiş.

### 12. AI ajan güvenlik açıkları (sandbox kaçışları, framework RCE, anahtar/veri sızıntıları, tedarik zinciri, AI ile otonom saldırılar) ve savunma araçları
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-11-13 | Son kontrol: 2026-11-13 | Durum: Aktif
- Özet (08-07/11-01): CISA 12 framework RCE; Cursor CVE'leri; CVE-2026-82533 (dsh); Archon CVE-2026-111322; OpenCode ihlali; sahte AGENTS.md npm; kurcalanmış Claude Code eklentisi 2.1.313.
  - 2026-11-04 (🟡): K3: Postman Desktop 12.33.4 sormadan hook kuruyor. OpenAI–Cathedral; Apple 10-K ajan riski.
  - 2026-11-10 (🟢): K3 (7 Kasım; Apiiro): Claude Code "don't ask again" sırları `.claude/settings.local.json`'a yazıyor; 1.122 açık repoda sır. İkincil: Operation Snowball, ARTEX kampanyası, Fireworks AI ikinci ihlal.
  - 2026-11-13 (🟡): İkincil (rakamlar K1): Microsoft Research "Lazarus" — 10'dan az uyuyan nöronla ajana arka kapı; Arctic Wolf: ARTEX fork'u AntiFox ile AWS kimlik bilgisi hırsızlığı (12 Kasım); Railway ihlali sonrası sahte AI harcamaları (BleepingComputer K2); Claude/Codex IoT tersine mühendisliğini engelliyor → #43. Perplexity sandbox kaçış testleri (part II).

### 13. DeepSeek V4-Pro / V4.1-Flash + DeepSeek Harness (dsh) + superagent prototipi
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-11-01 | Son kontrol: 2026-11-13 | Durum: Aktif
- Özet (08-07/11-01): V4-Pro GA; dsh; V4.1-Flash-1017 açık ağırlık (MIT, 763B, 1M bağlam); Search/Fetch API'leri. dsh-superagent-prototype (31 Ekim, MIT). Yıldız (1 Kasım): harness 267.639.
  - 2026-11-04 (yıldız, 4 Kasım — anomali): dsh-superagent-prototype 17.449 (3 günde +%360,9).
  - 2026-11-10 (yıldız, 10 Kasım): harness 277.594 (9 günde +%3,7); superagent 21.878 (6 günde +%25,4 — anomali eşiği).

### 24. Yeni GitHub AI/agent repoları (her rapor çalışmasında tarama)
- İlk görülme: 2026-08-10 | Son güncelleme: 2026-11-13 | Son kontrol: 2026-11-13 | Durum: Aktif
- Özet (08-10/11-04): taramalar raporlarda. Öne çıkanlar: anatomy, huashu-motion, dsh-superagent, pixelfx, teardown, agent-autoloop. ⚠️ Tekrarlayan desenler: sahte "free model"/sürüm, korsan installer, jailbreak/hile repoları.
  - 2026-11-07 (🟡, 5-7 Kasım): pixel-gif-sticker-pack (572), vork (480), hermes-voice (459), ⚠️ poki (437), turkish-anti-ai-skill (234). Anomali: agent-autoloop +%224,0; shim/verdict/EXZA-Remote −%54–61.
  - 2026-11-10 (🟡, 8-10 Kasım): image-to-sculpt (212), claude-work-mode (175), ste80-humanizer (162), numbrone (110), escapement (104). ⚠️ roblox-studio-mcp, valorant-ai-clip-editor.
  - 2026-11-13 (🟡, 11-13 Kasım; 26 sonuç): apex-compute/ANR (1.080), op7418/guizang-game-skill (264), nickvasilescu/bot-hq (154), AFangTeam/PrintLab (148), lawandrorder/mate (138). ⚠️ ai-texture-forge (292) ve Hyperliquid-Trade-Bot (289): "crack"/anahtar kelime doldurulmuş topic'ler.

### 25. AI imza/watermark temizleme araçları ve filigran tartışması
- İlk görülme: 2026-08-17 | Son güncelleme: 2026-11-04 | Son kontrol: 2026-11-13 | Durum: Aktif
- Özet (08-17/10-23): guillaumemeyer/watermarks-remover 12.177 → 24.680 (23 Eki); rakip ShadowAqueduct silindi.
  - 2026-11-01 (yıldız, 1 Kasım): 25.799 (9 günde +%4,5).
  - 2026-11-04 (🟡): Anthropic sürüm notu (3 Kasım): Mythos 5, Opus 4.7, Sonnet 4.6 metinleri Anthropic metin filigranı taşıyor.
  - 2026-11-10 (yıldız, 10 Kasım): 26.908 (9 günde +%4,3).

### 26. OpenAI GPT-6 ailesi ve ürünleri (Astra / Sol / Luna / 6.1 Sol / 6.1 Terra / Rosalind / Cyber, Dots, ChatGPT Space, Businesses)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-13 | Son kontrol: 2026-11-13 | Durum: Aktif
- Özet (07-27/11-01): GPT-6 Astra ($10/$50), Sol ($2/$10), Luna ($0,10/$0,50); 6.1 Astra iptal; DevDay: Dots, 6.1 Sol, Space, Agents API. GPT-6.1 Terra ($1/$5). Rosalind Research (30 Ekim).
  - 2026-11-04 (⚪): "GPT-6.2-Astra" kimliği (söylenti).
  - 2026-11-07 (🟢): GPT-6 Cyber (5 Kasım) — yalnızca Daybreak Red; siber "Critical". İkincil: Images 2.6; Community Compact → #42.
  - 2026-11-13 (🟡): İkincil: "Businesses in ChatGPT" beta (11 Kasım; doğrulanmış işletme profilleri, Business Agents, ABD'de reklam olarak satış); Advanced/Standard Voice 11 Aralık'ta emekli → Live Voice; Odessia satın alındı (10 Kasım).

### 28. Meta Muse ailesi (Muse Spark, Muse Code, Muse ajan uygulaması, Muse Wonder, Muse Spark Open, Muse Ember)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-10 | Son kontrol: 2026-11-13 | Durum: Aktif
- Özet (07-27/10-29): Muse Spark 1.3; Muse ajan uygulaması (8 Eyl); Muse Wonder (12 Eki; API $4/$20); Muse Spark Open (#35); 10 milyon+ Muse hesabı.
  - 2026-11-07 (⚪): Muse'da ifadeli avatarlar; site kazıma şart güncellemesi askıya alındı (ikincil).
  - 2026-11-10 (🟡): Muse Ember (9 Kasım) — $0,10/$0,50 (200K üstü $0,30/$1,50); 1M bağlam, 512K çıktı; AutomationBench-AA %37,8, Terminal-Bench 4.0 %40,9, FrontierCode 2.0-AA %27,2 (Meta).

### 29. Mistral AI (Series D, Mistral Large 4, CERN Flare, Studio)
- İlk görülme: 2026-09-14 | Son güncelleme: 2026-11-07 | Son kontrol: 2026-11-13 | Durum: Aktif (10-05 arşivlendi, 10-12 geri döndü)
- Özet (09-14/10-29): 3 milyar € Series D (8 Eyl); Large 4 public preview (6 Ekim); CERN "Flare".
  - 2026-11-01 (🟢): K3 (29 Ekim): Large 4 açık ağırlık — 1T/52B aktif, "Mistral Ecosystem Open-Weight license"; API $0,70/$2,10.
  - 2026-11-07 (🟡): Mistral Studio genişletmesi (5 Kasım) — managed agents, iş akışları, değerlendirme; bulut/VPC/on-prem.

### 31. TypeSafe AI — Jev / "System One Models"
- İlk görülme: 2026-09-21 | Son güncelleme: 2026-10-26 | Son kontrol: 2026-11-13 | Durum: Aktif
- Özet (09-21/10-05): Jev (15 Eylül) — tipli/kalibre kararlar; Jev 1.13 OpenRouter'da.
  - 2026-10-17 (⚪): Jev 1.14.0 (14 Ekim).
  - 2026-10-26 (🟡): Veri sızıntısı (24 Ekim) — tüm müşterilerin Jev çıktıları sızdı. Postmortem yok.

### 33. Always-on kişisel/iş ajanları (OpenAI Dots, Meta Muse, ChatGPT Space, Claude Duet, Perplexity Teammates, Databricks Genie, ByteDance; açık kaynak: OpenDots, nanoMuse)
- İlk görülme: 2026-10-05 | Son güncelleme: 2026-11-13 | Son kontrol: 2026-11-13 | Durum: Aktif
- Özet (10-05): OpenAI Dots (29 Eylül) ile kategori ana akım oldu.
  - 2026-10-23 (🟢): Claude Duet (21 Ekim; #2) — üç büyük laboratuvarda da always-on ajan var.
  - 2026-11-07 (🟡): Perplexity Teammates; Rerun self-host (ikincil).
  - 2026-11-13 (🟡): İkincil: ByteDance "haftalar içinde" Muse benzeri ajan (Bloomberg, 11 Kasım); Databricks Genie arka planda always-on + Ontology (11 Kasım); n8n Nod açık kaynak kişisel ajan.

### 34. Frontier güvenlik olayları, duraklatmalar ve düzenleyici yanıt (OpenAI eğitim durdurma/dönüş, SI Force, FTC, RSI eşiği, METR, NY RAISE, Avustralya)
- İlk görülme: 2026-09-28 | Son güncelleme: 2026-11-13 | Son kontrol: 2026-11-13 | Durum: Aktif
- Özet (09-28/11-04): OpenAI eğitim duraklaması ve dönüşü (23 Ekim); SI Force, FTC CID'leri; Newsom kararnamesi (rehber ~18 Kasım). Anthropic S-1/A: RSP "may imminently meet".
  - 2026-11-07 (🟢): METR (5 Kasım): Anthropic AECI ilerlemesi 1,9 kat (%95 GA 1,5–2,8); ≈%80 AI kaynaklı. ABD DOJ Super Intelligence Task Force (ikincil).
  - 2026-11-10 (⚪): Trump AI risklerini "yönetilebilir" buldu; Senato savunma yasası taslağında çip denetimi (ikincil).
  - 2026-11-13 (🟡): İkincil: New York RAISE Yasası frontier geliştirici kayıt portalı açıldı (10 Kasım; son tarih 1 Ocak 2027); NY eyalet AI test programı; Avustralya AI güvenlik düzenleyicisi planı (OpenAI ajanı Medicare olayı); ABD–Çin olay kanalı görüşmeleri; Demokratların AI eğitim izni taslağı.

### 35. ABD açık/lisanslı ağırlık yarışı (Muse Spark Open, Reflection Beam, MAI-Base-2, Inkling 2)
- İlk görülme: 2026-10-17 | Son güncelleme: 2026-11-07 | Son kontrol: 2026-11-13 | Durum: Aktif
  - 2026-10-17 (🟢) — İLK TAKİP: Reflection AI Beam (501B/23B, Apache 2.0), Microsoft MAI-Base-2, Meta Muse Spark Open (#28).
  - 2026-11-07 (🟡): Thinking Machines Inkling 2 Small (5 Kasım) — 594B/17B aktif MoE; Tinker'da kapalı ağırlık, "gelecek hafta" Apache 2.0 niyeti. (10 ve 13 Kasım: ağırlık yayımı teyit edilemedi, kaynaklar açılamadı, K2.)

### 37. AI destekli zafiyet keşfi (PHP2Shell, Node2Shell, Codex Security, Wiz Atlas, GPT-6 Cyber, Mythos 5.2)
- İlk görülme: 2026-10-23 | Son güncelleme: 2026-11-10 | Son kontrol: 2026-11-13 | Durum: Aktif
- Özet (10-23/10-29): PHP2Shell (CVE-2026-109618/109619) — Calif, Codex Security, Wiz bağımsız buldu; OpenAI php2shell-checker; CISA KEV (26 Ekim). K3: Node2Shell (CVE-2026-111497, CVSS 9,2).
  - 2026-11-07 (🟡): GPT-6 Cyber (#26) — exploit geliştirmeye izinli, Daybreak Red ile sınırlı.
  - 2026-11-10 (🟡): Claude Mythos 5.2 (9 Kasım; #2) — CVE Rediscovery %89,6.
  - 2026-11-13 (yıldız, 13 Kasım): php2shell-checker 1.470 (4 Kasım 1.460'a göre 9 günde +%0,7).

### 38. Kimi (Moonshot) — K3 → K3.1 Pro
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-07 | Son kontrol: 2026-11-13 | Durum: Aktif (08-31 arşivlendi, 10-26 geri döndü)
- Özet (07-27/11-04): K3.1 Pro + Highspeed (23 Ekim), API `kimi-k3.1-pro`, 1M bağlam. K2 serisi emeklilik Aralık sonu.
  - 2026-11-07 (🟢): Ağırlıklar yayımlandı — `moonshotai/Kimi-K3.1-Pro`: 2,8T / 104B aktif, 1.048.576 bağlam, MXFP4; lisans "Kimi K3.1 Pro License" (özel).

### 39. AI ile matematik/bilim keşif ve biçimsel doğrulama (OpenAI ETH/Yang–Mills, Axiom CFSG, Fable 5.2 FLT, AlphaProof Code)
- İlk görülme: 2026-10-29 | Son güncelleme: 2026-11-13 | Son kontrol: 2026-11-13 | Durum: Aktif
- Özet (10-29): K3 (26 Ekim): OpenAI ETH çürütme, local smoothing, 4B Yang–Mills/QCD varlık sonuçları (Lean açık). Axiom CFSG Lean formalizasyonu. Bağımsız teyit bekleniyor.
  - 2026-11-07 (yıldız, 7 Kasım): AxiomMath/CFSG 163 (9 günde +%22,6).
  - 2026-11-10 (🟢): Anthropic (9 Kasım): 1.000 Fable 5.2 ajanı FLT ispatını 30 saatte formalize etti (şirket iddiası, bağımsız teyit yok).
  - 2026-11-13 (🟡): K3 (10 Kasım; deepmind.google/blog/introducing-alphaproof-code): AlphaProof Code, Signal protokolünün cihazda çalışan kodunun temel güvenlik özelliklerini Lean'de 4 haftada kanıtladı; Gemini Carbon tabanlı; satır sayısı sayfada çelişkili ("over six million" / "over three million"); doğrulama artefaktları açık. Yeniden eklenmiş 2 eski hatayı yakaladı.

### 40. AI eğitim tercihi sinyali / yayıncı opt-out standardı (robots.txt token, IETF taslağı)
- İlk görülme: 2026-11-01 | Son güncelleme: 2026-11-01 | Son kontrol: 2026-11-13 | Durum: Aktif
  - 2026-11-01 (🟡) — İLK TAKİP: OpenAI, Google, Microsoft, Anthropic (30 Ekim) ortak eğitim tercihi sinyalini destekliyor; IETF taslağı `draft-kelley-aipref-training-preference-signal`. Microsoft'ta 1 Şubat 2027'de yürürlükte.

### 41. Meituan LongCat model ailesi
- İlk görülme: 2026-11-04 | Son güncelleme: 2026-11-04 | Son kontrol: 2026-11-13 | Durum: Aktif
  - 2026-11-04 (🟡) — İLK TAKİP: LongCat-2.5 Preview (2 Kasım; TechNode) — 1,6T / ~48B aktif; açık ağırlık henüz yok.

### 42. AI veri merkezi altyapısına yerel tepki, enerji ve piyasa etkisi
- İlk görülme: 2026-11-07 | Son güncelleme: 2026-11-13 | Son kontrol: 2026-11-13 | Durum: Aktif
  - 2026-11-07 (🟡) — İLK TAKİP: ABD yerel oylamalarında veri merkezi kısıtlamalarına destek; OpenAI "National Community Compact" (5 Kasım); çip hisselerinde satış (rakamlar K1).
  - 2026-11-10 (🟡): Anthropic'in OnePWR gaz jeneratörü siparişlerini devraldığı bildirildi (FT/CNBC; K1). SpaceX/xAI Starbase vergi indirimi başvurusu (ikincil).
  - 2026-11-13 (🟡): İkincil (rakamlar K1): Nvidia yönetim kurulunun Jensen Huang'ı görevden almaya hazırlandığı (WSJ, 12 Kasım); CoreWeave ön ödeme istiyor; EIA 2026–27 rekor elektrik talebi; Fed Bowman AI değerleme uyarısı.

### 43. Ajanlarla tersine mühendislik (REA ekosistemi) ve laboratuvar kısıtlamaları
- İlk görülme: 2026-11-13 | Son güncelleme: 2026-11-13 | Son kontrol: 2026-11-13 | Durum: Aktif
  - 2026-11-13 (🟡) — İLK TAKİP: Claude ve Codex, ajanları akıllı TV/bebek monitörü/IoT cihazlarına yönelten kullanıcıları güvenlik bloklarıyla durduruyor veya hesap kapatıyor (404 Media aktarımı, 10 Kasım; ikincil). Yıldız (13 Kasım, API): morluto/rea 455.826 (bülten "342.000" diyordu, K1); aicodeking/leanrea 4.240; JoasASantos/REA-Prompts 4.007.

### 44. MiniMax H3 ailesi (arşivden döndü: eski "DiffusionGemma/MiniMax H3", 08-31)
- İlk görülme: 2026-08-31 öncesi | Son güncelleme: 2026-11-13 | Son kontrol: 2026-11-13 | Durum: Aktif (08-31 arşivlendi, 11-13 geri döndü)
  - 2026-11-13 (🟡): MiniMax H3-Image (11 Kasım; minimax.io/blog/minimax-h3-image) — H3 tabanlı açık ağırlık görsel üretim/düzenleme (HF: MiniMaxAI/MiniMax-H3-Image); 4K "under 10 seconds", 16'ya kadar referans görsel; lisans adı sayfada yok; API, MiniMax Code, Hailuo AI.

## Arşivlenmiş Konular

(Geri dönüş olmadıkça satır eklenmez. Tam geçmiş git commit'lerinde.)

- **Vercel fx / libfx / fx0 [#27]** — İlk 08-24 | Son güncelleme 10-20 | Arşiv 11-10. Zig ile minimal kodlama ajanı; fx0 tasarım ajanı (19 Ekim). Son yıldızlar (10 Kasım): fx 3.801, fx0 431.
- **AB AI Act uygulama takvimi ve standartları [#36]** — İlk 08-07 | Son güncelleme 10-20 | Arşiv 11-10. Madde 50/yüksek riskli hükümler Ağustos'ta yürürlükte; EN 18286:2026 (19 Ekim).
- **Prime Agent (Prime Intellect) [#17]** — İlk 08-08 | Son güncelleme 10-12 | Arşiv 11-04. ARC-AGI-3 %95,5, MIT. Son yıldız (4 Kasım): 22.557.
- **AI ajan mimarisi/hafıza yaklaşımları [#20]** — İlk 08-08 | Son güncelleme 10-12 | Arşiv 11-04. Son yıldızlar (4 Kasım): agent-memory 4.303, okf-agent-memory 851, AgentMemoryRepo 847, leviathan 881.
- **Z.ai (Zhipu) ZCode ve GLM dikey modelleri [#32]** — İlk 09-21 | Son güncelleme 10-12 | Arşiv 11-04. ZCode açık kaynak (20 Eylül), GLM-Legal (12 Ekim). Son yıldız (4 Kasım): 8.461.
- **Yerel/açık kaynak Cowork ve kişisel ajan alternatifleri [#22]** — İlk 08-10 | Son güncelleme 10-05 | Arşiv 10-26. Son yıldızlar (26 Ekim): eigent 15.662, OpenDots 6.013, nanoMuse 2.600. Eğilim #33'te.
- **Grok 4.6 → 4.7 (xAI) [#30]** — İlk 07-27 | Son güncelleme 09-28 | Arşiv 10-20. Grok 4.7 (21 Eylül). Grok 5 çıkarsa geri döner.
- **Eski arşiv (tek satır):** Anthropic Cowork (09-21; #2), Salesforce Slackbot/Claudeforce (09-21), ChatGPT for Work & GPT-Live (08-17), OptMem (08-17), Sakana Fugu-Cyber (08-17), x402 (08-31), Mistral Shieldstral (08-31), DiffusionGemma (08-31; MiniMax H3 kısmı 11-13'te #44 olarak döndü), Gemini liderlik değişikliği (09-07).
- **OpenAI Astra (matematik modeli — GPT-6 Astra ile KARIŞTIRILMASIN)** — İlk 08-07 | Son 08-10 | Arşiv 08-31. Yeni matematik iddiaları #39'da.

## Değişiklik Geçmişi

- 2026-08-10 – 2026-10-26: bkz. git geçmişi (08-10'da bu repoya taşındı; 10-16'da 3 günlük ritim, kapı, "Son kontrol"/yıldız/BEKLEYEN NOT kuralları, `gorev-talimati.md`).
- 2026-10-29 (pencere 27-29 Ekim): +1 konu (#39); 9 güncelleme; 0 arşiv; 5 K3; sıkıştırma → ~24,8 KB.
- 2026-11-01 (pencere 30 Ekim–1 Kasım): +1 konu (#40); #6 arşivden döndü; 9 güncelleme; 0 arşiv; 2 K3; sıkıştırma → ~24,2 KB.
- 2026-11-04 (pencere 2-4 Kasım): +1 konu (#41); 8 güncelleme; 3 arşiv (#17, #20, #32); yıldız anomalileri; 1 K3; sıkıştırma → ~24,7 KB.
- 2026-11-07 (pencere 5-7 Kasım): +1 konu (#42); 12 güncelleme; 0 arşiv. Yıldız anomalileri. K2: WebFetch yok (alt ajan). Sıkıştırma.
- 2026-11-10 (pencere 8-10 Kasım): 0 yeni konu; 9 güncelleme; 2 arşiv (#27, #36). Yıldız satırları: #13, #25. Inkling 2 teyit edilemedi (K2). Sıkıştırma ~26,9 → ~24,5 KB.
- 2026-11-13 (pencere 11-13 Kasım): +1 yeni konu (#43 REA/tersine mühendislik); #44 MiniMax H3 arşivden döndü; 12 güncelleme (#2, #3, #6, #12, #24, #26, #33, #34, #39, #42, #43, #44); 0 arşiv. 4 K3 (10 Kasım duyuruları). Yıldız satırı: #37. K2: WebFetch yok (alt ajan); 13 Kasım bültenleri, WIRED, BleepingComputer, Inkling kaynakları açılamadı. K1: REA bülten 342k vs API 455.826. Sıkıştırma ~25,3 → ~24,7 KB. BEKLEYEN NOT yoktu.
