# OSI Modeli
**OSI (Açık Sistemler Bağlantısı) Modeli, bilgisayar ağlarının ardındaki teoriyi göstermek için kullandığımız standartlaştırılmış bir modeldir.Pratikte bu, gerçek dünya ağlarının temel aldığı daha kompakt TCP/IP modelidir; ancak OSI modelinin ilk anlaşılması birçok açıdan daha kolaydır.**
**OSI modeli yedi katmandan oluşur:**

![image](https://github.com/user-attachments/assets/c3b65f11-4155-4990-a3b6-a09bbf268235)


**Şimdi sırasıyla bunların her birine kısaca göz atalım:**

### Katman 7 - Uygulama:

OSI modelinin uygulama katmanı esas olarak bilgisayarda çalışan programlara ağ oluşturma seçenekleri sağlar.Neredeyse yalnızca uygulamalarla çalışır ve onlara veri iletmek için kullanmaları için bir arayüz sağlar. Uygulama katmanına veri verildiğinde sunum katmanına aktarılır.

### Katman 6 - Sunum:

Sunum katmanı, uygulama katmanından veri alır.Bu veriler genellikle uygulamanın anlayacağı bir formatta olur ancak alıcı bilgisayardaki uygulama katmanının anlayabileceği standart bir formatta olması gerekmez.
Sunum katmanı, verileri standartlaştırılmış bir formata çevirir ve ayrıca verilere yönelik her türlü şifreleme, sıkıştırma veya diğer dönüştürme işlemlerini gerçekleştirir. Bu işlem tamamlandıktan sonra veriler oturum katmanına aktarılır.

### Katman 5 - Oturum:

Oturum katmanı, sunum katmanından doğru formatlanmış verileri aldığında, ağ üzerindeki diğer bilgisayarla bağlantı kurup kuramayacağına bakar.Eğer başaramazsa bir hata gönderir ve süreç daha ileri gitmez.
Bir oturum oluşturulabiliyorsa bu durumda oturumu sürdürmek ve iletişimi senkronize etmek için uzak bilgisayarın oturum katmanıyla işbirliği yapmak oturum katmanının görevidir.
Oturum katmanı, oluşturduğu oturumun söz konusu iletişime özgü olması nedeniyle özellikle önemlidir.Bu, tüm veriler karışmadan aynı anda farklı uç noktalara birden fazla istekte bulunmanıza olanak tanıyan şeydir (bir web tarayıcısında aynı anda iki sekme açmayı düşünün)!
Oturum katmanı, ana bilgisayar ile uzak bilgisayar arasındaki bağlantıyı başarıyla kaydettiğinde, veriler Katman 4'e, yani taşıma katmanına aktarılır.

### Katman 4 - Taşıma:

Taşıma katmanı çok sayıda önemli fonksiyona hizmet eden çok ilginç bir katmandır.İlk amacı verinin iletileceği protokolü seçmektir.Aktarım katmanındaki en yaygın iki protokol TCP (İletim Kontrol Protokolü) ve UDP'dir (Kullanıcı Datagram Protokolü);
TCP ile iletim bağlantı tabanlıdır; bu, bilgisayarlar arasında bir bağlantının istek süresince kurulduğu ve sürdürüldüğü anlamına gelir.Bağlantı, paketlerin hepsinin doğru yere gitmesini sağlamak için kullanılabildiğinden bu, güvenilir bir aktarıma olanak tanır.
TCP bağlantısı, verilerin kabul edilebilir bir hızda gönderilmesini ve kaybolan verilerin yeniden gönderilmesini sağlamak için iki bilgisayarın sürekli iletişim halinde kalmasına olanak tanır.
UDP'de bunun tersi doğrudur; veri paketleri esas olarak alıcı bilgisayara atılır; eğer bilgisayar buna ayak uyduramıyorsa, o zaman bu onun sorunudur.

Bunun anlamı, TCP'nin genellikle doğruluğun hıza tercih edildiği durumlarda (örn. dosya aktarımı veya bir web sayfasının yüklenmesi) seçileceğidir.ve UDP, hızın daha önemli olduğu durumlarda (örneğin video akışı) kullanılacaktır.

### Katman 3 - Ağ:

Ağ katmanı, isteğinizin hedefini bulmaktan sorumludur.Örneğin İnternet çok büyük bir ağdır; Bir web sayfasından bilgi istemek istediğinizde, sayfanın IP adresini alan ve izlenecek en iyi rotayı belirleyen ağ katmanıdır.
Bu aşamada Mantıksal adresleme (yani IP adresleri) olarak adlandırılan şeyle çalışıyoruz.Mantıksal adresler ağlara düzen sağlamak, onları kategorilere ayırmak ve doğru şekilde sıralamamızı sağlamak için kullanılır.
Şu anda mantıksal adreslemenin en yaygın biçimi, muhtemelen zaten aşina olacağınız IPV4 biçimidir (ör. 192.168.1.1, ev yönlendiricisi için ortak bir adrestir).

### Katman 2 - Veri Bağlantısı:

Veri bağlantı katmanı iletimin fiziksel adreslenmesine odaklanır.Ağ katmanından (uzaktaki bilgisayarın IP adresini içeren) bir paket alır ve alıcı uç noktanın fiziksel (MAC) adresini ekler.
Ağ özellikli her bilgisayarın içinde, onu tanımlamak için benzersiz bir MAC (Medya Erişim Kontrolü) adresiyle birlikte gelen bir Ağ Arayüzü Kartı (NIC) bulunur.

**MAC Adresi : Bilgi bir ağ üzerinden gönderildiğinde, aslında bilginin tam olarak nereye gönderileceğini belirlemek için kullanılan fiziksel adrestir.**

Ek olarak, veriyi iletime uygun bir formatta sunmak da veri bağlantı katmanının görevidir.

### Katman 1 - Fiziksel:

Fiziksel katman bilgisayarın donanımına kadar uzanır.Burası bir ağ üzerinden veri aktarımını oluşturan elektrik darbelerinin gönderildiği ve alındığı yerdir.
İletimdeki ikili verileri sinyallere dönüştürmek ve bunları ağ üzerinden iletmek, ayrıca gelen sinyalleri alıp bunları tekrar ikili verilere dönüştürmek fiziksel katmanın görevidir.


