# STANDART HER DEPODA — filo kural seti tüm depolarda bayt-aynı durur · tek kaynak claude-config · ölçer ve eşitleyici `kural-yay.py` (KALICI · /herkes · Fatih 22 Kas 2026)

Kullanıcı, 22-11-2026 (birebir): *"Hepiniz, herkes artık bunu standartlaştırın. Artık bunu standartlaştırın tüm oturumlar için."* Kapsam kararı (AskUserQuestion, 22-11, bulut oturumu 689ad402): **"Tüm depolar (Önerilen)"** — aynı gün başka bir oturumdaki "3 depo" cevabından sonra, ölçüm gösterilerek soruldu.
Ölçülen sebep (22-11, bulut klonu): kural seti 33 depodan yalnız 3'ünde vardı (claude-config 10 · claude-takip 3 · claude-beyin 2). Bulut oturumu yalnız açıldığı deponun `.claude/rules/`'ini yükler ⇒ öteki 30 depoda açılan oturum hiçbir kuralı almıyordu. Başka yapay zekalara işaretçi (`AGENTS.md`) 32 depodan 1'inde, `GEMINI.md` 0'ında.

**Çalışma sırası ve tahmin kartı bu dosyada DEĞİL, `ideal-calisma.md`'dedir** (tek standart; aynı hüküm iki yerde yazılmaz). Bu dosya yalnız o standardın ve öteki kuralların her depoya nasıl ulaştığını söyler.

## Kural
1. **Tek kaynak claude-config `.claude/rules/`.** Öteki depolardaki kopyalar (claude-takip ve claude-beyin dahil) tüketicidir; kural değişikliği önce claude-config'e yazılır, sonra yayılır. Standart liste `scripts/kural-yay.py` içindeki `STANDART`'tır (claude-config'e özgü `bulut-main.md` ve `bulut-beyin.md` dışarıda).
2. **Ölç:** `python3 scripts/kural-yay.py --kontrol <depoların bulunduğu dizin>` (salt-okur; dosya sınıfı ESIT · EKSIK · ESKI · SAPMA, depo sınıfı TAM · EKSIK · SAPMALI · ENGEL).
3. **Eşitle:** `--yaz` EKSİK dosyayı ve ESKİ kopyayı (kanonun git geçmişindeki bir sürümle bayt-aynı) yazar; **SAPMA'nın (yerel düzenleme) üstüne asla yazmaz**, raporlar. Kanon değişince aynı komut kopyaları günceller. `AGENTS.md` / `GEMINI.md` yoksa kısa işaretçi yazar, varsa dokunmaz (standarda işaret etmeyen yerel dosya `YEREL` raporlanır).
4. **`--yaz` reddeder:** commit'lenmemiş kanon (rc 2) · symlink ya da depo dışına giden `.claude` / `.claude/rules` (U2) · dizin olmayan `.claude/rules` ya da düzenli dosya olmayan hedef (o depo ENGEL, koşu sürer) · yayın izi olan depo (`wrangler` · `netlify` · `vercel` · `CNAME` · kök `index.html` · deploy workflow'u), servis dizini ölçülüp `--yayin-onayli <depo>` verilmeden.
5. **Kapısı kırmızı depo:** depo kapısı yazımdan önce de kırmızıysa (bulutta çoğu PC yoluna bağlı) o depoya commit atılmaz; aynı komut kapısı yeşil makinede (PC) koşulur. Araç deterministik, iş kaybolmaz.
6. **Kanon ana dalda değilse yayılım "tamam" sayılmaz:** claude-config dalı `bulut-main.md` beş şartıyla main'e geçmeden kopyalar yetim kalabilir.
7. **PC:** M1'de `~/.claude` = claude-config ⇒ set M1 hesaplarına kendiliğinden gider; M2 ayağı `pc/M2-ilke-ai-ws/OTURUM-KANALI.md` isteğiyle (`kural-yay.py --yaz D:\`).

## Sınırlar (bu kural açmaz)
- 🔴 ayrı-onay sınıfı · U2 · ORTAK SINIR aynen. Kopya yaymak başka depoya main push izni değildir: claude-config dışında dal + taslak PR, birleştirme Fatih'te.
- Hesap girişi, başka yapay zeka çağrısı, PC dosyası bulutta `ÖLÇÜLEMEDİ (bulut)`.

## Ölçer
`scripts/kural-yay.py --kontrol` (taban 22-11: 32 kardeş depoda TAM 0 · EKSIK 31 · SAPMALI 1 · işaretçi yok 63); hermetik `--selftest` kapı ayağı `kural-yay-oz` (`scripts/oto-senkron-kapilari.tsv`). Tahmin kartının kalibrasyon ölçeri `ai-olcum/scripts/tahmin-kalibre.py` (`ideal-calisma.md` kart biçimini okur; n < 10 ⇒ ÖLÇÜLEMEDİ). Dayatıcı: yayılım kapısı eksikliği gösterir, engellemez — `KIRILGAN · yazılı`. Kanon bağı: kural ekleme kapısı ⓐ (ölçer adıyla yazılı) · 📣 · U2; bu dosya onları gevşetmez.
