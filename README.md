# OpenChamber Türkçe

[![Sürüm](https://img.shields.io/github/v/release/openchamber/openchamber?label=resm%C3%AE%20s%C3%BCr%C3%BCm)](https://github.com/openchamber/openchamber/releases/latest)
[![Lisans: MIT](https://img.shields.io/badge/lisans-MIT-green.svg)](LICENSE)

OpenChamber, yapay zekâ destekli kodlama çalışmalarını masaüstü, web, VS Code ve mobilde başlatmak, takip etmek ve incelemek için açık kaynaklı bir çalışma alanıdır.

Bu depo, [openchamber/openchamber](https://github.com/openchamber/openchamber) projesinin MIT lisanslı fork'udur. Türkçe arayüz varsayılan olarak açılır. Dil ayarlardan değiştirilebilir.

## Kurulum

Resmî masaüstü sürümlerini [OpenChamber yayınlarından](https://github.com/openchamber/openchamber/releases/latest) indirebilirsiniz.

Web/PWA ve CLI kurulumu için Node.js 24.14+ gerekir:

```bash
curl -fsSL https://raw.githubusercontent.com/openchamber/openchamber/main/scripts/install.sh | bash
openchamber --ui-password guclu-bir-parola-belirleyin
```

Yaygın komutlar:

```bash
openchamber status
openchamber connect-url --qr
openchamber logs
openchamber update
```

OpenChamber varsayılan olarak yalnızca localhost üzerinde dinler. Güvendiğiniz bir ağda değilseniz `--lan` kullanmayın. Tarayıcı erişimi için `--ui-password` belirleyin.

## Türkçe güncellemeler

Resmî sürümlerin Türkçe özetleri [posts](posts) dizininde bulunur. Özetler resmî yayın notuna bağlanır. Kaynak değişmezse yeni yazı veya boş commit oluşturulmaz.
- [2026-10-25: Sürükleme ile satır numarası düzeltmesi](posts/2026-10-25-openchamber-line-drag-fix.md)
- [2026-10-24: pnpm-store yollarını tespit düzeltmesi](posts/2026-10-24-openchamber-pnpm-store-detection.md)



- [2026-10-22: Server testleri geliştirici veri klasöründen izole edilmesi](posts/2026-10-22-openchamber-test-data-directory-isolation.md)
- [2026-10-21: GitLab SSH klon ana bilgisayarı farklı olduğunda merge request'ler yükleniyor](posts/2026-10-21-openchamber-gitlab-ssh-clone-host.md)
- [2026-10-19: OpenChamber v2.5.0](posts/2026-10-19-openchamber-v2-5-0.md)
- [2026-10-19: Sohbet klasörleri aynı sunucudaki cihazlar arasında eşitleniyor](posts/2026-10-19-openchamber-shared-chat-folders.md)
- [2026-10-18: Small Model üretim süresi istem boyutuna göre uzuyor](posts/2026-10-18-openchamber-small-model-prompt-deadline.md)
- [2026-10-17: OpenChamber v2.4.0](posts/2026-10-17-openchamber-v2-4-0.md)
- [2026-10-16: Agent sayfada seçim isteyebiliyor](posts/2026-10-16-openchamber-page-answer.md)
- [2026-10-14: OpenChamber v2.3.3](posts/2026-10-14-openchamber-v2-3-3.md)
- [2026-10-14: Entegrasyon kataloğu eklendi](posts/2026-10-14-openchamber-integrations-catalog.md)
- [2026-10-14: OpenChamber v2.3.2](posts/2026-10-14-openchamber-v2-3-2.md)
- [2026-10-12: Arşivlenmiş sohbetler gönderimden sonra geri açılıyor](posts/2026-10-12-openchamber-archived-sessions-restore.md)
- [2026-10-08: OpenChamber v2.2.0](posts/2026-10-08-openchamber-v2-2-0.md)

## Kaynak ve lisans

- Asıl proje: [openchamber/openchamber](https://github.com/openchamber/openchamber)
- Resmî sürümler: [OpenChamber Releases](https://github.com/openchamber/openchamber/releases)
- Lisans: [MIT](LICENSE)

Bu depo OpenChamber ekibiyle bağlantılı değildir. Ürün davranışı ve güvenlik duyuruları için resmî depo esas alınır.
