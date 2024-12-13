### Masaüstü bilgisayarınızdaki favori e-posta istemciniz gibi tek bir cihazdan çalışırken POP3 yeterlidir.Peki ya e-postanızı hem ofisinizdeki masaüstü bilgisayarınızdan hem de dizüstü bilgisayarınızdan veya akıllı telefonunuzdan kontrol etmek isterseniz ne olacak?

### Bu senaryoda, bir mesajı aldıktan sonra silmek yerine, mesajların senkronizasyonuna izin veren bir protokole ihtiyacınız vardır.Birden fazla cihazda senkronize bir posta kutusu sağlamanın bir çözümü İnternet İleti Erişim Protokolüdür (IMAP).

IMAP, okunan, taşınan ve silinen mesajların senkronize edilmesini sağlar. E-postanızı birden fazla istemci aracılığıyla kontrol ettiğinizde IMAP oldukça kullanışlıdır.E-postanın uzak sunucudan indirilmesi ve silinmesi nedeniyle sunucu depolama alanını en aza indirme eğiliminde olan POP3'ün aksine, e-posta sunucuda tutulduğu ve e-posta istemcileri arasında senkronize edildiği için IMAP daha fazla depolama alanı kullanma eğilimindedir.

IMAP protokol komutları POP3 protokol komutlarından daha karmaşıktır. Aşağıda birkaç örnek sıralıyoruz:

* **LOGIN** <kullanıcı adı> <şifre> kullanıcıyı doğrular
* **SELECT** <posta kutusu> çalışmak için posta kutusu klasörünü seçer
* **FETCH** <posta_numarası> <veri_öğesi_adı> Örnek fetch 3 body[] mesaj numarası 3, başlık ve gövdeyi almak için.
* **MOVE** <sequence_set> <posta kutusu> belirtilen iletileri başka bir posta kutusuna taşır
* **COPY** <sequence_set> <data_item_name> belirtilen iletileri başka bir posta kutusuna kopyalar
* **LOGOUT** oturumu kapatır

### IMAP sunucusunun varsayılan olarak TCP 143 portunu dinler.
