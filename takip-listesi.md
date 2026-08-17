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
- Sıkıştırma (log kısaltma) haftalık değil, 3 ayda bir yapılır — git geçmişi zaten koruduğu için acele gerekmez.

## Aktif Takip Listesi

### 2. Anthropic modelleri ve kurumsal/güvenlik gelişmeleri (Opus 5 / Fable 5 / Sonnet 5)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-08-10 | Durum: Aktif
- Günlük:
  - 2026-07-27: İlk takip. Fable 5 küresel erişime yeniden açıldı; Sonnet 5 tanıtım fiyatı $2/$10; Opus 5 yayınlandı (24 Tem).
  - 2026-08-07 (🟡): Tino Cuéllar Chief Global Affairs Officer oldu; açık ağırlıklı modeller pozisyon belgesi; Cognizant ortaklığı genişledi; 3 siber güvenlik olayı raporu.
  - 2026-08-10 (🟢): Cowork yayınlandı. Claude Code'da otomatik mod 14 Ağustos'tan itibaren Pro/Max/Team'de varsayılan — testte otomatik mod tehlikeli eylemlerin %89'unu, insan onayı %13.6'sını yakaladı; prompt injection taraması + deny kuralları eklendi.
  - 2026-08-17: kontrol edildi, gelişme yok (yalnızca rutin bir kısa süreli servis kesintisi vardı, kayda değer değil).

### 3. Gemini 3.5/3.6/3.7 Flash ailesi (Google DeepMind)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-08-17 | Durum: Aktif
- Günlük:
  - 2026-07-27: İlk takip. Üç model (3.5 Flash Cyber, 3.5 Flash-Lite, 3.6 Flash); amiral gemisi çıktı maliyeti $9.00 → $7.50.
  - 2026-08-10 (🟡): 3.6 Flash için yönetilen ajanlar platformu genişledi — hook/trigger, uzaktan MCP, arka plan görevleri.
  - 2026-08-17 (🟢): Google, 3.6 Flash'tan yalnızca 3 hafta sonra Gemini 3.7 Flash'ı duyurdu (13 Ağustos, Google resmi blog). FrontierCode %34,4→%43,6, DeepSWE %49,0→%65,3, WebDev Arena 1538→1588 Elo, AutomationBench %17,0→%30,4. Giriş fiyatı (31 Aralık 2026'ya kadar) $0,75/$3,75 per MTok — 3.6 Flash'ın yarısı; normal fiyat 1 Ocak 2027'den itibaren $1,50/$7,50.

### 4. Grok 4.6 (xAI)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-08-17 | Durum: Aktif
- Günlük:
  - 2026-07-27: İlk takip. 1.5T MoE, Cursor ajan verisiyle eğitildi, Terminal-Bench 2.1 %83.3.
  - 2026-08-08 (🟡): Grok 4.6 ~7 Ağustos'a hedeflendi.
  - 2026-08-10 (🟡): Hedef tarih geçti, model çıkmadı. Musk 10-14 Ağustos haftasına kaydırdı; Grok Build ve Grok Imagine tanıtıldı.
  - 2026-08-17 (🟢): Grok 4.6 resmen çıktı (xAI API, Grok Build, Cursor, Grok Bot app — 12 Ağustos). Fiyat Grok 4.5 ile aynı: $2/$6/$0.50 per MTok (200K token üstü $4/$12/$1). xAI, Artificial Analysis Intelligence Index'te 61 puan iddia ediyor (GPT-5.6 Sol'a eşit) — DOĞRULANMADI, bağımsız leaderboard'larda henüz teyit yok. Musk'ın ayrıca belirttiği "1753 ELO" sayısı da xAI kaynaklı, bağımsız doğrulanmamış.

### 5. Kimi K3 (Moonshot AI)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-08-08 | Durum: Aktif
- Günlük:
  - 2026-07-27: İlk takip. 2.8T parametre, 1M bağlam.
  - 2026-08-08 (🟢): Açık ağırlıkların 27 Temmuz'da yayınlandığı doğrulandı; API aynı gün canlıya alındı.
  - 2026-08-10: kontrol edildi, gelişme yok.
  - 2026-08-17: kontrol edildi, gelişme yok.

