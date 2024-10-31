### Büyük ölçekte bir ağın yönetimi kolay değildir. Ağlar boyut ve karmaşıklık açısından büyümeye devam ettikçe, ağ mühendisleri içlerinden akan önemli miktardaki trafiği yönetmek için en uygun rotaları belirleme zorluğuyla karşı karşıya kalmaktadır. Alt ağ oluşturma geliştirilen çözümlerden biridir, ancak soru şudur: alt ağ nedir? 
### Alt ağ(Subnet), ağ trafiğinin daha verimli bir şekilde seyahat etmesini sağlayan bir IP ağının mantıksal bir alt bölümüdür. Bu blogda, bilgisayar ağlarında alt ağ oluşturmanın ne olduğuna, nasıl çalıştığına, bununla ilişkili faydalara ve zorluklara odaklanacağız. Daha fazla ayrıntıya girmeden önce, öncelikle alt ağın gerçekte ne olduğunu anlayalım. 

## Alt Ağ Nedir? - SUBNET

Alt ağ , daha büyük bir ağ içindeki daha küçük bir ağdır. Özellikle alt ağlar, bir IP ağı çok sayıda ağa bölündüğünde oluşturulan daha küçük ağlardır. Bir ağda alt ağ oluşturmanın hedefleri, onu daha hızlı, daha verimli ve daha güvenli hale getirmektir.

