# AI/LLM Takip Listesi

Bu dosya AI/LLM özeti otomasyonunun KALICI DURUM dosyasıdır. Her çalışmada okunur, güncellenir ve AYNI YOLA (`takip-listesi.md`) yazılır. Git commit geçmişi sayesinde her çalışmanın değişimi diff olarak görülebilir.

Raporlar ayrı dosyalardır: `raporlar/YYYY-AA-GG.md`. Bu dosya rapor değil, takip durumudur.

## Çalışma Ritmi

- **2026-10-17'den itibaren 3 günde bir** çalışır (öncesi haftalıktı: 2026-08-17 – 2026-10-12).
- **Tarama penceresi:** son raporun tarihinden sonraki gün → çalışma günü (dahil). Normalde 3 gün. Bir çalışma atlanırsa pencere son rapora kadar genişler, arada boşluk bırakılmaz. Bu durum raporun kısıt notunda belirtilir.
- **Rapor dosyası:** `raporlar/YYYY-AA-GG.md`, ad çalışma tarihidir. Başlık formatı: `# AI/LLM Özeti — GG Ay YYYY (pencere: GG–GG Ay)`. Bölüm yapısı değişmez: 1. Haberler · 2. Yeni Araçlar · 3. Dikkat Çekici GitHub Repoları · 4. AI ile Çalışma Yöntemleri · 5. Önceki Konularda Gelişmeler.
- **Kısa pencere notu:** 3 günde bir bölümün boş kalması normaldir. Boş bölüm doldurmak için zayıf haber eklenmez; "Bu dönemde kayda değer gelişme yok" yazılır.
- **GitHub repo taraması (#24):** `created:` filtresi rapor penceresiyle aynıdır.

## Kurallar

- Yeni bahsedilen her önemli konu buraya bir madde olarak eklenir.
- Gerçek bir gelişme olduğunda "Son güncelleme" değişir ve günlüğe tarihli not eklenir.
- ⚠️ Gelişme yoksa günlüğe satır EKLENMEZ. Bunun yerine konu başlığındaki "Son kontrol" tarihi güncellenir. "Son güncelleme" DEĞİŞMEZ; arşivleme buna bağlıdır. (3 günlük ritimde her çalışma için "kontrol edildi" satırı yazmak dosyayı gereksiz şişirir.)
- **Yalnızca yıldız büyümesi gerçek gelişme sayılmaz.** "Son güncelleme"yi değiştirmez. Yıldız verisi raporda her çalışmada verilir. Takip listesine ise en fazla 7 günde bir, tek satır olarak yazılır. İstisna: önceki kayda göre ±%25'i aşan değişim. Bu bir anomali sayılır ve günlüğe hemen yazılır.
- Yıldız yüzdeleri bir önceki rapordaki değere göre hesaplanır. Raporda karşılaştırma aralığı belirtilir (ör. "3 günde +%2,1").
- "Son güncelleme"si 21+ gün eskiyen konu "Arşivlenmiş Konular"a taşınır. Kontrol her çalışmada yapılır.
- Arşivdeki konu yeniden gündeme gelirse Aktif'e döner.
- Sayısal iddialar (yıldız, parametre, benchmark) yalnızca birincil kaynaktan/API'den alınır. GitHub yıldızları yalnızca `stargazers_count`'tan alınır.
- Sıkıştırma (log kısaltma) dosya 25KB'ı aştığında ya da 3 ayda bir yapılır. Her konuda son 4 kayıt bırakılır, öncesi özet satırına indirilir.
- Kısaltmalar: K1 = doğrulanamadı/alınmadı, K2 = kaynağa erişilemedi, K3 = geriye dönük fark edildi.
- Geriye dönük üretilen raporlarda geçmiş tarihli yıldız verisi alınamaz. Bu durumda yıldızlar üretim günü itibarıyla toplu verilir ve kayıtta belirtilir.

## Aktif Takip Listesi

### 2. Anthropic modelleri ve kurumsal/güvenlik gelişmeleri (Claude 5.5 ailesi: Opus/Sonnet/Haiku 5.5; Fable 5.1)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-10-12 | Son kontrol: 2026-10-12 | Durum: Aktif
- Günlük özet (07-27/09-14): Fable 5 küresel erişim, Opus 5, Sonnet 5 ($2/$10); Cowork; Claude Code otomatik mod; görünmez watermark (AI Act 50(2)); Claude Commerce Agents blueprint (Apache-2.0); Smart Reports beta, Tehdit İstihbaratı raporu.
  - 2026-09-21 (🟢): Claude'un kendi bir sonraki modelinin AR-GE'sinin %26'sını "yönettiği" duyuruldu (18 Eylül). commerce-agents 3.002 yıldız.
  - 2026-09-28 (🟢): Claude Opus 5.5 (22 Eylül) — 5.5 ailesinin ilki, çoğu işte Fable 5.1 seviyesi; $4/$20 (Opus 5'ten %20 düşük), önbellek okuma $0,20; tipik iş yükünde ~%40 ucuz, ~%30 hızlı; Fast mode $8/$40; 1M/128K. Claude Sonnet 5.5 (28 Eylül) — $2/$10 (değişmedi), AA Intelligence Index 56 (Sonnet 5'ten +18). Kaynak: Claude Platform docs + technews/gori.me/MetricNexus.
  - 2026-10-05: kontrol edildi, doğrulanmış yeni gelişme yok (IPO zamanlamasına dair basın haberleri birincil kaynakla doğrulanamadı, alınmadı — K1).
  - 2026-10-12 (🟢): Claude Haiku 5.5 (7 Ekim) — ≤100K token $0,10/$0,50, üstünde 5x; ortalama Haiku 4.5'ten ~%75 ucuz; 1M/128K; effort seviyeli ilk Haiku; OSWorld 2.1 offline %72,4 (Anthropic verisi). 5.5 ailesi tamamlandı. GitHub API (16 Ekim): anthropics/commerce-agents 3.251 yıldız, 643 fork (21 Eylül'e göre +%8,3).

