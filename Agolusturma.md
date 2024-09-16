### Ağlar basitçe birbirine bağlı şeylerdir. Örneğin, arkadaşlık çevreniz: hepiniz benzer ilgi alanları, hobiler, beceriler ve türler nedeniyle birbirine bağlısınız. Ağlar hayatın her alanında bulunabilir:

* **Bir şehrin toplu taşıma sistemi**
* **Elektrik için ulusal elektrik şebekesi gibi altyapı**
* **Komşularınızla tanışmak ve selamlaşmak**
* **Mektup ve paket göndermek için posta sistemleri**

### Bilgi işlemde, 2 cihazdan milyarlarca cihaza kadar herhangi bir yerde bir ağ oluşturulabilir. Bu cihazlar, dizüstü bilgisayarınızdan ve telefonunuzdan güvenlik kameralarına, trafik ışıklarına ve hatta çiftçiliğe kadar her şeyi içerir!
Ağlar günlük yaşamımıza entegre edilmiştir.İster hava durumuyla ilgili veri toplayın, ister evlere elektrik dağıtın, hatta yolda kimin geçiş hakkına sahip olduğunu belirleyin.
Ağlar günümüzün içine o kadar gömülü ki, ağ oluşturma siber güvenlikte anlaşılması gereken önemli bir kavramdır.

## İnternet

İnternet, kendi içinde çok sayıda küçük ağdan oluşan dev bir ağdır. Örnek olarak:

**Alice'in Bob ve Jim'le tanıştırmak istediği Zayn ve Toby adında yeni arkadaşlar edindiğini hayal edelim.Alice her iki dili de konuşabildiği için Alice aracılığıyla birbirleriyle iletişim kurarak yeni bir ağ oluşturabilirler.**

