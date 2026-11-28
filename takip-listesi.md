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

### 2. Anthropic modelleri, ürünleri ve kurumsal gelişmeler (Claude 5.5; Fable/Mythos 5.2; Duet; Ship; IPO)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-28 | Son kontrol: 2026-11-28 | Durum: Aktif
- Özet (07-27/11-16): 5.5 ailesi Opus $4/$20, Sonnet $2/$10, Haiku $0,10/$0,50; Cowork; Duet (#33); Personal Finance; Fable/Mythos 5.2 (9 Kasım; $8/$40); Sheets/Whiteboards/Data (11 Kasım); homeopathic learning.
  - 2026-11-19 (🟢): Halka arz $83 (18 Kasım; anthropic.com) — 980M Class A +147M opsiyon; Nasdaq "ANT".
  - 2026-11-22 (🟡): ANT 19 Kasım açılış $111,50 (+%34; TechRepublic). Alpöge RH → #39.
  - 2026-11-25 (🟡): İkincil (K2: ZDNet, X): Claude Ship beta (`/ship`); Skills over MCP + Tasks; masaüstü artifact uygulamaları. ANT 24 Kasım'da düştü (Semafor; rakam K1).
  - 2026-11-28 (🟡): İkincil: Stainless satın alımı (>$300M; Economic Times, 26 Kasım) — Stainless OpenAI/Google SDK'larını da üretiyordu. API'nin Claude ile Rust'a taşınması (CPU −%70; The Neuron). WSJ: ANT hisse hareketi; tarihler kaynaklar arasında çelişkili, rakam yazılmadı (K1).

### 3. Gemini ailesi ve Google DeepMind (Gemini 4 Argon/Carbon/Hydrogen/Neon, Genie 4, Orchestrator, TPU 8, Gemini for Mac)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-22 | Son kontrol: 2026-11-28 | Durum: Aktif (09-28 arşivlendi, 10-05 geri döndü)
- Özet (07-27/11-16): Argon GA 13 Ekim; Genie 4; Omni 1.2 Flash; TPU 8tx/8i Max; Carbon (10 Kasım; $4/$20); Decisions API; AlphaGenome 2; Hydrogen (12 Kasım; AA 51).
  - 2026-11-19 (🟢): Gemini 4 Neon (18 Kasım) — $3/$15, 1M, AA Index 61, Terminal-Bench 4.1 %65,2.
  - 2026-11-22 (🟡): K3 (19 Kasım): Genie 4 Gemini API'de (720p, 24 fps, SynthID). İkincil: Gemini for Mac; Mirror Dimension; Suncatcher 2029.

### 6. Qwen serisi (Alibaba: 3.8, QwenWork, Qwen 4, Qwen4-Max)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-19 | Son kontrol: 2026-11-28 | Durum: Aktif (10-20 arşivlendi, 11-01 geri döndü)
- Özet (07-27/11-04): 3.8 ailesi, QwenWork; Qwen 4 duyurusu (22 Eyl); Apple–Alibaba (ikincil).
  - 2026-11-13 (🟢): Qwen4-Max-Preview (11 Kasım) — 1M bağlam; yalnızca Token Plan.
  - 2026-11-19 (🟢): K3 (16 Kasım): Qwen4-Max — 2,4T / 71B aktif, 1M; $1,5/$4,5; kapalı ağırlık.

### 12. AI ajan güvenlik açıkları ve savunma araçları
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-11-28 | Son kontrol: 2026-11-28 | Durum: Aktif
- Özet (08-07/11-13): CISA 12 framework RCE; Cursor CVE'leri; CVE-2026-82533 (dsh); Archon; OpenCode ihlali; sahte AGENTS.md npm; Claude Code sır sızıntısı (Apiiro); ARTEX kötüye kullanımı.
  - 2026-11-22 (🟡): K3 (19 Kasım; The Register): AB Komisyonu Sysper/MyPMO 10+ gün kapalı; ARTEX iddiası (Politico) resmi değil.
  - 2026-11-25 (🟢): K3 (20 Kasım; AWS): Cairn ajan çerçevesi MONAILabel'da sıfırıncı günü ~11 dk'da buldu (GHSA-qc22-rmgc-vg94). K3 (22 Kasım; OpenRouter): 3 sağlayıcı çıkarıldı, 125 uç nokta ZDR'den düştü. OpenAI + Cisco Shirudo (23 Kasım; eBPF kalkanları, BSD-2).
  - 2026-11-28 (🟡): İkincil (The Decoder ← The Neuron, 26 Kasım): Microsoft ARTEX'i belgeledi (devlet destekli saldırganlar, Temmuz'dan beri) — önceki "resmi değil" notu geçersiz. İsviçre ulusal siber ofisi: ajan kullanan 5 saldırı (Reuters).

