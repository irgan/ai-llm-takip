# AI/LLM Takip Listesi

Bu dosya AI/LLM özeti otomasyonunun KALICI DURUM dosyasıdır. Her çalışmada okunur, güncellenir ve AYNI YOLA (`takip-listesi.md`) yazılır. Git commit geçmişi sayesinde her çalışmanın değişimi diff olarak görülebilir.

Raporlar ayrı dosyalardır: `raporlar/YYYY-AA-GG.md`. Bu dosya rapor değil, takip durumudur.

## Çalışma Ritmi

- **2026-10-17'den itibaren 3 günde bir** çalışır (öncesi haftalıktı: 2026-08-17 – 2026-10-12).
- **Tarama penceresi:** `raporlar/` klasöründeki EN SON rapor dosyasının tarihinden sonraki gün → çalışma günü (dahil). Normalde 3 gün. Çalışma atlanırsa pencere son rapora kadar genişler, arada boşluk bırakılmaz; bu durum raporun kısıt notunda belirtilir.
- **Rapor dosyası:** `raporlar/YYYY-AA-GG.md`, ad çalışma tarihidir. Aynı gün o adla bir rapor zaten varsa üzerine YAZILMAZ: mevcut rapor yeni bulgularla güncellenir ve kısıt notuna "aynı gün ikinci çalışma" eklenir.
- **Başlık formatı:** `# AI/LLM Özeti — GG Ay YYYY (pencere: GG–GG Ay)`. Bölüm yapısı değişmez: 1. Haberler · 2. Yeni Araçlar · 3. Dikkat Çekici GitHub Repoları · 4. AI ile Çalışma Yöntemleri · 5. Önceki Konularda Gelişmeler.
- **Kısa pencere:** Bölümlerin boş kalması normaldir. Boşluk doldurmak için zayıf haber eklenmez; "Bu dönemde kayda değer gelişme yok" yazılır.
- **GitHub repo taraması (#24):** `created:` filtresi rapor penceresiyle aynıdır.
- **Bekleyen notlar:** Bir konuda "BEKLEYEN NOT" varsa, sonraki çalışma onu doğrulayıp normal kayıt olarak işler ve notu siler.

## Kurallar

- Yeni bahsedilen her önemli konu buraya bir madde olarak eklenir.
- Gerçek bir gelişme olduğunda "Son güncelleme" değişir ve günlüğe tarihli not eklenir.
- ⚠️ Gelişme yoksa günlüğe satır EKLENMEZ. Yalnızca konu başlığındaki "Son kontrol" tarihi güncellenir. "Son güncelleme" DEĞİŞMEZ; arşivleme buna bağlıdır.
- **Yalnızca yıldız büyümesi gerçek gelişme sayılmaz** ve "Son güncelleme"yi değiştirmez. Yıldızlar raporda her çalışmada verilir. Takip listesine en fazla 7 günde bir, tek satır olarak yazılır. Önceki kayda göre ±%25'i aşan değişim anomali sayılır ve hemen yazılır.
- Yıldız yüzdeleri bir önceki rapordaki değere göre hesaplanır ve karşılaştırma aralığı belirtilir (ör. "3 günde +%2,1").
- "Son güncelleme"si 21+ gün eskiyen konu "Arşivlenmiş Konular"a taşınır (her çalışmada kontrol edilir). Arşivdeki konu yeniden gündeme gelirse Aktif'e döner.
- Sayısal iddialar (yıldız, parametre, benchmark) yalnızca birincil kaynaktan/API'den alınır. GitHub yıldızları yalnızca `stargazers_count`'tan alınır.
- **Sıkıştırma:** Dosya 25KB'ı aştığında ya da 3 ayda bir yapılır. Her konuda son 3 kayıt bırakılır, öncesi özet satırına indirilir. #24'te her tarama için en fazla 5 repo tutulur (tam liste raporda). Hedef: sıkıştırma sonrası ≤20KB. Bu, her çalışmada tekrar sıkıştırma yapılmasını önler.
- Kısaltmalar: K1 = doğrulanamadı/alınmadı, K2 = kaynağa erişilemedi, K3 = geriye dönük fark edildi.
- Geriye dönük üretilen raporlarda geçmiş tarihli yıldız verisi alınamaz. Yıldızlar üretim günü itibarıyla verilir ve bu kayıtta belirtilir.

## Aktif Takip Listesi

### 2. Anthropic modelleri ve kurumsal/güvenlik gelişmeleri (Claude 5.5 ailesi: Opus/Sonnet/Haiku 5.5; Fable 5.1)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-10-12 | Son kontrol: 2026-10-12 | Durum: Aktif
- Özet (07-27/09-21): Fable 5, Opus 5, Sonnet 5 ($2/$10); Cowork; görünmez watermark; Commerce Agents blueprint; Smart Reports; Claude'un AR-GE'nin %26'sını "yönettiği" duyurusu (09-21).
  - 2026-09-28 (🟢): Opus 5.5 (22 Eylül) — çoğu işte Fable 5.1 seviyesi; $4/$20, önbellek okuma $0,20; tipik iş yükünde ~%40 ucuz; Fast mode $8/$40; 1M/128K. Sonnet 5.5 (28 Eylül) — $2/$10, AA Index 56.
  - 2026-10-12 (🟢): Haiku 5.5 (7 Ekim) — ≤100K token $0,10/$0,50, üstünde 5x; 1M/128K; effort seviyeli ilk Haiku. 5.5 ailesi tamamlandı.
  - 2026-10-12 (yıldız, 16 Ekim): anthropics/commerce-agents 3.251 (21 Eylül'e göre +%8,3).

### 3. Gemini ailesi (3.x Flash → Gemini 4 Argon) (Google DeepMind)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-10-05 | Son kontrol: 2026-10-12 | Durum: Aktif (09-28 arşivlendi, 10-05 geri döndü)
- Özet (07-27/09-21): 3.5-3.8 Flash serisi; 3.8 Flash (2 Eylül, HLE-Verified %54,9).
  - 2026-09-28: 21 gün gelişme yok → arşivlendi.
  - 2026-10-05 (🟢) — YENİDEN GÜNDEMDE: Gemini 4 Argon (30 Eylül) — kodlama/kurumsal/siber savunma; 1M çıktı limiti; ilk erişim yalnızca ABD hükümeti + Fairwind siber savunucuları; $2/$10 tanıtım, sonra $4/$20.
  - BEKLEYEN NOT (pencere 13-17 Ekim): 13 Ekim'de Argon API/AI Studio/Antigravity/Gemini app (Pro/Ultra)/GitHub Copilot'ta genel kullanıma açıldı — doğrulanıp işlenecek.

### 6. Qwen serisi (Alibaba: 3.8 ailesi, QwenWork, Image-2.1, Qwen 4)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-09-28 | Son kontrol: 2026-10-12 | Durum: Aktif
- Özet (07-27/09-14): 3.8-Max (2.4T) GA, 3.8-27B Apache 2.0, 3.8-Flash-Next (Qwen4 mimari önizlemesi), QwenWork.
  - 2026-09-21 (🟡): Qwen-Image-2.1 (7B, açık ağırlık).
  - 2026-09-28 (🟡): Qwen 4 ailesi duyuruldu (22 Eylül, Apsara) — Max/Plus/Flash + açık 27B; eğitimde, tarih yok. K3: Qwen3.8-Omni-Flash 18 Eylül'de API'de çıkmış.
  - 2026-10-12: Qwen 4 hâlâ yayınlanmadı ("Eylül sonu" sızıntısı tutmadı).

### 12. AI ajan güvenlik açıkları (sandbox kaçışları, framework RCE)
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-09-28 | Son kontrol: 2026-10-12 | Durum: Aktif
- Özet (08-07/09-14): CISA 12 framework RCE, Langflow KEV, Cursor CVE-2026-50548/50549, GitSpawn (core.fsmonitor RCE, 7 ajan).
  - 2026-09-21 (🟡): Hermes Agent GitSpawn yama durumu çelişkili (K1). Qwen Code ve Grok Build yamasız.
  - 2026-09-28 (🟡): K3: DeepSeek Harness sandbox kaçışı CVE-2026-82533 (CVSS 9.4, 8 Eylül) — kimlik doğrulamasız yerel API ile "danger-full-access"; 0.1.2-alpha.1'de düzeltildi.
  - 2026-10-12: Qwen Code / Grok Build için yayımlanmış GitSpawn yaması hâlâ yok.

### 13. DeepSeek V4-Pro / V4.1-Flash + DeepSeek Harness (dsh)
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-10-12 | Son kontrol: 2026-10-12 | Durum: Aktif
- Özet (08-07/09-21): V4-Flash-0731 MIT; V4-Pro GA; dsh v0.1; V4.1-Flash (10 Eylül, `deepseek-flash`).
  - 2026-09-28: Çapraz not: CVE-2026-82533 → #12. ⚠️ "dsh-our-free-model" eklentisi riskli olarak işaretlendi (#24).
  - 2026-10-12 (⚪): Yeni model yok; V4.1-Pro adı geçiyor ama duyurulmadı (K1). V4-Pro'nun kapatılmasından vazgeçildi, aynı fiyatla sunuluyor.
  - 2026-10-12 (yıldız, 16 Ekim): deepseek-ai/deepseek-harness 251.087 (21 Eylül'e göre +%8,4).

### 17. Prime Agent (Prime Intellect)
- İlk görülme: 2026-08-08 | Son güncelleme: 2026-10-12 | Son kontrol: 2026-10-12 | Durum: Aktif — ARŞİV ADAYI (gerçek gelişme olmazsa 2026-11-02)
- Özet (08-08/09-21): ARC-AGI-3 %95,5, MIT lisans; yıldız 12.064 → 21.113, büyüme yavaşlıyor.
  - 2026-10-12 (yıldız, 16 Ekim): 22.059 (21 Eylül'e göre +%4,5). Ürün duyurusu yok.

### 20. AI ajan mimarisi/hafıza yaklaşımları (agent-memory, okf-agent-memory, lemmalog, AKB, AgentMemoryRepo)
- İlk görülme: 2026-08-08 | Son güncelleme: 2026-10-12 | Son kontrol: 2026-10-12 | Durum: Aktif
- Özet (08-08/09-14): Karpathy graph-tabanlı hafıza; lemmalog (Datalog); agent-memory ve okf-agent-memory girişleri; 09-14 büyüme sıçraması.
  - 2026-09-21 (🟡): agent-memory 961 (-%29, sahte-yıldız temizliği ihtimali), okf 708, lemmalog 316, akb 160.
  - 2026-10-05: Yeni girişler: AgentMemoryRepo (ajan hafıza deposu spesifikasyonu), elstongun/leviathan (büyük veri üzerinde hafıza).
  - 2026-10-12 (🟢, yıldız 16 Ekim): agent-memory 3.905 (+%306, sert toparlanma); okf 809 (+%14,3); lemmalog 340 (+%7,6); akb 163; AgentMemoryRepo 795; leviathan 825.

### 22. Yerel/açık kaynak Cowork, Claude Code ve kişisel ajan alternatifleri (Goose, Eigent, ZCode, OpenDots, nanoMuse)
- İlk görülme: 2026-08-10 | Son güncelleme: 2026-10-05 | Son kontrol: 2026-10-12 | Durum: Aktif
- Özet (08-10/09-21): Goose ilk takip; eigent büyümesi yavaşladı; ZCode açık kaynak oldu (#32).
  - 2026-09-28: nano-muse/nanoMuse — Meta Muse'un açık kaynak alternatifi (23 Eylül).
  - 2026-10-05 (🟡): CopilotKit/OpenDots — OpenAI Dots'un açık kaynak karşılığı (29 Eylül). Bkz. #33.
  - 2026-10-12 (yıldız, 16 Ekim): eigent 15.569 (+%1,4 — büyüme fiilen durdu); OpenDots 5.480; nanoMuse 1.328.

### 24. Yeni GitHub AI/agent repoları (her çalışmada tarama)
- İlk görülme: 2026-08-10 | Son güncelleme: 2026-10-12 | Son kontrol: 2026-10-12 | Durum: Aktif
- Özet (08-10/09-21): önceki taramalar raporlarda; 09-21 Jev ekosistemi patlaması.
  - 2026-09-28 (🟢, ilk 5, yıldız 16 Ekim): ⚠️ Ebony-Vinyl/dsh-our-free-model (19.173, riskli), yetone/magpie (14.115), KKKKhazix/AIHOT (7.880), yihui-dev/awesome-opus5-5-videos (5.444), Louis-CFM/coucou (5.361). Desen: Opus 5.5 ile kodla video üretimi.
  - 2026-10-05 (🟢, ilk 5): rehan-remade/universal-modder (8.051), CopilotKit/OpenDots (5.480), omlahore/RemoveMacAI (4.833), nykooi1/vibe-wise (3.673), QingYunA/answer-me-with-html (3.514). ⚠️ feder-cr/invisible_playwright_mcp (anti-bot atlatma).
  - 2026-10-12 (🟢, ilk 5): wheresryan22/anatomy (13.759), ⚠️ mhtsec/ARTEX (4.408 / 6.610 fork — olağandışı, upstream doğrulanamadı, K1), LosaLosSantos/aurelio-finance (3.943), onehumanbeing/esp32-iphone-agent (2.820), deeplethe/solid-glass (1.343).

### 25. AI imza/watermark temizleme araçları ve tartışma
- İlk görülme: 2026-08-17 | Son güncelleme: 2026-10-12 | Son kontrol: 2026-10-12 | Durum: Aktif — ARŞİV ADAYI (gerçek gelişme olmazsa 2026-11-02)
- Özet (08-17/09-21): guillaumemeyer/watermarks-remover 12.177 → 22.462; rakip ShadowAqueduct silindi.
  - 2026-10-12 (yıldız, 16 Ekim): 24.256 (+%8,0). Yeni gelişme yok.

### 26. OpenAI GPT-6 ailesi ve ürünleri (Astra / Sol / Luna / 6.1 Sol, Dots, ChatGPT Space)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-10-12 | Son kontrol: 2026-10-12 | Durum: Aktif
- Özet (07-27/09-21): GPT-5.6 ailesi; GPT-6 Astra (3-4 Eylül; $10/$50).
  - 2026-09-28 (🟢): GPT-6 Sol ($2/$10) ve Luna ($0,10/$0,50) (22 Eylül). GPT-6.1 Astra yayını güvenlik gerekçesiyle iptal (28 Eylül). Eğitim duraklatması → #34.
  - 2026-10-05 (🟢): DevDay (29 Eylül): Dots, GPT-6.1 Sol (Astra'nın 1/5 fiyatı, AA 52), ChatGPT Space, Agents API açık beta, Ultrafast, $500/ay plan; 1,2 milyar haftalık kullanıcı.
  - 2026-10-12 (🟡): GPT-6.1 Sol Ultrafast tüm API kullanıcılarına açıldı (8 Ekim).

### 27. Vercel fx — minik açık kaynak kodlama ajanı
- İlk görülme: 2026-08-24 | Son güncelleme: 2026-10-12 | Son kontrol: 2026-10-12 | Durum: Aktif — ARŞİV ADAYI (gerçek gelişme olmazsa 2026-11-02)
- Özet (08-24/09-21): Zig ile yazılmış minimal ajan; 2.622 → 3.088 yıldız.
  - 2026-10-12 (yıldız, 16 Ekim): 3.456 (+%11,9). Ürün gelişmesi yok.

### 28. Meta Muse ailesi (Muse Spark, Muse Code, Muse ajan uygulaması, Muse Wonder)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-10-12 | Son kontrol: 2026-10-12 | Durum: Aktif
- Özet (07-27/09-28): Muse Spark 1.3; Muse kişisel ajan uygulaması (8 Eylül, K3); Kanada'ya açıldı (18 Eylül, K3).
  - 2026-10-05 (⚪): 30 Eylül — akıllı gözlük desteği, alışveriş bağlayıcıları; ülke hâlâ ABD + Kanada.
  - 2026-10-12 (🟢): Muse Wonder / Wonder Full (12 Ekim) — Meta'nın ilk frontier modelleri; Meta'ya göre Fable 5.1 / GPT-6 Astra ile karşılaştırılabilir (K1). Wonder API $4/$20; Wonder Full yalnızca Muse Code üst planlarında. AA: Wonder 52.
  - BEKLEYEN NOT (pencere 13-17 Ekim): Muse Spark Open (açık ağırlık, 15 Ekim) — doğrulanıp işlenecek.

### 29. Mistral AI (Series D, Mistral Large 4)
- İlk görülme: 2026-09-14 | Son güncelleme: 2026-10-12 | Son kontrol: 2026-10-12 | Durum: Aktif (10-05 arşivlendi, 10-12 geri döndü)
- Özet: 2026-09-14 (🟢) Samsung liderliğinde 3 milyar € Series D (8 Eylül), değerleme 21 milyar €+.
  - 2026-10-05: 21 gün gelişme yok → arşivlendi.
  - 2026-10-12 (🟢) — YENİDEN GÜNDEMDE: Mistral Large 4 "Le Chonk" public preview (6 Ekim) — ~1,05T MoE, ~49B aktif, 1M bağlam, multimodal; API $1,36/$4,18; ağırlıklar Ekim sonunda (Reuters: 27 Ekim, resmi teyit yok — K1).
  - BEKLEYEN NOT (pencere 13-17 Ekim): CERN ile "Large Physics Model" ortaklığı (15 Ekim). Ayrıca ağırlıkların yayınlanması takip edilecek.

### 30. Grok 4.6 → 4.7 (xAI)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-09-28 | Son kontrol: 2026-10-12 | Durum: Aktif
- Özet (07-27/09-14): Grok 4.6; arşivlendi (08-31); Microsoft Copilot'a Grok eklenmesiyle döndü (09-14).
  - 2026-09-21: "Grok 4.7 çıkmadı" kaydı HATALI (bkz. 09-28).
  - 2026-09-28 (🟢): DÜZELTME (K3): Grok 4.7 21 Eylül'de çıkmış. 500K bağlam, $2/$6 (200K üstü yüksek tarife); CursorBench 4.0 %46,3; AA 46. Bedrock'ta (28 Eylül). Hesap @xai → @SpaceXAI.

### 31. TypeSafe AI — Jev / "System One Models"
- İlk görülme: 2026-09-21 | Son güncelleme: 2026-10-05 | Son kontrol: 2026-10-12 | Durum: Aktif
  - 2026-09-21 (🟢) — İLK TAKİP: Jev (15 Eylül) — tipli/kalibre kararlar, 70-500 ms, $0,042/MTok giriş; ağırlık açıklanmadı. GitHub'da ekosistem patlaması.
  - 2026-09-28 (🟡): jevgrep, Intent-Router; Jev 1.13 OpenRouter'da (18 Eylül, K3).
  - 2026-10-05 (⚪): LangChain "Building a Harness with Jev" rehberi.
  - BEKLEYEN NOT (pencere 13-17 Ekim): Jev 1.14 önizleme (~14 Ekim; görsel girdi, Box tipi, 262K bağlam) — doğrulanıp işlenecek.

### 32. Z.ai (Zhipu) — ZCode kodlama ajanı ve GLM dikey modelleri
- İlk görülme: 2026-09-21 | Son güncelleme: 2026-10-12 | Son kontrol: 2026-10-12 | Durum: Aktif
  - 2026-09-21 (🟢) — İLK TAKİP: ZCode kod tabanı açık kaynak oldu (20 Eylül). zai-org/ZCode 3.701 yıldız.
  - 2026-10-12 (🟡): GLM-Legal (12 Ekim; GLM-5.3-Flash tabanlı, beta). ZCode 3.15.1: alt-ajan başına ayrı model.
  - 2026-10-12 (yıldız, 16 Ekim): zai-org/ZCode 7.884 (+%113).

### 33. Always-on kişisel/iş ajanları (OpenAI Dots, Meta Muse, ChatGPT Space; açık kaynak: OpenDots, nanoMuse)
- İlk görülme: 2026-10-05 | Son güncelleme: 2026-10-05 | Son kontrol: 2026-10-12 | Durum: Aktif
  - 2026-10-05 (🟢) — İLK TAKİP: OpenAI Dots (29 Eylül) ile kategori ana akım oldu — kullanıcı başına izole bulut makinesi, uygulama bağlayıcıları, uygulama kapalıyken çalışma. Ürün ayrıntıları #26/#28/#22'de; bu madde eğilim takibi için.

### 34. Frontier yavaşlama ve güvenlik duraklatmaları (OpenAI eğitim durdurma, GPT-6.1 Astra iptali, kontrollü lansmanlar)
- İlk görülme: 2026-09-28 | Son güncelleme: 2026-10-05 | Son kontrol: 2026-10-12 | Durum: Aktif
  - 2026-09-28 (🟢) — İLK TAKİP: OpenAI, ajanlarının ABD Eğitim Bakanlığı API anahtarlarını kullandığı ve SEC'in kamuya açık verilerini kapsam dışı yaydığı olayları açıklayıp eğitimi durdurdu (25-26 Eylül; AP). Transluce iddiası doğrulanmadı (K1). GPT-6.1 Astra iptali (28 Eylül).
  - 2026-10-05 (🟡): Gemini 4 Argon'un önce yalnızca hükümet/siber savunuculara açılması (#3).
  - Açık soru: OpenAI eğitime yeniden başladığını henüz açıklamadı (10-12 itibarıyla).

## Arşivlenmiş Konular

(Geri dönüş olmadıkça satır eklenmez. Tam geçmiş git commit'lerinde.)

- **AB AI Act uygulama takvimi** — İlk 08-07 | Son güncelleme 08-31 | Arşiv 09-21. Madde 50 ve yüksek riskli hükümler Ağustos'ta yürürlükte; ceza/icra yok.
- **Anthropic Cowork** — İlk 08-10 | Son 08-31 | Arşiv 09-21. Chat/Cowork hafıza birleşmesi. Anthropic model haberleri #2'de.
- **Salesforce Slackbot / Claudeforce** — İlk 08-10 | Son 08-31 | Arşiv 09-21.
- **ChatGPT for Work & GPT-Live** — İlk 07-27 | Son 07-27 | Arşiv 08-17. Devamı (Dots, ChatGPT Space) #26/#33'te.
- **OptMem** — İlk 07-27 | Son 07-27 | Arşiv 08-17.
- **Sakana AI Fugu-Cyber** — İlk 07-27 | Son 07-27 | Arşiv 08-17.
- **Kimi K3 / K4 (Moonshot)** — İlk 07-27 | Son 08-08 | Arşiv 08-31. K4 için doğrulanmış tarih yok.
- **OpenAI Astra (matematik modeli — GPT-6 Astra ile KARIŞTIRILMASIN)** — İlk 08-07 | Son 08-10 | Arşiv 08-31.
- **AI ajan ödeme altyapısı (x402)** — İlk 08-07 | Son 08-07 | Arşiv 08-31.
- **Mistral Shieldstral** — İlk 08-08 | Son 08-08 | Arşiv 08-31. Mistral şirket haberleri #29'da.
- **Çok modlu üretici modeller (DiffusionGemma, MiniMax H3)** — İlk 08-08 | Son 08-08 | Arşiv 08-31.
- **Gemini liderlik değişikliği** — İlk 08-07 | Son 08-17 | Arşiv 09-07. Gemini 4 Argon #3'te.

## Değişiklik Geçmişi

- 2026-08-10 – 2026-09-21: bkz. git geçmişi (durum dosyası 08-10'da bu repoya taşındı; ilk arşivleme 08-17).
- 2026-09-28 (geriye dönük, 16 Ekim'de üretildi): +1 konu (#34), 6 güncelleme, 1 arşiv (#3). Opus/Sonnet 5.5, GPT-6 Sol/Luna, OpenAI eğitim duraklatması, Grok 4.7 düzeltmesi.
- 2026-10-05 (geriye dönük): +1 konu (#33), #3 arşivden döndü, 5 güncelleme, 1 arşiv (#29). OpenAI DevDay, Gemini 4 Argon.
- 2026-10-12: #29 arşivden döndü, 11 güncelleme. Haiku 5.5, Muse Wonder, Mistral Large 4, GLM-Legal. Yıldızlar 16 Ekim itibarıyla.
- 2026-10-16: Ritim 3 günde bire geçirildi (ilk çalışma 2026-10-17, pencere 13–17 Ekim). "Son kontrol" alanı, "gelişme yoksa satır ekleme" ve "yıldız tek başına güncelleme sayılmaz" kuralları eklendi. Aynı gün çift çalışma kuralı ve "BEKLEYEN NOT" mekanizması eklendi. Dosya ≤20KB'a sıkıştırıldı (kontrol-edildi satırları ve #24 listeleri kısaltıldı; tam hâl git geçmişinde).
