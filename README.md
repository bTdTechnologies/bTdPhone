# bTd Phone

Kurumsal kullanim icin hazirlanmis Android SIP istemcisi. [Linphone Android](https://github.com/BelledonneCommunications/linphone-android)
(Belledonne Communications, GPLv3) uzerine kurulu, yeniden markalanmis ve sadelestirilmis bir surumdur.

Based on Linphone (c) Belledonne Communications. Bu proje GNU GPL v3 ile lisanslidir (`LICENSE.txt`).
Kaynak: Linphone `c3a08d8` kaydindan (upstream) turetilmistir; asil gecmis ve yazarlar icin upstream depoya bakin.

## Fark nelerdir
- Ad `bTd Phone`, paket `tr.net.btd.phone`; kendi simge ve turuncu-lacivert tema.
- Giris ekraninda yalniz dahili numara ve parola; varsayilan alan `pbx.example.com`, TLS, SRTP zorunlu.
- Giriste sirket rehberi (CardDAV) otomatik eklenir; gorunen ad rehber kartindan alinir.
- Linphone sunucularina giden gunluk, surum denetimi ve STUN trafigi kapatildi.

## Derleme
Ornek degerler (`pbx.example.com`, `hata@example.com`) yer tutucudur. Kendi sunucunuzun alan adini ve rehber adresini `app/src/main/assets/linphonerc_factory` icinde, hata e-postasini `app/src/main/res/values/strings.xml` icinde yazin.

Bu depoda **bulunmayan** dosyalar (kendiniz saglayin):
- `app/google-services.json` (kendi Firebase projeniz; yoksa anlik bildirim kapali derlenir)
- `keystore.properties` ve imza anahtari (kendi anahtariniz)

```
./gradlew assembleRelease
```
Ayrinti icin `UPSTREAM-README.md`.
