# İDEAL ÇALIŞMA STANDARDI — her oturum aynı sırayla çalışır · her iş tahminle başlar, ölçümle biter (KALICI · /herkes · Fatih 22 Kas 2026)

Kullanıcı, 22-11-2026 (birebir): *"Tüm dosyalara ulaş, tüm klasörlere ulaş, tüm hesaplara ulaş, tüm yapay zekalara ulaş. İdeal şekilde çalışmayı planla. Tanrısal kodlarla ideal şekilde çalışmayı planla. Hepiniz, herkes artık bunu standartlaştırın. Artık bunu standartlaştırın tüm oturumlar için. Kapsamlı planlayın. Altyapıyla kapsamlı planlayın. İdeal planlayın. Ölçülü planlayın. Hesap edilebilir planlayın. Tahminle planlayın. Tahmin de edin. İdeal tahminler de bulunun. Şimdi devam edin."*
Kapsam seçimi (AskUserQuestion, 22-11, bulut be00f1ac): **3 depo** — kaynak claude-config; claude-beyin ve claude-takip'te bayt-aynı kopya.
**Yollar:** bu dosyadaki bütün yollar (kurallar, `FATIH-GUNDEM.md`, `_KOL-ENVANTERI.md`, `scripts/`, `artifacts/`) **claude-config köküne göredir**; tek istisna `hafiza.md` (claude-takip `.claude/rules/`). Başka depoda açılan oturum bunları claude-config klonunda okur (bulut: `bulut-beyin.md` §4, ek depo; açamıyorsa `pano.md` PANO-BORCU yolu).
Ölçülen sebep (22-11): claude-config `.claude/rules/` altında 10 kural var ama hangisinin hangi sırayla uygulanacağı tek yerde yazılı değildi; envanterde 13 000+ KOL satırında iş tahmini ile gerçekleşeni yan yana yazan biçimli satır 0'dı (`TAHMİN` geçen 407 satır var, hiçbiri bu biçimde değil) ⇒ tahminlerin ne kadar tuttuğu ölçülemiyordu.

