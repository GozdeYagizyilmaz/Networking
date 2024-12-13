### Favori web sitelerinizin IP adreslerini hatırlıyor musunuz? Yerel bir cihazın özel IP adresi olmadığı sürece, hiç kimse IP adreslerini ezberlemek konusunda endişelenmek zorunda değil.

DNS, ISO OSI modelinin Uygulama Katmanı, yani 7. Katmanında çalışır.DNS trafiği varsayılan olarak UDP portu 53'ü ve varsayılan geri dönüş olarak TCP portu 53'ü kullanır. Birçok DNS kaydı türü vardır.Bunlardan bazıları;

* **A Record:** A (Adres) kaydı bir ana bilgisayar adını bir veya daha fazla IPv4 adresine eşler. Örneğin, example.com'u 172.17.2.172 olarak çözümleyecek şekilde ayarlayabilirsiniz.
* **AAAA Record:** AAAA kaydı A Kaydına benzerdir, ancak IPv6 içindir. AAAA (quad-A) olduğunu unutmayın, çünkü AA ve AAA bir pil boyutunu ifade eder;ayrıca AAA, Kimlik Doğrulama, Yetkilendirme ve Muhasebe anlamına gelir; bunların hiçbiri DNS kapsamına girmez.
* **CNAME Record:** CNAME (Canonical Name) kaydı bir alan adını başka bir alan adına eşler. Örneğin, www.example.com example.com'a veya hatta example.org'a eşlenebilir.
* **MX Record:** MX (Posta Değişimi) kaydı, bir etki alanına ait e-postaları işlemekten sorumlu posta sunucusunu belirtir.

Bir etki alanının IP adresini komut satırından aramak istiyorsanız, nslookup gibi bir araç kullanabilirsiniz. Aşağıdaki terminalde example.com'u aradığımız örneği ele alalım.

![image](https://github.com/user-attachments/assets/040158af-7542-480e-b75c-efbaca7c9a31)

Yukarıdaki sorgu dört pakete yol açtı. Aşağıdaki terminalde, birinci ve üçüncü paketlerin sırasıyla A ve AAAA kayıtları için DNS sorguları gönderdiğini görebiliriz. İkinci ve dördüncü paketler DNS sorgu yanıtlarını gösterir.

![image](https://github.com/user-attachments/assets/05b2b122-1ce3-4f5c-82c8-a7fa29b7afae)


Kaynak : https://tryhackme.com/r/room/networkingcoreprotocols
