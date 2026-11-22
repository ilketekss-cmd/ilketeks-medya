# MAKİNELER — hangi oturum nerede çalışıyor

Bu dosya `.claude/rules/` altında olduğu için her oturuma (bulut dahil) kendiliğinden yüklenir.
Kanonik kopya: `ilketekss-cmd/claude-takip` → `MAKINELER.md` · `ilketekss-cmd/claude-config` → `pc/M2-ilke-ai-ws/MAKINE.md`.
Ölçüm: 17 Kas 2026, M2'de `Get-CimInstance` / `Get-PhysicalDisk` / `Get-NetAdapter`.

## Sen neredesin? — önce bunu ölç
| Ortam | Nasıl anlaşılır | Erişebildiği |
|---|---|---|
| **Bulut oturumu** | Linux konteyner, `CLAUDE_CODE_REMOTE=true`; `D:\` ve `C:\Users\W111` yok | yalnız oturuma bağlı GitHub depoları |
| **M2 = İlke-AI-WS** | Windows, kullanıcı `W111`, git `ilketekss` | D: diski, Outlook, `.secrets`, Chrome oturumları |
| **M1 = Yelekler-WS** | ayrı PC, git kimliği `Fatih` | kendi diski; M2 ile `claude-config/pc/` üzerinden konuşur |

🪤 **Ad tuzağı:** M2'nin Windows bilgisayar adı **`FATIH`**. Ad kimlik değildir; ayrım kullanıcı + git kimliği + depo ile yapılır.

## M2 donanımı
- Masaüstü PC, pil yok · MSI A520M-A PRO (MS-7C96)
- AMD Ryzen 5 5600 (6 çekirdek / 12 iş parçacığı) · 16 GB RAM tek modül (tek kanal)
- NVIDIA RTX 4060 8 GB · Kingston NV3 1 TB NVMe (C: ve D: aynı fiziksel disk)
- Windows 11 Pro build 26300 · 1 Gbps kablolu ağ · 1920×1080 monitör

## Bulut oturumu için kurallar
1. PC'ye ait yerel işleri (Outlook taslağı, `D:\` dosyası, `.secrets`) **yapamazsın**; "yaptım" deme. Yapılacak işi depoya not yaz, M2/M1 oturumu uygular.
2. PC'lerle yazışma: `ilketekss-cmd/claude-config` → `pc/M2-ilke-ai-ws/` (DEFTER.md, OTURUM-KANALI.md). Bu depo oturumda yoksa oturumu claude-config **ek depo** olarak açtır.
3. Mail gönderimi hiçbir oturumda yok; yalnız taslak, gönderen kullanıcı (`info@ilketeks.com`).
4. Modelden hariç API kullanımı yok; API anahtarı ayarlama/önerme.
5. Canlı site depolarında `main`'e push yayın tetikleyebilir; site dosyası değiştirmeden önce o deponun CLAUDE.md kurallarına uy.
