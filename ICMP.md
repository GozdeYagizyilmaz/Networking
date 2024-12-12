## ICMP: Ağlarda Sorun Giderme

İnternet Kontrol İleti Protokolü (ICMP) esas olarak ağ tanılama ve hata raporlama için kullanılır. İki popüler komut ICMP'ye dayanır ve ağ sorun giderme ve ağ güvenliğinde etkilidirler. Komutlar şunlardır:

* **ping:** Bu komut, hedef sisteme bağlantıyı test etmek için ICMP kullanır ve gidiş-dönüş süresini (RTT) ölçer. Başka bir deyişle, hedefin hayatta olduğunu ve cevabının sistemimize ulaşabileceğini öğrenmek için kullanılabilir
* **traceroute:** Bu komut Linux ve UNIX benzeri sistemlerde traceroute, MS Windows sistemlerinde ise tracert olarak adlandırılır. Ana bilgisayarınızdan hedefe giden yolu keşfetmek için ICMP kullanır.

## Ping
Ping komutu bir ICMP Echo Request (ICMP Type 8) gönderir. Aşağıdaki ekran görüntüsü bir IP paketi içindeki ICMP mesajını gösterir.

![image](https://github.com/user-attachments/assets/883d34b6-0ecc-424a-b15e-14440e5575a4)


![image](https://github.com/user-attachments/assets/8ac67252-ac76-4f83-9734-6c3bfc116155)

**Alıcı taraftaki bilgisayar bir ICMP Yankı Yanıtı (ICMP Tip 0) ile yanıt verir.**

![image](https://github.com/user-attachments/assets/4337f696-7943-4433-a686-50df77a76503)

Birçok şey yanıt almamızı engelleyebilir. Hedef sistemin çevrimdışı veya kapalı olma olasılığına ek olarak, yol boyunca bir güvenlik duvarı ping'in çalışması için gerekli paketleri engelleyebilir.Aşağıdaki örnekte, ping komutunun dört paket gönderdikten sonra durmasını sağlamak için -c 4'ü kullandık.

![image](https://github.com/user-attachments/assets/89f63e9c-d29d-4edc-8079-1cce3809d98b)

Çıktıda herhangi bir paket kaybı görülmüyor; ayrıca gidiş-dönüş süresinin (RTT) minimum, ortalama, maksimum ve standart sapması (mdev) hesaplanıyor.

## Traceroute
Sistemimiz ile hedef sistem arasındaki her yönlendiricinin kendisini göstermesini nasıl sağlayabiliriz?
İnternet protokolünde, bir paketin düşürülmeden önce geçebileceği maksimum yönlendirici sayısını belirten Yaşam Süresi (TTL) adlı bir alan vardır. Yönlendirici, paketi göndermeden önce paketin TTL'sini bir azaltır.

TTL sıfıra ulaştığında, yönlendirici paketi bırakır ve bir ICMP Zaman Aşımı mesajı gönderir (ICMP Tip 11). (Bu bağlamda, "zaman" saniyelerle değil, yönlendirici sayısıyla ölçülür.)
Aşağıdaki terminal çıktısı, sistemimiz ile example.com arasındaki yönlendiricileri keşfetmek için tracert komutunu çalıştırmanın sonucunu gösterir.
Bazı yönlendiriciler yanıt vermez; başka bir deyişle, herhangi bir ICMP mesajı göndermeden paketi düşürürler. İSS'mize ait yönlendiriciler yanıt verebilir ve özel IP adreslerini açığa çıkarabilir.Komutu tekrar çalıştırdığımızda geçilen rota değişebilir.

![image](https://github.com/user-attachments/assets/fa96c1df-b01c-4b7f-b8b7-1b8a4eafd355)

