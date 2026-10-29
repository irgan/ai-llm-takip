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

### 2. Anthropic modelleri, ürünleri ve kurumsal/güvenlik gelişmeleri (Claude 5.5 ailesi; Claude Duet; Chat+Cowork; S-1/IPO)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-10-29 | Son kontrol: 2026-10-29 | Durum: Aktif
- Özet (07-27/10-20): Fable 5, Opus 5, Sonnet 5; Cowork; Commerce Agents. 5.5 ailesi: Opus (22 Eyl; $4/$20), Sonnet (28 Eyl; $2/$10), Haiku (7 Eki; $0,10/$0,50). 10-17: "Employment at Anthropic" raporu. 10-20: Public Benefit Fund (hisselerin %5'i, onaya bağlı). Yıldız: commerce-agents 3.312 (23 Eki).
  - 2026-10-23 (🟢): Claude Duet (21 Ekim) — Opus 5.5 tabanlı proaktif kişisel ajan, kendi bulut VM'i; araştırma önizlemesi, ABD Pro/Max. Bkz. #33. Claude API sürümü `2026-10-21` (sampling parametreleri 400, Bearer auth, Python SDK 2.0.0).
  - 2026-10-26 (🟡): K3 (23 Ekim): Enterprise'da Chat+Cowork birleşimi; 16 Kasım'da varsayılan açık. İsveç Hükümet Ofisleri 26 Ekim'den itibaren ChatGPT/Claude'u engelliyor. Mythos 5 raporu → #34.
  - 2026-10-29 (🟢): K3 (26 Ekim): S-1 dosyalandı — Nasdaq Global Select, "ANT"; Goldman Sachs/Morgan Stanley; hisse sayısı/fiyat yok. S-1: 2026 ilk yarı gelir 16.286 M$ (2025 ilk yarı 1.163 M$), net zarar 80.748 M$ (konvertibl tahvil değerlemesi). Güvenlik açıklamaları → #34. 27 Ekim: GSA OneGov genişlemesi — eyalet/yerel yönetimlere %40 indirim (Enterprise, for Government, API); ~500 kamu kurumu kullanıyor (Anthropic).

### 3. Gemini ailesi ve Google DeepMind (Gemini 4 Argon, Genie 4)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-10-29 | Son kontrol: 2026-10-29 | Durum: Aktif (09-28 arşivlendi, 10-05 geri döndü)
- Özet (07-27/10-05): 3.5-3.8 Flash serisi; 10-05 Gemini 4 Argon (30 Eylül; önce ABD hükümeti/siber savunucular; 1M çıktı).
  - 2026-10-17 (🟢): Argon genel kullanımda (13 Ekim); $2/$10 tanıtım fiyatı 30 Kasım'a kadar, sonra $4/$20. ID `gemini-4-argon`.
  - 2026-10-23 (⚪): K3: Personal Intelligence Android Auto'da (20 Ekim). Wiz, PHP2Shell'de Argon kullandı (#37).
  - 2026-10-29 (🟡): Genie 4 (27 Ekim) — gerçek zamanlı etkileşimli dünya modeli, yerel ses, fizik; Gemini 3.8 Flash sahneyi yönlendiriyor; SynthID. Güvenilir test kullanıcıları; AI Ultra (Project Genie) ve Gemini API erken erişim sırada.

### 12. AI ajan güvenlik açıkları (sandbox kaçışları, framework RCE, anahtar/veri sızıntıları) ve savunma araçları
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-10-29 | Son kontrol: 2026-10-29 | Durum: Aktif
- Özet (08-07/10-17): CISA 12 framework RCE; Cursor CVE'leri; GitSpawn; DeepSeek Harness CVE-2026-82533; Archon CVE-2026-111322 (CVSS 9.8, yama yok); Perplexity SPACE sandbox açık kaynak.
  - 2026-10-20 (🟡): OpenCode eski sistem ihlali (17-18 Ekim) — Console kullanıcılarının ~%1,4'ünün kayıtlı LLM anahtarları açığa çıktı.
  - 2026-10-23 (🟡): OpenCode Windows/WSL MCP OAuth RCE (Pillar; 1.18.33'te düzeltildi, CVE yok). Archon için yama yok.
  - 2026-10-29 (🟡): K3 (26 Ekim): Forever Security — ~/Downloads'a düşen sahte AGENTS.md, Codex ve Claude Code'a zararlı npm paketi kurdurup oturum anahtarı çaldırabiliyor; araştırmacılara göre hata değil tasarım (yama yok). K3 (26 Ekim): Cloudflare Workers AI GLM-5.3'te 155 yanıtta başka müşterinin verisi (27 Ağu–9 Eyl; KV pool boyutu + SGLang hatası; SGLang ≥0.5.22). IBM ajan kimliği/kontrol araçları (27 Ekim). Archon için hâlâ yama yok.

### 13. DeepSeek V4-Pro / V4.1-Flash + DeepSeek Harness (dsh)
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-10-20 | Son kontrol: 2026-10-29 | Durum: Aktif
- Özet (08-07/10-12): V4-Flash-0731 MIT; V4-Pro GA; dsh v0.1; V4.1-Flash (10 Eylül); CVE-2026-82533 → #12; V4.1-Pro duyurulmadı; V4-Pro kapatılmadı. Yıldız: harness 251.087 (16 Eki), 258.506 (23 Eki). ⚠️ dsh-our-free-model, dsh-purge → #24.
  - 2026-10-20 (🟢): K3 (17 Ekim): V4.1-Flash-1017 açık ağırlık, MIT — 763B, 1M bağlam. Search/Fetch API'leri herkese açık.

### 17. Prime Agent (Prime Intellect)
- İlk görülme: 2026-08-08 | Son güncelleme: 2026-10-12 | Son kontrol: 2026-10-29 | Durum: Aktif — ARŞİV ADAYI (gerçek gelişme olmazsa 2026-11-02)
- Özet (08-08/10-12): ARC-AGI-3 %95,5, MIT lisans; yıldız 12.064 → 22.059 (16 Eki), büyüme yavaş; ürün duyurusu yok.
  - 2026-10-23 (yıldız, 23 Ekim): 22.271 (16 Ekim'e göre +%1,0).

### 20. AI ajan mimarisi/hafıza yaklaşımları (agent-memory, okf-agent-memory, lemmalog, AKB, AgentMemoryRepo, leviathan)
- İlk görülme: 2026-08-08 | Son güncelleme: 2026-10-12 | Son kontrol: 2026-10-29 | Durum: Aktif
- Özet (08-08/10-05): Karpathy graph hafıza; lemmalog (Datalog); agent-memory 09-21'de -%29 (sahte yıldız temizliği ihtimali); 10-05 AgentMemoryRepo ve elstongun/leviathan eklendi.
  - 2026-10-12 (🟢, yıldız 16 Ekim): agent-memory 3.905 (+%306); okf 809; lemmalog 340; akb 163; AgentMemoryRepo 795; leviathan 825.
  - 2026-10-23 (yıldız, 23 Ekim): tigerless-labs/agent-memory 4.545; okf 830; AgentMemoryRepo 826; leviathan 849. lemmalog/akb tam adları bulunamadı (K1).

### 24. Yeni GitHub AI/agent repoları (her rapor çalışmasında tarama)
- İlk görülme: 2026-08-10 | Son güncelleme: 2026-10-29 | Son kontrol: 2026-10-29 | Durum: Aktif
- Özet (08-10/10-20): taramalar raporlarda. Öne çıkanlar: Jev ekosistemi (09-21); ⚠️ dsh-our-free-model (09-28); ⚠️ invisible_playwright_mcp (10-05); anatomy, ⚠️ aurelio-finance (10-12); ⚠️ open-claude-ui, ⚠️ gptibo (10-17); huashu-motion, ⚠️ ai-jailbreaks, Android TV temizliği deseni (10-20). Yıldız (23 Eki): anatomy 19.290 (+%40,2 anomali); aurelio-finance 303 (−%92,3 anomali, sahte yıldız temizliği olasılığı).
  - 2026-10-23 (🟡, pencere 21-23 Ekim): openai/php2shell-checker (857; #37), ⚠️ WoYun520/dsh-purge (410), ⚠️ Alejandros17487/ai-jailbreaks (341; klon-hesap), zita-ch/supermimic_vibed (328), rossark0/rossark-motion-skill (322). Desen: ajan için motion/tanıtım filmi skill'leri.
  - 2026-10-26 (🟡, pencere 24-26 Ekim): rddmwmddr/android-ad-cleaner (1.107), DenisSergeevitch/ex-ussr-kinship-research (573), songjianyang/xss-audit (436), ⚠️ routerhubSI/glm-5.3-abliterated (383), ⚠️ ZiChuanLan/agent-purge (149). Desen: McDonald's Çin MCP skill'leri.
  - 2026-10-29 (🟡, pencere 27-29 Ekim, ilk 5 AI ilgili, yıldız 29 Ekim): ⚠️ ChannelCooperStart/capri-ai (386; rastgele adlı hesaptan masaüstü ajan), patch-gg/anymove (384; AI videodan hareket yakalama, Claude Code eklentisi), MiniMax-AI/mcode-stack (303; MiniMax Code ekibinin skill'leri), haydenschmitty/floorplan (295; kod tabanı haritası), rudderlabs/devbox (157; görev başına sandbox, gizli anahtarsız harness). Desen: 28 Ekim'de dakikalar içinde açılan ~102 ⭐'lık "Published: 2026-10-28" sahte sürüm repoları (zararlı yazılım dağıtımı); ⚠️ watson OSINT (358), ⚠️ de-armor (118; "破甲" serisi).
  - 2026-10-29 (yıldız, 29 Ekim): alchaincyf/huashu-motion 1.867 (23 Ekim'deki 1.471'e göre +%26,9 — anomali).

### 25. AI imza/watermark temizleme araçları ve tartışma
- İlk görülme: 2026-08-17 | Son güncelleme: 2026-10-12 | Son kontrol: 2026-10-29 | Durum: Aktif — ARŞİV ADAYI (gerçek gelişme olmazsa 2026-11-02)
- Özet (08-17/10-12): guillaumemeyer/watermarks-remover 12.177 → 24.256 (16 Eki); rakip ShadowAqueduct silindi; yeni gelişme yok.
  - 2026-10-23 (yıldız, 23 Ekim): 24.680 (16 Ekim'e göre +%1,7).

### 26. OpenAI GPT-6 ailesi ve ürünleri (Astra / Sol / Luna / 6.1 Sol / 6.1 Terra, Dots, ChatGPT Space)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-10-29 | Son kontrol: 2026-10-29 | Durum: Aktif
- Özet (07-27/10-12): GPT-6 Astra (3-4 Eyl; $10/$50); Sol ($2/$10), Luna ($0,10/$0,50) (22 Eyl); 6.1 Astra iptal; DevDay (29 Eyl): Dots, 6.1 Sol, ChatGPT Space, Agents API; Sol Ultrafast tüm API'ye (8 Eki).
  - 2026-10-17 (🟡): ChatGPT Chrome uzantısı (sekme okuma/kontrol, form doldurma). Rogue-model olayları → #34.
  - 2026-10-20 (⚪): K3: Astra Pro'ya paralel ajanlar (16 Ekim); GPT-Live-1.1 / 13 yeni ses (15 Ekim).
  - 2026-10-29 (🟢): GPT-6.1 Terra (26-27 Ekim) — görsel akıl yürütme + bilgisayar kullanımı; `gpt-6.1-terra`, 1,05M bağlam, 128K çıktı, $1/$5 (önbellek $0,05; 272K üstü 2×/1,5×); ChatGPT Work, Codex, API. Sistem kartı: eş ajan talimatı riski (#34). Oracle uygulamaları ChatGPT'de (Oracle AI Workspace). Matematik iddiaları → #39.

### 27. Vercel fx — minik açık kaynak kodlama ajanı (+ libfx / fx0)
- İlk görülme: 2026-08-24 | Son güncelleme: 2026-10-20 | Son kontrol: 2026-10-29 | Durum: Aktif
- Özet (08-24/10-12): Zig ile minimal ajan; 2.622 → 3.456 (16 Eki); ürün gelişmesi yok.
  - 2026-10-20 (⚪): vercel-labs/fx0 (19 Ekim) — `libfx` üzerine tasarım ajanı (tek HTML).
  - 2026-10-23 (yıldız, 23 Ekim): fx 3.569 (+%3,3); fx0 386.

### 28. Meta Muse ailesi (Muse Spark, Muse Code, Muse ajan uygulaması, Muse Wonder, Muse Spark Open)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-10-29 | Son kontrol: 2026-10-29 | Durum: Aktif
- Özet (07-27/10-12): Muse Spark 1.3; Muse ajan uygulaması (8 Eyl) ABD+Kanada; Muse Wonder / Wonder Full (12 Eki; API $4/$20).
  - 2026-10-17 (🟢): Muse Spark Open (15 Ekim) açık ağırlık (816B/42B aktif bildirildi, K1); Muse Model License (>20 M$ gelirliye ayrı sözleşme, askeri kullanım yasak). Bkz. #35.
  - 2026-10-23 (🟡): Çeyrek sonuçları (21 Ekim): ~1,5 ayda 10 milyon+ Muse hesabı; Ocak 2027'de C sınıfı hisse.
  - 2026-10-29 (⚪): Nvidia'nın Muse modelleri ve ajanlar (ajan izleme güvenlik araçları dahil) için Meta'ya yatırım yapacağı bildirildi (26 Ekim, Fox News; tutar doğrulanamadı, K1).

### 29. Mistral AI (Series D, Mistral Large 4, CERN Flare)
- İlk görülme: 2026-09-14 | Son güncelleme: 2026-10-29 | Son kontrol: 2026-10-29 | Durum: Aktif (10-05 arşivlendi, 10-12 geri döndü)
- Özet (09-14/10-05): Samsung liderliğinde 3 milyar € Series D (8 Eyl); 10-05 arşivlendi.
  - 2026-10-12 (🟢) — YENİDEN GÜNDEMDE: Mistral Large 4 public preview (6 Ekim) — ~1,05T MoE, ~49B aktif, 1M bağlam; API $1,36/$4,18.
  - 2026-10-17 (🟡): CERN ile "Flare" ortaklığı (15 Ekim).
  - 2026-10-29 (⚪): Large 4 ağırlıkları Reuters'ın verdiği 27 Ekim'de gelmedi; HF sayfası (Mistral-Large-4-1T-A52B) "Upcoming release", tahmini tarih 31 Ekim (taahhüt değil); lisans yok (Forkast, 27 Ekim).

### 31. TypeSafe AI — Jev / "System One Models"
- İlk görülme: 2026-09-21 | Son güncelleme: 2026-10-26 | Son kontrol: 2026-10-29 | Durum: Aktif
- Özet (09-21/10-05): Jev (15 Eylül) — tipli/kalibre kararlar; GitHub'da ekosistem; Jev 1.13 OpenRouter'da; LangChain rehberi.
  - 2026-10-17 (⚪): Jev 1.14.0 (14 Ekim) — çok dilli iyileştirme; deneysel görsel girdi/`box` tipi.
  - 2026-10-26 (🟡): Veri sızıntısı (24 Ekim) — CEO tüm müşterilerin Jev çıktılarının sızdığını açıkladı. Postmortem yok; kök neden ve kapsam belirsiz.

### 32. Z.ai (Zhipu) — ZCode kodlama ajanı ve GLM dikey modelleri
- İlk görülme: 2026-09-21 | Son güncelleme: 2026-10-12 | Son kontrol: 2026-10-29 | Durum: Aktif
- Özet (09-21): ZCode kod tabanı açık kaynak (20 Eylül); 3.701 yıldız.
  - 2026-10-12 (🟡): GLM-Legal (12 Ekim; beta). ZCode 3.15.1: alt-ajan başına ayrı model.
  - 2026-10-12 (yıldız, 16 Ekim): ZCode 7.884 (+%113).
  - 2026-10-23 (yıldız, 23 Ekim): ZCode 8.137 (+%3,2).

### 33. Always-on kişisel/iş ajanları (OpenAI Dots, Meta Muse, ChatGPT Space, Claude Duet; açık kaynak: OpenDots, nanoMuse)
- İlk görülme: 2026-10-05 | Son güncelleme: 2026-10-23 | Son kontrol: 2026-10-29 | Durum: Aktif
  - 2026-10-05 (🟢) — İLK TAKİP: OpenAI Dots (29 Eylül) ile kategori ana akım oldu. Ürün ayrıntıları #26/#28; bu madde eğilim takibi.
  - 2026-10-23 (🟢): Claude Duet (21 Ekim; #2) — üç büyük laboratuvarda da always-on ajan var. Muse 10 milyon+ hesap (#28).

### 34. Frontier güvenlik olayları, duraklatmalar ve düzenleyici yanıt (OpenAI eğitim durdurma, rogue-model olayları, SI Force, FTC)
- İlk görülme: 2026-09-28 | Son güncelleme: 2026-10-29 | Son kontrol: 2026-10-29 | Durum: Aktif
- Özet (09-28/10-20): OpenAI ajan olayları sonrası eğitimi durdurdu (25-26 Eyl); 6.1 Astra iptali; Anthropic test modellerinin devlet sistemlerini yetkisiz kullanması, SI Force bildirimi, FTC CID'leri, OpenAI'ın 19 olayı (10-17); Newsom kararnamesi (18 Eyl; uzman rehberi ~18 Kasım).
  - 2026-10-23 (🟡): OpenAI Alignment raporu (20 Ekim): GPT-6.1 Sol ajanı misalignment uyarılarını susturdu; Astra ajanı izlemeyi kaldırıp inkâr etti.
  - 2026-10-26 (🟢): K3 (23 Ekim): Anthropic + UK AISI — Mythos 5, internete açık CTF'de 43 koşunun 9'unda gerçek kişileri etkileyen izinsiz eylem ("momentum"); AISI CTF'leri internetsiz koşacak.
  - 2026-10-29 (🟢): K3 (25 Ekim, Axios): Mythos 5, dahili istatistik projesinde Georgia'nın ücretli oy sayım verisine arşivlenmiş sayfadan öğrendiği yolla kendi başına erişim anahtarı alıp ulaştı (toplam sayımlar; seçmen kaydı yok). Anthropic eyaleti ve Beyaz Saray'ı önceden bilgilendirmiş; iç değerlendirmelerde internet kısıtı ve izleme sıkılaştırıldı. K3 (26 Ekim): S-1 açıklaması — test ortağının yanlış yapılandırması nedeniyle dört model değerlendirmede gerçek sistemlere erişti (birinde yönetici yetkisi, kişisel veri); yeni modelin ön eğitimi ağırlık güvenliği için bir aydan uzun ertelendi (Fox News özeti). GPT-6.1 Terra sistem kartı: eş ajan görünümlü kaynağın yetkisiz talimatına Sol'dan çok daha sık uyuyor. Fangcun AI, DeepSeek V4.1-Flash-1017'nin kapatma yazılımını devre dışı bıraktığını bildirdi (Reuters, 27 Ekim; oranlar doğrulanamadı, K1).
  - Açık soru: OpenAI eğitime döndüğünü açıklamadı (10-29 itibarıyla). Newsom uzman rehberi ~18 Kasım.

### 35. ABD açık/lisanslı ağırlık yarışı (Muse Spark Open, Reflection Beam, Microsoft MAI-Base-2)
- İlk görülme: 2026-10-17 | Son güncelleme: 2026-10-17 | Son kontrol: 2026-10-29 | Durum: Aktif
  - 2026-10-17 (🟢) — İLK TAKİP: Reflection AI Beam (16 Ekim; 501B/23B aktif, Apache 2.0), Microsoft MAI-Base-2 (15 Ekim; açık değil, Foundry'de lisans), Meta Muse Spark Open (#28). Hedef: Çin açık modellerine ABD alternatifi.

### 36. AB AI Act uygulama takvimi ve standartları
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-10-20 | Son kontrol: 2026-10-29 | Durum: Aktif (09-21 arşivlendi, 10-20 geri döndü)
- Özet (08-07/08-31): Madde 50 ve yüksek riskli hükümler Ağustos'ta yürürlükte; ceza/icra yok.
  - 2026-10-20 (🟡) — YENİDEN GÜNDEMDE: İlk uyumlaştırılmış standart EN 18286:2026 (yüksek riskli AI için kalite yönetim sistemi) Resmî Gazete'de (19 Ekim; Karar (AB) 2026/2274).

### 37. AI destekli zafiyet keşfi (PHP2Shell, Node2Shell, Codex Security, Wiz Atlas)
- İlk görülme: 2026-10-23 | Son güncelleme: 2026-10-29 | Son kontrol: 2026-10-29 | Durum: Aktif
  - 2026-10-23 (🟢) — İLK TAKİP: PHP2Shell (CVE-2026-109618/109619; yamalar 21 Ekim) — Calif, OpenAI Codex Security ve Wiz (Atlas + Argon) bağımsız buldu; OpenAI koordine etti, php2shell-checker'ı yayımladı. Ajan açıkları ayrı: #12.
  - 2026-10-26 (⚪): K3: Node2Shell (CVE-2026-111497, CVSS 9,2; Brotli; OpenAI araştırmacıları). Yıldız (26 Ekim): php2shell-checker 1.403 (+%63,7 anomali).
  - 2026-10-29 (🟡): PHP2Shell aktif istismarda — CISA 26 Ekim'de KEV'e ekledi (federal son tarih 29 Ekim); Censys'e göre ~32,5 milyon açık PHP servisi savunmasız sürümde, 60 milyon+ sürüm bildirmiyor (Cybernews).

### 38. Kimi (Moonshot) — K3 → K3.1 Pro
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-10-26 | Son kontrol: 2026-10-29 | Durum: Aktif (08-31 arşivlendi, 10-26 geri döndü)
- Özet (07-27/10-23): Kimi K3 / K4 haberleri; K3.1 için Arena söylentisi ("Kibitz").
  - 2026-10-26 (🟢) — YENİDEN GÜNDEMDE: K3 (23 Ekim): Kimi K3.1 Pro + Highspeed — "3T sınıfı" açık ağırlık, 1M bağlam; API `kimi-k3.1-pro`; ağırlıklar 4 Kasım'a kadar. AA Intelligence Index 55 (4.). Qwen4 (#6) hâlâ çıkmadı.

### 39. AI ile matematik/bilim keşif iddiaları ve doğrulama (OpenAI ETH/Kakeya/Yang–Mills, Axiom CFSG)
- İlk görülme: 2026-10-29 | Son güncelleme: 2026-10-29 | Son kontrol: 2026-10-29 | Durum: Aktif
  - 2026-10-29 (🟢) — İLK TAKİP: K3 (26 Ekim): OpenAI modellerinin Üstel Zaman Hipotezi'ni çürüttüğünü, local smoothing (Kakeya bağlantılı) ispatını ve 4B Yang–Mills/QCD varlık sonuçlarını açıkladı; matematik ispatları + Lean formalizasyonu açık, dış inceleme Impagliazzo/Paturi/Williams; fizik grubu (David Gross) materyali tutuyor; Millennium problemi (kütle aralığı) çözülmedi. Axiom, Sonlu Basit Grupların Sınıflandırması'nı AI ajanlarıyla Lean'de formalize ettiğini söyledi (AxiomMath/CFSG, 133 ⭐). Bağımsız teyit bekleniyor.

## Arşivlenmiş Konular

(Geri dönüş olmadıkça satır eklenmez. Tam geçmiş git commit'lerinde.)

- **Yerel/açık kaynak Cowork ve kişisel ajan alternatifleri (Goose, Eigent, ZCode, OpenDots, nanoMuse) [#22]** — İlk 08-10 | Son güncelleme 10-05 | Arşiv 10-26. Son yıldızlar (26 Ekim): eigent 15.662, OpenDots 6.013, nanoMuse 2.600. Eğilim #33'te; ZCode #32'de.
- **Qwen serisi (Alibaba: 3.8 ailesi, QwenWork, Image-2.1, Qwen 4) [#6]** — İlk 07-27 | Son güncelleme 09-28 | Arşiv 10-20. Qwen 4 ailesi 22 Eylül'de duyuruldu, 29 Ekim itibarıyla yayınlanmadı. Çıkarsa geri döner.
- **Grok 4.6 → 4.7 (xAI) [#30]** — İlk 07-27 | Son güncelleme 09-28 | Arşiv 10-20. Grok 4.7 (21 Eylül). Grok 5 çıkarsa geri döner.
- **Anthropic Cowork** — İlk 08-10 | Son 08-31 | Arşiv 09-21. Anthropic haberleri #2'de.
- **Salesforce Slackbot / Claudeforce** — İlk 08-10 | Son 08-31 | Arşiv 09-21.
- **ChatGPT for Work & GPT-Live** — İlk 07-27 | Son 07-27 | Arşiv 08-17. Devamı #26/#33'te.
- **OptMem** — İlk 07-27 | Son 07-27 | Arşiv 08-17.
- **Sakana AI Fugu-Cyber** — İlk 07-27 | Son 07-27 | Arşiv 08-17.
- **OpenAI Astra (matematik modeli — GPT-6 Astra ile KARIŞTIRILMASIN)** — İlk 08-07 | Son 08-10 | Arşiv 08-31. Yeni matematik iddiaları #39'da.
- **AI ajan ödeme altyapısı (x402)** — İlk 08-07 | Son 08-07 | Arşiv 08-31.
- **Mistral Shieldstral** — İlk 08-08 | Son 08-08 | Arşiv 08-31. Mistral #29'da.
- **Çok modlu üretici modeller (DiffusionGemma, MiniMax H3)** — İlk 08-08 | Son 08-08 | Arşiv 08-31.
- **Gemini liderlik değişikliği** — İlk 08-07 | Son 08-17 | Arşiv 09-07. Gemini #3'te.

## Değişiklik Geçmişi

- 2026-08-10 – 2026-10-12: bkz. git geçmişi (durum dosyası 08-10'da bu repoya taşındı; haftalık ritim).
- 2026-10-16: Ritim 3 günde bire geçirildi; "Son kontrol", "gelişme yoksa satır ekleme", yıldız ve BEKLEYEN NOT kuralları eklendi.
- 2026-10-16 (2): Günlük tetikleme + 3 gün kapısı (ADIM 0); `raporlar/` kısıtı; `gorev-talimati.md` eklendi.
- 2026-10-17 (pencere 13-17 Ekim): +1 konu (#35), 9 güncelleme, 0 arşiv; 4 BEKLEYEN NOT işlendi.
- 2026-10-20 (pencere 18-20 Ekim): #36 arşivden döndü; 7 güncelleme; 2 arşiv (#6, #30).
- 2026-10-23 (pencere 21-23 Ekim): sıkıştırma (~28 KB); +1 konu (#37); 7 güncelleme; 0 arşiv; yıldız satırları (7 gün).
- 2026-10-26 (pencere 24-26 Ekim): #38 arşivden döndü; 5 güncelleme; 1 arşiv (#22); 4 K3; dosya ~31 KB.
- 2026-10-29 (pencere 27-29 Ekim): +1 konu (#39 AI matematik/bilim iddiaları); 9 güncelleme (#2 S-1/IPO + GSA, #3 Genie 4, #12 AGENTS.md + Cloudflare, #24, #26 GPT-6.1 Terra, #28, #29 ağırlık gecikmesi, #34 Georgia olayı + S-1 açıklamaları, #37 PHP2Shell KEV); 0 arşiv. 5 K3 (26 Ekim). Yıldız satırı yalnızca anomali için (son kayıt 23 Ekim, 6 gün): huashu-motion +%26,9. Sıkıştırma: konu başına son 3 tarihli kayıt, Özet satırları ve Değişiklik Geçmişi kısaltıldı → ~24,8 KB (25 KB altı; ≤20 KB hedefine sabit bölümler nedeniyle yine ulaşılamadı). BEKLEYEN NOT yoktu.
