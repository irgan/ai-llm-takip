# AI/LLM Haftalık Takip Listesi

Bu dosya haftalık AI/LLM özeti otomasyonunun KALICI DURUM dosyasıdır. Her hafta okunur, güncellenir ve AYNI YOLA (`takip-listesi.md`) yazılır. Git commit geçmişi sayesinde her haftanın değişimi diff olarak görülebilir.

Haftalık raporlar ayrı dosyalardır: `raporlar/YYYY-AA-GG.md`. Bu dosya rapor değil, takip durumudur.

## Kurallar

- Yeni bahsedilen her önemli konu buraya bir madde olarak eklenir.
- Gerçek bir gelişme olduğunda "Son güncelleme" değişir ve günlüğe not eklenir.
- ⚠️ "Kontrol edildi, gelişme yok" notu günlüğe eklenir ama "Son güncelleme" tarihini DEĞİŞTİRMEZ. Arşivlemenin çalışması buna bağlıdır.
- "Son güncelleme"si 21+ gün eskiyen konu "Arşivlenmiş Konular"a taşınır.
- Arşivdeki konu yeniden gündeme gelirse Aktif'e döner.
- Sayısal iddialar (yıldız, parametre, benchmark) yalnızca birincil kaynaktan/API'den alınır. GitHub yıldızları yalnızca `stargazers_count`'tan.
- Sıkıştırma (log kısaltma) haftalık değil, dosya 25KB'ı aştığında ya da 3 ayda bir yapılır.

## Aktif Takip Listesi

