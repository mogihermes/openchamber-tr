# OpenChamber v2.5.2 - Güncelleme Özeti

- **Tarih:** 26 Ekim 2026, 00:48 UTC
- **Kaynak commit:** [`c4919abc1e7a0a3beeaa126666487806bf79cfe0`](https://github.com/openchamber/openchamber/commit/c4919abc1e7a0a3beeaa126666487806bf79cfe0)
- **GitHub Release:** [v2.5.2](https://github.com/openchamber/openchamber/releases/tag/v2.5.2) (26 Ekim 2026)

## Yenilikler (New)

- **Sidebar:** Sidebar, çalışma ağacını (worktree) ve tüm oturumları, veya ana checkout'taki bir oturumun fork'ları, revizyonları ve alt agent'ları tek satırda gösteren satırlarla listeler. Bir iş, bir worktree ile tüm oturumların ya da ana checkout'taki oturumun fork'ları, revizyonları ve alt agent'lerdir, görev adı, PR veya konu ve canlı durum olarak gösterilir. İşin bitmesi (Done) çalışma tab'larını kapatır.
- **Worktree archive:** Worktree'ın klasörünü silerek disk yerinden kazanır. Branch, oturumlar ve hatta.commit'lenmemiş değişiklikler korunur. Archive sayfasındaki Restore ile tümünü geri yükler; merged PR sonrası aynı şekilde temizlik yapar.
- **Folder trust:** Folder'ın plugin'leri, MCP sunucuları veya diğer komutları çalıştırmadan önce, hangi komutlar çalışacak gösterilir ve onay istenir. Yapılandirma değiştiğinde tekrar istenir; zaten listenin projelere onaylanmışlar ister tekrar istenir.
- **GitHub Discussions:** Discussions, konuların yanında konular ve pull request'ler üzerinde board'da gösterilir. Ekle menüsündeki New worktree'una da eklenir. Okumak, yanıtlamak, cevap işaretlemek, kapatmak veya tekrar açmak ve birini mesajına eklemek mümkündür.
- **Composer:** `@` ile başka bir oturumu ya da mesajınızın birini etiketleyebilir ya da linki yapıştırabilir. Ajan buyi bağlam olarak alır; mention chip olarak gösterilir ve oturumunu açar.
- **Comments:** Tıbbi dosyanın başlığından dosya genelinde yorum yapabilirsiniz. Değişiklikler ve seyahat izlemesinde görüntülenir.
- **Walkthrough:** Her durak, şu an kodun ne yapıyor ve hangi trade-off'leri kabul ettiklerini açıklar. Tüm dosyalar atladıysa tek satırlık notlar çıkar. Magic Prompts'ın kendi talimatları için Walkthrough sayfası vardır.
- **Mobile:** Çalışma çantası (workspace drawer) Work durumu sekmesini içerir; alt agent'lar, branch ve PR kontrolleri, sabit mesajlar ve bağlantılı konular gösterir.
- **Chat:** Yanıtta `diff` kod bloğu, diff önizlemesinde propoziyonal bir değişiklik olarak gösterilir (@cemarta7 sayesinde).
- **Chat:** Read File satırının ikonu, agent tarafından okunan görseli genişletilmiş panelde açar (@yulia-ivashko sayesinde).
- **Chat:** Mesaj kutundaki `:` emoji otomolay completer.
- **Sessions:** Agent tarafından başlatılan bir oturum, ilk mesajın altında "From session" ile göndericinin başlığını gösterir; başlık o oturumu açar.
- **Diagnostics:** Tanı zaman çizelgesi (Cmd/Ctrl+Shift+L), OpenCode 2.1.4'ü gerektiren bir bellek anı snapshot'ını hata bildirimine eklemek için kaydedebilir.

## Geliştirmeler (Improvements)

- **Yeni logo ve uygulama ikonları:** Her platformda (@yulia-ivashko sayesinde).
- **Prompt navigator:** Chat'ın üst köşesindeki küçük gösterici; hover, kısayol veya tıklayarak tüm prompt'ların listesine erişim.
- **Unsent draft'lar:** Sunucuya kaydedilir ve her cihazda sidebar'da gösterilir.
- **Side panel:** Tüm sekme'lar ortak genişliği paylaşır; projeler ve worktree'lar arası aynı kalır. Genişletilmiş panel, chat'ı ekrana bırakmadan sol tarafa kaydırır (yine @yulia-ivashko sayesinde).
- **Issues ve PR'ler:** GitHub metinlerini GitHub'un yaptığı gibi gösterir; uyarılar, emoji, revizyon önerileri olarak diff'ler ve #123, @user ve commit id'leri üzerindeki linkler.
- **Composer:** Yazıyı yazarken yanına otomatik liste açar.
- **Sessions:** Yeni oturum, ilk mesajından kısa bir konu başlığı alır.
- **Worktrees:** Issue'dan oluşturulan bir worktree, görev adıyla branch'i yeniden adlandırır (örneğin `issue-180-documentation-catalog`).
- **Browser:** Geliştirme sunucusu listesi, proje sunucularını first olarak gösterer, geri kalanı "Show hidden ports" önüne shelter eder (yine @yulia-ivashko).
- **Work Status:** Checks satırı `7/9` renkli nokta ile okunur (yine @yulia-ivashko sayesinde).
- **Arayüz boyutu:** Toots ve header, Work Status, Settings, komut paleti ve editor arayüz boyutuna ve yazı büyüğüne göre uyarlanır (yine @mossgowild, @yulia-ivashko).
- **Toasts:** Kapatı kesi sayaç; toast'un kaybolacağı süreyi gösterir, telefonlarda toasts bir satır bannertir.
- **Failed `!` command:** Çöküntü satırı üzerinde, komutun neden başarısız olduğunu gösterir (@kemaladlig, @yulia-ivashko).
- **Composer with queued messages:** Mesaj kuyruğundaysa, boş mesaj kutusundaki ArrowUp en yenisini çıkarıp düzenlemek için kullanılır.
- **Composer focus mode:** Footer'dan focus mode butonu kaldırıldı; Cmd/Ctrl+Shift+E hâlâ focus modunu açar.
- **Failed `!` command återkomst:** Session'a dönünce agent picker, picker'da gösterilen agent ile Plan ya da başka agent olarak gönderilirdi; düzeltildi.
- **Skills catalog:** Virüs tarayıcısı temp klasörü temizlenmezse (Windows) catalog serbest kalmaz; thousands of skills Freeze'i giderildi (@yulia-ivashko).
- **Git status refresh:** Windows antivirusu yavaşlattığı için git status için yarım kadar git process başlatılır; giderildi.
- **gh sign-in:** Her GitHub read için `gh auth token` process'i başlatmaktan kaçınılır; giderildi.
- **Checked-out tag:** Tag checked-out, branch veya push count göstermez; giderildi.
- **Forgeja/Gitea server with sign-in:** Token ile eklenebilir (@yulia-ivashko).
- **Session turn timer:** Başka cihazdan oturumun açıldığında başlangıç timer'ını korur (@Naputt1, @yulia-ivashko).
- **Subagent worktree move:** Başka worktree'a taşınan subagent, panel güncellemelerini sürdürür ve done tikini alır (@yulia-ivashko).
- **Reload and turn stats:** Reload sonrası turn stats response speed'i çıkarır; yanlış düşük sayıyı giderir (@yulia-ivashko).
- **Chat comment field:** Quote'ün yanında pencere kenarına yakın olarak kalır; ekranda kalır.
- **Text selection menu:** Chat'ten ayrıldığında kapanır.
- **PR/commit comment:** Pull request veya commit yorumunda, hangi diff'lerin satırlarından geldiğini agente bildirir; draft o diff'de sadece o diff için gösterilir.
- **Walkthrough regeneration:** Başka model veya dille yeniden generate eder; ikinci model öncekini kopyalamazdı; giderildi.
- **Plans:** "Run as goal" seçeneği artık agent'in planı implement etmesini sunmaz; giderildi.
- **Files Markdown preview:** Tek find butonu; çalışır (@yulia-ivashko).
- **Files drag across line numbers:** İşaretçi kod alanına kaydığında seçimin uzatılması engellenmez, pencere kenarında scroll olur; basmadan bırakılan tıklama iptal edilerek sürüklemenin tamamlanması sağlanır (@yulia-ivashko). Bu, #5556 düzeltmesinin devamıdır.
- **Files PDF previews:** Sayfa, ses ve video; sign-in refresh'ten sayfayı korur (@yulia-ivashko).
- **Desktop:** Dışarıdan açılan session linki, macOS'ta pencere ön plana getirilir (@JosueGalRe).
- **Mobile:** Chat'tan dosya linkine tıklandığında dosya açılır (@yulia-ivashko).
- **Mobile:** iPhone app, katlanabilir (Duo) cihazın inner ekranı dolguyu doldurur (@yulia-ivashko).
- **Mobile:** iPad'ta sidebar, klavyenin açılışında yerinde kalır (@yulia-ivashko).
- **Mobile:** Sidebar'da açılan veya kapanan satırlar, kaydırma eylemi metin üzerinden gösterilmemek üzere düzeltildi; suaveslide açılır (@yulia-ivashko).
- **CLI:** pnpm ile yapılan kurulumları tanıır; giderildi.

## Düzeltmeler (Fixes)

- **Composer:** Mesaj agent picker'da gösterilen agent ile aynı olmalı; session'a dönülürse Plan ya da başka agent olarak gönderilmezdi; giderildi.
- **Files > 10 MB:** 10 MB üzeri dosya açıldığında uyarı gösterilir; masaüstü üzerinde donma (freeze) düzeltildi; diğer platformlarda yolla erişim çalışır.
- **Skills:** Skills kataloğu, thousands of skills source freezes sayfasını engeller; giderildi (@yulia-ivashko).
- **Skills (Windows):** Temp folderda tutulan virus tarayıcısı temizlenmediği sorunu giderildi (@yulia-ivashko).
- **Git status refresh:** About half as many git processes started; Windows antivirüsü yavaşlatmasından kaçınıldı (@yulia-ivashko).
- **GitHub with gh sign-in:** Her read için auth token process'inden kaçınıldı (@yulia-ivashko).
- **Checked-out tag:** Branch veya push count göstermez; giderildi.
- **Forgejo/Gitea server with sign-in:** Token eklenmesi desteklenir (@yulia-ivashko).
- **Session turn timer:** Başka cihazdan oturum açıldığında timer koruması (@Naputt1, @yulia-ivashko).
- **Subagent worktree move:** Panel ve done tick güncellemesi sürdürülür (@yulia-ivashko).
- **Reload and turn stats:** Response speed çıkarılmadan; yanlış düşük sayı giderilir (@yulia-ivashko).
- **Chat comment field:** Window edge'e sabit kalır (@yulia-ivashko).
- **Text selection menu:** Chat'ten ayrıldığında kapanır.
- **PR/commit comment:** Hangı diff'ler agent'e ait olduğunu bildirir; draft sadece o diff'de gösterilir.
- **Walkthrough regeneration:** İkinci model öncekini kopyalamaz; giderildi.
- **Plans:** "Run as goal" disabled for plan implementation; giderildi.
- **Files Markdown preview:** Single find button; works; giderildi.
- **Files drag across line numbers:** Selection extends into code pointer drifts, edge scrolls; release click ignored; #5556 fix continues (@yulia-ivashko).
- **Files PDF previews:** Page, audio, video preserved across sign-in refresh (@yulia-ivashko).
- **Desktop:** Session link from outside brings window to front on macOS (@JosueGalRe).
- **Mobile:** File link tap opens file (@yulia-ivashko).
- **Mobile:** iPhone Duo inner screen fills on unfolded; @yulia-ivashko.
- **Mobile:** iPad sidebar stays put when keyboard opens; @yulia-ivashko.
- **CLI:** pnpm install recognition; giderildi.

## SDK

- **Work Status:** `contributes.statusSection.source` ile uzantı, kendi servisinden veri olarak section tanımlayabilir; app rows, charts ve controls kendi frame olmadan çizer. Şema: `guestStatusViewSchema` SDK'da.
- **Sessions:** `onSessions` carrier session records carry `links`, her issue ve pull request linked with title, url ve kind.

## Yeni sürüm

- OpenChamber v2.5.2: [GitHub Releases](https://github.com/openchamber/openchamber/releases/tag/v2.5.2) (26 Ekim 2026)
- Önceki sürüm: OpenChamber v2.5.1: [GitHub Releases](https://github.com/openchamber/openchamber/releases/tag/v2.5.1) (23 Ekim 2026)