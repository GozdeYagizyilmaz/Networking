## IP adresleri, fiziksel olarak bir cihaza girilerek elle veya otomatik olarak ve en yaygın olarak bir DHCP (Dinamik Ana Bilgisayar Yapılandırma Protokolü) sunucusu kullanılarak atanabilir. Bir cihaz bir ağa bağlandığında, daha önce elle bir IP adresi atanmamışsa, ağda herhangi bir DHCP sunucusu olup olmadığını görmek için bir istek (DHCP Discover) gönderir. 
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


