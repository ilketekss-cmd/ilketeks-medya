# TANRISAL KOD — tanrı nesne yazılmaz · yeni kod küçük ve tek işli · "kusursuz" ölçümle söylenir (KALICI · Fatih 21 Kas 2026)

Kullanıcı, 21-11-2026 (birebir; yapıştırılan metin yarıda kesik geldi, son madde "…Claude Code gibi araçlar için" diye bitiyor):
> "Tanrısal code" (God Code / God Object / God-tier code) ifadesi, kullanıldığı bağlama göre yazılım mühendisliğinden spiritüalizm ve oyun kültürüne kadar farklı anlamlar taşır.
> • Yazılım Mimarisi (God Object / God Class): Bir uygulamadaki neredeyse tüm verileri tutan, her şeyi kontrol eden ve birbirinden bağımsız çok fazla sorumluluğu üstlenen aşırı büyük sınıf veya modülleri tanımlayan bir karşıt örüntüdür (anti-pattern). Kodun bakımını ve test edilmesini zorlaştırdığı için kaçınılması gerekir.
> • Geliştirici Jargonu (God-Tier Code / Araçlar): Hata payı çok düşük, kaynakları (CPU, bellek) en verimli şekilde kullanan kusursuz kodları veya geliştiricilere olağanüstü hız kazandıran yapay zeka tabanlı kodlama araçlarını (örneğin Claude Code gibi araçlar için

Oturum sordu ("bu metinle ne yapayım"); cevap (birebir): *"Kural olarak kaydet"* (bulut oturumu 879efcd1).
Okuma notu — ③ TAHMİN: kesik metinden çıkarılan kapsam = "yeni kod tanrı nesne olmasın + büyük dosya daha da büyümesin + kusursuzluk ölçümle söylensin". Yanlışsa Fatih düzeltir. Fatih 19-11'de aynı terimi bir kez daha kullandı (birebir, envanterdeki sid 15ce560a kaydından: "Tanrısal kodlarıyla · altyapıyla · çalışmalarıyla tekrar kontrol et · güncelle"). ③ TAHMİN: orada terim övgü anlamında ("en güçlü kontrol seti") geçiyor; o günkü iki plan da böyle okuyup TAHMİN diye etiketledi (`plans/ULTRAPLAN-altyapi-55ccdd00-20261119.md:176` · `plans/filo-ideal-denetim-35f61242-20261119.md:86`). Bu kural iki anlamı da kapsar: madde 1–3 karşıt örüntü, madde 4 "kusursuz" iddiası.
Ölçülen durum (21-11, bulut klonu, `wc -l scripts/*.py`): 123 betiğin 32'si 1.000 satırın, 16'sı 2.000 satırın üstünde; en büyüğü `scripts/soz-defteri.py` 4.902 satır. Kural bugünkü kodu değil, bundan sonra yazılanı bağlar.

## Kural
1. **Tek iş.** Yeni betik tek iş yapar; birbirinden bağımsız ikinci sorumluluk ayrı dosyaya gider.
2. **Dosya 1.000 satırı geçmez.** Yeni dosya da, bugün eşiğin altındaki mevcut dosya da; geçecekse plana "neden bölünemedi" tek cümlesi yazılır.
3. **Büyük dosya daha da büyümez.** Bugün 1.000 satırın üstündeki dosyaya yeni sorumluluk eklenmez; onarım ve küçük ek serbest, ama dosya o commit'te net 200 satırdan fazla büyüyorsa SONUÇ satırında sayı + gerekçe yazılır.
4. **"Kusursuz kod" söylenmez; ölçülen söylenir.** Selftest + mutant + kapı rc'si adıyla ve sayısıyla yazılır (kanon 🛑 "0 hata" ölçülebilir kabul kapısıdır, mutlak garanti yok); hız ya da bellek iddiası ölçüm komutu olmadan yazılmaz.

Eşik notu: 1.000 ve 200 başlangıç eşikleridir. Satır sayısı sorumluluk sayısının VEKİLİDİR; sorumluluğu doğrudan ölçen araç yok (kanon 📊 🧟 "yeni tarayıcı YASAK" · 🧪 dört soru karşılanmadan yeni ölçer kurulmaz). Eşik taban sayım üzerinden seçildi (1.000 üstü dosya sayısı bugün 32). 200 eşiği ölçümden türetilmedi, seçildi; sonradan sınandı: son 30 günde bu 32 dosyaya dokunan 147 commit'in 8'i net +200'ü aşıyor (③ 21-11 sayımı). Madde yasaklamaz, sayı ve gerekçe ister.

## Muaf
Üretici betiğin çıktısı olan dosyalar · veri ve defter dosyaları · boyutunun çoğu selftest gövdesi olan dosya (gerekçesi SONUÇ'ta yazılarak).

## Sınırlar (bu kural açmaz)
- Mevcut büyük dosyaların bölünmesi bu kuralın işi değildir; her biri ayrı plan + selftest + ③ ister.
- Başkasının dosyasına yazma izni vermez (U2).
- claude-gelisim dosyaları yalnız ölçülür.
- Ayrı-onay sınıfı aynen.

## Ölçer
Filo sayımı: `wc -l scripts/*.py | awk '$2!="total"{if($1>1000)a++} END{print a}'` (taban 21-11: 32; hedef: artmaz). Commit başına: `git diff --numstat <taban> HEAD -- '*.py' '*.sh' '*.ps1'`. Dayatıcı YOK — `KIRILGAN · yazılı`; aynı sınıf ihlal n≥2 olursa koda çevrilir (kanon 4️⃣-2). Kanon bağı: 🏗️ · 🧪 · 8️⃣ (`ai-yazilim-denetim`); bu dosya onları gevşetmez. Kapsam notu: filo sayımı yalnız scripts/ kökündeki .py dosyalarını sayar. Kural .sh ve .ps1 dosyalarını ve alt dizinleri de bağlar, ama taban sayımı onları içermez (21-11: scripts/ kökünde 1.000 üstü 8 .sh/.ps1 dosyası; _EKIP/ ve artifacts/ altındaki aday ve mutant kopyaları sayılmaz).
