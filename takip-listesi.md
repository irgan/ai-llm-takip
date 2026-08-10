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

### 1. GPT-5.6 (OpenAI: Sol/Terra/Luna)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-07-27 | Durum: Aktif
- Günlük:
  - 2026-07-27: İlk takip. 2-9 Temmuz duyurusu: Sol (amiral gemisi, Ultra modu, ARC-AGI-3 %7.8), Terra (yarı maliyetle GPT-5.5 kalitesi), Luna (hızlı katman).
  - 2026-08-08, 08-10: kontrol edildi, gelişme yok.

### 2. Anthropic modelleri ve kurumsal/güvenlik gelişmeleri (Opus 5 / Fable 5 / Sonnet 5)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-08-10 | Durum: Aktif
- Günlük:
  - 2026-07-27: İlk takip. Fable 5 küresel erişime yeniden açıldı; Sonnet 5 tanıtım fiyatı $2/$10; Opus 5 yayınlandı (24 Tem).
  - 2026-08-07 (🟡): Tino Cuéllar Chief Global Affairs Officer oldu; açık ağırlıklı modeller pozisyon belgesi; Cognizant ortaklığı genişledi; 3 siber güvenlik olayı raporu.
  - 2026-08-10 (🟢): Cowork yayınlandı. Claude Code'da otomatik mod 14 Ağustos'tan itibaren Pro/Max/Team'de varsayılan — testte otomatik mod tehlikeli eylemlerin %89'unu, insan onayı %13.6'sını yakaladı; prompt injection taraması + deny kuralları eklendi.

### 3. Gemini 3.5/3.6 Flash ailesi (Google DeepMind)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-08-10 | Durum: Aktif
- Günlük:
  - 2026-07-27: İlk takip. Üç model (3.5 Flash Cyber, 3.5 Flash-Lite, 3.6 Flash); amiral gemisi çıktı maliyeti $9.00 → $7.50.
  - 2026-08-10 (🟡): 3.6 Flash için yönetilen ajanlar platformu genişledi — hook/trigger, uzaktan MCP, arka plan görevleri.

### 4. Grok 4.5 / 4.6 (xAI)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-08-10 | Durum: Aktif
- Günlük:
  - 2026-07-27: İlk takip. 1.5T MoE, Cursor ajan verisiyle eğitildi, Terminal-Bench 2.1 %83.3.
  - 2026-08-08 (🟡): Grok 4.6 ~7 Ağustos'a hedeflendi.
  - 2026-08-10 (🟡): Hedef tarih geçti, model çıkmadı. Musk 10-14 Ağustos haftasına kaydırdı; Grok Build ve Grok Imagine tanıtıldı.

### 5. Kimi K3 (Moonshot AI)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-08-08 | Durum: Aktif
- Günlük:
  - 2026-07-27: İlk takip. 2.8T parametre, 1M bağlam.
  - 2026-08-08 (🟢): Açık ağırlıkların 27 Temmuz'da yayınlandığı doğrulandı; API aynı gün canlıya alındı.
  - 2026-08-10: kontrol edildi, gelişme yok.