### 13. DeepSeek V4-Pro / V4.1-Flash + Harness (dsh) + superagent
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-11-16 | Son kontrol: 2026-11-28 | Durum: Aktif
- Özet (08-07/11-10): V4-Pro GA; dsh; V4.1-Flash-1017 (MIT, 763B, 1M); Search/Fetch API; superagent prototipi (31 Ekim).
  - 2026-11-16 (⚪): K3 (13 Kasım): flash'ta web arama/dosya/URL; Search, OCR, ASR, TTS API'leri.
  - 2026-11-28 (yıldız, 28 Kasım): harness 288.134 (19 Kasım: 283.801); superagent yenilenmedi.

### 24. Yeni GitHub AI/agent repoları (her rapor çalışmasında tarama)
- İlk görülme: 2026-08-10 | Son güncelleme: 2026-11-28 | Son kontrol: 2026-11-28 | Durum: Aktif
- Özet (08-10/11-25): taramalar raporlarda. ⚠️ Tekrarlayan desenler: sahte "free model"/sürüm, korsan installer, hile, muse.ai kayıt araçları, sahte yıldız ağları. 20-25 Kasım: riemann-hypothesis, navier-stokes, skill-distill, shrink-anything (210), squid5090 (219), weaponized-curiosity (174), LoopedWSP (105); VIctory/GTA VI türevleri.
  - 2026-11-28 (🟡, 26-28 Kasım; 94 sonuç): yalnızca es-ine/mcp (203; İspanya INE MCP sunucusu) anlamlı. ⚠️ Sonuçların neredeyse tamamı sahte yıldız ağı: 195-244 yıldızlı Go "…-pro-patcher-installer / desktop-suite" repoları (Claude Code/Aider/Devin/Trae "Pro Trial Reset", Topaz, Wan, GPT4All); waifu2x-image-upscaler-windows (820, 0 fork).
  - Anomali (28 Kasım): skill-distill 1.012 (3 günde +%35,5; 25 Kasım: 747).

