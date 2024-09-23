# Ağ Topolojisi

Ağ topolojisi, bir bilgisayar ağının fiziksel veya mantıksal yapısını anlamaya yönelik görsel bir haritadır. Ağdaki cihazların ve kabloların konumları ağ topolojisini belirleyen faktörler arasındadır.
Bir ağ topolojisine sahip olmanın birçok faydası vardır. Örneğin ağdaki bir cihazın görevini yerine getirememesi durumunda ağdaki diğer hangi cihaz(lar)ın etkileneceğini görmek mümkündür.Büyük bir ağın ağ topolojisine bakıyorsak, ağdaki alt ağları ve bağlı olduğu cihazları görmek mümkündür. Ağ topolojisi 2 türe ayrılır:

**1- Fiziksel Topoloji**

Ağdaki tüm cihaz ve bileşenlerin tam konumlarına göre çizildiği bir topoloji türüdür. Bu topolojiye bakıldığında hangi kablolamanın hangi yol ve cihazlar üzerinden yapıldığı görülmektedir.Çizimde görülenin fiziksel bir karşılığı vardır. Örneğin A cihazından B cihazına giden yolda bir ağ cihazı varsa bu cihaz fiziksel topolojide görülür.

**2-Mantıksal Topoloji**

Fiziksel topoloji gibi topolojide cihazların tam yerini göstermez. Genellikle fiziksel topolojiden daha az öğe içerir. Çünkü mantıksal topolojide veri akışı önemlidir.Örneğin, A cihazından B cihazına giden veriler, A cihazı ile B cihazı arasında C cihazı üzerinden geçiyorsa topolojiye dahil edilmeyebilir ve C cihazının, üzerinde görüntülenmesi gereken veriler üzerinde hiçbir etkisi yoktur. 

### Aşağıda diğer topoloji çeşitlerinden bahsedelim :

## Ring(Halka) Topology

Kapalı döngü mantığıyla çalışır. Gönderilen veri, hedefe ulaşana kadar halkanın etrafında tek yönde hareket eder.Her düğüm, gelen veriyi üzerinden geçirerek hedefe ulaşmasını sağlar. Düğümler arasında hiyerarşik bir ilişki yoktur.

![image](https://github.com/user-attachments/assets/5a2ee1c8-3a83-46fc-98c3-6ddedce211ef)

## Star(Yıldız) Topology

Yıldız topolojisindeki her düğüm merkezi bir düğüme bağlanır. Tüm veri akışı merkezi düğüm üzerinden yapılır. Yıldız topolojisi en yaygın bilgisayar ağı topolojilerinden biridir.

![image](https://github.com/user-attachments/assets/e56dede6-11dc-49bb-bf57-8193decf9bb4)

## Mesh(Örgü) Topology

Merkezi bir düğümün bulunmadığı ve her düğümün diğerine doğrudan bağlanabildiği bir ağ topolojisidir. Mesh topolojisi büyük ağlar için uygun bir topoloji değildir. 2 türe ayrılmıştır:

**1-Full Mesh**

![image](https://github.com/user-attachments/assets/a617cbde-05da-4881-a036-b42ac091062f)


Full-Mesh topolojisinde ağdaki her düğüm diğer tüm düğümlere ayrı ayrı kablolanarak bağlanır. Bu topolojide iki düğüm arasındaki bağlantının kopması pek olası değildir. Çünkü alternatif bağlantı yolları var.

**2-Partial Mesh**

![image](https://github.com/user-attachments/assets/2eadb0d2-99f5-49f8-8da3-99e0eab57967)


Kısmi Örgü topolojisinde her düğüm diğer tüm düğümlere doğrudan bağlı olmasa da büyük ölçüde birbirine bağlıdır. Tıpkı Full-Mesh topolojisinde olduğu gibi bağlantının kesilmesi durumunda hedef düğüme ulaşmanın alternatif yolları vardır.

## Bus(Veri Yolu) Topology

Bus topolojisi, düğümlerin ortak bir yol üzerinde yer aldığı ve bu yol üzerinde çift yönlü bağlantı ile veri iletiminin yapıldığı bir topolojidir.Bus topolojisinde her düğüm kendisine ait olmasa bile iletilen her veriyi alır. Düğümler arasında hiyerarşik bir düzen bulunmadığından iletim önceliği yoktur.

![image](https://github.com/user-attachments/assets/eec3102c-8be5-4a9a-9425-f2a3d5dd30fe)

## Point-to-Point(Noktadan Noktaya) Topology

Noktadan noktaya topoloji en basit topolojidir ve birbirine bağlı iki düğümden oluşur. Örneğin, iki telefon arasında geçen bir çağrı, noktadan noktaya bir topoloji oluşturur,veya iki bilgisayar arasındaki doğrudan bağlantı, noktadan noktaya topoloji oluşturur.

![image](https://github.com/user-attachments/assets/5a9af5aa-7e80-42a8-bdc9-78ebdd5b23bb)

## Tree(Ağaç) Topology

Ağaç topolojisi, yıldız ve veri yolu topolojisinin bağlanmasıyla oluşturulan hibrit bir ağ topolojisidir. Ağaç topolojisinin hiyerarşik bir düzeni vardır ve her düğüm herhangi bir sayıda alt düğüme sahip olabilir.

![image](https://github.com/user-attachments/assets/cff2a1e1-a74b-45ec-a5d7-6a7809ac1f24)


