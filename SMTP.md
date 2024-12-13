### Web'de gezinmek ve dosya indirmek gibi, e-posta göndermek de kendi protokolüne ihtiyaç duyar. Basit Posta Aktarım Protokolü (SMTP), bir posta istemcisinin bir posta sunucusuyla ve bir posta sunucusunun başka biriyle nasıl iletişim kurduğunu tanımlar.

### SMTP protokolü için benzetme, bir paket göndermek için yerel postaneye gittiğiniz zamandır. Çalışanı selamlarsınız, paketinizi nereye göndermek istediğinizi söylersiniz ve paketi teslim etmeden önce göndericinin bilgilerini verirsiniz.Bulunduğunuz ülkeye bağlı olarak kimlik kartınızı göstermeniz istenebilir. Bu işlem bir SMTP oturumundan çok da farklı değildir.

E-posta istemcinizin bir e-postayı SMTP sunucusuna aktarırken kullandığı komutlardan bazılarını sunalım:

* **HELO** veya **EHLO**
* **MAIL FROM** gönderenin e-posta adresini belirtir
* **RCPT TO** alıcının e-posta adresini belirtir
* **DATA**, istemcinin e-posta mesajının içeriğini göndermeye başlayacağını belirtir
* **.** sonunu belirtmek için kendi başına bir satırda gönderilir

### SMTP sunucusu varsayılan olarak TCP port 25'i dinler.



