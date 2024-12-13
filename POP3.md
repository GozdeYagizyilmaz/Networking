### Bir e-posta aldınız ve bunu yerel posta istemcinize indirmek istiyorsunuz. Posta Ofisi Protokolü sürüm 3 (POP3), istemcinin bir posta sunucusuyla iletişim kurmasına ve e-posta mesajlarını almasına olanak sağlamak için tasarlanmıştır.

### Çok teknik detaylara girmeden, bir e-posta istemcisi mesajlarını SMTP'ye güvenerek gönderir ve POP3 kullanarak alır.SMTP, zarfınızı veya paketinizi postaneye teslim etmeye benzer; POP3 ise yerel posta kutunuzu yeni mektuplar veya paketler için kontrol etmeye benzer.

![image](https://github.com/user-attachments/assets/58b65db4-2e19-4536-96ab-a7bba76867cf)

Bazı yaygın POP3 komutları şunlardır:

* **USER** <kullanıcı adı> kullanıcıyı tanımlar
* **PASS** <şifre> kullanıcının şifresini sağlar
* **STAT** mesaj sayısını ve toplam boyutu ister
* **LIST** tüm mesajları ve boyutlarını listeler
* **RETR** <mesaj_numarası> belirtilen mesajı alır
* **DELE** <mesaj_numarası> bir mesajı silinmek üzere işaretler
* **QUIT** silmeler gibi değişiklikleri uygulayarak POP3 oturumunu sonlandırır

### POP3 sunucusu varsayılan olarak TCP 110 portunu dinler.
