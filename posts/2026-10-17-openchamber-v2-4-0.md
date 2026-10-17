# OpenChamber v2.4.0

- Resmî sürüm: `v2.4.0`
- Yayın tarihi: 17 Ekim 2026, 00:52 UTC
- Resmî kaynak: [OpenChamber v2.4.0](https://github.com/openchamber/openchamber/releases/tag/v2.4.0)

## Yeni özellikler

Kenar çubuğundaki mağaza düğmesi, Linear, Sentry, Figma, Notion ve Supabase gibi 160'tan fazla hizmeti içeren entegrasyon kataloğunu açıyor. Bir hizmetin MCP server'ı, skill'leri veya plugin'leri tek tıklamayla kurulabiliyor. Sayfa, giriş yapılması gereken hizmetleri de gösteriyor.

Dosya ağacının üzerindeki arama alanı artık dosya içeriğinde arama yapıyor. `.*` anahtarı düzenli ifadeleri açıyor. Eşleşen satıra tıklamak dosyayı doğrudan o satırda açıyor.

Agent, seçenekleri bir sayfada gösterip kullanıcı seçim yapana kadar bekleyebiliyor. Seçim aynı turda agente dönüyor. `Cmd/Ctrl+Shift+L`, bağlantı ve OpenCode olaylarının zaman çizelgesini açıyor. Bu kayıt `.log` olarak indirilebiliyor; yollar ve oturum başlıkları kayda eklenmiyor.

SearXNG, Brave Search ve Kagi gibi plugin sağlayıcıları Settings → Web search bölümünden bağlanabiliyor. Resource Monitor entegrasyonu CPU ve bellek kullanımını makine, OpenChamber, OpenCode ve geliştirme sunucuları için gösteriyor.

## Sohbet, oturumlar ve dosyalar

Yan panel, bağlı PR, merge request, issue veya Linear kaydını ayrı sekmede açıyor. Etkinlik, kontroller, yanıt ve birleştirme işlemleri uygulama içinde kalıyor. Açık dosyalarda aynı ada sahip sekmeler klasör yolunu da gösteriyor.

Sabitlenmiş oturumlar cihazlar arasında eşitleniyor. Tree görünümündeki In work ve Pinned satırları alt oturumları açabiliyor. Sohbet sekmeleri çalışan veya kullanıcı girişi bekleyen oturumları gösteriyor.

## Düzeltmeler

Sürüm, boşta beklerken de CPU ve GPU kullanımını azaltıyor. Büyük dosya ağacı açıkken yan panelin açılıp kapanması akıcı hale geliyor.

Agent geri alma işleminden sonra proje notlarını, planlarını veya belleğini kaybetmiyor. Notlar sıkıştırma ve fork sonrasında da korunuyor. Sohbet metni ve tablolar yan panel açıldığında genişlik değişse de konumunu koruyor. Run through Code Mode açıkken agent sayfaları yeniden gösteriliyor.

Uzaktan erişimde, aynı kurulumun 2 kopyası artık relay bağlantısını birbirinden almıyor. Bir veri klasörü başka bilgisayara kopyalanırsa Settings → Connect to this server bu bilgisayar için ayrı relay kimliği oluşturuyor. Boşta kalan telefon da sunucuya her 5 saniyede bir güncelleme isteği göndermiyor.

## Diğer değişiklikler

SDK ile geliştirilen extension'lar, yeniden derleme gerektirmeden açık ve koyu temalarda uygulamanın yükseltilmiş kontrollerini ve çerçevesiz alanlarını kullanıyor. Paketlenen OpenCode sürümü `2.0.32` oldu.

## Kaynak

Bu yazı, resmî yayın notlarının Türkçe özetidir. Ayrıntılar için [OpenChamber v2.4.0](https://github.com/openchamber/openchamber/releases/tag/v2.4.0) esas alınır.
