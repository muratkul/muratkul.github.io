---
layout: default
title: Gizlilik Politikası
---

> **Diller:** [English](./privacy-policy) · **Türkçe** · [Español](./privacy-policy-es)

# Gizlilik Politikası

**Yürürlük tarihi:** 16 Mayıs 2026
**Son güncelleme:** 16 Mayıs 2026

Bu Gizlilik Politikası, **Sudoku Arena Online** ("Uygulama", "biz")
mobil uygulamasını kullandığınızda hangi bilgileri topladığımızı, nasıl
kullandığımızı ve nasıl koruduğumuzu açıklar. Uygulama İstanbul,
Türkiye'de yerleşik **Murat Kul** ("geliştirici") tarafından
işletilmektedir.

Uygulamayı kullanarak aşağıda anlatılan uygulamaları kabul etmiş
olursunuz. Kabul etmiyorsanız lütfen Uygulamayı kullanmayın.

---

## 1. Biz kimiz

| | |
|---|---|
| Uygulama adı | Sudoku Arena Online |
| Geliştirici | Murat Kul |
| Ülke | Türkiye |
| İletişim | nfvwzhbrbw@privaterelay.appleid.com |

Bu bağımsız bir projedir. Bölüm 4'te listelenen altyapı sağlayıcıları
(Firebase / Google AdMob), bizim adımıza veri işleyen tek üçüncü
taraflardır.

---

## 2. Neleri topluyoruz

Yalnızca Uygulamanın çalışması ve kişiselleştirilmemiş reklam
sunabilmek için gerekli olanı topluyoruz. Rehber, fotoğraf, konum,
sağlık verisi veya finansal veri **toplamıyoruz**.

### 2.1 Hesap verileri

**Google** veya **Apple** ile giriş yaptığınızda kimlik sağlayıcıdan
şunları alırız:

- Benzersiz bir kullanıcı kimliği (Firebase UID)
- Görünen ad
- E-posta adresi (Apple, Private Relay adresi döndürebilir)
- Profil fotoğrafı URL'i (görsel verisi değil, sadece referans)

**Misafir Olarak Devam Et** seçeneğini kullanırsanız sadece anonim bir
Firebase UID üretilir. Ad, e-posta veya fotoğraf toplanmaz.

### 2.2 Oynanış verileri

Çok oyunculu servisi çalıştırmak için Firestore'da şunları saklarız:

- Katıldığınız aktif maçlar: bulmaca, durum, oyuncular, hata sayısı,
  doldurulmuş hücre sayısı, bitirme zamanı, kazanan UID
- Rakip ararken eşleşme bileti: UID'niz, görünen ad, fotoğraf URL'i,
  mod, zorluk seviyesi, zaman damgası
- Kullanıcı belgenizdeki aktif maç referansı (`currentMatchId`)

### 2.3 Cihazda kalan veriler

Aşağıdaki veriler yalnızca cihazınızda kalır ve sunucularımıza
gönderilmez:

- Kaydettiğiniz tek oyunculu oturum ("Devam") ve oyun ayarları —
  yerel Hive veritabanında
- Tema, dil, titreşim ve diğer tercihleriniz — SharedPreferences'ta

### 2.4 Reklam verileri

Uygulama, reklam sunmak için Google AdMob'u kullanır. AdMob bizim
adımıza şunları işleyebilir:

- **iOS'ta Apple Reklam Tanımlayıcısı (IDFA)** — AdMob bunu reklam
  dolandırıcılığını önlemek ve Apple SKAdNetwork çerçevesi üzerinden
  yükleme atfı yapmak için kullanır. Yalnızca **kişiselleştirilmemiş
  reklam** (`npa=1`) talep ediyoruz; yani AdMob IDFA'yı sizinle ilgili
  bir reklam profili oluşturmak için **kullanmaz**. Uygulama, cihazlar
  arası izleme yapmadığı için App Tracking Transparency ekranı
  göstermez.
- **Android'de Google Reklam Kimliği (AAID)** — IDFA ile aynı rol,
  aynı kişiselleştirilmemiş yapılandırma.
