# test(web): geliştirici gerçek veri klasöründen testleri ayırma

- Tarih: 21 Ekim 2026, 20:43 UTC
- Kaynak commit: [`8e2db38a63ac56575aa1519acc49f19ba4d8fddb`](https://github.com/openchamber/openchamber/commit/8e2db38a63ac56575aa1519acc49f19ba4d8fddb)

## Ne değişti

Server modülleri `OPENCHAMBER_DATA_DIR` değişkenini yüklediğinde geliştirici veri klasörüne (`~/.config/openchamber`) bakar ve fallback olur. Test dosyası bir klasör seçmeden içeriği içeri aktığında gerçek ayarlar ve yetkilendirme deposu okunuyor ve yazılıyor: yerel bir çalışma gerçek bir `source-control-auth.json` dosyasını kontrol üzeyi yazıyor ve boş kalmış kilit dosyaları diğer test süreçleri başarısız oluyoruyor.

Affected dosyalar:

1. **`packages/web/test/isolated-data-dir.ts`** (yenikaydedildi): Her test dosyasının kendi boş OpenChamber veri klasörünü olur. Server modülleri `OPENCHAMBER_DATA_DIR` değişkenini yüklediğinde `~/.config/openchamber`e fallback yapar, böylece dosya seçeneği yapıldıkça geliştirici veri klasörü etkilenmez.

2. **`packages/web/vitest.config.ts`**: `setupFiles` olarak `./test/isolated-data-dir.ts` eklendi. Test ortamı her başlatıldığında veri klasörü izole edilir. `OPENCODE_DISABLE_CLAUDE_CODE`, `OPENCODE_DISABLE_CLAUDE_CODE_SKILLS` ve `OPENCODE_DISABLE_EXTERNAL_SKILLS` ortam değişkenleri test ortamı içinde temizlenir (enterprise modu ve Jev için zaten yapılıyordu).

3. **`packages/web/server/lib/guests/ssh-install.test.js`**: Child run'lar için `OPENCHAMBER_DATA_DIR` ortam değişkeni siliniyor. SSH install test suite'in kendi izole HOME klasöründen veri klasörü türetilmesini sağlar.

## Nasıl düzeltildi

- `OPENCHAMBER_DATA_DIR` ortam değişkeni testlerden önce ayarlanmadığı veya silindiği durumunda, server modülleri güvenli fallback (`~/.config/openchamber`) kullanır.
- Test setup dosyası her test başlangıcında geçici bir klasör oluşturup `OPENCHAMBER_DATA_DIR`'ı yönlendirir, test bitimi sonradan temizler.
- Vitest config'inde external skills'ların devre dışı bırakılması test sonuçlarının gereksiz etkilenmesini engeller.

## Kaynak

Bu yazı, resmî OpenChamber commit değişikliklerinin Türkçe özetidir. Ayrıntılar için [`8e2db38a63ac56575aa1519acc49f19ba4d8fddb`](https://github.com/openchamber/openchamber/commit/8e2db38a63ac56575aa1519acc49f19ba4d8fddb) esas alınır.

## Yeni sürüm

- OpenChamber v2.5.0: [GitHub Releases](https://github.com/openchamber/openchamber/releases/tag/v2.5.0) (20 Ekim 2026)