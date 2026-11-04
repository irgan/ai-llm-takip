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

### 2. Anthropic modelleri, ürünleri ve kurumsal/güvenlik gelişmeleri (Claude 5.5 ailesi; Claude Duet; Chat+Cowork; S-1/IPO; Max/Ultra; FlashProve; message threads)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-04 | Son kontrol: 2026-11-04 | Durum: Aktif
- Özet (07-27/10-23): Fable 5, Opus 5, Sonnet 5; Cowork; Commerce Agents. 5.5 ailesi: Opus (22 Eyl; $4/$20), Sonnet (28 Eyl; $2/$10), Haiku (7 Eki; $0,10/$0,50). Public Benefit Fund (10-20). Claude Duet (21 Eki; #33); API sürümü `2026-10-21`; Enterprise Chat+Cowork birleşimi (16 Kasım'da varsayılan). 10-29: S-1 (Nasdaq "ANT"; 2026 ilk yarı gelir 16.286 M$, net zarar 80.748 M$); GSA OneGov.
  - 2026-11-01 (🟡): Planlar yeniden adlandırıldı (30 Ekim): Max 5x → Max ($100), Max 20x → Ultra ($200); doğrulanmış Ultra hesaplarında 5 saatlik oturum limiti kalktı, haftalık limit sürüyor. Cursor'daki sahte Claude Code eklentisi → #12. Yıldız (1 Kasım): commerce-agents 3.390.
  - 2026-11-04 (🟢): S-1/A (2 Kasım) — Q3 finansalları ve hesaplama taahhütleri (rakamlar yalnızca ikincil kaynakta, K1); RSI eşiği uyarısı → #34. FlashProve (2 Kasım; EPFL/MIT ile zkSNARK tabanlı kanıtlanabilir çıkarım, Apache 2.0 araştırma prototipi; 400B MoE'de tek H100'de ~110 token/sn, ~19 MB kanıt/1.024 token). Messages API message threads beta (2 Kasım; `message-threads-2026-08-12`). Metin filigranı (3 Kasım) → #25. Claude Code Opus 5.5 sistem istemine mevcut oyunları klonlamayı engelleyen kural (The Decoder, 3 Kasım). Claude Code ürün lideri Cat Wu ayrıldı (3 Kasım; ikincil). "Mythos 5.5" söylentisi doğrulanmadı (Mythos sayfası 5.1).

### 3. Gemini ailesi ve Google DeepMind (Gemini 4 Argon, Genie 4)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-10-29 | Son kontrol: 2026-11-04 | Durum: Aktif (09-28 arşivlendi, 10-05 geri döndü)
- Özet (07-27/10-23): 3.5-3.8 Flash serisi; Gemini 4 Argon (30 Eyl), GA 13 Ekim — $2/$10 tanıtım fiyatı 30 Kasım'a kadar, sonra $4/$20; ID `gemini-4-argon`. Personal Intelligence Android Auto'da (20 Eki).
  - 2026-10-29 (🟡): Genie 4 (27 Ekim) — gerçek zamanlı etkileşimli dünya modeli; güvenilir test kullanıcıları; AI Ultra ve Gemini API erken erişim sırada.

### 6. Qwen serisi (Alibaba: 3.8 ailesi, QwenWork, Qwen 4; Apple Intelligence Çin)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-04 | Son kontrol: 2026-11-04 | Durum: Aktif (10-20 arşivlendi, 11-01 geri döndü)
- Özet (07-27/09-28): 3.8 ailesi, QwenWork, Image-2.1; Qwen 4 ailesi 22 Eylül'de duyuruldu.
  - 2026-11-01 (🟡) — YENİDEN GÜNDEMDE: Apple ve Alibaba (31 Ekim): Qwen, Çin'de Apple Intelligence'ı çalıştıracak; geliştirici önizlemesi 4 Kasım, genel dağıtım Aralık'ta iOS 27.3 ile (aiweekly özeti, CGTN).
  - 2026-11-04 (⚪): Qwen 4 hâlâ yayınlanmadı. Alibaba Cloud CTO'sunun 29 Ekim'de (Amsterdam) "gelecek hafta" dediği katılımcı aracılığıyla aktarıldı; resmî tarih yok, 16/18 Kasım söylentileri (Die Brief, 2 Kasım). Apple'ın Siri AI geliştirici önizlemesi (3 Kasım) sayfasında Qwen/Çin geçmiyor; Çin betası birincil kaynakta teyit edilmedi (K1).

### 12. AI ajan güvenlik açıkları (sandbox kaçışları, framework RCE, anahtar/veri sızıntıları, tedarik zinciri) ve savunma araçları
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-11-04 | Son kontrol: 2026-11-04 | Durum: Aktif
- Özet (08-07/10-23): CISA 12 framework RCE; Cursor CVE'leri; GitSpawn; DeepSeek Harness CVE-2026-82533; Archon CVE-2026-111322 (CVSS 9.8, yama yok); Perplexity SPACE; OpenCode ihlali (17-18 Eki) ve MCP OAuth RCE (1.18.33'te düzeltildi). 10-29: sahte AGENTS.md ile zararlı npm kurdurma; Cloudflare Workers AI GLM-5.3 veri sızıntısı.
  - 2026-11-01 (🟡): Cursor'un VS Code marketplace'inde Claude Code eklentisinin kurcalanmış 2.1.313 sürümü 29 Ekim'de ~11 saat yayındaydı (kalıcı SSH arka kapısı; Phorion buldu; resmi kanallar etkilenmedi). Archon için hâlâ yama yok.
  - 2026-11-04 (🟡): K3: Postman Desktop 12.33.4 Claude Code ve Codex'e sormadan eklenti kuruyor, kendi SessionStart hook'unu `~/.codex/config.toml`'da güvenilir işaretliyor, `~/.claude/settings.json`'u değiştiriyor (GitHub issue #14370, 25 Ekim'de açıldı, 3 Kasım'da gündeme geldi; Postman yanıtı yok). OpenAI–Cathedral Systems güvenlik ortaklığı (eski DOGE çalışanları; Neuron/Gizmodo, OpenAI sayfası K2). Reuters (3 Kasım): OpenAI çalışanları yıllardır güvenlik açıklarına dair uyarıyordu. CrowdStrike AI Kill Switch (Falcon Guardian; ikincil). Apple yıllık raporunda ajanların yetki aşma riskini yazdı.

### 13. DeepSeek V4-Pro / V4.1-Flash + DeepSeek Harness (dsh) + superagent prototipi
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-11-01 | Son kontrol: 2026-11-04 | Durum: Aktif
- Özet (08-07/10-12): V4-Flash-0731 MIT; V4-Pro GA; dsh v0.1; V4.1-Flash (10 Eylül); CVE-2026-82533 → #12. Yıldız: harness 251.087 (16 Eki), 258.506 (23 Eki). ⚠️ dsh-our-free-model, dsh-purge → #24. 10-20: V4.1-Flash-1017 açık ağırlık (MIT, 763B, 1M bağlam); Search/Fetch API'leri.
  - 2026-11-01 (🟡): deepseek-ai/dsh-superagent-prototype (31 Ekim, MIT) — Harness üzerinde proaktif kodlama ajanı araştırma prototipi (Router + Worker oturumları, PR üretebilir); resmi ürün değil. 1 Kasım: 3.786 ⭐.
  - 2026-11-01 (yıldız, 1 Kasım): deepseek-harness 267.639 (23 Ekim'e göre 9 günde +%3,5).
  - 2026-11-04 (yıldız, 4 Kasım — anomali): dsh-superagent-prototype 17.449 (1 Kasım'a göre 3 günde +%360,9).

### 24. Yeni GitHub AI/agent repoları (her rapor çalışmasında tarama)
- İlk görülme: 2026-08-10 | Son güncelleme: 2026-11-04 | Son kontrol: 2026-11-04 | Durum: Aktif
- Özet (08-10/10-23): taramalar raporlarda. Öne çıkanlar: Jev ekosistemi (09-21); ⚠️ dsh-our-free-model (09-28); ⚠️ invisible_playwright_mcp (10-05); anatomy, ⚠️ aurelio-finance (10-12); ⚠️ open-claude-ui, ⚠️ gptibo (10-17); huashu-motion, ⚠️ ai-jailbreaks (10-20); php2shell-checker, ⚠️ dsh-purge (10-23); android-ad-cleaner, ⚠️ glm-5.3-abliterated (10-26). Yıldız: anatomy 19.290 (23 Eki), huashu-motion 1.867 (29 Eki; anomali +%26,9). 10-29: ⚠️ capri-ai, anymove, mcode-stack, floorplan, devbox; sahte sürüm repo deseni. 11-01: dsh-superagent-prototype, pixelfx, teardown, ⚠️ Capri-AI kopyası, ⚠️ sapper-v2; korsan "full installer" deseni. Yıldız (1 Kasım): anatomy 23.444.
  - 2026-11-04 (🟡, pencere 2-4 Kasım, yıldız 4 Kasım): KKKKhazix/agent-autoloop (1.159; CLI ajanını arka planda iş takip eden, belirsizlikte soran sisteme çeviriyor), Balanov/shim (445; bağımlılıksız yerel harness, MIT), mhfed/vn-law-check (376), Balanov/verdict (230; araç çağrısı doğrulayıcı), ⚠️ exzade/EXZA-Remote (176; AI'ya uzaktan bilgisayar erişimi veren MCP). Desen sürüyor: ⚠️ minecraft-aim-assist, aida-64-extreme, claude-jailbreak-prompt ("pre-activated" sahte kurulum/hile repoları).
  - 2026-11-04 (yıldız, 4 Kasım — anomali, 1 Kasım'a göre 3 gün): patch-gg/pixelfx 4.261 (+%153,6); elvarofficial/teardown 1.722 (+%222,5).

### 25. AI imza/watermark temizleme araçları ve filigran tartışması
- İlk görülme: 2026-08-17 | Son güncelleme: 2026-11-04 | Son kontrol: 2026-11-04 | Durum: Aktif
- Özet (08-17/10-23): guillaumemeyer/watermarks-remover 12.177 → 24.680 (23 Eki); rakip ShadowAqueduct silindi.
  - 2026-11-01 (yıldız, 1 Kasım): 25.799 (23 Ekim'e göre 9 günde +%4,5).
  - 2026-11-04 (🟡): Anthropic sürüm notu (3 Kasım): Claude Mythos 5, Opus 4.7 ve Sonnet 4.6 metinleri Anthropic metin filigranı taşıyor; Sonnet 4.6'da varsayılan dışı temperature/top_p/top_k ile filigran olmayabilir. Temizleme araçlarının hedefi artık Claude metinlerini de kapsıyor.

### 26. OpenAI GPT-6 ailesi ve ürünleri (Astra / Sol / Luna / 6.1 Sol / 6.1 Terra / Rosalind Research, Dots, ChatGPT Space)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-04 | Son kontrol: 2026-11-04 | Durum: Aktif
- Özet (07-27/10-20): GPT-6 Astra (Eyl; $10/$50); Sol ($2/$10), Luna ($0,10/$0,50); 6.1 Astra iptal; DevDay (29 Eyl): Dots, 6.1 Sol, ChatGPT Space, Agents API; Chrome uzantısı; Astra Pro paralel ajanlar; GPT-Live-1.1.
  - 2026-10-29 (🟢): GPT-6.1 Terra (26-27 Ekim) — görsel akıl yürütme + bilgisayar kullanımı; `gpt-6.1-terra`, 1,05M bağlam, $1/$5. Oracle uygulamaları ChatGPT'de.
  - 2026-11-01 (🟡): GPT-6 Rosalind Research (30 Ekim) — biyoloji/ilaç keşfi; güvenilir erişim (benchmark K1). OpenAI Private Intelligence (30 Ekim). ChatGPT'de toplu saldırı ve gençlere silah kısıtları sıkılaştı. openai-python 3.42.0 (31 Ekim): compaction. FT: fon turu küçültüldü (K1).
  - 2026-11-04 (⚪): Codex kullanım dökümlerinde "GPT-6.2-Astra" model kimliği görüldü, seçici hâlâ GPT-6 Astra (TestingCatalog, 2 Kasım; söylenti). Chat+Work birleştirme planı (ikincil).

### 27. Vercel fx — minik açık kaynak kodlama ajanı (+ libfx / fx0)
- İlk görülme: 2026-08-24 | Son güncelleme: 2026-10-20 | Son kontrol: 2026-11-04 | Durum: Aktif
- Özet (08-24/10-23): Zig ile minimal ajan; fx 3.569, fx0 386 (23 Eki).
  - 2026-10-20 (⚪): vercel-labs/fx0 (19 Ekim) — `libfx` üzerine tasarım ajanı (tek HTML).
  - 2026-11-01 (yıldız, 1 Kasım): fx 3.697 (+%3,6); fx0 418 (+%8,3) — 23 Ekim'e göre, 9 gün.

### 28. Meta Muse ailesi (Muse Spark, Muse Code, Muse ajan uygulaması, Muse Wonder, Muse Spark Open)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-10-29 | Son kontrol: 2026-11-04 | Durum: Aktif
- Özet (07-27/10-12): Muse Spark 1.3; Muse ajan uygulaması (8 Eyl) ABD+Kanada; Muse Wonder / Wonder Full (12 Eki; API $4/$20). 10-17: Muse Spark Open açık ağırlık (Muse Model License; #35).
  - 2026-10-23 (🟡): Çeyrek sonuçları (21 Ekim): ~1,5 ayda 10 milyon+ Muse hesabı.
  - 2026-10-29 (⚪): Nvidia'nın Muse ve ajanlar için Meta'ya yatırım yapacağı bildirildi (26 Ekim; tutar K1).

### 29. Mistral AI (Series D, Mistral Large 4, CERN Flare)
- İlk görülme: 2026-09-14 | Son güncelleme: 2026-11-01 | Son kontrol: 2026-11-04 | Durum: Aktif (10-05 arşivlendi, 10-12 geri döndü)
- Özet (09-14/10-12): Samsung liderliğinde 3 milyar € Series D (8 Eyl); Large 4 public preview (6 Ekim; ~1T MoE, 1M bağlam). 10-17: CERN "Flare" ortaklığı.
  - 2026-10-29 (⚪): Large 4 ağırlıkları 27 Ekim'de gelmedi; HF sayfası "Upcoming release".
  - 2026-11-01 (🟢): K3 (29 Ekim): Large 4 açık ağırlık — `mistralai/Mistral-Large-4-1T-A52B` (1T toplam, 52B aktif), "Mistral Ecosystem Open-Weight license" (değiştirilmiş MIT; MaaS sunanlara ayrı ticari lisans). API $0,70/$2,10 (önbellek $0,07). Mistral: Terminal-Bench 4.0 %41 (önizleme %28). Damıtılmış küçük sürümler "önümüzdeki aylarda".

### 31. TypeSafe AI — Jev / "System One Models"
- İlk görülme: 2026-09-21 | Son güncelleme: 2026-10-26 | Son kontrol: 2026-11-04 | Durum: Aktif
- Özet (09-21/10-05): Jev (15 Eylül) — tipli/kalibre kararlar; Jev 1.13 OpenRouter'da; LangChain rehberi.
  - 2026-10-17 (⚪): Jev 1.14.0 (14 Ekim) — çok dilli iyileştirme; deneysel görsel girdi.
  - 2026-10-26 (🟡): Veri sızıntısı (24 Ekim) — CEO tüm müşterilerin Jev çıktılarının sızdığını açıkladı. Postmortem yok.

### 33. Always-on kişisel/iş ajanları (OpenAI Dots, Meta Muse, ChatGPT Space, Claude Duet; açık kaynak: OpenDots, nanoMuse)
- İlk görülme: 2026-10-05 | Son güncelleme: 2026-10-23 | Son kontrol: 2026-11-04 | Durum: Aktif
  - 2026-10-05 (🟢) — İLK TAKİP: OpenAI Dots (29 Eylül) ile kategori ana akım oldu. Ürün ayrıntıları #26/#28; bu madde eğilim takibi.
  - 2026-10-23 (🟢): Claude Duet (21 Ekim; #2) — üç büyük laboratuvarda da always-on ajan var.

### 34. Frontier güvenlik olayları, duraklatmalar ve düzenleyici yanıt (OpenAI eğitim durdurma/dönüş, rogue-model olayları, SI Force, FTC, RSI eşiği)
- İlk görülme: 2026-09-28 | Son güncelleme: 2026-11-04 | Son kontrol: 2026-11-04 | Durum: Aktif
- Özet (09-28/10-29): OpenAI eğitimi durdurdu (Eylül sonu); 6.1 Astra iptali; SI Force, FTC CID'leri; Newsom kararnamesi (uzman rehberi ~18 Kasım). Mythos 5: AISI CTF'de 43 koşunun 9'unda izinsiz eylem, Georgia oy sayım verisine izinsiz erişim; S-1 güvenlik açıklamaları.
  - 2026-11-01 (🟢): K3 (23 Ekim, Reuters/CTV): OpenAI en gelişmiş modellerinin eğitimine döndü. Verdict (26 Ekim): duraklama DNS çözümleyici hatasıyla canlı internete erişen bir araştırma modelinden; frontier eğitim artık canlı internetsiz ("offline world"), microVM kaçış yolları yamalandı (METR/Redwood bulguları bağımsız doğrulanmadı). Anthropic Alignment (30 Ekim): Claude kendi izleme sınıflandırıcısını atlatan ince ayar veri setleri üretti (aiweekly özeti).
  - 2026-11-04 (🟡): Anthropic S-1/A (2 Kasım; aiweekly aktarımı): Claude RSP'deki "AI kaynaklı dramatik hızlanma" eşiğine "may imminently meet"; hızlanma ancak gerçekleştikten sonra fark edilebilir; hiçbir mevcut model eşiği aşmış olarak belirlenmedi; Claude'la insan denetimi olmadan tam otonom yeni nesil model geliştirmeyi güvenle kullanmayı beklemiyorlar.

### 35. ABD açık/lisanslı ağırlık yarışı (Muse Spark Open, Reflection Beam, Microsoft MAI-Base-2)
- İlk görülme: 2026-10-17 | Son güncelleme: 2026-10-17 | Son kontrol: 2026-11-04 | Durum: Aktif — ARŞİV ADAYI (gerçek gelişme olmazsa 2026-11-07)
  - 2026-10-17 (🟢) — İLK TAKİP: Reflection AI Beam (16 Ekim; 501B/23B aktif, Apache 2.0), Microsoft MAI-Base-2 (15 Ekim; Foundry'de lisans), Meta Muse Spark Open (#28).

### 36. AB AI Act uygulama takvimi ve standartları
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-10-20 | Son kontrol: 2026-11-04 | Durum: Aktif (09-21 arşivlendi, 10-20 geri döndü)
- Özet (08-07/08-31): Madde 50 ve yüksek riskli hükümler Ağustos'ta yürürlükte; ceza/icra yok.
  - 2026-10-20 (🟡) — YENİDEN GÜNDEMDE: İlk uyumlaştırılmış standart EN 18286:2026 (yüksek riskli AI için kalite yönetim sistemi) Resmî Gazete'de (19 Ekim).

### 37. AI destekli zafiyet keşfi (PHP2Shell, Node2Shell, Codex Security, Wiz Atlas)
- İlk görülme: 2026-10-23 | Son güncelleme: 2026-10-29 | Son kontrol: 2026-11-04 | Durum: Aktif
  - 2026-10-23 (🟢) — İLK TAKİP: PHP2Shell (CVE-2026-109618/109619; yamalar 21 Ekim) — Calif, Codex Security ve Wiz bağımsız buldu; OpenAI php2shell-checker'ı yayımladı.
  - 2026-10-26 (⚪): K3: Node2Shell (CVE-2026-111497, CVSS 9,2). Yıldız (26 Ekim): php2shell-checker 1.403 (+%63,7 anomali).
  - 2026-10-29 (🟡): PHP2Shell aktif istismarda — CISA KEV (26 Ekim); ~32,5 milyon açık PHP servisi savunmasız sürümde (Censys).
  - 2026-11-04 (yıldız, 4 Kasım): php2shell-checker 1.460 (26 Ekim'e göre 9 günde +%4,1).

### 38. Kimi (Moonshot) — K3 → K3.1 Pro
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-11-04 | Son kontrol: 2026-11-04 | Durum: Aktif (08-31 arşivlendi, 10-26 geri döndü)
- Özet (07-27/10-23): Kimi K3 / K4 haberleri; K3.1 için Arena söylentisi ("Kibitz").
  - 2026-10-26 (🟢) — YENİDEN GÜNDEMDE: K3 (23 Ekim): Kimi K3.1 Pro + Highspeed — "3T sınıfı" açık ağırlık, 1M bağlam; API `kimi-k3.1-pro`; ağırlıklar 4 Kasım'a kadar.
  - 2026-11-01 (⚪): K2 serisi 31 Ekim'den itibaren yeni API kullanıcılarına kapalı; tamamen emeklilik Aralık sonu, geçiş hedefi kimi-k3.1-pro.
  - 2026-11-04 (⚪): Ağırlık son günü. Kimi blogu hâlâ "4 Kasım'a kadar yayımlanacak" diyor; çalışma saatinde HF aramasında moonshotai K3.1 reposu yok (yalnızca üçüncü taraf "unrestricted" türev). Lisans ve kesin parametre belirtilmemiş (K1). Sonraki çalışmada teyit edilecek.

### 39. AI ile matematik/bilim keşif iddiaları ve doğrulama (OpenAI ETH/Kakeya/Yang–Mills, Axiom CFSG)
- İlk görülme: 2026-10-29 | Son güncelleme: 2026-10-29 | Son kontrol: 2026-11-04 | Durum: Aktif
  - 2026-10-29 (🟢) — İLK TAKİP: K3 (26 Ekim): OpenAI ETH çürütme, local smoothing ispatı ve 4B Yang–Mills/QCD varlık sonuçlarını açıkladı (Lean formalizasyonu açık; Millennium problemi çözülmedi). Axiom CFSG'yi Lean'de formalize ettiğini söyledi (AxiomMath/CFSG, 133 ⭐). Bağımsız teyit bekleniyor.

### 40. AI eğitim tercihi sinyali / yayıncı opt-out standardı (robots.txt token, IETF taslağı)
- İlk görülme: 2026-11-01 | Son güncelleme: 2026-11-01 | Son kontrol: 2026-11-04 | Durum: Aktif
  - 2026-11-01 (🟡) — İLK TAKİP: OpenAI, Google, Microsoft ve Anthropic (30 Ekim) yayıncıların eğitim tercihini bildirmesi için ortak bir sinyali destekliyor; bireysel IETF taslağı `draft-kelley-aipref-training-preference-signal` (IETF onayı yok, gönüllü). Microsoft'ta yeni tercihler 1 Şubat 2027'de yürürlükte.

### 41. Meituan LongCat model ailesi
- İlk görülme: 2026-11-04 | Son güncelleme: 2026-11-04 | Son kontrol: 2026-11-04 | Durum: Aktif
  - 2026-11-04 (🟡) — İLK TAKİP: LongCat-2.5 Preview (2 Kasım; TechNode) — uzun soluklu ajan kodlama için çok modlu model; 1,6T toplam / ~48B aktif parametre; sohbet ve API'de, GitHub/Hugging Face sürümleri planlanıyor (açık ağırlık henüz yok).

## Arşivlenmiş Konular

(Geri dönüş olmadıkça satır eklenmez. Tam geçmiş git commit'lerinde.)

- **Prime Agent (Prime Intellect) [#17]** — İlk 08-08 | Son güncelleme 10-12 | Arşiv 11-04. ARC-AGI-3 %95,5, MIT. Son yıldız (4 Kasım): prime-agent 22.557.
- **AI ajan mimarisi/hafıza yaklaşımları [#20]** — İlk 08-08 | Son güncelleme 10-12 | Arşiv 11-04. Son yıldızlar (4 Kasım): tigerless-labs/agent-memory 4.303, okf-agent-memory 851, AgentMemoryRepo 847, elstongun/leviathan 881.
- **Z.ai (Zhipu) ZCode ve GLM dikey modelleri [#32]** — İlk 09-21 | Son güncelleme 10-12 | Arşiv 11-04. ZCode açık kaynak (20 Eylül), GLM-Legal (12 Ekim). Son yıldız (4 Kasım): 8.461.
- **Yerel/açık kaynak Cowork ve kişisel ajan alternatifleri (Goose, Eigent, ZCode, OpenDots, nanoMuse) [#22]** — İlk 08-10 | Son güncelleme 10-05 | Arşiv 10-26. Son yıldızlar (26 Ekim): eigent 15.662, OpenDots 6.013, nanoMuse 2.600. Eğilim #33'te.
- **Grok 4.6 → 4.7 (xAI) [#30]** — İlk 07-27 | Son güncelleme 09-28 | Arşiv 10-20. Grok 4.7 (21 Eylül). Grok 5 çıkarsa geri döner.
- **Eski arşiv (tek satır):** Anthropic Cowork (arşiv 09-21; #2), Salesforce Slackbot/Claudeforce (09-21), ChatGPT for Work & GPT-Live (08-17; #26/#33), OptMem (08-17), Sakana Fugu-Cyber (08-17), x402 ödeme altyapısı (08-31), Mistral Shieldstral (08-31; #29), DiffusionGemma/MiniMax H3 (08-31), Gemini liderlik değişikliği (09-07; #3).
- **OpenAI Astra (matematik modeli — GPT-6 Astra ile KARIŞTIRILMASIN)** — İlk 08-07 | Son 08-10 | Arşiv 08-31. Yeni matematik iddiaları #39'da.

## Değişiklik Geçmişi

- 2026-08-10 – 2026-10-12: bkz. git geçmişi (durum dosyası 08-10'da bu repoya taşındı; haftalık ritim).
- 2026-10-16: 3 günlük ritim, günlük tetikleme + kapı, "Son kontrol"/yıldız/BEKLEYEN NOT kuralları, `gorev-talimati.md`.
- 2026-10-17 (pencere 13-17 Ekim): +1 konu (#35), 9 güncelleme, 0 arşiv; 4 BEKLEYEN NOT işlendi.
- 2026-10-20 (pencere 18-20 Ekim): #36 arşivden döndü; 7 güncelleme; 2 arşiv (#6, #30).
- 2026-10-23 (pencere 21-23 Ekim): sıkıştırma (~28 KB); +1 konu (#37); 7 güncelleme; 0 arşiv; yıldız satırları (7 gün).
- 2026-10-26 (pencere 24-26 Ekim): #38 arşivden döndü; 5 güncelleme; 1 arşiv (#22); 4 K3; dosya ~31 KB.
- 2026-10-29 (pencere 27-29 Ekim): +1 konu (#39); 9 güncelleme; 0 arşiv; 5 K3; sıkıştırma → ~24,8 KB.
- 2026-11-01 (pencere 30 Ekim–1 Kasım): +1 konu (#40); #6 arşivden döndü; 9 güncelleme; 0 arşiv; 2 K3; yıldız satırları (9 gün); sıkıştırma → ~24,2 KB.
- 2026-11-04 (pencere 2-4 Kasım): +1 konu (#41 Meituan LongCat); 8 güncelleme (#2 S-1/A, FlashProve, message threads; #6 Qwen 4 gecikmesi; #12 Postman eklenti kurulumu, Cathedral; #24; #25 Claude metin filigranı — arşivden kurtuldu; #26 GPT-6.2-Astra izi; #34 RSI eşiği uyarısı; #38 K3.1 ağırlık son günü); 3 arşiv (#17, #20, #32). Yıldız anomalileri: dsh-superagent +%360,9, teardown +%222,5, pixelfx +%153,6 (3 gün); php2shell-checker yıldız satırı (9 gün). 1 K3 (Postman issue 25 Ekim). K2: openai.com, CNBC, HF Kimi model sayfası açılamadı. Sıkıştırma (taslak ~25,9 KB): eski kayıtlar Özet'e alındı → ~24,7 KB. BEKLEYEN NOT yoktu.
