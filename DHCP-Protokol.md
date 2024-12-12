## Bir ağa erişmek istediğimizde en azından aşağıdakileri yapılandırmamız gerekir:
* IP adresi alt ağ maskesiyle birlikte
* Yönlendirici (veya ağ geçidi) (Router or Gateway)
* DNS sunucusu (DNS Server)

Cihazımızı yeni bir ağa bağladığımızda yukarıdaki konfigürasyonların yeni ağa göre ayarlanması gerekmektedir.Bu ayarları elle yapılandırmak iyi bir seçenektir, özellikle sunucular için. Sunucuların ağları değiştirmesi beklenmez; etki alanı denetleyicinizi taşımaz ve onu kahve dükkanının WiFi'ına bağlamazsınız.Ayrıca diğer cihazların da sunuculara bağlanıp onları belirli IP adreslerinde bulmayı beklemesi gerekiyor.

Bağlı cihazları yapılandırmanın otomatik bir yolunun olması birçok avantaja sahiptir. İlk olarak, ağı manuel olarak yapılandırmaktan bizi kurtarırdı; bu özellikle mobil cihazlar için son derece önemlidir.

İkincisi, bizi adres çakışmalarından kurtarır, yani iki cihaz aynı IP adresiyle yapılandırıldığında. Bir IP adresi çakışması, ilgili ana bilgisayarların ağ kaynaklarını kullanmasını engeller; bu yerel kaynaklar ve İnternet için geçerlidir.

Çözüm, Dinamik Ana Bilgisayar Yapılandırma Protokolü'nü (DHCP) kullanmaktır.DHCP, UDP'ye dayanan uygulama düzeyinde bir protokoldür; sunucu UDP 67 portunu dinler ve istemci UDP 68 portundan gönderir. Akıllı telefonunuz ve dizüstü bilgisayarınız varsayılan olarak DHCP kullanacak şekilde yapılandırılmıştır.

### IP adresleri, fiziksel olarak bir cihaza girilerek elle veya otomatik olarak ve en yaygın olarak bir DHCP (Dinamik Ana Bilgisayar Yapılandırma Protokolü) sunucusu kullanılarak atanabilir. Bir cihaz bir ağa bağlandığında, daha önce elle bir IP adresi atanmamışsa, ağda herhangi bir DHCP sunucusu olup olmadığını görmek için bir istek (DHCP Discover) gönderir. 
## DHCP sunucusu daha sonra cihazın kullanabileceği bir IP adresiyle (DHCP Teklifi) yanıt verir. Cihaz daha sonra teklif edilen IP Adresini istediğini doğrulayan bir yanıt gönderir (DHCP Talebi) ve son olarak DHCP sunucusu bunun tamamlandığını onaylayan bir yanıt gönderir ve cihaz IP Adresini kullanmaya başlayabilir (DHCP ACK).

