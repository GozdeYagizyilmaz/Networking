### TCP/IP bilgisayar ağları oluşturulurken öncelikle ağdaki her cihaza bir mantıksal adres (IP Adresi) atanmalıdır. Bu atama işlemlerine "IP Adresleme Mekanizması" adı verilmektedir.Ağdaki bir cihaza IP adresi atanmamışsa, ağ içindeki veya dışındaki cihazlarla iletişim kuramaz.

## IP Adresi nedir?
IP Adresi cihazın ağ adresinin kimliğidir. Bağlantı işlemleri IP adresleri kullanılarak gerçekleştirilir. IP adresleri IPv4 ve IPv6'ya bölünmüştür. Her iki IP adresi türüne örnek olarak aşağıdaki IP adresleri verilebilir:

**IPv4:** 192.168.4.1

**IPv6:** 2001:0db8:85a3:0000:0000:8a2e:0370:7334

## IP Adresinin Yapısı

IP adresi 4 bayttan (32 bit) oluşur. Her baytın arasına bir nokta konulur ve ondalık gösterimle ifade edilir. Örneğin, aşağıdaki resim IP adresinin ikili gösterim ile ondalık gösterim arasında dönüştürülmesini göstermektedir:

![image](https://github.com/user-attachments/assets/7dc9a694-6a3b-458f-bac1-55c1c3266292)

Her bayt 8 bitten oluştuğu için her baytın minimum değeri alabilmesi için 8 bitlik değerin "0" (sıfır) olması gerekir. Benzer şekilde maksimum değeri alabilmek için her bayt için 8 bitlik değerin "1" olması gerekir.
Örneğin IP adresindeki her bir baytın alabileceği minimum ve maksimum değerleri hesaplayalım: 

**Minimum (İkili): 00000000**

![image](https://github.com/user-attachments/assets/4fc527da-6e74-4d59-9f60-29bb0cb9db54)

Hesaplama sonucunda görüldüğü gibi "00000000" ikili ifadesinin ondalık karşılığı "0" (sıfır)'dır.

**Maksimum (İkili): 11111111**

![image](https://github.com/user-attachments/assets/50b9bd51-d955-4879-9012-b7a11bc5c59c)

Hesaplama sonucunda görülebileceği gibi IP adresinin her bir baytı “0-255” arasında bir değer alabilmektedir.

## IP Adresi Sınıfları

IP adresleri 5 sınıfa ayrılmıştır. IP adresinin sınıfını öğrenmek için IP adresinin ilk baytı kontrol edilir.İlk baytın ondalık değerine göre aşağıdaki tabloda IP adresinin hangi sınıflara ait olduğu anlaşılmaktadır.

![image](https://github.com/user-attachments/assets/8dcafa7a-7a0a-4a27-9798-99cab9bdbdc4)

Bu IP adresine sahip cihazın hangi ağa dahil olduğunu IP adresi üzerinden öğrenmek mümkündür. Bu bilginin öğrenilebilmesi için öncelikle IP adresinin hangi sınıfa ait olduğunun bilinmesi gerekmektedir.Daha sonra aşağıdaki tabloda yer alan “Ağ Bitleri” alanları kontrol edilir.

![image](https://github.com/user-attachments/assets/e4b73d22-9c28-4aa7-935a-0df36a3bf8e8)

**Örneğin "192.168.4.1" IP adresinin hangi sınıfa ait olduğunu ve ağ bitlerinin hangi bayt olduğunu öğrenelim:**

**Adım 1:** İlk baytın ondalık değerini kontrol edin: "192"
**Adım 2:** Tabloya göre “192” değerinin hangi sınıfa ait olduğu öğrenilir: “C Sınıfı”
**Adım 3:** Tabloya göre "C" sınıfına ait bir IP adresinin hangi baytlarının ağ bitlerine ait olduğu kontrol edilir: "ilk 3 bayt"

Edindiğimiz bilgilere göre ilk 3 byte'ı aynı olan IP adreslerinin aynı ağdaki cihazlara ait olduğu söylenebilir.Örneğin “192.168.4.1” IP adresi ile “192.168.4.2” IP Adresi aynı ağ üzerindedir. Çünkü yalnızca konak bitlerin bulunduğu baytta değişiklik olur. Ağ bitleri aynı değere sahiptir: 192.168.4.X

![image](https://github.com/user-attachments/assets/b0859e24-fdc3-4f94-9906-dc6635a011e0)

## IPv6 nedir?

Günümüzde internet ağına bağlı cihaz sayısı oldukça fazladır. Tüm bu cihazların bir IP adresine sahip olduğu düşünüldüğünde IPv4 artık yeterli olmamaktadır.Bu nedenle bu sorunu çözmek için bazı teknolojiler (NAT) ve IPv6 geliştirilmiştir. IPv6 ile birlikte sınırlı sayıda adrese sahip olan IPv4'ün kullanımı azalmaya başlamış ve yerini IPv6'ya bırakmıştır.
Aşağıdaki tabloda IPv4 ve IPv6 karşılaştırılmaktadır:

![image](https://github.com/user-attachments/assets/36a49fcf-095a-4106-bc86-c0cf209cbbf8)

## Özel IP Adresleri

IP adreslerinden bazıları özel amaçlar için ayrılmıştır. Bu ayrılmış IP adresleri özel ağlarda kullanılan IP adresleridir.Özel ağlar, internete doğrudan bağlı olmayan ve internete bir aracı ağ cihazıyla bağlanan ağlardır.
Örneğin, ev ağları ve şirket içi ağlar. Ev içi ağlarda modem cihazı internete bağlantı sağlar ve paket akışını yönetir.Modem cihazı ev ağına bakan bir ağ arayüzüne ve internet tarafına bakan bir ağ arayüzüne sahiptir. Özel ağ olarak adlandırılan kısım, modem cihazının ev ağı arayüzünün bulunduğu kısımdır.

Bu bölümdeki cihazların IP adresleri internet ortamında kullanılmayan ayrılmış IP adresleridir. Aşağıdaki tabloda özel IP adresi aralıkları gösterilmektedir:

![image](https://github.com/user-attachments/assets/59de16b2-0947-457e-93d0-51b835414d7d)

## Localhost nedir?

Localhost, cihazın kendi ağ adresini belirten IP adresi aralığıdır. Cihazda yerel olarak çalışan hizmetlere erişmek için kullanılır. Yaygın olarak "127.0.0.1" IP adresi olarak bilinir.Ancak “127.0.0.1 - 127.255.255.255” aralığındaki herhangi bir IP adresi bu amaçla kullanılabilir. Bir diğer adı da "geri döngü" adresidir.