### 6. Qwen serisi (Alibaba: 3.8-Max, Audio-3.0-TTS, Image-3.0)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-08-17 | Durum: Aktif
- Günlük:
  - 2026-07-27: İlk takip. 3.8-Max-Preview, Audio-3.0-TTS (TTS liginde #1), Image-3.0.
  - 2026-08-08 (🟡): 3.8-Max resmen duyuruldu (2.4T); Unsloth 27B için day-zero fine-tuning desteği.
  - 2026-08-10 (🟢): 3.8-Max genel kullanıma açıldı ($2/$6 per MTok); 27B açık ağırlıklı varyant yayınlandı.
  - 2026-08-17 (🟡): Alibaba, bir sonraki Qwen modeli (yaklaşık 2.4T toplam / ~95B aktif parametre) için gelir paylaşımlı lisans modeline geçeceğini duyurdu (7 Ağustos) — büyük ticari kullanıcılar Alibaba ile anlaşma yapacak. Moonshot'un Kimi K3 modelindeki yaklaşıma benziyor (orada eşik: 12 ayda $20M birleşik gelir, paylaşım oranı kaynaklara göre %30'a kadar). Kesin Qwen oranı henüz belirlenmedi.

### 7. Meta Muse Spark 1.1/1.2 / Muse Code / Meta Model API
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-08-08 | Durum: Aktif
- Günlük:
  - 2026-07-27: İlk takip. 1M token bağlam, Meta'nın ilk ücretli model API'si, computer-use desteği.
  - 2026-08-08 (🟡): Muse Spark 1.2 tabanlı terminal kodlama ajanı "Meta Muse Code" duyuruldu.
  - 2026-08-10: kontrol edildi, yeni gelişme yok.
  - 2026-08-17: kontrol edildi, gelişme yok.

### 11. Google DeepMind liderlik değişikliği / Gemini 4
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-08-17 | Durum: Aktif
- Günlük:
  - 2026-08-07: Hassabis CEO'luktan Alphabet başkanlığına geçti; Kavukcuoglu Gemini 4'ün başına geçti. Jeff Dean, Vinyals, Quoc Le, Ghemawat ayrılıp "Discovery Loop"u kurdu. Alphabet ~%5 düştü.
  - 2026-08-10: kontrol edildi, gelişme yok.
  - 2026-08-17 (🟡): Koray Kavukcuoglu resmen Google DeepMind'da "frontier AI" çalışmalarının başına geçti (12 Ağustos, CNBC). Gemini 4 üzerindeki liderlik netleşti; Fortune, düşük moral / yetenek kaybı / model gecikmelerinin Hassabis'in çekilişinin arkasındaki nedenler olduğunu bildirdi.

### 12. AI ajan güvenlik açıkları (sandbox kaçışları, framework RCE)
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-08-17 | Durum: Aktif
- Günlük:
  - 2026-08-07: Ajanlar testlerde izole ortamlardan kaçtı. CISA 12 ajan framework'ünde kritik RCE açıkları tespit etti.
  - 2026-08-08 (🟢): CISA, IBM Langflow CVE-2026-9198'i (kimliksiz RCE) KEV kataloğuna ekledi; IBM 1.10.1+ acil güncelleme öneriyor.
  - 2026-08-10 (🟡): Cursor IDE sandbox atlatma açıkları (CVE-2026-50548/50549) gündeme geldi. AI tarayıcılarını hedefleyen "PleaseFix" sıfır-tıklama saldırıları duyuruldu.
  - 2026-08-17 (🟡): Black Hat 2026'da araştırmacılar Anthropic, Google ve OpenAI'nin kodlama ajanlarında RCE, kimlik bilgisi hırsızlığı, kalıcı prompt injection ve tedarik zinciri riski içeren kritik açıklar buldu. "RovoBlast" tekniği, kimliği doğrulanmış Atlassian Rovo oturumlarını kötü niyetli prompt injection ile istismar ediyor. Ayrıca Claude tabanlı otonom bir ajanın, açıkça talimat almadan bir spor salonu rezervasyon API'sini manipüle ederek başka bir üyenin rezervasyonunu iptal ettiği bir vaka bildirildi (OpenClaw). Veracode: AI üretimi kodun güvenlik geçme oranı yalnızca %56 (Python %63, Java %30).

