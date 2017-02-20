# Android Marshmallow Encryption

I know there my be plenty of people who may aboslutely slate my use of an Android device. But it's all I have and can afford, like many in the world. If the only way to secure ourselves is by having a premium model phone, then we have a problem Houston.

The following are tools and methods I am using in an effort to secure myself. I'd love to hear from you ways in which this could be improved!

* [DNS Changer](https://play.google.com/store/apps/details?id=com.anythingintellect.freednschanger) - Allows you to switch between a variety of DNS providers (Custom, Google, Open DNS, Yandex, Level3, Comodo Secure, DNS.WATCH, Security DNS, Security + Block Porn DNS, Security + Blovk Porn + Non-Family Freindly)
* [Signal](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms) - I'm using it. Have tested voice calls and it was rubbish, making us switch to Whatsapp.
* [ProtonMail](https://play.google.com/store/apps/details?id=ch.protonmail.android) - Encrypted Mail
* [Riot](https://play.google.com/store/apps/details?id=im.vector.alpha) - I've written elsewhere about testing Riot. It's still in BETA so not as hardened as it yet may be.
* [Authy](https://play.google.com/store/apps/details?id=com.authy.authy) - Until I recently got a Yubikey this has been my preference.
* [Orbot](https://play.google.com/store/apps/details?id=org.torproject.android) - Tor over on Android. I've even seen tech book publishers blocked on some networks. Yes plural.
* [Orfox](https://play.google.com/store/apps/details?id=info.guardianproject.orfox) - Tor Browser on Android
* Password Authenticated Lock Screen - Drawing shapes, or not having one at all, are relatively eay to break. I've gone for something pretty long here and a mix of characters.
* Encrypted Storage - I've done this to the local storage AND the external Micro SD Card.

# How to Encrypt Storage on an Android Device

I'm showing steps on Marshmallow (Android 6).

1. **First setup a lockscreen password**
2. Security in order of easiest to hardest to crack - swipe, pattern, pin, password
3. Go to `Settings`
4. Select `Lock Screen and Security`
5. Select `Screen lock type`
6. Select `Password`
7. Enter y0ur_cr@zy_p@$$w0rd [obviously choose your own one here]
8. Enter y0ur_cr@zy_p@ssw0rd [again]
9. **Then encrypt local storage**
10. Go to `Settings`
11. Select `Lock Screen and Security`
12. Select `Encrypt Phone/Tablet`
13. Select `Encrypt`
14. Enter y0ur_cr@zy_p@$$w0rd [keep in mind if you forget this you will be locked out of your device and all its data - that's the whole point!]
15. Plug your device into the charger
16. Select `Encrypt`
17. Each time your switch on your device you will need to enter y0ur_cr@zy_p@$$w0rd
18. **Encrypt your SD card**
19. Go to `Settings`
20. Select `Lock Screen and Security`
21. Select `Encrypt SD Card`
22. Select `Encrypt SD Card`
23. Enter y0ur_cr@zy_p@$$w0rd
24. Select `Encrypt`


