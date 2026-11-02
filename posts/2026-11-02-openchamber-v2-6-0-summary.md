# OpenChamber v2.6.0 Türkçe Özeti

- Düzeltme tarihi: 2 Kasım 2026, 01:31 UTC
- Sürüm: [v2.6.0](https://github.com/openchamber/openchamber/releases/tag/v2.6.0)
- Commit: [fix(electron): re-sign the macOS executable ad hoc only on arm64](https://github.com/openchamber/openchamber/commit/6140a6a6a2596efc9556b3612f12d37ed114f3c1)

## Yenilikler

- **Chat: Ajantlar tablolar, grafikler, adımlar ve formlaryla cevaplarıyla birlikte gelir.** Modellerin yazdığına bakılır; form seçeneklerini toplar ve tek cevaba gönderir.
- **Balkon: Bölümleri yeniden düzenle ve kendi sections'unu oluştur.** Chats, Pinned, In work ve Projects'ı yeniden sırala, state, type, linked PR/issue veya projeye göre filtrelemeye ekleme ekle. Özelleştirme menüsünden Customize sections ile açılabilir.
- **Canary build'lar:** Ayarlar > About'ten Stable veya Canary güncellemeleri seçilebilir. Canary, her gece main'den derlenir, değişimi gösterir ve Android ve iOS uygulamalarını içerir (thanks to @yulia-ivashko).
- **Bellek:** Ajantlar [sessions arası öğrenmelerini](https://docs.openchamber.dev/notes-todos-plans/#memory) koruyabilir. Ayarlar > Genel > OpenChamber Tools'ta Agent memory tool'u açmak; girişler Project knowledge sayfasının Memory tab'ında görünür.
- **Workflows:** Ajant [çok adımlı bir iş](https://docs.openchamber.dev/workflows/) planlayıp onaylayabilir ve sonunda rapor alır. Ayarlar > Genel > OpenChamber Tools'da Workflow tool'u açılır.

## İyileştirmeler

- **Mobil: Yazı alanı, chat, çekme generalleri ve dialog'lar iOS klavyesi ile birlikte hareket eder.** Tıklamalar, çekme generalleri ve paneller hemen yanıt verir.
- **Uygama daha az border, renk sadece durumu işaret eder, tek bir gölge seti ve menüler spring'le açılır.** Mesaj alt kısmı model, ajant ve süreyi gösterir, hover'da eylemler vardır.
- **Chat: Uzun sessions daha hızlı açılır, uzun cevaplar ekranda sadece gerekli görüntülerle çizer, iOS'da scroll yukarı kaydırıldığında sarsımaz.**
- **Chat: Konu başına konum preservation gerçekleşir.** Turn bittiğinde, row açıldığında ve collapsed turn çalışırken tutulur.
- **Composer: Model, ajant ve thinking pickers daha sakin olur, model listesi çok modeliyle hızlı açılır.** Telefonun model ve agent sheet'leri aynı davranışı gösterir.
- **Composer: Thinking level model'e göreremember edilir** (thanks to @Hayston1001).
- **Model ve agent sheets'ları model ve agent seçiciler daha sakin olur, model listesi çok modeliyle hızlı açılır.**
- **Dosya: Uzun dosya isimleri bütünlüğünü korur, tree yana kaydırılır, tree klasörleri sidebar hareketiyle açılır/kapatılır.**
- **Paneller: Genişletilmiş panel boyutlandırılabilir, herhangi bir panel için kısayol açar.**
- **Markdown önizlemeleri daha hızlı açılır, sidebar veya panel çekilip bırakırken pointer hareketiyle hareket eder.**
- **Terminal: Cmd+Backspace, Cmd+Left/Right, Option+Left/Right ve scroll kısayolları Ghostty gibi çalışır** (thanks to @gaojunran).
- **Sessions: Başlatılan generate titles, mesajın diliyle kısadır ve dilinizle takip eder** (thanks to @MorningStar0709).
- **Settings > About: Her sürümü tek satırda gösterir, update eylemi ve gün içinde iki Canary build**'r.
- **Images and files: Yükleme ve hata durumu gösterir** (thanks to @mossgowild).
- **Chat: Ajant picker, session'in klasörünün o ajantı çalıştıramadığında uyarır.**
- **Chat: Alt+Enter yeni satır koyar, long-press newline kalın newLine kalır.**
- **Mobile: Yeni chat proje olmadan gösterilir, Open settings Settings'i açar, project ikonları sembol gösterir** (thanks to @yulia-ivashko).
- **Mobile: Cevap alanı klavyeyi açığında görünür, terminal klavyeyi açığında sıkışmaz.**
- **Mobile: Return key comment gönderir, long-press newline kalın newLine kalır.**
- **Mobile: New chat hiçbir project göstermeden, Open settings Settings'i açar, project ikonları sembol gösterir** (thanks to @IbrahimKhan12).
- **Mobile: Terminal clock ileri olduğunda blank kalmaz** (thanks to @yulia-ivashko).
- **Android: Files'ta PDF sayfaları gösterir, keyboarddan image paste app'i kapatılmaz** (thanks to @yulia-ivashko), pasting an image from the keyboard no longer closes the app (thanks to @mannex111).
- **Voice: read-aloud arka planda başlatılmaz, older answer okumaz** (thanks to @dmyoung9), OpenAI-compatible services custom endpoint path kullanabilir (thanks to @MorningStar0709).
- **Notifications: Phone notifications network drop sonra kısa gecikme sonra gelir** (thanks to @yulia-ivashko), interrupted step error olarak uyarmaz (thanks to @gaojunran), session notification no reload (thanks to @ykai55).
- **Desktop: Cmd+W side panel tab'ı kapar, pencere açık kalır** (thanks to @yulia-ivashko), Restart to Update installs download update (thanks to @MLGSW4G).
- **macOS: Uygulama kendi isimlerinde Local Network access ister** (thanks to @yulia-ivashko), full-screen window kapatıldığında black screen kalmaz, maximized window minimize after kalır.
- **Desktop: dock badge sadece sidebar gösterilen sessions sayar** (thanks to @yulia-ivashko).
- **Windows: Network share'lerde uzun paths frozen kalmaz, worktree with long paths archive biter** (thanks to @yulia-ivashko). SSH remote connect çalışır (thanks to @Pterosaur), dictation çalışır (thanks to @IbrahimKhan12).
- **Git: Managed SSH keys with passphrase work** (thanks to @cemarta7), Sync clean tree CRLF veya Git LFS kullanır (thanks to @yulia-ivashko).
- **Git: Gitea and Forgejo SSH host aliases ve newer versions behind** (thanks to @JeremyKennedy), Gitea Actions links open (thanks to @akrhin), GitHub sign-in XDG_CONFIG_HOME honors (thanks to @pwuersch).
- **Terminal: Bağlanamıyorsa hata gösterir ve Try again** (thanks to @yulia-ivashko), interrupted step error olarak uyarmaz (thanks to @gaojunran).
- **MCP: Test connection server'i sadece düzelttiği için kapatmaz, failed server with browser sign-in sign-in again sunar, input form Submit ve Cancel çalışır** (thanks to @yulia-ivashko).
- **Extensions: Her pencere ve cihaza reload olmadan ulaşıp güncelle veya yeniden build** (thanks to @JosueGalRe).
- **Settings > Global plugins OPENCODE_CONFIG ayarlanırsa gösterilir, sadece image model'ler gösterilir** (thanks to @yulia-ivashko).
- **Settings: select fields option'un ismini gösterir, config array'ler commented survive save** (thanks to @IbrahimKhan12).
- **Settings: plugin cards duplicated olmaz, plugins without pinned version sürekli günceller** (thanks to @IbrahimKhan12).
- **Small Model: OpenCode Zen free modeller login olmadan sunmaz** (thanks to @yulia-ivashko).
- **Files: Wrap lines choice reload survival** (thanks to @yulia-ivashko).
- **Search: file-name search hidden ve gitignored toggles honorlar** (thanks to @xhang108).
- **Worktrees: Commands ve file search worktree session folder'undan izlenir, checkout failed recovery** (thanks to @moczix).
- **Scheduled tasks: Multiline command prompts full text tutar, dispatched run sent olarak işaretler** (thanks to @mpeter).
- **Projects: Typed label tutar, editor leaving Saved when you leave** (thanks to @xhang108).
- **Goal Mode: Goal check, agent'lar tarafından başlatılan background commands bekler.**
- **Workflows: Her onay bekleyen run kart gösterir, Workflows panel decline eder.**

## Düzeltmeler

- **Projects: Başlatma home folder, /tmp ve her kullanılan klasörü projeler eklemez, kaldırılanları geri getirmez.**
- **Folder trust: Never trusted folder'lar In work, Pinned, search ve notifications'dan tutulur, session such folder'a trust istenir.**
- **MCP: Server kapatıldığında OpenCode restart'ta kalır.**
- **Windows: Network share'lerde projeler tekrar açılır.**
- **Files: Çoklu kolonlu CSV freezing yapmaz.**
- **Mobile: iOS'tan image save'app kapatmaz.**
- **iPhone: / veya @ yazmaz çökme, klavyeyi paragraph break sonra kaybetmez.**
- **Chat: Agent çalıştıramaz oferta vermez, seçilen agent tutulur tot next message.**
- **Chat: Pinned session kendi session tutar, child session parent'ın tuttuğu tool results gösterir.**
- **Chat: Interrupted chat restart sonrası tekrar başlar** (thanks to @noget1200).
- **Chat: /compact session seçili model ve effort kullanır.**
- **Chat: Alt+Enter yeni satır koyar.**
- **Chat: Tek tilde artık metni çiteleri (strike) yapmaz, inline code kelime içinde bozulmaz.**
- **Chat: Skill list loading gösterir, skill okunurken @ list ziplenmez.**
- **Chat: Dosya modeline tam path verir.**
- **Pinned messages kendi session'ında tutar, child session'in kendi subsession'ları gösterir** (thanks to @mradwankhalil).
- **Chat: Question cevap verilebilir, cevap sona erdiğinde kalır. Uzun cevap silindiğinde crash olur** (thanks to @alohaninja).
- **Chat: Yanıt bekleyen sayfa long reply after scroll yapar, mesaj sayfaya appeared önceden beklemez** (thanks to @yulia-ivashko).
- **/:btw: Main chat'ın latest answer'ı gönerir, favorite-model shortcutlar model'i switch eder, notifications parent chat'i açar** (thanks to @yulia-ivashko, @IbrahimKhan12, @Naputt1).
- **Chat: Response style turns across** (thanks to @theacrat).
- **Composer: 20 MB üzeri dosya attached reddedilir, desktop'tan large file attached removed** (thanks to @yulia-ivashko).
- **Composer: Forked mention file twice göndermez, issue ve PR chips selected session'le tutar, comments ve quotes composition you are using** (thanks to @xhang108, @Chapax, @gaojunran).
- **Sessions: Only comment or annotation started title oluşturur.**
- **Sessions: Todo veya plan new session'a default model ve agent başlar.**
- **Agent message archived chat sidebar'a döndürür** (thanks to @yulia-ivashko).
- **Sidebar: Reading row değişmez, sessions veya projects değişirse yukarıda, Detailed rows switching.**
- **Sidebar: Sub-parent altında kalır, non-Git project rows tek satır, one-project picker restart survival** (thanks to @Hayston1001), Archive session subsessions üzerinde hareket (thanks to @woolsen).
- **Mobile: Keyboard açığında answer field görünür, terminal klavyeye sıkışmaz** (thanks to @yulia-ivashko).
- **Mobile: / veya @ yazmaz crash, klavyeyi paragraph break sonrası metin kaybetmez** (thanks to @yulia-ivashko).
- **Mobile: New chat hiçbir project göstermeden, Open settings Settings'i açar, project icons sembol gösterir** (thanks to @IbrahimKhan12).
- **Mobile: Terminal clock ileri olduğunda blank kalmaz** (thanks to @yulia-ivashko).
- **Android: PDF pages gösterir, keyboarddan image paste app kapatmaz** (thanks to @yulia-ivashko), pasting an image from the keyboard no longer closes the app (thanks to @mannex111).
- **Voice: read-aloud arka planda başlatılmaz, older answer okumaz** (thanks to @dmyoung9), OpenAI-compatible custom endpoint path (thanks to @MorningStar0709).
- **Notifications: Brief network drop sonra phone notifications gelir, interrupted step error uyarmaz** (thanks to @gaojunran), opening session notification no reload (thanks to @ykai55).
- **Desktop: Cmd+W side panel tab kapar, pencere açık kalır** (thanks to @yulia-ivashko), Restart to Update install update (thanks to @MLGSW4G).
- **macOS: Local Network access ister kendi isimlerinde, full-screen window black screen kalmaz, maximized window minimize after kalır** (thanks to @yulia-ivashko).
- **Desktop: Dock badge sadece sidebar gösterilen sessions sayar** (thanks to @yulia-ivashko).
- **Windows: Network share freeze kalmaz, long paths archive biter** (thanks to @yulia-ivashko). SSH remote connect çalışır (thanks to @Pterosaur), dictation çalışır (thanks to @IbrahimKhan12).
- **Git: Managed SSH keys with passphrase work** (thanks to @cemarta7), Sync clean tree CRLF veya Git LFS (thanks to @yulia-ivashko).
- **Git: Gitea and Forgejo SSH host aliases newer Forgejo versions behind** (thanks to @JeremyKennedy), Gitea Actions links open (thanks to @akrhin), GitHub sign-in XDG_CONFIG_HOME honors (thanks to @pwuersch).
- **Terminal: Error ve Try again gösterir, interrupted step error uyarmaz** (thanks to @yulia-ivashko).
- **MCP: Test connection repaired server kapatmaz, failed server with browser sign-in sign-in again sunar, input form Submit ve Cancel çalışır** (thanks to @yulia-ivashko).
- **Extensions: Reload olmadan her cihaza ulaşıp install, update veya rebuild** (thanks to @JosueGalRe).
- **Settings: OPENCODE_CONFIG ayarlanırsa global plugins gösterir, sadece image model'ler gösterir** (thanks to @yulia-ivashko).
- **Settings: select fields option ismini gösterir, config array'ler commented survive save** (thanks to @IbrahimKhan12).
- **Settings: plugin cards duplicated olmaz, plugins without pinned version sürekli günceller** (thanks to @IbrahimKhan12).
- **Small Model: OpenCode Zen free modeller login olmadan sunmaz** (thanks to @yulia-ivashko).
- **Files: Wrap lines choice reload survival** (thanks to @yulia-ivashko).
- **Search: file-name search hidden ve gitignored toggles honorlar** (thanks to @xhang108).
- **Worktrees: Commands ve file search worktree session folder'undan izlenir, checkout failed recovery** (thanks to @moczix).
- **Scheduled tasks: Multiline command prompts full text, dispatched run sent olarak** (thanks to @mpeter).
- **Projects: Typed label tutar, editor leaving Saved** (thanks to @xhang108).
- **Goal Mode: Agent'lar tarafından başlatılan background commands bekler.**
- **Workflows: Onay bekleyen run kart gösterir, Workflows panel decline eder.**

## SDK

- **Services: Her project'den session events'e subscribe contributes.sessionEvents, phone yanınextra notifications channel** (thanks to @deatheros).
- **Trackers: Work items YouTrack, Jira veya Plane next to Linear with provides: ["tracker"] ve contributes.tracker** (thanks to @deatheros).
- **Shared surfaces: Key events carry keyCode computed by viewer's browser** (thanks to @JosueGalRe).
- **UI kit: Panels match app shadows ve badges, progress 100% only when done** (thanks to @JosueGalRe).

## Kaynakça

- Bu yazı, [resmî commit](https://github.com/openchamber/openchamber/commit/6140a6a6a2596efc9556b3612f12d37ed114f3c1) üzerine kuruludur. Teknik detaylar ve tam workflow değişiklikleri için esas alınır.
- [Resmî GitHub release v2.6.0](https://github.com/openchamber/openchamber/releases/tag/v2.6.0)
- [OpenCode 2.2.5 güncellemesi](https://github.com/openchamber/openchamber/releases/tag/v2.6.0) (Bundled OpenCode updated to 2.2.5)
- Electron updated to 44.10