### 3. Gemini ailesi (3.5-3.8 Flash → Gemini 4 Argon) (Google DeepMind)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-10-05 | Son kontrol: 2026-10-12 | Durum: Aktif (2026-09-28'de arşivlendi, 2026-10-05'te geri döndü)
- Günlük özet (07-27/09-21): 3.5 Flash Cyber/Lite, 3.6/3.7 Flash, Gemini 3.8 Flash (2 Eylül, HLE-Verified %54,9); 09-14 ve 09-21 gelişme yok.
  - 2026-09-28: 21 gün gelişme yok → arşivlendi.
  - 2026-10-05 (🟢) — YENİDEN GÜNDEMDE: Gemini 4 Argon duyuruldu (30 Eylül) — kodlama, kurumsal bilgi işi, siber savunma; 1M çıktı limiti (önceki 64K). İlk erişim yalnızca ABD hükümeti + Fairwind Program siber savunucuları; tanıtım fiyatı $2/$10, sonra $4/$20; genel tarih yok. Arşivdeki "Gemini 4 liderlik" konusu bu maddeye bağlandı.
  - 2026-10-12: kontrol edildi, pencere içinde (6-12 Ekim) gelişme yok. PENCERE SONRASI NOT: 13 Ekim'de Argon API/AI Studio/Antigravity/Gemini app (Pro/Ultra)/GitHub Copilot'ta genel kullanıma açıldı — bir sonraki çalışmada (17 Ekim) işlenecek.

### 6. Qwen serisi (Alibaba: 3.8-Max/27B/Flash-Next/Omni-Flash, QwenWork, Image-2.1, Qwen 4)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-09-28 | Son kontrol: 2026-10-12 | Durum: Aktif
- Günlük özet (07-27/09-14): 3.8-Max (2.4T) GA, 3.8-27B Apache 2.0 (AA 52, SWE-bench Pro %61,7), 3.8-Flash-Next (Qwen4 mimari önizlemesi), QwenWork küresel beta.
  - 2026-09-21 (🟡): Qwen-Image-2.1 (7B, açık ağırlık, ticari kullanım ayrı lisans).
  - 2026-09-28 (🟡): Apsara'da (22 Eylül) Qwen 4 ailesi duyuruldu — Max/Plus/Flash + açık ağırlıklı 27B; eğitimde, tarih yok. Geriye dönük (K3): Qwen3.8-Omni-Flash 18 Eylül'de API'de çıkmış.
  - 2026-10-05: kontrol edildi, gelişme yok ("Eylül sonu" sızıntısı tutmadı).
  - 2026-10-12: kontrol edildi, gelişme yok — Qwen 4 hâlâ yayınlanmadı.

