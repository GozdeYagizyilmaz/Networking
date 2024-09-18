### TCP/IP modeli birçok bakımdan OSI modeline çok benzemektedir.Birkaç yıl daha eskidir ve gerçek dünyadaki ağ oluşturmanın temelini oluşturur. TCP/IP modeli dört katmandan oluşur:Uygulama, Taşıma, İnternet ve Ağ Arayüzü. Bunlar, OSI Modelinin yedi katmanıyla aynı işlev aralığını kapsar.

![image](https://github.com/user-attachments/assets/f3719c9b-ec20-4d2f-9f0c-284fc73c43cd)

### The two models match up something like this:

![image](https://github.com/user-attachments/assets/103da810-0bee-4026-98a2-7c4af5f48761)

**Kapsülleme ve kapsülden çıkarma işlemleri, OSI modelinde olduğu gibi TCP/IP modelinde de tamamen aynı şekilde çalışır.**

### Katmanlı bir model görsel bir yardım olarak harikadır; bize verilerin bir ağ üzerinden nasıl kapsüllenip gönderilebileceğine ilişkin genel süreci gösterir, ancak bu gerçekte nasıl gerçekleşir?

TCP bağlantı tabanlı bir protokoldür. Yani TCP üzerinden herhangi bir veri göndermeden önce iki bilgisayar arasında stabil bir bağlantı kurmanız gerekiyor. Bu bağlantıyı kurma sürecine üç yönlü el sıkışma denir.
Bağlantı kurmaya çalıştığınızda, bilgisayarınız öncelikle uzak sunucuya bağlantı başlatmak istediğini belirten özel bir istek gönderir.Bu istek, esasen bağlantı sürecini başlatırken ilk teması sağlayan SYN (senkronizasyonun kısaltması) biti adı verilen bir şey içerir.
Sunucu daha sonra SYN bitini ve ayrıca ACK adı verilen başka bir "onay" bitini içeren bir paketle yanıt verecektir.
Son olarak bilgisayarınız, bağlantının başarıyla kurulduğunu onaylayan, ACK bitini içeren bir paket gönderecektir.

Üç yönlü el sıkışmanın başarıyla tamamlanmasıyla veriler iki bilgisayar arasında güvenilir bir şekilde iletilebilir.İletim sırasında kaybolan veya bozulan veriler yeniden gönderilir, böylece kayıpsız görünen bir bağlantı sağlanır.

![image](https://github.com/user-attachments/assets/e84c9b57-58e4-4c49-b63f-e36f543d03f0)

### TCP/IP ve OSI modellerinin başlangıçta neden oluşturulduğunu tam olarak anlamak önemlidir.Başlangıçta hiçbir standardizasyon yoktu; farklı üreticiler kendi metodolojilerini takip ediyordu ve sonuç olarak farklı üreticiler tarafından üretilen sistemler, konu ağ oluşturma olduğunda tamamen uyumsuzdu.TCP/IP modeli, 1982 yılında Amerikan Savunma Bakanlığı tarafından, tüm farklı üreticilerin takip edeceği bir standart sağlamak amacıyla tanıtıldı.
### Bu tutarsızlık sorunlarını çözdü. Daha sonra OSI modeli Uluslararası Standardizasyon Örgütü (ISO) tarafından da tanıtıldı;ancak TCP/IP modeli hâlâ modern ağ oluşturmanın dayandığı standart olduğundan, çoğunlukla öğrenme için daha kapsamlı bir kılavuz olarak kullanılır.



