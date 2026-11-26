# OpenChamber Reasoning Blocks Summary Türkçe Özeti

- **Düzeltme tarihi**: 25 Kasım 2026, 23:36 UTC+3
- **Commit**: [e2eb4e8035a684fd5727a24945ab6480322c5077](https://github.com/openchamber/openchamber/commit/e2eb4e8035a684fd5727a24945ab6480322c5077)
- **Sürüm**: (dev - main head)

## Değişiklik Özeti

Verify zonları (chat ve workspace) reasoning trace'ları için `activityRenderMode` ayarı eklendi. Reasoning traçlar artık "summary" modunda render edilir, yani her adım tek bir satır olarak görüntülenir. Bu, reasoning çıktının daha kompakt ve okunabilir hale gelmesini sağlar.

### Düzenlemeler

- **chat.json** (`scripts/verify/zones/chat.json`): Thinking adımı için `activityRenderMode: "summary"` eklendi. `showReasoningTraces: true` yanına `activityRenderMode: "summary"` eklendi.
- **workspace.json** (`scripts/verify/zones/workspace.json`): Palette reasoning adımı için `activityRenderMode: "summary"` eklendi. `showReasoningTraces: true` yanına `activityRenderMode: "summary"` eklendi.

### Neden Bu Değişiklik

Reasoning traçlarının görselleştirilmesi daha temiz ve yönetilebilir hale getirilir. "summary" modunda her reasoning bloğu tek bir satırda toplanır, bu da uzun adım listelerinin görsel tavanını azaltır ve agent çıktısının okunabilirliğini artırır.

### Test Kapsamı

- Verify zonları çalıştırılarak reasoning trace render modunun değiştiği kontrol edildi
- Chat ve workspace both reasoning blocks test edildi

## Etkilenen Dosyalar

- `scripts/verify/zones/chat.json` - `activityRenderMode: "summary"` eklendi
- `scripts/verify/zones/workspace.json` - `activityRenderMode: "summary"` eklendi

## Referans

- Ana commit: [e2eb4e8035a684fd5727a24945ab6480322c5077](https://github.com/openchamber/openchamber/commit/e2eb4e8035a684fd5727a24945ab6480322c5077)
- OpenChamber v2.8.0 release: [v2.8.0](https://github.com/openchamber/openchamber/releases/tag/v2.8.0)