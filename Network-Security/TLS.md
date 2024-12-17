### SSL gibi, selefi olan TLS de OSI modelinin taşıma katmanında çalışan bir kriptografik protokoldür. Güvenli olmayan bir ağ üzerinden bir istemci ve bir sunucu arasında güvenli iletişime izin verir.
### Güvenli derken gizlilik ve bütünlüğü kastediyoruz; TLS ise hiç kimsenin değiştirilen veya okunan verileri okuyamamasını veya değiştirememesini sağlar.

![image](https://github.com/user-attachments/assets/9bd7858e-73c1-4cbe-935c-467464cf7f34)


## Tarihçe

### 1990'ların başında Netscape Communications, World Wide Web'de güvenli iletişime olan ihtiyacı fark etti.Sonunda SSL'i (Güvenli Yuva Katmanı) geliştirdiler ve 1995'te ilk genel sürüm olarak SSL 2.0'ı yayınladılar. 1999'da, İnternet Mühendislik Görev Gücü (IETF) TLS'yi (Taşıma Katmanı Güvenliği) geliştirdi.Çok benzer olmasına rağmen, TLS 1.0, SSL 3.0'ın bir yükseltmesiydi ve çeşitli iyileştirilmiş güvenlik önlemleri sunuyordu. 2018'de TLS, protokolünde önemli bir revizyona gitti ve TLS 1.3 yayınlandı.

###Amaç tam tarihleri ​​hatırlamak değil, TLS'nin güncel sürümü olan TLS 1.3'ün geliştirilmesinde ne kadar emek ve zaman harcandığını fark etmektir.Yirmi yılı aşkın süredir her versiyonda öğrenilecek ve geliştirilecek çok şey oldu.

Günümüzde onlarca protokol, TLS'nin eklenmesiyle güvenlik yükseltmeleri aldı.Örnek olarak HTTP, DNS, MQTT ve SIP, daha sonra HTTPS, DoT (DNS over TLS), MQTTS ve SIPS olmuştur; SSL/TLS kullanımından dolayı eklenen “S” Güvenli anlamına gelir.

## Teknik Arka Plan
Kendini tanımlaması gereken her sunucunun (veya istemcinin) ilk adımı imzalı bir TLS sertifikası almaktır.Genellikle, sunucu yöneticisi bir Sertifika İmzalama İsteği (CSR) oluşturur ve bunu bir Sertifika Yetkilisine (CA) iletir; CA, CSR'yi doğrular ve bir dijital sertifika verir.
(İmzalanmış) sertifika alındığında, sunucunun (veya istemcinin) başkalarına tanıtılması ve imzanın geçerliliğinin doğrulanması için kullanılabilir.

Bir ana bilgisayarın imzalanmış bir sertifikanın geçerliliğini doğrulaması için, imzalayan yetkililerin sertifikalarının ana bilgisayara yüklenmesi gerekir. Dijital olmayan dünyada, bu çeşitli yetkililerin damgalarını tanımaya benzer.Aşağıdaki ekran görüntüsü web tarayıcısına yüklenen güvenilir otoriteleri göstermektedir.

![image](https://github.com/user-attachments/assets/0480b946-8569-4b0c-80a1-22aee5612eca)

Son olarak, bazı kullanıcıların kendi kendine imzalanmış bir sertifika oluşturmayı tercih ettiğini belirtmeliyiz. Kendi kendine imzalanmış bir sertifika, hiçbir üçüncü taraf tarafından doğrulanmadığı için sunucunun gerçekliğini kanıtlayamaz.
