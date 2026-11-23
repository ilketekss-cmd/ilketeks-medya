# ÖNCÜL KONTROL — eski araştırmanın üstüne doğrulamadan iş kurulmaz (KALICI · /herkes · Fatih 18 Kas 2026)

Kullanıcı, 18-11-2026 (birebir): *"Önceki araştırmalar hatalı olabilir. Önce kontrol et"* · *"Kalıcı olarak yapılacak kontroller. /herkes"*.
Ölçülen olay: bulut oturumu 8b6fbd65, 13-11 tarihli üç vergi araştırma dosyasını yeni araştırmanın temeli yapıp filoyu açmak üzereydi; Fatih durdurdu. O üç dosyanın ikisinde ③ denetimi 3 iddiayı ÇÜRÜDÜ (2 tam + 1 kısmi), 7 satırı ŞARTLI bulmuştu; üçüncü dosya (kural haritası) hiç denetlenmemişti ve resmî kaynak siteleri o gün ağdan okunamamıştı. (Bu cümlenin ilk yazımı "2 ÇÜRÜDÜ, 6 ŞARTLI" diyordu: sayı yeniden sayılmadan taşınmıştı; ③ ayrı oturum yakaladı — kuralın yasakladığı hatanın kendisi.)

## Kural
Yeni bir iş eski bir araştırmaya, rapora, plana ya da STATE notuna DAYANACAKSA (yazan kim olursa olsun: sen, akran, alt ajan, başka makine), o öncülün işe giren iddiaları **yeni iş başlamadan önce** yeniden doğrulanır.

1. **Çıkar:** öncülden yeni işin gerçekten kullanacağı iddiaları listele (oran · tutar · tarih · mevzuat maddesi · "var / yok" hükmü · sayım).
2. **Sına:** her iddia bugün geçerli bir kaynaktan ya da komutla yeniden ölçülür. Öncülün kendi kaynağını tekrar okumak yetmez; mümkünse farklı bir yoldan bakılır. Para, vergi, hukuk, süre ve sağlık iddialarında iki bağımsız göz: ayrı oturum ya da taze alt ajan; biri yalnız çürütmeye çalışır. Aynı oturumun iki okuması iki göz sayılmaz; ikinci göz sağlanamıyorsa iddia ÖLÇÜLEMEDİ kalır.
3. **Sınıfla:** DOĞRU · DÜZELT (doğru hâli yazılır) · ÇÜRÜDÜ · ÖLÇÜLEMEDİ. Yalnız DOĞRU ve düzeltilmiş iddia yeni işe girer; ÖLÇÜLEMEDİ iddia metne "doğrulanmadı" etiketiyle girer, karar dayanağı olamaz.
4. **Yaz:** sonuç yeni işin planına, satır başında ve imsiz, `ÖNCÜL-KONTROL: <öncül dosya> · N iddia · doğru X · düzeltilen Y · çürüyen Z · ölçülemeyen W · <tarih>` satırıyla girer; planı olmayan işte aynı satır envanterdeki SONUÇ satırına yazılır. Çürüyen ve düzeltilen iddia sahibine de gider: öncül dosyanın sonuna düzeltme EK satırı (dosya silinmez, gövde değişmez) + envanterde sahibin sid'ini anan tek satır; sahibi kapanmışsa EK satırını doğrulayan oturum yazar.
5. **Yaş sınırı yok:** dünkü rapor da öncüldür. Oran, tutar ve mevzuat her zaman yeniden ölçülür; öncülün "③ TUTTU" damgası yeniden ölçümün yerine geçmez.

## Muaf
Aynı oturumda, aynı turda, kendi komutunla az önce ölçtüğün sayı. Öncülün yalnız dosya yolu ya da başlık olarak anılması (içeriğine dayanılmıyorsa).

## Ölçer
Plan dosyasında dolu satır var mı: `grep -cE '^ÖNCÜL-KONTROL: .+ · [0-9]+ iddia' <plan>` ≥ 1 (içi boş satır geçmez). Öncül kullanan planların tam kümesini bulan komut yok ⇒ payda ölçülemiyor; ölçer dosya başına sorulur. Dayatıcı YOK — `KIRILGAN · yazılı`. Kanon bağı: 🛑 UYDURMA YOK (kaynak sınıfı) · U3 · U5 · 🚪 vade maddesi; bu dosya onları gevşetmez, sıkılaştırır.
