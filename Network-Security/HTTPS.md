![image](https://github.com/user-attachments/assets/d079e764-2c28-4134-bfd2-1894367e98d7)


### HTTPS, Hypertext Transfer Protocol Secure'un kısaltmasıdır. Temel olarak TLS üzerinden HTTP'dir. Sonuç olarak, HTTPS üzerinden bir sayfa istemek (alan adını çözdükten sonra) aşağıdaki üç adımı gerektirir:

1- **Hedef sunucuyla TCP üç yönlü el sıkışması kurun** 
2- **TLS oturumu kurun**
3- **HTTP protokolünü kullanarak iletişim kurun; örneğin, GET / HTTP/1.1 gibi HTTP istekleri yayınlayın**

### Aşağıdaki ekran görüntüsü, 1 ile işaretlenen ilk üç pakette bir TCP oturumunun kurulduğunu gösteriyor. Daha sonra, 2 ile işaretlenen TLS protokolünde müzakere etmek için birkaç paket değiştiriliyor.Son olarak, 3 ile işaretlenen HTTP uygulama verileri değiştirilir. Wireshark ekran görüntüsüne baktığımızda, bunun gerçekten HTTP mi yoksa 443 portu üzerinden gönderilen başka bir protokol mü olduğunu bilmenin bir yolu olmadığı için Application Data-"Uygulama Verileri" yazdığını görüyoruz.

![image](https://github.com/user-attachments/assets/6a19d6a4-22da-44b9-87cc-52ac5367d779)

### Beklendiği üzere, eğer birisi paket akışını takip etmeye ve tüm içeriklerini birleştirmeye çalışırsa, aşağıdaki ekran görüntüsünde görüldüğü gibi sadece anlamsız bir sonuç elde edecektir.Değiştirilen trafik şifrelenir; kırmızı istemci tarafından gönderilir ve mavi sunucu tarafından gönderilir. Şifreleme anahtarını edinmeden içerikleri bilmenin bir yolu yoktur.

![image](https://github.com/user-attachments/assets/242199da-cdf3-4ec1-9c26-1651469e5fb7)

## Şifreleme Anahtarını Alma

HTTP'ye TLS eklemek tüm paketlerin şifrelenmesine yol açar. Özel anahtara erişim sağlamadığımız sürece artık değiştirilen paketlerin içeriklerini göremeyiz.
TLS oturumunda şifreleme için kullanılan anahtarlara erişmemiz pek mümkün görünmese de, Wireshark'a şifre çözme anahtarını verdikten sonra yukarıdaki ekran görüntülerini tekrarladık.TCP ve TLS el sıkışmaları değişmez; asıl fark 3 olarak işaretlenen HTTP protokolüyle başlar. Örneğin, istemcinin GET gönderdiğini görebiliriz.

![image](https://github.com/user-attachments/assets/bc820f47-1698-432f-bfa4-53498126e790)

Eğer veri alışverişini görmek istiyorsanız, şimdi tam zamanı! Hala meraklı gözlerden gizlenmiş normal HTTP trafiğidir.

![image](https://github.com/user-attachments/assets/005106de-c907-4759-8d2e-50a3e8aa84be)

### Önemli çıkarım, TLS'nin alt veya üst katman protokollerinde herhangi bir değişiklik gerektirmeden HTTP için güvenlik sağlamasıdır. Başka bir deyişle, TCP ve IP değiştirilmedi, HTTP ise TCP üzerinden gönderileceği şekilde TLS üzerinden gönderildi.