### 2. Anthropic modelleri ve kurumsal/güvenlik gelişmeleri (Opus 5 / Fable 5 / Sonnet 5)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-09-21 | Durum: Aktif
- Günlük (07-27/08-17 özet: Fable 5 küresel erişim, Sonnet 5 tanıtım fiyatı $2/$10, Opus 5 yayınlandı; Cuéllar CGAO oldu, açık ağırlık pozisyon belgesi, Cognizant ortaklığı; Cowork yayınlandı, Claude Code'da otomatik mod varsayılan oldu — tehlikeli eylemlerin %89'unu yakaladı; 17 Ağustos'ta gelişme yok):
  - 2026-08-24 (🟡): Anthropic 11 Ağustos'ta tüm AI-üretimi çıktılara görünmez watermark ekleyeceğini duyurdu (AB AI Act Madde 50(2) uyumu, uygulama küresel).
  - 2026-08-31: kontrol edildi, gelişme yok (büyük haberler #21/#23 altında işlendi).
  - 2026-09-07 (🟢): "Claude Commerce Agents" (Apache-2.0) açık kaynak blueprint'i yayınlandı — Alışveriş + Satıcı ajanları. GitHub API: anthropics/commerce-agents 2.275 yıldız, 392 fork.
  - 2026-09-14 (🟡): Üç gelişme — "Smart Reports" (beta, 10 Eylül), Tehdit İstihbaratı raporu (10 Eylül), Claude Code 2.1.270 bash regresyon düzeltmesi (12 Eylül). commerce-agents 2.821 yıldız, 533 fork (%24,0 haftalık artış).
  - 2026-09-21 (🟢): Anthropic, Claude'un kendi bir sonraki modelinin AR-GE'sinde artık işin %26'sını "yönettiğini" duyurdu — Şubat'ta %0'dan Ağustos'ta %26'ya; R&D'nin %90'ında bir şekilde katkısı var; Ağustos itibarıyla ~30.000 ajan araştırma/mühendislik işi yapıyor (18 Eylül; resmi Anthropic duyurusu + spectrumlocalnews haberi ile doğrulandı). Duyuru, Dario Amodei'nin "yavaşlama" çağrılarıyla aynı haftaya denk geldi; Anthropic şeffaflık için diğer laboratuvarları da benzer metrikleri paylaşmaya çağırdı. GitHub API ile doğrulandı: anthropics/commerce-agents — 3.002 yıldız, 579 fork (2.821'den, %6,4 haftalık artış).

### 3. Gemini 3.5/3.6/3.7/3.8 Flash ailesi (Google DeepMind)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-09-07 | Durum: Aktif
- Günlük (07-27/08-17 özet: 3.5 Flash Cyber/Lite, 3.6 Flash ilk takip, amiral gemisi çıktı maliyeti $9.00→$7.50; yönetilen ajanlar platformu genişledi; Gemini 3.7 Flash duyuruldu — FrontierCode %34,4→%43,6, WebDev Arena 1538→1588 Elo):
  - 2026-08-24: kontrol edildi, gelişme yok.
  - 2026-08-31: kontrol edildi, gelişme yok.
  - 2026-09-07 (🟢): Gemini 3.8 Flash duyuruldu (2 Eylül) — "daha derin analiz" odaklı, HLE-Verified %54,9. NOT (K1): Giriş fiyatı kaynakta 3.7 Flash ile birebir aynıydı, doğrulanamadı olarak işaretlendi.
  - 2026-09-14: kontrol edildi, gelişme yok (Gemini API changelog'da 2-3 Eylül'den bu yana yeni girdi yok).
  - 2026-09-21: kontrol edildi, gelişme yok (Gemini API changelog'da yeni girdi yok; Gemini 4 hakkında yalnızca doğrulanmamış "release date" tahmin makaleleri bulundu, rapora alınmadı — K1).

### 6. Qwen serisi (Alibaba: 3.8-Max, 3.8-27B, 3.8-Flash-Next, QwenWork, Image-2.1)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-09-21 | Durum: Aktif
- Günlük (07-27/08-17 özet: 3.8-Max-Preview, Audio-3.0-TTS #1, Image-3.0 ilk takip; 3.8-Max resmen duyuruldu 2.4T; 3.8-Max GA oldu + 27B açık ağırlıklı varyant yayınlandı; gelir paylaşımlı lisans modeli duyurusu):
  - 2026-08-24: kontrol edildi, doğrudan AI/ürün gelişmesi yok.
  - 2026-08-31 (🟢): Qwen3.8-27B (Apache 2.0) geniş basın ilgisi gördü — Artificial Analysis Intelligence Index 52 puan, SWE-bench Pro %61,7.
  - 2026-09-07 (🟡): Geriye dönük fark edilen gelişme — Qwen3.8-Flash-Next yayınlandı (~26 Ağustos), Qwen4 mimarisinin önizlemesi olarak sunuluyor.
  - 2026-09-14 (🟡): Geriye dönük fark edilen gelişme — "QwenWork" ajan platformu küresel beta olarak genişledi (1 Eylül duyurusu).
  - 2026-09-21 (🟡): Alibaba, açık ağırlıklı Qwen-Image-2.1'i yayınladı (20 Eylül; CellCog/ExplainX/RuntimeWire/36Kr haberleri + resmi GitHub reposu ile doğrulandı). 7B parametreli görsel üretici, metinden-görsele üretim ve görsel düzenlemeyi tek sistemde birleştiriyor, native RGBA şeffaflık destekliyor, tek kompozisyonda 10 referans görsele kadar destekliyor (32 katmanlı diffusion transformer + Qwen3-VL 8B metin kodlayıcı). Hugging Face/ModelScope/GitHub'da eşzamanlı yayınlandı, ComfyUI/Diffusers entegrasyonu hazır. NOT: Hiçbir kaynak rakip modellere karşı sayısal bir benchmark tablosu yayınlamadı (K1) — bu yüzden karşılaştırmalı puan rapora alınmadı. Lisans: ticari kullanım için "Qwen Research License" ile ayrı izin gerekiyor.

### 12. AI ajan güvenlik açıkları (sandbox kaçışları, framework RCE)
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-09-21 | Durum: Aktif
- Günlük (08-07/08-17 özet: Ajanlar izole ortamlardan kaçtı, CISA 12 framework'te kritik RCE tespit etti, IBM Langflow CVE-2026-9198 KEV'e eklendi; Cursor sandbox atlatma CVE-2026-50548/50549; Black Hat 2026'da kodlama ajanlarında RCE/kimlik hırsızlığı/prompt injection bulguları, Veracode: AI kodunun güvenlik geçme oranı %56):
  - 2026-08-24: kontrol edildi, yeni gelişme yok.
  - 2026-08-31 (⚪): DavidCarliez/trustmebro (304 yıldız) — sahte tool-output ile guardrail atlatma aracı gündeme geldi.
  - 2026-09-07 (🟢): "GitSpawn" araştırması (Manifold Security, 2 Eylül) Git'in `core.fsmonitor` ayarını istismar eden RCE zinciri buldu. 7 ajan etkilendi: goose ve Claude Code (kısmen, "ultrareview" yolunda ek açık) düzeltildi, Cursor/Codex düzeltildi; Hermes Agent, Qwen Code, Grok Build YAMANMAMIŞ.
  - 2026-09-14: kontrol edildi, doğrulanmış yeni gelişme bulunamadı (hedef sayfa 404 döndü — K2).
  - 2026-09-21 (🟡): Karışık/çelişkili sinyal. Hermes Agent'ın resmi GitHub deposunda GitSpawn açığını kapatan bir PR (#101483, GHSA-7x36-8jrh-v4pw / CVE-2026-71963) 2 Eylül tarihinde birleştirilmiş görünüyor — `noninteractive_git_env()` ile `core.fsmonitor`/`core.hooksPath` sinklerini etkisizleştiriyor. Ancak 16 Eylül tarihli ikincil bir kaynak (shattered.io) o tarihte hâlâ Hermes Agent'ı "yamasız, düzeltme bekliyor" olarak listeliyor — iki kaynak çelişiyor, kesin güncel durum doğrulanamadı (K1), izlenmeye devam edilecek. Aynı kaynağa göre 16 Eylül itibarıyla Qwen Code ve Grok Build hâlâ yamasız; Claude Code, Cursor, Codex, goose patched.

### 13. DeepSeek V4-Flash/V4.1-Flash/V4-Pro + DeepSeek Harness (dsh)
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-09-21 | Durum: Aktif
- Günlük (08-07/08-17 özet: V4-Flash-0731 MIT lisansıyla açık kaynak, 284B MoE, Terminal-Bench ~82.7; V4 Pro GA oldu — SWE-bench Verified %80,6, 1,6T toplam/49B aktif parametre; DeepSeek Harness (dsh) v0.1 yayınlandı):
  - 2026-08-24 (🟢): dsh resmi reposu 11 günde 189.256 yıldıza ulaştı.
  - 2026-08-31 (🟡): dsh 205.243 yıldız, 23.773 fork (%8,4 haftalık artış).
  - 2026-09-07 (⚪): dsh 214.358 yıldız, 25.247 fork (%4,4 haftalık artış).
  - 2026-09-14 (🟢): DeepSeek, V4.1-Flash modelini yayınladı (10 Eylül) — yerel çok-modlu yetenekler, model adı `deepseek-flash` oldu. dsh 222.968 yıldız, 26.482 fork (%4,0 haftalık artış).
  - 2026-09-21 (⚪): DeepSeek API resmi changelog'da 10-21 Eylül arasında yeni bir girdi yok — bu hafta yeni model/ürün gelişmesi yok. GitHub API ile doğrulandı: deepseek-ai/deepseek-harness — 231.547 yıldız, 27.765 fork (222.968'den, %3,9 haftalık artış — büyüme yavaş da olsa sürüyor).

### 17. Prime Agent (Prime Intellect)
- İlk görülme: 2026-08-08 | Son güncelleme: 2026-09-21 | Durum: Aktif
- Günlük (08-08/08-24 özet: ARC-AGI-3 %95,5, MIT lisanslı, "Continual Harness" mimarisi; yıldız 12.064→16.671→18.055→19.305):
  - 2026-09-07 (⚪): 20.074 yıldız, 2.196 fork (%4,0 haftalık artış).
  - 2026-09-14 (⚪): 20.710 yıldız, 2.265 fork (%3,2 haftalık artış).
  - 2026-09-21 (⚪): Bu hafta yeni bir ürün/model duyurusu bulunamadı. GitHub API ile doğrulandı: PrimeIntellect-ai/prime-agent — 21.113 yıldız, 2.311 fork (20.710'dan, %1,9 haftalık artış — büyüme yavaşlamaya devam ediyor).

### 20. AI ajan mimarisi/hafıza yaklaşımları (Karpathy, MCP spec, AKB, lemmalog, agent-memory, okf-agent-memory)
- İlk görülme: 2026-08-08 | Son güncelleme: 2026-09-21 | Durum: Aktif
- Günlük (08-08/08-31 özet: Karpathy graph-tabanlı hafıza dokümanı; dnotitia/akb 140→147→154→156 yıldız; JordyZomer/lemmalog gündeme geldi — 212 yıldız, Datalog-tabanlı ajan hafızası):
  - 2026-09-07 (🟡): akb 158 yıldız. lemmalog 288 yıldız (%35,8 artış). İki yeni giriş: tigerless-labs/agent-memory (405, 1 Eylül) ve okf-agent-memory/okf-agent-memory (388, 5 Eylül).
  - 2026-09-14 (🟢): Büyük büyüme sıçraması — tigerless-labs/agent-memory 1.353 yıldız (%234 artış); okf-memory/okf-agent-memory 629 yıldız (%62 artış); lemmalog 308 yıldız; akb 160 yıldız.
  - 2026-09-21 (🟡): Karışık sinyal. GitHub API ile doğrulandı: tigerless-labs/agent-memory — 961 yıldız, 61 fork (1.353'ten, %-29,0 — DÜŞÜŞ; hem geçen haftaki hem bu haftaki rakam API'den, sahte-yıldız temizliği ihtimali var, izleniyor). okf-memory/okf-agent-memory — 708 yıldız, 52 fork (629'dan, %12,6 artış). JordyZomer/lemmalog — 316 yıldız, 30 fork (308'den, %2,6 artış). dnotitia/akb — 160 yıldız, sabit.

### 22. Yerel/açık kaynak Cowork & Claude Code alternatifleri (Goose, Eigent, ZCode)
- İlk görülme: 2026-08-10 | Son güncelleme: 2026-09-21 | Durum: Aktif
- Günlük (08-10/08-31 özet: Block Goose ilk takip; eigent-ai/eigent 14.898→15.022→15.087→15.162 yıldız, büyüme hız kesiyor):
  - 2026-09-07 (⚪): eigent 15.205 yıldız, 1.815 fork (%0,3 artış — büyüme neredeyse durdu). Çapraz not: Goose, GitSpawn RCE açığını 1.44.0'da düzeltenler arasında (bkz. #12).
  - 2026-09-14 (⚪): eigent 15.269 yıldız, 1.823 fork (%0,4 artış).
  - 2026-09-21 (🟡): Çapraz not — Z.ai (Zhipu), kodlama ajanı ZCode'u açık kaynağa açtı (20 Eylül; bkz. #32, yeni ayrı konu) — bu kategoriye güçlü yeni bir rakip. eigent-ai/eigent GitHub API ile doğrulandı — 15.354 yıldız, 1.828 fork (15.269'dan, %0,6 artış — büyüme neredeyse tamamen durdu).

### 24. Yeni GitHub AI/agent repoları (haftalık tarama)
- İlk görülme: 2026-08-10 | Son güncelleme: 2026-09-21 | Durum: Aktif
- Günlük (08-10/08-31: önceki taramalar, bkz. geçmiş commit'ler):
  - 2026-09-07: 1-7 Eylül (stars:>100 filtresi): commerce-agents (2.275, bkz. #2), niubigeo (621), agent-memory (405), okf-agent-memory (388), awesome-grokbot (331), image-prompt-reverse (308), unigit-ecosystem (307), boardui (261), consulting-pptx-skill (249), qiaomu-book-reader (235), awesome-ai-agent-platforms (234), botmaker (223), bot-crossing (180), agent-fleet-manager (171), ApexAgents-SkyRL-Recipe (156).
  - 2026-09-14: 8-14 Eylül (stars:>100 filtresi): Edge0 (1.629, Apple Silicon MoE çıkarım motoru), text-humanizer/SpaceDudem (737), short-video-generator-AI (723), viserys-agent (630), reelbench-skills (577), ai-data-extractor (461), Awesome-Astra-Embodied-AI (334, bkz. #26), DeepSelect (333), deepseek-recipe (323), DeepJIT (303), Phyzical_org (282), routeVSCODE (238), birdview (218), YourDesk (202).
  - 2026-09-21 (🟢): 15-21 Eylül'de oluşturulanlar (stars:>100 llm/agent/ai filtresi, API doğrulu) — haftanın en dikkat çekici deseni: yeni repoların büyük bölümü TypeSafe AI'nin "Jev" System One modeli etrafında oluşan bir ekosistem (bkz. #31). zai-org/ZCode (3.701, Z.ai'nin yeni açık kaynak kodlama ajanı, bkz. #32), mcncarl/jianying-headless (2.126, Jianying video düzenleme agent skill'i), jarrodwatts/jev-trader (1.612, Jev tabanlı kripto trading ajanı), korcarc/text-humanizer (737, AI metin "insansılaştırma"/dedektör atlatma — SpaceDudem'in geçen hafta bahsedilen aynı isimli reposundan FARKLI bir depo), yibie/awesome-jev (706, Jev ekosistemi küratörlü listesi), v-modal/awesome-jev-tools (580), pallavi-shekhar/ai-engineering-interview-questions-company-wise (567), Continuum-AI-Corp/OrcaBonsai-27B-Uncensored (505, ağırlık değiştirmeden davranışsal ablasyonla sansürsüzleştirme), rmalde/minecraft-agent (332, Jev kontrollü Minecraft ajanı), fhshaik/typesafe-mario (306, Jev ile Super Mario oynayan ajan), kerpopule/hermes-jev-skills (303), cobanov/awesome-jev (280), sutro-sh/jev-align (248), huangbai-AI/post-production-skill (223), ruc-datalab/EvoOntology (220, bkz. Bölüm 4/Çalışma Yöntemleri), kitze/skillbox (218), wuyoscar/jev-skill (217), Oldcircle/geo-sleuth (213), coldteadotai/abide (196), NiazMorshed2007/jev-review (187).

### 25. AI imza/watermark temizleme araçları ve tartışma
- İlk görülme: 2026-08-17 | Son güncelleme: 2026-09-21 | Durum: Aktif
- Günlük (08-17 özet: guillaumemeyer/watermarks-remover 6 günde 12.177 yıldıza ulaştı):
  - 2026-08-24 (🟢): 17.557 yıldız (+%44). Rakip ShadowAqueduct/watermark-remover 1 günde 760 yıldıza ulaştı.
  - 2026-08-31 (🟡): guillaumemeyer 19.536 yıldız (+%11,3). ShadowAqueduct 836 yıldız, ivme kesildi.
  - 2026-09-07 (🟡): guillaumemeyer 21.055 yıldız, 2.425 fork (%7,8 artış). ShadowAqueduct artık GitHub API'de bulunamıyor (muhtemelen silindi).
  - 2026-09-14 (🟡): guillaumemeyer 21.934 yıldız, 2.527 fork (%4,2 artış).
  - 2026-09-21 (⚪): Bu hafta yeni bir gelişme yok, yalnızca büyüme. GitHub API ile doğrulandı: guillaumemeyer/watermarks-remover — 22.462 yıldız, 2.595 fork (21.934'ten, %2,4 haftalık artış — büyüme yavaşlıyor).

### 26. GPT-5.6 → GPT-6 Astra (OpenAI)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-09-07 | Durum: Aktif
- Günlük (07-27 özet: 2-9 Temmuz duyurusu — Sol (amiral gemisi), Terra, Luna):
  - 2026-08-24 (🟡): GPT-5.6 Sol/Luna için "effort slider" güncellemesi; halüsinasyon oranında ~%60 azalma iddiası.
  - 2026-08-31: kontrol edildi, gelişme yok.
  - 2026-09-07 (🟢): GPT-6 Astra yayınlandı (3-4 Eylül) — ARC-AGI-3 %99,9, FrontierMath Tier 4 %97,6, ExploitBench %100. API $10/$50 per MTok.
  - 2026-09-14: kontrol edildi, doğrudan yeni gelişme yok (GitHub'da "Awesome-Astra-Embodied-AI" listesi gündeme geldi, bkz. #24).
  - 2026-09-21: kontrol edildi, doğrudan yeni model/ürün gelişmesi yok. NOT: 7 Eylül tarihli (pencere dışı) bir CSO Online haberinde Sam Altman rollout'u "dağınık" (messy) olarak nitelendirmiş ve kurumsal erişimin gecikmesinden özür dilemişti — bu hafta bunun devamı niteliğinde yeni bir haber bulunamadı.

### 27. Vercel fx — minik açık kaynak kodlama ajanı
- İlk görülme: 2026-08-24 | Son güncelleme: 2026-09-21 | Durum: Aktif
- Günlük (08-24 özet: Vercel Labs, Zig ile yazılmış minimal kodlama ajanı "fx"i açık kaynak yaptı):
  - 2026-08-31 (🟡): 2.622 yıldız, 300 fork (+%15,5).
  - 2026-09-07 (🟡): 2.786 yıldız, 319 fork (%6,3 artış).
  - 2026-09-14 (🟡): 2.947 yıldız, 336 fork (%5,8 artış).
  - 2026-09-21 (🟡): Bu hafta yeni bir ürün gelişmesi yok, yalnızca büyüme. GitHub API ile doğrulandı: vercel-labs/fx — 3.088 yıldız, 352 fork (2.947'den, %4,8 haftalık artış).

### 28. Meta Muse ailesi (Muse Spark modeli, Muse Code, Muse kişisel ajan uygulaması, Model API)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-09-21 | Durum: Aktif
- Günlük özet (arşivlenmeden önce, 07-27/08-31): 1M token bağlam ve Meta'nın ilk ücretli model API'si ilk takip edildi (07-27); Muse Spark 1.2 tabanlı "Meta Muse Code" duyuruldu (08-08); 23 gün gelişme yok → arşivlendi (08-31).
- Günlük (yeniden gündeme geldikten sonra):
  - 2026-09-07 (🟢) — YENİDEN GÜNDEMDE: Muse Spark 1.3 yayınlandı (2 Eylül) — önceki sürüme göre ~%20 daha az araç çağrısı, ~%25 daha az token kullanımı (resmi Meta AI Research blogu). NOT (K1): İkincil kaynaklardaki spesifik benchmark puanları resmi blogla teyit edilemedi, rapora alınmadı.
  - 2026-09-14: kontrol edildi, gelişme yok.
  - 2026-09-21 (🟢): Muse Spark modelini temel alan tüketici odaklı "Muse" kişisel AI ajanı uygulaması duyuruldu (8 Eylül; resmi about.fb.com duyurusu + Bloomberg + TechCrunch + Axios ile doğrulandı). E-posta gönderme, seyahat rezervasyonu, form doldurma, kullanıcı adına pazarlık gibi görevleri uygulama kapalıyken bile sürdürebiliyor; Muse app, WhatsApp veya muse.ai üzerinden erişilebiliyor, Link by Stripe ile güvenli ödeme ve izole "Muse Secure VM" içinde çalışıyor. Fiyatlandırma "çoğu ihtiyaç için ücretsiz, daha fazlası için abonelik" olarak açıklandı, kesin tier bilgisi verilmedi. ABD'de iOS/Android/web'de kullanıma açıldı, AI gözlük desteği yakında geliyor. NOT: Bu duyuru 8 Eylül tarihli olup geçen haftanın (8-14 Eylül) tarama penceresindeydi ama atlanmış — bu hafta geriye dönük fark edildi (K3).

### 29. Mistral AI 3 milyar € Series D turu (Samsung liderliğinde) — Avrupa'nın "sovereign AI" hamlesi
- İlk görülme: 2026-09-14 | Son güncelleme: 2026-09-14 | Durum: Aktif
- Günlük:
  - 2026-09-14 (🟢): Mistral AI, Samsung liderliğinde 3 milyar € Series D turu kapattığını duyurdu (8 Eylül) — değerleme 21 milyar €'nun üzerine çıktı, Avrupa teknoloji tarihinin en büyük özkaynak turu.
  - 2026-09-21: kontrol edildi, gelişme yok (bu tura dair yeni bir gelişme bulunamadı).

### 30. Grok 4.6 → 4.7 (xAI)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-09-21 | Durum: Aktif
- Günlük özet (arşivlenmeden önce, 07-27/08-31): 1.5T MoE, Terminal-Bench 2.1 %83.3 ilk takip (07-27); Grok 4.6 resmen çıktı — $2/$6/$0.50 per MTok (08-17); Grok 5 için doğrulanmış tarih yok, 21 gün gelişme yok → arşivlendi (08-31).
- Günlük (yeniden gündeme geldikten sonra):
  - 2026-09-14 (🟢) — YENİDEN GÜNDEMDE: Microsoft, Copilot'a (Word/Excel/PowerPoint) Grok modellerini ekledi (12 Eylül). Grok 4.7 beşinci kez hedef tarihini kaçırdı — Musk resmi bir tarih vermedi (yalnızca X paylaşımları, docs.x.ai'de kayıt yok).
  - 2026-09-21 (🟡): Grok 4.7 hâlâ resmi olarak yayınlanmadı. Birkaç düşük güvenilirlikli ikincil kaynak (ör. startupfortune.com) Musk'ın Grok 4.7'yi "rafa kaldırıp" doğrudan Grok 4.8'e geçeceğini iddia ediyor, ancak bu iddia ne xAI'nin resmi kanallarında ne de birinci kademe haber kaynaklarında doğrulanabildi — K1 gereği kesin bir iddia olarak rapora ALINMADI, yalnızca "gecikme sürüyor" bilgisi kullanıldı.

### 31. TypeSafe AI — Jev / "System One Models"
- İlk görülme: 2026-09-21 | Son güncelleme: 2026-09-21 | Durum: Aktif
- Günlük:
  - 2026-09-21 (🟢) — İLK TAKİP: TypeSafe AI, ilk "System One Model"i Jev'i tanıttı (15 Eylül, erken erişim; resmi typesafe.ai blogu + MarkTechPost/DataCamp/LangChain/Vercel haberleriyle doğrulandı). Geleneksel LLM'lerin aksine, tipli/kalibre edilmiş kararları paralel ve milisaniyeler içinde üretiyor; otomasyon/karar-verme görevlerine odaklı (sohbet değil). Resmi kaynağa göre System One görevlerinde frontier LLM'lere kıyasla 40-200x daha hızlı (70ms-500ms'ye karşı 3-329 saniye) ve iş akışı değerlendirmelerinde 444,6x daha ucuz olduğu iddia ediliyor; tip hatası/halüsinasyon "matematiksel olarak garantili sıfır" deniyor. Fiyatlandırma: $0,042/MTok giriş, çıkış ücretsiz. Lisans/kaynak modeli belirsiz — kod tabanı açık kaynak değil gibi görünüyor (typesafeai/jev adında bir GitHub reposu bulunamadı), erken erişim programı üzerinden sunuluyor. Hafta içinde GitHub'da Jev etrafında organik olarak onlarca bağımsız araç/entegrasyon reposu ortaya çıktı (bkz. #24) — haftanın en büyük ekosistem hareketlenmesi.

### 32. Z.ai (Zhipu) — ZCode kodlama ajanı
- İlk görülme: 2026-09-21 | Son güncelleme: 2026-09-21 | Durum: Aktif
- Günlük:
  - 2026-09-21 (🟢) — İLK TAKİP: Z.ai (Zhipu AI), kodlama ajanı ZCode'un kod tabanını açık kaynağa açtı (20 Eylül; resmi zai-org/ZCode GitHub reposu — "feat: open source" commit'i + repo oluşturulma tarihi ile doğrulandı). ZCode, GLM ailesi modelleriyle çalışan, Cursor/Claude Code/GitHub Copilot'a rakip bir ajan geliştirme ortamı; resmi changelog'a göre en son sürüm 3.14.0 (19 Eylül) alt-ajanları tek script ile orkestre eden "dynamic workflows" özelliğini ekledi. GitHub API ile doğrulandı: zai-org/ZCode — 3.701 yıldız, 968 fork (<1 günde, repo 20 Eylül'de oluşturuldu). NOT: ZCode uygulamasının kendisi Temmuz 2026'dan beri mevcuttu (GLM-5.2 ile); bu haftaki gelişme spesifik olarak kod tabanının açık kaynağa açılması.

## Arşivlenmiş Konular

### AB Yapay Zeka Yasası (AI Act) uygulama takvimi
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-08-31 | Arşivlenme: 2026-09-21 (21+ gün gelişme yok)
- Günlük (arşivlenmeden önce): 08-07: Madde 50 şeffaflık kuralları 3 Ağustos'ta, yüksek riskli AI hükümleri 2 Ağustos'ta yürürlüğe girdi. 08-08 – 08-24: gelişme yok. 08-31 (🟡): Axios'un "AI Act gets real" değerlendirmesi şirket uyum tepkilerini detaylandırdı; AB AI Ofisi bilgi talep edebiliyor ama henüz ceza/uygulama eylemi yok. 09-07: kontrol edildi, gelişme yok (dolaşımdaki "AB AI Ofisi 3 şirkete 47M€ ceza kesti" iddiası doğrulanamadı, alınmadı — K1). 09-14: kontrol edildi, gelişme yok. 09-21: 21 gün gelişme yok → arşivlendi (bu hafta da yalnızca görüş makaleleri/eski haberler bulundu, somut bir icra/ceza gelişmesi yok).

### Anthropic Cowork
- İlk görülme: 2026-08-10 | Son güncelleme: 2026-08-31 | Arşivlenme: 2026-09-21 (21+ gün gelişme yok)
- Günlük (arşivlenmeden önce): 08-10: ilk takip. 08-17, 08-24: gelişme yok. 08-31 (🟢): chat/Cowork hafıza sistemleri birleştirildi (25 Ağustos). 09-07 – 09-21: kontrol edildi, gelişme yok (bu dönemin büyük Anthropic haberleri — Commerce Agents, Smart Reports, self-improvement duyurusu — #2 altında işlendi).

### Salesforce Slackbot'un AI ajanına dönüştürülmesi (Claudeforce)
- İlk görülme: 2026-08-10 | Son güncelleme: 2026-08-31 | Arşivlenme: 2026-09-21 (21+ gün gelişme yok)
- Günlük (arşivlenmeden önce): 08-10: ilk takip. 08-17, 08-24: gelişme yok. 08-31 (🟢): Salesforce-Anthropic "Claudeforce" ortaklığı duyuruldu (26 Ağustos). 09-07 – 09-21: kontrol edildi, gelişme yok (yalnızca 26 Ağustos duyurusunun yankıları/analizleri bulundu).

### ChatGPT for Work & GPT-Live (OpenAI ürünleri)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-07-27 | Arşivlenme: 2026-08-17 (21+ gün gelişme yok)
- Günlük: 07-27: ilk takip — Codex+ChatGPT birleşimi, site barındırma, tam-dupleks sesli asistan. 08-08 – 09-21: kontrol edildi, gelişme yok (arşivde kalıyor).

### OptMem — AI ajanları için hafıza aracı
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-07-27 | Arşivlenme: 2026-08-17 (21+ gün gelişme yok)
- Günlük: 07-27: ilk takip — VictorTaelin, 426 token'lık prompt + script ile minimalist kalıcı hafıza. 08-08 – 09-21: kontrol edildi, gelişme yok (arşivde kalıyor).

### Sakana AI — Fugu-Cyber
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-07-27 | Arşivlenme: 2026-08-17 (21+ gün gelişme yok)
- Günlük: 07-27: ilk takip — CyberGym %86.9, CTI-REALM %72.1. 08-08 – 09-14: kontrol edildi, gelişme yok. 09-21: kontrol edildi, gelişme yok (bu hafta yalnızca pencere dışı — 10 Eylül tarihli — bir Sumitomo ortaklığı haberi bulundu; arşivde kalıyor).

### Kimi K3 / K4 (Moonshot AI)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-08-08 | Arşivlenme: 2026-08-31 (21+ gün gelişme yok)
- Günlük: 07-27: ilk takip — 2.8T parametre, 1M bağlam. 08-08 (🟢): açık ağırlıklar 27 Temmuz'da yayınlandı. 08-10 – 08-24: gelişme yok. 08-31: 23 gün gelişme yok → arşivlendi. 09-07 – 09-21: kontrol edildi, gelişme yok (Kimi K4 hâlâ doğrulanmış bir sürüm tarihine sahip değil, tüm kaynaklar tahmin/spekülasyon niteliğinde).

### OpenAI Astra (matematik/araştırma modeli — GPT-6 Astra ile KARIŞTIRILMASIN)
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-08-10 | Arşivlenme: 2026-08-31 (21+ gün gelişme yok)
- Günlük: 08-07: ~2.000 dolarlık hesaplamayla 10 açık problem çözüldü. 08-08 (🟢): Fields madalyalı Jacob Tsimerman OpenAI'ye katıldı. 08-10 (🟢): kanıtlar tartışmalı bulundu. 08-17 – 08-24: gelişme yok. 08-31: 21 gün gelişme yok → arşivlendi. 09-07 – 09-21: kontrol edildi, gelişme yok (arşivde kalıyor; GPT-6 Astra adıyla aynı isim ama resmi kaynaklarda doğrudan bağlantı doğrulanamadı — karıştırılmasın).

### AI ajan ödeme altyapısı (agent payments)
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-08-07 | Arşivlenme: 2026-08-31 (21+ gün gelişme yok)
- Günlük: 08-07: Cloudflare "Wallets" ve MoonPay "PayBox" (x402 standardı) duyuruldu. 08-10 – 08-31: 24 gün gelişme yok → arşivlendi. 09-07 – 09-21: kontrol edildi, gelişme yok (arşivde kalıyor).

### Mistral Shieldstral
- İlk görülme: 2026-08-08 | Son güncelleme: 2026-08-08 | Arşivlenme: 2026-08-31 (21+ gün gelişme yok)
- Günlük: 08-08: ilk takip — 3B parametreli çok modlu güvenlik sınıflandırıcı. 08-10 – 08-31: 23 gün gelişme yok → arşivlendi. 09-07 – 09-21: kontrol edildi, Shieldstral ürününün kendisine dair gelişme yok (Mistral'ın 3 milyar € Series D turu ayrı bir konu, bkz. #29).

### Çok modlu üretici modeller (DiffusionGemma, MiniMax H3)
- İlk görülme: 2026-08-08 | Son güncelleme: 2026-08-08 | Arşivlenme: 2026-08-31 (21+ gün gelişme yok)
- Günlük: 08-08: DiffusionGemma ve MiniMax H3 ilk takip. 08-10 – 08-31: 23 gün gelişme yok → arşivlendi. 09-07 – 09-21: kontrol edildi, gelişme yok (arşivde kalıyor).

### Gemini 3.5/3.6/3.7 Flash liderlik değişikliği / Gemini 4 (Google DeepMind)
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-08-17 | Arşivlenme: 2026-09-07 (21+ gün gelişme yok)
- Günlük: 08-07: Hassabis Alphabet başkanlığına geçti, Kavukcuoglu Gemini 4'ün başına geçti; Jeff Dean vb. ayrılıp "Discovery Loop"u kurdu. 08-10: gelişme yok. 08-17 (🟡): Kavukcuoglu resmen "frontier AI" başına geçti. 08-24 – 08-31: gelişme yok. 09-07: 21 gün gelişme yok → arşivlendi (spekülatif "checkpoint sızdı" haberleri doğrulanamadı, alınmadı). 09-14 – 09-21: kontrol edildi, gelişme yok (arşivde kalıyor; Gemini modellerinin kendisi #3'te ayrı takip ediliyor).

## Değişiklik Geçmişi

(NOT: Dosya 25KB sınırını aştığı için bu hafta sıkıştırma uygulandı — her konu için son 5 günlük kayıt bırakıldı, daha eskisi özet cümlelere indirildi; git commit geçmişinde tam hâli korunuyor. 2026-07-22, 07-27, 08-07 ve 08-08 tarihli Değişiklik Geçmişi girdileri de bu sıkıştırmada özetlenip kaldırıldı.)

- 2026-08-10: 3 yeni konu, 9 konu güncellendi; GitHub konektörüyle repo bölümü gerçek API'den doğrulandı.
- 2026-08-10 (mimari değişiklik): Durum dosyası Google Drive'dan bu git deposuna taşındı.
- 2026-08-17: 1 yeni konu, 10 konu güncellendi, 4 konu arşivlendi (GPT-5.6, ChatGPT for Work & GPT-Live, OptMem, Sakana Fugu-Cyber). İlk arşivleme turu.
- 2026-08-24: 1 yeni konu (Vercel fx), 1 konu arşivden döndü (GPT-5.6), 11 konu güncellendi, 0 konu arşivlendi.
- 2026-08-31: 0 yeni konu, 12 konu güncellendi, 6 konu arşivlendi (Kimi K3, Meta Muse Spark/Code, OpenAI Astra, AI ajan ödeme altyapısı, Mistral Shieldstral, çok modlu üretici modeller). Öne çıkan: Anthropic-Salesforce "Claudeforce" ortaklığı; Cowork hafıza birleşmesi; Qwen3.8-27B basın ilgisi; DeepSeek Harness 205.243 yıldız.
- 2026-09-07: 0 yeni konu, 1 konu arşivden döndü (Meta Muse Spark 1.3, #28), 13 konu güncellendi, 2 konu arşivlendi (Grok 4.6, Google DeepMind liderlik/Gemini 4). Öne çıkan: OpenAI GPT-6 Astra'yı yayınladı (ARC-AGI-3 %99,9); Anthropic Claude Commerce Agents blueprint'ini açtı; Meta Muse Spark 1.3; GitSpawn RCE açığı 7 kodlama ajanını etkiledi.
- 2026-09-14: 1 yeni konu (Mistral 3 milyar € Series D, #29), 1 konu arşivden döndü (Grok 4.6→4.7, #30), 9 konu gerçek gelişmeyle güncellendi, 7 konu kontrol edildi/gelişme yok, 0 konu arşivlendi. Öne çıkan: Mistral 3 milyar € Series D (21 milyar € değerleme); Microsoft Copilot'a Grok eklendi; DeepSeek V4.1-Flash; ajan hafızası repolarında büyük büyüme sıçraması; Anthropic Smart Reports.
- 2026-09-21: 2 yeni konu (TypeSafe AI Jev/System One Models #31, Z.ai ZCode #32), 12 konu gerçek gelişmeyle güncellendi (#2, #6, #12, #13, #17, #20, #22, #24, #25, #27, #28, #30), 3 konu kontrol edildi/gelişme yok (#3, #26, #29), 3 konu arşivlendi (AB AI Act #15, Anthropic Cowork #21, Salesforce Claudeforce #23 — üçü de 21+ gün gelişme yok). Bu hafta ayrıca dosya 25KB sınırını aştığı için sıkıştırma uygulandı. Öne çıkan: Anthropic, Claude'un kendi AR-GE'sinin %26'sını yönettiğini duyurdu; TypeSafe AI'nin "Jev" System One Model'i haftanın en büyük GitHub ekosistem patlamasını yarattı (onlarca bağımsız repo); Z.ai kodlama ajanı ZCode'u açık kaynağa açtı; Meta'nın "Muse" kişisel AI ajanı duyurusu geriye dönük eklendi; ajan hafızası kategorisinde tigerless-labs/agent-memory yıldızında %-29 düşüş gözlendi (izleniyor); GitSpawn açığının Hermes Agent'taki yama durumu kaynaklar arası çelişkili.
