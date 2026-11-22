# TEK KOMUT YETER — yazılan komut, ilgili bütün komutları ideal sırayla çalıştırır (KALICI · Fatih 18 Kas 2026)

Kullanıcı, 18-11-2026 (birebir): *"yazdığım herhangi bir skill Tüm skill ler i /ideal şekilde kullansın. /uygula"*.
Ölçülen sebep (18-11, bulut oturumu 8b6fbd65): Fatih aynı isteği dört kez gönderdi; her seferinde komut listesini elle uzattı (`/planla /arastir /karsila /karne /altyapi` + `/zincir`, sonra `/altyapi-claude-beyin`, sonra `/altyapi-ai-uygulama-takip`, sonra `/doldur`). Komutları saymak Fatih'in işi olmamalı. Aynı sınıf daha önce de ölçüldü: aynı 10 halkalık liste 24 saatte 23 oturuma yapıştırıldı (`skills/zincir/SKILL.md` H6).

## Kural
> Okuma notu (kaynak sınıfı ③ — TAHMİN: Fatih'in sözündeki "/ideal şekilde" = en uygun sırayla ve yalnız ilgili komutlarla; `/ideal` komutunun kendisi zincire yalnız mülk ölçümü gerekiyorsa girer. Yanlışsa Fatih düzeltir.) Aynı söz 19-10'da da söylendi; o günün planı `plans/skill-ideal-plan-119a6f35-20261019.md` açık duruyor, bu dosya onu tamamlar.
Fatih tek bir komut (skill) yazdığında oturum, o işin ideal zincirini KENDİSİ kurar ve koşar; Fatih'in öteki komutları tek tek yazmasını beklemez.

1. **Zinciri kur.** Yazılan komut zincirin bir halkasıdır. İşin türüne göre eksik halkalar eklenir. Sıra, tekil yükleme ve bağlam bandı kuralı `skills/zincir/SKILL.md` gövdesindedir; burada yeniden tanımlanmaz. İşin gerektirmediği halka atlanır ve atlandığı tek satırla yazılır.
2. **Koşulu olan altyapı komutunu ekle.** Kanon 8️⃣ koşul tablosunda koşulu OLUŞAN her `/altyapi-<mülk>` sormadan çağrılır (kod değiştiyse yazılım denetimi, sayı karar metnine girecekse ölçüm, hukuk boyutu varsa avukat, ≥3 eksense kadro). Koşulu oluşmayan çağrılmaz.
3. **"Tümü" = ilgili olanların tümü.** İdeal kullanım her komutu yüklemek değildir; gereksiz yüklenen komut bağlamı doldurur ve işi yavaşlatır. Ölçü: zincirdeki her halkanın yanında "neden var" tek cümlesi.
4. **Zinciri göster, sonra koş.** İlk mesajda halka tablosu (halka · neden · bitti ölçütü) tek blok olarak yazılır; onay beklenmez, koşulur. Kırılan halka zinciri durdurur ve adıyla yazılır.
5. **Sonunda karşıla.** Fatih'in söylediği her kalem teslim edilenle yan yana konur; karşılanmayan adıyla ve sebebiyle yazılır.
6. **Kurulu olmayan komut.** Komut oturumda yoksa gövdesi `skills/<ad>/SKILL.md` dosyasından okunur ve uygulanır. PC yoluna bağlı adımı bulutta koşulamıyorsa "ÖLÇÜLEMEDİ (bulut)" yazılır, atlanmış sayılmaz.

## Sınırlar (bu kural açmaz)
- Ayrı onay sınıfı aynen: yayın · para · geçmiş yeniden yazımı · mail gönderimi · başkasının dosyasına yazma zincire kendiliğinden girmez.
- `/uygula` halkası kendiliğinden EKLENMEZ: `skills/uygula/SKILL.md` FAZ 0 ve `skills/zincir/SKILL.md` ⑤ kapısına tabidir. Fatih `/uygula` yazmadıysa zincir plan denetiminde durur. Yazdıysa da plan denetimi temiz değilse uygulama başlamaz; onay yoksa yalnız yerel ve geri alınabilir adımlar koşar.
- Yazan (②) ile denetleyen (③) aynı oturum olamaz; zincir bunu kısaltmaz.
- Açık "dur / bekle / kapat" zinciri keser.
- Görev, ajan ve iş akışı oluşturmadan önce tek cümle onay kuralı (Fatih 19-09) sürer; yalnız ajanı, filoyu ya da ekibi adıyla anan söz ("filo ile", "ekip") o iş için onay sayılır, sonraki iş için sayılmaz. "Uygula" sözü ajan açma onayı değildir.

## Ölçer
Aynı isteğin ikinci kez gönderilme sayısı (`/karsila` gerekçesi: n≥2 yinelenen söz karşılanmamış taleptir): ölçer adıyla `scripts/soz-defteri.py` (yinelenen söz) ve `scripts/mulk-gate.sh` "AYNI İSTEM" bandı; ikisi de PC'de çalışır, bulutta ÖLÇÜLEMEDİ (bulut). Hedef 0. Dayatıcı YOK — `KIRILGAN · yazılı`. Kanon bağı: 8️⃣ (altyapı talimatsız çağrılır) · 🔥 (varsayılan ilerle) · 🧩-10 (yinelenen söz); bu dosya onları gevşetmez, tek komuta indirir. PC tarafında kanona işlenmesi ve 18-11 sözlerinin söz arşivine yazılması ayrı kalemdir (kuyrukta kayıtlı).
