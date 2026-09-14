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
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-09-14 | Durum: Aktif
- Günlük (07-27/08-07 özet: Fable 5 küresel erişim, Sonnet 5 tanıtım fiyatı $2/$10, Opus 5 yayınlandı; Cuéllar CGAO oldu, açık ağırlık pozisyon belgesi, Cognizant ortaklığı):
  - 2026-08-10 (🟢): Cowork yayınlandı. Claude Code'da otomatik mod 14 Ağustos'tan itibaren Pro/Max/Team'de varsayılan — testte otomatik mod tehlikeli eylemlerin %89'unu, insan onayı %13.6'sını yakaladı; prompt injection taraması + deny kuralları eklendi.
  - 2026-08-17: kontrol edildi, gelişme yok (yalnızca rutin bir kısa süreli servis kesintisi vardı, kayda değer değil).
  - 2026-08-24 (🟡): Geriye dönük fark edilen gelişme — Anthropic 11 Ağustos'ta Claude'un tüm AI-üretimi çıktılarına (metin/ses/görsel/video) görünmez, makine-okunur watermark ekleyeceğini duyurdu. Gerekçe AB AI Act Madde 50(2) uyumu ama uygulama küresel; yeni ürünlerde 2 Ağustos'tan itibaren, eski modellerde 2 Aralık 2026'ya kadar tamamlanacak. Bu hafta (17-24 Ağustos) ayrıca yeni gelişme yok.
  - 2026-08-31: kontrol edildi, gelişme yok (bu haftaki büyük Anthropic haberleri — Cowork hafıza birleşmesi ve Salesforce ortaklığı — ayrı konu başlıkları altında işlendi, bkz. #21 ve #23).
  - 2026-09-07 (🟢): Anthropic, "Claude Commerce Agents" adında Apache-2.0 lisanslı bir referans blueprint'i açık kaynak yaptı (1-3 Eylül, resmi repo + PYMNTS/MarkTechPost haberleri). Perakende, seyahat, telekom ve eğlence dikeylerinde çalışan bir Alışveriş Ajanı (ürün arama/karşılaştırma/sepet) ve bir Satıcı Ajanı (envanter/fiyatlandırma/kampanya) içeriyor; Messages API, Agent SDK ve Managed Agents üzerinde çalışıyor. Güvenlik tasarımı fencing, provenance gate'leri, onay iş akışları ve hafıza doğrulamasını içeriyor. GitHub API ile doğrulandı: anthropics/commerce-agents — 1 haftadan kısa sürede 2.275 yıldız, 392 fork. Visa/Mastercard ile bağlantılı olduğu bildiriliyor (PYMNTS), fiyatlandırma açıklanmadı.
  - 2026-09-14 (🟡): Üç ayrı gelişme: (1) "Smart Reports" (beta) yayınlandı — Enterprise kullanıcılar için ekip kullanım deseni, maliyet, sürtünme noktaları ve tekrar kullanılabilir skill fırsatlarını analiz eden bir araç (10 Eylül; resmi Claude Yardım Merkezi release notes ile doğrulandı). (2) Anthropic Tehdit İstihbaratı ekibi "Detecting and countering misuse of AI: September 2026" raporunu yayınladı (10 Eylül, resmi anthropic.com/news) — 8 aylık dönemde tespit edilip durdurulan kötüye kullanım operasyonlarını detaylandırıyor. (3) Claude Code 2.1.270 (12 Eylül) uzun oturumlarda salt-okunur git komutlarının gereksiz yere izin istemesine yol açan bash regresyonunu düzeltti. GitHub API ile doğrulandı: anthropics/commerce-agents — 2.821 yıldız, 533 fork (2.275'ten, %24,0 haftalık artış).

### 3. Gemini 3.5/3.6/3.7/3.8 Flash ailesi (Google DeepMind)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-09-07 | Durum: Aktif
- Günlük (07-27 özet: 3.5 Flash Cyber/Lite, 3.6 Flash ilk takip, amiral gemisi çıktı maliyeti $9.00→$7.50):
  - 2026-08-10 (🟡): 3.6 Flash için yönetilen ajanlar platformu genişledi — hook/trigger, uzaktan MCP, arka plan görevleri.
  - 2026-08-17 (🟢): Google, 3.6 Flash'tan yalnızca 3 hafta sonra Gemini 3.7 Flash'ı duyurdu (13 Ağustos, Google resmi blog). FrontierCode %34,4→%43,6, DeepSWE %49,0→%65,3, WebDev Arena 1538→1588 Elo, AutomationBench %17,0→%30,4. Giriş fiyatı (31 Aralık 2026'ya kadar) $0,75/$3,75 per MTok — 3.6 Flash'ın yarısı; normal fiyat 1 Ocak 2027'den itibaren $1,50/$7,50.
  - 2026-08-24: kontrol edildi, gelişme yok (Gemini API resmi changelog'da 13 Ağustos'tan bu yana yeni girdi yok).
  - 2026-08-31: kontrol edildi, gelişme yok (Gemini API changelog'da hâlâ yeni girdi yok).
  - 2026-09-07 (🟢): Google, 3.7 Flash'tan yalnızca 3 hafta sonra Gemini 3.8 Flash'ı duyurdu (2 Eylül, 9to5Google haberi). Hız/verimlilik yerine "daha derin analiz" odaklı — karmaşık görevlerde ek akıl yürütme adımları ve yinelemeli araç çağrıları yapıyor. HLE-Verified (çok adımlı STEM/profesyonel akıl yürütme): %54,9. DeepSWE v1.1'de daha büyük amiral gemisi modelleri daha düşük maliyetle geçiyor (spesifik puan verilmedi). NOT: Kaynakta belirtilen giriş fiyatı ($0,75/$3,75 per MTok, 31 Aralık'a kadar) 3.7 Flash'la birebir aynı — WebFetch özetleyicisinin eski rakamı tekrarlamış olma ihtimali var (K1), bu yüzden fiyat bilgisi doğrulanamadı olarak işaretleniyor.
  - 2026-09-14: kontrol edildi, gelişme yok (Gemini API resmi changelog'da 2-3 Eylül'den (3.8 Flash GA, Lyria 3.5 önizleme) bu yana yeni girdi yok).

### 6. Qwen serisi (Alibaba: 3.8-Max, 3.8-27B, 3.8-Flash-Next, QwenWork, Audio-3.0-TTS, Image-3.0)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-09-14 | Durum: Aktif
- Günlük (07-27/08-08 özet: 3.8-Max-Preview, Audio-3.0-TTS #1, Image-3.0 ilk takip; 3.8-Max resmen duyuruldu 2.4T, Unsloth day-zero destek):
  - 2026-08-10 (🟢): 3.8-Max genel kullanıma açıldı ($2/$6 per MTok); 27B açık ağırlıklı varyant yayınlandı.
  - 2026-08-17 (🟡): Alibaba, bir sonraki Qwen modeli için gelir paylaşımlı lisans modeline geçeceğini duyurdu (7 Ağustos) — büyük ticari kullanıcılar Alibaba ile anlaşma yapacak. Kesin oran henüz belirlenmedi.
  - 2026-08-24: kontrol edildi, doğrudan AI/ürün gelişmesi yok.
  - 2026-08-31 (🟢): Qwen3.8-27B (16 Ağustos, Apache 2.0) geniş basın ilgisi gördü — Artificial Analysis Intelligence Index'te 52 puan, GPT-5.6 Luna ile eşit; SWE-bench Pro %61,7, LiveCodeBench %90,3. 4-bit sıkıştırılmış versiyonu ~17GB VRAM ile çalışıyor.
  - 2026-09-07 (🟡): Geriye dönük fark edilen gelişme — Alibaba, Qwen4 mimarisinin önizlemesi olarak sunulan Qwen3.8-Flash-Next'i yayınladı (~26 Ağustos, TechNode/Decrypt/The Decoder haberleri; önceki haftanın taramasında atlanmış). 6B aktif parametreli MoE, "ultimate cost efficiency" hedefli, açık ağırlıklı. Qwen4'ün mimari yönelimine dair ilk somut işaret olarak sunuluyor. Spesifik benchmark rakamları kaynaklar arası tutarsız olduğu için rapora alınmadı.
  - 2026-09-14 (🟡): Geriye dönük fark edilen gelişme — Alibaba, üç mevcut ajan servisini (QoderWork, MuleRun, Wukong) birleştiren "QwenWork" adlı ajan platformunun küresel beta sürümünü duyurdu (1 Eylül; newsbytes.ph haberi). Standart katman Qwen3.8 Flash modelini kullanıyor; web/bilgisayar otomasyonu, doküman/görsel/video/ses üretimi, dosya analizi ve oturumlar arası tercih hafızası ("awareness") içeriyor. Önce Çin'de ağustos başında tanıtılmış, bu hafta Asya/Orta Doğu/Latin Amerika'da küresel beta olarak genişledi.

### 12. AI ajan güvenlik açıkları (sandbox kaçışları, framework RCE)
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-09-07 | Durum: Aktif
- Günlük (08-07/08-08 özet: Ajanlar izole ortamlardan kaçtı, CISA 12 framework'te kritik RCE tespit etti; IBM Langflow CVE-2026-9198 KEV kataloğuna eklendi):
  - 2026-08-10 (🟡): Cursor IDE sandbox atlatma açıkları (CVE-2026-50548/50549). AI tarayıcılarını hedefleyen "PleaseFix" sıfır-tıklama saldırıları duyuruldu.
  - 2026-08-17 (🟡): Black Hat 2026'da Anthropic/Google/OpenAI kodlama ajanlarında RCE, kimlik bilgisi hırsızlığı, prompt injection ve tedarik zinciri riskleri bulundu. "RovoBlast" tekniği Atlassian Rovo oturumlarını istismar ediyor. Veracode: AI üretimi kodun güvenlik geçme oranı %56.
  - 2026-08-24: kontrol edildi, yeni gelişme yok.
  - 2026-08-31 (⚪): DavidCarliez/trustmebro (304 yıldız) — sahte tool-output ile guardrail atlatma aracı gündeme geldi.
  - 2026-09-07 (🟢): Manifold Security'nin "GitSpawn" araştırması (2 Eylül, The Hacker News haberi) Git'in `core.fsmonitor` ayarını istismar eden bir RCE zinciri buldu — kötü niyetli bir `.git/config` (arşiv/USB/paylaşılan sürücü ile taşınan repolarda) agent'ın sandbox/onay adımları dışında, kullanıcı yetkisiyle komut çalıştırmasına yol açıyor. 1 Eylül itibarıyla 7 ajan etkilendi: goose (1.44.0'da düzeltildi), Claude Code (2.1.196'da kısmen düzeltildi, "ultrareview" yolunda ek açık sürüyor), Cursor ve Codex CLI/Desktop düzeltildi; Hermes Agent, Qwen Code ve Grok Build HÂLÂ YAMANMAMIŞ. Aynı gün OpenAI ayrıca Codex için 3 ayrı CVE yayınladı.
  - 2026-09-14: kontrol edildi, bu hafta (8-14 Eylül) için doğrulanmış yeni bir ajan güvenlik açığı/yama duyurusu bulunamadı — GitSpawn açığının bu haftaki güncel yama durumunu doğrulayan bir kaynağa erişilemedi (WebFetch hedef sayfası 404 döndü), bu yüzden rapora alınmadı (K2/K1). Son güncelleme değişmedi.

### 13. DeepSeek V4-Flash/V4.1-Flash/V4-Pro + DeepSeek Harness (dsh)
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-09-14 | Durum: Aktif
- Günlük:
  - 2026-08-07: V4-Flash-0731 MIT lisansıyla açık kaynak; 284B MoE, Terminal-Bench ~82.7.
  - 2026-08-17 (🟢): V4 Pro GA oldu (12 Ağustos). SWE-bench Verified %80,6; 1,6T toplam/49B aktif parametre. DeepSeek Harness (dsh) v0.1 yayınlandı (13 Ağustos).
  - 2026-08-24 (🟢): dsh resmi reposu 11 günde 189.256 yıldıza ulaştı (GitHub API doğrulu).
  - 2026-08-31 (🟡): dsh 205.243 yıldız, 23.773 fork (%8,4 haftalık artış) — büyüme sürüyor ama hız kesiyor.
  - 2026-09-07 (⚪): deepseek-ai/deepseek-harness GitHub API ile doğrulandı — 214.358 yıldız, 25.247 fork (205.243'ten, %4,4 haftalık artış). Büyüme yavaşlamaya devam ediyor.
  - 2026-09-14 (🟢): DeepSeek, V4.1-Flash modelini yayınladı (10 Eylül; resmi DeepSeek API değişiklik günlüğü ile doğrulandı) — yerel çok-modlu (multimodal) yetenekler ekliyor, model adı `deepseek-flash` olarak güncellendi. Aynı duyuruda DeepSeek, V4 Pro API hizmetini 14 Eylül sonrasında da aynı ücretlendirmeyle sürdüreceğini bildirdi. GitHub API ile doğrulandı: deepseek-ai/deepseek-harness — 222.968 yıldız, 26.482 fork (214.358'den, %4,0 haftalık artış — büyüme yavaş da olsa sürüyor).

### 15. AB Yapay Zeka Yasası (AI Act) uygulama takvimi
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-08-31 | Durum: Aktif
- Günlük:
  - 2026-08-07: Madde 50 şeffaflık kuralları 3 Ağustos'ta yürürlüğe girdi. Yüksek riskli AI hükümleri 2 Ağustos'ta yürürlüğe girdi.
  - 2026-08-08, 08-10, 08-17, 08-24: kontrol edildi, gelişme yok.
  - 2026-08-31 (🟡): Axios'un "AI Act gets real" değerlendirmesi şirket uyum tepkilerini detaylandırdı (Anthropic watermark, Google/Meta taahhüt, OpenAI provenance, Microsoft iç yönetişim). AB AI Ofisi bilgi talep edebiliyor ama henüz ceza/uygulama eylemi yok.
  - 2026-09-07: kontrol edildi, gelişme yok. NOT: Bu hafta dolaşımda "AB AI Ofisi 3 şirkete 47M€ ceza kesti" iddiası olan birkaç ikincil kaynak bulundu, ancak birincil kaynak taraması bunun gerçekleşmediğini, ileriye dönük bir tahmin makalesinin başlığının yanlış yorumlandığını gösterdi (K1) — rapora ALINMADI.
  - 2026-09-14: kontrol edildi, gelişme yok (bu hafta yalnızca AB AI Act'e karşı ABD tarafından yazılmış eleştirel bir görüş makalesi bulundu — somut bir uygulama/ceza gelişmesi değil).

### 17. Prime Agent (Prime Intellect)
- İlk görülme: 2026-08-08 | Son güncelleme: 2026-09-14 | Durum: Aktif
- Günlük (08-08/08-24 özet: ARC-AGI-3 %95,5, MIT lisanslı, "Continual Harness" mimarisi; yıldız 12.064→16.671→18.055):
  - 2026-08-31 (⚪): 19.305 yıldız, 2.101 fork (+%6,9).
  - 2026-09-07 (⚪): GitHub API ile doğrulandı — 20.074 yıldız, 2.196 fork (19.305'ten, %4,0 haftalık artış). Büyüme yavaşlamaya devam ediyor.
  - 2026-09-14 (⚪): PrimeIntellect-ai/prime-agent GitHub API ile doğrulandı — 20.710 yıldız, 2.265 fork (20.074'ten, %3,2 haftalık artış — büyüme hafif hızlandı).

### 20. AI ajan mimarisi/hafıza yaklaşımları (Karpathy, MCP spec, AKB, lemmalog, agent-memory, okf-agent-memory)
- İlk görülme: 2026-08-08 | Son güncelleme: 2026-09-14 | Durum: Aktif
- Günlük (08-08/08-24 özet: Karpathy graph-tabanlı hafıza dokümanı; dnotitia/akb 140→147→154 yıldız):
  - 2026-08-31 (⚪): akb 156 yıldız. JordyZomer/lemmalog gündeme geldi (212 yıldız, 27 Ağustos, Datalog-tabanlı ajan hafızası).
  - 2026-09-07 (🟡): dnotitia/akb GitHub API ile doğrulandı — 158 yıldız (156'dan, marjinal). Buna karşın JordyZomer/lemmalog GitHub API ile doğrulandı — 288 yıldız, 25 fork (212'den, %35,8 haftalık artış) — belirgin bir sıçrama. Alanda iki yeni giriş de bu hafta oluşturuldu: tigerless-labs/agent-memory (405 yıldız, 1 Eylül) ve okf-agent-memory/okf-agent-memory (388 yıldız, 5 Eylül — Google OKF v0.2'yi uygulayan, harici veritabanı gerektirmeyen Go tabanlı git-native kalıcı hafıza). Sembolik/yapılandırılmış ve dosya-tabanlı hafıza yaklaşımlarına ilgi çeşitleniyor.
  - 2026-09-14 (🟢): Bu haftanın en dikkat çekici gelişmesi hafıza repolarındaki büyüme sıçraması. GitHub API ile doğrulandı: tigerless-labs/agent-memory — 1.353 yıldız, 83 fork (405'ten, %234 haftalık artış); okf-memory/okf-agent-memory — 629 yıldız, 44 fork (388'den, %62 haftalık artış); JordyZomer/lemmalog — 308 yıldız, 28 fork (288'den, %6,9 artış); dnotitia/akb — 160 yıldız (158'den, marjinal). Dosya-tabanlı/git-native ajan hafızası kategorisinde belirgin bir ilgi patlaması yaşanıyor.

### 21. Anthropic Cowork
- İlk görülme: 2026-08-10 | Son güncelleme: 2026-08-31 | Durum: Aktif
- Günlük:
  - 2026-08-10: İlk takip. Claude Code'un ajan yeteneklerini teknik olmayan kullanıcılara taşıyan ürün.
  - 2026-08-17, 08-24: kontrol edildi, gelişme yok.
  - 2026-08-31 (🟢): Anthropic, Claude'un chat ve Cowork hafıza sistemlerini birleştirdi (25 Ağustos).
  - 2026-09-07: kontrol edildi, gelişme yok (bu haftaki büyük Anthropic haberi — Commerce Agents — ayrı konu başlığı altında işlendi, bkz. #2).
  - 2026-09-14: kontrol edildi, gelişme yok (bu haftaki Anthropic haberleri — Smart Reports, tehdit istihbaratı raporu — #2 altında işlendi).

### 22. Yerel/açık kaynak Cowork & Claude Code alternatifleri (Goose, Eigent)
- İlk görülme: 2026-08-10 | Son güncelleme: 2026-09-14 | Durum: Aktif
- Günlük (08-10/08-24 özet: Block Goose ilk takip; eigent-ai/eigent 14.898→15.022→15.087 yıldız):
  - 2026-08-31 (⚪): eigent 15.162 yıldız — hız kesmeye devam ediyor.
  - 2026-09-07 (⚪): eigent-ai/eigent GitHub API ile doğrulandı — 15.205 yıldız, 1.815 fork (15.162'den, marjinal %0,3 artış — büyüme neredeyse durdu). Çapraz not: Block Goose, bu hafta gündeme gelen GitSpawn RCE açığını 1.44.0 sürümünde düzeltenler arasında (bkz. #12).
  - 2026-09-14 (⚪): eigent-ai/eigent GitHub API ile doğrulandı — 15.269 yıldız, 1.823 fork (15.205'ten, %0,4 artış — büyüme neredeyse tamamen durdu).

### 23. Salesforce Slackbot'un AI ajanına dönüştürülmesi (Claudeforce)
- İlk görülme: 2026-08-10 | Son güncelleme: 2026-08-31 | Durum: Aktif
- Günlük:
  - 2026-08-10: İlk takip. Slackbot, AI ajanına dönüştürüldü.
  - 2026-08-17, 08-24: kontrol edildi, gelişme yok.
  - 2026-08-31 (🟢): Salesforce ve Anthropic "Claudeforce" ortaklığını duyurdu (26 Ağustos) — iki yönlü entegrasyon (Salesforce in Claude / Claude in Salesforce).
  - 2026-09-07: kontrol edildi, gelişme yok (bu hafta bulunan haberler yalnızca 26 Ağustos duyurusunun yankıları/analizleri, yeni bir gelişme yok).
  - 2026-09-14: kontrol edildi, gelişme yok.

### 24. Yeni GitHub AI/agent repoları (haftalık tarama)
- İlk görülme: 2026-08-10 | Son güncelleme: 2026-09-14 | Durum: Aktif
- Günlük:
  - 2026-08-10, 08-17, 08-24, 08-31: önceki taramalar (bkz. geçmiş commit'ler).
  - 2026-09-07: 1-7 Eylül'de oluşturulanlar (yıldızlar GitHub API ile doğrulandı, created:>2026-08-31 stars:>100 llm/agent/ai filtresi): anthropics/commerce-agents (2.275, resmi Anthropic reposu — bkz. #2), Albert-Weasker/niubigeo (621, açık kaynak AI marka görünürlüğü/rakip raporları), tigerless-labs/agent-memory (405), okf-memory/okf-agent-memory (388), kydlikebtc/awesome-grokbot (331, Grok Bot paylaşım kataloğu), LunarXuan/image-prompt-reverse (308, Codex için görsel prompt tersine mühendislik skill'i), adtexterry-lgtm/unigit-ecosystem (307), BoardUI/boardui (261, ajan arayüzleri için React tasarım sistemi), gozen3ji/consulting-pptx-skill (249, Claude Code için Japonca PPTX üretim skill'i), joeseesun/qiaomu-book-reader (235, Obsidian içinde AI destekli kitap okuma), Agenta-AI/awesome-ai-agent-platforms (234, küratörlü açık kaynak ajan platformları listesi), techjanitor/botmaker (223), jarrenrocks/bot-crossing (180, AI ajanları için video oyunu), dreamers-laboratory/agent-fleet-manager (171), Mercor-Intelligence/ApexAgents-SkyRL-Recipe (156).
  - 2026-09-14: 8-14 Eylül'de oluşturulanlar (yıldızlar GitHub API ile doğrulandı, created:>2026-09-07 stars:>100 llm/agent/ai filtresi): Edge0-AI/Edge0 (1.629, Apple Silicon için MoE akış çıkarım motoru — SSD expert offload + Recover-LoRA + prerouter routing prediction, Apache-2.0), SpaceDudem/text-humanizer (737, AI-üretimi metni "insansılaştırıp" GPTZero/Turnitin gibi dedektörleri atlatma aracı), Colafornia/short-video-generator-AI (723, YouTube videolarını viral kısa videolara çeviren araç), eternityspring/reelbench-skills (577, AI video analiz/üretim skill'i — Claude Code), rizqinrr/viserys-agent (630), kruzovic7/ai-data-extractor (461, Claude Code/Cursor/Windsurf/Aider/Cline sohbet geçmişi çıkarıcı), zjwzcx/Awesome-Astra-Embodied-AI (334, GPT-6 Astra'yı gömülü/robotik AI'ya uygulama listesi — bkz. #26), deepseek-ai/DeepSelect (333, DeepSeek Sparse Attention için TopK kernelleri — resmi DeepSeek reposu), deepseek-ai/deepseek-recipe (323, resmi DeepSeek reposu), deepseek-ai/DeepJIT (303, resmi DeepSeek reposu), Phyzicalorg/Phyzical_org (282, elizaOS uyumlu gömülü-AI teleoperasyon veri platformu), yudaprasetya007/routeVSCODE (238, VSCode Copilot Chat için sıfır-yeniden-yükleme model değiştirici/yerel proxy), Qiuner/birdview (218, kod değişikliği öncesi mimariyi haritalayan geliştirici aracı), VaderChen/YourDesk (202, MCP entegrasyonlu uzak masaüstü — AI ajanlarının bilgisayarı kontrol etmesi için).

### 25. AI imza/watermark temizleme araçları ve tartışma
- İlk görülme: 2026-08-17 | Son güncelleme: 2026-09-14 | Durum: Aktif
- Günlük:
  - 2026-08-17: İlk takip. guillaumemeyer/watermarks-remover 6 günde 12.177 yıldıza ulaştı.
  - 2026-08-24 (🟢): 17.557 yıldız (+%44). Rakip ShadowAqueduct/watermark-remover 1 günde 760 yıldıza ulaştı.
  - 2026-08-31 (🟡): guillaumemeyer 19.536 yıldız (+%11,3). ShadowAqueduct 836 yıldız (760'tan, ivme kesildi).
  - 2026-09-07 (🟡): guillaumemeyer/watermarks-remover GitHub API ile doğrulandı — 21.055 yıldız, 2.425 fork (19.536'dan, %7,8 haftalık artış). DİKKAT: ShadowAqueduct/watermark-remover artık GitHub API'de bulunamıyor (`404 Not Found`, hem doğrudan repo sorgusu hem de arama API'si üzerinden doğrulandı) — repo silinmiş veya kullanıcı hesabı kaldırılmış/yeniden adlandırılmış görünüyor. WebFetch ile eski bir önbellek sayfası hâlâ görüntülenebiliyor (760 yıldız gösteriyor, muhtemelen bayat veri) ama API kesin: repo artık mevcut değil. Ekosistemde onlarca küçük "watermarks-remover" fork/türevi var (çoğu <15 yıldız), tekel oluşmadı.
  - 2026-09-14 (🟡): guillaumemeyer/watermarks-remover GitHub API ile doğrulandı — 21.934 yıldız, 2.527 fork (21.055'ten, %4,2 haftalık artış — büyüme yavaş ama istikrarlı sürüyor). ShadowAqueduct/watermark-remover hâlâ GitHub'da bulunamıyor.

### 26. GPT-5.6 → GPT-6 Astra (OpenAI)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-09-07 | Durum: Aktif
- Günlük:
  - 2026-07-27: İlk takip. 2-9 Temmuz duyurusu: Sol (amiral gemisi), Terra, Luna.
  - 2026-08-24 (🟡): GPT-5.6 Sol/Luna için "effort slider" güncellemesi (6 Ağustos); halüsinasyon oranında ~%60 azalma iddiası.
  - 2026-08-31: kontrol edildi, gelişme yok.
  - 2026-09-07 (🟢): OpenAI, GPT-6 Astra'yı yayınladı (3-4 Eylül; OpenAI'nin resmi sayfası + CNBC + Al Jazeera + Axios ile doğrulandı) — "dünyanın en zeki ve en hizalı modeli" olarak tanıtıldı. Kademeli erişim: ChatGPT Plus/Pro/Business/Enterprise'a günler içinde, ayrıca API/Azure/Bedrock üzerinden. Benchmark'lar (OpenAI'nin resmi sayfasından): ARC-AGI-3 %99,9 (seviyelerin %96'sında insan paritesi), FrontierMath Tier 4 %97,6, ExploitBench %100, OSWorld 2.0 (computer use) %72,6 (öncekinden ~%47 daha az sürede), Terminal-Bench 4.0 %57,9. Fiyatlandırma: API standart $10/milyon giriş, $50/milyon çıkış token; hızlı mod 2x hız/2x fiyat. Güvenlik: yetkisiz görevleri reddetme oranı %48'den %100'e çıktı; yanlış hizalanma izleme sistemi eklendi. Duyuru, Temmuz'daki Hugging Face'e yönelik AI-öncülüğünde siber saldırı sonrası artan güvenlik/etik tartışması gölgesinde yapıldı — uzmanlar yetenek artışı ile hizalama/kontrol arasındaki açığın kapanmadığını belirtiyor.
  - 2026-09-14: kontrol edildi, doğrudan yeni model/ürün gelişmesi yok (ilgi sürüyor — bu hafta GitHub'da "Awesome-Astra-Embodied-AI" adlı bir listeleme reposu gündeme geldi, bkz. #24).

### 27. Vercel fx — minik açık kaynak kodlama ajanı
- İlk görülme: 2026-08-24 | Son güncelleme: 2026-09-14 | Durum: Aktif
- Günlük:
  - 2026-08-24: İlk takip. Vercel Labs, Zig ile yazılmış minimal kodlama ajanı "fx"i açık kaynak yaptı.
  - 2026-08-31 (🟡): 2.622 yıldız, 300 fork (+%15,5).
  - 2026-09-07 (🟡): GitHub API ile doğrulandı — 2.786 yıldız, 319 fork (2.622'den, %6,3 haftalık artış). Topluluk türevleri artmaya devam ediyor.
  - 2026-09-14 (🟡): vercel-labs/fx GitHub API ile doğrulandı — 2.947 yıldız, 336 fork (2.786'dan, %5,8 haftalık artış).

### 28. Meta Muse Spark (1.1→1.3) / Muse Code / Meta Model API
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-09-07 | Durum: Aktif (arşivden döndü)
- Günlük (arşivlenmeden önceki geçmiş):
  - 2026-07-27: İlk takip. 1M token bağlam, Meta'nın ilk ücretli model API'si, computer-use desteği.
  - 2026-08-08 (🟡): Muse Spark 1.2 tabanlı "Meta Muse Code" duyuruldu.
  - 2026-08-10, 08-17, 08-24: kontrol edildi, yeni gelişme yok.
  - 2026-08-31: kontrol edildi, gelişme yok. 23 gün gelişme yok → arşivlendi.
- Günlük (yeniden gündeme geldikten sonra):
  - 2026-09-07 (🟢) — YENİDEN GÜNDEMDE: Meta, Muse Spark 1.3'ü yayınladı (2 Eylül; Meta AI Research'in resmi blogu + Bloomberg/VentureBeat/Axios/MarkTechPost ile doğrulandı). Vurgu ham yetenek artışı değil verimlilik — resmi duyuruya göre karşılaştırılabilir mühendislik görevlerini bitirmek için önceki sürüme (1.2) göre ~%20 daha az araç çağrısı ve ~%25 daha az token kullanıyor; daha uzun ufuklu ajan iş akışları, geri döndürülemez eylemlerde daha iyi yargı ve güçlendirilmiş adversarial sağlamlık içeriyor. Muse Code ve dev.meta.ai üzerindeki Meta Model API üzerinden erişilebiliyor. NOT (K1): Bazı ikincil kaynaklar (ör. tech-insider.org) spesifik benchmark puanları (DeepSWE v1.1 75,4; Terminal-Bench 2.1 88,8 vb.) verdi, ancak resmi Meta blog özeti bu rakamları teyit etmedi ("spesifik sayısal puan verilmedi") — bu yüzden spesifik puanlar rapora ALINMADI, yalnızca resmi kaynakla örtüşen %20/%25 verimlilik iddiası kullanıldı.
  - 2026-09-14: kontrol edildi, gelişme yok.

### 29. Mistral AI 3 milyar € Series D turu (Samsung liderliğinde) — Avrupa'nın "sovereign AI" hamlesi
- İlk görülme: 2026-09-14 | Son güncelleme: 2026-09-14 | Durum: Aktif
- Günlük:
  - 2026-09-14 (🟢): Mistral AI, Samsung Electronics liderliğinde (Scaleup Europe Fund/EQT ve mevcut yatırımcı PSG Equity ortak liderliğinde) 3 milyar € tutarında Series D turu kapattığını duyurdu (8 Eylül; Mistral'ın resmi haber sayfası + TechCrunch ile doğrulandı). Tur sonrası şirket değerlemesi 21 milyar €'nun üzerine çıktı. Resmi açıklamaya göre bu, bir Avrupa teknoloji şirketinin şimdiye kadar gerçekleştirdiği en büyük özkaynak fonlama turu (şirketin 3 yıllık geçmişinde). Fon frontier araştırmanın genişletilmesine, model eğitimi için hesaplama kapasitesine ve şirketin faaliyet gösterdiği 20 ülkedeki altyapı ölçeklendirmesine ayrılacak.

### 30. Grok 4.6 → 4.7 (xAI)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-09-14 | Durum: Aktif (arşivden döndü)
- Günlük (arşivlenmeden önceki geçmiş):
  - 2026-07-27: İlk takip. 1.5T MoE, Cursor ajan verisiyle eğitildi, Terminal-Bench 2.1 %83.3.
  - 2026-08-08 (🟡): Grok 4.6 ~7 Ağustos'a hedeflendi.
  - 2026-08-10 (🟡): Hedef tarih geçti. Musk 10-14 Ağustos haftasına kaydırdı.
  - 2026-08-17 (🟢): Grok 4.6 resmen çıktı (12 Ağustos). $2/$6/$0.50 per MTok. xAI'nin 61 puan/1753 ELO iddiaları bağımsız doğrulanmadı.
  - 2026-08-24, 08-31: kontrol edildi, gelişme yok (Grok 5 için doğrulanmış tarih yok).
  - 2026-09-07: kontrol edildi, gelişme yok. Bu hafta yalnızca eski (temmuz/ağustos tarihli) "Grok 5 ne zaman çıkar" tahmin makaleleri bulundu, yeni bir doğrulanmış gelişme yok. Çapraz not: Grok Build bu hafta GitSpawn RCE açığı bakımından hâlâ yamanmamış ajanlar arasında sayıldı (bkz. #12), ancak bu Grok 4.6 modelinin kendisiyle ilgili bir gelişme değil. 21 gün gelişme yok → arşivlendi.
- Günlük (yeniden gündeme geldikten sonra):
  - 2026-09-14 (🟢) — YENİDEN GÜNDEMDE: İki gelişme: (1) Microsoft, Copilot'a (Word/Excel/PowerPoint) Grok modellerini ekledi (12 Eylül; Microsoft'un resmi Tech Community blogu ile doğrulandı) — varsayılan olarak kapalı, AB/EFTA/İngiltere önizlemeye dahil değil, modeller Microsoft altyapısı dışında barındırılıyor, kiracı düzeyinde veri izolasyonu var. (2) Grok 4.7 beşinci kez hedef tarihini kaçırdı — Musk 11 Eylül'de X'te modelin "birkaç gün daha pişmesi" gerektiğini, yanıt uzunluğuna aşırı reinforcement-learning cezası verilmesinin görevlerin erken bırakılmasına yol açtığını belirtti; yeni bir tarih verilmedi. NOT (K1): Grok 4.7'ye dair hiçbir teknik özellik (model ID, fiyat, bağlam penceresi, benchmark) resmi olarak doğrulanmadı — bilgiler yalnızca Musk'ın X gönderilerine dayanıyor, docs.x.ai'de belge yok; bu yüzden rapora sayısal/teknik iddia olarak ALINMADI.

## Arşivlenmiş Konular

### ChatGPT for Work & GPT-Live (OpenAI ürünleri)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-07-27 | Arşivlenme: 2026-08-17 (21+ gün gelişme yok)
- Günlük (arşivlenmeden önce):
  - 2026-07-27: İlk takip. Codex+ChatGPT birleşimi, site barındırma, tam-dupleks sesli asistan.
  - 2026-08-08, 08-10, 08-17: kontrol edildi, gelişme yok.
  - 2026-08-24, 08-31, 09-07: kontrol edildi, gelişme yok (arşivde kalıyor).
  - 2026-09-14: kontrol edildi, gelişme yok (arşivde kalıyor).

### OptMem — AI ajanları için hafıza aracı
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-07-27 | Arşivlenme: 2026-08-17 (21+ gün gelişme yok)
- Günlük (arşivlenmeden önce):
  - 2026-07-27: İlk takip. VictorTaelin; 426 token'lık prompt + script ile minimalist kalıcı hafıza.
  - 2026-08-08, 08-10, 08-17: kontrol edildi, gelişme yok.
  - 2026-08-24, 08-31, 09-07: kontrol edildi, gelişme yok (arşivde kalıyor).
  - 2026-09-14: kontrol edildi, gelişme yok (arşivde kalıyor).

### Sakana AI — Fugu-Cyber
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-07-27 | Arşivlenme: 2026-08-17 (21+ gün gelişme yok)
- Günlük (arşivlenmeden önce):
  - 2026-07-27: İlk takip. CyberGym %86.9, CTI-REALM %72.1.
  - 2026-08-08, 08-10, 08-17: kontrol edildi, gelişme yok.
  - 2026-08-24, 08-31, 09-07: kontrol edildi, gelişme yok (arşivde kalıyor).
  - 2026-09-14: kontrol edildi, gelişme yok (bu hafta Sakana için yeni bir model/araştırma duyurusu bulunamadı; arşivde kalıyor).

### Kimi K3 / K4 (Moonshot AI)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-08-08 | Arşivlenme: 2026-08-31 (21+ gün gelişme yok)
- Günlük (arşivlenmeden önce):
  - 2026-07-27: İlk takip. 2.8T parametre, 1M bağlam.
  - 2026-08-08 (🟢): Açık ağırlıkların 27 Temmuz'da yayınlandığı doğrulandı.
  - 2026-08-10, 08-17, 08-24: kontrol edildi, gelişme yok.
  - 2026-08-31: kontrol edildi, gelişme yok. 23 gün gelişme yok → arşivlendi.
  - 2026-09-07: kontrol edildi, gelişme yok (Kimi K4 için yalnızca Nvidia Blackwell çip talebine dair 28 Temmuz tarihli eski haberler var — yeni model gelişmesi değil, arşivde kalıyor).
  - 2026-09-14: kontrol edildi, gelişme yok (Kimi K4 hâlâ doğrulanmış bir sürüm tarihine sahip değil — tüm kaynaklar tahmin/spekülasyon niteliğinde; arşivde kalıyor).

### OpenAI Astra (matematik/araştırma modeli — GPT-6 Astra ile KARIŞTIRILMASIN)
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-08-10 | Arşivlenme: 2026-08-31 (21+ gün gelişme yok)
- Günlük (arşivlenmeden önce):
  - 2026-08-07: ~2.000 dolarlık hesaplamayla 10 açık problemi Lean kanıtlarıyla çözdü.
  - 2026-08-08 (🟢): 10 çözülememiş problem çözüldü; Fields madalyalı Jacob Tsimerman OpenAI'ye katıldı.
  - 2026-08-10 (🟢): Kanıtlar tartışmalı bulundu.
  - 2026-08-17, 08-24: kontrol edildi, gelişme yok.
  - 2026-08-31: kontrol edildi, gelişme yok. 21 gün gelişme yok → arşivlendi.
  - 2026-09-07: kontrol edildi, gelişme yok. NOT: Bu hafta OpenAI'nin yeni amiral gemisi modeli "GPT-6 Astra" adıyla piyasaya çıktı (bkz. #26) — isim burada arşivlenen matematik-araştırma projesiyle aynı ama resmi kaynaklarda bu iki "Astra" arasında doğrudan bir bağlantı doğrulanamadı; karıştırılmaması için bu not eklendi.
  - 2026-09-14: kontrol edildi, gelişme yok (arşivde kalıyor).

### AI ajan ödeme altyapısı (agent payments)
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-08-07 | Arşivlenme: 2026-08-31 (21+ gün gelişme yok)
- Günlük (arşivlenmeden önce):
  - 2026-08-07: Cloudflare "Wallets" ve MoonPay "PayBox" (x402 standardı) duyuruldu.
  - 2026-08-10, 08-17, 08-24, 08-31: kontrol edildi, gelişme yok. 24 gün gelişme yok → arşivlendi.
  - 2026-09-07: kontrol edildi, gelişme yok (arşivde kalıyor).
  - 2026-09-14: kontrol edildi, gelişme yok (arşivde kalıyor).

### Mistral Shieldstral
- İlk görülme: 2026-08-08 | Son güncelleme: 2026-08-08 | Arşivlenme: 2026-08-31 (21+ gün gelişme yok)
- Günlük (arşivlenmeden önce):
  - 2026-08-08: İlk takip. 3B parametreli çok modlu güvenlik sınıflandırıcı.
  - 2026-08-10, 08-17, 08-24, 08-31: kontrol edildi, gelişme yok. 23 gün gelişme yok → arşivlendi.
  - 2026-09-07: kontrol edildi, gelişme yok (Mistral için bu hafta yalnızca spekülatif "Large 3" söylentileri bulundu, doğrulanmış bir duyuru yok — arşivde kalıyor).
  - 2026-09-14: kontrol edildi, Shieldstral ürününün kendisine dair gelişme yok. NOT: Bu hafta Mistral hakkında büyük bir haber vardı (3 milyar € Series D turu) ama bu Shieldstral'la ilgili değil, ayrı bir konu olarak eklendi (bkz. #29).

### Çok modlu üretici modeller (DiffusionGemma, MiniMax H3)
- İlk görülme: 2026-08-08 | Son güncelleme: 2026-08-08 | Arşivlenme: 2026-08-31 (21+ gün gelişme yok)
- Günlük (arşivlenmeden önce):
  - 2026-08-08: DiffusionGemma ve MiniMax H3 ilk takip.
  - 2026-08-10, 08-17, 08-24, 08-31: kontrol edildi, gelişme yok. 23 gün gelişme yok → arşivlendi.
  - 2026-09-07: kontrol edildi, gelişme yok (arşivde kalıyor).
  - 2026-09-14: kontrol edildi, gelişme yok (arşivde kalıyor).

### Gemini 3.5/3.6/3.7 Flash liderlik değişikliği / Gemini 4 (Google DeepMind)
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-08-17 | Arşivlenme: 2026-09-07 (21+ gün gelişme yok)
- Günlük (arşivlenmeden önce):
  - 2026-08-07: Hassabis CEO'luktan Alphabet başkanlığına geçti; Kavukcuoglu Gemini 4'ün başına geçti. Jeff Dean, Vinyals, Quoc Le, Ghemawat ayrılıp "Discovery Loop"u kurdu.
  - 2026-08-10: kontrol edildi, gelişme yok.
  - 2026-08-17 (🟡): Koray Kavukcuoglu resmen "frontier AI" çalışmalarının başına geçti (12 Ağustos).
  - 2026-08-24, 08-31: kontrol edildi, gelişme yok.
  - 2026-09-07: kontrol edildi, gelişme yok. Bu hafta yalnızca doğrulanmamış/spekülatif "Gemini 4 Pro checkpoint sızdı" haberleri (tek kaynaklı, güvenilirliği düşük bloglar) bulundu — birincil kaynak yok, rapora alınmadı. 21 gün gelişme yok → arşivlendi. NOT: Gemini modellerinin kendisi (Flash ailesi) ayrı bir konu olarak (#3) aktif takipte kalmaya devam ediyor; bu konu özel olarak DeepMind liderlik değişikliği ve Gemini 4 programını kapsıyor.
  - 2026-09-14: kontrol edildi, gelişme yok (arşivde kalıyor).

## Değişiklik Geçmişi

(NOT: 3 aylık sıkıştırma kuralı gereği 2026-07-22 ve 2026-07-27 girdileri — takip sisteminin başlangıcı ve ilk 10 konu — özetlenip kaldırıldı; git commit geçmişinde korunuyor.)

- 2026-08-07: 7 yeni konu; üç ayrı dosyaya bölünmüş liste birleştirildi.
- 2026-08-08: 4 yeni konu, 7 konu güncellendi.
- 2026-08-10: 3 yeni konu, 9 konu güncellendi; GitHub konektörüyle repo bölümü gerçek API'den doğrulandı.
- 2026-08-10 (mimari değişiklik): Durum dosyası Google Drive'dan bu git deposuna taşındı.
- 2026-08-17: 1 yeni konu, 10 konu güncellendi, 4 konu arşivlendi (GPT-5.6, ChatGPT for Work & GPT-Live, OptMem, Sakana Fugu-Cyber). İlk arşivleme turu.
- 2026-08-24: 1 yeni konu (Vercel fx), 1 konu arşivden döndü (GPT-5.6), 11 konu güncellendi, 0 konu arşivlendi.
- 2026-08-31: 0 yeni konu, 12 konu güncellendi, 6 konu arşivlendi (Kimi K3, Meta Muse Spark/Code, OpenAI Astra, AI ajan ödeme altyapısı, Mistral Shieldstral, çok modlu üretici modeller). Öne çıkan: Anthropic-Salesforce "Claudeforce" ortaklığı; Cowork hafıza birleşmesi; Qwen3.8-27B basın ilgisi; DeepSeek Harness 205.243 yıldız.
- 2026-09-07: 0 yeni konu, 1 konu arşivden döndü (Meta Muse Spark 1.3, #28), 13 konu güncellendi (#2, #3, #6, #12, #13, #17, #20, #22, #24, #25, #26, #27, #28), 2 konu arşivlendi (Grok 4.6, Google DeepMind liderlik/Gemini 4 — ikisi de 21+ gün gelişme yok). Öne çıkan: OpenAI GPT-6 Astra'yı yayınladı (haftanın en büyük tekil gelişmesi — ARC-AGI-3 %99,9); Anthropic Claude Commerce Agents blueprint'ini açtı (2.275 yıldız <1 haftada); Meta Muse Spark 1.3 ile yeniden gündemde; Google Gemini 3.8 Flash'ı 3 hafta arayla art arda üçüncü kez yayınladı; GitSpawn (`core.fsmonitor`) RCE açığı 7 kodlama ajanını etkiledi (Claude Code, Cursor, Codex kısmen/tam yamalı — Hermes Agent, Qwen Code, Grok Build hâlâ açık); ShadowAqueduct/watermark-remover GitHub API'de artık bulunamıyor (muhtemelen silindi).
- 2026-09-14: 1 yeni konu (Mistral AI 3 milyar € Series D turu, #29), 1 konu arşivden döndü (Grok 4.6 → 4.7, #30), 9 konu gerçek gelişmeyle güncellendi (#2, #6, #13, #17, #20, #22, #24, #25, #27), 7 konu kontrol edildi/gelişme yok (#3, #12, #15, #21, #23, #26, #28), 0 konu arşivlendi. Öne çıkan: Mistral AI, Samsung liderliğinde 3 milyar € Series D turu kapattı (Avrupa teknoloji tarihinin en büyük özkaynak turu, 21 milyar € değerleme); Microsoft Copilot'a Grok modelleri eklendi ve Grok 4.7 beşinci kez gecikti; DeepSeek V4.1-Flash yayınlandı; ajan hafızası repolarında büyük büyüme sıçraması (tigerless-labs/agent-memory %234, okf-agent-memory %62 haftalık artış); Anthropic Smart Reports (beta) ve tehdit istihbaratı raporu yayınladı.
