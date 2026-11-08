# OpenChamber v2.7.0 Türkçe Özeti

- Düzeltme tarihi: 8 Kasım 2026, 02:37 UTC
- Sürüm: [v2.7.0](https://github.com/openchamber/openchamber/releases/tag/v2.7.0)
- Commit: [release v2.7.0](https://github.com/openchamber/openchamber/commit/651a0564880633fbcdc2ac3f84d08e42c7748a64)

## Yenilikler

- **/new-extension komutuyla kendi eklentilerinizi oluşturun:** İstediğiniz özellikleri tanımlayın, ajent eklentiyi yazar ve kur butonu chat'inizin sağ kısmında gösterilir. Eklentiler artık chat'ta çizebilir, ajentin sorularına cevap verebilir, oturum üzerinde kendi eylemine geçebilir, eylem ve @ satırı ekleyebilir ve güncellemeler sunabilir.
- **Word, PowerPoint, Excel ve OpenDocument dosyaları:** Dosya görüntüleyicisinde açılırlar. Tablolar sıralayabilir, filtreleyebilir, boyutlandırmayı uygulayabilir ve formüllerle Düzenlemek mümkündür. Seçili hücreler veya metin composer'a quote olarak gönderilir, ajantın değiştirdi hücreler işaretlenir.
- **Cmd'den komut çalıştırma:** Ajantın cevabı içinde kod blokları çalıştırılır. Çıktı blok içinde gösterilir ve ajant komut bittiğinde devam eder.
- **SQLite, Parquet, zip ve Jupyter dosyaları:** Salt okunur açılır. Office dosyaları Değişiklikler içinde karşılaştırılır ve pulled request'lar oluşturulur. Markdown Word ve PDF'e, CSV ise Excel'e dışa aktarılabilir.
- **Session Toplar kartı:** Tüm oturmanın girdiyi, çıkışı, mantığı, cache okuma/yazma ve cache verim oranını gösterir. Çalışma durumu son reply'nin cache verim oranını gösterir.
- **Görsel session etkileri:** Ajant arka planda oluşturduğu oturum görseli sidebar'da görünür. Composer'da listing edilir until kaydedilir.
- **Gitea entegrasyonı:** `gt` CLI ile login olunmuş Gitea örnekleri Ayarlar > Entegrasyonlar'da görünür ve gt CLI signaturasıyla OpenChamber'a token olmadan oturum açılabilir.
- **Ajant sınırları:** Ajant provider limitlerini kontrol edebilir ve sıfırlandığında bilişir. Ayarlar > Genel > OpenChamber Tools (rebelliard'a teşekkürler) Agent kullanım aracını açabilirsiniz.
- **Worktearown teardown komutları:** Projeler listeleyebilir ki worktree silinmeden önce çalıştırılacak commands. Başarısız teardown worktree'ı tutar ve "Delete without teardown" seçeneği sunar (JosueGalRe'a teşekkürler).
- **Klavye kısayolları:** Her komut Ayarlar'da listelenir ve palette komutları bir anahtar alabilir. Sayfa arama destekler ve kısayola temizleme yapılabilir (nickchomey ve ykai55'e teşekkürler).
- **Eklenti anahtarı:** Her eklenti kartı üzerinde aç/kapa anahtarı konfigürasyon girişini ve seçenekleri tutar (jwcrystal'a teşekkürler).
- **Chat yazı boyutu:** Sohbeti büyütür veya küçültür, geri kalan etkilenmeden. (dangreenlee'a teşekkürler).
- **Yeni chat formu:** Tabs ayrılmış bir bekleme formu. Her tabın sonunda Next butonu ve son tabda Send butonu (JosueGalRe'ya teşekkürler).
- **Cevap bekleme formu:** Ajantın size sorsun bekleyen sayfa. Tabs ile bölünür, her tabın sonunda Next butonu ve sonunda Send butonu. Ajant'in sizin "Decline" (Reddedi) bildirimi aldığında size seçim yapmaz (yulia-ivashko'a teşekkürler).
- **Tav séçinde thumbs-up:** Seçim menüsüne thumbs-up atarak passage'ı "Sounds good" yorumu ile ekler, bunu göndermeden önce düzenleyebilirsiniz (ChangeHow'a teşekkürler).
- **Gizli istek göz ikonu:** Gizli bir istek üzerinde eye butonu. Sorduğunuzdan önce ne yazdığınızı gösterir. (Naputt1'e teşekkürler).
- **Session ID'ler linklere dönüşür:** Composer'a pasted session ID, o session'a link olur. (yulia-ivashko'a teşekkürler).
- **Shift+Enter numaralı listaye devam eder:** Composer'da Shift+Enter tuşları numaralı listedeki sonraki satıra devam eder (gabrielantoniosilvaoficial'a teşekkürler).
- **Mobil: Tüm telefon uygulaması geçişi:** Her ekranda aynı üst çubuk. Her dialog ve picker bottom sheet olarak opens. Bağlantı ekranı ve Instanslar bir görünüm. Git sekmesi, Ayarlar ve editorun find bar telefon için oluşturulmuştur.
- **Dosya: 100.000 satırlık workbook veya millions satırlı SQLite dosyaları gibi büyük tablolar ve veritabaları app'yi donmadan açılır.**
- **Mobile: Pencere attached comment'leri comment field'ine düzenleme açar.** (yulia-ivashko'a teşekkürler).
- **Mobile: Tüm ekranda aynı üst çubuk.** Her dialog ve picker bottom sheet olarak opens. Bağlantı ekranı ve Instanslar bir görünüm. Git sekmesi, Ayarlar ve editorun find bar telefon için oluşturulmuştur. (yulia-ivashko'a teşekkürler).
- **Mobile: Dosya yolu veya changed file under reply'i tıklandığında açar.** Browser back butonu topmost sheet'i kapatır. Phone rotasyonu landscape tutar. (yulia-ivashko/mv2sa'a teşekkürler).
- **Mobile: Session switcher recent activity'ye göre sıralama.**

## İyileştirmeler

- **Mobil: Tüm telefon uygulaması pass over.** Her ekranda aynı üst çubuk. Her dialog ve picker bottom sheet olarak opens. Bağlantı ekranı ve Instanslar bir görünüm. Git tab, Settings ve editorun find bar phone için built.
- **Dosya: 100.000 satırlık workbook veya millions satırlı SQLite dosyaları gibi büyük tablolar ve veritabaları app'yi donmadan açılır.**
- **Chat: OpenChamber ve OpenCode kendi araçları yaptıklarını gösterir.** "Remembered" veya "Session renamed" gibi. Expanded row result draws. Screenshot row'da link açar.
- **Chat: PR güncellemesi tek satırda.** Dilinizde bir satır. Pull request'a açar, GitLab'da merge request der.
- **Sidebar: Her liste içinde klasörler.** Zaman ve In work listesinde. Move to folder her satırda available.
- **/btw: Ajant seçin.** Model ve thinking level ile normal kısayollarla tercih edebilir ve own thinking level after answer'ı korur (epustobaev'a teşekkürler).
- **Desktop: 10 MB üzeri dosya nota olarak attach.** Agent dosya ihtiyaçlarını okur. Büyük PDF'ler context'yi aşmıyordu, EPUB'ler dışarı atılırdı.
- **Ajant: OpenChamber aracları her zaman Code Mode üzerinden çalışır.** Session ilk request'i yaklaşık 30% daha küçük. Ayarlar > Genel > OpenChamber Tools'daki ayar kaldırıldı.
- **Session warming: Warm session, model cache'inin expiration'una antesinden ping gönderir.** Saat uzunluğunda cache' olan modeller çok daha az ping ihtiyacını vardır.
- **Goals ve ready bildirimleri:** Subagent'lar ve ajant tarafından.generate images için bekler.
- **Ajant: Session beklerken ne beklediğini söyler.** Yanlış session ID "not found" der.
- **Side panel: Butonlar language'lı tooltips.** (Cyneric'a teşekkürler).
- **Composer: Thinking level after model name level renkli.** @ listesi @ genişliğine kadar genişler. (yulia-ivashko'a teşekkürler).
- **Work status: Context sources Usage'dan sonra gösterilir.**
- **Changes: Last turn Changed view picker.** Last turn nothing için Changed'da gösterilir.
- **Comments: Her oturumda gönderilmeyen comment korunur.** (lesderid'a teşekkürler).
- **Sessions: Folder açmadan move works.** Window current chat folders gösterir when comes back. Late move newer'i undo edemez.
- **Archived sessions sidebar'a döndürülmez.** (mattv8'a teşekkürler).
- **Auto routing: Plan sonra bir sonraki request replaced agent'e gönderilir.** (yulia-ivashko'a teşekkürler).
- **MCP: Remote MCP server sign-in başka makineden tamamlanır.** Private relay üzeründen pasted address browser'a landetini gösterir.
- **Plugins: Broken plugin switch file OpenCode başlatmayı durdurmaz.** Her config file'ından okuyanlar listesini sayfa listeler (zerone0x ve yulia-ivashko'a teşekkürler).
- **Settings/Skills: Skills kapalıysa off gösterir.** Switch comments'ını opencode.jsonc'de korur (zerone0x ve yulia-ivashko'a teşekkürler).
- **Usage: Codex numbers.** OpenChamber ile ChatGPT signed in ve Codex CLI signed in olduğunda.
- **OpenCode Go Teams limits.** "no subscription" der. z.ai gift reset zamanını gösterir. Sign out provider eski numbers'ı drops.
- **Stats: Büyük history yükler.** Transport error durumunda.
- **Notifications: Finished turn kendi session project ismini söyler.** (MorningStar0709'a teşekkürler).
- **Scheduled tasks: Task model yoksa kaydedilemez.** Sadece time değiştirirse date veya weekdays'ı korur (weierliteyangming-hue ve mpeter'a teşekkürler).
- **Workflows: Progress kaydedilemezse durdurulur.** Restart saved point'tan devam eder (mpeter'a teşekkürler).
- **Files: Symlink üzerinden açılan dosyalar refresh.** HTML previews file change üzerine refresh. Arrow keys image right away (JeremyKennedy, yulia-ivashko'a teşekkürler).
- **Files: Failed upload file adı ve reason gösterir.** Markdown preview tables ve headings editor font boyutuna uyar.
- **Editor: Nested repositories change markers.** Proje içinde nested repo'larda gösterir. (Cyneric'a teşekkürler).
- **Projects: Chinese, Japanese veya Korean karakterli path'tan açıldığında sessions listeler.** (IbrahimKhan12'a teşekkürler).
- **Project icon without discover.** New project icon directly shows without pressing discover (yulia-ivashko'a teşekkürler).
- **Provider icon status chip ve message footer.** Picked provider status chip gösterir. (Cyneric'a teşekkürler).
- **Android: Older system WebView ile chat ve composer gösterimi.** (yulia-ivashko'a teşekkürler).
- **Desktop: Remote instance request header first start.** Canary build stable release'ı update olarak sunmaz (JosueGalRe'a teşekkürler).
- **Desktop: macOS before command another app kontrolü.** Signed in başka app kontrolü olmadan reddi (yulia-ivashko'a teşekkürler).
- **Desktop: Cloudflare browser panel geçişi.** Sign-in popups plain Chrome (yulia-ivashko'a teşekkürler).
- **macOS fullscreen sidebar toolbar moves into place.** (daynetran'a teşekkürler).
- **Linux: Open In Terminal project folder.** (Factor-scd ve MorningStar0709'a teşekkürler).
- **Terminal: Input method text cursor konumunda gösterir.** Older Bun kurulursa terminals çalışır (yulia-ivashko'a teşekkürler).
- **CLI: macOS ve Windows startup service update sonra restart.** Docker'da session commands çalışır (DeryFerd ve yulia-ivashko'a teşekkürler).
- **Server: OpenChamber custom XDG_DATA_HOME OpenCode verisi.** (yulia-ivashko'a teşekkürler).
- **Themes: Modified files ve lines teal renk OpenChamber Light'ta.** Yeni olarak görünmez, zaten yeni olarak işaretlenmemiş gibi.

## Düzeltilmeler

- **Context panel: Raw Messages açık uzun live session'de app donmaz.** Agent stream while freezing yapmaz.
- **Git: Git safe.directory engellendiğinde folder Git kendi mesajı gösterir.** retry seçeneği eski davranışa göre.
- **Git: Büyük workspace'da sluggish olmaktan kaçınır.** Hundreds worktrees restart'ta freeze olmaktan kaçınır (android6 ve android6'a teşekkürler).
- **Git: Disk üzerindeki remote git broken panel.** Azure DevOps remote remove name before @ (yulia-ivashko'a teşekkürler).
- **Git: Walkthrough diff.noprefix veya diff.mnemonicPrefix set repolar.** (chen-ye'a teşekkürler).
- **Self-hosted GitLab glab connected network blip.** Settings'ta kaybolmaz (SyuTingSong'a teşekkürler).
- **Git LFS files SSH remote worktrees.** Again worktree creation (GaryBer'a teşekkürler).
- **Worktearown setup commands.** Agent worktree'lar project setup komutlarını çalıştırır (rebelliard'a teşekkürler).
- **New worktree session vanishes home symlink.** Home folder symlink new worktree session (IbrahimKhan12'a teşekkürler).
- **Archived worktree deleted folder.** Archive page lists its sessions.
- **Pasted text @john.doe veya @types/node text kalır.** Missing file mention send'i durdurmaz.
- **Attached context revert staged form answer veya ! command.** (IbrahimKhan12 ve yulia-ivashko'a teşekkürler).
- **New chat agent request.** Running chat break "Agent isn't available in this session's folder" (yulia-ivashko'a teşekkürler).
- **Chat window squeezed fractional display scale.** Between two heights at fractional display scale, selectable while form waits (ChangeHow'a teşekkürler).
- **Form reply session model ve agent.** Always has Send, broken part charts ve tables gizlestirmez.
- **Answered question text positioning.** Before it ve reply after it between Activity collapsed.
- **Collapsed message many comments two lines.** Show more long message place opens (yulia-ivashko'a teşekkürler).
- **Rendered pages fixed height jumping.** Fractional display scale at two heights, selectable while form waits.
- **Unsent comments session boyunca korunur.** (lesderid'a teşekkürler).
- **Move session folder unimoved.** Window current chat folders when comes back. Late move newer'i undo edemez. (yulia-ivashko'a teşekkürler).
- **Auto routing after Plan.** Next one replaced agent'e gönderilir. (yulia-ivashko'a teşekkürler).
- **MCP private relay address.** Browser landed address gösterir (Factor-scd'a teşekkürler).
- **Plugins broken plugin file OpenCode başlatmaz.** Her config file'dan plugins listeler (zerone0x, yulia-ivashko'a teşekkürler).
- **Skills off display.** Switch comments opencode.jsonc korur (zerone0x ve yulia-ivashko'a teşekkürler).
- **Usage Codex numbers.** OpenChamber ChatGPT signed in Codex CLI signed in (yulia-ivashko'a teşekkürler).
- **OpenCode Go Teams limits.** "no subscription" z.ai gift reset z.ai signed out provider numbers drops (yulia-ivashko'a teşekkürler).
- **Stats large history.** Transport error (fuchs-alexander'a teşekkürler).
- **Notifications turn names project.** MorningStar0709'a teşekkürler.
- **Scheduled tasks task model check.** Model yoksa kaydedilemez, sadece time değişir date/weekdays korur (weierliteyangming-hue mpeter'a teşekkürler).
- **Workflows progress saved check.** Kaydedilirse durur, restart last saved point devam (mpeter'a teşekkürler).
- **Files symlink refresh.** HTML previews refresh file change arrow keys image right away (JeremyKennedy yulia-ivashko'a teşekkürler).
- **Files failed upload name reason.** Markdown preview tables headings font size uyar (gaojunran'a teşekkürler).
- **Editor nested repo markers.** nested repo'larda change markers (Cyneric'a teşekkürler).
- **Projects Chinese Japanese Korean sessions.** path'ten sessions listesi (IbrahimKhan12'a teşekkürler).
- **Provider icon status chip message footer.** (Cyneric'a teşekkürler).
- **Android older WebView chat composer.** (yulia-ivashko'a teşekkürler).
- **Desktop remote instance request header first start.** Canary stable show not (JosueGalRe'a teşekkürler).
- **Desktop macOS command another app silent refusal.** Before asks, now explicit (yulia-ivashko'a teşekkürler).
- **Desktop macOS sidebar fullscreen.** (daynetran'a teşekkürler).
- **Linux Open In Terminal project folder.** (Factor-scd MorningStar0709'a teşekkürler).
- **Terminal input method cursor.** Older Bun terminals çalışır (yulia-ivashko'a teşekkürler).
- **CLI macOS Windows startup restart.** Docker commands work (DeryFerd yulia-ivashko'a teşekkürler).
- **Server XDG_DATA_HOME custom.** (yulia-ivashko'a teşekkürler).

## SDK

- **sessions.stop:** Turn durdurur, sessionControl.answers flag açıklar sessions.answerPermission ve sessions.answerForm, chat bridge permission ve forms geçebilirse.
- **provides: ["opencode"]:** Service aynı OpenCode'a erişir, kendi onayı sonrası.
- **provides: ["quota"]:** Usage sayfası, work status ve tray'a provider ekler.
- **contributes.opencodePlugin:** Extension içinde OpenCode plugin ship eder (deatheros'a teşekkürler).
- **Service data folder:** OPENCHAMBER_SERVICE_DATA_DIR. Tracker extensions account learning ready.connection ve host.onConnection.

## Diğer

- **Bunold OpenCode 2.2.6** entegre edildi.
