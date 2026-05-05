# Momentum — Gizlilik Politikası

**Yürürlük tarihi:** 2026-05-04  
**Son güncelleme:** 2026-05-04  
**Veri sorumlusu:** Murat Kul (bireysel geliştirici)  
**İletişim:** nfvwzhbrbw@privaterelay.appleid.com

Momentum ("Uygulama"), kişisel finans takibi için tasarlanmış bir mobil
uygulamadır. Bu Gizlilik Politikası, Momentum'u kullandığınızda hangi
verileri topladığımızı, nasıl kullandığımızı ve haklarınızı açıklar.

---

## 1. Topladığımız Veriler

Sizden yalnızca uygulamayı çalıştırmak için gerekli olan verileri toplarız.

### 1.1. Hesap verileri
- **E-posta adresi** — kayıt ve giriş için
- **Şifre** — Firebase Authentication tarafından hash'lenerek saklanır.
  Açık metin şifrenizi biz görmeyiz, sunucularımızda da saklamayız.

### 1.2. Finansal veriler (uygulama içeriği)
Bu veriler **siz** girersiniz; biz size sormayız, otomatik almayız:
- Varlıklar (ad, kategori, tutar, para birimi, açıklama)
- Borçlar (ad, kategori, tutar, para birimi, vade, faiz oranı)
- Aylık snapshot'lar (varlık ve borç değerlerinin o tarihteki anlık fotoğrafı)
- Giderler (ad, kategori, tutar, tarih)
- Tercihleriniz (temel para birimi, dil, tema, snapshot günü)

### 1.3. Cihaz verisi
- Yerel önbellekte (Hive) yalnızca **döviz kurları** saklanır. Kişisel
  veriniz cihazda **kalıcı olarak** tutulmaz; tüm kullanıcı verisi
  Google Cloud Firestore üzerindedir.

### 1.4. Tanı verileri (çökme raporları)
- Uygulama beklenmedik şekilde kapandığında, **Firebase Crashlytics**
  aracılığıyla aşağıdaki teknik bilgiler otomatik olarak toplanır:
  - Cihaz modeli, işletim sistemi sürümü, uygulama sürümü
  - Hata izi (stack trace) ve uygulama durumu
  - Anonim crash id
- Bu veri **kişisel finans bilgilerinizi içermez** (varlık, borç,
  snapshot tutarları gönderilmez).
- Yalnızca release build'lerde toplanır; geliştirme ve debug
  oturumlarında devre dışıdır.
- Amacı: prod ortamda oluşan hataları teşhis edip düzeltmek.

### 1.5. Toplamadığımız veriler
- ❌ Reklam tanımlayıcıları (IDFA / GAID)
- ❌ Konum verisi
- ❌ Rehber, fotoğraf, dosya erişimi
- ❌ Kullanım analitiği / davranış izleme (3. taraf analytics SDK yok)
- ❌ Banka API entegrasyonu (manuel veri girişi)

### 1.6. İleride eklenebilecek veri kategorileri

Aşağıdaki veri türleri **şu an toplanmamaktadır**. Gelecekteki bir
sürümde aktive edilirse, bu politikayı güncelleyip uygulama içinde
bildirim göstereceğiz. Açıkça belirtmediğimiz sürece bu kategorilerde
veri toplamıyoruz:

- **Push bildirim token'ı**: Bildirim aboneliği eklersek, Firebase Cloud
  Messaging tarafından üretilen anonim cihaz token'ı saklanır.
- **Anonim kullanım metriği**: Hangi ekranların kaç kere açıldığı,
  uygulama sürüm dağılımı (kişisel veri içermeden).
- **Ödeme verisi**: İleride ücretli özellik eklenirse, ödemeler **Apple
  App Store / Google Play** tarafından işlenir. Kart bilginizi biz
  görmeyiz; yalnızca abonelik durumunu doğrulamak için makbuz
  alırız.
- **Açık Bankacılık (Open Banking) verileri** (opt-in): Banka hesabı
  bağlama özelliği eklenirse, açık rızanızla işlem geçmişi ve bakiye
  çekilir. Bu özellik isteğe bağlı olur; bağlamazsanız hiçbir banka
  verisi alınmaz.
- **AI / öneri motoru** (opt-in): İleride AI tabanlı analiz özellikleri
  eklenirse, sadece açık onayınız ile seçtiğiniz veriler AI sağlayıcıya
  gönderilir. Veri sağlayıcı tarafında saklanmaz.

Bu özelliklerin **hiçbiri** açıkça aktive edilmeden veri toplamaz.

---

## 2. Verileri Nasıl Kullanıyoruz

| Amaç | Veri |
|---|---|
| Hesabınıza giriş yapmanızı sağlamak | E-posta, şifre (hash) |
| Verilerinizi saklamak ve cihazlar arası senkronize etmek | Tüm finansal veriler |
| Çoklu para biriminde tutarları normalize etmek | Döviz kurları (cihazda cache) |
| Kanun gereği bilgi paylaşımı talep edildiğinde yetkililere yanıt vermek | Hesap kimliği |

