# OpenChamber v2.3.2 Türkçe özet

- Yayın tarihi: 14 Ekim 2026, 00:39 UTC
- Resmî yayın: [OpenChamber v2.3.2: Project knowledge for agents and Linux packages](https://github.com/openchamber/openchamber/releases/tag/v2.3.2)
- Kaynak commit: [`601babc783c77c51c58e56e7003e17c9105faef8`](https://github.com/openchamber/openchamber/commit/601babc783c77c51c58e56e7003e17c9105faef8)

## Yeni özellikler

- Ayarlarda bellek seçeneğinin yanında açılan Project knowledge ile agent'lar proje notlarını, yapılacaklarını ve planlarını kendi araçlarıyla okuyup düzenleyebiliyor. Agent'ın gösterdiği plan Project knowledge panelinde açılıyor.
- GitHub, GitLab ve Linear issue, pull request ve merge request bağlantıları oturumun yanındaki issues board'da açılıyor. Masaüstünde Settings → General içindeki `Open links in the built-in browser`, diğer bağlantıları tarayıcı panelinde açıyor. `Cmd/Ctrl-click` sistem tarayıcısını kullanmaya devam ediyor.
- Linux için x64 ve arm64 mimarilerinde AppImage'ın yanında `.deb` ve `.rpm` paketleri eklendi. Paketler uygulamayı simgesiyle uygulama menüsüne koyuyor ve güncellemeyi parola onayından sonra uygulama içinden kuruyor.
- Daraltılmış kenar çubuğu, pencerenin sol kenarında imleç bekletildiğinde sohbetin üstünde açılıyor. Pinned bölümü de görünüm menüsünden In work üstüne eklenebiliyor.
- Project actions, `Cmd/Ctrl+Alt+R` ya da komut paletinden açılan iletişim kutusuyla başlatılıp durduruluyor. Masaüstünde üstte sabit açılan Mini Chat penceresi de var.

## İyileştirmeler ve düzeltmeler

- Project knowledge paneli sekme, arama ve ortak ekleme alanı kazandı. Not, plan veya belleği silme işlemi 5 saniye içinde geri alınabiliyor.
- Sohbette asistan görselleri metindeki konumunda gösteriliyor. Ekran görüntüsü paragrafları tek satırda gruplanıyor. Kısa mesaj balonları gereksiz sol boşluk bırakmıyor.
- Yan panel açılış animasyonu sohbeti kaydırmıyor. Çalışma durum satırı son sohbet satırını kapatmıyor ve kendi kaydırma çubuğunu oluşturmuyor.
- Değişiklik görünümündeki seçili diff düzeni hatırlanıyor. Issues board son açık öğeyi, aramayı ve kaydırma konumunu koruyor.
- Mobilde sessions sheet, issues board ve Git drawer daha az satır kullanıyor. Git drawer içinden AI review başlatılabiliyor.
- Git hesabıyla fetch, pull, push ve PR worktree işlemleri `safe.directory` ile güvenilen depolarda çalışıyor. GitLab 18.0 öncesi self-managed örneklerde merge request değişiklikleri, kontrolleri ve gözden geçirenleri gösteriliyor.
- Ayar dosyaları atomik değiştiriliyor. OpenCode yarım yazılmış yapılandırmayı okumuyor, symlink hedefi korunuyor ve salt okunur yapılandırmaya dokunulmuyor.
- Paketlenmiş OpenCode sürümü `2.0.28` oldu.

## Kaynak

Bu yazı, resmî OpenChamber yayın notlarının Türkçe özetidir. Eksiksiz değişiklik listesi için [resmî yayın](https://github.com/openchamber/openchamber/releases/tag/v2.3.2) esas alınır.
