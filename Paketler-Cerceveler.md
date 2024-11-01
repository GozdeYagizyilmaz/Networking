### Paketler ve çerçeveler, bir araya geldiklerinde daha büyük bir bilgi veya mesaj parçası oluşturan küçük veri parçalarıdır. Ancak, OSI modelinde bunlar iki farklı şeydir. 

## 1- Çerçeveler(Frames)

### Bir çerçeve 2. katmandadır - veri bağlantı katmanı, yani IP adresleri gibi bir bilgi yoktur. Bunu bir zarfın içine bir zarf koyup göndermek olarak düşünün. İlk zarf, göndereceğiniz paket olacaktır, ancak açıldığında içindeki zarf hala var olur ve veri içerir (bu bir çerçevedir). Paketler,  ağ aygıtları arasında veri iletişiminin etkili bir yoludur. 

### Bu veriler küçük parçalar halinde değiştirildiği için, büyük mesajların aynı anda gönderilmesinden daha az ağ genelinde darboğaz oluşma olasılığı vardır. Örneğin, bir web sitesinden bir resim yüklerken, bu resim bilgisayarınıza bir bütün olarak gönderilmez, bunun yerine bilgisayarınızda yeniden yapılandırıldığı küçük parçalar gönderilir. 

## 2- Paketler (Packets)

### Paketler, gönderilen paketin türüne bağlı olarak farklı yapılara sahiptir.Ağ,paketin bir cihazda nasıl işleneceğine dair bir dizi kural görevi gören standartlar ve protokollerle doludur. İnternete bağlı milyarlarca cihazla, bir standardizasyon yoksa işler hızla bozulabilir. İnternet Protokolü örneğimize devam edelim. Bu protokolü kullanan bir paket, bir ağ üzerinden gönderilen verilere ek bilgi parçaları içeren bir dizi başlığa sahip olacaktır. Bazı önemli başlıklar şunlardır:

![image](https://github.com/user-attachments/assets/eed1eeee-eb0b-46e8-8c88-fb6e456b4c04)


