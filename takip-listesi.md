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
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-22 | Son kontrol: 2026-11-22 | Durum: Aktif
- Özet (07-27/11-13): 5.5 ailesi Opus $4/$20, Sonnet $2/$10, Haiku $0,10/$0,50; Cowork; Duet (#33); Personal Finance beta; Fable 5.2 + Mythos 5.2 (9 Kasım; $8/$40). IPO roadshow (10 Kasım); Sheets/Whiteboards/Data, MAMUBench (11 Kasım).
  - 2026-11-16 (🟡): İkincil: talep ~6 kat (Bloomberg). K3 (10 Kasım): homeopathic learning — seyreltilmiş zehirli veri arka kapı oluşturabiliyor.
  - 2026-11-19 (🟢): Halka arz $83'tan fiyatlandı (18 Kasım; anthropic.com) — 980.000.000 Class A, +147.000.000 opsiyon; Nasdaq "ANT".
  - 2026-11-22 (🟡): ANT 19 Kasım'da $111,50'dan açıldı (+%34; TechRepublic). İkincil (Semafor): $26 milyar özel finansmanla toplam $107,3 milyar. Teknik kadrodan Levent Alpöge'nin Claude destekli RH iddiası → #39; şirket açıklaması bulunamadı.

### 3. Gemini ailesi ve Google DeepMind (Gemini 4 Argon/Carbon/Hydrogen/Neon, Genie 4, Orchestrator, Decisions API, Wallet, TPU 8, AlphaGenome 2, Gemini for Mac)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-22 | Son kontrol: 2026-11-22 | Durum: Aktif (09-28 arşivlendi, 10-05 geri döndü)
- Özet (07-27/11-13): Argon GA 13 Ekim; Genie 4 duyurusu; Omni 1.2 Flash GA; TPU 8tx/8i Max; Gemini 4 Carbon (10 Kasım; $2/$10 → $4/$20); Decisions API; AlphaGenome 2.
  - 2026-11-16 (🟢): K3 (12 Kasım): Gemini 4 Hydrogen — AA Index 51, Terminal-Bench 4.1 %57. Orchestrator: %24 daha az kota. Wallet → #45; /teamwork → #39.
  - 2026-11-19 (🟢): Gemini 4 Neon (18 Kasım) — $3/$15, 1M bağlam, AA Index 61 (xhigh), Terminal-Bench 4.1 %65,2. Genie 4 AI Ultra'ya açıldı.
  - 2026-11-22 (🟡): K3 (19 Kasım; blog.google): Genie 4 Gemini API'de — 720p, 24 fps, senkron ses, SynthID. İkincil: Gemini for Mac (ajan, ABD); Chrome ajanları için "Mirror Dimension" (Wired); Project Suncatcher — Blue Origin, 2029 Q1.

### 6. Qwen serisi (Alibaba: 3.8 ailesi, QwenWork, Qwen 4, Qwen4-Max; Apple Intelligence Çin)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-19 | Son kontrol: 2026-11-22 | Durum: Aktif (10-20 arşivlendi, 11-01 geri döndü)
- Özet (07-27/11-04): 3.8 ailesi, QwenWork; Qwen 4 duyurusu (22 Eyl); Apple–Alibaba (ikincil).
  - 2026-11-13 (🟢): Qwen4-Max-Preview (11 Kasım) — 1M bağlam, 393.216 maks. çıktı; yalnızca Token Plan.
  - 2026-11-19 (🟢): K3 (16 Kasım; Alibaba basın): Qwen4-Max — 2,4T / 71B aktif, yerleşik görsel, 1M bağlam; $1,5/$4,5. Kapalı ağırlık; küçük Qwen4'ler "yakında" açık.

### 12. AI ajan güvenlik açıkları (sandbox kaçışları, framework RCE, sızıntılar, tedarik zinciri, otonom saldırılar) ve savunma araçları
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-11-22 | Son kontrol: 2026-11-22 | Durum: Aktif
- Özet (08-07/11-04): CISA 12 framework RCE; Cursor CVE'leri; CVE-2026-82533 (dsh); Archon CVE-2026-111322; OpenCode ihlali; sahte AGENTS.md npm; kurcalanmış Claude Code eklentisi; Postman hook.
  - 2026-11-10 (🟢): K3 (7 Kasım; Apiiro): Claude Code "don't ask again" sırları `.claude/settings.local.json`'a yazıyor; 1.122 açık repoda sır.
  - 2026-11-13 (🟡): İkincil (K1): Microsoft "Lazarus" arka kapı; ARTEX fork'u ile AWS kimlik bilgisi hırsızlığı; IoT tersine mühendislik blokları → #43.
  - 2026-11-22 (🟡): K3 (19 Kasım; The Register): AB Komisyonu'nda Sysper ve MyPMO 10+ gün kapalı; Politico kaynaklarına göre ARTEX (AI sızma testi aracı) kullanıldı — Komisyon yalnızca "siber kampanya"yı doğruladı. CERT-EU 5 Kasım'da ARTEX uyarısı; FBI 1.600+ açık ARTEX konsolu (raporlanmış).

### 13. DeepSeek V4-Pro / V4.1-Flash + DeepSeek Harness (dsh) + superagent prototipi + uygulama API'leri
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-11-16 | Son kontrol: 2026-11-22 | Durum: Aktif
- Özet (08-07/11-01): V4-Pro GA; dsh; V4.1-Flash-1017 açık ağırlık (MIT, 763B, 1M); Search/Fetch API; dsh-superagent-prototype (31 Ekim, MIT).
  - 2026-11-10 (yıldız, 10 Kasım): harness 277.594; superagent 21.878 (6 günde +%25,4 — anomali eşiği).
  - 2026-11-16 (⚪): K3 (13 Kasım): deepseek-flash'ta web arama, dosya, URL okuma; bağımsız Search, OCR, ASR, TTS API'leri. Yeni ağırlık yok.
  - 2026-11-19 (yıldız, 19 Kasım): harness 283.801 (9 günde +%2,2); superagent 23.869 (9 günde +%9,1).

### 24. Yeni GitHub AI/agent repoları (her rapor çalışmasında tarama)
- İlk görülme: 2026-08-10 | Son güncelleme: 2026-11-22 | Son kontrol: 2026-11-22 | Durum: Aktif
- Özet (08-10/11-13): taramalar raporlarda. Öne çıkanlar: anatomy, huashu-motion, dsh-superagent, pixelfx, teardown, agent-autoloop, vork, hermes-voice, image-to-sculpt, apex-compute/ANR. ⚠️ Tekrarlayan desenler: sahte "free model"/sürüm, korsan installer, jailbreak/hile, muse.ai kayıt araçları, sahte yıldız ağları.
  - 2026-11-16 (🟡, 14-16 Kasım): PeakCut (472), tiny-voca (425). ⚠️ muse-protocol (1.167), "Gemini-Config-Checker-" sahte yıldız ağı.
  - 2026-11-19 (🟡, 17-19 Kasım): replit/datacat (219), holospot (168), java4shell-poc (157). ⚠️ muse-JP-Reg (253), cloud-exit-node-deploy (304).
  - 2026-11-22 (🟡, 20-22 Kasım; 744 sonuç, çoğu spam): leanprover-community/riemann-hypothesis (450), navier-stokes (332), skill-distill (397), sprite-stacking (393). ⚠️ google-one-tools (1.131; Frida ile Google One faturalandırma), Leonida/GTA 6 "PC" repoları, 20+ "portable x64" hile reposu (331–351 ⭐, aynı şablon — sahte yıldız ağı).

### 25. AI imza/watermark temizleme araçları ve filigran tartışması
- İlk görülme: 2026-08-17 | Son güncelleme: 2026-11-04 | Son kontrol: 2026-11-22 | Durum: Aktif
- Özet (08-17/11-01): guillaumemeyer/watermarks-remover 12.177 → 25.799 (1 Kasım); rakip ShadowAqueduct silindi.
  - 2026-11-04 (🟡): Anthropic sürüm notu (3 Kasım): Mythos 5, Opus 4.7, Sonnet 4.6 metinleri Anthropic metin filigranı taşıyor.
  - 2026-11-10 (yıldız, 10 Kasım): 26.908 (9 günde +%4,3).
  - 2026-11-19 (yıldız, 19 Kasım): 27.794 (9 günde +%3,3).

### 26. OpenAI GPT-6 ailesi ve ürünleri (Astra / Sol / Luna / 6.1 Sol / Terra / Rosalind / Cyber / 6.2 Astra-Sol, Dots, Space, Businesses, Wallet)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-19 | Son kontrol: 2026-11-22 | Durum: Aktif
- Özet (07-27/11-07): GPT-6 Astra ($10/$50), Sol ($2/$10), Luna ($0,10/$0,50); DevDay: Dots, 6.1 Sol, Space, Agents API; 6.1 Terra ($1/$5); Rosalind; GPT-6 Cyber (5 Kasım, siber "Critical").
  - 2026-11-13 (🟡): İkincil: Businesses in ChatGPT beta; Advanced/Standard Voice 11 Aralık'ta emekli; Odessia satın alındı.
  - 2026-11-16 (🟡): İkincil: ChatGPT Wallet (13 Kasım) → #45. Bağımsız robotik ekibi dağıtıldı (Fortune).
  - 2026-11-19 (🟢): GPT-6.2 Astra ($8/$40) ve Sol ($2/$10) (17 Kasım): Astra AI Self-Improvement'ta High eşiğine ulaşan ilk dışa sunulan model; ikisi de siber "Critical", bio/kimya "High". İkincil: ChatGPT for Sales; Oregon AG davası.

### 28. Meta Muse ailesi (Muse Spark, Muse Code, Muse ajan uygulaması, Muse Wonder, Muse Spark Open, Muse Ember, Muse Charm)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-22 | Son kontrol: 2026-11-22 | Durum: Aktif
- Özet (07-27/10-29): Muse Spark 1.3; Muse ajan uygulaması (8 Eyl); Muse Wonder (API $4/$20); Muse Spark Open (#35).
  - 2026-11-07 (⚪): ifadeli avatarlar; site kazıma şart güncellemesi askıya alındı (ikincil).
  - 2026-11-10 (🟡): Muse Ember (9 Kasım) — $0,10/$0,50; 1M bağlam, 512K çıktı.
  - 2026-11-22 (🟡): K3 (19 Kasım; TechCrunch ← Reuters): çalışan testlerinde Muse konuşmaları karıştırıyor, başkasına ait banka bakiyesi/çocuk bakımı mesajları görünüyor; Meta: "çalışanlar farklı sürümleri test ediyor". Muse 10M+ indirme. İkincil: "Muse Charm" $300 olabilir (Gizmodo).

### 29. Mistral AI (Series D, Mistral Large 4, CERN Flare, Studio)
- İlk görülme: 2026-09-14 | Son güncelleme: 2026-11-07 | Son kontrol: 2026-11-22 | Durum: Aktif (10-05 arşivlendi, 10-12 geri döndü)
- Özet (09-14/10-29): 3 milyar € Series D; Large 4 public preview (6 Ekim); CERN "Flare".
  - 2026-11-01 (🟢): K3 (29 Ekim): Large 4 açık ağırlık — 1T/52B aktif; API $0,70/$2,10.
  - 2026-11-07 (🟡): Mistral Studio genişletmesi (5 Kasım) — managed agents, iş akışları, değerlendirme.

### 30. Grok (xAI) — 4.7 → 4.8 (arşivden döndü)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-16 | Son kontrol: 2026-11-22 | Durum: Aktif (10-20 arşivlendi, 11-16 geri döndü)
- Özet (07-27/09-28): Grok 4.6 → Grok 4.7 (21 Eylül).
  - 2026-11-16 (⚪): İkincil (15 Kasım): Grok 4.8 Bot kullanıcılarına "soft rollout" (13 Kasım). Model kartı, API, fiyat yok.

### 33. Always-on kişisel/iş ajanları (OpenAI Dots, Meta Muse, ChatGPT Space, Claude Duet, Perplexity Teammates, Databricks Genie, ByteDance, Apple; açık kaynak: OpenDots, nanoMuse)
- İlk görülme: 2026-10-05 | Son güncelleme: 2026-11-22 | Son kontrol: 2026-11-22 | Durum: Aktif
- Özet (10-05/10-23): OpenAI Dots (29 Eylül) ile kategori ana akım; Claude Duet (21 Ekim).
  - 2026-11-07 (🟡): Perplexity Teammates; Rerun self-host (ikincil).
  - 2026-11-13 (🟡): İkincil: ByteDance Muse benzeri ajan; Databricks Genie always-on; n8n Nod.
  - 2026-11-22 (⚪): İkincil (K3, 19 Kasım): Apple'ın cihaz/uygulama/tarayıcı kontrol eden ajan geliştirdiği bildiriliyor (Bloomberg); Gemini for Mac (#3).

### 34. Frontier güvenlik olayları ve düzenleyici yanıt (OpenAI duraklatma, SI Force, FTC, METR, NY RAISE, Avustralya, AB sandbox)
- İlk görülme: 2026-09-28 | Son güncelleme: 2026-11-22 | Son kontrol: 2026-11-22 | Durum: Aktif
- Özet (09-28/11-13): OpenAI eğitim duraklaması; SI Force, FTC CID'leri; METR AECI 1,9 kat; DOJ SI Task Force; NY RAISE portalı (1 Ocak 2027); Avustralya planı; ABD–Çin olay kanalı.
  - 2026-11-16 (🟡): İkincil: AB Uygulama Tüzüğü 2026/2487 — AI sandbox'ları. "San Francisco Bildirgesi" (FT).
  - 2026-11-19 (🟡): İkincil: Oregon AG – OpenAI davası; 4 STK'nın ihtiyati tedbir davası (K3); Çin misilleme tehdidi; Vals askeri hedefleme testi.
  - 2026-11-22 (⚪): İkincil (Semafor, 19 Kasım): dört senatörden halka açık şirketlerin AI açıklamalarına dair iki partili tasarı.

### 35. ABD açık/lisanslı ağırlık yarışı (Muse Spark Open, Reflection Beam, MAI-Base-2, Inkling 2)
- İlk görülme: 2026-10-17 | Son güncelleme: 2026-11-16 | Son kontrol: 2026-11-22 | Durum: Aktif
  - 2026-10-17 (🟢) — İLK TAKİP: Reflection AI Beam (501B/23B, Apache 2.0), Microsoft MAI-Base-2, Meta Muse Spark Open (#28).
  - 2026-11-07 (🟡): Thinking Machines Inkling 2 Small (5 Kasım) — 594B/17B aktif MoE.
  - 2026-11-16 (🟡): K3 (12 Kasım): ağırlıklar HF'de `thinkingmachines/Inkling-2-Small`; AA Intelligence Index 31.

### 37. AI destekli zafiyet keşfi (PHP2Shell, Node2Shell, Codex Security, Wiz Atlas, GPT-6 Cyber, Mythos 5.2)
- İlk görülme: 2026-10-23 | Son güncelleme: 2026-11-19 | Son kontrol: 2026-11-22 | Durum: Aktif
- Özet (10-23/11-07): PHP2Shell (CVE-2026-109618/109619); php2shell-checker; CISA KEV; Node2Shell (CVE-2026-111497, CVSS 9,2); GPT-6 Cyber.
  - 2026-11-10 (🟡): Claude Mythos 5.2 (9 Kasım; #2) — CVE Rediscovery %89,6.
  - 2026-11-19 (🟡): GPT-6.2 Astra/Sol siber "Critical" (#26). İkincil: Calif AI ile Java'da ciddi açık (NYT); Reflection Laser (Axios).
  - 2026-11-22 (yıldız, 22 Kasım): php2shell-checker 1.477 (9 günde +%0,5).

### 38. Kimi (Moonshot) — K3 → K3.1 Pro
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-22 | Son kontrol: 2026-11-22 | Durum: Aktif (08-31 arşivlendi, 10-26 geri döndü)
- Özet (07-27/11-04): K3.1 Pro + Highspeed (23 Ekim), 1M bağlam; K2 serisi emeklilik Aralık sonu.
  - 2026-11-07 (🟢): Ağırlıklar — `moonshotai/Kimi-K3.1-Pro`: 2,8T / 104B aktif, 1.048.576 bağlam; özel lisans.
  - 2026-11-19 (⚪): İkincil (K3 16 Kasım): kodlama yarışından çekilip biyoloji/kimya/ilaç araştırmasına yöneliyor.
  - 2026-11-22 (⚪): İkincil (The Information, K3 19 Kasım): Endonezya veri merkezi için $150 milyonluk Nvidia çip anlaşması iptal.

### 39. AI ile matematik/bilim keşif ve biçimsel doğrulama (OpenAI ETH/Yang–Mills, Axiom CFSG, Fable 5.2 FLT, AlphaProof Code, /teamwork, Alpöge RH ve Navier–Stokes)
- İlk görülme: 2026-10-29 | Son güncelleme: 2026-11-22 | Son kontrol: 2026-11-22 | Durum: Aktif
- Özet (10-29/11-10): OpenAI ETH çürütme, local smoothing, 4B Yang–Mills (Lean). Axiom CFSG Lean formalizasyonu. 1.000 Fable 5.2 ajanı FLT'yi 30 saatte formalize etti (Anthropic iddiası, 9 Kasım).
  - 2026-11-13 (🟡): K3 (10 Kasım): AlphaProof Code — Signal protokol güvenlik özellikleri Lean'de.
  - 2026-11-16 (🟡): Google Research (13 Kasım): /teamwork-LEAP Weil sanıları Lean'de (~1,8M satır). Yıldız (16 Kasım): CFSG 166.
  - 2026-11-22 (🟢): Levent Alpöge (Anthropic teknik kadro) 20 Kasım'da Claude ile RH + Dirichlet GRH ispatı iddiası — 175.187 dosyalık Lean arşivi, insan-okur makale yok (leanprover-community/riemann-hypothesis; Al Jazeera). Buzzard: ~17M satır, "neden doğru bilmiyoruz". Bağımsız Comparator doğrulaması sürüyor. Aynı gün Alpöge & Buckmaster: Navier–Stokes sonlu zamanda patlama, 79 sayfa + ~2.270 dosya/600.000 satır Lean; aralık aritmetiği sertifikası henüz yayımlanmadı (tristanbuckmaster/navier-stokes).

### 41. Meituan LongCat model ailesi
- İlk görülme: 2026-11-04 | Son güncelleme: 2026-11-04 | Son kontrol: 2026-11-22 | Durum: Aktif
  - 2026-11-04 (🟡) — İLK TAKİP: LongCat-2.5 Preview (2 Kasım; TechNode) — 1,6T / ~48B aktif; açık ağırlık henüz yok.

### 42. AI veri merkezi altyapısına yerel tepki, enerji ve piyasa etkisi (Nvidia liderlik krizi dahil)
- İlk görülme: 2026-11-07 | Son güncelleme: 2026-11-22 | Son kontrol: 2026-11-22 | Durum: Aktif
- Özet (11-07/11-13): ABD yerel oylamalarında veri merkezi kısıtları; OpenAI "National Community Compact"; Anthropic OnePWR (K1); EIA rekor talep.
  - 2026-11-16 (🟡): İkincil: Huang görevden alındı (Bloomberg, 15 Kasım).
  - 2026-11-19 (🟡): Nvidia Q3 FY27: gelir $115,8 milyar (+%103), veri merkezi $107,6 milyar; Q4 beklenti $130,0 milyar; Kress geçici CEO. İkincil: Çin'e çip satışı bırakılıyor.
  - 2026-11-22 (⚪): İkincil (K3, 19 Kasım): Nvidia'nın Inception'ı (Mercury difüzyon modelleri) satın alma görüşmesi; 403 ABD veri merkezi ABD elektriğinin ~%2'si (Semafor).

### 43. Ajanlarla tersine mühendislik (REA ekosistemi) ve laboratuvar kısıtlamaları
- İlk görülme: 2026-11-13 | Son güncelleme: 2026-11-13 | Son kontrol: 2026-11-22 | Durum: Aktif
  - 2026-11-13 (🟡) — İLK TAKİP: Claude ve Codex, ajanları IoT cihazlarına yönelten kullanıcıları güvenlik bloklarıyla durduruyor (404 Media aktarımı; ikincil). Yıldız (13 Kasım, API): morluto/rea 455.826 (bülten "342.000", K1); leanrea 4.240; REA-Prompts 4.007.
  - 2026-11-22 (yıldız, 22 Kasım): rea 473.043 (9 günde +%3,8); leanrea 4.419 (+%4,2); REA-Prompts 4.331 (+%8,1).

### 44. MiniMax H3 ailesi (arşivden döndü: eski "DiffusionGemma/MiniMax H3", 08-31)
- İlk görülme: 2026-08-31 öncesi | Son güncelleme: 2026-11-13 | Son kontrol: 2026-11-22 | Durum: Aktif (08-31 arşivlendi, 11-13 geri döndü)
  - 2026-11-13 (🟡): MiniMax H3-Image (11 Kasım) — açık ağırlık görsel üretim/düzenleme (HF: MiniMaxAI/MiniMax-H3-Image); lisans adı yok.

### 45. Ajan ödemeleri ve kişisel finans entegrasyonları (ChatGPT Wallet, Gemini + Google Wallet, Claude Personal Finance)
- İlk görülme: 2026-11-16 | Son güncelleme: 2026-11-16 | Son kontrol: 2026-11-22 | Durum: Aktif
  - 2026-11-16 (🟡) — İLK TAKİP: K3 (13 Kasım): Gemini + Google Wallet (ABD, salt-okunur, Plaid). İkincil: ChatGPT Wallet — ajanlar onayla tokenize kartla satın alıyor. İlişkili: Claude Personal Finance (#2).

### 46. Tencent Hunyuan Hy4 ailesi
- İlk görülme: 2026-11-22 | Son güncelleme: 2026-11-22 | Son kontrol: 2026-11-22 | Durum: Aktif
  - 2026-11-22 (🟡) — İLK TAKİP: K3 (18 Kasım ağırlıklar; TechNode): Hy4 Flash — ~224B / ~12B aktif, 1M bağlam, metin+görsel; standart, FP8, base; "Tencent Hy License" (HF: tencent/Hy4-flash).

## Arşivlenmiş Konular

(Geri dönüş olmadıkça satır eklenmez. Tam geçmiş git commit'lerinde.)

- **AI eğitim tercihi sinyali / yayıncı opt-out standardı [#40]** — İlk 11-01 | Son güncelleme 11-01 | Arşiv 11-22. OpenAI, Google, Microsoft, Anthropic ortak sinyal (30 Ekim); IETF `draft-kelley-aipref-training-preference-signal`; Microsoft'ta 1 Şubat 2027.
- **TypeSafe AI — Jev / "System One Models" [#31]** — İlk 09-21 | Son güncelleme 10-26 | Arşiv 11-16. Jev 1.14.0 (14 Ekim); 24 Ekim veri sızıntısı.
- **Vercel fx / libfx / fx0 [#27]** — İlk 08-24 | Son güncelleme 10-20 | Arşiv 11-10. Son yıldızlar (10 Kasım): fx 3.801, fx0 431.
- **AB AI Act uygulama takvimi ve standartları [#36]** — İlk 08-07 | Son güncelleme 10-20 | Arşiv 11-10. EN 18286:2026 (19 Ekim).
- **Prime Agent (Prime Intellect) [#17]** — İlk 08-08 | Son güncelleme 10-12 | Arşiv 11-04. Son yıldız (4 Kasım): 22.557.
- **AI ajan mimarisi/hafıza yaklaşımları [#20]** — Son güncelleme 10-12 | Arşiv 11-04. Yıldız (4 Kasım): agent-memory 4.303.
- **Z.ai (Zhipu) ZCode ve GLM dikey modelleri [#32]** — İlk 09-21 | Son güncelleme 10-12 | Arşiv 11-04. Son yıldız (4 Kasım): 8.461.
- **Yerel/açık kaynak Cowork alternatifleri [#22]** — Son güncelleme 10-05 | Arşiv 10-26. Yıldız (26 Ekim): eigent 15.662, OpenDots 6.013.
- **Eski arşiv (tek satır):** Anthropic Cowork (09-21; #2), Salesforce Slackbot/Claudeforce (09-21), ChatGPT for Work & GPT-Live (08-17), OptMem (08-17), Sakana Fugu-Cyber (08-17), x402 (08-31), Mistral Shieldstral (08-31), DiffusionGemma (08-31; MiniMax H3 kısmı #44), Gemini liderlik değişikliği (09-07).
- **OpenAI Astra (matematik modeli — GPT-6 Astra ile KARIŞTIRILMASIN)** — İlk 08-07 | Son 08-10 | Arşiv 08-31. Yeni matematik iddiaları #39'da.

## Değişiklik Geçmişi

- 2026-08-10 – 2026-11-07: bkz. git geçmişi (08-10 repoya taşındı; 10-16 3 günlük ritim, kapı, "Son kontrol"/yıldız/BEKLEYEN NOT kuralları, `gorev-talimati.md`).
- 2026-11-10 (pencere 8-10 Kasım): 0 yeni konu; 9 güncelleme; 2 arşiv (#27, #36). Sıkıştırma ~26,9 → ~24,5 KB.
- 2026-11-13 (pencere 11-13 Kasım): +1 konu (#43); #44 arşivden döndü; 12 güncelleme; 0 arşiv. Sıkıştırma ~25,3 → ~24,7 KB.
- 2026-11-16 (pencere 14-16 Kasım): +1 konu (#45); #30 arşivden döndü; 11 güncelleme; 1 arşiv (#31). Sıkıştırma.
- 2026-11-19 (pencere 17-19 Kasım): 0 yeni konu; 9 güncelleme; 0 arşiv. Yıldız satırları: #13, #25. Sıkıştırma ~27,6 → ~24,3 KB.
- 2026-11-22 (pencere 20-22 Kasım, hafta sonu): +1 konu (#46 Tencent Hy4); 11 güncelleme (#2, #3, #12, #24, #28, #33, #34, #38, #39, #42, #46); 1 arşiv (#40). Ana olay: Alpöge + Claude RH Lean iddiası (#39). K3: 19 Kasım haberleri (EC/ARTEX, Muse sızıntısı, Genie 4 API, Hy4). Yıldız satırları: #37, #43. K2: WebFetch yok (alt ajan); Newegg, alpo.ge/remark.pdf açılmadı. Sıkıştırma (#2, #3, #24, #34, #39, #42 özetlendi; geçmiş satırları kısaltıldı). BEKLEYEN NOT yoktu.
