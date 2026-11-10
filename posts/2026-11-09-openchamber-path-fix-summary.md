# OpenChamber PATH Düzeltmesi Özeti

- Düzeltme tarihi: 9 Kasım 2026, 22:12 UTC
- Sürüm: v2.7.0 (resmi sürüm)
- Commit: [fix: resolve OpenCode from the current login shell PATH](https://github.com/openchamber/openchamber/commit/9cd77a61dcdc0bea6276cdf3cea950c8f9c1be77)

## Değişiklikler

OpenCode komut satırı çalıştırıldığında, sistem PATH ortam değişkeninde opencode bulunamazsa hata veriyordu. Bu düzeltme, startup hizmetlerinin eskisi kaybolan PATH değerlerini sürdürmemesini ve kullanıcının login shell'inki PATH'i kullanımına izin vermesini sağlar.

### Yapılan değişiklikler:

1. **cli.js - PATH araştırması düzeltimi**: `searchPathFor('opencode')` çağrısı önce login shell ortamını snapshot alarak PATH'i yeniden deneme seçeneği eklendi. Eğer default PATH'de opencode bulunamazsa, sunucu kullanıcının login shell PATH'ini uygular.

2. **cli-startup.js - PATH sürdürülmesi engellendi**: `shouldPersistStartupEnv` fonksiyonuna eklendiği gibi, PATH anahtarının hizmet ortamında kalması engelleniyor. Böylece araçlar yok edilen klasörlerden sonra PATH'de sürdürülmez.

3. **Dokümantasyon güncellemesi**: STARTUP.md'de PATH yönetimi hakkında kullanıcılara yönelik bilgi eklendi: "Servis başlatıldığında platform varsayılan PATH kullanılır; sunucu başlatıldığında login shell PATH'i eklenir. Kendi PATH'nizi sabit olarak ayarlamak için Çeviriler > Ortam ayarları'nde PATH değişkenini ekleyin."

4. **Test eklentisi**: cli-startup.test.js'e yeni test eklendi: "macOS başlatma hizmetinin login shell PATH'ini hizmet ortamına dahil etmemesi" testi.

### Kullanıcı etkileri:

- **Önceki davranış**: Opencode PATH ortam değişkenindeyseniz bile, startup hizmeti eskisi kaybolan PATH değerini sürdürür ve opencode bulunamıyor gibi hata verirdi.

- **Yeni davranış**: Hizmet başlatıldığında platform varsayılan PATH kullanılır ve sunucu başlatıldığında login shell PATH'i öncelikle eklenir. Böylece yeni kurduğunuz veya kaldırdığınız araçlar terminal ve agent komutlarında görünür.

- **Kendi PATH'nizi sabitlemek**: Eğer belirli bir PATH girişini hizmetinizde sabit tutmak istiyorsanız, Çeviriler > Ortam ayarları'ndan PATH değişkenini manuel olarak ekleyebilirsiniz.

### İlgili dosyalar:

- `packages/web/bin/cli.js` - PATH araştırması ve login shell ortamı entegrasyonu
- `packages/web/bin/lib/cli-startup.js` - PATH sürdürülmesi engelleme
- `packages/web/bin/lib/cli-startup.test.js` - PATH testleri
- `packages/web/bin/lib/DOCUMENTATION.md` - Başlatma dokümantasyonu güncellemesi

## Özet

Bu düzeltme, OpenCode'un startup hizmetlerinde login shell PATH'i doğru şekilde algılayıp uygulamamasının sorununu giderir. Kullanıcılar artık opencode'u standart dışı konumlara kurarak da terminal ve agent komutlarında sorunsuz kullanabilir. Ayarlar sayfasından PATH değişkenini manuel olarak ekleyerek hizmet ortamında da belirli yolları sabitleyebilirsiniz.