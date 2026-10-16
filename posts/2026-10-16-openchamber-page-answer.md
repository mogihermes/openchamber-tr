# Agent sayfada seçim isteyebiliyor

- Tarih: 16 Ekim 2026, 00:45 UTC
- Kaynak commit: [`2b94db8470ca77d946917e937e3b04d7b0b678bc`](https://github.com/openchamber/openchamber/commit/2b94db8470ca77d946917e937e3b04d7b0b678bc)

## Ne değişti

`openchamber_render` ile gösterilen sayfalar artık `awaitAnswer` alabiliyor. Agent, tasarım veya yerleşim seçeneklerini sayfada gösterebiliyor; kullanıcı bir düğmeye bastığında `openchamber.submit(data, summary)` ile yanıt aynı turdaki agente dönüyor.

Yanıt, çağrının metaverisinde tutuluyor ve istemciler sayfa yenilendikten sonra da görebiliyor. Aynı oturumda herhangi bir gönderenden gelen sohbet mesajı beklemeyi bitiriyor. Tur durdurulursa sayfa yanıtlanmamış olarak kalıyor.

Yanıt bekleyen sayfa, bekleyen form gibi işleniyor. Kenar çubuğu, mobil görünüm, tray ve çalışma rozetleri, `Input needed` bildirimi, uygulama içi bildirim ve boşta duran space'i durdurma mantığı bu durumu dikkate alıyor. Bekleme sırasında yazılan sohbet mesajı kuyruğa alınmadan doğrudan gönderiliyor.

Kaynak commit, yanıt kaydı, HTTP rotası, sayfa ayrıştırma, bekleyen istek indeksi, bildirimler ve idle stop için birim ve rota testlerinin yanında headless Chrome, WebKit, masaüstü ve telefon üzerinde manuel test yapıldığını belirtiyor.

## Kaynak

Bu yazı, resmî OpenChamber commit açıklamasının Türkçe özetidir. Ayrıntılar için [`2b94db8470ca77d946917e937e3b04d7b0b678bc`](https://github.com/openchamber/openchamber/commit/2b94db8470ca77d946917e937e3b04d7b0b678bc) esas alınır.