### 6. Qwen serisi (Alibaba: 3.8-Max, Audio-3.0-TTS, Image-3.0)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-08-10 | Durum: Aktif
- Günlük:
  - 2026-07-27: İlk takip. 3.8-Max-Preview, Audio-3.0-TTS (TTS liginde #1), Image-3.0.
  - 2026-08-08 (🟡): 3.8-Max resmen duyuruldu (2.4T); Unsloth 27B için day-zero fine-tuning desteği.
  - 2026-08-10 (🟢): 3.8-Max genel kullanıma açıldı ($2/$6 per MTok); 27B açık ağırlıklı varyant yayınlandı.

### 7. Meta Muse Spark 1.1/1.2 / Muse Code / Meta Model API
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-08-08 | Durum: Aktif
- Günlük:
  - 2026-07-27: İlk takip. 1M token bağlam, Meta'nın ilk ücretli model API'si, computer-use desteği.
  - 2026-08-08 (🟡): Muse Spark 1.2 tabanlı terminal kodlama ajanı "Meta Muse Code" duyuruldu.
  - 2026-08-10: kontrol edildi, yeni gelişme yok.

### 8. ChatGPT for Work & GPT-Live (OpenAI ürünleri)
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-07-27 | Durum: Aktif
- Günlük:
  - 2026-07-27: İlk takip. Codex+ChatGPT birleşimi, site barındırma, tam-dupleks sesli asistan.
  - 2026-08-08, 08-10: kontrol edildi, gelişme yok.

### 9. OptMem — AI ajanları için hafıza aracı
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-07-27 | Durum: Aktif
- Günlük:
  - 2026-07-27: İlk takip. VictorTaelin; 426 token'lık prompt + script ile minimalist kalıcı hafıza.
  - 2026-08-08, 08-10: kontrol edildi, gelişme yok.

### 10. Sakana AI — Fugu-Cyber
- İlk görülme: 2026-07-27 | Son güncelleme: 2026-07-27 | Durum: Aktif
- Günlük:
  - 2026-07-27: İlk takip. CyberGym %86.9, CTI-REALM %72.1.
  - 2026-08-08, 08-10: kontrol edildi, gelişme yok.
  - ⚠️ 21 gün eşiği 2026-08-17'de doluyor — o hafta gelişme yoksa ARŞİVLENMELİ. İlk arşivleme testi.

### 11. Google DeepMind liderlik değişikliği / Gemini 4
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-08-07 | Durum: Aktif
- Günlük:
  - 2026-08-07: Hassabis CEO'luktan Alphabet başkanlığına geçti; Kavukcuoglu Gemini 4'ün başına geçti. Jeff Dean, Vinyals, Quoc Le, Ghemawat ayrılıp "Discovery Loop"u kurdu. Alphabet ~%5 düştü.
  - 2026-08-10: kontrol edildi, gelişme yok.

### 12. AI ajan güvenlik açıkları (sandbox kaçışları, framework RCE)
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-08-10 | Durum: Aktif
- Günlük:
  - 2026-08-07: Ajanlar testlerde izole ortamlardan kaçtı. CISA 12 ajan framework'ünde kritik RCE açıkları tespit etti.
  - 2026-08-08 (🟢): CISA, IBM Langflow CVE-2026-9198'i (kimliksiz RCE) KEV kataloğuna ekledi; IBM 1.10.1+ acil güncelleme öneriyor.
  - 2026-08-10 (🟡): Cursor IDE sandbox atlatma açıkları (CVE-2026-50548/50549) gündeme geldi. AI tarayıcılarını hedefleyen "PleaseFix" sıfır-tıklama saldırıları duyuruldu.

### 13. DeepSeek V4-Flash
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-08-10 | Durum: Aktif
- Günlük:
  - 2026-08-07: V4-Flash-0731 MIT lisansıyla açık kaynak; 284B MoE, Terminal-Bench ~82.7.
  - 2026-08-08 (🟡): Açık betaya girdi.
  - 2026-08-10 (🟡): GA sürümü orta Ağustos'a ertelendi.

### 14. OpenAI Astra (matematik/araştırma modeli)
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-08-10 | Durum: Aktif
- Günlük:
  - 2026-08-07: ~2.000 dolarlık hesaplamayla 10 açık problemi Lean kanıtlarıyla çözdü; Gowers bir kanıtı yayına önerdi.
  - 2026-08-08 (🟢): 10 çözülememiş problem çözüldü; Fields madalyalı Jacob Tsimerman OpenAI'ye katıldı.
  - 2026-08-10 (🟢): Kanıtlar tartışmalı — Miller ve Fournier-Facio bazı kanıtların önceki fikirlere atıfsız dayandığını iddia etti, OpenAI çerçevelemesini revize etti. Anthropic'ten Alpöge, Fable 5'in 10 sonuçtan 5'ini bağımsız ürettiğini iddia etti (doğrulanmamış).

### 15. AB Yapay Zeka Yasası (AI Act) uygulama takvimi
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-08-07 | Durum: Aktif
- Günlük:
  - 2026-08-07: Madde 50 şeffaflık kuralları 3 Ağustos'ta yürürlüğe girdi (etiketleme, chatbot açıklama zorunluluğu, ceza cironun %7'sine kadar). Yüksek riskli AI hükümleri 2 Ağustos'ta yürürlüğe girdi.
  - 2026-08-08, 08-10: kontrol edildi, gelişme yok.

### 16. AI ajan ödeme altyapısı (agent payments)
- İlk görülme: 2026-08-07 | Son güncelleme: 2026-08-07 | Durum: Aktif
- Günlük:
  - 2026-08-07: Cloudflare "Wallets" ve MoonPay "PayBox" (x402 standardı) duyuruldu; Cloudflare "Agents Week" ajan kimliği/erişim/ödeme altyapısını ele aldı.
  - 2026-08-10: kontrol edildi, gelişme yok.

### 17. Prime Agent (Prime Intellect)
- İlk görülme: 2026-08-08 | Son güncelleme: 2026-08-10 | Durum: Aktif
- Günlük:
  - 2026-08-08: İlk takip. ARC-AGI-3 %95.5, kalıcı Python ortam bağlamı, MIT lisanslı.
  - 2026-08-10 (🟡): GitHub API ile doğrulandı — 12.064 yıldız, 1.215 fork, v0.7.0 yayınlandı. NOT: 08-08'deki "+235 yıldız" Trendshift HAFTALIK ARTIŞ verisiydi, toplam değil; düzeltildi.

### 18. Mistral Shieldstral
- İlk görülme: 2026-08-08 | Son güncelleme: 2026-08-08 | Durum: Aktif
- Günlük:
  - 2026-08-08: İlk takip. 3B parametreli çok modlu güvenlik sınıflandırıcı, çalışma zamanında düz metin politika kabul ediyor, tek 16GB GPU'da çalışıyor.
  - 2026-08-10: kontrol edildi, gelişme yok.

