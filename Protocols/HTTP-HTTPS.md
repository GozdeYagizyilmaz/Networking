### Tarayıcınızı açtığınızda çoğunlukla HTTP ve HTTPS protokollerini kullanırsınız.HTTP, Hypertext Transfer Protocol'ü temsil eder; HTTPS'deki S, Secure'i temsil eder. Bu protokol TCP'ye dayanır ve web tarayıcınızın web sunucularıyla nasıl iletişim kurduğunu tanımlar.

Web tarayıcınızın web sunucusuna sıklıkla gönderdiği komut veya yöntemlerden bazıları şunlardır:

* **GET,** bir HTML dosyası veya resim gibi bir sunucudan veri alır.
* **POST,** bir form göndermek veya bir dosya yüklemek gibi sunucuya yeni veriler göndermemize olanak tanır.
* **PUT,** sunucuda yeni bir kaynak oluşturmak ve var olan bilgileri güncellemek ve üzerine yazmak için kullanılır.
* **DELETE,** adından da anlaşılacağı gibi sunucudaki belirli bir dosyayı veya kaynağı silmek için kullanılır.

### HTTP ve HTTPS genellikle sırasıyla 80 ve 443 numaralı TCP portlarını ve daha az sıklıkla 8080 ve 8443 gibi diğer portları kullanır.

Aşağıdaki örnekte, Firefox tarayıcımızı MACHINE_IP üzerindeki web sunucusuna erişmek için kullanıyoruz. Tarayıcımız web sayfasını alır ve mükemmel bir şekilde görüntüler; ancak, biz sahne arkasında neler olup bittiğiyle ilgileniyoruz.

![image](https://github.com/user-attachments/assets/df5b9958-8483-4d48-8a52-b0966a7a9c04)

Wireshark'ı kullanarak Firefox tarayıcısı ile web sunucusu arasındaki alışverişi daha yakından inceleyebiliriz. Aşağıdaki Wireshark ekran görüntüsü, tarayıcımızın gönderdiği metni kırmızı, web sunucusunun yanıtını ise mavi olarak göstermektedir.
Gördüğünüz gibi, istemci ile sunucu arasında kullanıcıya sunulmayan çok fazla bilgi alışverişi yapılıyor. Örnekler arasında web sunucusu sürümü ve sayfanın en son ne zaman değiştirildiği yer alıyor.

![image](https://github.com/user-attachments/assets/ebcd7aa8-0f5d-456c-9e14-8e1bf3aa6eb9)
