### Cihazların iki tanımlayıcısı olabilir: Bir MAC adresi ve bir IP adresi, Adres Çözümleme Protokolü veya kısaca ARP, cihazların kendilerini bir ağda tanımlamalarına izin veren teknolojidir. Basitçe, ARP protokolü bir cihazın MAC adresini ağdaki bir IP adresiyle ilişkilendirmesine izin verir. Bir ağdaki her cihaz, diğer cihazlarla ilişkili MAC adreslerinin bir kaydını tutar. Cihazlar başkalarıyla iletişim kurmak istediklerinde, belirli cihazı aramak için tüm ağa bir yayın gönderirler. Cihazlar, iletişim için bir cihazın MAC adresini (ve dolayısıyla fiziksel tanımlayıcısını) bulmak için ARP protokolünü kullanabilir.

## ARP Nasıl Çalışır? 
**Bir ağdaki her cihazın, önbellek adı verilen bilgileri depolamak için bir defteri vardır. ARP protokolü bağlamında, bu önbellek ağdaki diğer cihazların tanımlayıcılarını depolar.** 
**Bu iki tanımlayıcıyı (IP adresi ve MAC adresi) birlikte eşlemek için, ARP protokolü iki tür mesaj gönderir:** 

*ARP İsteği ve ARP Cevabı* 

**Bir ARP isteği gönderildiğinde, ağda diğer cihazlara "Bu IP adresine sahip olan mac adresi nedir?" diye soran bir mesaj yayınlanır. 
Diğer cihazlar bu mesajı aldığında, yalnızca bu IP adresine sahiplerse yanıt verirler ve MAC adresiyle bir ARP cevabı gönderirler. 
İstekte bulunan cihaz artık bu eşlemeyi hatırlayabilir ve gelecekte kullanmak üzere ARP önbelleğinde saklayabilir. 
Bu işlem aşağıdaki diyagramda gösterilmiştir:**

![image](https://github.com/user-attachments/assets/0c9d4cea-c1f1-48a1-9b63-e97a9a3846de)

## ARP Türleri Nelerdir? 
ARP'nin farklı versiyonları ve kullanım örnekleri vardır. Birkaçına bir göz atalım:

**Proxy ARP** 

Proxy ARP, belirli bir ağdaki bir proxy aygıtının, o ağda olmayan bir IP adresi için ARP isteğine yanıt verdiği bir tekniktir. 
Proxy, trafiğin hedefinin yerini bilir ve hedef olarak kendi MAC adresini sunar.

**Ücretsiz ARP** 

Ücretsiz ARP, bir ağdaki ana bilgisayarın IP-MAC adresini duyurması veya güncellemesi için bir yol olarak gerçekleştirilen bir idari prosedüre neredeyse benzer. 
Ücretsiz ARP, bir IP adresini bir MAC adresine çevirmek için bir ARP isteği tarafından istenmez. 

**Ters ARP (RARP)** 

Kendi IP adreslerini bilmeyen ana bilgisayar makineleri keşif için Ters Adres Çözümleme Protokolünü (RARP) kullanabilir. 
Ters ARP (IARP) ARP bir MAC adresini bulmak için bir IP adresi kullanırken, IARP bir IP adresini bulmak için bir MAC adresi kullanır.

[Kaynak](https://www.fortinet.com/resources/cyberglossary/what-is-arp)