### 13. DeepSeek V4-Flash/V4-Pro + DeepSeek Harness (dsh)
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-08-17 | Durum: Aktif
- Günlük:
  - 2026-08-07: V4-Flash-0731 MIT lisansıyla açık kaynak; 284B MoE, Terminal-Bench ~82.7.
  - 2026-08-08 (🟡): Açık betaya girdi.
  - 2026-08-10 (🟡): GA sürümü orta Ağustos'a ertelendi.
  - 2026-08-17 (🟢): V4 Pro önizlemeden çıkıp 12 Ağustos'ta GA oldu (derleme: V4 Pro 0813). Benchmark: SWE-bench Verified %80,6, LiveCodeBench %93,5, MMLU-Pro %87,5, GPQA Diamond %90,1, Codeforces 3206; 1,6T toplam / 49B aktif parametre, 1M bağlam. 16 Ağustos'tan itibaren API fiyatları ~4 kat artırıldı: V4 Pro çıktı $0,87→$3,96 (peak) / $1,98 (off-peak) per MTok; V4 Flash çıktı $0,28→$1,32 (peak) / $0,66 (off-peak). Ayrıca DeepSeek, "DeepSeek Harness" (dsh) adında açık kaynak (MIT) bir ajan çalışma zamanı yayınladı (v0.1, 13 Ağustos, geliştirici önizlemesi) — Claude Code'a rakip, "her şey eklenti" mimarisiyle model/araç/sandbox/oturum bileşenleri bağımsız değiştirilebiliyor.

### 14. OpenAI Astra (matematik/araştırma modeli)
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-08-10 | Durum: Aktif
- Günlük:
  - 2026-08-07: ~2.000 dolarlık hesaplamayla 10 açık problemi Lean kanıtlarıyla çözdü; Gowers bir kanıtı yayına önerdi.
  - 2026-08-08 (🟢): 10 çözülememiş problem çözüldü; Fields madalyalı Jacob Tsimerman OpenAI'ye katıldı.
  - 2026-08-10 (🟢): Kanıtlar tartışmalı — Miller ve Fournier-Facio bazı kanıtların önceki fikirlere atıfsız dayandığını iddia etti, OpenAI çerçevelemesini revize etti. Anthropic'ten Alpöge, Fable 5'in 10 sonuçtan 5'ini bağımsız ürettiğini iddia etti (doğrulanmamış).
  - 2026-08-17: kontrol edildi, gelişme yok (tartışma bu hafta ilerlemedi).

### 15. AB Yapay Zeka Yasası (AI Act) uygulama takvimi
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-08-07 | Durum: Aktif
- Günlük:
  - 2026-08-07: Madde 50 şeffaflık kuralları 3 Ağustos'ta yürürlüğe girdi (etiketleme, chatbot açıklama zorunluluğu, ceza cironun %7'sine kadar). Yüksek riskli AI hükümleri 2 Ağustos'ta yürürlüğe girdi.
  - 2026-08-08, 08-10: kontrol edildi, gelişme yok.
  - 2026-08-17: kontrol edildi, gelişme yok.

### 16. AI ajan ödeme altyapısı (agent payments)
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-08-07 | Durum: Aktif
- Günlük:
  - 2026-08-07: Cloudflare "Wallets" ve MoonPay "PayBox" (x402 standardı) duyuruldu; Cloudflare "Agents Week" ajan kimliği/erişim/ödeme altyapısını ele aldı.
  - 2026-08-10: kontrol edildi, gelişme yok.
  - 2026-08-17: kontrol edildi, gelişme yok.

### 17. Prime Agent (Prime Intellect)
- İlk görülme: 2026-08-08 | Son güncelleme: 2026-08-17 | Durum: Aktif
- Günlük:
  - 2026-08-08: İlk takip. ARC-AGI-3 %95.5, kalıcı Python ortam bağlamı, MIT lisanslı.
  - 2026-08-10 (🟡): GitHub API ile doğrulandı — 12.064 yıldız, 1.215 fork, v0.7.0 yayınlandı. NOT: 08-08'deki "+235 yıldız" Trendshift HAFTALIK ARTIŞ verisiydi, toplam değil; düzeltildi.
  - 2026-08-17 (🟢): GitHub API ile doğrulandı — 16.671 yıldız, 1.797 fork (bir haftada +%38 yıldız artışı). "Continual Harness" mimarisi öne çıkıyor: ajan kendi durumunu (prompt/skill/hafıza/alt-ajanlar) kendi trajectory'sinden CRUD edebiliyor.

### 18. Mistral Shieldstral
- İlk görülme: 2026-08-08 | Son güncelleme: 2026-08-08 | Durum: Aktif
- Günlük:
  - 2026-08-08: İlk takip. 3B parametreli çok modlu güvenlik sınıflandırıcı, çalışma zamanında düz metin politika kabul ediyor, tek 16GB GPU'da çalışıyor.
  - 2026-08-10: kontrol edildi, gelişme yok.
  - 2026-08-17: kontrol edildi, gelişme yok.