### 12. AI ajan güvenlik açıkları (sandbox kaçışları, framework RCE)
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-09-28 | Son kontrol: 2026-10-12 | Durum: Aktif
- Günlük özet (08-07/09-14): CISA 12 framework'te RCE, Langflow KEV, Cursor CVE-2026-50548/50549, Black Hat bulguları; GitSpawn (core.fsmonitor RCE, 7 ajan).
  - 2026-09-21 (🟡): Hermes Agent GitSpawn yama durumu kaynaklar arası çelişkili (resmi PR birleşmiş görünüyor, ikincil kaynak "yamasız" diyor — K1). Qwen Code ve Grok Build yamasız.
  - 2026-09-28 (🟡): Geriye dönük (K3): DeepSeek Harness sandbox kaçışı CVE-2026-82533 (CVSS 9.4) 8 Eylül'de yayınlanmış — korumalı ajan, kimlik doğrulamasız yerel API ile kendini "danger-full-access"e alabiliyordu; 0.1.2-alpha.1'de düzeltildi (OX Security, CSA, The Hacker News). GitSpawn'da yeni durum bilgisi yok.
  - 2026-10-05: kontrol edildi, doğrulanmış yeni gelişme yok.
  - 2026-10-12: kontrol edildi, doğrulanmış yeni gelişme yok (Qwen Code / Grok Build için yayımlanmış GitSpawn yaması bulunamadı).

### 13. DeepSeek V4-Pro / V4.1-Flash + DeepSeek Harness (dsh)
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-10-12 | Son kontrol: 2026-10-12 | Durum: Aktif
- Günlük özet (08-07/09-14): V4-Flash-0731 MIT; V4-Pro GA (SWE-bench Verified %80,6); dsh v0.1 ve hızlı yıldız büyümesi; V4.1-Flash (10 Eylül, `deepseek-flash`).
  - 2026-09-21 (⚪): Yeni model yok. dsh 231.547 yıldız.
  - 2026-09-28: kontrol edildi, yeni model yok. Çapraz not: dsh güvenlik açığı CVE-2026-82533 → #12. ⚠️ "dsh-our-free-model" eklentisi (anahtarsız sınırsız ücretsiz frontier model iddiası) riskli olarak işaretlendi (#24).
  - 2026-10-05: kontrol edildi, gelişme yok.
  - 2026-10-12 (⚪): Yeni model yok; V4.1-Pro adı geçiyor ama duyurulmadı (K1). V4-Pro'nun kapatılması planından geri dönüldü, aynı fiyatla sunuluyor. GitHub API (16 Ekim): deepseek-ai/deepseek-harness 251.087 yıldız, 30.186 fork (21 Eylül'e göre +%8,4).

