# OpenChamber v2.8.0 Türkçe Özeti

- **Düzeltme tarihi**: 22 Kasım 2026, 00:19 UTC
- **Sürüm**: [v2.8.0](https://github.com/openchamber/openchamber/releases/tag/v2.8.0)
- **Commit**: [release v2.8.0](https://github.com/openchamber/openchamber/commit/30c70496a5ca0105e04e60a783964576973edc8f)

## Yenilikler

- **Ajant çalışma durumu**: Her alt ajant satırı mevcut adımını gösterir ve Tüm alt ajantlar paneli listesini gösterir, stalled veya yanlış yolda geçen ajantı görmek için chat'ı açmadan
- **Çat mesajı seçimi**: Birden fazla mesaj seçip birlikte paylaşabilme; Shift ile aralık seçimi mümkün, Markdown veya tek görüntü olarak kaydetme seçenekleri
- **Composer chipleme**: Bağlantı dosyaları, resimler, konular, pull request'ler ve paylaşımlı sayfalar chiple olarak eklenir; chip'lar yerinize göre cümle içinde yer alır ve silinirse ekstraksyon da geri alınır
- **PDF mesaj açığı**: Çat mesajında PDF'ler belgenin içinde açılır dialog'da görüntülenir
- **Context kaynakları**: Session'ın yüklenmiş skill'leri listeler, hangi skill'ler aktif olduğunu görüntüler
- **Ajant çalışan oturumları**: Operator ajantının worker oturumları artık kenar çubuğunda oturumlar altında gruplanır, karışmaz
- **PR bekletme**: Ajant "Start runs without my approval" ayarıyla ayrılmadan PR'leri timer gibi bekletebilir
- **Board etiket filtreleme**: Repository listelerini etiketlere göre filtreleme, filtre hatırlanır
- **Proje notları ve todos**: Depo içinde notlar ve todos yaşayabilir, birlikte dolaşır
- **Dosya tabı yolu**: File tab menüsü yol kopyalar ve dosyayı gösterir
- **GitHub ayarları**: Her gh girişini lists the host maintains
- **Git comparison picker**: Her uzaktan default branch'i listeden önce listeler
- **Browser dev server**: Her dev serverin arkasında hangi işlemin çalıştığını panel naming'leri
- **Mobil ekran açık**: Session çalışırken telefon ekranı açık kalır
- **Mobil önizleme**: Telefonunda ajantın remote dev server'ını önizleme
- **Mobil Ayarlar > Hakkında**: Android'da uygulama release notlarını gösterir
- **Leads**: Yeni yönlendirme ile bir projesi çalıştırabilirsiniz; Lead, görevleri kendi alt oturumlarına dağıtır, geri döndükleriğinde kısa bir özet ve kabul için bir digest sağlar. Proje menüsünden Yeni lead başlatmak veya mevcut bir oturumu lead yapmak mümkündür.
- **OpenCode Server**: Tek bir OpenCode'u CLI ve TUI ile paylaşabilirsiniz. Ayarlar > Genel > OpenCode Server içinde shared service'i etkinleştirerek OpenCode'yu bağlayabilirsiniz. `opencode update` ile güncellendikten sonra bildirimin Update ve Reload OpenCode butonları hizmeti yeni sürüme taşır. OpenChamber eklentisini aynı bölümden ekleyerek OpenChamber'ın araçları orada da çalışır.
- **Chat: Activity üçüncü mod**: Show notes, araç satırlarını katmanlayıp adımlar arasında ne yazıldıysa görünür (teşekkürler @yulia-ivashko).
- **Chat: Shell bloğu**: Bittiğinde Run in terminal, proje terminallinde çalıştırır (teşekkürler @Cyneric).
- **Chat: Ofice dokümanları**: Orijinal dosya olarak eklenti, aracı düzenleyebilir. Her zaman kaydetmek, her zaman dönüştürmek veya sormak için Chat > Composer ayarını değiştirebilirsiniz (teşekkürler @cemarta7).
- **Files: Code comment**: Tüm dosya yerine kesin bir parçayı comment'lemek (teşekkürler @cemarta7).
- **Files: Image view**: Tüm pencereyi kaplayan görüntü açar (teşekkürler @Galnaz).
- **Sessions: Default model**: Proje dışı sohbetler kendi modeli, düşünme seviyesi ve aracına sahip olur (teşekkürler @Galnaz).
- **Mobile: Text/links/files sharing**: Son kullanılan projeye link ve dosya paylaşımı, Quick Settings tile'ından session başlatma (teşekkürler @gaojunran).
- **Mobile: Portrait phone tabs**: Dik ekran telefonlarında terminal sekmesi liste olarak açılır, yeniden adlandırma ve kapatma (teşekkürler @gaojunran).

## İyileştirmeler

- **Panels**: Bir panel'i başka bir panelden açtıysanız kapanırken önceki panele dönülür.
- **Chat: Wide Markdown tables**: Geniş tablolar chat genişliğine otomay genişleyeir (teşekkürler @chaosmanage).
- **Chat: Unread attachment**: Model okuyamazsa kaydedilen dosya olarak gelir, açarak okuyabilir (teşekkürler @chaosmanage).
- **Chat: Dropped provider**: Bağlantı hatası gösterilir, OpenCode yeniden deneme yapar, başarısız turn yok (teşekkürler @mv2sa).
- **Chat: Shell row**: Satır "Shell" readme, komut için alan bırakır.
- **Appearance**: Menüler ve popover'lar again cam yöntemi, composer ve durum pilleri dark temada birbirine daha yakın.
- **Sidebar**: Session listesi ajantlar çalıştırırken bile ymooth kalır (binlerce session olsa bile).
- **Worktrees**: Branch picker hızlı açılır, birçok branch olduğunda tek continuous list.
- **Usage**: Work status headline eklenti kullanımını, OpenRouter aylık harcamasını ve OpenCode Go'ın account adını içerir (teşekkürler @AlistairDClarke, @ghaabor ve @kennycch).
- **Desktop**: Tray menü ve its tooltip uygulamanın diliyle aynı olur.
- **Browser**: Browser panelinde Google oturum açma çalışır.
- **Chat: Markdown tables**: Genişlik uyumluluğu iyileşti.
- **Chat: Unreadable attachment**: Kaydedildi, model tarafından açılabilir.
- **Chat: Provider reconnection**: Retry gösterilir, failed turn yok.
- **Chat: Shell command row**: "Shell" etiketi, komut alanını ayırır.
- **Appearance**: Glass menus, closer composer/status pills in dark themes.
- **Sidebar**: Session list smoothly visible with thousands of active sessions.
- **Worktrees**: Branch picker opens fast, shows continuous list.
- **Usage headline**: Extension usage, OpenRouter monthly spend (with your own keys), OpenCode Go account name included.

## Düzeltilmeler

- **Desktop**: OpenCode Zen free modeller her mesajda usage limit error veriyordu; eklenti kaldırılıp Claude Agent bağlanıldı.
- **Desktop**: Claude "Bun is not defined" hatası; eski opencode-claude eklentisi kaldırıldı, Claude Agent bağlandığına göre çalışır.
- **OpenCode Server**: Shared service on iken About ve update notification restart isteği sıfır görünür; diagnostics yanlış OpenCode adını gösteriyordu.
- **Chat**: Late error kopisi running turn'ı durdurup tekrar gösteriyordu.
- **Chat**: Kaldırılan veya taşınan dosyaların kopyaları sunucaya kalırdı.
- **Chat**: Revote sonrası hemen gönderilen mesaj Revote bitmeden çıkabiliyordu.
- **Chat**: Revote sonrası git revert tamamlanmadan önce gönderilen mesaj çıkabiliyordu.
- **Sessions**: Farklı folder'da başlatılan artık gösteriliyor ve açılıyor, composer okuyup-readonly kalır.
- **Sessions**: Fork, önceki mesajları live update geldiğinde gösterir.
- **Sessions**: Silindiğinde chat folder da siliniyor.
- **Connection**: Server kaybolup tekrar gelince app kendi kendine connected görünür.
- **Git**: GnuPG kurulu ve SSH agent yoksa her hareket 1-3 saniye daha uzar.
- **Git**: Sadece yeni dosyalı stash empty gösterirdi.
- **Git**: Dosya yolu değil SSH anahtarını içeren kaydedilmiş anahtar clone içi hata verirdi.
- **Git**: Repository bağlamları remount sonunda kayboluyor.
- **GitHub**: Ayarlar'da devre dışı kalmışken gh hala çalışıyordu.
- **Files**: Tabs arası switching sonrası file tree boş görünüyordu.
- **Files**: Go to line fokus too late to type into.
- **Files**: File tabs mouse wheel ile scroll oluyordu.
- **Büyük spreadsheet**: Preview limit'ı aşan satır ve sütun sayısını rapor ediyordu.
- **Ayarlar**: Session link hala yüklenirken Ayarlar'i açtıysa kapanıyordu.
- **Usage**: Model checkbox'ları panel gösterdiği gibi görünüyor.
- **Usage**: Codex credits balance diğer kredit satırları gibi görünüyor.
- **Providers**: Zen provider "OpenCode Zen" olarak adlandırılıyor, bundled paketler yerinde kalıyor.
- **Worktrees**: Worktree, üzerindeki OpenCode configuration'ını honors.
- **Share pages**: Shared page viewer içinde scroll yapar, Windows build'ından shared sayfalar boş açılıyorymıyordu.
- **Layout**: Window too short olduğunda context rail scroll yapar.
- **Terminal**: Zoom kısayolları focused terminal's font boyutunu değiştirir.
- **Markdown**: Tables content yönüne göre yönlendirilir.
- **Board**: Phone list preview kapanınca konumunu korur.
- **Mobil**: Detaylı satır artık kendi içinde scroll yapmıyor.
- **Masaüstü**: Linux SSH one-time codes ister, cevapları sesli olarak okur.
- **Server**: Slow başlamış bir external OpenCode server tekrar kontrol ediliyor.
- **Server**: Cloudflare Access headers browser preflight check'ini pass ediyor.
- **Memory**: Invalid memory document diğer scope'ları duraksatmadan reddediliyor.
- **CLI**: `openchamber stop` sunucuyu öldürmeden önce kapatma süresi veriyor.
- **Bundled OpenCode**: 2.3.2'den 2.8.0'a güncellendi.
- **Server and CLI**: Currently written in TypeScript.

## İlgili dosyalar

- `CHANGELOG.md` - Tam değişiklik kaydı
- `packages/vscode/` - VS Code eklentisi değişiklikleri
- `packages/web/` - Web arayüzü ve server değişiklikleri