### Ping komutu, uzak bir kaynağa bağlantının mümkün olup olmadığını test etmek istediğimizde kullanılır.Genellikle bu internetteki bir web sitesi olacaktır, ancak doğru yapılandırılıp yapılandırılmadığını kontrol etmek istiyorsanız ev ağınızdaki bir bilgisayar için de olabilir.
### Ping, daha önce bahsedilen, biraz daha az bilinen TCP/IP protokollerinden biri olan ICMP protokolünü kullanarak çalışır.ICMP protokolü, OSI Modelinin Ağ katmanında ve dolayısıyla TCP/IP modelinin İnternet katmanında çalışır.
### Ping'in temel sözdizimi ping <target> şeklindedir. Bu örnekte, Google'a ağ bağlantısının mümkün olup olmadığını test etmek için ping kullanıyoruz:

![image](https://github.com/user-attachments/assets/c70e07eb-0e28-48eb-8fbf-23e791098c1e)

Ping komutunun aslında istenen URL yerine, bağlandığı Google sunucusunun IP adresini döndürdüğüne dikkat edin.Ping'in en büyük avantajlarından biri, ağ özellikli herhangi bir cihazda hemen hemen her yerde bulunmasıdır. Tüm işletim sistemleri onu kutudan çıktığı haliyle destekler ve hatta çoğu gömülü cihaz bile ping'i kullanabilir!

![image](https://github.com/user-attachments/assets/89cbfcdd-3ee5-4adb-aef9-d1ea0ab5d34f)


## Traceroute

**Ping komutunun mantıksal devamı 'traceroute'tur. Traceroute, isteğinizin hedef makineye giderken izlediği yolu haritalamak için kullanılabilir.İnternet, hepsi birbirine bağlı çok sayıda farklı sunucu ve uç noktadan oluşur.Bu, gerçekten istediğiniz içeriğe ulaşmak için öncelikle bir dizi başka sunucudan geçmeniz gerektiği anlamına gelir.**
**Traceroute bu bağlantıların her birini görmenizi sağlar; bilgisayarınız ile istediğiniz kaynak arasındaki her ara adımı görmenizi sağlar.**
**Linux'ta traceroute'un temel sözdizimi şudur: traceroute <destination>**
**Varsayılan olarak Windows traceroute yardımcı programı (tracert), ping'in kullandığı ICMP protokolünün aynısını kullanarak çalışır ve Unix eşdeğeri UDP üzerinden çalışır. Bu, her iki durumda da anahtarlarla değiştirilebilir.**

![image](https://github.com/user-attachments/assets/1f5bb7ac-e571-4839-9545-f4ff17e3c5ca)


Yönlendiricimden (_gateway) 216.58.205.46 adresindeki Google sunucusuna ulaşmanın 13 atlama sürdüğünü görebilirsiniz.


