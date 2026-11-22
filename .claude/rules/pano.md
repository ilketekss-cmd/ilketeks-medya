# PANO — her iş panoya yazılır (KALICI · /herkes · tüm oturumlar · bulut dahil)

Kullanıcı, 17 Kas 2026: *"bulut oturumu panoyu da okusun · buluttaki tüm çalışmalar da panoya yazılsın · herşey panoda olacak · /temiz ve /kontrollü çalışılacak · tüm oturumlar, tüm işlerde geçerli · doğrulanacak · /zincirleyin · orkestratörler ile çalışın · /herkes"*

Bu dosya `.claude/rules/` altında; yerel ve bulut her oturuma kendiliğinden yüklenir.

## Pano nerede
GitHub `ilketekss-cmd/claude-config` deposu:
- `_KOL-ENVANTERI.md` — İLAN / SONUÇ / DEVİR satırları (tek yazım yolu `scripts/ilan-yaz.py`)
- `ledger/karar-kuyrugu.jsonl` — görev kuyruğu · `HANDOFF-LIVE.md` — devir notları
- Görünüm: `python3 scripts/is-panosu.py liste` (okuma; komut yürütmez)

## Her oturum, her iş — sıra
1. **AÇILIŞ: panoyu oku.** claude-config kökünde `python3 -I -X utf8 scripts/is-panosu.py liste | head -40` + kendi mülkün: `grep -n "KOL-<mülk>-" _KOL-ENVANTERI.md | tail -20`. Açık kalem varsa önce onu üstlen.
2. **İLAN (ilk yazımdan önce):**
   `python3 -I -X utf8 scripts/ilan-yaz.py --envanter _KOL-ENVANTERI.md --satir '| KOL-<mülk>-<KALEM>-<sid8> | <tarih> (UTC) · sid <sid8> · <makine: bulut|M2|M1> · BEKLENEN … | <dosyalar> | - |'`
   Önce `--kuru` ile dene. Bulut oturumu satıra **`· bulut ·`** yazar.
3. **/zincir:** planla → /kontrol → uygula → /kontrol. Ölçülebilir kabul kriteri olmayan işe zincir açılmaz.
4. **/temiz + /kontrol + /dogrula:** her iş temiz biter (geçici dosya, yarım dal, yetim kayıt kalmaz), çıktı kontrol edilir, her iddia komutla yeniden ölçülür. Kanıtsız "bitti" yok.
5. **SONUÇ (iş sonunda, aynı KOL kimliğiyle):** `| KOL-…-<sid8> · ✅ SONUÇ | … BEKLENEN ↔ GÖRÜLEN · commit sha · ls-remote yerel=uzak |`. Bitmediyse **DEVİR** satırı.
6. **Push:** claude-config'e commit + push; kanıt `git ls-remote origin main` == `git rev-parse HEAD`.

## Orkestratör
Çok parçalı işte orkestratörle çalış (Agent ekibi / Workflow; `model` boş). 🪤 Kullanıcının kalıcı kuralı geçerli: **görev/ajan/workflow oluşturmadan önce tek cümleyle onay al**, onay görev başınadır. Ajan raporu ölçüm değildir; rakamı ana oturum yeniden ölçer.

## Bulut oturumu claude-config'e erişemiyorsa
- Oturumu **claude-config ek depo** olarak yeniden açtır (bulut ortamı "claude-beyin filo" ile panoya yazan bulut oturumları var: envanterde `· bulut ·` satırları).
- Yine olmuyorsa işi **yapma diye durma**; kendi deposunda `.claude/pano-borcu/<tarih>-<sid8>.md` dosyasına İLAN+SONUÇ satırını yaz, commit'le, kullanıcıya **"PANO-BORCU"** diye bildir. Sonraki PC oturumu bu satırı panoya taşır.

## Skill'ler
`/herkes` `/temiz` `/zincir` `/kontrol` `/dogrula` gövdeleri: claude-config `skills/<ad>/SKILL.md`. Oturumda kurulu değilse dosyayı oku ve uygula.
