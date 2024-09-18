### Veriler modelin her katmanından aşağı aktarıldıkça, söz konusu katmana özgü ayrıntıları içeren daha fazla bilgi aktarımın başlangıcına eklenir.Örnek olarak, Ağ Katmanı tarafından eklenen başlık, kaynak ve hedef IP adresleri gibi şeyleri içerecektir ve Aktarım Katmanı tarafından eklenen başlık, (diğer şeylerin yanı sıra) kullanılan protokole özel bilgileri içerecektir.
### Veri bağlantısı katmanı ayrıca iletimin sonuna, verilerin iletim sırasında bozulmadığını doğrulamak için kullanılan bir parça ekler;bu aynı zamanda artan güvenlik avantajına da sahiptir, çünkü veriler fragmanı bozmadan ele geçirilemez ve değiştirilemez.Tüm bu sürece kapsülleme adı verilir; Verilerin bir bilgisayardan diğerine gönderilebildiği süreç.

![image](https://github.com/user-attachments/assets/8f198e1e-1ac8-494d-a6b7-c3e7b723b147)

**Kapsüllenmiş verilere sürecin farklı adımlarında farklı bir ad verildiğine dikkat edin. 7., 6. ve 5. katmanlarda veriler basitçe veri olarak anılır.Aktarım katmanında kapsüllenmiş verilere bir segment veya bir veri birimi denir (iletim protokolü olarak TCP veya UDP'nin seçilmesine bağlı olarak).**
**Ağ Katmanında verilere paket adı verilir.Paket Veri Bağlantısı katmanına iletildiğinde bir çerçeve haline gelir ve bir ağ üzerinden iletildiğinde çerçeve bitlere bölünmüş olur.**

**Mesaj ikinci bilgisayar tarafından alındığında, fiziksel katmandan başlayıp uygulama katmanına ulaşana kadar süreci tersine çevirir ve ilerledikçe eklenen bilgileri çıkarır.Buna kapsülden çıkarma denir. Bu nedenle OSI modelinin katmanlarının, ağ yeteneklerine sahip her bilgisayarın içinde mevcut olduğunu düşünebilirsiniz.**
**Pratikte bu kadar kesin olmasa da, bilgisayarların tümü veri göndermek için aynı kapsülleme sürecini izler ve veriyi aldıktan sonra kapsülden çıkarma işlemini gerçekleştirir.**

