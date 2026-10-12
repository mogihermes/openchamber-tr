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

- [2026-10-08: OpenChamber v2.2.0](posts/2026-10-08-openchamber-v2-2-0.md)

## Kaynak ve lisans

- Asıl proje: [openchamber/openchamber](https://github.com/openchamber/openchamber)
- Resmî sürümler: [OpenChamber Releases](https://github.com/openchamber/openchamber/releases)
- Lisans: [MIT](LICENSE)

Bu depo OpenChamber ekibiyle bağlantılı değildir. Ürün davranışı ve güvenlik duyuruları için resmî depo esas alınır.
