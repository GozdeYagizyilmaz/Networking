### Ağ Güvenliği, ağa bağlı verileri, uygulamaları, cihazları ve sistemleri korumaya yönelik bir dizi işlemdir. Siber güvenliğin önemli alt alanlarından biri olarak kabul edilir.Ağ erişilebilirliğini, bütünlüğünü, sürekliliğini ve güvenilirliğini sağlamak amacıyla mimari/altyapının sistem tasarımı, işletimi ve yönetimine odaklanır.Trafik analizi (genellikle Ağ Trafik Analizi olarak adlandırılır), Ağ Güvenliği alanının bir alt alanıdır ve temel odak noktası, sorunları ve anormallikleri belirlemek için ağ verilerini araştırmaktır.

## Ağ Güvenliği

Ağ Güvenliğinin temel ilgi alanı iki temel kavramdır: kimlik doğrulama ve yetkilendirme.Bu iki temel kavramın uygulanmasını sağlamak ve ölçmek ve bunun ötesine geçerek sürekliliği ve güvenilirliği sağlamak için çeşitli araçlar, teknolojiler ve yaklaşımlar mevcuttur.
Ağ güvenliği operasyonları, mümkün olan en yüksek güvenlik yönetimini sağlamak için üç temel kontrol seviyesi içerir.

**Temel Ağ Güvenlik Kontrol Seviyeleri:**

**1- Fiziksel** , Fiziksel güvenlik kontrolleri, ağ cihazlarına, kablo panolarına, kilitlere ve tüm bağlantılı bileşenlere yetkisiz fiziksel erişimi engeller.
**2- Teknik** , Veri güvenliği kontrolleri, tüneller kurmak ve güvenlik katmanları uygulamak gibi yöntemlerle ağ verilerine yetkisiz erişimi önler.
**3- İdari** , Yönetimsel güvenlik kontrolleri, politika oluşturma, erişim düzeyleri ve kimlik doğrulama süreçleri gibi güvenlik işlemlerinde tutarlılık sağlar.

### Bu kontrol seviyeleri altında iki ana yaklaşım ve birden fazla unsur bulunmaktadır. Ağ güvenliği operasyonlarında kullanılan en yaygın unsurlar aşağıda açıklanmıştır.

## Access Control(Erişim Kontrolü)
Ağ Güvenliğinin başlangıç ​​noktası. Kimlik doğrulama ve yetkilendirmeyi sağlamak için bir dizi kontroldür.

### Threat Control(Tehdit Kontrolü)
Ağdaki anormal/kötü niyetli aktiviteleri tespit etme ve engelleme. Hem dahili (güvenilir) hem de harici trafik verisi araştırmalarını içerir.

## Erişim Kontrolünün temel unsurları:

* **Firewall Protection - Güvenlik Duvarı Koruması:** Gelen ve giden ağ trafiğini önceden belirlenmiş güvenlik kurallarıyla kontrol eder. Meşru ve beklenen trafiğe izin verirken şüpheli/kötü amaçlı trafiği ve uygulama katmanı tehditlerini engellemek için tasarlanmıştır.
* **Network Access Control-Ağ Erişim Kontrolü (NAC):** Ağa erişimden önce cihazların uygunluğunu kontrol eder. Ağa bağlanmadan önce cihaz özelliklerinin ve koşullarının önceden belirlenmiş profille uyumlu olduğunu doğrulamak için tasarlanmıştır.
* **Identy and Access Management -Kimlik ve Erişim Yönetimi (IAM):** Ağ üzerinden varlık kimliklerini ve veri sistemlerine ve kaynaklara kullanıcı erişimini kontrol eder ve yönetir.
* **Load Balancing-Yük Dengeleme:** Kaynak kullanımını kontrol ederek görevleri bir dizi kaynağa dağıtır (ölçümlere göre) ve genel veri işleme akışını iyileştirir.
* **Network Segmention-Ağ Segmentasyonu:** Kullanıcıların erişim seviyelerini izole etmek, varlıkları ortak işlevlerle gruplamak ve hassas/dahili cihazların/verilerin daha güvenli bir ağda korunmasını iyileştirmek için ağ aralıklarını ve segmentasyonunu oluşturur ve kontrol eder.
* **Virtual Private Networks-Sanal Özel Ağlar (VPN):** Ağ üzerinden (internet üzerinden iletişimler dahil) cihazlar arasında şifreli iletişimi oluşturur ve kontrol eder (genellikle güvenli uzaktan erişim için).
* **Zero Trust Model-Sıfır Güven Modeli:** Erişim ve izinlerin en düşük seviyede yapılandırılmasını ve uygulanmasını (atanmış rolü yerine getirmek için gereken erişimi sağlayarak) önerir. Zihniyet şuna odaklanır: "Asla güvenme, her zaman doğrula".