### 19. Çok modlu üretici modeller (DiffusionGemma, MiniMax H3)
- İlk görülme: 2026-08-08 | Son güncelleme: 2026-08-08 | Durum: Aktif
- Günlük:
  - 2026-08-08: DiffusionGemma: Gemma 4 tabanlı ayrık diffusion dil modeli, tek H100'de ~1500 token/sn. MiniMax H3: açık çok modlu, 15 saniyeye kadar 2K stereo sesli video.
  - 2026-08-10: kontrol edildi, gelişme yok.

### 20. AI ajan mimarisi/hafıza yaklaşımları (Karpathy, MCP spec, AKB)
- İlk görülme: 2026-08-08 | Son güncelleme: 2026-08-10 | Durum: Aktif
- Günlük:
  - 2026-08-08: Karpathy graph-tabanlı hafıza kalıcılığı üzerine 12 sayfalık doküman yayınladı. MCP 2026-07-28 spesifikasyonu stateless çekirdeğe geçti.
  - 2026-08-10 (🟡): dnotitia/akb öne çıktı — MCP üzerinden vault-scoped doküman/tablo/dosya, URI-graph; Recall@5 %98.4 iddiası. API ile doğrulandı: 140 yıldız, 238 commit, henüz release yok — erken aşama.

### 21. Anthropic Cowork
- İlk görülme: 2026-08-10 | Son güncelleme: 2026-08-10 | Durum: Aktif
- Günlük:
  - 2026-08-10: İlk takip. Claude Code'un ajan yeteneklerini teknik olmayan kullanıcılara taşıyan ürün; ~10 günde, ağırlıkla Claude Code'un kendisiyle geliştirilmiş.

### 22. Yerel/açık kaynak Cowork & Claude Code alternatifleri (Goose, Eigent)
- İlk görülme: 2026-08-10 | Son güncelleme: 2026-08-10 | Durum: Aktif
- Günlük:
  - 2026-08-10: İlk takip. Block Goose: yerel ve ücretsiz otonom kodlama ajanı. eigent-ai/eigent: "Open Source Cowork Desktop", API ile doğrulandı 14.898 yıldız / 1.761 fork; Cowork lansmanıyla yeniden gündeme geldi.

### 23. Salesforce Slackbot'un AI ajanına dönüştürülmesi
- İlk görülme: 2026-08-10 | Son güncelleme: 2026-08-10 | Durum: Aktif
- Günlük:
  - 2026-08-10: İlk takip. Slackbot; kurumsal veride arama, doküman taslağı ve çalışan adına görev yürütme yapabilen AI ajanına dönüştürüldü.

### 24. Yeni GitHub AI/agent repoları (haftalık tarama)
- İlk görülme: 2026-08-10 | Son güncelleme: 2026-08-10 | Durum: Aktif
- Günlük:
  - 2026-08-10: İlk takip (yıldızlar GitHub API ile doğrulandı). 3-10 Ağustos'ta oluşturulanlar: KKKKhazix/human-writing (2.157), Binaryify/open-kimi-ppt-skill (1.605, arşivlenmiş), ShawnPana/phone-harness (1.039), AMAP-ML/LongHorizon-Harness (527), fuxicodex/Fuxi (455), sv-number/mcp-server (377). Daha olgun ama bu hafta ivmelenenler: mattpocock/skills (211.720), msitarzewski/agency-agents (141.175, masaüstü uygulaması çıktı), zhaoxuya520/reverse-skill (22.895).

## Arşivlenmiş Konular

(henüz konu yok — ilk arşivleme 2026-08-17'de konu 10 için bekleniyor)

## Değişiklik Geçmişi

- 2026-07-22: Takip sistemi başlatıldı.
- 2026-07-27: 10 yeni konu (ilk aktif rapor).
- 2026-08-07: 7 yeni konu; üç ayrı dosyaya bölünmüş liste birleştirildi.
- 2026-08-08: 4 yeni konu, 7 konu güncellendi.
- 2026-08-10: 3 yeni konu, 9 konu güncellendi; GitHub konektörüyle repo bölümü gerçek API'den doğrulandı, 1 konu daha eklendi.
- 2026-08-10 (mimari değişiklik): Durum dosyası Google Drive'dan bu git deposuna taşındı. Sebep: Drive MCP'sinde üzerine yazma aracı yok, bu yüzden dosya her hafta yeni bir ID ile yeniden oluşuyor ve otomasyonun talimatı da her hafta kendini güncellemek zorunda kalıyordu — bu kırılganlık Temmuz'da veri kaybına yol açtı. Git'te dosya yolu sabit, güncelleme in-place, geçmiş commit'lerde. Ayrıca tüm yıldız sayıları API'den yeniden doğrulandı (prime-agent 12.064; reverse-skill 22.895 — daha önce hatalı 573; akb 140 — daha önce hatalı 7).
