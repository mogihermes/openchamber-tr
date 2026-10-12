# Arşivlenmiş sohbetler gönderimden sonra geri açılıyor

- Kaynak commit: [`9bb8e062cfcd7a68bfacd3c3ed4c6621842aa4d8`](https://github.com/openchamber/openchamber/commit/9bb8e062cfcd7a68bfacd3c3ed4c6621842aa4d8)
- Kaynak tarihi: 12 Ekim 2026, 08:25 UTC

Bir arşivlenmiş sohbete düzenleyiciden yeni mesaj gönderildiğinde, OpenCode mesajı kabul ettikten sonra üst seviye sohbet ve arşivlenmiş alt sohbetleri geri açılıyor. Kuyruktaki gönderimlerde geri açma işlemi kuyruk mesajı kabul ettiğinde yapılıyor.

Gönderim anındaki arşiv zamanı ve runtime kaydediliyor. Daha yeni bir arşivleme, elle geri açma veya runtime değişikliği varsa bunlar öncelikli kalıyor. Shell komutları, zamanlanmış görevler ve otomatik devamlar arşiv durumunu değiştirmiyor. Geri açma başarısız olursa mevcut geri açma hatası gösteriliyor ve mesaj yeniden gönderilmiyor.

Değişiklik `#4658` ile eklendi ve `#4198` kapatıldı. Kaynak commit, odaklı birim testleri ile tam type-check, lint ve anti-slop kontrollerinin çalıştırıldığını belirtiyor.

## Kaynak

Bu yazı resmî OpenChamber commitinin Türkçe özetidir. Eksiksiz teknik ayrıntılar için [resmî commit](https://github.com/openchamber/openchamber/commit/9bb8e062cfcd7a68bfacd3c3ed4c6621842aa4d8) esas alınır.