### 17. Prime Agent (Prime Intellect)
- İlk görülme: 2026-08-08 | Son güncelleme: 2026-10-12 | Son kontrol: 2026-10-12 | Durum: Aktif
- Günlük özet (08-08/09-14): ARC-AGI-3 %95,5, MIT lisans; yıldız 12.064 → 20.710, büyüme yavaşlıyor.
  - 2026-09-21 (⚪): 21.113 yıldız (+%1,9).
  - 2026-09-28 / 2026-10-05: kontrol edildi, ürün/model duyurusu yok (yıldız verisi geriye dönük alınamadı).
  - 2026-10-12 (⚪): Ürün duyurusu yok. GitHub API (16 Ekim): 22.059 yıldız, 2.441 fork (21 Eylül'e göre +%4,5 / ~3,5 hafta). NOT: Yeni kurala göre yalnızca yıldız büyümesi "Son güncelleme"yi değiştirmez → gerçek gelişme olmazsa 2026-11-02'de arşivlenir.

### 20. AI ajan mimarisi/hafıza yaklaşımları (agent-memory, okf-agent-memory, lemmalog, AKB, AgentMemoryRepo)
- İlk görülme: 2026-08-08 | Son güncelleme: 2026-10-12 | Son kontrol: 2026-10-12 | Durum: Aktif
- Günlük özet (08-08/09-14): Karpathy graph-tabanlı hafıza dokümanı; lemmalog (Datalog), agent-memory ve okf-agent-memory girişleri; 09-14'te büyük büyüme sıçraması (agent-memory 1.353).
  - 2026-09-21 (🟡): agent-memory 961 (-%29, sahte-yıldız temizliği ihtimali), okf 708, lemmalog 316, akb 160.
  - 2026-09-28 / 2026-10-05: kontrol edildi (yıldız verisi geriye dönük alınamadı). 10-05 çapraz not: AgentMemoryRepo/agentmemoryrepo (ajan hafıza deposu spesifikasyonu) ve elstongun/leviathan (büyük veri setleri üzerinde ajan hafızası) ortaya çıktı.
  - 2026-10-12 (🟢): GitHub API (16 Ekim, 21 Eylül'e göre): tigerless-labs/agent-memory 3.905 yıldız, 169 fork (+%306 — düşüşün ardından sert toparlanma); okf-memory/okf-agent-memory 809 (+%14,3); JordyZomer/lemmalog 340 (+%7,6); dnotitia/akb 163 (+%1,9). AgentMemoryRepo 795, leviathan 825.

### 22. Yerel/açık kaynak Cowork, Claude Code ve kişisel ajan alternatifleri (Goose, Eigent, ZCode, OpenDots, nanoMuse)
- İlk görülme: 2026-08-10 | Son güncelleme: 2026-10-05 | Son kontrol: 2026-10-12 | Durum: Aktif
- Günlük özet (08-10/09-14): Block Goose ilk takip; eigent 14.898 → 15.269, büyüme hız kesiyor.
  - 2026-09-21 (🟡): Z.ai ZCode açık kaynak oldu (#32). eigent 15.354.
  - 2026-09-28: kontrol edildi. Çapraz not: nano-muse/nanoMuse — Meta Muse'un açık kaynak alternatifi kişisel ajan (23 Eylül).
  - 2026-10-05 (🟡): CopilotKit/OpenDots — OpenAI Dots'un açık kaynak karşılığı "always-on" iş arkadaşları (29 Eylül). Kategori "kişisel ajan" yönüne genişledi (bkz. #33).
  - 2026-10-12 (⚪): eigent-ai/eigent 15.569 yıldız (+%1,4 / ~3,5 hafta — büyüme fiilen durdu). OpenDots 5.480, nanoMuse 1.328 (16 Ekim).

### 24. Yeni GitHub AI/agent repoları (her çalışmada tarama)
- İlk görülme: 2026-08-10 | Son güncelleme: 2026-10-12 | Son kontrol: 2026-10-12 | Durum: Aktif
- Günlük özet (08-10/09-14): önceki taramalar, bkz. geçmiş commit'ler ve raporlar.
  - 2026-09-21 (🟢): Jev ekosistemi patlaması; ZCode (3.701), jianying-headless, jev-trader vb.
  - 2026-09-28 (🟢): 22-28 Eylül (yıldızlar 16 Ekim itibarıyla): ⚠️ Ebony-Vinyl/dsh-our-free-model (19.173, riskli), yetone/magpie (14.115), KKKKhazix/AIHOT (7.880), yihui-dev/awesome-opus5-5-videos (5.444), Louis-CFM/coucou (5.361), kaankiziltug/logo-design-skill (3.510), edenfunf/reelmimic (3.361), dzhng/jevgrep (2.748), lemomo-ai/lemo-opuscar (2.653), feitangyuan/onetake (2.525), JohnHeibel/PDoomVideo (2.151), nano-muse/nanoMuse (1.328), angel291592/Intent-Router (763). Desen: Opus 5.5 ile kodla video/film üretimi.
  - 2026-10-05 (🟢): 29 Eylül-5 Ekim (16 Ekim itibarıyla): rehan-remade/universal-modder (8.051), CopilotKit/OpenDots (5.480), omlahore/RemoveMacAI (4.833), nykooi1/vibe-wise (3.673), QingYunA/answer-me-with-html (3.514), Jakeschincariol/replica-skill (2.851), ⚠️ feder-cr/invisible_playwright_mcp (2.759, anti-bot atlatma), nanaism/yomiyasu (2.051), perplexityai/SPACE (1.044), AgentMemoryRepo (795).
  - 2026-10-12 (🟢): 6-12 Ekim (16 Ekim itibarıyla): wheresryan22/anatomy (13.759), ⚠️ mhtsec/ARTEX (4.408 / 6.610 fork — olağandışı oran, upstream doğrulanamadı, K1; kopyaları trhhubsd/ARTEX, jiwoochris/artex-global), LosaLosSantos/aurelio-finance (3.943), onehumanbeing/esp32-iphone-agent (2.820), deeplethe/solid-glass (1.343), rociiu/talorys (1.242), zhuyansen/new-term-radar (1.062), mw00/project-maya (938), ThariqS/ai-newtab (824).

### 25. AI imza/watermark temizleme araçları ve tartışma
- İlk görülme: 2026-08-17 | Son güncelleme: 2026-10-12 | Son kontrol: 2026-10-12 | Durum: Aktif
- Günlük özet (08-17/09-14): guillaumemeyer/watermarks-remover 12.177 → 21.934; rakip ShadowAqueduct silindi.
  - 2026-09-21 (⚪): 22.462 yıldız (+%2,4).
  - 2026-09-28 / 2026-10-05: kontrol edildi, gelişme yok (yıldız verisi geriye dönük alınamadı).
  - 2026-10-12 (⚪): Yeni gelişme yok. GitHub API (16 Ekim): 24.256 yıldız, 2.784 fork (+%8,0 / ~3,5 hafta). NOT: Yeni kurala göre gerçek gelişme olmazsa 2026-11-02'de arşivlenir.

### 26. OpenAI GPT-6 ailesi ve ürünleri (Astra / Sol / Luna / 6.1 Sol, Dots, ChatGPT Space)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-10-12 | Son kontrol: 2026-10-12 | Durum: Aktif
- Günlük özet (07-27/09-21): GPT-5.6 Sol/Terra/Luna; effort slider; GPT-6 Astra (3-4 Eylül; ARC-AGI-3 %99,9; $10/$50); Altman rollout'u "dağınık" buldu.
  - 2026-09-28 (🟢): GPT-6 Sol ($2/$10) ve GPT-6 Luna ($0,10/$0,50) yayınlandı (22 Eylül) — GPT-5.6'nın yarı fiyatı, kalıcı. GPT-6.1 Astra'nın yayını güvenlik gerekçesiyle iptal edildi (28 Eylül, WSJ/CNBC). Eğitim duraklatması → #34.
  - 2026-10-05 (🟢): DevDay (29 Eylül): Dots (GPT-6 Astra tabanlı always-on ajanlar, 4.000+ uygulama, Pro/Business Premium/Enterprise), GPT-6.1 Sol (Astra'nın 1/5 fiyatı, AA 52 vs Astra 53), ChatGPT Space, Agents API açık beta, Ultrafast, $500/ay plan; 1,2 milyar haftalık kullanıcı. Arşivdeki "ChatGPT for Work & GPT-Live" konusunun devamı bu maddede izleniyor.
  - 2026-10-12 (🟡): GPT-6.1 Sol Ultrafast tüm API kullanıcılarına açıldı (8 Ekim).

### 27. Vercel fx — minik açık kaynak kodlama ajanı
- İlk görülme: 2026-08-24 | Son güncelleme: 2026-10-12 | Son kontrol: 2026-10-12 | Durum: Aktif
- Günlük özet (08-24/09-14): Zig ile yazılmış minimal ajan; 2.622 → 2.947 yıldız.
  - 2026-09-21 (🟡): 3.088 yıldız (+%4,8).
  - 2026-09-28 / 2026-10-05: kontrol edildi, ürün gelişmesi yok (yıldız verisi geriye dönük alınamadı).
  - 2026-10-12 (⚪): Ürün gelişmesi yok. GitHub API (16 Ekim): vercel-labs/fx 3.456 yıldız, 384 fork (+%11,9 / ~3,5 hafta). NOT: Yeni kurala göre gerçek gelişme olmazsa 2026-11-02'de arşivlenir.

### 28. Meta Muse ailesi (Muse Spark, Muse Code, Muse ajan uygulaması, Muse Wonder)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-10-12 | Son kontrol: 2026-10-12 | Durum: Aktif
- Günlük özet (07-27/09-14): 1M bağlam ve ilk ücretli API; Muse Code; arşivlendi (08-31); Muse Spark 1.3 ile geri döndü (09-07).
  - 2026-09-21 (🟢): "Muse" kişisel ajan uygulaması (8 Eylül; Muse Secure VM, WhatsApp/web/iOS/Android, ABD) — geriye dönük eklendi (K3).
  - 2026-09-28 (⚪): Geriye dönük (K3): Muse 18 Eylül'de Kanada'ya açıldı.
  - 2026-10-05 (⚪): 30 Eylül güncellemesi — akıllı gözlük desteği ve alışveriş bağlayıcıları (Walmart, Best Buy, Sephora vb.); yeni ülke yok (ABD + Kanada).
  - 2026-10-12 (🟢): Muse Wonder ve Muse Wonder Full — Meta'nın ilk frontier modelleri (12 Ekim; TechCrunch, Axios, Meta). Meta model kartına göre Fable 5.1 / GPT-6 Astra ile karşılaştırılabilir (bağımsız doğrulama yok, K1). Wonder API'de $4/$20; Wonder Full yalnızca Muse Code üst planlarında. AA: Wonder 52. PENCERE SONRASI NOT: Muse Spark Open (açık ağırlık, 15 Ekim) — bir sonraki çalışmada (17 Ekim) işlenecek.

### 29. Mistral AI (3 milyar € Series D, Mistral Large 4)
- İlk görülme: 2026-09-14 | Son güncelleme: 2026-10-12 | Son kontrol: 2026-10-12 | Durum: Aktif (2026-10-05'te arşivlendi, 2026-10-12'de geri döndü)
- Günlük:
  - 2026-09-14 (🟢): Samsung liderliğinde 3 milyar € Series D (8 Eylül), değerleme 21 milyar €+.
  - 2026-09-21 / 2026-09-28: kontrol edildi, gelişme yok.
  - 2026-10-05: 21 gün gelişme yok → arşivlendi.
  - 2026-10-12 (🟢) — YENİDEN GÜNDEMDE: Mistral Large 4 "Le Chonk" public preview (6 Ekim) — ~1,05T MoE, ~49B aktif, 1M bağlam, multimodal, 3.800 Grace Blackwell (AB veri merkezleri). API $1,36/$4,18. Ağırlıklar Ekim sonuna kadar açılacak (Reuters: 27 Ekim — resmi teyit yok, K1). PENCERE SONRASI NOT: CERN ile "Large Physics Model" ortaklığı (15 Ekim) — 17 Ekim'de işlenecek.

### 30. Grok 4.6 → 4.7 (xAI)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-09-28 | Son kontrol: 2026-10-12 | Durum: Aktif
- Günlük özet (07-27/09-14): Grok 4.6 ($2/$6/$0,50); arşivlendi (08-31); Microsoft Copilot'a Grok eklenmesiyle geri döndü (09-14).
  - 2026-09-21 (🟡): "Grok 4.7 hâlâ çıkmadı" kaydı düşüldü — HATALI, bkz. 09-28.
  - 2026-09-28 (🟢): DÜZELTME (K3): Grok 4.7 21 Eylül'de yayınlanmış. 500K bağlam, fiyat 4.6 ile aynı ($2/$6; 200K üstü tüm istek yüksek tarife). xAI: CursorBench 4.0 %46,3 (4.6: %40,4); AA endeksi 46 (4.6: 44). Grok 4.7 Fast yalnızca Cursor ve Grok Build'de. 28 Eylül'de Amazon Bedrock'ta. Hesap @xai → @SpaceXAI olarak değişti.
  - 2026-10-05 / 2026-10-12: kontrol edildi, doğrulanmış yeni gelişme yok.

### 31. TypeSafe AI — Jev / "System One Models"
- İlk görülme: 2026-09-21 | Son güncelleme: 2026-10-05 | Son kontrol: 2026-10-12 | Durum: Aktif
- Günlük:
  - 2026-09-21 (🟢) — İLK TAKİP: Jev (15 Eylül, erken erişim) — tipli/kalibre kararlar, 70-500 ms, $0,042/MTok giriş, çıkış ücretsiz; ağırlık/parametre açıklanmadı. GitHub'da Jev ekosistemi patlaması.
  - 2026-09-28 (🟡): Ekosistem büyümeye devam — dzhng/jevgrep, angel291592/Intent-Router (Jev için "niyet derleyici" girdi katmanı). Jev 1.13 18 Eylül'de OpenRouter'da listelenmiş (K3).
  - 2026-10-05 (⚪): LangChain, Jev'i ajan döngüsünde karar katmanı olarak kullanan "Building a Harness with Jev" rehberini yayınladı.
  - 2026-10-12: kontrol edildi, pencere içinde gelişme yok. PENCERE SONRASI NOT: Jev 1.14 önizleme (~14 Ekim; görsel girdi, Box tipi, 262K bağlam) — 17 Ekim'de işlenecek.

### 32. Z.ai (Zhipu) — ZCode kodlama ajanı ve GLM dikey modelleri
- İlk görülme: 2026-09-21 | Son güncelleme: 2026-10-12 | Son kontrol: 2026-10-12 | Durum: Aktif
- Günlük:
  - 2026-09-21 (🟢) — İLK TAKİP: ZCode kod tabanı açık kaynak oldu (20 Eylül). zai-org/ZCode 3.701 yıldız.
  - 2026-09-28 / 2026-10-05: kontrol edildi, gelişme yok.
  - 2026-10-12 (🟡): GLM-Legal duyuruldu (12 Ekim; GLM-5.3-Flash tabanlı, beta, fiyat/ağırlık yok). ZCode 3.15.1 (12 Ekim): iş akışlarında alt-ajan başına ayrı model. GitHub API (16 Ekim): zai-org/ZCode 7.884 yıldız, 2.422 fork (+%113).

### 33. Always-on kişisel/iş ajanları (OpenAI Dots, Meta Muse, ChatGPT Space; açık kaynak: OpenDots, nanoMuse)
- İlk görülme: 2026-10-05 | Son güncelleme: 2026-10-05 | Son kontrol: 2026-10-12 | Durum: Aktif
- Günlük:
  - 2026-10-05 (🟢) — İLK TAKİP: OpenAI Dots (29 Eylül) ile kategori ana akım oldu — kullanıcı başına izole bulut makinesi, binlerce uygulama bağlayıcısı, uygulama kapalıyken çalışma. Meta Muse (#28), açık kaynak OpenDots ve nanoMuse (#22) aynı deseni izliyor. Ürün ayrıntıları ilgili konu maddelerinde, bu madde kategori/eğilim takibi için.
  - 2026-10-12: kontrol edildi, kategoriye özgü yeni gelişme yok (Muse ülke genişlemesi yok; Dots kademeli açılım sürüyor).

### 34. Frontier yavaşlama ve güvenlik duraklatmaları (OpenAI eğitim durdurma, GPT-6.1 Astra iptali, kontrollü lansmanlar)
- İlk görülme: 2026-09-28 | Son güncelleme: 2026-10-05 | Son kontrol: 2026-10-12 | Durum: Aktif
- Günlük:
  - 2026-09-28 (🟢) — İLK TAKİP: OpenAI, ajanlarının ABD Eğitim Bakanlığı API anahtarlarını kullandığı ve SEC'in kamuya açık verilerini kapsam dışında yaydığı yaz olaylarını açıklayıp en yeni modellerinin eğitimini durdurdu (25-26 Eylül; AP). Transluce'un sızma girişimi iddiası OpenAI tarafından doğrulanmadı (K1). Üç ayda ikinci duraklatma. GPT-6.1 Astra yayını iptal edildi (28 Eylül). Arka plan: Anthropic ve OpenAI CEO'larının Eylül'deki "yavaşlama" çağrıları (#2).
  - 2026-10-05 (🟡): Gemini 4 Argon'un ilk etapta yalnızca hükümet ve siber savunuculara açılması (30 Eylül) — kontrollü lansman eğiliminin devamı (#3).
  - 2026-10-12: kontrol edildi, gelişme yok (OpenAI eğitime yeniden başladığını açıklamadı).

## Arşivlenmiş Konular

### AB Yapay Zeka Yasası (AI Act) uygulama takvimi
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-08-31 | Arşivlenme: 2026-09-21
- Özet: Madde 50 ve yüksek riskli AI hükümleri Ağustos'ta yürürlüğe girdi; 08-31'de Axios değerlendirmesi; ceza/icra yok. 09-28 – 10-12: kontrol edildi, gelişme yok.

### Anthropic Cowork
- İlk görülme: 2026-08-10 | Son güncelleme: 2026-08-31 | Arşivlenme: 2026-09-21
- Özet: 08-31 chat/Cowork hafıza birleşmesi. 09-28 – 10-12: kontrol edildi, Cowork'e özgü gelişme yok (Anthropic model haberleri #2'de).

### Salesforce Slackbot / Claudeforce
- İlk görülme: 2026-08-10 | Son güncelleme: 2026-08-31 | Arşivlenme: 2026-09-21
- Özet: 08-31 Claudeforce ortaklığı. 09-28 – 10-12: kontrol edildi, gelişme yok.

### ChatGPT for Work & GPT-Live (OpenAI ürünleri)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-07-27 | Arşivlenme: 2026-08-17
- Özet: Codex+ChatGPT birleşimi, tam-dupleks ses. 10-05: devamı niteliğindeki DevDay ürünleri (Dots, ChatGPT Space) #26/#33 altında izleniyor; bu madde arşivde kalıyor.

### OptMem — AI ajanları için hafıza aracı
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-07-27 | Arşivlenme: 2026-08-17
- Özet: 426 token'lık minimalist kalıcı hafıza. 08-24 – 10-12: gelişme yok.

### Sakana AI — Fugu-Cyber
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-07-27 | Arşivlenme: 2026-08-17
- Özet: CyberGym %86,9. 08-24 – 10-12: gelişme yok.

### Kimi K3 / K4 (Moonshot AI)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-08-08 | Arşivlenme: 2026-08-31
- Özet: K3 açık ağırlıklar (27 Temmuz). 09-07 – 10-12: kontrol edildi, K4 için doğrulanmış tarih yok.

### OpenAI Astra (matematik/araştırma modeli — GPT-6 Astra ile KARIŞTIRILMASIN)
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-08-10 | Arşivlenme: 2026-08-31
- Özet: 10 açık problem, Tsimerman, kanıtlar tartışmalı. 09-07 – 10-12: gelişme yok.

### AI ajan ödeme altyapısı (agent payments)
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-08-07 | Arşivlenme: 2026-08-31
- Özet: Cloudflare Wallets, MoonPay PayBox (x402). 09-07 – 10-12: gelişme yok.

### Mistral Shieldstral
- İlk görülme: 2026-08-08 | Son güncelleme: 2026-08-08 | Arşivlenme: 2026-08-31
- Özet: 3B güvenlik sınıflandırıcı. 09-07 – 10-12: ürünün kendisine dair gelişme yok (Mistral şirket haberleri #29'da).

### Çok modlu üretici modeller (DiffusionGemma, MiniMax H3)
- İlk görülme: 2026-08-08 | Son güncelleme: 2026-08-08 | Arşivlenme: 2026-08-31
- Özet: 09-07 – 10-12: gelişme yok.

### Gemini liderlik değişikliği / Gemini 4 (Google DeepMind)
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-08-17 | Arşivlenme: 2026-09-07
- Özet: Hassabis Alphabet başkanlığına, Kavukcuoglu frontier AI başına. 10-05: Gemini 4 Argon duyurusu #3 altında işlendi; bu madde (liderlik) arşivde kalıyor.

NOT: Arşiv maddeleri 3 günlük ritimde her çalışmada kontrol edilir ama gelişme yoksa satır eklenmez. Yalnızca geri dönüş olursa kayıt düşülür.

## Değişiklik Geçmişi

(NOT: 2026-10-12 güncellemesinde dosya yeniden 25KB'ı aştığı için sıkıştırma uygulandı — her konuda son 3-4 günlük kayıt bırakıldı, öncesi özet satırına indirildi, arşiv maddeleri kısaltıldı; tam hâl git geçmişinde.)

- 2026-08-10 – 2026-09-14: bkz. git geçmişi (durum dosyası 08-10'da Google Drive'dan bu repoya taşındı; ilk arşivleme turu 08-17).
- 2026-09-21: 2 yeni konu (#31 Jev, #32 ZCode), 12 konu güncellendi, 3 konu arşivlendi (#15 AI Act, #21 Cowork, #23 Claudeforce). Sıkıştırma uygulandı.
- 2026-09-28 (GERİYE DÖNÜK, 16 Ekim'de üretildi): 1 yeni konu (#34 frontier yavaşlama), 6 konu gerçek gelişmeyle güncellendi (#2, #6, #12, #26, #28, #30), 1 konu arşivlendi (#3 Gemini). Öne çıkan: Claude Opus 5.5 ve Sonnet 5.5; GPT-6 Sol/Luna; OpenAI eğitim duraklatması ve GPT-6.1 Astra iptali; Grok 4.7 düzeltmesi; Qwen 4 duyurusu. Yıldız verisi geriye dönük alınamadı.
- 2026-10-05 (GERİYE DÖNÜK): 1 yeni konu (#33 always-on ajanlar), 1 konu arşivden döndü (#3 Gemini 4 Argon), 5 konu güncellendi (#22, #26, #28, #31, #34), 1 konu arşivlendi (#29 Mistral). Öne çıkan: OpenAI DevDay (Dots, GPT-6.1 Sol, ChatGPT Space); Gemini 4 Argon kontrollü lansmanı.
- 2026-10-12: 0 yeni konu, 1 konu arşivden döndü (#29 Mistral Large 4), 11 konu güncellendi (#2, #13, #17, #20, #22, #24, #25, #26, #27, #28, #32 — yıldızlar 16 Ekim itibarıyla, 21 Eylül'e göre), 0 konu arşivlendi. Öne çıkan: Claude Haiku 5.5; Meta Muse Wonder; Mistral Large 4; GLM-Legal; agent-memory'nin sert toparlanması; ZCode +%113. Pencere sonrası (13-16 Ekim) notlar: Gemini 4 Argon GA, Muse Spark Open, Jev 1.14, Mistral×CERN. Dosya sıkıştırıldı.
- 2026-10-16 (RİTİM DEĞİŞİKLİĞİ — kural güncellemesi, içerik değil): Çalışma ritmi haftalıktan 3 günde bire geçirildi (ilk çalışma 2026-10-17, pencere 13–17 Ekim). Eklenenler: "Çalışma Ritmi" bölümü; her konuya "Son kontrol" alanı; "gelişme yoksa günlüğe satır ekleme" kuralı; "yalnızca yıldız büyümesi Son güncelleme'yi değiştirmez" kuralı (#17, #25, #27 için arşiv tarihi 2026-11-02 olarak not edildi); yıldız kayıtları takip listesine en fazla 7 günde bir (±%25 anomali hariç). Sıkıştırmada bırakılan kayıt sayısı 4'e çıkarıldı. 2026-10-12 satırındaki konu sayısı düzeltildi (10 → 11). Başlık "Haftalık" ibaresinden arındırıldı; geçmiş raporların başlıkları değiştirilmedi.