## Standart sıra — her oturum, her iş birimi
Bu dosya kural kopyalamaz; sırayı ve yeri gösterir. Ayrıntı ve sınır her satırdaki dosyadadır.
| # | adım | nerede |
|---|---|---|
| 0 | **Nerede olduğunu ölç** (bulut · M2 · M1) | `makineler.md` |
| 1 | **Açılışta oku:** beyin `STATE ## ŞİMDİ` · mülk STATE · `HANDOFF-LIVE ## SIRADAKİ` · `FATIH-GUNDEM.md` A–D · pano | kanon 5️⃣ · `bulut-beyin.md` §2 · `fatih-takip.md` 1 · `pano.md` 1 |
| 2 | **Hatırla ve öncülü sına:** daha önce çözüldü mü; dayandığın eski iddiayı yeniden ölç | `hafiza.md` (claude-takip) · `oncul-kontrol.md` |
| 3 | **Tahmin kartı + İLAN:** ilk yazımdan önce, kart ilan satırının içinde (aşağıda) | kanon 7️⃣-1 · `pano.md` 2 |
| 4 | **Zinciri ve altyapıyı kur:** tek komut ilgili halkaları çağırır; koşulu oluşan `/altyapi-<mülk>` sormadan | `skill-ideal.md` · kanon 8️⃣ |
| 5 | **Uygula:** tek iş, küçük dosya; boş görev ve gereksiz oturum yok | `tanri-kod.md` · `uyum.md` |
| 6 | **SONUÇ + GÖRÜLEN kartı:** beklenen ↔ görülen, commit, uzak = yerel | kanon 7️⃣-2 · `pano.md` 5 |
| 7 | **Bağımsız denetim (③):** İLAN ↔ SONUÇ çiftini yazan olmayan biri denetler (oturum içi taze ajan SONUÇ'tan önce de koşabilir) | kanon 7️⃣-4 · 6️⃣-2 |
| 8 | **Ana dala geçir:** beş şart | `bulut-main.md` (claude-config) |
| 9 | **Temiz bitir:** geçici dosya, yarım dal, yetim kayıt 0 | kanon 🧼 · `/temiz` |
Sesle yazdırılmış mesaj önce `sesli-mesaj.md` ile okunur (adım 1'den önce).

## Tahmin kartı — tek yeni hüküm
1. **İLAN satırına** (adım 3): `TAHMİN: süre <N> dk · ajan <N> · dosya <N> · ③ ilk geçiş TUTTU %<N> · risk <tek söz> · dayanak <ölçülmüş benzer iş + komutu>`
2. **SONUÇ satırına** (adım 6): `GÖRÜLEN: süre <N> dk · ajan <N> · dosya <N> · ③ <TUTTU|ŞARTLI|ÇÜRÜDÜ|BEKLİYOR> · sapma süre <±N>%` (③ henüz gelmediyse `BEKLİYOR`)
3. **Dayanaksız tahmin yazılmaz.** Dayanak ölçülmüş bir şeydir: envanterde benzer işin süresi, son günlerin ③ oranı, dosya sayısı. Dayanak yoksa alan `ÖLÇÜLEMEDİ` yazılır, sayı uydurulmaz (kanon 🛑). Kart ③ sınıfıdır (TAHMİN); karar metnine tek başına girmez.
4. **Süre = duvar saati, `date -u` ile ölçülür;** başlangıç İLAN anı, bitiş SONUÇ anı. Saat damgası tahmin edilmez (damga ölçülür); tahmin yalnız ileriye dönük iş içindir.
5. **Sapma büyükse ders:** |sapma| > %100 ise sebebi SONUÇ'ta tek cümle; aynı sebep n≥2 ⇒ kanon 4️⃣-2.
6. **"İdeal tahmin"** = geçmiş GÖRÜLEN kartlarının ortancasına dayanan tahmin. Kart sayısı ≥10 olunca dayanak olarak ortanca yazılır; öncesinde benzer tek iş yeter.

## Erişim — "tüm dosyalara, hesaplara, yapay zekalara ulaş"
Ulaşmak = her yüzeyi ölçmek, ulaşılamayana reçete yazmak. Oturum hesap açmaz, şifre görmez, kurulum yapmaz; bunlar Fatih'in elindedir (`FATIH-GUNDEM.md` C7–C9). Güncel tablo: `artifacts/ERISIM-TABLOSU-<tarih>-<sid8>.md` (ilk: `ERISIM-TABLOSU-20261122-be00f1ac.md`). 7 günden eski tablo yeniden ölçülmeden karar metnine girmez. Bir iznin varlığı kuralı gevşetmez (örnek: posta gönderme izni olan bağlayıcıyla da mail gönderilmez).

## Ölçer
- Kart kullanımı (claude-config kökünde): `grep -cE 'TAHMİN: süre ([0-9]+ dk|ÖLÇÜLEMEDİ) · ajan' _KOL-ENVANTERI.md` ÷ İLAN sayısı `awk -F'|' '$2 ~ /^ KOL-[^ ]+-[0-9a-f]{8} $/ && $3 ~ /<YYYY-MM-DD>/' _KOL-ENVANTERI.md | wc -l` · eşli kapanış: `grep -cE 'GÖRÜLEN: süre ([0-9]+ dk|ÖLÇÜLEMEDİ) · ajan' _KOL-ENVANTERI.md` (taban 22-11: 1 kart / 28 İLAN · 0 eşli; ilk kart bu kuralı yazan ilan).
- Kalibrasyon: GÖRÜLEN kartlarındaki `sapma süre` değerlerinin ortancası (hedef |ortanca| ≤ %50); kart <10 iken ÖLÇÜLEMEDİ.
- Kopya eşitliği: `sha256sum` üç depodaki `.claude/rules/ideal-calisma.md` aynı.
Dayatıcı YOK — `KIRILGAN · yazılı`; kart eksikliği n≥2 ölçülürse `scripts/ilan-yaz.py`'ye kol olarak koda çevrilir (sahibine U12). Kanon bağı: 🛑 (kaynak sınıfı) · 7️⃣ · 8️⃣ · 🥇-2 (BEKLENEN önce, GÖRÜLEN sonra); bu dosya onları gevşetmez.

## Sınırlar (bu kural açmaz)
🔴 ayrı-onay sınıfı (yayın · para · silme · geçmiş yazımı · mail gönderimi) · U2 tek yazıcı · ORTAK SINIR aynen. Görev/ajan/workflow açmadan önce tek cümle onay sürer (`uyum.md` 1). Kanon `CLAUDE.md` metnine bir şey eklemez.