![image](https://github.com/user-attachments/assets/a6a06f3e-d7a0-4bab-846c-9983da5b926a)

### İnternetin ilk versiyonu 1960'ların sonunda ARPANET projesi kapsamında gerçekleşti. Bu proje Amerika Birleşik Devletleri Savunma Bakanlığı tarafından finanse edildi ve belgelenen ilk ağ oldu.

### Ancak, bildiğimiz haliyle İnternet'in Tim Berners-Lee tarafından World Wide Web'in (WWW) yaratılmasıyla icat edilmesi 1989 yılına kadar değildi.İnternetin günümüzde olduğu gibi bilgi depolama ve paylaşma ortamı olarak kullanılmaya başlaması ancak bu noktaya kadar mümkün olmuştur.

Alice'in arkadaş ağını bilgi işlem cihazlarıyla ilişkilendirelim. İnternet bu tür bir diyagramın çok daha büyük bir versiyonuna benziyor:

![image](https://github.com/user-attachments/assets/1d132f95-0c38-4f6f-80e6-11c91c65a1cc)

# Ağdaki Cihazları Tanımlama

İletişim kurmak ve düzeni sürdürmek için cihazların bir ağ üzerinde hem tanımlayıcı hem de tanımlanabilir olması gerekir.Her insanın kendine özgü bir dizi parmak izi vardır; bu da, isimlerini değiştirseler bile bunun arkasında hâlâ bir kimlik olduğu anlamına gelir. Cihazlar aynı şeye sahiptir: biri geçirgen olmak üzere iki tanımlama aracı. Bunlar:

* **Bir IP Adresi**
* **Medya Erişim Kontrolü (MAC) Adresi - bunun seri numarasına benzer olduğunu düşünün.**

## IP Adresleri

![image](https://github.com/user-attachments/assets/4019be94-6906-483d-9ac6-1fd3af4483d1)


IP adresi, dört sekizliye bölünmüş bir sayı kümesidir. Her sekizlinin değeri, cihazın ağdaki IP adresi olarak özetlenecektir.Burada anlaşılması gereken , IP adreslerinin cihazdan cihaza değişebileceği ancak aynı ağ içerisinde aynı anda birden fazla kez aktif olamayacağıdır.
IP Adresleri, protokoller olarak bilinen bir dizi standardı izler. Bu protokoller ağ oluşturmanın omurgasıdır ve birçok cihazı aynı dilde iletişim kurmaya zorlar.
Ancak cihazların hem özel hem de genel ağda olabileceğini unutmamalıyız. Nerede olduklarına bağlı olarak ne tür bir IP adresine sahip olduklarını belirleyecektir: genel veya özel bir IP adresi.

![image](https://github.com/user-attachments/assets/9fe5dd12-01ea-4241-ba10-b98cc07c9043)

Bu iki cihaz birbirleriyle iletişim kurmak için özel IP adreslerini kullanabilecek. Ancak bu cihazların herhangi birinden İnternet'e gönderilen tüm veriler aynı genel IP adresiyle tanımlanacaktır.
Giderek daha fazla cihaz birbirine bağlandıkça, halihazırda kullanımda olmayan bir genel adrese ulaşmak giderek zorlaşıyor.
Örneğin ağ dünyasının endüstri devlerinden Cisco, 2021 yılı sonuna kadar yaklaşık 50 milyar cihazın internete bağlı olacağını tahmin ediyordu. [Cisco,2021](https://www.cisco.com/c/dam/en_us/about/ac79/docs/innov/IoT_IBSG_0411FINAL.pdf
)

## MAC Adresleri

![image](https://github.com/user-attachments/assets/5f388ce4-025a-4852-92c2-08b34bd952d2)


Ağdaki cihazların tümü, cihazın anakartında bulunan bir mikroçip kartı olan fiziksel bir ağ arayüzüne sahip olacaktır.Bu ağ arayüzüne, oluşturulduğu fabrikada MAC (Medya Erişim Kontrolü) adresi adı verilen benzersiz bir adres atanmıştır.
MAC adresi, ikiye bölünmüş ve iki nokta üst üste ile ayrılmış on iki karakterli onaltılık bir sayıdır (bilgi işlemde sayıları temsil etmek için kullanılan on altı tabanlı bir numaralandırma sistemi).
Bu iki nokta üst üste ayırıcılar olarak kabul edilir. Örneğin, a4:c3:f0:85:ac:2d. İlk altı karakter ağ arayüzünü oluşturan şirketi temsil eder ve son altı karakter benzersiz bir sayıdır.

## Ping (ICMP)

Ping, elimizdeki en temel ağ araçlarından biridir. Ping, cihazlar arasındaki bağlantının performansını (örneğin, bağlantının var olup olmadığını veya güvenilir olup olmadığını) belirlemek için ICMP (İnternet Kontrol Mesajı Protokolü) paketlerini kullanır.
Cihazlar arasında dolaşan ICMP paketlerinin süresi, aşağıdaki ekran görüntüsünde olduğu gibi ping ile ölçülür. Bu ölçüm, ICMP'nin yankı paketi ve ardından ICMP'nin hedef cihazdan gelen yankı yanıtı kullanılarak yapılır.
Ping'ler, ev ağınız gibi bir ağdaki cihazlara veya web siteleri gibi kaynaklara karşı gerçekleştirilebilir.
Bu araç kolaylıkla kullanılabilir ve Linux ve Windows gibi İşletim Sistemlerine (OS) kurulu olarak gelir. Basit bir ping işleminin sözdizimi ping IP adresi veya web sitesi URL'sidir. Aşağıdaki ekran görüntüsünde bunu çalışırken görelim.

![image](https://github.com/user-attachments/assets/e04800a3-ff4a-4ba7-ab5c-ed98e1bf6b9a)

Burada özel adresi 192.168.1.254 olan bir cihaza ping atıyoruz. Ping bize altı ICMP paketi gönderdiğimizi ve bunların hepsinin ortalama 4,16 milisaniye sürede alındığını bildirdi.



