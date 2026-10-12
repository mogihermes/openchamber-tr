# OpenChamber v2.2.0 Türkçe özet

- Yayın tarihi: 8 Ekim 2026
- Resmî yayın: [OpenChamber v2.2.0](https://github.com/openchamber/openchamber/releases/tag/v2.2.0)

## Öne çıkanlar

- Kenar çubuğuna GitHub, GitLab ve Linear kayıtlarını listeleyen bir sorun ve pull request panosu eklendi. Önizleme üzerinden yorum, inceleme, birleştirme, kapatma, etiket ve gözden geçiren yönetimi yapılabiliyor. Bir kayıttan oturum veya worktree başlatılabiliyor.
- Ortam değişkenleri artık Ayarlar > Genel altında OpenCode, Git, terminal ve proje eylemleri için saklanabiliyor. Projeler kendi değişkenlerini ekleyebiliyor veya direnv, devenv ve Nix shell üzerinden yükleyebiliyor.
- Yeni oturumlar, sohbet içinde en son seçilen modeli kullanıyor. Proje ve genel ayarlardaki varsayılan model önceliğini koruyor.
- Agent menüsünde favori agent seçimi ve yalnızca favoriler arasında Tab ile geçiş eklendi. Agent rengi değiştirilebiliyor veya agent silmeden devre dışı bırakılabiliyor.
- Türkçe arayüz bu forkta varsayılan dil olarak ayarlandı.

## İyileştirmeler

- Mesaj içinde `$` yazarak skill seçimi eklendi. Mesaj başındaki `/` yalnızca komutları listeliyor.
- Paralel araç çağrıları durum satırında sayıyla gösteriliyor.
- Uzun sohbet mesajları katlanabiliyor. Dosya, bahsetme, skill ve snippet ekleri düzenleyicide ve gönderilmiş mesajlarda etiket olarak görünüyor.
- Git görünümü açık pull requestleri pano görünümüne benzer biçimde gösteriyor. Yayınlanmamış veya önde olan dal, pull request oluşturulmadan önce gönderiliyor.
- Zamanlanmış görevler model ve agent ayarlarını oturum varsayılanlarından alabiliyor. Son çalıştırmanın oturumuna doğrudan gidilebiliyor.

## Düzeltmeler

- SSH biçimindeki Git uzak adresleriyle fetch, pull, push ve sync işlemleri düzeltildi.
- Büyük skill klasörlerinin uygulamayı kilitlemesine yol açan yükleme sorunu giderildi.
- Zamanlanmış depo döngülerinin etkinleştirme ve duraklatma durumu doğru kaydediliyor.
- Sohbette düzenleyici büyürken oluşan kaydırma sıçramaları, uzun oturumların eksik açılması ve bazı mobil görünüm sorunları düzeltildi.
- Kullanım kotası verilerinin bazı kurulumlarda hata ile yüklenmesi düzeltildi.

## Not

Bu yazı resmî sürüm notlarının Türkçe özetidir. Ayrıntı ve eksiksiz değişiklik listesi için resmî yayına bakın.
