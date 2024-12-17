![image](https://github.com/user-attachments/assets/c2ec6adc-c745-40ea-b1e1-baae9948805b)


### Telnet kullandığınızda ağ trafiğini izleyen herhangi birinin oturum açma bilgilerinizi ele geçirmesi kolaydır. Bu sorun bir çözüm gerektiriyordu.Tatu Ylönen, Secure Shell (SSH) protokolünü geliştirdi ve SSH-1'i 1995'te ücretsiz yazılım olarak yayınladı. (İlginçtir ki, aynı yıl Netscape Communications da SSL 2.0 protokolünü yayınladı.)

### Daha güvenli bir versiyonu olan SSH-2, 1996 yılında tanımlandı. 1999 yılında OpenBSD geliştiricileri, SSH'nin açık kaynaklı bir uygulaması olan OpenSSH'yi yayınladı.
### Günümüzde, bir SSH istemcisi kullandığınızda, büyük olasılıkla OpenSSH kütüphanelerine ve kaynak koduna dayanmaktadır. OpenSSH çeşitli avantajlar sunar. Birkaç önemli noktayı listeleyeceğiz:

* **Güvenli kimlik doğrulama:** Parola tabanlı kimlik doğrulamanın yanı sıra SSH, açık anahtar ve iki faktörlü kimlik doğrulamayı destekler.
* **Gizlilik:** OpenSSH, dinlemeye karşı koruma sağlayan uçtan uca şifreleme sağlar. Ayrıca, aracı saldırılara karşı koruma sağlamak için yeni sunucu anahtarlarını size bildirir.
* **Bütünlük:** Kriptografi, değiştirilen verilerin gizliliğini korumanın yanı sıra trafiğin bütünlüğünü de korur.
* **Tünelleme:** SSH, diğer protokolleri SSH üzerinden yönlendirmek için güvenli bir "tünel" oluşturabilir. Bu kurulum, VPN benzeri bir bağlantıya yol açar.
* **X11 Yönlendirme:** Eğer grafiksel kullanıcı arayüzüne sahip Unix benzeri bir sisteme bağlanıyorsanız, SSH ağ üzerinden grafiksel uygulamayı kullanmanıza olanak tanır.

### Bir SSH sunucusuna bağlanmak için ssh username@hostname komutunu vermeniz gerekir.Kullanıcı adınız oturum açtığınız kullanıcı adınızla aynıysa, yalnızca ssh ana bilgisayar adına ihtiyacınız vardır. Ardından, bir parola sorulacaktır; ancak, açık anahtar kimlik doğrulaması kullanılırsa, hemen oturum açacaksınız.
Aşağıdaki ekran görüntüsü Wireshark'ın uzak bir Kali Linux sisteminde çalıştırılmasına dair bir örneği göstermektedir.-X argümanı, örneğin ssh 192.168.124.148 -X gibi grafiksel arayüzlerin çalıştırılmasını desteklemek için gereklidir. (Yerel sistemde uygun bir grafiksel sistemin kurulu olması gerekir.)

![image](https://github.com/user-attachments/assets/65394114-30ab-4456-8a7f-92dc84aa230a)

TELNET sunucusu 23 numaralı bağlantı noktasını dinlerken, SSH sunucusu 22 numaralı bağlantı noktasını dinler.

