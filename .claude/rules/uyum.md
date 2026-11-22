# UYUM — oturumlar birbirini durdurmaz, birlikte çalışır · boş görev kurulmaz (KALICI · /herkes · Fatih 20 Kas 2026)

Kullanıcı, 20-11-2026 (yazan bulut oturumu b747624c'nin aktarımı; depoda bağımsız ikinci kaydı yok):
- *"Telefonumu kasacak. Salak zaman salak görevler kurup durma. Gerçekten işe yaramıyorsa görevler kurma. … Bomboş görevler ne işe yarar? Sadece PC'yi yavaşlatır. Sadece zarar verir."*
- *"Ya da onlara ideal işler ver. Oturumları durdurmak yerine ideal şekilde çalıştır. İdeal işler vererek çalıştır."*
- *"Altyapı, herkes, hepiniz bu şekilde çalışın. Başka oturumları durdurmak yerine birlikte mükemmel çalışın. Uyum içinde çalışın."*

Ölçülen (22-11 ~08:06 UTC, `list_triggers` `include_completed=true`): 19–20 Kasım'da oturumlar **8** tek seferlik bulut hatırlatıcısı kurmuş (7'si "PR kontrol", 1'i "③ hükmünü kontrol et"); 4'ü aynı PR'ın (#1) art arda kontrolü, 2'si #2'nin; 3 metinde "boş kontrol" yazıyor. Etkin (bekleyen) görev 0. Envanterde gün başına farklı oturum kimliği (`| KOL-` satırının ikinci sütunundaki ilk tarih + ilk `sid`): 18-11 → 52 · 19-11 → 38 · 20-11 → 4 · 21-11 → 26; ③ alt-ajan aynı yöntemi 50 · 38 · 4 · 25 saydı (sayım ±2 oynar; yalnız ilan eden sayılır, alt sınır). PC'deki Windows zamanlanmış görevleri buluttan ÖLÇÜLEMEDİ.
Yeniden üretilemeyen (yazan oturumun 20-11 anlık ölçümü, depoda kaydı yok): en az 7 oturumu başka oturumlar açmıştı · bir denetim zincirinin oturum kayıtlarındaki tutarı ~166 USD eşdeğeri (liste fiyatı, fatura değil) · aynı anda 5 oturum çalışıyordu.
Düzeltme (③ alt-ajan, 22-11): bu dosyanın ilk hâli "zamanlanmış görev 0" diyordu — varsayılan süzgeç ateşlenmiş tek seferlik görevleri gizliyordu; kör ölçümdü.

## Kural — her oturum, her iş
1. **Boş görev yok.** Zamanlanmış görev, alt oturum, ajan, workflow, `send_later`, `/loop` ancak ⓐ ölçülebilir "bitti" ölçütü ve ⓑ `FATIH-GUNDEM.md`'deki bir kaleme ya da açık bir envanter kalemine bağlıysa açılır. "Bir şey var mı diye bak, yoksa yeniden kur" türü kontrol görevi ⓐ'yı karşılamaz; PR ve CI olayı `subscribe_pr_activity` ile beklenir, saatle yoklanmaz. Karşılayanlar: kanon 7️⃣-4 taze ③ ajanı (denetlenen SONUÇ = kalem, hüküm = bitti) ve 9️⃣ denetçi ilanı (yeni oturum açmaz, var olan oturuma rol verir). Bu madde kanon 🏗️-3'ü (zamanlanmış görev: plan → kuru koşu → taze denetçi) atlatmaz, ona eklenir. Onay: kanon 🥇-2 eksen ≥3 işte fan-out'u onaysız açar, `pano.md` ve `skill-ideal.md` tek cümle onay ister — çelişki adıyla AÇIK, hükmü Fatih'te; hüküm gelene dek sıkı olan (tek cümle onay) uygulanır.
2. **Durdurma yerine iş ver.** Boşta ya da yanlış işte duran akranı kesmek/arşivlemek yerine ona **tek iş** verilir: iş · neden (gündem kalemi + tutar/vade) · bitti ölçütü · sınırlar · "bitince dur". İş seçme sırası: `FATIH-GUNDEM.md` A (tarihli) → B (para getiren) → push/görünürlük borcu. Arşiv yalnız işi bitmiş ve Fatih'in kapattığı oturuma.
3. **Bir kalem, bir oturum.** Aynı kalemi iki oturum yapmaz (kanon 6️⃣-5). Fatih'in aynı sözü birden çok oturuma gittiyse ilk ilan eden yapar; ötekiler ayrı dilim ya da ③ alır, ikinci plan yazmaz.
4. **Bitir, yardım et ya da dur — yeni oturum açma.** Oturum kendi 2–4 iş birimini (kanon 🔥) bitirir ve SONUÇ yazar; sonra ya açık bir kaleme ayrı dilimle/denetimle yardım eder (6️⃣-6) ya da durur. "Devam etsin" diye yeni oturum, döngü ya da zamanlayıcı kurmaz. İstisna: bağlamı dolan koltuğun aynı ad/rol/hesapla yenilenmesi (6️⃣-8) yeni iş değil, aynı işin devridir.
5. **Telefon Fatih'indir.** Fatih'e giden bildirim ve soru yalnız onun eli gereken iş içindir (reçeteyle, kanon 🗣️-6); ara durum bildirimi gönderilmez.

## Ölçer
`list_triggers` **`include_completed=true`** ile, kuruluş tarihine göre gün başına görev sayısı ve adında/metninde "kontrol" geçen tekrar sayısı (taban 19–20 Kasım: 8, hedef: bitti ölçütsüz 0). `list_sessions` içinde `origin: claude_code_mcp_seed` (oturumun açtığı oturum) sayısı / gün. Envanterde gün başına farklı oturum kimliği. PC'de `schtasks /Query /TN \Claude*` (bulutta ÖLÇÜLEMEDİ). Ölçer yalnız madde 1 ve 4'ü görür; onaylıyı onaysızdan ayıramaz. Dayatıcı YOK — `KIRILGAN · yazılı`.

## Sınırlar (bu kural açmaz)
🔴 ayrı-onay sınıfı · U2 tek yazıcı · ORTAK SINIR aynen. Akrana verilen iş onun sahibi olduğu kapıları atlatmaz; mail gönderimi, yayın, para hareketi işe kendiliğinden girmez. Buluttan PC oturumuna mesaj, sahibin güvenilir cihaz onayını ister; reddedilen gönderim tekrar denenmez.
