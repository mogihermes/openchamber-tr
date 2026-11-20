# OpenChamber v2.7.3 Türkçe Özeti

- **Düzeltme tarihi**: 19 Kasım 2026, 22:06 UTC
- **Sürüm**: [v2.7.3](https://github.com/openchamber/openchamber/releases/tag/v2.7.3)
- **Commit**: [release v2.7.3](https://github.com/openchamber/openchamber/commit/cf18602cc77146f35e26e103dbee1ab8e218b663)

## Yenilikler

- **Ajant çalışma durumu**: Her alt ajant satırı mevcut adımını gösterir ve Tüm alt ajantlar paneli listesini gösterir, stalled veya yanlış yolda geçen ajantı görmek için chat'ı açmadan
- **Çat mesajı seçimi**: Birden fazla mesaj seçip birlikte paylaşabilme; Shift ile aralık seçimi mümkün, Markdown veya tek görüntü olarak kaydetme seçenekleri
- **Composer chipleme**: Bağlantı dosyaları, resimler, konular, pull request'ler ve paylaşımlı sayfalar chiple olarak eklenir; chip'lar yerinize göre cümle içinde yer alır ve silinirse ekstraksyon da geri alınır
- **PDF mesaj açığı**: Çat mesajında PDF'ler belgenin içinde açılır dialog'da görüntülenir
- **Context kaynakları**: Session'ın yüklenmiş skill'leri listeler, hangi skill'ler aktif olduğunu görüntüler
- **Ajant çalışan oturumları**: Operator ajantının worker oturumları artık kenar çubuğunda oturumlar altında gruplanır, karışmaz
- **PR bekletme**: Ajant "Start runs without my approval" ayarıyla ayrılmadan PR'leri timer gibi bekletebilir
- **Board etiket filtreleme**: Repository listelerini etiketlere göre filtreleme, filtre hatırlanır
- **Proje notları ve todos**: Depo içinde notlar ve todos yaşayabilir, bDepo ile birlikte dolaşır
- **Dosya tabı yolu**: File tab menüsü yol kopyalar ve dosyayı gösterir
- **GitHub ayarları**: Her gh girişini lists the host maintains
- **Git comparison picker**: Her uzaktan default branch'i listeden önce listeler
- **Browser dev server**: Her dev serverin arkasında hangi işlemin çalıştığını panel naming'leri
- **Mobil ekran açık**: Session çalışırken telefon ekranı açık kalır
- **Mobil önizleme**: Telefonunda ajantın remote dev server'ını önizleme
- **Mobil Ayarlar > Hakkında**: Android'da uygulama release notlarını gösterir

## İyileştirmeler

- **Masaüstü çok daha küçük uygulama**: Masaüstü uygulaması full command-line program yerine OpenCode sunucusunu taşır, kurulumda yaklaşık 170 MB tasarruf
- **Performance**: Streaming reply daha az çalışmalı gerektirir, binlerce session kenar çubuğunda olsa bile sidebar daha hızılı stabilize olur
- **Ayarlar güncelleme**: Sağlanan update About üst kısmında strip olarak görünür
- **Chat başlık folding**: Scroll up while okuyup ikçe konuyu başlığa collapsing
- **Yerel dictation**: Makinenin tüm core'larını kullanır
- **Git büyük repo**: Very large repository'larda status ve checkout responsive kalır

## Düzeltilmeler

- **Startup**: Masaüstü uygulaması ve VS Code eklentisi "Configured OpenCode binary not found" hatası alıyordu; Settings henüz taşıdığı OpenCode'yı gösteriyormuş
- **Startup**: Settings dosyasındaki damaged projects listi sunucuyu başlatmayı durduruyordu
- **Composer**: Sayfayi reload veya kapatmadan önce gönderdiğiniz prompt artık geri dönüyor, kaybolmuyor
- **Composer**: Modelin sadece text okuyan bir model'e gönderilen bir image artık hata vermez, dosya yolu olarak gelir
- **Chat**: Revote ardından hemen gönderilen mesaj Revote bitmeden önce çıkabilir
- **Chat**: Revote sonrası git revert tamamlanmadan önce gönderilen mesaj Revote bitmeden çıkabilir
- **Sessions**: Ajant başka folder'da başlattığı session artık gösterilir ve açılır, composer okuyup-readonly kalır
- **Sessions**: Fork, önceki mesajları shows when live update first arrives
- **Sessions**: Session silindiğinde chat folder da silinir
- **Connection**: Server kaybolduğunda artık app kendi kendine connected görünür
- **Git**: GnuPG kurulu ve SSH agent yoksa her git hareketi 1-3 saniye daha uzar
- **Git**: Sadece yeni dosyalı bir stash empty gösterirdi
- **Git**: Dosya yolu değil SSH anahtarını içeren kaydedilmiş bir anahtar clone içi hata verirdi
- **Git**: Repository bağlamları remount sonunda kayboluyor
- **GitHub**: github.com hesabı Ayarlar'da devre dışı kalmışken gh hala çalışıyordu
- **Files**: Tabs arası switching sonra file tree boş görünüyordu
- **Files**: Go to line fokus too late to type into
- **Files**: File tabs mouse wheel ile scroll oluyordu
- **Büyük spreadsheet**: Preview limit'ı aşan gerçek satır ve sütun sayısını rapor ediyordu
- **Ayarlar**: Session link hala yüklenirken Ayarlar'i açtıysa kapanıyordu
- **Usage**: Model checkbox'ları panel gösterdiği gibi görünüyor
- **Usage**: Codex credits balance diğer kredit satırları gibi görünüyor
- **Providers**: Zen provider "OpenCode Zen" olarak adlandırılıyor, bundled OpenCode paketleri yerinde kalıyor
- **Worktrees**: Worktree, üzerindeki OpenCode configuration'ını honors
- **Share pages**: Paylaşımlı sayfa viewer içinde scroll yapar, Windows build'ından shared sayfalar boş açılmıyor
- **Layout**: Window too short olduğunda context rail scroll yapar
- **Terminal**: Zoom kısayolları focused terminal's font boyutunu değiştirir
- **Markdown**: Tables content yönüne göre yönlendirilir
- **Board**: Phone list preview kapanınca konumunu korur
- **Mobil**: Detaylı satır artık kendi içinde scroll yapmıyor
- **Masaüstü**: Linux SSH one-time codes ister ve cevapları sesli olarak okur
- **Server**: Slow başlamış bir external OpenCode server tekrar kontrol ediliyor
- **Server**: Cloudflare Access headers browser preflight check'ini pass ediyor
- **Memory**: Invalid memory document diğer scope'ları duraksatmadan reddediliyor
- **CLI**: `openchamber stop` sunucuyu öldürmeden önce kapatma süresi veriyor
- **Bundled OpenCode**: 2.3.2'e güncellendi
- **Server and CLI**: Currently written in TypeScript

## Duzeltmeler

- **Bilinmeyen içerik**: Release notlarında belirtilen değişiklikler ve düzeltmeler

## İlgili dosyalar

- `CHANGELOG.md` - Tam değişiklik kaydı
- `packages/vscode/` - VS Code eklentisi değişiklikleri
- `packages/web/` - Web arayüzü ve server değişiklikleri