### 26. OpenAI GPT-6 ailesi ve ürünleri (Astra / Sol / Luna / Terra / Rosalind / Cyber / 6.2, Dots, Space, Wallet)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-28 | Son kontrol: 2026-11-28 | Durum: Aktif
- Özet (07-27/11-16): GPT-6 Astra ($10/$50), Sol ($2/$10), Luna; DevDay: Dots, 6.1 Sol, Space, Agents API; Terra; Rosalind; GPT-6 Cyber; Businesses; Wallet (#45); robotik ekibi dağıtıldı.
  - 2026-11-19 (🟢): GPT-6.2 Astra ($8/$40) ve Sol ($2/$10) (17 Kasım); Astra AI Self-Improvement "High", siber "Critical".
  - 2026-11-25 (🟡): GPT-6.2 Sol ChatGPT Chat'te (23 Kasım; MacRumors) — Plus/Pro/Business/Enterprise; politika uyumu %77–80 → %91–94. Shirudo → #12; protein, ω=9/4 → #39. İkincil: OpenWorks; Alfozan davası.
  - 2026-11-28 (🟡): Faturalama hatası düzeltildi (26 Kasım; The Neuron ← OpenAI'den Sottiaux): Astra limitlerine %40, Sol'a %25 daha hızlı ulaşılıyor, ek kullanım ücretlendirilmiyor; Aralık'ta ChatGPT+Codex ortak jeton kotası. OpenAI Apple'a karşı dava açtı (27 Kasım; ticari sır + tedarikçi baskısı; AI Weekly ← 9to5Mac); duruşma 19 Temmuz 2027. İkincil: ChatGPT alışveriş sanal denemesi.

### 28. Meta Muse ailesi (Spark, Code, ajan uygulaması, Wonder, Spark Open, Ember, Charm)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-25 | Son kontrol: 2026-11-28 | Durum: Aktif
- Özet (07-27/11-10): Muse Spark 1.3; ajan uygulaması (8 Eyl); Wonder ($4/$20); Spark Open (#35); Ember (9 Kasım; $0,10/$0,50).
  - 2026-11-22 (🟡): K3 (19 Kasım; TechCrunch ← Reuters): çalışan testlerinde konuşma karışması/gizli veri görünmesi.
  - 2026-11-25 (🟡): Muse Instagram DM'lerinde (24 Kasım; TechCrunch) — ABD, CA, MX, JP, SG. İkincil: Walmart Black Friday.

### 29. Mistral AI (Series D, Large 4, CERN Flare, Studio)
- İlk görülme: 2026-09-14 | Son güncelleme: 2026-11-28 | Son kontrol: 2026-11-28 | Durum: Aktif (10-05 arşivlendi, 10-12 geri döndü)
- Özet (09-14/10-29): 3 milyar € Series D; Large 4 preview (6 Ekim); CERN "Flare".
  - 2026-11-01 (🟢): K3 (29 Ekim): Large 4 açık ağırlık — 1T/52B aktif; $0,70/$2,10.
  - 2026-11-07 (🟡): Mistral Studio genişletmesi (5 Kasım).
  - 2026-11-28 (⚪): K3 (24 Kasım; ikincil, Distill): Singapur bölge merkezi.

### 30. Grok (xAI) — 4.8; deepfake davaları
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-25 | Son kontrol: 2026-11-28 | Durum: Aktif (10-20 arşivlendi, 11-16 geri döndü)
  - 2026-11-16 (⚪): İkincil: Grok 4.8 "soft rollout" (13 Kasım); model kartı/API yok.
  - 2026-11-25 (🟡): İkincil (CNBC açılmadı, K2; 23 Kasım): Oregon ve Virginia, Grok'un rıza dışı cinsel görselleri nedeniyle SpaceX ve bağlı şirketlere dava açtı.

### 32. Z.ai (Zhipu) ZCode ve GLM modelleri
- İlk görülme: 2026-09-21 | Son güncelleme: 2026-11-28 | Son kontrol: 2026-11-28 | Durum: Aktif (11-04 arşivlendi, 11-25 geri döndü)
- Özet (09-21/10-12): ZCode, GLM dikey modelleri. Yıldız (4 Kasım): 8.461.
  - 2026-11-25 (🟡): GLM-5.4 (23 Kasım; TechNode) — ilk "Loop Transformer", görsel, 1M; Coding Plan. Parametre/lisans yok.
  - 2026-11-28 (⚪): İkincil (Reuters 26 Kasım ← The Neuron/Distill): bir sonraki amiral gemisi (Distill: GLM-5.5) takvimin gerisinde; ABD çip kısıtları ve damıtma kısıtları nedeniyle Q1 2027 veya sonrasına kayabilir.

### 33. Always-on kişisel/iş ajanları (Dots, Muse, Space, Duet, Teammates, Genie, Apple)
- İlk görülme: 2026-10-05 | Son güncelleme: 2026-11-28 | Son kontrol: 2026-11-28 | Durum: Aktif
- Özet (10-05/11-07): OpenAI Dots (29 Eylül); Claude Duet (21 Ekim); Perplexity Teammates.
  - 2026-11-13 (🟡): İkincil: ByteDance ajanı; Databricks Genie always-on; n8n Nod.
  - 2026-11-22 (⚪): İkincil (K3): Apple bilgisayar kontrol eden ajan (Bloomberg); Gemini for Mac.
  - 2026-11-28 (⚪): K3 (25 Kasım; ikincil): Claude Duet Hindistan, Endonezya, Brezilya, Japonya'da.

### 34. Frontier güvenlik olayları ve düzenleyici yanıt
- İlk görülme: 2026-09-28 | Son güncelleme: 2026-11-28 | Son kontrol: 2026-11-28 | Durum: Aktif
- Özet (09-28/11-19): OpenAI eğitim duraklaması; SI Force, FTC; METR AECI; NY RAISE (1 Ocak 2027); AB 2026/2487 sandbox; Oregon AG – OpenAI; STK tedbir davası.
  - 2026-11-22 (⚪): İkincil: dört senatörden AI açıklama tasarısı.
  - 2026-11-25 (⚪): İkincil (K2): Axios — OpenAI/Anthropic çalışanlarında yayın güvenliği endişesi; İngiltere FCA otonom AI beklentileri; OpenAI Pachocki ortak sınır önerisi (22 Kasım).
  - 2026-11-28 (⚪): Guardian (26 Kasım): İngiltere ve Galler'de ≥25 mahkeme davasında bildirilmeyen AI kullanımı. İkincil: NYT — iki partiden milletvekilleri AI düzenlemesine ilgili; Kanada AI Compute Access Fund C$1 milyar.

### 35. ABD açık/lisanslı ağırlık yarışı (Muse Spark Open, Beam, MAI-Base-2, Inkling 2)
- İlk görülme: 2026-10-17 | Son güncelleme: 2026-11-25 | Son kontrol: 2026-11-28 | Durum: Aktif
- Özet (10-17/11-07): Reflection Beam (501B/23B, Apache 2.0), MAI-Base-2, Muse Spark Open; Inkling 2 Small (594B/17B).
  - 2026-11-16 (🟡): K3: `thinkingmachines/Inkling-2-Small` HF'de; AA Index 31.
  - 2026-11-25 (🟢): K3 (20 Kasım; thinkingmachines.ai): Inkling 2 Mini — döngülü MoE, 26,4B / 3,4B aktif (etkin 5,4B), 1M, Apache 2.0, ~20 GB; DeepSWE %48,2 (firma).

### 37. AI destekli zafiyet keşfi (PHP2Shell, Node2Shell, GPT-6 Cyber, Mythos 5.2)
- İlk görülme: 2026-10-23 | Son güncelleme: 2026-11-19 | Son kontrol: 2026-11-28 | Durum: Aktif
- Özet (10-23/11-07): PHP2Shell CVE'leri; php2shell-checker; Node2Shell (CVSS 9,2); GPT-6 Cyber.
  - 2026-11-10 (🟡): Mythos 5.2 — CVE Rediscovery %89,6.
  - 2026-11-19 (🟡): GPT-6.2 siber "Critical". İkincil: Calif AI Java açığı; Reflection Laser.
  - 2026-11-22 (yıldız, 22 Kasım): php2shell-checker 1.477.

### 38. Kimi (Moonshot) — K3.1 Pro
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-28 | Son kontrol: 2026-11-28 | Durum: Aktif (08-31 arşivlendi, 10-26 geri döndü)
- Özet (07-27/11-07): K3.1 Pro (23 Ekim); ağırlıklar 2,8T / 104B aktif, özel lisans.
  - 2026-11-19 (⚪): İkincil: biyoloji/kimya/ilaç araştırmasına yöneliyor.
  - 2026-11-22 (⚪): İkincil: Endonezya $150M Nvidia anlaşması iptal.
  - 2026-11-28 (⚪): İkincil (Reuters ← The Neuron, 26 Kasım): Moonshot, çip erişimi kaybederse büyük sürümler arası sürenin 6 aydan 1 yıla çıkabileceğini bekliyor. Together AI: Kimi-K3.1-Pro'dan ~1.000 çeviriyle Qwen3.8-27B'nin Lao/Tayca karışıklığı giderildi.

### 39. AI ile matematik/bilim keşif ve biçimsel doğrulama (RH, Navier–Stokes, ω=9/4, CFSG, FLT, kuantum, protein)
- İlk görülme: 2026-10-29 | Son güncelleme: 2026-11-28 | Son kontrol: 2026-11-28 | Durum: Aktif
- Özet (10-29/11-22): OpenAI ETH, Yang–Mills (Lean); Axiom CFSG; Fable 5.2 FLT (Anthropic iddiası); AlphaProof Code; /teamwork-LEAP Weil sanıları; Alpöge (Anthropic) + Claude RH + Dirichlet GRH, 175.187 dosyalık Lean arşivi (20 Kasım); Navier–Stokes patlama + Lean (aralık aritmetiği sertifikası bekleniyor).
  - 2026-11-25 (🟢): K3 (21 Kasım): Lean FRO + Mathlib Initiative RH'nin "ifadesi ve ispatı doğru" dedi (comparator/con-leche, çoklu çekirdek denetimi). Eleştiri: Association for Human Mathematics. OpenAI ön baskısı (24 Kasım): ω = 9/4 — bağımsız doğrulama yok. DeepMind (23 Kasım): Gemini 4 ajanları + Lean, füzyon devresi 11,8 kat ucuz. OpenAI (24 Kasım): GPT-6.2 mini-bağlayıcılar 35/322 (%10,9). Yıldız anomalisi (25 Kasım): riemann-hypothesis 1.090, navier-stokes 430; CFSG 178.
  - 2026-11-28 (🟡): ω=9/4 makalesi 111 sayfa; Lean dosyaları yalnızca bölmesiz durum; adı geçen uzman incelemesi yok (25 Kasım; dev.to ← The Neuron). İkincil: Google Research Cogentic (Gemini 4) 6 matematik makalesi (25 Kasım). Yıldız anomalisi (28 Kasım): riemann-hypothesis 1.529 (3 günde +%40,3), navier-stokes 455 (+%5,8), CFSG 178 (0).

### 42. AI veri merkezi, enerji ve piyasa etkisi (Nvidia liderlik krizi dahil)
- İlk görülme: 2026-11-07 | Son güncelleme: 2026-11-28 | Son kontrol: 2026-11-28 | Durum: Aktif
- Özet (11-07/11-22): yerel veri merkezi kısıtları; OpenAI Community Compact; EIA rekor talep; Huang ayrıldı (15 Kasım); Nvidia Q3 FY27 gelir $115,8 milyar; Nvidia–Inception görüşmesi.
  - 2026-11-25 (🟢): Huang CEO olarak geri döndü (23 Kasım; nvidianews); Kress CFO; ulusal güvenlik/ihracat komitesi. İkincil: Megaspeed entity list; Amazon–Decart ~$7,5 milyar; SpaceX hesaplama satıyor (NYT).
  - 2026-11-28 (🟢): İkincil (Bloomberg 27 Kasım ← The Neuron/Kelly Abbott): Blackwell çipleri Şanghay'da Alice Huang bağlantılı sahada bulundu; Huang 1 Aralık'ta üç Meclis komitesine (kapalı), 3 Aralık'ta Senato Bankacılık dinlemesine çıkacak. The Decoder: Nvidia, SEA (MY, SG, TH, ID) sunucu sevkiyatlarını durdurdu. Moody's görünümü pozitiften durağana (Semafor). SemiAnalysis: OpenAI Jalapeño çipi watt başına ~1,5–1,9× Blackwell (ikincil, dipnotlu).

### 43. Ajanlarla tersine mühendislik (REA ekosistemi)
- İlk görülme: 2026-11-13 | Son güncelleme: 2026-11-13 | Son kontrol: 2026-11-28 | Durum: Aktif
  - 2026-11-13 (🟡) — İLK TAKİP: Claude/Codex IoT tersine mühendislik blokları (ikincil). rea 455.826 (bülten "342.000", K1).
  - 2026-11-28 (yıldız, 28 Kasım): rea 481.356 (22 Kasım: 473.043); leanrea 4.516 (4.419); REA-Prompts 4.458 (4.331).

### 44. MiniMax H3 ailesi
- İlk görülme: 2026-08-31 öncesi | Son güncelleme: 2026-11-28 | Son kontrol: 2026-11-28 | Durum: Aktif (08-31 arşivlendi, 11-13 geri döndü)
  - 2026-11-13 (🟡): MiniMax H3-Image (11 Kasım) — açık ağırlık; lisans adı yok.
  - 2026-11-28 (🟡): İkincil (26 Kasım): Apple, MiniMax'in Talkie sohbet botunu dünya genelinde kaldırdı (Seeking Alpha ← Distill); Dragos/HD Moore çalışmasında AI isteklerindeki özel bağlantıların yetkisizce açılması (Reuters ← The Neuron).

### 45. Ajan ödemeleri ve kişisel finans (ChatGPT Wallet, Gemini/AI Mode + Google Wallet, Claude Personal Finance)
- İlk görülme: 2026-11-16 | Son güncelleme: 2026-11-25 | Son kontrol: 2026-11-28 | Durum: Aktif
  - 2026-11-16 (🟡) — İLK TAKİP: K3: Gemini + Google Wallet (salt-okunur, Plaid). İkincil: ChatGPT Wallet.
  - 2026-11-25 (⚪): İkincil (TechCrunch, 23 Kasım): Google AI Mode'a Drive ve salt-okunur Wallet bağlantısı.

### 46. Tencent Hunyuan Hy4 ailesi
- İlk görülme: 2026-11-22 | Son güncelleme: 2026-11-28 | Son kontrol: 2026-11-28 | Durum: Aktif
  - 2026-11-22 (🟡) — İLK TAKİP: K3 (18 Kasım): Hy4 Flash — ~224B / ~12B aktif, 1M, metin+görsel; "Tencent Hy License".
  - 2026-11-28 (🟡): İkincil (X ← The Neuron): DFly2 açık kaynak hızlandırıcı — firma iddiası: Hy4 Flash ajan görevlerinde 4,2×, DeepSeek-V4.1-Flash'ta (64K) %81'e kadar.

## Arşivlenmiş Konular

(Geri dönüş olmadıkça satır eklenmez. Tam geçmiş git commit'lerinde.)

- **AI imza/watermark temizleme araçları ve filigran tartışması [#25]** — İlk 08-17 | Son güncelleme 11-04 | Arşiv 11-25. Anthropic metin filigranı (3 Kasım). Son yıldız (28 Kasım): watermarks-remover 29.002.
- **Meituan LongCat model ailesi [#41]** — İlk 11-04 | Son güncelleme 11-04 | Arşiv 11-25. LongCat-2.5 Preview (2 Kasım) — 1,6T / ~48B aktif; açık ağırlık yok.
- **AI eğitim tercihi sinyali / yayıncı opt-out standardı [#40]** — İlk 11-01 | Son güncelleme 11-01 | Arşiv 11-22. OpenAI, Google, Microsoft, Anthropic ortak sinyal (30 Ekim); IETF `draft-kelley-aipref-training-preference-signal`; Microsoft'ta 1 Şubat 2027.
- **TypeSafe AI — Jev / "System One Models" [#31]** — İlk 09-21 | Son güncelleme 10-26 | Arşiv 11-16. Jev 1.14.0 (14 Ekim); 24 Ekim veri sızıntısı.
- **Vercel fx / libfx / fx0 [#27]** — İlk 08-24 | Son güncelleme 10-20 | Arşiv 11-10. Son yıldızlar (10 Kasım): fx 3.801, fx0 431.
- **AB AI Act uygulama takvimi ve standartları [#36]** — İlk 08-07 | Son güncelleme 10-20 | Arşiv 11-10. EN 18286:2026 (19 Ekim).
- **Prime Agent (Prime Intellect) [#17]** — İlk 08-08 | Son güncelleme 10-12 | Arşiv 11-04. Son yıldız (4 Kasım): 22.557.
- **AI ajan mimarisi/hafıza yaklaşımları [#20]** — Son güncelleme 10-12 | Arşiv 11-04. Yıldız (4 Kasım): agent-memory 4.303.
- **Yerel/açık kaynak Cowork alternatifleri [#22]** — Son güncelleme 10-05 | Arşiv 10-26. Yıldız (26 Ekim): eigent 15.662, OpenDots 6.013.
- **Eski arşiv (tek satır):** Anthropic Cowork (09-21; #2), Salesforce Slackbot/Claudeforce (09-21), ChatGPT for Work & GPT-Live (08-17), OptMem (08-17), Sakana Fugu-Cyber (08-17), x402 (08-31), Mistral Shieldstral (08-31), DiffusionGemma (08-31; MiniMax H3 kısmı #44), Gemini liderlik değişikliği (09-07).
- **OpenAI Astra (matematik modeli — GPT-6 Astra ile KARIŞTIRILMASIN)** — İlk 08-07 | Son 08-10 | Arşiv 08-31. Yeni matematik iddiaları #39'da.

## Değişiklik Geçmişi

- 2026-08-10 – 2026-11-07: bkz. git geçmişi (08-10 repoya taşındı; 10-16 3 günlük ritim, kapı, "Son kontrol"/yıldız/BEKLEYEN NOT kuralları, `gorev-talimati.md`).
- 2026-11-10 (pencere 8-10 Kasım): 0 yeni konu; 9 güncelleme; 2 arşiv (#27, #36). Sıkıştırma ~26,9 → ~24,5 KB.
- 2026-11-13 (pencere 11-13 Kasım): +1 konu (#43); #44 arşivden döndü; 12 güncelleme; 0 arşiv. Sıkıştırma ~25,3 → ~24,7 KB.
- 2026-11-16 (pencere 14-16 Kasım): +1 konu (#45); #30 arşivden döndü; 11 güncelleme; 1 arşiv (#31). Sıkıştırma.
- 2026-11-19 (pencere 17-19 Kasım): 0 yeni konu; 9 güncelleme; 0 arşiv. Yıldız satırları: #13, #25. Sıkıştırma ~27,6 → ~24,3 KB.
- 2026-11-22 (pencere 20-22 Kasım, hafta sonu): +1 konu (#46 Tencent Hy4); 11 güncelleme; 1 arşiv (#40). Ana olay: Alpöge + Claude RH Lean iddiası (#39). Yıldız satırları: #37, #43. K2: WebFetch yok (alt ajan). Sıkıştırma.
- 2026-11-25 (pencere 23-25 Kasım): 0 yeni konu; #32 arşivden döndü; 12 güncelleme; 2 arşiv (#25, #41). Ana olay: Lean FRO + Mathlib RH ispatını onayladı (K3); OpenAI ω=9/4 ön baskısı. Yıldız anomalileri: #39, #24. K2: WebFetch yok (alt ajan). Sıkıştırma ~28,1 → ~21 KB.
- 2026-11-28 (pencere 26-28 Kasım, Şükran Günü hafta sonu): 0 yeni konu; 13 güncelleme (#2, #12, #24, #26, #29, #32, #33, #34, #38, #39, #42, #44, #46); 0 arşiv (#29 24 Kasım gelişmesiyle arşivden kurtuldu). Ana olay: OpenAI–Apple karşı davası (27 Kasım); Nvidia ihracat baskısı (Blackwell Çin'de, Huang dinlemeleri 1/3 Aralık). Yıldız: #13, #43 satırları; anomaliler #39 (riemann-hypothesis), #24 (skill-distill). K2: WebFetch yok (alt ajan), birincil kaynaklar açılmadı; ANT hisse tarihleri çelişkili (K1). BEKLEYEN NOT yoktu. Sıkıştırma gerekmedi (~24 KB).