Verilerinizi **reklam, profilleme, satış veya pazarlama** amacıyla
kullanmıyoruz. 3. taraflara satmıyor, paylaşmıyoruz.

---

## 3. Verilerin Saklandığı Yer

- **Google Cloud Firestore** (Google LLC, ABD/AB sunucuları). Firebase
  Security Rules ile yalnızca giriş yapmış kullanıcı kendi verisine
  erişebilir; başka kullanıcılar erişemez.
- **Cihazınız** (lokal Hive cache — yalnızca döviz kurları).

Firebase'in kendi gizlilik politikası:
https://firebase.google.com/support/privacy

---

## 4. Üçüncü Taraf Hizmetler

### 4.1. Şu an kullanılan hizmetler

| Hizmet | Amaç | Aktarılan veri |
|---|---|---|
| Firebase Authentication (Google) | Kullanıcı kimlik doğrulama | E-posta, şifre hash |
| Cloud Firestore (Google) | Veri saklama ve sync | Finansal veriler, tercihler |
| Firebase Crashlytics (Google) | Çökme raporları (release build) | Cihaz modeli, OS sürümü, hata izi — finansal veri içermez |
| OpenExchangeRates API | Güncel döviz kuru | Yalnızca anonim API isteği — kullanıcı verisi gönderilmez |

Apple App Store üzerinden indirme/yükleme sürecinde Apple'ın kendi
politikaları geçerlidir.

### 4.2. İleride kullanılabilecek hizmetler

Aşağıdaki hizmetler şu an aktif değildir; aktive edildiklerinde bu tablo
güncellenir ve uygulama içinde bildirim gösterilir:

- **Firebase Cloud Messaging** (Google) — push bildirimleri için
- **Apple StoreKit / Google Play Billing** — ücretli özellikler için
- **Açık Bankacılık (Open Banking) sağlayıcıları** — opt-in banka
  bağlantısı için
- **AI sağlayıcıları** (örn. Anthropic, OpenAI) — opt-in öneri motoru
  için

---

## 5. Veri Saklama Süresi

- Hesabınız aktif olduğu sürece verileriniz saklanır.
- Hesabınızı sildiğinizde (Ayarlar → Hesabı Sil) tüm finansal verileriniz
  Firestore'dan silinir, ardından kimlik bilgileriniz Firebase
  Authentication'dan kaldırılır. Bu işlem **geri alınamaz**.
- Yedeklerde 30 günlük teknik gecikme olabilir (Google Firebase'in
  altyapı yedek politikası).

---

## 6. Haklarınız (KVKK / GDPR)

Veri sahibi olarak şu haklara sahipsiniz:

- ✅ **Erişim hakkı**: Hangi verileri tuttuğumuzu öğrenebilirsiniz.
  Tüm veriler uygulamada size görünür durumda.
- ✅ **Düzeltme hakkı**: Yanlış veriyi uygulama içinde düzenleyebilirsiniz.
- ✅ **Silme hakkı (unutulma)**: Ayarlar → Hesabı Sil ile tek tıkla
  tüm verinizi sileriz.
- ✅ **Veri taşınabilirliği**: Ayarlar → Veriyi Dışa Aktar ile CSV/PDF
  formatında dışa aktarabilirsiniz.
- ✅ **İşleme itiraz hakkı**: Bize e-posta atın, talebinizi 30 gün
  içinde işleriz.

KVKK / GDPR kapsamındaki taleplerinizi yukarıdaki iletişim adresine
iletebilirsiniz.

---

## 7. Çocukların Gizliliği

Momentum 13 yaşın altındaki kullanıcılara yönelik değildir. Bu yaş
grubundaki bir kullanıcının kayıt olduğunu fark edersek, hesabı sileriz.

---

## 8. Güvenlik

- Tüm veri trafiği TLS (HTTPS) üzerinden şifrelenir.
- Firestore Security Rules ile her kullanıcı yalnızca kendi verisine
  erişebilir (`request.auth.uid == userId` kuralı).
- Şifreniz hiçbir zaman açık metin olarak saklanmaz; Firebase Auth
  tarafından PBKDF2-SHA256 ile hash'lenir.
- Lokal cihaz cache'i (Hive) finansal veri içermez.

Hiçbir sistem %100 güvenli değildir. Bir güvenlik ihlali fark edersek,
yasal yükümlülüğümüz çerçevesinde sizi 72 saat içinde bilgilendiririz.

---

## 9. Politikadaki Değişiklikler

Bu politika güncellenirse, yeni sürümün yürürlük tarihini buraya
yazarız. Önemli değişiklikler için uygulama içinde de bildirim
göstereceğiz.

---

## 10. İletişim

Veri talepleri, sorular veya endişeler için:  
**E-posta:** nfvwzhbrbw@privaterelay.appleid.com
