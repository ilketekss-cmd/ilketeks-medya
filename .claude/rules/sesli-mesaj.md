# SESLİ MESAJI DOĞRU ANLAMA — Fatih'in sesle yazdırdığı mesaj kelimesiyle değil sesiyle ve bağlamıyla okunur (KALICI · Fatih 22 Kas 2026)

Kullanıcı, 22-11-2026 (birebir): *"Konuşmayı yazıya çevirmeyi bu oturumun yaptığı gibi yapmayı tüm yapay zekaları muzda /altyapi mizda /esitle /zincir"*. Oturum sordu (AskUserQuestion: sesli mesajı doğru anlama · düz Türkçe rapor · panoya kayıt · ses→yazı aracı); cevap: **"Sesli mesajı doğru anlama"** (bulut oturumu e209b6f2).
Ölçülen durum (22-11): Fatih mesajlarının bir kısmını telefonda sesle yazdırıyor; ses tanıma kelimeleri bozuyor ("Claude bin", "AG'yi", "muzda"). Kelimesi kelimesine okuyan oturum ya yanlış işe gider ya "böyle bir şey yok" der. Aynı gün bu oturum bozuk sözleri bağlamla çözdü, iki anlamlı kalan tek sözü seçenekli tek soruyla netleştirdi. Sözlüğün 4 satırı bu oturumun okumasıdır, 3 satırı 11-10 ve 14-10 tarihli skill okuma notlarından alındı (sesle mi yazıldı, klavye hatası mı, ölçülmedi).
Kendi hatam (③ ayrı alt-ajan 22-11 yakaladı): bu kuralın ilk yazımında envanter ilanı ve commit mesajı Fatih'in sözünü "birebir" diye **düzeltilmiş** hâliyle aktardı ("yapay zekalarımızda") — kuralın reddettiği körlüğün kendisi. Birebir alıntı yukarıdaki satırdır.
Bu dosya `.claude/rules/` altında; claude-config'te açılan her Claude oturumuna (bulut dahil) kendiliğinden yüklenir. Codex · Kimi · Cursor ajanlarına `AGENTS.md`, Gemini ajanlarına `GEMINI.md` → `AGENTS.md` üzerinden ulaşır.

## Yöntem — beş adım
1. **Sesi oku, harfi değil.** Anlamsız ya da depoda karşılığı olmayan söz önce ses benzerliğiyle depodaki adlara eşlenir: komut (`/esitle`), mülk/depo (claude-beyin), kural adı (tanrısal kod), oturum kimliği, kişi rolü. Türkçe ekler sık kopar ya da öne yapışır ("muzda" = "-mızda").
2. **Bağlamla doğrula.** Eşleşme son mesajlarla, açık işle ve envanterle tutarlı mı bakılır. Tutarsızsa eşleşme kurulmaz.
3. **Okumayı yaz.** Cevapta bir kez, kısa: *Okuma: "AG'yi" = AGI'yi.* Kaynak sınıfı ③ TAHMİN'dir; Fatih düzeltebilsin diye görünür yazılır, sessizce kesin sayılmaz.
4. **İki yola ayrılıyorsa tek soru.** Okumalar farklı işe götürüyorsa işe başlamadan **tek** seçenekli soru sorulur (AskUserQuestion; önerilen ilk sırada; kanon 8️⃣ gereği soru `ai-otonom` yoluyla tek reçeteye iner). Anlam değişmiyorsa soru sorulmaz; her belirsizlikte soru yağdırmak sesli mesajı yorar (kanon 🔥: soru yalnız gerçek yön/kapsam seçiminde).
5. **Doğrulanan okuma sözlüğe girer.** Fatih seçimiyle ya da düzeltmesiyle doğrulanan okuma aşağıdaki tabloya bir satır olarak eklenir (önce ara, mükerrer yok; yanlış çıkan satır silinmez, `SÜPERSEDE`).