## Tehdit Kontrolünün temel unsurları:

* **Intrusion Detection and Prevention (IDS/IPS)-Saldırı Algılama ve Önleme:** Trafiği denetler ve bir anormallik/tehdit algıladığında uyarılar oluşturur (IDS) veya bağlantıyı sıfırlar (IPS).
* **Data Loss Prevention- Veri Kaybı Önleme (DLP):** Trafiği denetler (kablodaki verilerin içerik denetimini ve bağlamsal analizini gerçekleştirir) ve hassas verilerin çıkarılmasını engeller.
* **Endpoint Protection-Uç Nokta Koruması:** Şifreleme, antivirüs, kötü amaçlı yazılımdan koruma, DLP ve IDS/IPS gibi çok katmanlı bir yaklaşım kullanarak ağa bağlanan her türlü uç noktayı ve cihazı koruma.
* **Cloud Security-Bulut Güvenliği:** VPN ve veri şifreleme gibi uygun karşı önlemleri uygulayarak bulut/çevrimiçi tabanlı sistem kaynaklarını tehditlerden ve veri sızıntısından korumak.
* **Security Information and Event Management (SIEM)-Güvenlik ve olay bilgisi yönetimi:** Olay ve bağlam analizini kullanarak anormallikleri, tehditleri ve güvenlik açıklarını tespit ederek mevcut veriler (kayıtlar ve trafik istatistikleri) aracılığıyla tehdit algılama, uyumluluk ve güvenlik olayı yönetimine yardımcı olan teknoloji.
* **Security Orchestration Automation and Response (SOAR)-Güvenlik orkestrasyonu otomasyonu ve yanıtı:** Tek bir platform içerisinde çeşitli kişiler, araçlar ve veriler arasında anormallikleri, tehditleri ve güvenlik açıklarını tespit etmek için görevlerin koordine edilmesine ve otomatikleştirilmesine yardımcı olan teknoloji.Ayrıca zafiyet yönetimi, olay müdahalesi ve güvenlik operasyonlarını da destekler.
* **Network Traffic Analysis & Network Detection and Response-Ağ Trafiği Analizi ve Ağ Algılama ve Tepkisi:** Anormallikleri ve tehditleri belirlemek için ağ trafiğini veya trafik yakalamalarını incelemek.

### Tipik Ağ Güvenlik Yönetimi İşlemi verilen tabloda açıklanmıştır:

![image](https://github.com/user-attachments/assets/a7881aa0-2d15-476d-99a2-c1944778991c)

## Yönetilen Güvenlik Hizmetleri
Her kuruluşun belirli güvenlik alanları için özel gruplar oluşturmak için yeterli kaynağı yoktur. Bunun birçok nedeni vardır: bütçe, çalışan beceri seti ve kuruluş büyüklüğü, güvenlik operasyonlarının nasıl ele alınacağını belirleyebilir.
Bu noktada, güvenlik ihtiyaçlarının sağlanması/artırılması için gereken çabayı yerine getirmek üzere Yönetilen Güvenlik Hizmetleri (MSS) devreye girmektedir. MSS'ler, servis sağlayıcılara dış kaynaklı olarak verilen hizmetlerdir.
Bu hizmet sağlayıcılarına Yönetilen Güvenlik Hizmet Sağlayıcıları (MSSP'ler) denir. Günümüzde, çoğu MSS zaman ve maliyet açısından etkilidir, şirket içinde veya dışarıdan kaynak alınarak yürütülebilir, katılımı kolaydır ve yönetim sürecini kolaylaştırır.MSS’nin çeşitli unsurları vardır ve en yaygın olanları aşağıda açıklanmıştır.

* **Ağ Penetrasyon Testi** Ağ güvenliğinin, ağa sızmak için kullanılan harici/dahili saldırgan tekniklerinin simüle edilmesi yoluyla değerlendirilmesi.
* **Güvenlik Açığı Değerlendirmesi** Ortamdaki güvenlik açıklarını keşfedip analiz ederek ağ güvenliğinin değerlendirilmesi.
* **Olay Müdahalesi** Güvenlik ihlallerini ele almak ve yönetmek için organize bir yaklaşım. Olayları tanımlamak, sınırlamak ve ortadan kaldırmak için bir dizi eylem içerir.
* **Davranış Analizi** Sistem ve kullanıcı davranışlarını ele almak, anormallikleri, tehditleri, güvenlik açıklarını ve saldırıları tespit etmek için belirli kalıplar için temel çizgiler ve trafik profilleri oluşturmak için organize bir yaklaşım.