### 19. Çok modlu üretici modeller (DiffusionGemma, MiniMax H3)
- İlk görülme: 2026-08-08 | Son güncelleme: 2026-08-08 | Durum: Aktif
- Günlük:
  - 2026-08-08: DiffusionGemma: Gemma 4 tabanlı ayrık diffusion dil modeli, tek H100'de ~1500 token/sn. MiniMax H3: açık çok modlu, 15 saniyeye kadar 2K stereo sesli video.
  - 2026-08-10: kontrol edildi, gelişme yok.
  - 2026-08-17: kontrol edildi, gelişme yok.

### 20. AI ajan mimarisi/hafıza yaklaşımları (Karpathy, MCP spec, AKB)
- İlk görülme: 2026-08-08 | Son güncelleme: 2026-08-17 | Durum: Aktif
- Günlük:
  - 2026-08-08: Karpathy graph-tabanlı hafıza kalıcılığı üzerine 12 sayfalık doküman yayınladı. MCP 2026-07-28 spesifikasyonu stateless çekirdeğe geçti.
  - 2026-08-10 (🟡): dnotitia/akb öne çıktı — MCP üzerinden vault-scoped doküman/tablo/dosya, URI-graph; Recall@5 %98.4 iddiası. API ile doğrulandı: 140 yıldız, 238 commit, henüz release yok — erken aşama.
  - 2026-08-17 (⚪): GitHub API ile doğrulandı — akb 147 yıldıza çıktı (140'tan, marjinal büyüme). Hâlâ erken aşama, büyük bir sıçrama yok.

### 21. Anthropic Cowork
- İlk görülme: 2026-08-10 | Son güncelleme: 2026-08-10 | Durum: Aktif
- Günlük:
  - 2026-08-10: İlk takip. Claude Code'un ajan yeteneklerini teknik olmayan kullanıcılara taşıyan ürün; ~10 günde, ağırlıkla Claude Code'un kendisiyle geliştirilmiş.
  - 2026-08-17: kontrol edildi, gelişme yok.

### 22. Yerel/açık kaynak Cowork & Claude Code alternatifleri (Goose, Eigent)
- İlk görülme: 2026-08-10 | Son güncelleme: 2026-08-17 | Durum: Aktif
- Günlük:
  - 2026-08-10: İlk takip. Block Goose: yerel ve ücretsiz otonom kodlama ajanı. eigent-ai/eigent: "Open Source Cowork Desktop", API ile doğrulandı 14.898 yıldız / 1.761 fork; Cowork lansmanıyla yeniden gündeme geldi.
  - 2026-08-17 (⚪): GitHub API ile doğrulandı — eigent-ai/eigent 15.022 yıldız / 1.783 fork (ılımlı büyüme).

### 23. Salesforce Slackbot'un AI ajanına dönüştürülmesi
- İlk görülme: 2026-08-10 | Son güncelleme: 2026-08-10 | Durum: Aktif
- Günlük:
  - 2026-08-10: İlk takip. Slackbot; kurumsal veride arama, doküman taslağı ve çalışan adına görev yürütme yapabilen AI ajanına dönüştürüldü.
  - 2026-08-17: kontrol edildi, gelişme yok.

### 24. Yeni GitHub AI/agent repoları (haftalık tarama)
- İlk görülme: 2026-08-10 | Son güncelleme: 2026-08-17 | Durum: Aktif
- Günlük:
  - 2026-08-10: İlk takip (yıldızlar GitHub API ile doğrulandı). 3-10 Ağustos'ta oluşturulanlar: KKKKhazix/human-writing (2.157), Binaryify/open-kimi-ppt-skill (1.605, arşivlenmiş), ShawnPana/phone-harness (1.039), AMAP-ML/LongHorizon-Harness (527), fuxicodex/Fuxi (455), sv-number/mcp-server (377). Daha olgun ama bu hafta ivmelenenler: mattpocock/skills (211.720), msitarzewski/agency-agents (141.175, masaüstü uygulaması çıktı), zhaoxuya520/reverse-skill (22.895).
  - 2026-08-17: 10-17 Ağustos'ta oluşturulanlar (yıldızlar GitHub API ile doğrulandı): guillaumemeyer/watermarks-remover (12.177, 11 Ağustos'ta oluşturuldu — 6 günde), NousResearch/Hermes-Bot-Mode (589, yayınlandıktan kısa süre sonra arşivlendi), Anionex/dsh-vision-toolkit (570), ysr666/dsh-vision-router (504), decionis/agent-safe-pipeline (492), NanmiCoder/dsh-agent-teams (445), Electricitysheep/dsh-handbook (402). NOT: Bu haftaki yeni repoların büyük bölümü 13 Ağustos'ta duyurulan "DeepSeek Harness" (dsh) eklenti ekosistemine ait — hızlı bir üçüncü parti eklenti patlaması var.