## Reddedilen körlük
- Harfi harfine okuyup "anlaşılmadı / böyle bir şey yok" demek (kanon 🛑 YOK/0 kapısı: görmediğin anlam yok sayılmaz).
- Tahmini sessizce kesin saymak; yanlış okumayla iş açmak.
- Aynı mesaj birkaç kez gelince körü körüne baştan başlamak: önce neyin karşılanmadığı `/karsila` ile ölçülür (kanon 🧩-10), soru ancak ölçüm iki yol bırakırsa adım 4'e göre sorulur. Aynı metin tüm oturumlara toplu yapıştırılmış da olabilir (`.claude/rules/uyum.md` madde 3).

## Sözlük (yalnız ölçülmüş ya da depoda yazılı okumalar)
| duyulan / yazılan | kastedilen | durum | kaynak |
|---|---|---|---|
| "AG'yi kontrol et" | AGI'yi kontrol et | doğrulandı | 22-11 mesajı; Fatih "AGI kontrolü tanımlansın" seçeneğini seçti (e209b6f2) |
| "yapay zekaları muzda /altyapi mizda" | yapay zekalarımızda / altyapımızda | ③ TAHMİN (dolaylı: Fatih'in seçimi bu okumayla kurulan soruya verildi, okumanın kendisi onaylanmadı) | 22-11 mesajı (e209b6f2) |
| "Claude bin" | claude-beyin | ③ TAHMİN | 22-11 mesajı "Deriz ki Claude bin şu an bulutta açık"; bağlam claude-beyin deposu (e209b6f2) |
| "zinir i" | zinciri | depoda yazılı (sesli olduğu ölçülmedi) | `skills/zincir/SKILL.md:102` ⑧ okuma notu (11-10) |
| "dogrula ma" | doğrulama | depoda yazılı (sesli olduğu ölçülmedi) | `skills/zincir/SKILL.md:102` ⑧ okuma notu (11-10) |
| "sem yönet" | sen yönet | depoda yazılı (sesli olduğu ölçülmedi; klavye kayması olabilir) | `skills/zincir/SKILL.md:157` ⑩ okuma notu (14-10) |
| "konuşmayı yazıya çevirmek" | sesli mesajı doğru anlama (bu kural) | doğrulandı (niyet ayrımı, tanıma hatası değil) | 22-11 AskUserQuestion cevabı (e209b6f2) — adım 4'ün örneği |

## Sınırlar (bu kural açmaz)
- Okuma ③ TAHMİN'dir: karar metnine (STATE · kanon · Fatih raporu) tek başına giremez; 🔴 ayrı-onay işini (yayın · para · silme · geçmiş yazımı) okumaya dayanarak başlatmak YOK — önce sorulur.
- Bu kural yalnız oturuma gelen yazıyı okumayı anlatır; ses kaydı, telefon mesajı ya da e-posta okuma izni vermez (`.claude/rules/fatih-takip.md` › Sınırlar geçerli); üçüncü kişi adı sözlüğe yazılmaz.
- Kanonu gevşetmez; 🛑 UYDURMA YOK aynen.

## Ölçer
Sözlük satır sayısı: `grep -cE '^\| "' .claude/rules/sesli-mesaj.md` (taban 22-11: 7). Yanlış okumanın bedeli = aynı isteğin yeniden gönderilmesi: kanon 🧩-10 ölçeri `scripts/soz-defteri.py` (yinelenen söz; PC'de çalışır, bulutta ÖLÇÜLEMEDİ). Okuma satırı (`Okuma: "…" = …`) cevap metnindedir, depoya düşmez ⇒ oturum başına sayılamaz. Dayatıcı YOK — `KIRILGAN · yazılı`. Kanon bağı: 🛑 (kaynak sınıfı, YOK/0) · 🧩-1 · 🧩-10 · 🗣️-4 · U14; bu dosya onları gevşetmez.
