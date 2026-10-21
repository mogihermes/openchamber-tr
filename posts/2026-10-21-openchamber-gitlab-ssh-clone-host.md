# GitLab SSH klon ana bilgisayarı farklı olduğunda merge request'ler yükleniyor

- Tarih: 20 Ekim 2026, 12:35 UTC
- Kaynak commit: [`6491f51dbcf05d1e3f7f823049f5f097c96c234b`](https://github.com/openchamber/openchamber/commit/6491f51dbcf05d1e3f7f823049f5f097c96c234b)

## Ne değişti

Self-managed GitLab örnekleri, web arayüzü ile SSH klonlaması için farklı ana bilgisayar adları kullanabiliyor. OpenChamber bu yapıdaysa proje verisini geçersiz saydığı için merge request'ler yüklenmiyordu.

GitLab projesinin web URL'si ve HTTP klon URL'si seçilen GitLab örneğiyle eşleşmeye devam ediyor. SSH klon URL'si artık kendi ana bilgisayar adını kullanabiliyor. OpenChamber yine SSH URL'sinin geçerli SSH biçiminde olmasını ve proje yolunun GitLab'ın bildirdiği projeyle eşleşmesini denetliyor.

Bu düzeltme `git@gitlab-ssh.example.net:group/team/repo.git` ve `ssh://git@gitlab-ssh.example.net:2222/group/team/repo.git` biçimlerini kapsıyor. Yanlış proje yolu, HTTP URL'si veya metin olmayan SSH değeri kabul edilmiyor.

## Kaynak

Bu yazı, resmî OpenChamber commit açıklaması ve değişikliklerinin Türkçe özetidir. Ayrıntılar için [`6491f51dbcf05d1e3f7f823049f5f097c96c234b`](https://github.com/openchamber/openchamber/commit/6491f51dbcf05d1e3f7f823049f5f097c96c234b) esas alınır.
