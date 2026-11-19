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

### 2. Anthropic modelleri, ürünleri ve kurumsal/güvenlik gelişmeleri (Claude 5.5 ailesi; Fable/Mythos 5.2; Duet; Sheets/Whiteboards/Data; IPO)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-19 | Son kontrol: 2026-11-19 | Durum: Aktif
- Özet (07-27/11-10): 5.5 ailesi Opus $4/$20, Sonnet $2/$10, Haiku $0,10/$0,50; Cowork; Duet (#33); S-1; Personal Finance beta. Fable 5.2 + Mythos 5.2 (9 Kasım; $8/$40; Mythos yalnızca doğrulanmış kuruluşlara).
  - 2026-11-13 (🟢): K3: IPO roadshow (10 Kasım). Claude Sheets/Whiteboards/Data; MAMUBench (11 Kasım).
  - 2026-11-16 (🟡): İkincil: talep ~6 kat (Bloomberg). K3 (10 Kasım): homeopathic learning — seyreltilmiş zehirli veri arka kapı oluşturabiliyor (Qwen3-8B %7 → %16).
  - 2026-11-19 (🟢): Halka arz $83'tan fiyatlandı (18 Kasım; anthropic.com) — 980.000.000 Class A (956.351.354 şirket, 23.648.646 satıcı hissedar), +147.000.000 opsiyon; Nasdaq "ANT" işlem 19 Kasım, kapanış 20 Kasım. S-1/A No.3 (17 Kasım): 825M hisse, $70–78.

### 3. Gemini ailesi ve Google DeepMind (Gemini 4 Argon/Carbon/Hydrogen/Neon, Genie 4, Orchestrator, Decisions API, Wallet, TPU 8, AlphaGenome 2)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-19 | Son kontrol: 2026-11-19 | Durum: Aktif (09-28 arşivlendi, 10-05 geri döndü)
- Özet (07-27/11-10): Argon GA 13 Ekim ($2/$10 → 30 Kasım sonrası $4/$20); Genie 4 duyurusu; Omni 1.2 Flash GA; TPU 8tx/8i Max (9 Kasım).
  - 2026-11-13 (🟢): K3: Gemini 4 Carbon (10 Kasım; $2/$10 → $4/$20). Decisions API (11 Kasım). AlphaGenome 2.
  - 2026-11-16 (🟢): K3 (12 Kasım): Gemini 4 Hydrogen — AA Index 51 (en yüksek ayar 54), Terminal-Bench 4.1 %57. Orchestrator (Carbon plan + Hydrogen uygulama): %24 daha az kota. Wallet → #45; /teamwork → #39.
  - 2026-11-19 (🟢): Gemini 4 Neon (18 Kasım; blog.google) — $3/$15 (önbellek $0,15), 1M bağlam, AA Intelligence Index 61 (xhigh, #3), Terminal-Bench 4.1 %65,2; varsayılan ayarda görev başı maliyet Carbon'dan %32 düşük. Genie 4 Project Genie'de AI Ultra'ya açıldı (18 Kasım).

### 6. Qwen serisi (Alibaba: 3.8 ailesi, QwenWork, Qwen 4, Qwen4-Max; Apple Intelligence Çin)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-19 | Son kontrol: 2026-11-19 | Durum: Aktif (10-20 arşivlendi, 11-01 geri döndü)
- Özet (07-27/11-04): 3.8 ailesi, QwenWork; Qwen 4 duyurusu (22 Eyl); Apple–Alibaba (ikincil).
  - 2026-11-13 (🟢): Qwen4-Max-Preview (11 Kasım) — 1M bağlam, 393.216 maks. çıktı; yalnızca Token Plan, 25 Kasım'a kadar. Fiyat ve açık ağırlık belirtilmemiş.
  - 2026-11-19 (🟢): K3 (16 Kasım; Alibaba basın): Qwen4-Max — 2,4T / 71B aktif, yerleşik görsel, 1M bağlam; Singapur fiyatı $1,5/$4,5. Kapalı ağırlık; küçük Qwen4 modelleri "yakında" açık ağırlık.

### 12. AI ajan güvenlik açıkları (sandbox kaçışları, framework RCE, sızıntılar, tedarik zinciri, otonom saldırılar) ve savunma araçları
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-11-13 | Son kontrol: 2026-11-19 | Durum: Aktif
- Özet (08-07/11-04): CISA 12 framework RCE; Cursor CVE'leri; CVE-2026-82533 (dsh); Archon CVE-2026-111322; OpenCode ihlali; sahte AGENTS.md npm; kurcalanmış Claude Code eklentisi; Postman hook.
  - 2026-11-10 (🟢): K3 (7 Kasım; Apiiro): Claude Code "don't ask again" sırları `.claude/settings.local.json`'a yazıyor; 1.122 açık repoda sır.
  - 2026-11-13 (🟡): İkincil (K1): Microsoft "Lazarus" arka kapı; ARTEX fork'u AntiFox ile AWS kimlik bilgisi hırsızlığı; Railway sonrası sahte AI harcamaları; IoT tersine mühendislik blokları → #43.

### 13. DeepSeek V4-Pro / V4.1-Flash + DeepSeek Harness (dsh) + superagent prototipi + uygulama API'leri
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-11-16 | Son kontrol: 2026-11-19 | Durum: Aktif
- Özet (08-07/11-01): V4-Pro GA; dsh; V4.1-Flash-1017 açık ağırlık (MIT, 763B, 1M); Search/Fetch API; dsh-superagent-prototype (31 Ekim, MIT).
  - 2026-11-10 (yıldız, 10 Kasım): harness 277.594 (9 günde +%3,7); superagent 21.878 (6 günde +%25,4 — anomali eşiği).
  - 2026-11-16 (⚪): K3 (13 Kasım; api-docs.deepseek.com/updates): "full suite of application APIs" — deepseek-flash'ta web arama, dosya girdisi, URL okuma; bağımsız Search, OCR, ASR, TTS API'leri. Yeni ağırlık yok.
  - 2026-11-19 (yıldız, 19 Kasım): harness 283.801 (9 günde +%2,2); superagent 23.869 (9 günde +%9,1).

### 24. Yeni GitHub AI/agent repoları (her rapor çalışmasında tarama)
- İlk görülme: 2026-08-10 | Son güncelleme: 2026-11-19 | Son kontrol: 2026-11-19 | Durum: Aktif
- Özet (08-10/11-10): taramalar raporlarda. Öne çıkanlar: anatomy, huashu-motion, dsh-superagent, pixelfx, teardown, agent-autoloop, vork, hermes-voice, image-to-sculpt. ⚠️ Tekrarlayan desenler: sahte "free model"/sürüm, korsan installer, jailbreak/hile, muse.ai kayıt araçları, sahte yıldız ağları.
  - 2026-11-13 (🟡, 11-13 Kasım): apex-compute/ANR (1.080), guizang-game-skill (264), bot-hq (154), PrintLab (148), mate (138). ⚠️ ai-texture-forge, Hyperliquid-Trade-Bot.
  - 2026-11-16 (🟡, 14-16 Kasım): PeakCut (472), tiny-voca (425). ⚠️ muse-protocol (1.167), "Gemini-Config-Checker-" sahte yıldız ağı.
  - 2026-11-19 (🟡, 17-19 Kasım; 16 sonuç): replit/datacat (219), holospot (168), java4shell-poc (157). ⚠️ muse-JP-Reg (253; muse.ai kayıt/davet — muse-protocol deseni), cloud-exit-node-deploy (304; şişirilmiş), korsan/hile repoları.

### 25. AI imza/watermark temizleme araçları ve filigran tartışması
- İlk görülme: 2026-08-17 | Son güncelleme: 2026-11-04 | Son kontrol: 2026-11-19 | Durum: Aktif
- Özet (08-17/11-01): guillaumemeyer/watermarks-remover 12.177 → 25.799 (1 Kasım); rakip ShadowAqueduct silindi.
  - 2026-11-04 (🟡): Anthropic sürüm notu (3 Kasım): Mythos 5, Opus 4.7, Sonnet 4.6 metinleri Anthropic metin filigranı taşıyor.
  - 2026-11-10 (yıldız, 10 Kasım): 26.908 (9 günde +%4,3).
  - 2026-11-19 (yıldız, 19 Kasım): 27.794 (9 günde +%3,3).

### 26. OpenAI GPT-6 ailesi ve ürünleri (Astra / Sol / Luna / 6.1 Sol / Terra / Rosalind / Cyber / 6.2 Astra-Sol, Dots, Space, Businesses, Wallet)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-19 | Son kontrol: 2026-11-19 | Durum: Aktif
- Özet (07-27/11-07): GPT-6 Astra ($10/$50), Sol ($2/$10), Luna ($0,10/$0,50); DevDay: Dots, 6.1 Sol, Space, Agents API; 6.1 Terra ($1/$5); Rosalind; GPT-6 Cyber (5 Kasım, Daybreak Red, siber "Critical").
  - 2026-11-13 (🟡): İkincil: Businesses in ChatGPT beta (11 Kasım); Advanced/Standard Voice 11 Aralık'ta emekli; Odessia satın alındı.
  - 2026-11-16 (🟡): İkincil (openai.com sayfası K2): ChatGPT Wallet (13 Kasım) → #45. Fortune (13 Kasım): bağımsız robotik ekibi dağıtıldı, 2027 insansı demo hedefi sürüyor.
  - 2026-11-19 (🟢): GPT-6.2 Astra ($8/$40, GPT-6 Astra'dan %20 ucuz) ve Sol ($2/$10) (17 Kasım; openai.com + sistem kartı): Astra AI Self-Improvement'ta High eşiğine ulaşan ilk dışa sunulan model; ikisi de siber "Critical", bio/kimya "High". İkincil: ChatGPT for Sales, Astra for Law 6.2; Oregon AG davası ($2,035 milyar, 17 Kasım).

### 28. Meta Muse ailesi (Muse Spark, Muse Code, Muse ajan uygulaması, Muse Wonder, Muse Spark Open, Muse Ember)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-10 | Son kontrol: 2026-11-19 | Durum: Aktif
- Özet (07-27/10-29): Muse Spark 1.3; Muse ajan uygulaması (8 Eyl); Muse Wonder (API $4/$20); Muse Spark Open (#35).
  - 2026-11-07 (⚪): ifadeli avatarlar; site kazıma şart güncellemesi askıya alındı (ikincil).
  - 2026-11-10 (🟡): Muse Ember (9 Kasım) — $0,10/$0,50 (200K üstü $0,30/$1,50); 1M bağlam, 512K çıktı; AutomationBench-AA %37,8, Terminal-Bench 4.0 %40,9.

### 29. Mistral AI (Series D, Mistral Large 4, CERN Flare, Studio)
- İlk görülme: 2026-09-14 | Son güncelleme: 2026-11-07 | Son kontrol: 2026-11-19 | Durum: Aktif (10-05 arşivlendi, 10-12 geri döndü)
- Özet (09-14/10-29): 3 milyar € Series D; Large 4 public preview (6 Ekim); CERN "Flare".
  - 2026-11-01 (🟢): K3 (29 Ekim): Large 4 açık ağırlık — 1T/52B aktif, "Mistral Ecosystem Open-Weight license"; API $0,70/$2,10.
  - 2026-11-07 (🟡): Mistral Studio genişletmesi (5 Kasım) — managed agents, iş akışları, değerlendirme; bulut/VPC/on-prem.

### 30. Grok (xAI) — 4.7 → 4.8 (arşivden döndü)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-16 | Son kontrol: 2026-11-19 | Durum: Aktif (10-20 arşivlendi, 11-16 geri döndü)
- Özet (07-27/09-28): Grok 4.6 → Grok 4.7 (21 Eylül).
  - 2026-11-16 (⚪): İkincil (Zeniteq, 15 Kasım): resmi Grok hesabı 13 Kasım'da Grok 4.8'in Bot kullanıcılarına "soft rollout"unu duyurdu (C/C++ yığın yeniden yazımı sonrası). Model kartı, API, fiyat, benchmark yok.

### 33. Always-on kişisel/iş ajanları (OpenAI Dots, Meta Muse, ChatGPT Space, Claude Duet, Perplexity Teammates, Databricks Genie, ByteDance; açık kaynak: OpenDots, nanoMuse)
- İlk görülme: 2026-10-05 | Son güncelleme: 2026-11-13 | Son kontrol: 2026-11-19 | Durum: Aktif
- Özet (10-05/10-23): OpenAI Dots (29 Eylül) ile kategori ana akım; Claude Duet (21 Ekim).
  - 2026-11-07 (🟡): Perplexity Teammates; Rerun self-host (ikincil).
  - 2026-11-13 (🟡): İkincil: ByteDance "haftalar içinde" Muse benzeri ajan; Databricks Genie always-on + Ontology; n8n Nod.

### 34. Frontier güvenlik olayları ve düzenleyici yanıt (OpenAI duraklatma, SI Force, FTC, METR, NY RAISE, Avustralya, AB sandbox)
- İlk görülme: 2026-09-28 | Son güncelleme: 2026-11-19 | Son kontrol: 2026-11-19 | Durum: Aktif
- Özet (09-28/11-10): OpenAI eğitim duraklaması (dönüş 23 Ekim); SI Force, FTC CID'leri; Newsom kararnamesi; METR AECI 1,9 kat; DOJ SI Task Force; Senato taslağında çip denetimi.
  - 2026-11-13 (🟡): İkincil: NY RAISE kayıt portalı (son tarih 1 Ocak 2027); Avustralya AI düzenleyici planı; ABD–Çin olay kanalı.
  - 2026-11-16 (🟡): İkincil: AB Uygulama Tüzüğü 2026/2487 — AI sandbox'ları (son tarih 2 Ağustos 2027). ABD + 8 müttefik "San Francisco Bildirgesi" (FT).
  - 2026-11-19 (🟡): İkincil: Oregon AG – OpenAI davası (17 Kasım); 4 kâr amacı gütmeyen kuruluşun Anthropic/Google/Meta/OpenAI/SpaceXSI'ya ihtiyati tedbir davası (K3, 12 Kasım); Çin'in uzaktan çip erişimi kısıtlarına misilleme tehdidi (Semafor); Vals askeri hedefleme testi (oyun çerçevesi reddi aşıyor).

### 35. ABD açık/lisanslı ağırlık yarışı (Muse Spark Open, Reflection Beam, MAI-Base-2, Inkling 2)
- İlk görülme: 2026-10-17 | Son güncelleme: 2026-11-16 | Son kontrol: 2026-11-19 | Durum: Aktif
  - 2026-10-17 (🟢) — İLK TAKİP: Reflection AI Beam (501B/23B, Apache 2.0), Microsoft MAI-Base-2, Meta Muse Spark Open (#28).
  - 2026-11-07 (🟡): Thinking Machines Inkling 2 Small (5 Kasım) — 594B/17B aktif MoE; Tinker'da kapalı ağırlık, "gelecek hafta" Apache 2.0 niyeti.
  - 2026-11-16 (🟡): K3 (12 Kasım; thinkingmachines.ai/news/inkling-2-small): ağırlıklar HF'de `thinkingmachines/Inkling-2-Small`; AA Intelligence Index 31. (10 ve 13 Kasım'daki K2 kapandı.)

### 37. AI destekli zafiyet keşfi (PHP2Shell, Node2Shell, Codex Security, Wiz Atlas, GPT-6 Cyber, Mythos 5.2)
- İlk görülme: 2026-10-23 | Son güncelleme: 2026-11-19 | Son kontrol: 2026-11-19 | Durum: Aktif
- Özet (10-23/11-07): PHP2Shell (CVE-2026-109618/109619; Calif, Codex Security, Wiz); php2shell-checker; CISA KEV; Node2Shell (CVE-2026-111497, CVSS 9,2); GPT-6 Cyber.
  - 2026-11-10 (🟡): Claude Mythos 5.2 (9 Kasım; #2) — CVE Rediscovery %89,6.
  - 2026-11-13 (yıldız, 13 Kasım): php2shell-checker 1.470 (9 günde +%0,7).
  - 2026-11-19 (🟡): GPT-6.2 Astra/Sol siber "Critical" (#26). İkincil: Calif AI ile Java'da ciddi açık (NYT, 17 Kasım); Reflection Laser kısıtlı erişimli siber aracı (Axios). java4shell-poc (CVE-2026-114938) ile bağlantısı doğrulanamadı.

### 38. Kimi (Moonshot) — K3 → K3.1 Pro
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-19 | Son kontrol: 2026-11-19 | Durum: Aktif (08-31 arşivlendi, 10-26 geri döndü)
- Özet (07-27/11-04): K3.1 Pro + Highspeed (23 Ekim), 1M bağlam; K2 serisi emeklilik Aralık sonu.
  - 2026-11-07 (🟢): Ağırlıklar yayımlandı — `moonshotai/Kimi-K3.1-Pro`: 2,8T / 104B aktif, 1.048.576 bağlam, MXFP4; lisans "Kimi K3.1 Pro License" (özel).
  - 2026-11-19 (⚪): İkincil (SCMP/The Decoder, K3 16 Kasım): Moonshot kodlama benchmark yarışından çekilip Kimi'yi biyoloji/kimya/ilaç araştırmasına yönlendiriyor.

### 39. AI ile matematik/bilim keşif ve biçimsel doğrulama (OpenAI ETH/Yang–Mills, Axiom CFSG, Fable 5.2 FLT, AlphaProof Code, Antigravity /teamwork)
- İlk görülme: 2026-10-29 | Son güncelleme: 2026-11-16 | Son kontrol: 2026-11-19 | Durum: Aktif
- Özet (10-29/11-07): OpenAI ETH çürütme, local smoothing, 4B Yang–Mills (Lean). Axiom CFSG Lean formalizasyonu.
  - 2026-11-10 (🟢): Anthropic (9 Kasım): 1.000 Fable 5.2 ajanı FLT ispatını 30 saatte formalize etti (şirket iddiası).
  - 2026-11-13 (🟡): K3 (10 Kasım): AlphaProof Code — Signal protokol güvenlik özellikleri Lean'de.
  - 2026-11-16 (🟡): Google Research (13 Kasım): /teamwork-LEAP Weil sanılarını Lean'de formalize etti (~1,8M satır). Yıldız (16 Kasım): CFSG 166.

### 40. AI eğitim tercihi sinyali / yayıncı opt-out standardı (robots.txt token, IETF taslağı)
- İlk görülme: 2026-11-01 | Son güncelleme: 2026-11-01 | Son kontrol: 2026-11-19 | Durum: Aktif
  - 2026-11-01 (🟡) — İLK TAKİP: OpenAI, Google, Microsoft, Anthropic (30 Ekim) ortak eğitim tercihi sinyali; IETF `draft-kelley-aipref-training-preference-signal`. Microsoft'ta 1 Şubat 2027'de yürürlükte.

### 41. Meituan LongCat model ailesi
- İlk görülme: 2026-11-04 | Son güncelleme: 2026-11-04 | Son kontrol: 2026-11-19 | Durum: Aktif
  - 2026-11-04 (🟡) — İLK TAKİP: LongCat-2.5 Preview (2 Kasım; TechNode) — 1,6T / ~48B aktif; açık ağırlık henüz yok.

### 42. AI veri merkezi altyapısına yerel tepki, enerji ve piyasa etkisi (Nvidia liderlik krizi dahil)
- İlk görülme: 2026-11-07 | Son güncelleme: 2026-11-19 | Son kontrol: 2026-11-19 | Durum: Aktif
- Özet (11-07/11-10): ABD yerel oylamalarında veri merkezi kısıtları; OpenAI "National Community Compact"; Anthropic OnePWR gaz jeneratörleri (K1); Starbase vergi indirimi.
  - 2026-11-13 (🟡): İkincil (K1): Nvidia kurulu Huang'ı görevden almaya hazırlanıyor (WSJ, 12 Kasım); EIA rekor talep.
  - 2026-11-16 (🟡): İkincil: Huang görevden alındı (Bloomberg, 15 Kasım); Bessent dışarıdan CEO istiyor.
  - 2026-11-19 (🟡): Nvidia Q3 FY27 (17 Kasım; nvidianews): gelir $115,8 milyar (+%103), veri merkezi $107,6 milyar (+%110), Q4 beklenti $130,0 milyar ±%3; Colette Kress geçici CEO. İkincil: kurul Huang'ı geri getirmeyecek (K1, yalnızca başlık); Çin'e çip satışı bırakılıyor (TechCrunch); Huang 1 Aralık'ta Temsilciler Meclisi'nde.

### 43. Ajanlarla tersine mühendislik (REA ekosistemi) ve laboratuvar kısıtlamaları
- İlk görülme: 2026-11-13 | Son güncelleme: 2026-11-13 | Son kontrol: 2026-11-19 | Durum: Aktif
  - 2026-11-13 (🟡) — İLK TAKİP: Claude ve Codex, ajanları IoT cihazlarına yönelten kullanıcıları güvenlik bloklarıyla durduruyor/hesap kapatıyor (404 Media aktarımı; ikincil). Yıldız (13 Kasım, API): morluto/rea 455.826 (bülten "342.000", K1); leanrea 4.240; REA-Prompts 4.007.

### 44. MiniMax H3 ailesi (arşivden döndü: eski "DiffusionGemma/MiniMax H3", 08-31)
- İlk görülme: 2026-08-31 öncesi | Son güncelleme: 2026-11-13 | Son kontrol: 2026-11-19 | Durum: Aktif (08-31 arşivlendi, 11-13 geri döndü)
  - 2026-11-13 (🟡): MiniMax H3-Image (11 Kasım) — açık ağırlık görsel üretim/düzenleme (HF: MiniMaxAI/MiniMax-H3-Image); 4K "under 10 seconds", 16 referans görsel; lisans adı yok.

### 45. Ajan ödemeleri ve kişisel finans entegrasyonları (ChatGPT Wallet, Gemini + Google Wallet, Claude Personal Finance)
- İlk görülme: 2026-11-16 | Son güncelleme: 2026-11-16 | Son kontrol: 2026-11-19 | Durum: Aktif
  - 2026-11-16 (🟡) — İLK TAKİP: K3 (13 Kasım): Gemini + Google Wallet (ABD, salt-okunur, Plaid). İkincil: ChatGPT Wallet (13 Kasım) — ajanlar onayla tokenize kartla satın alıyor; ABD Pro. İlişkili: Claude Personal Finance (#2).

## Arşivlenmiş Konular

(Geri dönüş olmadıkça satır eklenmez. Tam geçmiş git commit'lerinde.)

- **TypeSafe AI — Jev / "System One Models" [#31]** — İlk 09-21 | Son güncelleme 10-26 | Arşiv 11-16. Jev (15 Eylül), Jev 1.14.0 (14 Ekim); 24 Ekim veri sızıntısı, postmortem yok.
- **Vercel fx / libfx / fx0 [#27]** — İlk 08-24 | Son güncelleme 10-20 | Arşiv 11-10. Son yıldızlar (10 Kasım): fx 3.801, fx0 431.
- **AB AI Act uygulama takvimi ve standartları [#36]** — İlk 08-07 | Son güncelleme 10-20 | Arşiv 11-10. EN 18286:2026 (19 Ekim). (AB sandbox tüzüğü 11-16'da #34'e işlendi.)
- **Prime Agent (Prime Intellect) [#17]** — İlk 08-08 | Son güncelleme 10-12 | Arşiv 11-04. ARC-AGI-3 %95,5, MIT. Son yıldız (4 Kasım): 22.557.
- **AI ajan mimarisi/hafıza yaklaşımları [#20]** — Son güncelleme 10-12 | Arşiv 11-04. Yıldız (4 Kasım): agent-memory 4.303.
- **Z.ai (Zhipu) ZCode ve GLM dikey modelleri [#32]** — İlk 09-21 | Son güncelleme 10-12 | Arşiv 11-04. Son yıldız (4 Kasım): 8.461.
- **Yerel/açık kaynak Cowork alternatifleri [#22]** — Son güncelleme 10-05 | Arşiv 10-26. Yıldız (26 Ekim): eigent 15.662, OpenDots 6.013. Eğilim #33'te.
- **Eski arşiv (tek satır):** Anthropic Cowork (09-21; #2), Salesforce Slackbot/Claudeforce (09-21), ChatGPT for Work & GPT-Live (08-17), OptMem (08-17), Sakana Fugu-Cyber (08-17), x402 (08-31), Mistral Shieldstral (08-31), DiffusionGemma (08-31; MiniMax H3 kısmı #44), Gemini liderlik değişikliği (09-07).
- **OpenAI Astra (matematik modeli — GPT-6 Astra ile KARIŞTIRILMASIN)** — İlk 08-07 | Son 08-10 | Arşiv 08-31. Yeni matematik iddiaları #39'da.

## Değişiklik Geçmişi

- 2026-08-10 – 2026-11-07: bkz. git geçmişi (08-10 repoya taşındı; 10-16 3 günlük ritim, kapı, "Son kontrol"/yıldız/BEKLEYEN NOT kuralları, `gorev-talimati.md`).
- 2026-11-10 (pencere 8-10 Kasım): 0 yeni konu; 9 güncelleme; 2 arşiv (#27, #36). Inkling 2 teyit edilemedi (K2). Sıkıştırma ~26,9 → ~24,5 KB.
- 2026-11-13 (pencere 11-13 Kasım): +1 konu (#43); #44 arşivden döndü; 12 güncelleme; 0 arşiv; 4 K3. K1: REA bülten 342k vs API 455.826. Sıkıştırma ~25,3 → ~24,7 KB.
- 2026-11-16 (pencere 14-16 Kasım, hafta sonu): +1 konu (#45 ajan ödemeleri); #30 Grok arşivden döndü; 11 güncelleme (#2, #3, #13, #24, #26, #30, #34, #35, #39, #42, #45); 1 arşiv (#31). Çoğu bulgu 12-13 Kasım K3. Inkling 2 K2'si kapandı. Yıldız satırı: #39 (CFSG). K2: WebFetch yok (alt ajan); The Neuron, creati.ai, OpenAI Wallet, EUR-Lex, Bloomberg, CNBC açılamadı. Anomali (raporda): modern-web-guidance +%133. Sıkıştırma. BEKLEYEN NOT yoktu.
- 2026-11-19 (pencere 17-19 Kasım): 0 yeni konu; 9 güncelleme (#2, #3, #6, #24, #26, #34, #37, #38, #42); 0 arşiv. K3: Qwen4-Max (16 Kasım), Kimi pivot. Yıldız satırları: #13, #25. K2: WebFetch yok (alt ajan); CNBC, WaPo, NBC, cryptobriefing açılamadı. Anomali (raporda): modern-web-guidance +%25,3. Sıkıştırma ~27,6 → ~24,3 KB. BEKLEYEN NOT yoktu.