- **AdMob'un COPPA / GDPR / KVKK / IAB TCF uyumu için ihtiyacı olan
  kaba sinyaller** (ör. ülke, cihaz modeli, OS sürümü, sadece ülke
  türetmek için IP adresi). Bunlar Google tarafından işlenir,
  geliştirici olarak bize hiç gösterilmez.
- **Ödüllü reklam izleyip ekstra ipucu kazandığınızda** sadece "izleme
  tamamlandı mı?" sinyali alınır — reklamın içeriği değil.

iOS'ta Limit Ad Tracking'i açabilir (Ayarlar → Gizlilik ve Güvenlik →
Apple Reklamcılık) veya Android'de Reklam Kimliğinizi
sıfırlayabilirsiniz (Ayarlar → Google → Reklamlar). Limit Ad Tracking
açıkken AdMob yine kişiselleştirilmemiş reklam servis eder, sadece
dolandırıcılık tespit sinyalleri azalır.

---

## 3. Neden topluyoruz

| Amaç | Kullanılan veri |
|---|---|
| Sizi tanımak ve maçlarınızı belirlemek | Hesap verileri |
| Bir rakiple eşleştirmek | Eşleşme bileti, hesap verileri |
| Maçı çalıştırmak ve rakibinizin ilerlemenizi görmesini sağlamak | Oynanış verileri |
| Ana ekranda "Devam" kartını göstermek | Cihazda kalan veriler |
| Kişiselleştirilmemiş reklam servis etmek + dolandırıcılık kontrolü | Reklam verileri |
| Apple SKAdNetwork üzerinden yükleme atfı | Reklam verileri |
| Çökmeleri tespit etmek ve düzeltmek | Çökme tanı verileri (Crashlytics) |

Kişisel verilerinizi satmıyoruz ve sizin için pazarlama profili
oluşturmuyoruz. Bölüm 2.4'te listelenen reklam tanımlayıcıları
**yalnızca kişiselleştirilmemiş reklam ve dolandırıcılık tespiti**
için kullanılır; herhangi bir izleme SDK'sı, atıf SDK'sı veya kitle
segmentasyonu özelliği etkinleştirmedik.

---

## 4. Üçüncü taraf servisleri

Uygulama backend olarak Google LLC tarafından işletilen **Firebase**'i
kullanır:

- **Firebase Authentication** — Google, Apple ya da anonim girişleri
  yönetir.
- **Cloud Firestore** — maç belgelerini ve kullanıcı kayıtlarını
  saklar.
- **Firebase Remote Config** — çalışma zamanı yapılandırmasını
  (eşleşme zaman aşımı, reklam yerleşim bayrakları vb.) çeker. Kişisel
  veri gönderilmez — Google'a sadece doğru config payload'unu iletmesi
  için genel bir kurulum tanımlayıcısı gider.
- **Firebase Crashlytics** — kişiselleştirilmemiş çökme tanılaması
  kaydeder, sadece Uygulama çöktüğünde gönderilir.
- **Google Sign-In** ve **Sign in with Apple** — federe kimlik
  sağlayıcıları.

Uygulama ayrıca reklam sunmak için Google LLC tarafından işletilen
**Google AdMob**'u içerir. AdMob'un neyi topladığı ve nasıl
yapılandırıldığı için bölüm 2.4'e bakın.

Bu servisler bizim adımıza **veri işleyen** sıfatıyla hareket eder.
Verilerinize sahip değillerdir. Gizlilik uygulamaları:

