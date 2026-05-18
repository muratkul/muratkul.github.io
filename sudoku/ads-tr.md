---
layout: default
title: Reklamlar
---

> **Diller:** [English](./ads) · **Türkçe** · [Español](./ads-es)

# Sudoku Arena Online'da Reklamlar

Sudoku Arena Online ücretsiz oynanır. Bulmaca üreteci, çok oyunculu
eşleşme ve günlük bulmaca arkasındaki iş, reklamlarla desteklenir. Bu
sayfa, hangi reklamları gösterdiğimizi, nerede gösterdiğimizi ve
bunları nasıl yapılandırdığımızı sade bir dille anlatır — oynamadan
önce neyi konfor edebileceğinize karar verebilesiniz diye.

Veri toplama tablosunun tamamı için
[Gizlilik Politikası](./privacy-policy-tr)'na bakın. Sözleşmesel taraf
için [Kullanım Koşulları](./terms-of-service-tr)'na.

---

## Reklamları kim sunuyor

Google LLC tarafından işletilen **Google AdMob**'u kullanıyoruz.
Sudoku Arena Online içinde gördüğünüz her reklam AdMob ağı üzerinden
sunulur. Başka herhangi bir reklam SDK'sı eklemiyoruz — Meta Audience
Network, Unity Ads, IronSource, uygulama içi webview reklamları gibi
hiçbir şey yok.

AdMob'un politikaları ve Google'ın bizim adımıza topladığı bilgileri
nasıl kullandığı:

- [Google'ın hizmetlerimizi kullanan site veya uygulamalardan elde ettiği bilgileri nasıl kullandığı](https://policies.google.com/technologies/partner-sites)
- [Google AdMob ve AdSense gizlilik uygulamaları](https://support.google.com/admob/answer/6128543)

---

## Reklamlar nerede çıkıyor

Uygulamada dört olası reklam yuvası var. Her birinin aktif olup
olmadığı, yeni bir build yayınlamadan ayarlayabildiğimiz bir çalışma
zamanı yapılandırma değeri (Firebase Remote Config) ile yönetilir.
Lansmanda mümkün olan en muhafazakar ayarla geliyoruz — sadece ödüllü
yuva açık.

| Yuva | Ne zaman | Lansman varsayılanı |
|---|---|---|
| **Ödüllü — "Reklam izle, ipucu kazan"** | Ücretsiz ipucunuzu kullandıktan sonra ipucu butonunda isteğe bağlı play ikonu çıkar. Tıklarsanız kısa bir ödüllü video yüklenir; tamamlayınca bir ekstra ipucu kazanırsınız. Reddetmek veya reklamı kapatmak hiçbir şey yapmaz. | **Açık** (sadece kullanıcı tetikli) |
| **Banner — Ana ekran ve maç-sonuç ekranları** | Ana ekran ve maç-bitiş modalının altında küçük bir banner. Tahta veya tıklanabilir oyun arayüzünün üzerini asla kaplamaz. | **Kapalı** (lansmanda) |
| **Banner — Oyun içi** | Oynarken sayı pad'inin altında küçük bir banner. Aynı eli-uzaktan tutma yerleşimi — tahta üzerinde asla. | **Kapalı** (lansmanda) |
| **Interstitial — Maç başında** | Çok oyunculu maç başlamadan önce tam ekran reklam, net Kapat butonuyla. Maç başına en fazla bir kez. | **Kapalı** (lansmanda) |

Reklamsız bir Pro yükseltmesi ileride planlanıyor; ayrıntılar
yayınlandığında netleşecek.

---

## AdMob hangi bilgiyi alır

AdMob'u yalnızca **kişiselleştirilmemiş reklam** (`npa=1`) talep
edecek şekilde yapılandırdık. Pratikte bu şu demektir:

- AdMob, cihazınızdaki herhangi bir tanımlayıcıyı sizinle ilgili bir
  profil oluşturmak veya güncellemek için **kullanmaması** için
  bilgilendirilir.
- Gördüğünüz reklamlar bağlamsal sinyallere göre seçilir — uygulama
  türü (bulmaca oyunu), IP adresinizden türetilen ülke ve cihaz dili.
  Geçmiş davranışınıza göre değil.
- Apple App Tracking Transparency ekranı **göstermiyoruz** çünkü
  uygulama cihazlar arası izleme yapmıyor. ATT ekranı izleme yapan
  uygulamalar içindir.

AdMob, platformunuzun reklam tanımlayıcısını (iOS'ta **Apple IDFA**,
Android'de **Google AAID**) **dolandırıcılık tespiti** ve Apple'ın
[SKAdNetwork](https://developer.apple.com/documentation/storekit/skadnetwork)
atıf çerçevesi için kullanmaya devam eder. Bu kullanım politikaya
bağlıdır — Google bu tanımlayıcıları başka yerlerde size reklam
göstermek için kullanma hakkına sahip değildir.

Yapabilecekleriniz:

- **iOS**: Ayarlar → Gizlilik ve Güvenlik → Apple Reklamcılık →
  *Kişiselleştirilmiş Reklamlar*'ı kapatın veya aynı ekrandan
  IDFA'nızı sıfırlayın.
- **Android**: Ayarlar → Google → Reklamlar → *Reklam
  Kişiselleştirmesini Kapat*'ı açın ve Reklam Kimliğinizi sıfırlayın.

Reklam izleme sınırlı olduğunda AdMob uygulamada yine
kişiselleştirilmemiş reklam servis eder — hiçbir işlevsellik
kaybetmezsiniz.

---

## Biz (geliştirici) hangi bilgiyi görüyoruz

AdMob'dan aldığımız tek reklam ilişkili veri AdMob konsolundaki
**toplu gelir ve gösterim sayısıdır** — "dün X gösterim, Y CPM,
Z USD gelir" gibi totaller, reklam yuvası başına, ülke başına. Birey
olarak sizin hakkınızda hiçbir şey görmüyoruz: gördüğünüz reklamları
değil, tıklayıp tıklamadığınızı değil, günün hangi saatinde
oynadığınızı değil.

---

## Bize nasıl ulaşırsınız

Bu sayfadaki herhangi bir nokta belirsizse veya 4+ yaş kategorimize
uygunsuz görünen bir reklam fark ettiyseniz, lütfen
**nfvwzhbrbw@privaterelay.appleid.com** adresine ekran görüntüsü ile
yazın. AdMob, belirli reklam verenleri kategori bazlı engellememize
izin veriyor ve deneyimi temiz tutmak için bunu düzenli olarak
kullanıyoruz.

---

## Bu sayfadaki değişiklikler

Reklam ayarlarındaki önemli değişiklikler (örneğin yeni bir reklam
SDK'sı eklenmesi veya önceden kapalı olan bir yuvanın açılması) önce
burada yansıtılır.
[Gizlilik Politikası](./privacy-policy-tr) aynı anda güncellenir ve
üstteki "Son güncelleme" tarihi neyin değiştiğini görebilmeniz için
güncellenir.

Son güncelleme: 16 Mayıs 2026
