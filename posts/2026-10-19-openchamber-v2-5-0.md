# OpenChamber v2.5.0

- Resmî sürüm: `v2.5.0`
- Yayın tarihi: 19 Ekim 2026, 16:27 UTC
- Resmî kaynak: [OpenChamber v2.5.0](https://github.com/openchamber/openchamber/releases/tag/v2.5.0)

## Değişiklikleri dosya içinde bulma ve sayfa notları

Changes ve Walkthrough panellerinde `Cmd/Ctrl+F` artık değişiklik kümesindeki tüm dosyalarda arama yapıyor. Eşleşme sayısı ile ileri ve geri gezinme düğmeleri aynı çubukta yer alıyor.

Agent'in sohbette gösterdiği sayfalar ile Files içindeki HTML dosyaları Annotate page düğmesini alıyor. Sayfanın bir bölümünü işaretleyip agente o bölümle ilgili değişiklik isteği gönderilebiliyor. Sohbette gösterilen sayfadaki metin seçilerek yorum, BTW, not veya sesli okuma isteği de oluşturulabiliyor.

## Oturumlar, kenar çubuğu ve mobil

Settings, yanıt tamamlandıktan sonra oturumları 30 dakika ile 3 saat arasında açık tutabiliyor. Bu seçenek tüm oturumlara veya seçilen oturumlara uygulanıyor. Kenar çubuğunun List görünümü, Sessions seçeneğiyle tüm projelerdeki oturumları zamana göre sıralıyor.

Birden fazla depo içeren proje klasörleri artık tüm issue ve PR kayıtlarını listeliyor ve arıyor. Proje menüsü Issues and PRs panosunu açıyor. Mobilde çalışma alanı sekmeleri Settings › General bölümünden gizlenebiliyor ve sıralanabiliyor. Uzun basma da sekme sırasını değiştiriyor.

## Düzeltmeler ve altyapı

Uzun süre kullanılan sohbetlerde mesaj kutusunun her akış adımında yeniden çizilmesi kaldırıldı. Auto, model seçmeden önce yerel sınıflandırıcıyı çalıştırıyor. Kaydedilmiş Auto modeli artık bulunamazsa sohbet çökmeden açılıyor.

Mobil tarafında dosya arama yeniden çalışıyor. Android klavyesindeki Backspace terminalde silme işlemi yapıyor ve terminale yapıştırma desteği geliyor. Aynı adresteki 2 sunucuyu eşleyen telefonlar birbirini ezmiyor; bilgisayar yeniden başlatıldıktan sonra telefonlar yeniden bağlanıyor.

Paketlenen masaüstü uygulaması Electron `44.9` kullanıyor. Windows ARM yükleyicisi ARM için derlenmiş OpenCode içeriyor. macOS masaüstü uygulaması için gereken en düşük sürüm macOS 13 oldu.

## Kaynak

Bu yazı, resmî yayın notlarının Türkçe özetidir. Ayrıntılar için [OpenChamber v2.5.0](https://github.com/openchamber/openchamber/releases/tag/v2.5.0) esas alınır.