- [Google Gizlilik Politikası](https://policies.google.com/privacy)
- [Google'ın hizmetlerimizi kullanan site veya uygulamalardan elde ettiği bilgileri nasıl kullandığı](https://policies.google.com/technologies/partner-sites)
- [Apple Gizlilik Politikası](https://www.apple.com/legal/privacy/)

Üçüncü taraf servis listesi gelecekteki sürümlerde değişebilir;
güncellemeleri nasıl ilettiğimiz bölüm 11'de.

---

## 5. Veri konumu ve güvenliği

Veriler Firebase tarafından kullanılan Google Cloud bölgelerinde
(genelde `us-central1` veya Firebase'in seçtiği başka bir bölge)
saklanır. Uygulama ile Firebase arasındaki tüm trafik TLS ile
şifrelidir. Firestore, verileri varsayılan olarak diskte de
şifreler.

---

## 6. Saklama süresi

Verileriniz yalnızca hesabınız aktif olduğu sürece saklanır:

- **Hesap kaydı** (`users/{uid}`) — siz hesabınızı silene kadar.
- **Eşleşme bileti** — 30 saniye içinde (zaman aşımı) veya eşleşme
  bulunduğunda / iptal ettiğinizde anında silinir.
- **Maç belgeleri** — her iki katılımcının geçmişini görebilmesi için
  süresiz saklanır. UID, görünen ad ve bölüm 2.2'deki metrikler
  dışında bilgi içermez.
- **Cihazda kalan veriler** — Uygulamayı silene kadar.

---

## 7. Haklarınız

Avrupa Ekonomik Alanı, Birleşik Krallık veya Türkiye (KVKK) sınırları
içinde bulunuyorsanız şu haklara sahipsiniz:

- Hakkınızda tuttuğumuz kişisel verilere erişme
- Yanlış verileri düzelttirme
- Verilerinizi sildirme ("unutulma hakkı")
- Verilerinizi taşınabilir formatta dışa aktarma
- İşlemeye itiraz etme veya sınırlandırma
- Yerel veri koruma otoritenize şikayette bulunma

Bu haklardan herhangi birini kullanmak için
**nfvwzhbrbw@privaterelay.appleid.com** adresine yazın. 30 gün
içinde dönüş yapıyoruz.

---

## 8. Hesap silme

Hesabınızı Uygulama içinden istediğiniz zaman silebilirsiniz:

> **Ayarlar → Hesabı sil**

Bu işlem:

1. Sizi giriş sağlayıcınızla yeniden kimliklendirir (güvenlik
   kontrolü).
2. Kullanıcı kaydınızı ve bekleyen eşleşme biletinizi Firestore'dan
   kalıcı olarak siler.
3. Firebase Authentication kullanıcınızı kalıcı olarak siler.
4. Sizi çıkış yaptırır.

Silme sonrası, UID'niz katıldığınız tarihsel maç belgelerinde, oyun
sırasında rakibinizin gördüğü görünen ad ve fotoğraf URL'i ile
birlikte hâlâ görünebilir. Bu maç belgeleri kendi başına kişisel
olarak tanımlanabilir değildir.

Uygulama içi seçeneğe herhangi bir nedenle ulaşamıyorsanız
**nfvwzhbrbw@privaterelay.appleid.com** adresine yazın; hesabınızı 30
gün içinde manuel olarak sileceğiz.

---

## 9. Çocuklar

Uygulama **13 yaş altı çocuklara yönelik değildir** (veya bulunduğunuz
ülkedeki eşdeğer asgari yaş sınırı). Çocuklardan bilerek veri
toplamıyoruz. Bir çocuğun bize kişisel veri verdiğini düşünüyorsanız
iletişime geçin, sileceğiz.

---

## 10. Uluslararası transferler

Uygulama Türkiye'de geliştiriliyor, ancak altyapı (Google Firebase)
veriyi Türkiye ve EEA dışına aktarabilir. Google'ın altyapısı bu
transferler için Avrupa Komisyonu tarafından onaylanmış standart
sözleşme maddelerini kullanır.

---

## 11. Politika değişiklikleri

Bu Gizlilik Politikasını zaman zaman güncelleyebiliriz. Sayfanın
üstündeki "Yürürlük tarihi" en son sürümü yansıtır. Önemli
değişiklikler için yeni politika yürürlüğe girmeden en az 7 gün önce
Uygulama içinde bildirim yayınlayacağız.

---

## 12. İletişim

Her türlü gizlilik sorusu, talebi veya şikayeti için:

> **Murat Kul**
> nfvwzhbrbw@privaterelay.appleid.com
> İstanbul, Türkiye
