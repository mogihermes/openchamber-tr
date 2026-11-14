# OpenChamber Özet: Built-in Timer for Waits

- **Düzeltme tarihi**: 14 Kasım 2026, 08:03 UTC
- **Sürüm**: v2.7.1 (resmi sürüm)
- **Commit**: [Built-in timer for waits](https://github.com/openchamber/openchamber/commit/c075210f9a67d45701281c3cdd150e9db9f480af)

## Değişikler

- **Built-in timer source for waits**: Bir built-in timer source eklendi, böylece bir ajan kendi oturumunu 1 ile 1440 dakika sonra uyandırmak için kendi timer'ını tetikleyebilir. Ajan, bir uzantının takip ettiği bir şey üzerinde beklerken, timer'ın dolmasını sağlayarak kendi devam etmesine olanak tanıyan kendi timer'ını başlatabilir.

## Kullanıcı etkileri

- Ajanlar artık kendi timer'larını kullanarak belirli süreler (1-1440 dakika) bekleyebilir
- Oturum, timer'ın dolduğunda ya da uzantının bildirdiği olduğunda uyandırılır
- Kullanıcı müdahalesiz olarak süreyi kontrol edebilir, genişletilmiş bekleme seçenekleri elde eder

## İlgili dosyalar

- `packages/ui/src/components/chat/ChatInput.tsx` - Bütun değişiklik: "The agent waits on a timer or on something an extension follows" güncellendi
- `packages/ui/src/components/chat/ExtensionWaitStrip.tsx` - "Timer (10 s)" başlığı güncellendi: "Timer (10 s): the wait's title with the label its extension, or the host for a timer, gave it."

## Özet

Bu güncelleme, ajanların kendi built-in timer'larını kullanarak 1 ile 1440 dakika arasında beklemelerini sağlar. Ajan, timer'ın dolmasını sağlayarak kendi oturumunu uyandırdığı için, dışarıdan tetikleme gerektirmez. Özellik, wait mekanizmasındaki esneklik artırarak zaman kontrolünü ajanın kendi eline verir.