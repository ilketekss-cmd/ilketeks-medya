# HAFIZA — her oturum hafızayla ve hatırlayarak çalışır (yerel + bulut)

Kullanıcı, 19 Kas 2026: *"herkes Claude beyinle çalışsın, hafızayla çalışsın, hatırlayla çalışsın."*
Bu dosya `.claude/rules/` altında; yerel ve bulut her oturuma kendiliğinden yüklenir. Kural metni kopyalamaz, **yer gösterir**.

## Hafıza nerede (ortama göre)
| Ortam | Hafıza | Beyin (kanon · ders · STATE) |
|---|---|---|
| **M2** (W111) | `C:\Users\W111\.claude\memory-ortak\` (indeks `MEMORY.md`, durum `SON-DURUM.md` ilk 60 satır) | `D:\m1-beyin` (= claude-config klonu, salt-okuma) + `D:\claude-beyin` |
| **M1** (Fatih) | `claude-config/ortak-hafiza/` | claude-config kökü (`CLAUDE.md`, `KANON-DETAY.md`, `DERSLER.md`, `STATE-*.md`) |
| **Bulut** | claude-config klonunda `ortak-hafiza/MEMORY.md` (M1 indeksi); M2 hafızası ayrı depodur (`ilketekss-cmd/memory-ortak`, ek depo olarak açtırılırsa okunur) | claude-config klonu (`bin/bulut-acilis.sh` çeker) |

## Sıra
1. **Açılışta oku:** kendi ortamının durum dosyası (M2: `SON-DURUM.md` ilk 60 satır · bulut/M1: `STATE-claude-beyin.md` `## ŞİMDİ` ilk bloğu) + bu deponun `OTURUM-KANALI.md` son bloğu.
2. **Konuya girmeden hatırla:** *"bunu daha önce çözdük mü / ne karar verdik"* → `/hatirla` (anlamdan) ya da `/beyin-ara` (kelimeden; M2'de üç kökü birden tarar). Bulduğunu **açıp doğrula**, dosya yolu + tarihle aktar; 90 günden eski hükmü yeniden ölçmeden karar metnine alma.
3. **Öğrendiğini yaz:** hata düzeltildi / yaklaşım onaylandı → `/ders` (atomik not + indeks satırı). Ortamının hafızasına yaz; başka makinenin ağacına yazma.
4. **Kapanışta devret:** durum dosyası + kanal bloğu (oturumlar birbirini canlı görmez; tek ortak yüzey disk/depo).

## Bulut oturumu hafızaya yazamıyorsa
Dersi kendi deposunda `.claude/pano-borcu/<tarih>-<sid8>.md` dosyasına **"HAFIZA-BORCU"** başlığıyla yaz, commit'le, kullanıcıya bildir; sonraki PC oturumu hafızaya taşır.
