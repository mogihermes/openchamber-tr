# Small Model üretim süresi istem boyutuna göre uzuyor

- Tarih: 18 Ekim 2026, 08:09 UTC
- Kaynak commit: [`006c75ae77b06f2561f0b5dcb0409d33086bd141`](https://github.com/openchamber/openchamber/commit/006c75ae77b06f2561f0b5dcb0409d33086bd141)

## Ne değişti

Small Model ile üretim için sabit 60 saniyelik süre sınırı kaldırıldı. Süre, gönderilen istemin boyutundan hesaplanıyor: 60 saniye temel süreye, tahmini her token için 40 ms ekleniyor. Hesap yaklaşık 4 karakteri 1 token sayıyor ve 900 saniyede duruyor.

Bu değişiklik, uzun istemlerde veya yerel modellerde üretimin erken kesilmesini azaltıyor. Çağıran kod `timeoutMs` verirse bu değer geçerli kalıyor.

SDK uzantılarındaki `generate` bekleme süresi `90 s` değerinden `960 s` değerine yükseltildi. En büyük izinli uzantı istemi için sunucunun hesapladığı süre `780 s` olduğundan, yanıt üretilirken uzantının bağlantıyı erken kapatması engelleniyor.

Süre dolarsa API `504` ve `generation-timeout` kodunu döndürüyor. Hata iletisi seçilen modeli ve o istem için hesaplanan süreyi içeriyor.

## Kaynak

Bu yazı, resmî OpenChamber commit açıklaması ve değişikliklerinin Türkçe özetidir. Ayrıntılar için [`006c75ae77b06f2561f0b5dcb0409d33086bd141`](https://github.com/openchamber/openchamber/commit/006c75ae77b06f2561f0b5dcb0409d33086bd141) esas alınır.