![image](https://github.com/user-attachments/assets/016f0ba3-448f-4fe8-93a3-e0f2996dcb66)

Aşırı miktarda trafik ağınız üzerinden aynı yolu kullanırsa tıkanıklık, gecikmeler ve darboğazlar ortaya çıkar ve bu da verimsiz beklemelere yol açar. Ağlar genişledikçe, daha fazla yönlendiriciye duyulan ihtiyaç karşılanmalıdır; alt ağlar burada devreye girer. Ağ trafiği, daha az doğrudan ancak daha zaman açısından verimli yollardan kaçınarak mümkün olan en hızlı yolu seçecektir. Alt ağlar her zaman VLAN'larla karıştırılır. 
Şimdi alt ağları ayrıntılı olarak anlayalım. 

## Bilgisayar Ağlarında Alt Ağ Oluşturma Nedir? 

Alt ağ oluşturma, bir ağı birden fazla küçük ağa bölme işlemidir. Bu küçük ağ, alt ağ olarak bilinir. Bu çözümün uygulanması, iyileştirilmiş yönlendirme verimliliği, gelişmiş ağ güvenliği ve azaltılmış yayın alanı boyutuyla sonuçlanır. Alt ağ oluşturmayı bir örnek yardımıyla anlayalım.

![image](https://github.com/user-attachments/assets/fef5aa6c-f829-49c5-8369-6bfe3dae3b2c)

Resimde gördüğümüz gibi 10.1.0.0/8'li bir ağ var. Ağdaki tüm ana bilgisayarlar aynı alt ağa ait olduğunda aşağıdaki sorunlar ortaya çıkıyor:

* **Görüldüğü gibi tüm sunucular aynı yayın alanında yer alıyor ve bu da gereksiz trafiğe yol açacaktır.**
* **Bu, organizasyon içinde güvenlik sorunlarına da yol açabilir, çünkü diyelim ki satış ekibinin tüm gizli verileri operasyon ekibiyle paylaşılacak ve tam tersi de geçerli olacak. Bu nedenle, farklı departmanlar için ayrı alt ağlara sahip olmak çok önemlidir.**

![image](https://github.com/user-attachments/assets/05b9c0ff-3ef0-4b58-81ca-f82ad337aaf8)

Şimdi farklı departmanlar için iki farklı alt ağın oluşturulduğunu görebiliriz, biri Satış için, yani 10.1.0.0/8 ve biri Operasyon için, yani 10.2.0.0/8.

Her alt ağdaki cihazlar için yeni bir yayın alanı oluşturuldu. Sonuç olarak, yönlendiricide paket filtrelemeyi uygulayabilecek ve ağ trafiğini büyük ölçüde azaltabileceğiz.

## Alt Ağ Oluşturma Nasıl Çalışır? 
Bildiğimiz gibi, alt ağ oluşturma, daha iyi çalışması için tek bir ağı birden fazla küçük ağa böler. Yönlendiriciler ağlar arasında veri aktarımına izin verirken, her alt ağ cihazların kendi aralarında veri alışverişinde bulunmasını sağlar. 
Alt ağ boyutları, kullanılan ağ teknolojisine ve gereken bağlantı sayısına göre ayarlanır. Her şirket, kendisine tahsis edilen IPv4 adres alanının sınırlarına kadar uygun gördüğü kadar çok ve büyük alt ağ oluşturmakta özgürdür. 
Alt ağ oluşturma sürecini bir örnek yardımıyla ayrıntılı olarak anlayalım. 

Bir IP adresi iki bölümden oluşur, yani ağ öneki (ağ kimliği olarak da bilinir) ve Ana Bilgisayar Kimliği. 

![image](https://github.com/user-attachments/assets/62913493-b4ef-4487-8981-5426759e5506)

Bir alt ağı belirlemek için bir alt ağ maskesi kullanmak gerekir. Bu maske, tüm Ağ Kimliği bitlerini '1' ile değiştirerek ve alt ağı oluşturma amacıyla Ana Bilgisayar Kimliğinde belirli sayıda bit tahsis ederek hesaplanır. 
Alt ağ maskesinin amacı, veri paketlerinin internetten amaçlanan alt ağ ağlarına yönlendirilmesine yardımcı olmaktır. 
Alt ağ maskesi, bir adresin Alt Ağ Kimliği olarak kullanılmak üzere belirlenmiş belirli bölümünü belirtme amacına hizmet eder.

![image](https://github.com/user-attachments/assets/2c5b65f1-4592-41c5-9832-d94e6184cbcb)

Alt ağ maskesi için aşağıdaki görseldeki formu gösterdik.

![image](https://github.com/user-attachments/assets/4321f365-ef28-4aea-a911-1c2a7695c673)

Bir alt ağın yayın adresi, alt ağı temsil etmek için belirli bitleri ayırdıktan sonra Host ID'nin kalan tüm bitlerini '1' olarak ayarlayarak belirlenir. Yayın adresi, belirli bir ağdaki tüm hostlara bir mesaj yayınlamak için kullanılır. Aşağıda yayın adresini bir resimle gösterdik.

![image](https://github.com/user-attachments/assets/e0b8197d-e111-4760-ae83-413493f880db)

## Alt ağ oluşturma neden gereklidir? 
Alt ağ oluşturma, ağ kimliklerinin aşırı kullanımını yönetmeye yardımcı olduğu için önemlidir. Şirketin ağ kanalı üzerinden sorunsuz ve hatasız veri paylaşımı için ağ kanalını verimli bir şekilde geliştirmesini sağlar. Bunu açıkça anlamak için, alt ağ oluşturmanın neden gerekli olduğuna dair bazı nedenler şunlardır: 

* **IP adreslerinin ağ gereksinimine göre daha küçük alt birimlere verimli bir şekilde dağıtılmasını sağlar.**
* **Ağ kanalında güvenlik varlıklarını hızla oluşturarak veri ihlallerinin önlenmesine yardımcı olur.**
* **Alt ağ oluşturma, IP adreslerinin boşa harcanmasını önler.**
* **Ağ kanalındaki her alt ağ arasında sorunsuz iletişim sağlar.**

## Alt Ağ Oluşturmanın Kullanımları 
Alt Ağ Oluşturmanın bazı kullanımları şunlardır: 

* Alt Ağ Oluşturma, trafiği azaltmaya ve düzen ve verimliliği korumaya yardımcı olan belirli bir personel yapısı tasarlar.
* Ağın verimli bir şekilde yönetilmesine yardımcı olur ve şirketlerin ve daha büyük firmaların teknolojiyi genişletmesine olanak tanır.
* Trafiğin verimli bir şekilde yönlendirilmesini sağlar ve yayın alanlarını bölerek ağ performansını iyileştirir.
* Ağ güvenliğini artırmak için kullanılır.

## Alt Ağ Maskesi Nedir? 
Bir alt ağ maskesi ve bir IP adresi benzer görünse de, yine de büyük bir fark vardır. 

Alt ağ maskelerinin yaygın örnekleri arasında 255.255.255.0, 255.255.0.0 ve 255.0.0.0 bulunur. 
Adres, bir IP adresi içinde bir ağ adresi ile bir bilgisayar ana bilgisayar adresi arasında ayrım yapmak için kullanılan 32 bitlik bir değerdir. 
TCP/IP'nin düzgün çalışması için bir alt ağ maskesinin kullanılması gerekir. Bu aracın işlevi, bir bilgisayarın veya başka bir cihazın, özellikle uzak bir ağa mı yoksa yerel bir alt ağa mı bağlı olduğunu belirlemektir.

## Alt Ağ Oluşturmanın Avantajları 
Alt ağ oluşturma çeşitli avantajlar sunar, bunlardan bazıları şunlardır: 

**Ağ performansını iyileştirin**
Bir cihaz bir paket ilettiğinde, bu paket tüm ağ cihazları tarafından alınır ve böylece ağ üzerinde bir yük oluşur. 
Uygun bağlamın yokluğunda, yayın paketleri ağ içindeki cihazları boğma potansiyeline sahiptir ve bu da spam benzeri bir davranışa neden olur. 
Bu, ağ performansında düşüşe neden olabilir. Alt ağlar, ağ içi yayın mesajlarının aralığını yalnızca belirlenmiş bir alt ağla sınırlamak için kullanılabilir. 
Bu işlevsellik, bir alt ağ içindeki cihazlar arasında etkili iletişim sağlar ve bir hedef adresin alt ağ içinde olmaması durumunda, alt ağın dışına yönlendirme için bir paket iletir. 
Bu yaklaşım, ağ tıkanıklığını ve ağ sorunlarını en aza indirmeye yardımcı olur.

**Ağ güvenliğini artırın** 
Alt ağların yardımıyla, tehlikeye atılan alt ağı izole edebileceğiniz için ağ ihlallerini sınırlamak mümkündür. 
Bu nedenle, hassas verileri koruyarak genel güvenliği artırmaya yardımcı olur. 

**Ağ ölçeklenebilirliğini artırma** 
Değişken uzunluklara sahip alt ağlar kullanarak, her segmente ihtiyaçlarına bağlı olarak daha fazla veya daha az adres tahsis edebiliriz, böylece adresleri boşa harcamadan veya tükenmeden yeni cihazlara veya ağlara yer açabiliriz. 
Tartıştığımız tüm avantajların yanı sıra, Alt Ağ Oluşturma'nın bazı dezavantajları da vardır, bunları ayrıntılı olarak tartışalım.

## Alt Ağ Oluşturmanın Dezavantajları 
Farklı alt ağlar arasında iletişimin gerçekleşmesi için bir yönlendiricinin kullanılması gerekir. 

* Ek alt ağların kullanılması, her alt ağ için benzersiz ağ ve yayın adreslerinin tahsis edilmesi nedeniyle daha fazla IP adresi tüketimine neden olur.
* Alt ağ oluşturma süreci, ağ altyapısına artan karmaşıklık getirir.
* Alt ağlı ağın yönetimini denetlemek için yetenekli bir ağ yöneticisine ihtiyaç vardır.

  [Kaynak](https://www.pynetlabs.com/what-is-a-subnet-and-how-subnetting-works/)

  ![image](https://github.com/user-attachments/assets/615b0970-7785-46bf-9e2d-89c12857e6e0)

                    