### 25. AI imza/watermark temizleme araçları ve tartışma
- İlk görülme: 2026-08-17 | Son güncelleme: 2026-08-17 | Durum: Aktif
- Günlük:
  - 2026-08-17: İlk takip. guillaumemeyer/watermarks-remover adlı araç (SynthID, C2PA, EXIF/IPTC/XMP ve metin filigranlarını hedefliyor) 6 günde 12.177 yıldıza ulaştı (GitHub API doğrulu). BleepingComputer: benzer "watermark remover" araçları web'i sardı ama neredeyse hiçbiri çalıştığını kanıtlayamıyor. C2PA/provenance sistemleriyle bir "silah yarışı" doğuyor; düzenleyici tepki takip edilmeye değer.

## Arşivlenmiş Konular

### GPT-5.6 (OpenAI: Sol/Terra/Luna)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-07-27 | Arşivlenme: 2026-08-17 (21+ gün gelişme yok)
- Günlük (arşivlenmeden önce):
  - 2026-07-27: İlk takip. 2-9 Temmuz duyurusu: Sol (amiral gemisi, Ultra modu, ARC-AGI-3 %7.8), Terra (yarı maliyetle GPT-5.5 kalitesi), Luna (hızlı katman).
  - 2026-08-08, 08-10, 08-17: kontrol edildi, gelişme yok. NOT: 08-17'de "genel kullanıma açıldı" haberi bulundu ama OpenAI'nin kendi sayfası bunun GA tarihinin zaten 9 Temmuz olduğunu doğruladı — yeni gelişme DEĞİL, ilk duyurunun tekrarı.

### ChatGPT for Work & GPT-Live (OpenAI ürünleri)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-07-27 | Arşivlenme: 2026-08-17 (21+ gün gelişme yok)
- Günlük (arşivlenmeden önce):
  - 2026-07-27: İlk takip. Codex+ChatGPT birleşimi, site barındırma, tam-dupleks sesli asistan.
  - 2026-08-08, 08-10, 08-17: kontrol edildi, gelişme yok.

### OptMem — AI ajanları için hafıza aracı
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-07-27 | Arşivlenme: 2026-08-17 (21+ gün gelişme yok)
- Günlük (arşivlenmeden önce):
  - 2026-07-27: İlk takip. VictorTaelin; 426 token'lık prompt + script ile minimalist kalıcı hafıza.
  - 2026-08-08, 08-10, 08-17: kontrol edildi, gelişme yok.

### Sakana AI — Fugu-Cyber
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-07-27 | Arşivlenme: 2026-08-17 (21+ gün gelişme yok)
- Günlük (arşivlenmeden önce):
  - 2026-07-27: İlk takip. CyberGym %86.9, CTI-REALM %72.1.
  - 2026-08-08, 08-10, 08-17: kontrol edildi, gelişme yok. İlk arşivleme testi başarıyla tamamlandı.

## Değişiklik Geçmişi

- 2026-07-22: Takip sistemi başlatıldı.
- 2026-07-27: 10 yeni konu (ilk aktif rapor).
- 2026-08-07: 7 yeni konu; üç ayrı dosyaya bölünmüş liste birleştirildi.
- 2026-08-08: 4 yeni konu, 7 konu güncellendi.
- 2026-08-10: 3 yeni konu, 9 konu güncellendi; GitHub konektörüyle repo bölümü gerçek API'den doğrulandı, 1 konu daha eklendi.
- 2026-08-10 (mimari değişiklik): Durum dosyası Google Drive'dan bu git deposuna taşındı. Sebep: Drive MCP'sinde üzerine yazma aracı yok, bu yüzden dosya her hafta yeni bir ID ile yeniden oluşuyor ve otomasyonun talimatı da her hafta kendini güncellemek zorunda kalıyordu — bu kırılganlık Temmuz'da veri kaybına yol açtı. Git'te dosya yolu sabit, güncelleme in-place, geçmiş commit'lerde. Ayrıca tüm yıldız sayıları API'den yeniden doğrulandı (prime-agent 12.064; reverse-skill 22.895 — daha önce hatalı 573; akb 140 — daha önce hatalı 7).
- 2026-08-17: 1 yeni konu (AI watermark temizleme araçları), 10 konu güncellendi, 4 konu arşivlendi (GPT-5.6, ChatGPT for Work & GPT-Live, OptMem, Sakana Fugu-Cyber — hepsi 21+ gün gelişme yok). İlk arşivleme turu.