![image](https://github.com/user-attachments/assets/11baaeca-b2c9-495e-b7c4-ddc733d5230c)

### Ağlarımızda, tüm son kullanıcı cihazlarının ağa erişmek için bir IP adresine ihtiyacı vardır. Statik IP adresleri genellikle yönlendiricilere, anahtarlardaki yönetim arayüzlerine, sunuculara ve ağdaki fiziksel veya mantıksal olarak konum değiştirmeyen diğer cihazlara atanır. Statik IP adresleri ayrıca bu cihazlara uzaktan erişmek ve onları yönetmek için kullanılır. Öte yandan, bilgisayarlar, akıllı telefonlar, IP telefonları ve diğerleri gibi kullanıcı cihazlarının konumlarını fiziksel veya mantıksal olarak değiştirmeleri muhtemeldir. Bu, onlara statik IP adresleri atamanın uygulanamaz bir çözüm olacağı anlamına gelir. DHCP, bu sorunları çözmek için icat edilmiş bir protokoldür. DHCP ile IP adres bilgilerini kullanıcı düğümlerine otomatik olarak atayabiliriz, bu da istemcilere statik olarak IP adresleme bilgisi atamakla ilgili olacak idari yükü azaltır. 

## DHCP İşlemi 
Kullanıcı cihazlarına IP adresleme bilgisi atamak, ağlarımızdaki DHCP sunucuları tarafından gerçekleştirilen en önemli görevlerden biridir. Bu görevleri üç yoldan biriyle gerçekleştirir: 

**Manuel IP tahsisi** – bu tür DHCP tahsisinde, ağ yöneticisi kullanıcılara DHCP sunucusundan IP adresleri atar ve ardından DHCP sunucusu bu bilgileri istemcilere iletir. 

**Otomatik IP tahsisi** – bu modda, DHCP sunucusu istemcilere bir havuzdan statik IP adresleri atar. Bu adresler, yönetici farklı şekilde yapılandırmadığı sürece değişmez. 

**Dinamik IP tahsisi** – bu modda, yönetici istemcilere atanabilecek bir adres havuzu yapılandırır. İstemciler daha sonra DHCP sunucusundan IP adresleme bilgilerini ister ve kendilerine belirli bir zaman aralığı için bir IP adresi ve diğer adresleme bilgileri verilir, zaman dolduğunda IP adresi DHCP havuzuna döndürülür ve istemcinin başka bir IP adresi istemesi gerekir.

### Bir PC bir DHCP sunucusuna bağlandığında, DHCP sunucusu genellikle ona IP adresleme bilgisi verir. PC, belirtilen kiralama süresi sona erene kadar kendisine atanan IP adresleme bilgisini kullanabilir. Aşağıdaki şekil, bir istemci ile bir DHCP sunucusu arasındaki DHCP sürecini göstermektedir.

![image](https://github.com/user-attachments/assets/b24ff9a6-37a1-4c23-ac0d-5b64f360e27b)

### DHCP dört adımı izler: Keşfetme, Teklif Etme, Talep Etme ve Onaylama 

**DHCP Discover:** İstemci, varsa yerel DHCP sunucusunu arayan bir DHCPDISCOVER mesajı yayınlar. 
**DHCP Offer:** Sunucu, istemcinin kabul edebileceği bir IP adresi içeren bir DHCPOFFER mesajıyla yanıt verir.
**DHCP İsteği:** İstemci, teklif edilen IP'yi kabul ettiğini belirtmek için bir DHCPREQUEST mesajıyla yanıt verir. 
**DHCP Onayı:** Sunucu, teklif edilen IP adresinin artık bu istemciye atandığını doğrulamak için bir DHCPACK mesajıyla yanıt verir.

![image](https://files.oaiusercontent.com/file-Jq2gCUdX6NAwLdsMMwJSQ8?se=2024-12-12T06%3A52%3A47Z&sp=r&sv=2024-08-04&sr=b&rscc=max-age%3D604800%2C%20immutable%2C%20private&rscd=attachment%3B%20filename%3D824c0096-d7d4-4504-9535-b6d81a40a61c.webp&sig=HoRCDUUSiER37j09IMDr03rN/53krMN3C7r1JYg/mAE%3D)

Aşağıdaki paket yakalama yukarıda açıklanan dört adımı göstermektedir. Bu örnekte, istemci 192.168.66.133 adresini alır.

![image](https://github.com/user-attachments/assets/9fb99fea-fcad-44b5-bba7-62d016c1d2a2)

### DHCP paket alışverişinde şunları görebiliriz:
İstemci herhangi bir IP ağ yapılandırması olmadan başlar. Sadece bir MAC adresi vardır.Birinci ve üçüncü paketlerde, DHCP Discover ve DHCP Request'de, DHCP sunucusu arayan istemcinin henüz IP ağ yapılandırması yoktur ve DHCP sunucusunun sunduğu IP adresini henüz kullanmamıştır.
Bu nedenle 0.0.0.0 IP adresinden yayın IP adresi olan 255.255.255.255'e paketler gönderir.

### Bağlantı katmanına gelince, birinci ve üçüncü paketlerde istemci, yayın MAC adresine ff:ff:ff:ff:ff:ff (yukarıdaki çıktıda gösterilmemiştir) gönderir.DHCP sunucusu, DHCP teklifindeki ağ yapılandırmasıyla birlikte kullanılabilir bir IP adresi sunar. İstemcinin hedef MAC adresini kullanır. (Bu örnek sistemde önerilen IP adresini kullandı.)

DHCP sürecinin sonunda, cihazımız ağa veya hatta İnternete erişmek için gereken tüm yapılandırmayı almış olacaktır. Özellikle, DHCP sunucusunun bize aşağıdakileri sağladığını umuyoruz:
* Ağ kaynaklarına erişmek için kiralanan IP adresi
* Paketlerimizi yerel ağın dışına yönlendirmek için ağ geçidi
* Alan adlarını çözümlemek için bir DNS sunucusu






