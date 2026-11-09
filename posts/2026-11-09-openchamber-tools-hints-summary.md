# OpenChamber Ayar Araç İpuçları Özeti

- Düzeltme tarihi: 9 Kasım 2026, 01:10 UTC
- Sürüm: [v2.7.1](https://github.com/openchamber/openchamber/releases/tag/v2.7.1) (dev branch)
- Commit: [feat(settings): fold OpenChamber Tools hints into their summaries](https://github.com/openchamber/openchamber/commit/183d935e9cb602ef6ce7f64cbf5f615e4d6b8048)

## Değişiklikler

Ayar araçları (tools) için yapılan değişiklik, her araç satırının yanında gösterilen ayrı "bilgi" (info) ipuçlarını ve üzerine gelince çıkıp görünen ipucu bileşenlerini kaldırıp, tüm bilgiyi özet (summary) metni içinde birleştirir.

### Yapılan değişiklikler:

1. **Araç satırı tasarımı değişti:** Her araç satırı artık `info` ipucunu göstermek için ayrı bir `SettingsInfoHint` bileşeni kullanmaz. Özet metni (`summary`) artık kullanıcıya gösterilecek tek bilgi kaynağıdır.

2. **Özet metni genişletildi:** Her araç için özet metni, önceki `info` ipucundaki detayları içerecek şekilde güncellendi. Kullanıcılar artık araçı etkinleştirirken ayrı bir ipucu görmemiş olur, tüm önemli bilgiler özet içinde yer alır.

3. **Ayarlar yapısı değişti:**
   - `ToolRow` bileşeni: `info` prop'ı kaldırıldı, özet artık satırın altında tek başına gösterilir
   - `ToolOption` bileşeni: `info` prop'ı opsiyonel (?) yapıldı, hala varsa gösterilir ama eksikse null gösterilir
   - Ayarlar dosyalarında (`OpenChamberToolsSettings.tsx`), her araçtan `info={t(...)}` ifadeleri kaldırıldı

4. **Dil dosyaları güncellendi:** `info` anahtarları i18n (uluslararasılaştırma) dosyalarından kaldırıldı ve içeriği `summary` anahtarlarına entegre edilmiştir. Araç özetlerindeki değişiklikler şunları içerir:
   - Control aracı: "Sessions ve worktrees oluşturup yönettiğinizi, hiç silinmez" öne çıkmıştı
   - Schedule aracı: "Günlük/haftalık/tek sefer cron tablosu" ipucu özet içinde yerleştirildi
   - Web aracı: "Uygulama çalışırken sayfaları görüntüleme ve ekran görüntüsü" ipucu özet içinde entegre edildi
   - Memory aracı: "Sadece başlıkları görebilir, ilgili girdi açılır, kapatıldığında memory penceresi gizlenir" ipucu özet içinde
   - Notify aracı: "İş bitince veya takıldığında sizi uyar" ipucu özet içinde
   - Knowledge aracı: "Proje elemanlarını okuyup görevleri ve planları güncelleme" ipucu özet içinde
   - Image aracı: "Her görsel modeli sağlayıcısından ücretlendirilme" ipucu özet içinde

5. **Tarayıcı/Render aracı:** Samandan önceki "sandbox ortamı, dosya erişimi yok, bağlantılar tarayıcıda açılır" ipucu özet içinde entegre edilmiştir. Kullanıcılar artık araç etkinleştirirken ayrı bilgi almamış olur.

### Kullanıcı etkileri:

- **Önceki davranış:** Her araç satırı yanında küçük bir "i" (info) ikonu vardı; üzerine gelince açıklayan ipucu çıkıyordu
- **Yeni davranış:** Tüm bilgiler araç başlığının altındaki özet metni içinde bulunur. İpucu ikonları ve üzerine gelince çıkan bileşenler kaldırıldı
- **Ayarlar sayfası:** Daha temiz görünüm, ipucu bileşenleri ayrıçalma (clutter) olmadan özet metniyle birleştirildi

### İlgili dosyalar:

- `packages/ui/src/components/sections/openchamber/OpenChamberToolsSettings.tsx` - Arayüz değişiklikleri
- `packages/ui/src/lib/i18n/messages/*.settings.ts` - i18n mesajları (info anahtarları kaldırıldı, summary güncellendi)
- `packages/ui/src/lib/i18n/messages/image-tool.i18n.ts` - Görsel aracı i18n değişiklikleri

## Özet

Bu güncelleme, Ayarlar > OpenChamber Tools sayfasında araç ipuçlarını daha temiz ve entegre bir yapıya taşır. Kullanıcılar artık araçları etkinleştirirken ayrı ipucu görmemiş olur, tüm kritik bilgiler özet text içinde mevcuttur. Bu, arayüzun karmaşasını azaltır ve araç özetlerini tek bir kaynak olarak görürsunuz.